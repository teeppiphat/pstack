<!-- mirror:start — ส่วนต้นนี้เป็นข้อมูลเฉพาะของ mirror ส่วนหลัง mirror:end แปลจาก README ต้นทาง cursor/plugins/pstack โดยคงโครงสร้างและความหมายเดิม หากต้องการซิงก์กับต้นทาง ให้ทำตาม MIRROR.md -->
<a id="pstack--standalone-mirror"></a>

# pstack — mirror สำหรับใช้งานแยก

> **สำเนา mirror** ของ [`cursor/plugins/pstack`](https://github.com/cursor/plugins/tree/main/pstack) ที่ซิงก์ไว้สำหรับใช้งานแยกจากต้นทาง
> ใช้ได้กับ Claude Code, Codex, Pi และเอเจนต์อื่น ๆ ไม่จำกัดเฉพาะ Cursor
> ดู [`backnotprop/bro`](https://github.com/backnotprop/bro) เพิ่มเติม ซึ่งสกิล [`/bro`](./skills/bro/SKILL.md) อ้างถึง

README ของ Cursor ฉบับแปลอยู่ [ด้านล่างของหน้านี้](#pstack)

<a id="install"></a>

## ติดตั้ง

pstack เป็นโฟลเดอร์ของ [Agent Skills](https://agentskills.io) แบบไฟล์ทั่วไป (`skills/<name>/SKILL.md`) ไม่จำเป็นต้องใช้ Cursor เครื่องมือ [`skills` CLI](https://skills.sh) ติดตั้งสกิลเข้า Claude Code, Codex, Pi, Cursor, OpenCode และเอเจนต์อื่นได้:

```bash
npx skills add backnotprop/pstack
```

CLI แสดงรายการสกิลทั้งหมดให้ค้นหา เลือกสกิลที่ต้องการ แล้วเลือกเอเจนต์ที่จะใช้

<a id="skills"></a>

## สกิล

สกิลต่อไปนี้ไม่เรียกสกิลอื่นของ pstack จึงใช้แยกได้:

`unslop`, `bro`, `how`, `tdd`, `typescript-best-practices`, `arena`, `swarm`, `interrogate`, `reflect`, `show-me-your-work`, `figure-it-out`, `automate-me`, `correct`

บางสกิลเรียกสกิลอื่นด้วย ให้ติดตั้งกลุ่มเหล่านี้ด้วยกัน:

| สกิล | ติดตั้งเพิ่มด้วย |
|---|---|
| `teach` | `how`, `why` |
| `why` | `how` |
| `technical-writing` | `unslop` |
| `architect` | `arena`, `how` |
| `blast-radius` | `arena`, `how`, `why`, `unslop` |
| `create-verification-skill` | `maintain-verification-skill` |
| `benchmark-checklist` | `principle-explain-the-number` |
| `poteto-mode` | สกิล `principle-*` ทั้งหมดและสกิลอื่นส่วนใหญ่ |

<a id="what-this-mirror-changes"></a>

## สิ่งที่ mirror นี้เปลี่ยน

หลายสกิลเดิมใช้ได้เฉพาะ Cursor ปัจจุบันปรับให้ใช้กับสภาพแวดล้อมเอเจนต์อื่นได้แล้ว
<!-- mirror:end -->

---

<a id="pstack"></a>

# pstack

ผมคือ [poteto](https://x.com/poteto) ไม่ใช่ประธานหรือ CEO แต่เคยทำงานกับโค้ดหลายล้านบรรทัดที่ Meta, Netflix และ Cursor และเป็นสมาชิกทีมหลักของ React ที่ช่วยสร้างและดูแล React Compiler

หลายคนเริ่มรู้สึกว่า AI เขียนโค้ดรกและคุณภาพต่ำมากเกินไป ผมเห็นด้วย ผมไม่อยากส่งงานเหมือนมีทีมยี่สิบคนที่ผลิตแต่โค้ดแบบนั้น ปริมาณงานที่ไม่มีคุณภาพไม่ใช่เป้าหมายของผม ถ้าอยากไปเร็ว ต้องเข้าใจให้ลึกก่อน

**pstack คือคำตอบของผม** นี่คือสกิลชุดเดียวกับที่ผมใช้ทุกวันเพื่อส่งโค้ดคุณภาพสูงที่ Cursor ช่วยเปลี่ยน Cursor ให้เป็นทีมวิศวกรรมจริง ๆ เป้าหมายไม่ใช่เพิ่มจำนวนบรรทัดโค้ด แต่ตรงกันข้าม pstack ช่วยให้เขียนน้อยลงและได้โค้ดที่ดีขึ้น

**pstack ช่วยให้ทำงานพร้อมกันได้อย่างมั่นใจ** เมื่อคุณลงลึกกับเอเจนต์ตัวหนึ่งและเชื่อใจให้เขียนโค้ดที่ดีและตรวจสอบได้ คุณก็ขยายไปทำงานหลายตัวพร้อมกันได้ เริ่มเอเจนต์หลายตัวด้วย `poteto-mode` แล้วให้พวกมันใช้หลักวิศวกรรมที่รอบคอบกับงาน

**Cursor รวมข้อดีจากหลายโมเดลให้คุณ** โมเดลชั้นนำแต่ละตัวมีจุดแข็งและจุดอ่อน คุณใช้โมเดลใดกับ pstack ก็ได้ หลายสกิลของผมใช้ workflow หลายโมเดลเพื่อดึงจุดแข็งเฉพาะของแต่ละตัว

fork ไป ปรับปรุง และทำให้เป็นสไตล์ของคุณ ยินดีรับ PR!

<a id="install-1"></a>

## ติดตั้ง

```bash
/add-plugin pstack
```

<a id="get-started"></a>

## เริ่มต้น

มีสองขั้นตอน:

1. เรียก [`/setup-pstack`](./skills/setup-pstack/SKILL.md) เลือกงบประมาณการใช้เหตุผลและโมเดลที่ต้องการ
2. ใช้ [`/poteto-mode`](./skills/poteto-mode/SKILL.md) เมื่อทำงานที่ต้องการความรอบคอบ

เพิ่งเริ่มใช้หรือไม่? [คู่มือ pstack](./docs/guide/README.md) พาทำงานจริงครั้งแรก ตั้งแต่ตั้งค่าและเขียนคำขอ ไปจนตรวจสอบและปล่อยทำงานข้ามคืน

เท่านี้ก็พอ สกิลอื่นใช้ตามสถานการณ์ โดยสกิลโหมดจะเรียกให้เมื่อจำเป็น ค่าเริ่มต้นแบ่งงานตามจุดแข็งของโมเดล: งานเขียนโค้ดที่มอบหมาย (เพิ่มฟีเจอร์ ปรับโครงสร้าง แก้บั๊ก ปรับประสิทธิภาพ และปรับตัวชี้วัดทีละรอบ) ใช้ grok ส่วนงานแก้ที่ยากที่สุด งานเขียนข้อความ และการตัดสินใช้ opus 5.5 ทีมรีวิวเริ่มต้นคือ opus 5.5 / sol / grok เปลี่ยนได้ด้วย [`/setup-pstack`](./skills/setup-pstack/SKILL.md)

<a id="usage"></a>

## การใช้งาน

ใช้ [`/poteto-mode`](./skills/poteto-mode/SKILL.md) เมื่อเริ่มงาน ระบบอ่านคำขอ เลือกแนวทางทำงาน (playbook) และเรียกสกิลอื่นตามที่แต่ละขั้นต้องใช้

<a id="just-use-poteto-mode"></a>

### เริ่มด้วย [`/poteto-mode`](./skills/poteto-mode/SKILL.md) ก็พอ

นี่คือทางลัดหลัก ผมใช้เมื่ออยากให้เอเจนต์ทำงานวิศวกรรมอย่างรอบคอบ มาพร้อมแนวทางทำงาน 23 แบบ:

```
/poteto-mode PR นี้มีบั๊กแฝงที่ตำแหน่งเลื่อนหน้าจอขยับทุก 750ms แม้ไม่ได้ใช้งาน ทำให้ปัญหา
เกิดซ้ำก่อน แล้วแก้และตรวจสอบ
```

```
/poteto-mode ผมจะนอนแล้ว รวมชุด PR แม้ CI จะมีผลไม่แน่นอน ผมอยากให้ทุกอย่าง merge เสร็จ
ก่อนเช้า
```

<details>
<summary>แนวทางทำงานทั้ง 23 แบบ</summary>

| แนวทาง | ใช้สำหรับ |
|---|---|
| [สืบค้น](./skills/poteto-mode/playbooks/investigation.md) | คำถามแบบอ่านอย่างเดียว เช่น x ทำงานอย่างไร ทำไมสร้าง y แบบนี้ และมั่นใจได้หรือไม่ |
| [แก้บั๊ก](./skills/poteto-mode/playbooks/bug-fix.md) | ทำให้เกิดปัญหาซ้ำ หาต้นเหตุ และแก้ด้วยหลักฐานขณะรันจริง |
| [ประสิทธิภาพ](./skills/poteto-mode/playbooks/perf-issue.md) | ไล่สาเหตุความช้าที่วัดได้ และปรับปรุงเทียบกับค่าฐาน |
| [ปรับตัวชี้วัดทีละรอบ](./skills/poteto-mode/playbooks/hillclimb.md) | ปรับตัวชี้วัดหนึ่งอย่างสู่เป้าหมายอย่างเป็นระบบ วนทดสอบสมมติฐาน วัดก่อนและหลัง และ commit หนึ่งครั้งต่อผลดีขึ้นที่ยอมรับ |
| [วิเคราะห์อาการขณะทำงาน](./skills/poteto-mode/playbooks/runtime-forensics.md) | ตรวจอาการสด เช่น หน่วยความจำรั่ว CPU ทำงานวนตอนว่าง หรือความผิดปกติ โดยใช้เครื่องมือเก็บข้อมูล |
| [วิเคราะห์ trace](./skills/poteto-mode/playbooks/trace-forensics.md) | วิเคราะห์ข้อมูลประสิทธิภาพที่บันทึกไว้ เช่น cpuprofile, trace, spindump และ heap snapshot |
| [เพิ่มฟีเจอร์](./skills/poteto-mode/playbooks/feature.md) | สร้างพฤติกรรมใหม่หรือเปลี่ยนพฤติกรรม โดยเริ่มจากรูปแบบข้อมูลที่กำหนดชัด |
| [ปรับโครงสร้าง](./skills/poteto-mode/playbooks/refactoring.md) | เปลี่ยนโครงสร้างหรือรูปแบบโดยคงพฤติกรรมเดิม |
| [ต้นแบบ](./skills/poteto-mode/playbooks/prototype.md) | สร้างแบบทดลองที่ทิ้งได้เพื่อช่วยตัดสินใจเรื่องออกแบบหรือพฤติกรรม หรือเลือกทางจากผลที่สังเกตจริง |
| [ทำภาพให้ตรงกัน](./skills/poteto-mode/playbooks/visual-parity.md) | ทำ UI จากสองวิธีให้ตรงกันระดับพิกเซล |
| [เขียนสกิล](./skills/poteto-mode/playbooks/authoring-a-skill.md) | เขียนหรือแก้ SKILL.md |
| [ประเมิน](./skills/poteto-mode/playbooks/eval.md) | ทดสอบว่าการเปลี่ยนสกิลหรือคำขอส่งผลต่อเอเจนต์อย่างไร โดยไม่เปิดเผยเงื่อนไขการประเมิน |
| [ดูแล PR](./skills/poteto-mode/playbooks/babysit.md) | ทำ PR หรือชุด PR ให้พร้อม merge โดยแก้ conflict บทสนทนารีวิว และ CI |
| [รวมงาน](./skills/poteto-mode/playbooks/shipping.md) | ตรวจชุด PR ที่ผ่านการตรวจอีกครั้งอย่างอิสระ แล้วรวมเฉพาะช่วงต่อเนื่องที่พิสูจน์แล้วจากล่างขึ้นบน ผ่าน GitHub ตามค่าเริ่มต้น หรือ Origin เมื่อพร้อมใช้ |
| [ทำงานอัตโนมัติต่อเนื่อง](./skills/poteto-mode/playbooks/autonomous-run.md) | ทำงานยาวให้เสร็จโดยไม่หยุด |
| [ประสานโครงการ](./skills/poteto-mode/playbooks/orchestrate.md) | ฝากโครงการหลายวัน หลายชุด PR และเอเจนต์ย่อยจำนวนมากไว้กับแชตผู้ประสานงานหนึ่งตัว |
| [autopilot-full](./skills/poteto-mode/playbooks/autopilot-full.md) | ทำ PR อิสระจน merge มีเจ้าของหนึ่งตัวต่อ PR และผลตัดสินจากทีมตรวจระดับหลักในแต่ละรอบ ตั้งแต่ commit ที่โค้ดพร้อม |
| [autopilot-stack](./skills/poteto-mode/playbooks/autopilot-stack.md) | สร้างและตรวจชุด PR ที่ต่อเป็นเส้นเดียวจาก branch ฐาน ให้ผู้ใช้งานรีวิวและรวม |
| [รับช่วงเซสชัน](./skills/poteto-mode/playbooks/session-pickup.md) | ทำต่อหรือรับช่วงงานค้างของเอเจนต์ก่อนหน้า |
| [พักอย่างปลอดภัย](./skills/poteto-mode/playbooks/pause-safely.md) | หยุดพักงานที่กำลังทำให้เรียบร้อย เพื่อกลับมาทำต่อได้ |
| [แผนหลายระยะ](./skills/poteto-mode/playbooks/multi-phase-plan.md) | งานที่มีหลายระยะหรือหลาย PR ต่อกัน |
| [ล้าง worktree](./skills/poteto-mode/playbooks/worktree-cleanup.md) | คืนพื้นที่โดยลบ worktree ที่ merge แล้วหรือเลิกใช้ และตัวจำลอง iOS ที่ค้างอยู่ โดยผ่านการตรวจความปลอดภัย |
| [เปิด PR](./skills/poteto-mode/playbooks/opening-a-pr.md) | เปิด PR พร้อมรีวิวจาก commit เล็กตามลำดับ ใช้ชื่อแบบ Conventional Commits และคำอธิบายแบบสรุปงาน เรียกเมื่อจบแนวทางอื่นทุกแบบ |

</details>



เมื่อเรียกใช้ ระบบจะ:

1. จับคู่งานกับ [playbook](./skills/poteto-mode/playbooks/) และเปิดรายการงาน โดยรายการแรก ๆ คัดลอกขั้นตอนจาก playbook ตรงตามต้นฉบับ
2. ส่งต่อให้สกิลอื่นเมื่อถึงขั้นตอนที่ต้องใช้
3. เขียนคำตอบที่กระชับและตรงประเด็นสำหรับผู้ใช้งานและผู้ดูแลระบบ

กฎและแนวทางฉบับเต็มอยู่ใน [`skills/poteto-mode/SKILL.md`](./skills/poteto-mode/SKILL.md)

[`/poteto-mode`](./skills/poteto-mode/SKILL.md) เป็นโหมดที่ทำงานต่อเนื่อง เมื่อเปิดแล้วจะอยู่ข้ามข้อความ ใช้เมื่อมี playbook ที่ตรงหรืองานต้องการความรอบคอบ และไม่รบกวนงานอื่น คุณบอกให้ปิดได้ทุกเมื่อ

[`/poteto-mode`](./skills/poteto-mode/SKILL.md) ใช้ร่วมกับคำสั่ง `/loop` ของ Cursor ได้ดีมาก ให้ Cursor ทำงานหลายชั่วโมงโดยยังรักษาความรอบคอบได้

<a id="skills-1"></a>

## สกิล

[`/poteto-mode`](./skills/poteto-mode/SKILL.md) เรียกสกิลส่วนใหญ่ให้เมื่อขั้นตอนต้องใช้ (`how`, `why`, `architect`, `arena`, `swarm`, `interrogate`, `unslop`, `no-comments`, `technical-writing`, `tdd` และหลักการต่าง ๆ) ตารางนี้สำหรับเวลาที่อยากเรียกเองโดยตรง:

```
/how เรายกเลิกการรันอย่างไร? มีปัญหา n+1 ตอนค้นหาทุกการรันที่จะยกเลิกหรือไม่?
```

```
/interrogate รีวิว PR นี้
```

<details>
<summary>สกิลทั้งหมด</summary>

| สกิล | ใช้เมื่อ |
|---|---|
| [`/poteto-mode`](./skills/poteto-mode/SKILL.md) | จุดเริ่มต้นมาตรฐานสำหรับงานที่ไม่ใช่เรื่องเล็กน้อย |
| [`/how`](./skills/how/SKILL.md) | ต้องการคำอธิบายว่าระบบย่อยทำงานอย่างไร |
| [`/why`](./skills/why/SKILL.md) | ต้องการรู้เหตุผลที่สร้างไว้แบบนี้ ตรวจหา MCP ที่ใช้ได้ขณะทำงาน และค้นหลักฐานแต่ละประเภทพร้อมกัน (source control ระบบติดตามงาน เอกสารยาว แชตสด ข้อมูลเฝ้าระวังโครงสร้างพื้นฐาน บันทึกข้อผิดพลาด และคลังข้อมูลวิเคราะห์) |
| [`/recall`](./skills/recall/SKILL.md) | เริ่มหรือกลับมาทำงาน และอยากรวบรวมบริบทล่าสุดจากประวัติแชตกับข้อมูลร่วม เป็นสรุปสถานะปัจจุบันที่กระชับ |
| [`/blast-radius`](./skills/blast-radius/SKILL.md) | มีการแก้ที่ดูเล็กและอยากรู้ว่าอาจกระทบอะไร พร้อมพิสูจน์เหตุผลหลักที่ทำให้ปลอดภัยด้วยการรันโค้ด |
| [`/architect`](./skills/architect/SKILL.md) | กำลังจะเขียนโค้ดข้ามขอบเขตฟังก์ชัน และต้องการกำหนดการใช้งานของผู้เรียก ชนิดข้อมูล และรูปแบบโมดูลก่อน |
| [`/arena`](./skills/arena/SKILL.md) | ต้องการลองงานเดียวกัน N แนวทางพร้อมกัน แล้วเลือกส่วนที่ดีที่สุดจากแต่ละแบบ |
| [`/swarm`](./skills/swarm/SKILL.md) | ต้องการผู้ทำงาน N ตัวแบ่งส่วนงานหรือแข่งหลายทาง แล้วรวมรายงานเดียว |
| [`/interrogate`](./skills/interrogate/SKILL.md) | มี diff และอยากให้หลายโมเดลหาจุดที่ทำให้พัง รวมถึงตรวจคุณภาพโค้ดอย่างเข้มงวด |
| [`/automate-me`](./skills/automate-me/SKILL.md) | อยากมีสกิล `-mode` ของตัวเอง โดยร่างจากวิธีทำงานจริง |
| [`/make-bot-ui`](./skills/make-bot-ui/SKILL.md) | อยากได้หน้าหรือแดชบอร์ดที่ปุ่มปลุก Grok Bot ผ่าน webhook รวมถึงการส่งต่อ sender key และ Tailscale |
| [`/setup-pstack`](./skills/setup-pstack/SKILL.md) | อยากเลือกโมเดลที่ pstack ใช้ในแต่ละบทบาท ระบบตรวจโมเดลและเขียนกฎตั้งค่า |
| [`/reflect`](./skills/reflect/SKILL.md) | งานยาวเสร็จแล้วและอยากเก็บวิธีทำเป็นการปรับสกิล |
| [`/correct`](./skills/correct/SKILL.md) | ต้องแก้พฤติกรรมเอเจนต์ซ้ำเรื่องเดิม ระบบค้นรูปแบบความผิดพลาดและแก้ในระดับที่มีผลสูงสุด (สถาปัตยกรรม ตามด้วยชนิดข้อมูล lint และ CI แล้วจึง test โดยเอกสารอยู่ท้ายสุด) พร้อมตารางจับคู่กฎกับกลไกบังคับใช้ |
| [`/teach`](./skills/teach/SKILL.md) | อยากเข้าใจการเปลี่ยนแปลงหรือระบบย่อยจริง ๆ ใช้ how + why แล้วเรียบเรียงคำอธิบายง่าย ๆ ทีละแผนภาพ |
| [`/tdd`](./skills/tdd/SKILL.md) | แก้บั๊กที่มีวิธีทดสอบในเครื่องต้นทุนต่ำ เขียน test ที่ล้มเหลวก่อนแล้วจึงแก้ |
| [`/benchmark-checklist`](./skills/benchmark-checklist/SKILL.md) | รัน benchmark หรือวัดความเร็วที่ดีขึ้นหรือแย่ลง ตรวจความน่าเชื่อถือของตัวเลข (ข้อจำกัด การปรับค่า ข้อผิดพลาด การรันซ้ำ และความเกี่ยวข้องกับการใช้งานจริง) ก่อนรายงานหรือตัดสินใจ |
| [`/no-comments`](./skills/no-comments/SKILL.md) | ตัดคอมเมนต์ก่อนรีวิว เรียก Comment Sicko แก้ข้อค้นพบที่ยอมรับ และเสนอวิธีฝังข้อจำกัดในโครงสร้าง |
| [`/typescript-best-practices`](./skills/typescript-best-practices/SKILL.md) | อ่านหรือแก้ TypeScript เพื่อใช้หลักการระบบชนิดข้อมูลกับไวยากรณ์จริง |
| [`/figure-it-out`](./skills/figure-it-out/SKILL.md) | ไม่มี playbook ที่รวมมาตรงกับงาน จึงออกแบบแนวทางที่รอบคอบและตรวจย้อนหลังได้ |
| [`/show-me-your-work`](./skills/show-me-your-work/SKILL.md) | ต้องการประวัติการตัดสินใจที่รีวิวได้ บันทึกเป็น TSV ที่ commit ได้ |
| [`/create-verification-skill`](./skills/create-verification-skill/SKILL.md) | โปรเจกต์ยังไม่มีวิธีใช้คำสั่งพิสูจน์พฤติกรรมแอป สร้างสกิลตรวจสอบเฉพาะโปรเจกต์พร้อมแผนที่ฟีเจอร์ ใช้ได้กับทุกภาษาและแพลตฟอร์ม |
| [`/maintain-verification-skill`](./skills/maintain-verification-skill/SKILL.md) | แผนที่ฟีเจอร์ของสกิลตรวจสอบไม่ตรงกับแอป ตรวจ source แล้วลองจริงหนึ่งรอบ และเปิด PR แก้ที่พิสูจน์แล้วไม่เกินหนึ่งรายการ |
| [`/unslop`](./skills/unslop/SKILL.md) | เก็บข้อความให้เรียบร้อยและลดสำนวนที่ดูเป็นข้อความสำเร็จรูปจาก AI |
| [`/bro`](./skills/bro/SKILL.md) | อยากให้เล่าข้อความล่าสุดใหม่ด้วยภาษาคนทั่วไป ไม่ใช้ศัพท์ยาก |
| [`/technical-writing`](./skills/technical-writing/SKILL.md) | ใช้มาตรฐานเอกสารหลายชั้น (Diátaxis + Google developer style + STE + Global English) กับเอกสาร RFC, README, คำอธิบาย PR และข้อความ commit |

</details>



<a id="examples"></a>

### ตัวอย่าง

ส่วนใหญ่ผมพิมพ์ [`/poteto-mode`](./skills/poteto-mode/SKILL.md) ตอนเริ่มงาน แล้วให้เลือกแนวทางเอง สกิลอื่นจะทำงานเมื่อถึงขั้นที่ต้องใช้ มีบางตัวที่ผมเรียกตรง ๆ


<details>
<summary>ตัวอย่างทั้งหมด</summary>

```
แก้บั๊ก:           /poteto-mode PR นี้มีบั๊กแฝงที่ตำแหน่งเลื่อนขยับทุก 750ms แม้ไม่ได้ใช้งาน
                   ทำให้เกิดปัญหาซ้ำก่อน แล้วแก้และตรวจสอบ
ประสิทธิภาพ:      /poteto-mode รายการใหญ่ใช้เวลาหนึ่งถึงสองวินาทีโหลด แม้ใช้ virtualization
                   เก็บ cpu trace แล้วบอกสาเหตุ
เพิ่มฟีเจอร์:      /poteto-mode สร้างฟีเจอร์เล็กหลัง feature flag ตรวจว่าทำงานจริง
ต้นแบบ:           /poteto-mode สร้างต้นแบบตัวแสดง markdown สองแบบเพื่อเปรียบเทียบ
                   ให้เอเจนต์หนึ่งตัวทำแต่ละแบบ
หลายระยะ:         /poteto-mode เปิดสกิลเหล่านี้เป็นปลั๊กอินโอเพนซอร์ส ห้ามข้อมูลภายในรั่ว ทำงาน
                   ในไดเรกทอรีชั่วคราว แสดงแผนผัง dependency ก่อน
งานข้ามคืน:       /poteto-mode ผมจะนอนแล้ว รวมชุด PR แม้ CI จะมีผลไม่แน่นอน อยากให้
                   merge ครบก่อนเช้า
ดูแล PR:          /poteto-mode ตรวจ PR 123 มีอะไรค้างอยู่ไหม?
ภาพตรงกัน:        /poteto-mode ระยะห่างแถวสูงเกินไปเมื่อเปิด flag นี้ ภาพที่สองถูกต้อง
                   ทำให้เกิดปัญหาซ้ำแล้วแก้จนตรงกัน
หาแนวทาง:         /poteto-mode ผมจะไปทำอย่างอื่น ย้ายผู้เรียกทุกจุดจากระบบจัดเก็บแบบ synchronous
                   ไปแบบ async ใหม่ โดยคงพฤติกรรมเดิม ผมอยากเชื่อได้ว่าทำถูก
                   เมื่อกลับมา
how:               /how เรายกเลิกการรันอย่างไร? มีปัญหา n+1 ตอนค้นหาการรันที่จะยกเลิกไหม?
why:               /why ทำไมยังไม่เปิด feature flag นี้?
architect:         ออกแบบเครื่องมือเก็บข้อมูลนี้ให้ได้ข้อมูลสำคัญและไม่มีผลบวกลวง ใช้ /architect
                   ก่อน
arena:             /arena ส่งคำขอของผมให้แต่ละทีมตรงตามต้นฉบับ อยากเทียบข้อเสนอของพวกเขา
                   กับของคุณ
swarm:             /swarm ตรวจทุก package ใต้ packages/ ด้วย check.sh ของแต่ละตัว
                   ผู้ทำงานหนึ่งตัวต่อ package รายงานเดียว
interrogate:       /interrogate รีวิว PR นี้
tdd:               /tdd ลงมือทำ
unslop:            ช่วย unslop และทำส่วนที่เพิ่งแก้ให้กระชับได้ไหม?
reflect:           /reflect งานนั้นนานเกินไป เก็บสิ่งที่เรียนรู้เพื่อไม่ให้รอบหน้า
                   ทำซ้ำ
correct:           /correct
show-me-your-work: /show-me-your-work เก็บบันทึกการตัดสินใจให้ผมรีวิวเมื่อกลับมา
automate-me:       /automate-me
```

</details>

<a id="the-poteto-agent-and-comment-sicko-subagents"></a>

## เอเจนต์ย่อย `poteto-agent` และ Comment Sicko

pstack มีเอเจนต์ย่อยที่ทำงานตามสไตล์ของผมตั้งแต่ต้นจนจบ เรียกจากเอเจนต์หลักด้วย [`subagent_type: "poteto-agent"`](./agents/poteto-agent.md) จะอ่าน `poteto-mode` ทั้งหมด รวมสารบัญหลักการในไฟล์ก่อนเริ่มงาน ถ้าแทนด้วย `generalPurpose` จะข้ามการอ่านนี้และอาจทำงานออกนอกแนวทาง

[`/poteto-mode`](./skills/poteto-mode/SKILL.md) และ [`subagent_type: "poteto-agent"`](./agents/poteto-agent.md) ผ่านตัวห่อเดียวกัน

pstack ยังมี [Comment Sicko](./agents/comment-sicko.md) ผู้รีวิวคอมเมนต์แบบอ่านอย่างเดียว ใช้เป็น `subagent_type: "Comment Sicko"` โดยปกติเรียกผ่าน [`/no-comments`](./skills/no-comments/SKILL.md) แทนการเรียกตรง

<a id="principles"></a>

## หลักการ

สกิลสั้น 24 ตัว ตัวละหนึ่งหลักการ `poteto-mode` มีสารบัญในไฟล์และอ่านเมื่อเริ่มงาน ไฟล์แยกช่วยให้สกิลอื่นอ้างชื่อหลักการได้ และให้สารบัญเชื่อมไปยังกฎฉบับเต็มแต่ละข้อ

<details>
<summary>หลักการทั้ง 24 ข้อ</summary>

| หลักการ | กลุ่ม | กฎ |
|---|---|---|
| [laziness-protocol](./skills/principle-laziness-protocol/SKILL.md) | พื้นฐาน | เน้นการลบและการเปลี่ยนแปลงที่เล็กที่สุดซึ่งแก้ปัญหาได้ |
| [foundational-thinking](./skills/principle-foundational-thinking/SKILL.md) | พื้นฐาน | ใช้ก่อนเขียนตรรกะ: เลือกชนิดข้อมูลและโครงสร้างหลัก จัดลำดับงานวางโครงกับฟีเจอร์ และดูว่างานที่ทำพร้อมกันใช้อะไรร่วมกัน วางโครงสร้างข้อมูลให้ถูกเพื่อให้โค้ดต่อจากนั้นชัดเจน |
| [redesign-from-first-principles](./skills/principle-redesign-from-first-principles/SKILL.md) | พื้นฐาน | ออกแบบใหม่ราวกับความต้องการนี้เป็นพื้นฐานตั้งแต่วันแรก แทนการต่อเติมภายหลัง |
| [attack-the-premise](./skills/principle-attack-the-premise/SKILL.md) | พื้นฐาน | ใช้เมื่อวิธีแก้ตั้งแต่สองแบบที่มีสมมติฐานร่วมล้มเหลวที่เกณฑ์เดียวกัน ตรวจว่าใครทำให้เกิดความไม่สมดุลก่อนลองครั้งถัดไป แล้วตั้งคำถามกับสมมติฐานนั้น แทนการแก้อีกแบบที่ยังเชื่อเหมือนเดิม |
| [subtract-before-you-add](./skills/principle-subtract-before-you-add/SKILL.md) | พื้นฐาน | ลบส่วนเกิน ตัวตรวจซ้ำ และการอ้างถึงส่วนที่เป็นเพียงโครงร่างก่อน แล้วสร้างต่อบนฐานที่ง่ายขึ้น |
| [minimize-reader-load](./skills/principle-minimize-reader-load/SKILL.md) | พื้นฐาน | นับชั้นระหว่างคำถามกับคำตอบ และสถานะที่ผู้อ่านต้องจำ ลดตัวห่อที่มีผู้เรียกเดียว และลดขอบเขตที่เปลี่ยนค่าได้ |
| [outcome-oriented-execution](./skills/principle-outcome-oriented-execution/SKILL.md) | พื้นฐาน | ใช้กับการเขียนใหม่และการย้ายระบบที่แบ่งระยะชัด มุ่งสู่สถาปัตยกรรมเป้าหมาย ไม่รักษาสถานะกลางด้วยโค้ดรองรับชั่วคราวที่ต้องทิ้ง |
| [experience-first](./skills/principle-experience-first/SKILL.md) | พื้นฐาน | เลือกประสบการณ์ที่ดีของผู้ใช้ก่อนความสะดวกในการสร้าง ส่งฟีเจอร์น้อยแต่เรียบร้อยแทนจำนวนมากที่ยังหยาบ |
| [exhaust-the-design-space](./skills/principle-exhaust-the-design-space/SKILL.md) | พื้นฐาน | สร้างต้นแบบ 2–3 ทางเลือกและเปรียบเทียบคู่กันก่อนเลือก |
| [build-the-lever](./skills/principle-build-the-lever/SKILL.md) | พื้นฐาน | ใช้กับทุกงานที่ไม่เล็กน้อย ไม่ใช่แค่งานจำนวนมาก ทั้งแก้ไข ย้ายระบบ วิเคราะห์ และตรวจ สร้างเครื่องมือที่ทำหรือพิสูจน์งาน (codemod สคริปต์ ตัวสร้าง หรือสกิลให้เอเจนต์ย่อยทำตาม) แทนทำด้วยมือ เพื่อให้ผู้รีวิวรันซ้ำได้ |
| [model-the-domain](./skills/principle-model-the-domain/SKILL.md) | สถาปัตยกรรม | แทนกฎของงานด้วยโครงสร้าง แทนเงื่อนไขที่กระจายหลายจุด |
| [boundary-discipline](./skills/principle-boundary-discipline/SKILL.md) | สถาปัตยกรรม | รวมการตรวจที่ขอบเขตระบบ (CLI การตั้งค่า เครือข่าย API ภายนอก) เชื่อชนิดข้อมูลภายใน และเก็บตรรกะธุรกิจในฟังก์ชันที่ไม่มีผลข้างเคียง |
| [type-system-discipline](./skills/principle-type-system-discipline/SKILL.md) | สถาปัตยกรรม | ทำให้สร้างสถานะผิดกฎไม่ได้ แยกชนิดพื้นฐานตามความหมายด้วย brand แยกวิเคราะห์ข้อมูลภายนอกที่ขอบเขต ไม่หลอก compiler ตรวจทุกกรณี และอิง schema ที่เป็นแหล่งหลัก |
| [make-operations-idempotent](./skills/principle-make-operations-idempotent/SKILL.md) | สถาปัตยกรรม | ทำให้จบที่สถานะเดียวกัน แม้รอบก่อนทำสำเร็จเพียงบางส่วน |
| [migrate-callers-then-delete-legacy-apis](./skills/principle-migrate-callers-then-delete-legacy-apis/SKILL.md) | สถาปัตยกรรม | ย้ายผู้เรียกและลบ API เก่าในรอบเดียว แทนการเก็บชั้นรองรับไว้ |
| [separate-before-serializing-shared-state](./skills/principle-separate-before-serializing-shared-state/SKILL.md) | สถาปัตยกรรม | เลิกใช้ร่วมก่อน จัดลำดับการเขียนด้วยโครงสร้างเฉพาะเมื่อจำเป็นจริงว่าต้องมีผู้เขียนร่วมเพียงตัวเดียว |
| [prove-it-works](./skills/principle-prove-it-works/SKILL.md) | ตรวจสอบ | ใช้หลังทำงานเสร็จ ก่อนประกาศว่าจบ ตรวจผลงานจริง (รันฟีเจอร์ อ่านค่าจริง ตรวจ diff) ไม่ใช้สิ่งแทน คำรายงานตัวเอง หรือ “คอมไพล์ผ่าน” |
| [fix-root-causes](./skills/principle-fix-root-causes/SKILL.md) | ตรวจสอบ | ไล่แต่ละอาการถึงต้นเหตุและแก้ตรงนั้น ทำให้เกิดซ้ำก่อน ถามว่าทำไมจนถึงสาเหตุ ไม่เพิ่มเงื่อนไขตรวจค่าว่างเพื่อกลบการล้มเหลว |
| [sequence-verifiable-units](./skills/principle-sequence-verifiable-units/SKILL.md) | ตรวจสอบ | ใช้กับงานหลายขั้น (การตรวจเป็นชุด การย้ายระบบ การแก้คล้ายกันหลายจุด) และการเรียง commit กับ PR แบ่งเป็นหน่วยเล็กที่ตรวจได้ ตรวจแต่ละหน่วยก่อนทำต่อ และจัดลำดับให้ผู้รีวิวเห็นหลักฐานต่อเนื่อง |
| [test-behavior-not-implementation](./skills/principle-test-behavior-not-implementation/SKILL.md) | ตรวจสอบ | ใช้เมื่อเขียน แก้ หรือเก็บ test เรียกโค้ดแบบผู้ใช้และเทียบผลกับค่าคาดหวังตรงตัว หากยังผ่านเมื่อทุกฟังก์ชันที่ import คืน undefined ให้เขียน assertion ใหม่หรือลบ test |
| [explain-the-number](./skills/principle-explain-the-number/SKILL.md) | ตรวจสอบ | ใช้ก่อนเชื่อ รายงาน หรือตัดสินใจจากตัวเลขที่วัด ทั้งความเร็วที่ดีขึ้นหรือแย่ลง throughput latency และผลประเมิน หาว่าอะไรจำกัดผล และตัดความเป็นไปได้ว่าวัดคนละสิ่งกับที่คิด |
| [guard-the-context-window](./skills/principle-guard-the-context-window/SKILL.md) | มอบหมายงาน | ส่งงานปริมาณมากให้เอเจนต์ย่อย เก็บสรุปในบทสนทนาหลักแทนข้อมูลดิบ |
| [never-block-on-the-human](./skills/principle-never-block-on-the-human/SKILL.md) | มอบหมายงาน | เดินหน้า นำเสนอผล และให้คนปรับทิศทางภายหลัง ขอการยืนยันเฉพาะการกระทำที่ย้อนกลับไม่ได้ |
| [encode-lessons-in-structure](./skills/principle-encode-lessons-in-structure/SKILL.md) | ปรับวิธีทำงาน | ฝังกฎเป็น lint, flag ใน metadata การตรวจขณะทำงาน หรือสคริปต์ แทนเพิ่มข้อความ |

</details>

<a id="not-shipped-here"></a>

## สิ่งที่ไม่ได้รวมมา

บางสิ่งที่ `poteto-mode` อ้างถึงไม่ได้รวมอยู่ในชุดนี้:

- `/deslop` และสกิล `deslop` อยู่ในปลั๊กอิน `cursor-team-kit`
- `control-cli` (สำหรับ CLI และ TUI) กับ `control-ui` (สำหรับเบราว์เซอร์ Electron และเว็บ) อยู่ใน `cursor-team-kit` เช่นกัน
- `/create-skill` เป็นคำสั่งในตัวของ Cursor และ Cursor มี `/babysit` ในตัวด้วย แต่ภายใน `poteto-mode` จะใช้ [แนวทาง babysit](./skills/poteto-mode/playbooks/babysit.md) แทนเมื่อถามสถานะ PR

ถ้าต้องการครบชุด ให้ติดตั้ง `cursor-team-kit` คู่กับ pstack

<a id="why-are-there-no-planning-skills"></a>

## ทำไมไม่มีสกิลวางแผน?

Cursor มีโหมดวางแผนที่ดีและใช้กับ pstack ได้ดีอยู่แล้ว แต่ส่วนตัวผมไม่เชื่อในการวางแผน ข้อกำหนดที่ดีที่สุดคือโค้ด หากอยากวางแผน [`/poteto-mode`](./skills/poteto-mode/SKILL.md) รองรับ แต่ไม่ใช่ค่าเริ่มต้น

<a id="make-it-yours"></a>

## ปรับให้เป็นสไตล์ของคุณ

`poteto-mode` เป็นสไตล์ของผม คุณอาจไม่ต้องการเหมือนกันทุกอย่าง

พิมพ์ [`/automate-me`](./skills/automate-me/SKILL.md) ระบบจะค้นบทสนทนาล่าสุด ร่างสกิล `<your-name>-mode` จากวิธีทำงานจริงของคุณ และใช้ pstack เป็นกลไกเบื้องหลัง คุณยังใช้ pstack เป็นฐานและมีสกิลเลือกเส้นทางของตัวเองคู่กับ `poteto-mode`

โมเดลปรับได้เช่นกัน พิมพ์ [`/setup-pstack`](./skills/setup-pstack/SKILL.md) ระบบตรวจโมเดลที่คุณใช้ได้แล้วเขียนกฎสั้นที่ใช้เสมอ เพื่อจับคู่แต่ละบทบาท (โค้ด การตัดสิน ทีมรีวิว) กับโมเดล ทุกสกิลอ่านกฎนี้และใช้ค่าเริ่มต้นที่เหมาะสมเมื่อไม่มีกฎ คุณจึงเปลี่ยนเฉพาะสิ่งที่ต้องการ

กฎที่เขียนก่อน 0.15.3 จะตรึงโมเดลเริ่มต้นรุ่นเก่า ลบบรรทัดของบทบาทเหล่านั้นหรือลบไฟล์ แล้วเรียก `/setup-pstack` ใหม่ การเรียกซ้ำจะเก็บบทบาทที่เลือกโมเดลต่างจากค่าเริ่มต้น

<a id="automations"></a>

## ระบบอัตโนมัติ

pstack มี [แพ็กระบบอัตโนมัติ benny](./automations/benny/) ที่ยังไม่เปิดใช้งาน benny คัดกรองรายงานปัญหาจาก Slack จากนั้นทำให้บั๊กที่ยืนยันแล้วเกิดซ้ำและแก้ด้วยหลักฐาน UI จริง ไฟล์เหล่านี้ไม่ได้ลงทะเบียนเป็นสกิลที่เรียกด้วย slash

หากต้องการตั้งค่า ให้ Cursor อ่าน [`FOR_AGENTS.md`](./automations/benny/FOR_AGENTS.md) ระบบจะคัดลอกแพ็กไปที่ `.cursor/automations/benny/` ใน repository เป้าหมาย เปิด pstack เพื่อใช้สกิลร่วม และเก็บการตั้งค่าของผู้ใช้ไว้นอกแพ็กที่คัดลอก

<a id="license"></a>

## ใบอนุญาต

MIT
