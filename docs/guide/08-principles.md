<a id="steer-with-principle-names"></a>

# ชี้ทิศทางด้วยชื่อหลักการ

pstack มีหลักการ 24 ข้อแยกเป็นสกิล `/poteto-mode` อ่านสารบัญหลักการเมื่อเริ่มงานหลายขั้นตอนทุกครั้ง ใช้ข้อที่ตรงกับงาน และระบุชื่อหลักการที่ใช้ในคำตอบ พร้อมบอกว่าทำให้เปลี่ยนการตัดสินใจใด

คุณไม่ต้องเรียกหลักการเป็นคำสั่ง ใช้ชื่อเพื่อชี้ทิศทาง แต่ละชื่ออ้างถึงกฎฉบับเต็มที่เอเจนต์อ่านแล้ว วลีเดียวจึงเปลี่ยนแนวทางได้แม่นกว่าคำสั่งยาวหนึ่งย่อหน้า

<a id="steering-in-practice"></a>

## ตัวอย่างการชี้ทิศทาง

สมมติเอเจนต์กำลังจะเพิ่ม adapter ใหม่ต่อจากสามตัวเดิม:

```text
ใช้ subtract before you add ลบ adapter ที่ล้าสมัยก่อน แล้วออกแบบส่วนที่เหลือ
```

สมมติเอเจนต์อ้างว่าสำเร็จเพราะ build ผ่าน:

```text
ใช้ prove it works รันกระบวนการ import จริง แล้วแสดงรายการที่เขียนลงไป
```

สมมติสองแนวทางที่ทำพร้อมกันกำลังจะเขียนลง branch เดียวกัน:

```text
ใช้ separate before serializing shared state ให้แต่ละแนวทางมี worktree ของตัวเอง ไม่ใช้ lock
```

แต่ละวลีได้ผลเพราะกฎเบื้องหลังเฉพาะเจาะจง เอเจนต์ยังต้องบอกในคำตอบว่ากฎนั้นเปลี่ยนการตัดสินใจอะไร หากอ้างชื่อหลักการโดยไม่มีการตัดสินใจรองรับ แสดงว่าแค่เอ่ยชื่อ ไม่ได้ใช้จริง

<a id="the-24-briefly"></a>

## สรุปหลักการทั้ง 24 ข้อ

หลักการพื้นฐานกำหนดว่าควรสร้างมากแค่ไหนและเมื่อใดควรทบทวนการออกแบบ:

- [Laziness Protocol — แก้ให้น้อยที่สุด](../../skills/principle-laziness-protocol/SKILL.md) เน้นการลบและการเปลี่ยนแปลงที่เล็กที่สุดซึ่งแก้ปัญหาได้
- [Foundational Thinking — วางรากฐานก่อน](../../skills/principle-foundational-thinking/SKILL.md) เลือกโครงสร้างข้อมูลหลักก่อนเขียนตรรกะ
- [Redesign from First Principles — ออกแบบจากหลักพื้นฐาน](../../skills/principle-redesign-from-first-principles/SKILL.md) รวมความต้องการใหม่ให้เหมือนมีมาตั้งแต่วันแรก
- [Attack the Premise — ตั้งคำถามกับสมมติฐาน](../../skills/principle-attack-the-premise/SKILL.md) ตรวจว่าใครทำให้เกิดความไม่สมดุล แล้วทบทวนสมมติฐานร่วมของวิธีแก้ตั้งแต่สองแบบที่ล้มเหลว
- [Subtract Before You Add — ลบก่อนเพิ่ม](../../skills/principle-subtract-before-you-add/SKILL.md) เอาส่วนเกินออกก่อนสร้างต่อ
- [Minimize Reader Load — ลดภาระผู้อ่าน](../../skills/principle-minimize-reader-load/SKILL.md) ลดชั้นและสถานะที่ผู้อ่านต้องจำไว้ในหัว
- [Outcome-Oriented Execution — มุ่งสู่ผลลัพธ์](../../skills/principle-outcome-oriented-execution/SKILL.md) นำการเขียนใหม่ไปสู่แบบเป้าหมาย แทนการรักษาสถานะรองรับชั่วคราวที่ต้องทิ้งทีหลัง
- [Experience First — ประสบการณ์ผู้ใช้มาก่อน](../../skills/principle-experience-first/SKILL.md) เลือกผลลัพธ์ของผู้ใช้ก่อนความสะดวกในการเขียนโค้ด
- [Exhaust the Design Space — สำรวจทางเลือกให้พอ](../../skills/principle-exhaust-the-design-space/SKILL.md) สร้างต้นแบบสองหรือสามแบบเมื่อไม่มีตัวอย่างเดิมให้ยึด
- [Build the Lever — สร้างเครื่องมือทุ่นแรง](../../skills/principle-build-the-lever/SKILL.md) สร้างสคริปต์ที่ทำงานหรือพิสูจน์งาน เพื่อให้ผู้รีวิวรันซ้ำได้

หลักการสถาปัตยกรรมกำหนดที่อยู่ของสถานะ การตรวจข้อมูล และการรองรับของเดิม:

- [Model the Domain — ออกแบบโครงสร้างตามงาน](../../skills/principle-model-the-domain/SKILL.md) รวมกฎที่ซ้ำไว้ในโครงสร้างเดียว แทนเงื่อนไขกระจายหลายจุด
- [Boundary Discipline — ตรวจที่ขอบเขต](../../skills/principle-boundary-discipline/SKILL.md) ตรวจข้อมูลที่ขอบเขตระบบและเชื่อชนิดข้อมูลภายใน
- [Type System Discipline — ใช้ชนิดข้อมูลอย่างมีวินัย](../../skills/principle-type-system-discipline/SKILL.md) ทำให้สถานะที่ผิดกฎไม่สามารถสร้างขึ้นได้
- [Make Operations Idempotent — ทำซ้ำแล้วได้ผลเดิม](../../skills/principle-make-operations-idempotent/SKILL.md) ทำให้การลองซ้ำจบที่สถานะเดียวกัน
- [Migrate Callers Then Delete Legacy APIs — ย้ายผู้เรียกแล้วลบ API เก่า](../../skills/principle-migrate-callers-then-delete-legacy-apis/SKILL.md) ย้ายและลบในรอบเดียว
- [Separate Before Serializing Shared State — แยกก่อนจัดคิวใช้สถานะร่วม](../../skills/principle-separate-before-serializing-shared-state/SKILL.md) ยกเลิกการใช้ร่วมก่อนเพิ่มกลไกประสานงาน

หลักการตรวจสอบกำหนดว่าอะไรนับเป็นหลักฐาน:

- [Prove It Works — พิสูจน์ว่าใช้ได้จริง](../../skills/principle-prove-it-works/SKILL.md) ตรวจผลงานจริง ไม่ใช่สิ่งแทน
- [Fix Root Causes — แก้ที่ต้นเหตุ](../../skills/principle-fix-root-causes/SKILL.md) ทำให้เกิดปัญหาซ้ำและไล่ถึงสาเหตุก่อนแก้โค้ด
- [Sequence Work into Verifiable Units — แบ่งงานเป็นหน่วยที่ตรวจได้](../../skills/principle-sequence-verifiable-units/SKILL.md) ตรวจหน่วยเล็กแต่ละส่วนให้จบก่อนเริ่มส่วนถัดไป
- [Test Behavior, Not Implementation — ทดสอบพฤติกรรม](../../skills/principle-test-behavior-not-implementation/SKILL.md) เรียกโค้ดแบบผู้ใช้และเทียบกับค่าคาดหวังที่ระบุชัด ลบ test ที่ยังผ่านแม้ทุกฟังก์ชันที่ import คืนค่า `undefined`
- [Explain the Number — อธิบายตัวเลข](../../skills/principle-explain-the-number/SKILL.md) ระบุข้อจำกัดของตัวเลขที่วัดและตัดความเป็นไปได้ว่าวัดอย่างอื่น ก่อนเชื่อหรือรายงานผล

หลักการมอบหมายงานช่วยให้การทำพร้อมกันเป็นระเบียบ:

- [Guard the Context Window — รักษาพื้นที่บริบท](../../skills/principle-guard-the-context-window/SKILL.md) ส่งงานอ่านจำนวนมากให้เอเจนต์ย่อย และเก็บข้อค้นพบไว้ในแชตหลัก
- [Never Block on the Human — อย่าหยุดรอคนโดยไม่จำเป็น](../../skills/principle-never-block-on-the-human/SKILL.md) เดินหน้างานที่ย้อนกลับได้แล้วนำเสนอผล

และหลักการเพื่อปรับปรุงวิธีทำงานอีกหนึ่งข้อ:

- [Encode Lessons in Structure — ฝังบทเรียนในโครงสร้าง](../../skills/principle-encode-lessons-in-structure/SKILL.md) เปลี่ยนคำแนะนำที่ต้องย้ำสองครั้งให้เป็น lint การตรวจ หรือสคริปต์

ไม่ต้องท่องจำ อ่านผ่านรอบหนึ่ง แล้วกลับมาดูเมื่อพบว่าเอเจนต์กำลังทำสิ่งที่ชื่อหลักการเหล่านี้ช่วยป้องกันได้ คุณจะจำคำศัพท์ได้จากการใช้

ถัดไป: [ปรับให้เป็นสไตล์ของคุณ](./09-make-it-yours.md)
