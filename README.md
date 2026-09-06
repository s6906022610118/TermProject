# KMUTNB Admission

โปรเจกต์ UX/UI หลายหน้าที่ใช้เฉพาะ HTML และ CSS ไม่มี JavaScript ไม่มีฐานข้อมูล และไม่ต้องติดตั้งแพ็กเกจเพิ่ม

## วิธีเปิด

เปิด `index.html` ได้โดยตรง หรือเปิดโฟลเดอร์ใน VS Code แล้วเลือก **Open with Live Server**

## ลำดับหน้าหลัก

- `index.html` — หน้าแรกและรอบการรับสมัคร
- `programs.html` — รวมหลักสูตร IT, INE และ INET
- `program-it.html` — รายละเอียดหลักสูตร IT
- `program-ine.html` — รายละเอียดหลักสูตร INE
- `program-inet.html` — รายละเอียดหลักสูตร INET
- `apply-personal.html` — ขั้นที่ 1 ข้อมูลส่วนตัว
- `apply-parent.html` — ขั้นที่ 2 ข้อมูลผู้ปกครอง
- `apply-education.html` — ขั้นที่ 3 ข้อมูลการศึกษา
- `select-program.html` — ขั้นที่ 4 เลือกหลักสูตร
- `review.html` — ขั้นที่ 5 ตรวจสอบข้อมูล
- `success.html` — หน้าสมัครสำเร็จ

ลำดับฟอร์มคือ:

`apply-personal.html → apply-parent.html → apply-education.html → select-program.html → review.html → success.html`

## CSS แต่ละไฟล์ดูแลอะไร

- `css/style.css` — reset, สีหลัก, container, ปุ่ม, หน้าแรก และ Footer
- `css/navbar.css` — Navbar และการครอบรูปโลโก้
- `css/programs.css` — หน้ารวมหลักสูตร
- `css/program-detail.css` — หน้ารายละเอียดหลักสูตรทั้งสามหน้า
- `css/application.css` — ฟอร์มสมัครขั้นที่ 1–4
- `css/review.css` — หน้าตรวจสอบขั้นที่ 5
- `css/success.css` — หน้าสมัครสำเร็จ

หน้าเว็บถูกขยายประมาณ 120% จาก `zoom: 1.2` ใน `style.css` ถ้าต้องการกลับเป็นขนาดปกติให้เปลี่ยนเป็น `zoom: 1`

## เรื่องที่ควรรู้ก่อนแก้

Navbar และ Footer เขียนซ้ำในแต่ละไฟล์ HTML เพื่อให้เปิดอ่านโครงสร้างได้ง่าย ถ้าแก้เมนูหรือข้อมูลติดต่อ ต้องแก้ให้เหมือนกันทุกหน้า

ช่องกรอกและปุ่มต่าง ๆ เป็นงาน UX/UI เท่านั้น การกดถัดไปใช้ `action` ของ `<form>` เพื่อเปิดหน้า HTML ถัดไป ข้อมูลที่กรอกจะไม่ถูกเก็บหรือส่งไปฐานข้อมูล

ช่องค้นหาใน `programs.html` เป็นหน้าตาตัวอย่างและยังค้นหาจริงไม่ได้ ส่วนข้อมูลใน `review.html`, วันที่ และหมายเลขใบสมัครใน `success.html` เป็นข้อมูลตัวอย่างแบบคงที่

คอมเมนต์ใน HTML ใช้แบ่งส่วนใหญ่ของหน้า ส่วนคอมเมนต์ใน CSS บอกว่ากฎแต่ละกลุ่มควบคุมอะไร ไม่จำเป็นต้องใส่คอมเมนต์ทุกบรรทัด เพราะจะทำให้อ่านยากกว่าเดิม
