# Q-20261123-land-and-coffee-06-qa — QA review

- Status: ผ่าน QA สำหรับเลือก 8 Style + Original ในมุมเฉียงท้ายรถ
- Parent: `Q-20261123-land-and-coffee-06`
- Owner: QA Department
- Files: review `output/stage-1-original-line-options.png`; report at `Context/qa/Q-20261123-land-and-coffee-06-qa.md`
- Stage 1 pass: 7 แบบขาวดำที่ต่างกันที่ลายเส้น เปรียบเทียบกับภาพแนบโดยตรง ทุกแบบคงองค์ประกอบ คน รถ ว่าว ท่าทาง ตำแหน่ง ตัวหนังสือ โลโก้ และกรอบเดิม
- FAIL returns location-specific corrections to Designer via PM; PASS returns to PM to send Stage 1 options to user
- Do not begin Stage 2 or Stage 3 until the user selects

- Stage 2 files: output/stage-2-compositions/ และ output/stage-2-composition-options.png
- Stage 2 pass: 7 องค์ประกอบต่างกันชัด ครบสองคน รถเปิดหลังคา ว่าวและสาย หมาไทยหลังอาน ใช้ลายเส้นแบบ 3 ขาวดำ ตรวจโครงสร้างและท่าทาง ไม่มีข้อความในงาน
- Gate: รอผู้ใช้เลือกการจัดวางก่อนเริ่ม Stage 3

- รอบเลือกแนวภาพ: ตรวจว่าเห็นความต่างของรูปหน้า สัดส่วน silhouette และพื้นที่ดำในตัวเลือกทั้ง 7 ฉากครบ ใช้ตำแหน่งและมุมร่วมกัน ตามแนวภาพอ้างอิงล่าสุด
- Files: output/stage-1-art-direction-options.png และ output/stage-1-art-directions/
- รอบ 1, 3, 6 ตรวจลักษณะหัวปากกาแบนตรงไฟล์ 03 ที่ตกลงไว้ ตรวจฉากครบและขาวดำ พร้อมตรวจช่อง 2, 4, 5, 7, 8 ตรงกับก่อนแก้
- รอบมุมเฉียงท้ายรถ ตรวจ 8 ภาพขาวดำยึดมุมและตำแหน่งตามโจทย์ เปรียบเทียบสไตล์กับชุดเดิม และตรวจไฟล์ Original ตรงกับภาพแนบ ตรวจ output/rear-view-style-options.png และ output/rear-view-styles/
