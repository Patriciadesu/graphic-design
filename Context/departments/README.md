# Departments

## Routing
- PM (`/root`) รับคำสั่งและเป็นช่องทางเดียวถึงผู้ใช้
- Designer ทำเฉพาะ Stage ที่ PM มอบหมาย และส่ง PNG ให้ QA ผ่าน PM
- QA ตรวจแยกจากผู้สร้าง; FAIL ให้รายการแก้เฉพาะจุด, PASS ให้ PM ส่งผู้ใช้เลือก
- วน Designer → QA จน PASS; หยุดหลังส่งผู้ใช้แต่ละ Stage จนมีตัวเลือก

## Ownership
| Department | Owned paths | รับจาก | ส่งต่อ |
|---|---|---|---|
| Designer | `output/`, `Context/quests/designer/` | PM | QA ผ่าน PM |
| QA | `Context/qa/`, `Context/quests/qa/` | PM | Designer ผ่าน PM; PM เมื่อ PASS |

## Session workflow
อ่าน `README.md` → `Context/Rules.md` → Status → Department นี้ → `INBOX.md` → Quest active → Queue
ใช้ `get_session` ชื่อ `self` เพื่อยืนยันบทบาทหัวหน้า Department เมื่อเปิด Department session

## Handoff and limits
- ทุก Sub Agent brief ต้องมี Quest, Goal, Files, Acceptance, และ isolated worktree; ห้ามสอง Agent แก้ไฟล์ชุดเดียวกัน
- ลองแก้ปัญหาใน scope ให้ครบก่อนรายงาน PM; ถ้าติดจริงส่งสิ่งที่ลองหนึ่งครั้ง
- หากส่งข้อความข้าม session ไม่ได้/ไม่มีตอบใน 30 นาที ให้บันทึกใน `INBOX.md` ใต้ `## ใหม่` หรือ `## ทำแล้ว`
- context เกินราว 60% ให้สรุปใน Quest; 5-hour เกิน 90% ไม่เริ่ม Quest ใหม่, เกิน 95% หยุด
- ทุกงานออกแบบต้องส่งภาพ PNG ใน `output/`
