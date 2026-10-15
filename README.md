[README.md](https://github.com/user-attachments/files/33471634/README.md)
# ATF Settlement Date Calculator

| | ลิงก์ |
|---|---|
| หน้า Calculator (แชร์ให้ IC) | https://asiawork.github.io/atf-settledatecalculator/ |
| หน้า Editor (อัปเดตข้อมูล) | https://asiawork.github.io/atf-settledatecalculator/editor.html |
| หน้าอัปโหลดไฟล์ใน repo | https://github.com/asiawork/atf-settledatecalculator/upload/main |

## อัปเดตข้อมูลวันหยุด / T+N

1. Refresh ไฟล์ `portfolioweight.xlsx` ในเครื่อง แล้วกดบันทึก
2. เปิด **หน้า Editor** แล้วลาก Excel ใส่กล่องที่ 1 (ไม่ต้องอัป Excel ขึ้น GitHub)
3. ตรวจตาราง T+N ในข้อ 2 ถ้าค่าเปลี่ยนจะเป็นตัวแดงหรือเขียว
4. ข้อ 4 วันหยุดสถาบันการเงินไทย: ต้องใส่ให้ครบถึงเดือนสุดท้ายของข้อมูล (ระบบไม่ได้ดึงจาก Excel)
5. ข้อ 5 ช่วงวันที่: ระบบตั้งให้เอง แก้ช่อง "ถึง" เฉพาะเมื่อเดือนสุดท้ายในไฟล์ไม่มีกองทุนไหนหยุด
6. กด **ดาวน์โหลด data.json**
   - ถ้าไฟล์ได้ชื่อ `data (1).json` ให้เปลี่ยนชื่อกลับเป็น `data.json` ก่อน
7. เปิด **หน้าอัปโหลดไฟล์ใน repo** แล้วลาก `data.json` ไปวางทับ จากนั้นกด **Commit changes**
8. รอ 1–2 นาที แล้วเปิดหน้า Calculator ดูมุมขวาบนว่าวันที่ "ข้อมูล ณ" เปลี่ยนเป็นวันนี้แล้ว

## ไฟล์ใน repo

| ไฟล์ | คืออะไร | ต้องแก้ไหม |
|---|---|---|
| `index.html` | หน้า Calculator | ไม่ต้อง |
| `editor.html` | หน้าสร้าง data.json | ไม่ต้อง |
| `data.json` | ข้อมูล T+N + วันหยุด ที่หน้า Calculator ใช้ | อัปโหลดทับทุกครั้งที่อัปเดต |

## ถ้ามีปัญหา

- **หน้า Calculator ยังเป็นข้อมูลเก่า:** รอสักครู่แล้วกด Ctrl+F5 หรือเช็กแท็บ Actions ว่ามีเครื่องหมายถูกสีเขียวแล้ว
- **ข้อมูลผิด อยากย้อนกลับ:** เปิด `data.json` › History › เลือกเวอร์ชันก่อนหน้า › ดาวน์โหลดแล้วอัปโหลดทับ
- **IC เลือกวันที่ไม่ได้ / ขึ้นว่าข้อมูลหมดช่วง:** ถึงเวลาอัปเดต Excel แล้ว
