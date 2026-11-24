# TDD Log: Lab 2 GradeCalculator
 
> วงจร TDD: 🔴 **RED** เขียนเทสต์ก่อนแล้วรันให้เห็นว่าแดง → 🟢 **GREEN** เขียนโค้ดน้อยที่สุดให้ผ่าน → 🔵 **REFACTOR** ปรับโค้ดให้ดีขึ้นโดยเทสต์ยังผ่านทั้งหมด
 
## สรุปทุกรอบ
 
| รอบ | เทสต์ที่เพิ่ม | 🔴 RED | 🟢 GREEN |
|---|---|---|---|
| [1](#รอบที่-1) | `gradeOf100ReturnsA`, `gradeOf80ReturnsA` | ✘ แดง 2 เทสต์ | ✔ ผ่าน |
| [2](#รอบที่-2) | `gradeOf75ReturnsBPlus` | ✘ แดง 1 เทสต์ | ✔ ผ่าน |
| [3](#รอบที่-3) | `gradeOf70ReturnsB` | ✘ แดง 1 เทสต์ | ✔ ผ่าน |
| [4](#รอบที่-4) | `gradeOf65ReturnsCPlus` | ✘ แดง 1 เทสต์ | ✔ ผ่าน |
| [5](#รอบที่-5) | `gradeOf60ReturnsC` | ✘ แดง 1 เทสต์ | ✔ ผ่าน |
| [6](#รอบที่-6) | `gradeOf55ReturnsDPlus` | ✘ แดง 1 เทสต์ | ✔ ผ่าน |
| [7](#รอบที่-7) | `gradeOf50ReturnsD` | ✘ แดง 1 เทสต์ | ✔ ผ่าน |
| [8](#รอบที่-8) | `gradeOf49ReturnsF`, `gradeOf0ReturnsF` | ✘ แดง 2 เทสต์ | ✔ ผ่าน |
| [9](#รอบที่-9) | `scoreAboveHundredThrows` | ✘ แดง 1 เทสต์ | ✔ ผ่าน |
| [10](#รอบที่-10) | `scoreBelowZeroThrows` | ✘ แดง 1 เทสต์ | ✔ ผ่าน |
| [11](#รอบที่-11) | — (Refactor ไม่เพิ่มเทสต์) | — | ✔ ผ่านทั้งหมด |
 
---
 
## รอบที่ 1
 
### 🔴 RED
 
ไฟล์ GradeCalculator.java:
 
```java
public class GradeCalculator {
    public String gradeOf(int score) {
        return null;
    }
}
```
 
เทสต์ที่เพิ่มใน GradeCalculatorTest.java:
 
```java
@Test
public void gradeOf100ReturnsA() {
    assertEquals("A", calc.gradeOf(100));
}
 
@Test
public void gradeOf80ReturnsA() {
    assertEquals("A", calc.gradeOf(80));
}
```
 
ผลรัน:
 
```text
✘ gradeOf100ReturnsA
   expected:<A> but was:<null>
✘ gradeOf80ReturnsA
   expected:<A> but was:<null>
```
 
### 🟢 GREEN
 
GradeCalculator.java:
 
```java
public class GradeCalculator {
    public String gradeOf(int score) {
        return "A";
    }
}
```
 
ผลรัน:
 
```text
✔ gradeOf100ReturnsA
✔ gradeOf80ReturnsA
```
 
### 💡 Learning
 
เป็นรอบแรกเขียนเทสต์ก่อนที่จะมีโค้ดจริง พอรันแล้วแดงตามสไลด์ (expected:<A> but was:<null>) ก็เข้าใจว่า RED มีไว้พิสูจน์ว่าเทสต์จับความผิดได้จริง
 
ตอน GREEN ลอง return A ตรง ๆ ตามที่อาจารย์บอกว่าให้เขียนโค้ดน้อยที่สุด ถึงจะรู้ยังไม่ถูกต้อง แต่ 2 เทสต์ก็ผ่าน ส่วนที่เหลือยังต้องเรียนรู้และแก้แต่
 
[↑ กลับไปสรุปทุกรอบ](#สรุปทุกรอบ)
 
---
 
## รอบที่ 2
 
### 🔴 RED
 
เทสต์ที่เพิ่มใน GradeCalculatorTest.java:
 
```java
@Test
public void gradeOf75ReturnsBPlus() {
    assertEquals("B+", calc.gradeOf(75));
}
```
 
ผลรัน:
 
```text
✘ gradeOf75ReturnsBPlus
   expected:<[B+]> but was:<[A]>
```
 
### 🟢 GREEN
 
GradeCalculator.java:
 
```java
public class GradeCalculator {
    public String gradeOf(int score) {
        if (score >= 80) return "A";
        return "B+";
    }
}
```
 
ผลรัน:
 
```text
✔ gradeOf100ReturnsA
✔ gradeOf80ReturnsA
✔ gradeOf75ReturnsBPlus
```
 
### 💡 Learning
 
พอเพิ่มเทสต์ 75 → B+ โค้ดที่ return แค่ "A" อย่างเดียวก็พังทัน เลยต้องกลับมาเขียนเงื่อนไขเพิ่ม เพิ่ม if ตัวแรกที่ if (score >= 80) return "A"; ตามโจทย์เงื่อนไขในสไลด์ก่อน เพื่อให้ไม่พังทั้ง A และ B
 
[↑ กลับไปสรุปทุกรอบ](#สรุปทุกรอบ)
 
---
 
## รอบที่ 3
 
### 🔴 RED
 
เทสต์ที่เพิ่มใน GradeCalculatorTest.java:
 
```java
@Test
public void gradeOf70ReturnsB() {
    assertEquals("B", calc.gradeOf(70));
}
```
 
ผลรัน:
 
```text
✘ gradeOf70ReturnsB
   expected:<B[]> but was:<B[+]>
```
 
### 🟢 GREEN
 
GradeCalculator.java:
 
```java
public class GradeCalculator {
    public String gradeOf(int score) {
        if (score >= 80) return "A";
        if (score >= 75) return "B+";
        return "B";
    }
}
```
 
ผลรัน:
 
```text
✔ gradeOf100ReturnsA
✔ gradeOf80ReturnsA
✔ gradeOf75ReturnsBPlus
✔ gradeOf70ReturnsB
```
 
### 💡 Learning
 
ลองเทสต์ 70 แล้วได้ B+ แปลว่าต้องเพิ่มเงื่อนไขของ B+ เข้ามาให้ตรงตามเงื่อนไขที่โ๗ทย์กำหนด เลยเพิ่ม if อีกตัว ไม่งั้นมันก็จะอกมาเป็น B+ ทั้งหมด ต่อให้ได้แค่ 1 ก็ตาม
 
[↑ กลับไปสรุปทุกรอบ](#สรุปทุกรอบ)
 
---
 
## รอบที่ 4
 
### 🔴 RED
 
เทสต์ที่เพิ่มใน GradeCalculatorTest.java:
 
```java
@Test
public void gradeOf65ReturnsCPlus() {
    assertEquals("C+", calc.gradeOf(65));
}
```
 
ผลรัน:
 
```text
✘ gradeOf65ReturnsCPlus
   expected:<[C+]> but was:<[B]>
```
 
### 🟢 GREEN
 
GradeCalculator.java:
 
```java
public class GradeCalculator {
    public String gradeOf(int score) {
        if (score >= 80) return "A";
        if (score >= 75) return "B+";
        if (score >= 70) return "B";
        return "C+";
    }
}
```
 
ผลรัน:
 
```text
✔ gradeOf100ReturnsA
✔ gradeOf80ReturnsA
✔ gradeOf75ReturnsBPlus
✔ gradeOf70ReturnsB
✔ gradeOf65ReturnsCPlus
```
 
### 💡 Learning
 
เริ่มจับจังหวะได้ในแต่ละรอบการเทสว่า ถ้าเพิ่มเทสต์ 1 ตัว → แดง ก็ให้เพิ่ม if 1 บรรทัด → เขียว ทันที แล้วทำวนไปเรื่อยๆ ค่อยๆ เพิ่มเงื่อนไขไปทีละตัวตามโจทย์
 
[↑ กลับไปสรุปทุกรอบ](#สรุปทุกรอบ)
 
---
 
## รอบที่ 5
 
### 🔴 RED
 
เทสต์ที่เพิ่มใน GradeCalculatorTest.java:
 
```java
@Test
public void gradeOf60ReturnsC() {
    assertEquals("C", calc.gradeOf(60));
}
```
 
ผลรัน:
 
```text
✘ gradeOf60ReturnsC
   expected:<C[]> but was:<C[+]>
```
 
### 🟢 GREEN
 
GradeCalculator.java:
 
```java
public class GradeCalculator {
    public String gradeOf(int score) {
        if (score >= 80) return "A";
        if (score >= 75) return "B+";
        if (score >= 70) return "B";
        if (score >= 65) return "C+";
        return "C+";
        return "C";
    }
}
```
 
ผลรัน:
 
```text
✔ gradeOf100ReturnsA
✔ gradeOf80ReturnsA
✔ gradeOf75ReturnsBPlus
✔ gradeOf70ReturnsB
✔ gradeOf65ReturnsCPlus
✔ gradeOf60ReturnsC
```
 
### 💡 Learning
 
เลือกเทสต์ 60 ที่เป็นขอบล่างของ C แทนค่ากลางด้วย 62 เพราะในคาบบอกว่า bug มักอยู่ที่ขอบ เช่นพิมพ์ > แทน >= ถ้าเทสต์แค่ค่ากลางจะจับไม่ได้
 
[↑ กลับไปสรุปทุกรอบ](#สรุปทุกรอบ)
 
---
 
## รอบที่ 6
 
### 🔴 RED
 
เทสต์ที่เพิ่มใน GradeCalculatorTest.java:
 
```java
@Test
public void gradeOf55ReturnsDPlus() {
    assertEquals("D+", calc.gradeOf(55));
}
```
 
ผลรัน:
 
```text
✘ gradeOf55ReturnsDPlus
   expected:<[D+]> but was:<[C]>
```
 
### 🟢 GREEN
 
GradeCalculator.java:
 
```java
public class GradeCalculator {
    public String gradeOf(int score) {
        if (score >= 80) return "A";
        if (score >= 75) return "B+";
        if (score >= 70) return "B";
        if (score >= 65) return "C+";
        if (score >= 60) return "C";
        return "D+";
    }
}
```
 
ผลรัน:
 
```text
gradeOf100ReturnsA
✔ gradeOf80ReturnsA
✔ gradeOf75ReturnsBPlus
✔ gradeOf70ReturnsB
✔ gradeOf65ReturnsCPlus
✔ gradeOf60ReturnsC
✔ gradeOf55ReturnsDPlus
```
 
### 💡 Learning
 
if ของเงื่อนไขตามโจทย์เริ่มเรียงซ้ำยาวขึ้นเรื่อย ๆ น่าจะ refactor ได้ แต่ฟีเจอร์ยังไม่ครบ
 
[↑ กลับไปสรุปทุกรอบ](#สรุปทุกรอบ)
 
---
 
## รอบที่ 7
 
### 🔴 RED
 
เทสต์ที่เพิ่มใน GradeCalculatorTest.java:
 
```java
@Test
public void gradeOf50ReturnsD() {
    assertEquals("D", calc.gradeOf(50));
}
```
 
ผลรัน:
 
```text
✘ gradeOf50ReturnsD
   expected:<D[]> but was:<D[+]>
```
 
### 🟢 GREEN
 
GradeCalculator.java:
 
```java
public class GradeCalculator {
    public String gradeOf(int score) {
        if (score >= 80) return "A";
        if (score >= 75) return "B+";
        if (score >= 70) return "B";
        if (score >= 65) return "C+";
        if (score >= 60) return "C";
        if (score >= 55) return "D+";
        return "D";
    }
}
```
 
ผลรัน:
 
```text
✔ gradeOf50ReturnsD
```
 
### 💡 Learning
 
พอตั้งชื่อเทสต์แบบ gradeOf50ReturnsD อ่านชื่อแล้วก็รู้ได้ทันทีเลยว่ากำลงัจะทดสอบอะไร ตอนเทสต์พังก็รู้ทันทีว่าช่วงคะแนนไหนผิด ต้องแก้หรือเพิ่มเงื่อนไข if ที่ตรงไหน
 
[↑ กลับไปสรุปทุกรอบ](#สรุปทุกรอบ)
 
---
 
## รอบที่ 8
 
### 🔴 RED
 
เทสต์ที่เพิ่มใน GradeCalculatorTest.java:
 
```java
@Test
public void gradeOf49ReturnsF() {
    assertEquals("F", calc.gradeOf(49));
}
@Test
public void gradeOf0ReturnsF() {
    assertEquals("F", calc.gradeOf(0));
}
```
 
ผลรัน:
 
```text
✘ gradeOf49ReturnsF
   expected:<[F]> but was:<[D]>
✘ gradeOf0ReturnsF
   expected:<[F]> but was:<[D]>
```
 
### 🟢 GREEN
 
GradeCalculator.java:
 
```java
public class GradeCalculator {
    public String gradeOf(int score) {
        if (score >= 80) return "A";
        if (score >= 75) return "B+";
        if (score >= 70) return "B";
        if (score >= 65) return "C+";
        if (score >= 60) return "C";
        if (score >= 55) return "D+";
        if (score >= 50) return "D";
        return "F";
    }
}
```
 
ผลรัน:
 
```text
✔ gradeOf49ReturnsF
✔ gradeOf0ReturnsF
```
 
### 💡 Learning
 
รอบนี้เพิ่ม 2 เทสต์ทีเดียว คือเพิ่ม 49 กับ 0 เพราะเป็นช่วงเดียวกันคือ F: 49 = ขอบบนของ F ติดกับ D, 0 = ขอบล่างสุดของคะแนนที่ถูกต้อง
 
[↑ กลับไปสรุปทุกรอบ](#สรุปทุกรอบ)
 
---
 
## รอบที่ 9
 
### 🔴 RED
 
เทสต์ที่เพิ่มใน GradeCalculatorTest.java:
 
```java
@Test(expected = IllegalArgumentException.class)
public void scoreAboveHundredThrows() {
    calc.gradeOf(101);
}
```
 
ผลรัน:
 
```text
✘ scoreAboveHundredThrows
   Expected exception: java.lang.IllegalArgumentException
```
 
### 🟢 GREEN
 
GradeCalculator.java:
 
```java
public class GradeCalculator {
    public String gradeOf(int score) {
        if (score > 100) {
            throw new IllegalArgumentException("score must be 0-100");
        }
        if (score >= 80) return "A";
        if (score >= 75) return "B+";
        if (score >= 70) return "B";
        if (score >= 65) return "C+";
        if (score >= 60) return "C";
        if (score >= 55) return "D+";
        if (score >= 50) return "D";
        return "F";
    }
}
```
 
ผลรัน:
 
```text
✔ scoreAboveHundredThrows
```
 
### 💡 Learning
 
ลองเทสต์ exception ตามโจทย์ดู แล้วต้องกำหนดให้ ถ้า คะแนน > 100 ต้องโยนออกมาเป็นค่า throw new IllegalArgumentException("score must be 0-100")
 
[↑ กลับไปสรุปทุกรอบ](#สรุปทุกรอบ)
 
---
 
## รอบที่ 10
 
### 🔴 RED
 
เทสต์ที่เพิ่มใน GradeCalculatorTest.java:
 
```java
@Test(expected = IllegalArgumentException.class)
public void scoreBelowZeroThrows() {
    calc.gradeOf(-1);
}
```
 
ผลรัน:
 
```text
✘ scoreBelowZeroThrows
   Expected exception: java.lang.IllegalArgumentException
```
 
### 🟢 GREEN
 
GradeCalculator.java:
 
```java
public class GradeCalculator {
    public String gradeOf(int score) {
        if (score < 0 || score > 100) {
            throw new IllegalArgumentException("score must be 0-100");
        }
        if (score >= 80) return "A";
        if (score >= 75) return "B+";
        if (score >= 70) return "B";
        if (score >= 65) return "C+";
        if (score >= 60) return "C";
        if (score >= 55) return "D+";
        if (score >= 50) return "D";
        return "F";
    }
}
```
 
ผลรัน:
 
```text
✔ scoreBelowZeroThrows
```
 
### 💡 Learning
 
เทส exception ตามโจทย์อีกตัว คือ -1 เดิมได้ "F" เพราะตกลงมาถึง return "F" จากคำสั่งเพิ่มที่ไม่ได้กำหนดเงื่อนไขของ F เอาไว้เลยแดง แก้เป็น score < 0 || score > 100 รวมไว้ที่เดียว
 
[↑ กลับไปสรุปทุกรอบ](#สรุปทุกรอบ)
 
---
 
## รอบที่ 11
 
### 🔵 REFACTOR
 
**ก่อน Refactor**
 
GradeCalculator.java:
 
```java
public class GradeCalculator {
    public String gradeOf(int score) {
        if (score < 0 || score > 100) {
            throw new IllegalArgumentException("score must be 0-100");
        }
        if (score >= 80) return "A";
        if (score >= 75) return "B+";
        if (score >= 70) return "B";
        if (score >= 65) return "C+";
        if (score >= 60) return "C";
        if (score >= 55) return "D+";
        if (score >= 50) return "D";
        return "F";
    }
}
```
 
**หลัง Refactor**
 
GradeCalculator.java:
 
```java
public class GradeCalculator {
    private static final int[] MIN =
        {80, 75, 70, 65, 60, 55, 50};
    private static final String[] GRADE =
        {"A", "B+", "B", "C+", "C", "D+", "D"};
 
    public String gradeOf(int score) {
        if (score < 0 || score > 100) {
            throw new IllegalArgumentException("score must be 0-100");
        }
        for (int i = 0; i < MIN.length; i++) {
            if (score >= MIN[i]) return GRADE[i];
        }
        return "F";
    }
}
```
 
ผลรัน:
 
```text
✔ gradeOf100ReturnsA
✔ gradeOf80ReturnsA
✔ gradeOf75ReturnsBPlus
✔ gradeOf70ReturnsB
✔ gradeOf65ReturnsCPlus
✔ gradeOf60ReturnsC
✔ gradeOf55ReturnsDPlus
✔ gradeOf50ReturnsD
✔ gradeOf49ReturnsF
✔ gradeOf0ReturnsF
✔ upperBoundOfEachGrade
✔ scoreAboveHundredThrows
✔ scoreBelowZeroThrows
```
 
### 💡 Learning
 
ปรับโค้ดให้อ่านง่ายขึ้นตามเฉลยของโจทย์ในสไลด์ ด้วยการ ย้ายเกณฑ์คะแนนไปไว้ในตาราง MIN กับ GRADE แล้ววนลูปหา แทน if 7 ชั้นซ้ำๆ ประหยัดพื้นที่ รันครบ 12 เทสต์ยังเขียวทุกตัว
 
[↑ กลับไปสรุปทุกรอบ](#สรุปทุกรอบ)
 
---
 
