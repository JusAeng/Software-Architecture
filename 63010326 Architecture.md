# Architectural Patterns

## Audacity

### Purpose
ที่ใช้บันทึกเสียงและตัดต่อเสียง มิกซ์เสียง ซึ่งเป็นที่นิยมมากในกลุ่ม Sound Engineer
ยกตัวอย่าง Feature ของ Audacity
- การแก้ไขไฟล์เสียงหลายรูปแบบ เช่น MP3, MP2, AIFF, FLAC, WAV
- การเปลี่ยนความเร็วหรือระดับเสียง
- ความสามารถในการบันทึกเสียงสดและการเล่นเสียงบนพีซี
- ทำซ้ำ ตัด ผสม และต่อกิ่งเอกสารเสียงต่างๆ เข้าด้วยกัน
- บันทึกตัวจับเวลาที่ช่วยให้ผู้ใช้สามารถกำหนดเวลาเมื่อการบันทึกเริ่มต้นและสิ้นสุด
- ลด noise
- การลดเสียงและการแยกเสียงเพื่อสร้างแทร็กเสียงหรือแทร็กคาราโอเกะที่แยกออกมา

### Architectural Styles
<img
  src="https://www.aosabook.org/images/audacity/Layers.png">

asdfasdf

### 3 Quality Attribute Scanario
1. <br />
   Source of stimulus:<br />
   Stimulus:<br />
   Environment:<br />
   Artifact:<br />
   Response:<br />
   Response measure:<br />

2. <br />
   Source of stimulus:<br />
   Stimulus:<br />
   Environment:<br />
   Artifact:<br />
   Response:<br />
   Response measure:<br />

3. <br />
   Source of stimulus:<br />
   Stimulus:<br />
   Environment:<br />
   Artifact:<br />
   Response:<br />
   Response measure:<br />
   
Ref : https://www.aosabook.org/en/audacity.html

## Matplotlib
เป็น Library ตัวนึงที่นิยมใช้กันอย่างแพร่หลายในภาษา Python มีความยืดหยุ่นในวิธีการสร้างพล็อต

### Purpose
เพื่อ Visualize data ให้เห็นภาพที่ชัดเจนทั้งในรูปแบบ2Dและ3D เหมาะสำหรับการเรียนรู้ Machine learning

### Architectural Styles
Matplotlib ประกอบด้วย 3 Layer หลัก
- Backend Layer มี 3 Abstract class คือ
  1. FigureCanvas ใช้กำหนดพื้นที่ที่ร่างถูกวาด
  2. Renderer ใช้เป็นเครื่องมือในการวาดบน FigureCanvas
  3. Event ใช้จัดการอินพุตของผู้ใช้ เช่น การกดแป้นพิมพ์และการคลิกเมาส์
 
-คล้ายกับที่เราวาดบนกระดาษ พิจารณาว่าคุ ณต้องการวาดภาพวาด คุณได้รับกระดาษเปล่า (FigureCanvas) และแปรง (Renderer) คุณถามเพื่อนของคุณว่าจะวาดอะไร (กิจกรรม)
- Artist Layer ประกอบด้วย object 1 ตัว เรียก Artist
- Scripting Layer คือ matplotlib interface คือ Layer ที่เราใช้ติดต่อกับตัวmatplotlib

### 3 Quality Attribute Scanario
1. Useability<br />
   Source of stimulus: User<br />
   Stimulus: เรียนรู้วิธีการใช้งาน<br />
   Environment: Runtime<br />
   Artifact: System<br />
   Response: โค้ดทีอ่านแล้วเข้าใจง่าย<br />
   Response measure: knowledge<br />

2. Integrability<br />
   Source of stimulus: Component<br />
   Stimulus: Update version<br />
   Environment: Development<br />
   Artifact: System<br />
   Response: Complete?<br />
   Response measure: ความเข้าใจง่ายของcode<br />

3. Modifiablity<br />
   Source of stimulus: ผู้สร้าง<br />
   Stimulus: Edit<br />
   Environment: Runtime<br />
   Artifact: Code<br />
   Response: ผลการเปลี่ยนแปลง<br />
   Response measure: ความซับซ้อนApplication<br />
   
Ref : https://towardsdatascience.com/understanding-the-structure-of-matplotlib-23b97f507fac



## Matplotlib


### Purpose


### Architectural Styles


### 3 Quality Attribute Scanario
1. Useability<br />
   Source of stimulus: User<br />
   Stimulus: เรียนรู้วิธีการใช้งาน<br />
   Environment: Runtime<br />
   Artifact: System<br />
   Response: โค้ดทีอ่านแล้วเข้าใจง่าย<br />
   Response measure: knowledge<br />

2. Integrability<br />
   Source of stimulus: Component<br />
   Stimulus: Update version<br />
   Environment: Development<br />
   Artifact: System<br />
   Response: Complete?<br />
   Response measure: ความเข้าใจง่ายของcode<br />

3. Modifiablity<br />
   Source of stimulus: ผู้สร้าง<br />
   Stimulus: Edit<br />
   Environment: Runtime<br />
   Artifact: Code<br />
   Response: ผลการเปลี่ยนแปลง<br />
   Response measure: ความซับซ้อนApplication<br />
   
Ref : https://towardsdatascience.com/understanding-the-structure-of-matplotlib-23b97f507fac

