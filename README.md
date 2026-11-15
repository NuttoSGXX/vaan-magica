# ตารางเซสชัน · Vaan Magica (Vercel)

ระบบเดียวกับตารางของ DM Bank แต่เป็นเว็บแยก ข้อมูลแยก รหัสแยก

ไฟล์
- index.html       หน้าเว็บ
- api/schedule.js  ฟังก์ชันฝั่งเซิร์ฟเวอร์ (อ่าน/บันทึก + ตรวจรหัสผู้ดูแล)
- package.json

ตั้งค่า (ทำครั้งเดียว)
1. สร้าง repo ใหม่บน GitHub แล้วอัปโหลดไฟล์ทั้งหมดในโฟลเดอร์นี้ (ลากโฟลเดอร์ api ไปทั้งโฟลเดอร์)
2. Vercel -> Add New -> Project -> เลือก repo นี้ -> Deploy
3. ในโปรเจกต์ใหม่: Storage / Marketplace -> Upstash for Redis -> สร้าง -> Connect to Project
   (ใช้ฐานข้อมูลเดียวกับตารางของ DM Bank ก็ได้ ข้อมูลไม่ปนกัน เพราะเก็บใต้ชื่อ vaan-schedule)
4. Settings -> Environment Variables -> ADMIN_PIN = รหัสของ Vaan
5. Deployments -> ⋯ -> Redeploy

วิธีเข้าโหมดแก้ไข
- กดข้อความ "— by Vaan Magica" มุมล่างซ้าย 8 ครั้ง -> ใส่รหัส
