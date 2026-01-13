# JavaScript Fundamentals – Code Explanation & Output

ไฟล์นี้อธิบายการทำงานของโค้ดในแต่ละ Activity พร้อมตัวอย่างผลลัพธ์ (Output) ที่ได้จากการรันด้วย Node.js

---

## 1️⃣ 01-variables.js

### 6. Challenge: Create a Person Object

**โค้ดหลัก**

* สร้าง object ชื่อ `student` ซึ่งประกอบด้วย

  * properties: `firstName`, `lastName`, `age`, `gpa`, `courses`, `isActive`
  * methods: `getFullName()` และ `getInfo()`
* ใช้ `this` เพื่ออ้างอิงข้อมูลภายใน object เดียวกัน

**การทำงาน**

* `getFullName()` คืนค่า string ของชื่อ–นามสกุล
* `getInfo()` เรียก `getFullName()` แล้วรวมข้อมูลอายุและเกรดเฉลี่ย

**ตัวอย่างผลลัพธ์**

```text
Full name: Alice Smith
Info: Alice Smith, Age: 20, GPA: 3.8
Courses: HTML, CSS, JavaScript
```

---

## 2️⃣ 02-functions.js

### 8. Returning Objects

**โค้ดหลัก**

* ฟังก์ชัน `createUser()` คืนค่า object
* ใช้ shorthand property (`firstName, lastName, age`)
* มี method ภายใน object เช่น `getFullName()`

**การทำงาน**

* เมื่อเรียก `createUser("John", "Doe", 30)` จะได้ object ใหม่
* สามารถเรียกใช้ property และ method ได้ทันที

**ตัวอย่างผลลัพธ์**

```text
Email: john.doe@example.com
Full name: John Doe
```

---

### 9. Function as Parameter (Callback)

**โค้ดหลัก**

* ฟังก์ชัน `processArray(arr, callback)` รับฟังก์ชันเป็นพารามิเตอร์
* ใช้ callback ประมวลผลแต่ละค่าใน array

**การทำงาน**

* ส่ง arrow function `(x) => x * 2` เพื่อคูณสอง
* ส่ง `(x) => x * x` เพื่อยกกำลังสอง

**ตัวอย่างผลลัพธ์**

```text
Original: [1,2,3,4,5]
Doubled: [2,4,6,8,10]
Squared: [1,4,9,16,25]
```

---

## 3️⃣ 03-control-flow.js

### 5. Short-Circuit Evaluation

**โค้ดหลัก**

* ใช้ `||` เพื่อเลือกค่าที่เป็น truthy ตัวแรก
* ใช้ optional chaining `?.` เพื่อป้องกัน error จาก null/undefined

**การทำงาน**

* `admin?.name` คืนค่า `undefined` เพราะ admin เป็น `null`
* JavaScript จึงไปใช้ `user.name` แทน

**ตัวอย่างผลลัพธ์**

```text
User name: John
```

---

### 7. Form Validation

**โค้ดหลัก**

* ฟังก์ชัน `validateRegistration(formData)` ตรวจสอบข้อมูลทีละเงื่อนไข
* เก็บ error ไว้ใน array `errors`

**การทำงาน**

* ถ้า `errors.length === 0` → valid
* ถ้ามี error → invalid พร้อมข้อความแจ้งเตือน

**ตัวอย่างผลลัพธ์**

```text
Valid user: { isValid: true, errors: [] }
Invalid user: { isValid: false, errors: [...] }
```

---

## 4️⃣ 04-loops.js

### 9. Chaining Methods

**โค้ดหลัก**

* ใช้ `filter → map → join` ต่อกันในบรรทัดเดียว

**การทำงาน**

1. `filter` เลือกเลขคู่
2. `map` แปลงเป็นข้อความยกกำลังสอง
3. `join` รวมเป็น string เดียว

**ตัวอย่างผลลัพธ์**

```text
Even numbers squared: 2²=4, 4²=16, 6²=36, 8²=64, 10²=100
```

---

### 10. Challenge: Student Grades

**โค้ดหลัก**

* ใช้ `map` ดึงชื่อ
* ใช้ `filter` เลือกคะแนนสูง
* ใช้ `reduce` หา average และ top scorer
* ใช้ `sort` เรียงคะแนน

**ตัวอย่างผลลัพธ์**

```text
Class average: 87.00
Top scorer: Alice (95)
Alice: 95 (A)
Diana: 92 (A)
Eve: 88 (B)
```

---

## 5️⃣ 05-integration.js

### Quiz Application

**โค้ดหลัก**

* เก็บคำถามใน array `quizzes`
* สุ่มคำตอบผู้ใช้ด้วย `Math.random()`
* ตรวจสอบความถูกต้อง และเก็บผลใน `results`

**การทำงาน**

1. วนลูปคำถามด้วย `forEach`
2. เปรียบเทียบคำตอบผู้ใช้กับคำตอบที่ถูก
3. คำนวณคะแนนและเกรด
4. สรุปสถิติด้วย `filter` และ `reduce`

**ตัวอย่างผลลัพธ์**

```text
FINAL SCORE: 3/5 (60.0%)
GRADE: D
Correct: 3
Incorrect: 2
```

---

✅ ไฟล์นี้สามารถเปิดอ่านได้โดยตรงบน GitHub เพื่อทำความเข้าใจโค้ดและผลลัพธ์ของแต่ละ Activity
