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

Sercive-Oriented Architecture <br>
Audacity ใช้ libraries มากมาย Libraryหลักที่ใช้สำหรับติดต่อUser นั้นคือ wxWidgets ซึ่งเป็นแพลตฟอร์มข้ามแพลตฟอร์ม (Windows, Mac, Linux) ซึงจากภาพด้านบนแสดงถึงการจัดวาง
Library ของ Audacity

### 3 Quality Attribute Scanario
1. Useability<br />
   Source of stimulus: User<br />
   Stimulus: เรียนรู้ระบบsoftware<br />
   Environment: Runtime<br />
   Artifact: GUI<br />
   Response: ใช้งานได้ง่าย<br />
   Response measure: Knowledge<br />

2. Performance<br />
   Source of stimulus: User<br />
   Stimulus: ใช้งานมิกซ์เสียง<br />
   Environment: การทำงานบนApplication<br />
   Artifact: ส่วนของระบบที่ใช้มิกซ์เสียง<br />
   Response: System resource<br />
   Response measure: ใช้เวลาเร็วขึ้นในการมิกซ์<br />

3. Modifiability <br />
   Source of stimulus: ผู้สร้าง<br />
   Stimulus: เพิ่ม feature<br />
   Environment: Runtime<br />
   Artifact: Code ,UI<br />
   Response: ผลทดสอบจากการเปลี่ยนแปลง<br />
   Response measure: ผลตอบรับผู้ใช้งาน<br />
   
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
   Response: ความเปลี่ยนแปลงที่เข้ากับระบบ<br />
   Response measure: ความเข้าใจง่ายของcode<br />

3. Modifiablity<br />
   Source of stimulus: ผู้สร้าง<br />
   Stimulus: Edit<br />
   Environment: Runtime<br />
   Artifact: Code<br />
   Response: ผลการเปลี่ยนแปลงโค้ด<br />
   Response measure: ความซับซ้อนApplication<br />
   
Ref : https://towardsdatascience.com/understanding-the-structure-of-matplotlib-23b97f507fac



## Yesod


### Purpose
Web framework ที่พัฒนาโดยภาษาHaskell ซึ่งเป็น Functional Programming Language พัฒนาขึ้นเพื่อย่อScaleของโค้ด โดยโค้ดถูกCompile ด้วยCompiler แทนLibraryภายนอก 

### Architectural Styles
<img src="https://www.aosabook.org/images/yesod/overview.png">
MVC (Model View Controller)
- Model = Database
- View = Shakespeare Templates
- Yesod app = Controller

### 3 Quality Attribute Scanario
1. Security<br />
   Source of stimulus: ผู้ไม่ประสงค์ดี<br />
   Stimulus: การโจมตีจากผู้ไม่ประสงค์ดี<br />
   Environment: System<br />
   Artifact: Data<br />
   Response: ข้อมูลถูกป้องกันไม่ให้ผู้ไม่ประสงค์ดีเข้าถึงได้<br />
   Response measure: อัตราส่วนการป้องกันสำเร็จ<br />

2. Testability <br />
   Source of stimulus: Tester<br />
   Stimulus: ทดสอบฟังก์ชัน<br />
   Environment: All system<br />
   Artifact: System<br />
   Response: ผลจากCompiler<br />
   Response measure: ฟังก์ชันที่บัค<br />

3. Performance<br />
   Source of stimulus: User<br />
   Stimulus: เรียกใช้งานหลายfunction<br />
   Environment: การทำงานของApplication<br />
   Artifact: functional system<br />
   Response: resorceที่ใช้งาน<br />
   Response measure: ใช้resourceลดลง<br />
 

   


