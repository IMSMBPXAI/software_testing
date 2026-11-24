# software_testing
for subject SOFTWARE TESTING 2/2026
#### **GROUP 2 ราชวงศ์คนส่งช้า**


---

### WORK 2 (23/11/2026)
> [LINK](https://docs.google.com/spreadsheets/d/1YeRQe2XnzSe2_zXn6VsFZrO4-R8I0vIG3lN9MCni_IA/edit?usp=sharing )


# Test Cases: Lab 2 GradeCalculator
 
| Req ID | Feature | Test Case |
|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | TC-01 – TC-21 (21 เคส) |
| R2 | คะแนน 0–49 ได้ F | TC-22 – TC-24 (3 เคส) |
| R3 | คะแนนติดลบ (< 0) ต้องโยน exception<br>คะแนนนอกช่วง (< 0 หรือ > 100) ต้องโยน exception | TC-25 – TC-26 (2 เคส) |
| R4 | Refactor แล้วผลลัพธ์ต้องไม่เปลี่ยน | TC-27 (1 เคส) |
 
## สรุปผลการทดสอบ
 
**ผลรวม: 27/27 ผ่าน**
 
**ผลการทดสอบ**
 
| Status | จำนวน |
|---|---|
| ผ่าน | 27 |
 
**ประเภท (Type)**
 
| Type | จำนวน |
|---|---|
| ปกติ | 9 |
| ขอบเขต | 16 |
| ผิดปกติ | 2 |
 
**เทคนิค (Technique)**
 
| Technique | จำนวน |
|---|---|
| EP | 8 |
| BVA | 18 |
| Use case | 1 |
 
**ความสำคัญ (Priority)**
 
| Priority | จำนวน |
|---|---|
| M | 8 |
| H | 19 |
 
## ตาราง Test Case ทั้งหมด
 
| TC ID | Req | Test Scenario | Type | Technique | Priority | Test Data | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|---|---|---|
| [TC-01](#tc-01) | R1 | คะแนนกลางช่วง A (80–100) | ปกติ | EP | M | `score = 85` | คืนค่า `"A"` | คืนค่า `"A"` | ✅ ผ่าน |
| [TC-02](#tc-02) | R1 | ขอบบนสุดของคะแนน (100) ได้ A | ขอบเขต | BVA | H | `score = 100` | — | คืนค่า `"A"` | ✅ ผ่าน |
| [TC-03](#tc-03) | R1 | ขอบล่างของช่วง A (80) | ขอบเขต | BVA | H | `score = 80` | คืนค่า `"A"` | คืนค่า `"A"` | ✅ ผ่าน |
| [TC-04](#tc-04) | R1 | ขอบบนของช่วง B+ (79) ต่ำกว่า A อยู่ 1 คะแนน | ขอบเขต | BVA | H | `score = 79` | คืนค่า `"B+"` | คืนค่า `"B+"` | ✅ ผ่าน |
| [TC-05](#tc-05) | R1 | คะแนนกลางช่วง B+ (75–79) | ปกติ | EP | M | `score = 77` | คืนค่า `"B+"` | คืนค่า `"B+"` | ✅ ผ่าน |
| [TC-06](#tc-06) | R1 | ขอบล่างของช่วง B+ (75) | ขอบเขต | BVA | H | `score = 75` | คืนค่า `"B+"` | คืนค่า `"B+"` | ✅ ผ่าน |
| [TC-07](#tc-07) | R1 | ขอบบนของช่วง B (74) | ขอบเขต | BVA | H | `score = 74` | คืนค่า `"B"` | คืนค่า `"B"` | ✅ ผ่าน |
| [TC-08](#tc-08) | R1 | คะแนนกลางช่วง B (70–74) | ปกติ | EP | M | `score = 72` | คืนค่า `"B"` | คืนค่า `"B"` | ✅ ผ่าน |
| [TC-09](#tc-09) | R1 | ขอบล่างของช่วง B (70) | ขอบเขต | BVA | H | `score = 70` | คืนค่า `"B"` | คืนค่า `"B"` | ✅ ผ่าน |
| [TC-10](#tc-10) | R1 | ขอบบนของช่วง C+ (69) | ขอบเขต | BVA | H | `score = 69` | คืนค่า `"C+"` | คืนค่า `"C+"` | ✅ ผ่าน |
| [TC-11](#tc-11) | R1 | คะแนนกลางช่วง C+ (65–69) | ปกติ | EP | M | `score = 67` | คืนค่า `"C+"` | คืนค่า `"C+"` | ✅ ผ่าน |
| [TC-12](#tc-12) | R1 | ขอบล่างของช่วง C+ (65) | ขอบเขต | BVA | H | `score = 65` | คืนค่า `"C+"` | คืนค่า `"C+"` | ✅ ผ่าน |
| [TC-13](#tc-13) | R1 | ขอบบนของช่วง C (64) | ขอบเขต | BVA | H | `score = 64` | คืนค่า `"C"` | คืนค่า `"C"` | ✅ ผ่าน |
| [TC-14](#tc-14) | R1 | คะแนนกลางช่วง C (60–64) | ปกติ | EP | M | `score = 62` | คืนค่า `"C"` | คืนค่า `"C"` | ✅ ผ่าน |
| [TC-15](#tc-15) | R1 | ขอบล่างของช่วง C (60) | ขอบเขต | BVA | H | `score = 60` | คืนค่า `"C"` | คืนค่า `"C"` | ✅ ผ่าน |
| [TC-16](#tc-16) | R1 | ขอบบนของช่วง D+ (59) | ขอบเขต | BVA | H | `score = 59` | คืนค่า `"D+"` | คืนค่า `"D+"` | ✅ ผ่าน |
| [TC-17](#tc-17) | R1 | คะแนนกลางช่วง D+ (55–59) | ปกติ | EP | M | `score = 57` | คืนค่า `"D+"` | คืนค่า `"D+"` | ✅ ผ่าน |
| [TC-18](#tc-18) | R1 | ขอบล่างของช่วง D+ (55) | ขอบเขต | BVA | H | `score = 55` | คืนค่า `"D+"` | คืนค่า `"D+"` | ✅ ผ่าน |
| [TC-19](#tc-19) | R1 | ขอบบนของช่วง D (54) | ขอบเขต | BVA | H | `score = 54` | คืนค่า `"D"` | คืนค่า `"D"` | ✅ ผ่าน |
| [TC-20](#tc-20) | R1 | คะแนนกลางช่วง D (50–54) | ปกติ | EP | M | `score = 52` | คืนค่า `"D"` | คืนค่า `"D"` | ✅ ผ่าน |
| [TC-21](#tc-21) | R1 | ขอบล่างของช่วง D (50) ต่ำสุดที่ยังไม่ติด F | ขอบเขต | BVA | H | `score = 50` | คืนค่า `"D"` | คืนค่า `"D"` | ✅ ผ่าน |
| [TC-22](#tc-22) | R2 | ขอบบนของช่วง F (49) ต่ำกว่า D อยู่ 1 คะแนน | ขอบเขต | BVA | H | `score = 49` | คืนค่า `"F"` | คืนค่า `"F"` | ✅ ผ่าน |
| [TC-23](#tc-23) | R2 | คะแนนกลางช่วง F (0–49) | ปกติ | EP | M | `score = 25` | คืนค่า `"F"` | คืนค่า `"F"` | ✅ ผ่าน |
| [TC-24](#tc-24) | R2 | ขอบล่างสุดของคะแนนที่ถูกต้อง (0) | ขอบเขต | BVA | H | `score = 0` | คืนค่า `"F"` | คืนค่า `"F"` | ✅ ผ่าน |
| [TC-25](#tc-25) | R3 | คะแนน -1 (ต่ำกว่า 0 อยู่ 1) | ผิดปกติ | BVA | H | `score = -1` | โยน `IllegalArgumentException` (ไม่คืนเกรด) | โยน `IllegalArgumentException: "score must be 0-100"` | ✅ ผ่าน |
| [TC-26](#tc-26) | R3 | คะแนน 101 (เกิน 100 อยู่ 1) | ผิดปกติ | BVA | H | `score = 101` | โยน `IllegalArgumentException` (ไม่คืนเกรด) | โยน `IllegalArgumentException: "score must be 0-100"` | ✅ ผ่าน |
| [TC-27](#tc-27) | R4 | รันเทสต์ทั้งหมดหลัง Refactor<br>(MIN/GRADE + loop) ต้อง GREEN ทุกตัว | ปกติ | Use case | H | ชุดเทสต์ทั้งหมดในชีต TDD<br>(gradeOf100ReturnsA<br>... scoreBelowZeroThrows) | ทุกเทสต์ผ่าน ไม่มีตัวใดแดง | ผ่านครบทุกตัว | ✅ ผ่าน |
 
## รายละเอียดแต่ละ Test Case
 
### TC-01
 
**คะแนนกลางช่วง A (80–100)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ปกติ | EP | M | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 85`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(85)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("A", calc.gradeOf(85))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"A"` | คืนค่า `"A"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-02
 
**ขอบบนสุดของคะแนน (100) ได้ A**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ขอบเขต | BVA | H | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 100`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(100)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("A", calc.gradeOf(100))`
| Expected Result | Actual Result |
|---|---|
| — | คืนค่า `"A"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-03
 
**ขอบล่างของช่วง A (80)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ขอบเขต | BVA | H | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 80`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(80)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("A", calc.gradeOf(80))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"A"` | คืนค่า `"A"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-04
 
**ขอบบนของช่วง B+ (79) ต่ำกว่า A อยู่ 1 คะแนน**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ขอบเขต | BVA | H | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 79`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(79)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("B+", calc.gradeOf(79))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"B+"` | คืนค่า `"B+"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-05
 
**คะแนนกลางช่วง B+ (75–79)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ปกติ | EP | M | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 77`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(77)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("B+", calc.gradeOf(77))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"B+"` | คืนค่า `"B+"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-06
 
**ขอบล่างของช่วง B+ (75)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ขอบเขต | BVA | H | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 75`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(75)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("B+", calc.gradeOf(75))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"B+"` | คืนค่า `"B+"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-07
 
**ขอบบนของช่วง B (74)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ขอบเขต | BVA | H | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 74`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(74)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("B", calc.gradeOf(74))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"B"` | คืนค่า `"B"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-08
 
**คะแนนกลางช่วง B (70–74)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ปกติ | EP | M | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 72`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(72)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("B", calc.gradeOf(72))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"B"` | คืนค่า `"B"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-09
 
**ขอบล่างของช่วง B (70)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ขอบเขต | BVA | H | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 70`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(70)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("B", calc.gradeOf(70))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"B"` | คืนค่า `"B"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-10
 
**ขอบบนของช่วง C+ (69)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ขอบเขต | BVA | H | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 69`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(69)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("C+", calc.gradeOf(69))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"C+"` | คืนค่า `"C+"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-11
 
**คะแนนกลางช่วง C+ (65–69)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ปกติ | EP | M | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 67`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(67)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("C+", calc.gradeOf(67))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"C+"` | คืนค่า `"C+"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-12
 
**ขอบล่างของช่วง C+ (65)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ขอบเขต | BVA | H | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 65`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(65)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("C+", calc.gradeOf(65))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"C+"` | คืนค่า `"C+"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-13
 
**ขอบบนของช่วง C (64)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ขอบเขต | BVA | H | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 64`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(64)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("C", calc.gradeOf(64))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"C"` | คืนค่า `"C"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-14
 
**คะแนนกลางช่วง C (60–64)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ปกติ | EP | M | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 62`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(62)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("C", calc.gradeOf(62))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"C"` | คืนค่า `"C"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-15
 
**ขอบล่างของช่วง C (60)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ขอบเขต | BVA | H | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 60`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(60)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("C", calc.gradeOf(60))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"C"` | คืนค่า `"C"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-16
 
**ขอบบนของช่วง D+ (59)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ขอบเขต | BVA | H | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
 
**Test Data**
 
`score = 59`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(59)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("D+", calc.gradeOf(59))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"D+"` | คืนค่า `"D+"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-17
 
**คะแนนกลางช่วง D+ (55–59)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ปกติ | EP | M | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 57`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(57)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("D+", calc.gradeOf(57))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"D+"` | คืนค่า `"D+"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-18
 
**ขอบล่างของช่วง D+ (55)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ขอบเขต | BVA | H | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 55`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(55)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("D+", calc.gradeOf(55))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"D+"` | คืนค่า `"D+"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-19
 
**ขอบบนของช่วง D (54)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ขอบเขต | BVA | H | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 54`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(54)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("D", calc.gradeOf(54))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"D"` | คืนค่า `"D"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-20
 
**คะแนนกลางช่วง D (50–54)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ปกติ | EP | M | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 52`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(52)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("D", calc.gradeOf(52))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"D"` | คืนค่า `"D"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-21
 
**ขอบล่างของช่วง D (50) ต่ำสุดที่ยังไม่ติด F**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R1 | แปลงคะแนน 50–100 เป็นเกรด A–D | ขอบเขต | BVA | H | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 50`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(50)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("D", calc.gradeOf(50))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"D"` | คืนค่า `"D"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-22
 
**ขอบบนของช่วง F (49) ต่ำกว่า D อยู่ 1 คะแนน**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R2 | คะแนน 0–49 ได้ F | ขอบเขต | BVA | H | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 49`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(49)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("F", calc.gradeOf(49))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"F"` | คืนค่า `"F"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-23
 
**คะแนนกลางช่วง F (0–49)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R2 | คะแนน 0–49 ได้ F | ปกติ | EP | M | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 25`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(25)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("F", calc.gradeOf(25))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"F"` | คืนค่า `"F"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-24
 
**ขอบล่างสุดของคะแนนที่ถูกต้อง (0)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R2 | คะแนน 0–49 ได้ F | ขอบเขต | BVA | H | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 0`
 
**Test Steps**
 
1. เรียก `calc.gradeOf(0)`
2. ตรวจค่าที่ได้ด้วย `assertEquals("F", calc.gradeOf(0))`
| Expected Result | Actual Result |
|---|---|
| คืนค่า `"F"` | คืนค่า `"F"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-25
 
**คะแนน -1 (ต่ำกว่า 0 อยู่ 1)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R3 | คะแนนติดลบ (< 0) ต้องโยน exception | ผิดปกติ | BVA | H | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = -1`
 
**Test Steps**
 
1. ใส่ `@Test(expected = IllegalArgumentException.class)`
2. เรียก `calc.gradeOf(-1)`
| Expected Result | Actual Result |
|---|---|
| โยน `IllegalArgumentException` (ไม่คืนเกรด) | โยน `IllegalArgumentException: "score must be 0-100"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-26
 
**คะแนน 101 (เกิน 100 อยู่ 1)**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R3 | คะแนนนอกช่วง (< 0 หรือ > 100) ต้องโยน exception | ผิดปกติ | BVA | H | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
`score = 101`
 
**Test Steps**
 
1. เขียนเทสต์ `@Test(expected = IllegalArgumentException.class)`
2. เรียก `calc.gradeOf(101)`
3. ตรวจว่ามี exception ถูกโยนออกมา
| Expected Result | Actual Result |
|---|---|
| โยน `IllegalArgumentException` (ไม่คืนเกรด) | โยน `IllegalArgumentException: "score must be 0-100"` |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
### TC-27
 
**รันเทสต์ทั้งหมดหลัง Refactor (MIN/GRADE + loop) ต้อง GREEN ทุกตัว**
 
| Req ID | Feature | Type | Technique | Priority | Status |
|---|---|---|---|---|---|
| R4 | Refactor แล้วผลลัพธ์ต้องไม่เปลี่ยน | ปกติ | Use case | H | ✅ ผ่าน |
 
**Preconditions**
 
1. มีคลาส GradeCalculator เวอร์ชันหลัง Refactor (ตาราง MIN/GRADE + loop) ที่ compile ได้
2. ใช้ JUnit 4.13.2
3. `@Before` สร้าง `calc = new GradeCalculator()` ใหม่ทุกเทสต์
**Test Data**
 
ชุดเทสต์ทั้งหมดในชีต TDD (gradeOf100ReturnsA ... scoreBelowZeroThrows)
 
**Test Steps**
 
1. Refactor โค้ดตาม TDD รอบ 11 (ย้ายเกณฑ์ไปไว้ใน array MIN และ GRADE แล้วใช้ loop)
2. รันคลาสเทสต์ทั้งหมดด้วย JUnit 4.13.2
3. ตรวจผลรัน
| Expected Result | Actual Result |
|---|---|
| ทุกเทสต์ผ่าน ไม่มีตัวใดแดง | ผ่านครบทุกตัว |
 
Tester: ปานชนก พรหมศรีสวัสดิ์ 68026484 · Test Date: 2026-11-23 · Defect ID: —
 
[↑ กลับไปตาราง](#ตาราง-test-case-ทั้งหมด)
 
---
 
