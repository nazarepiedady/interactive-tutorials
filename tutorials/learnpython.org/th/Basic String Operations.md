Strings เป็นกลุ่มของข้อความ สามารถกำหนดได้เป็นอะไรก็ตามที่อยู่ระหว่างเครื่องหมายคำพูด:

astring = "Hello world!"
astring2 = 'Hello world!'

จากตัวอย่างข้างต้น สิ่งแรกที่คุณได้เรียนรู้คือการพิมพ์ประโยคง่ายๆ ประโยคนี้ถูกจัดเก็บโดย Python เป็นสตริง อย่างไรก็ตาม แทนที่จะพิมพ์สตริงออกมาทันที เราจะสำรวจสิ่งต่างๆ ที่คุณสามารถทำกับสตริงได้
คุณสามารถใช้เครื่องหมายคำพูดเดี่ยวเพื่อกำหนดสตริงได้เช่นกัน แต่คุณจะพบปัญหาหากค่าที่จะกำหนดเองมีเครื่องหมายคำพูดเดี่ยวอยู่ข้างใน ยกตัวอย่างเพื่อกำหนดสตริงในวงเล็บเหล่านี้ (เครื่องหมายคำพูดเดี่ยวคือ ' ') คุณจำเป็นต้องใช้เครื่องหมายคำพูดคู่เท่านั้นเช่นนี้

astring = "Hello world!"
print("single quotes are ' '")

print(len(astring))

คำสั่งนี้พิมพ์เลข 12 ออกมา เพราะ "Hello world!" มีความยาว 12 ตัวอักษร รวมถึงเครื่องหมายวรรคตอนและช่องว่าง

astring = "Hello world!"
print(astring.index("o"))

คำสั่งนี้พิมพ์เลข 4 ออกมา เพราะตำแหน่งที่เจออักษร "o" ครั้งแรกอยู่ห่างจากอักษรตัวแรก 4 ตัวอักษร สังเกตว่าในวลีนี้มี 'o' อยู่สองตัว - วิธีนี้จะรู้จักเฉพาะตัวแรก

แต่ทำไมมันไม่พิมพ์เลข 5 ออกมา? "o" ไม่ใช่ตัวอักษรอันดับที่ห้าในสตริงเหรอ? เพื่อทำให้สิ่งนี้ง่ายขึ้น Python (และภาษาโปรแกรมอื่นๆ ส่วนใหญ่) เริ่มนับจาก 0 แทนที่ 1 ดังนั้น index ของ "o" คือ 4

astring = "Hello world!"
print(astring.count("l"))

สำหรับคนที่ใช้ฟอนต์แปลกๆ นั่นคือตัว L เล็ก ไม่ใช่เลขหนึ่ง คำสั่งนี้จะนับจำนวนตัวอักษร l ในสตริง ดังนั้นมันควรจะแสดงเลข 3

astring = "Hello world!"
print(astring[3:7])

คำสั่งนี้พิมพ์ชิ้นส่วนของสตริง โดยเริ่มที่ index 3 และสิ้นสุดที่ index 6 แต่ทำไมถึงเป็น 6 ไม่ใช่ 7? อีกครั้ง ภาษาการโปรแกรมส่วนใหญ่ทำแบบนี้ - มันทำให้การคำนวณภายในวงเล็บง่ายขึ้น

ถ้าคุณใส่เลขหนึ่งตัวในวงเล็บ มันจะให้ตัวอักษรเดียวที่ตำแหน่งนั้น ถ้าคุณละเว้นเลขตัวแรกแต่ใส่โคลอน มันจะให้ชิ้นส่วนจากเริ่มต้นถึงเลขที่คุณใส่ไว้ ถ้าคุณละเว้นเลขตัวที่สอง มันจะให้ชิ้นส่วนจากเลขตัวแรกถึงจบ

คุณยังสามารถใส่เลขติดลบภายในวงเล็บได้อีกด้วย มันเป็นวิธีง่ายๆ ในการเริ่มจากจบของสายอักขระแทนที่จะเป็นเริ่มต้น ด้วยวิธีนี้ -3 หมายถึง "อักขระที่สามจากจบ"

astring = "Hello world!"
print(astring[3:7:2])

คำสั่งนี้พิมพ์อักขระของสายอักขระจาก 3 ถึง 7 ข้ามหนึ่งตัวอักษร นี่คือไวยากรณ์ที่ขยายเพิ่มเติม ช่วงโครงสร้างทั่วไปคือ [start:stop:step]

astring = "Hello world!"
print(astring[3:7])
print(astring[3:7:1])

สังเกตว่าทั้งสองคำสั่งให้ผลลัพธ์แบบเดียวกัน

ไม่มีฟังก์ชัน เช่น strrev ในภาษา C เพื่อย้อนกลับสายอักขระ แต่ด้วยไวยากรณ์ประเภทชิ้นส่วนที่กล่าวมาก่อนหน้านี้ คุณสามารถย้อนกลับสายอักขระได้ง่ายๆ ดังนี้

astring = "Hello world!"
print(astring[::-1])

คำสั่งนี้

astring = "Hello world!"
print(astring.upper())
print(astring.lower())

คำสั่งเหล่านี้สร้างสายอักขระใหม่ที่ตัวอักษรถูกเปลี่ยนเป็นตัวพิมพ์ใหญ่และพิมพ์เล็กตามลำดับ

astring = "Hello world!"
print(astring.startswith("Hello"))
print(astring.endswith("asdfasdfasdf"))

สิ่งนี้ใช้เพื่อกำหนดว่าสายอักขระเริ่มด้วยอะไรหรือสิ้นสุดด้วยอะไรตามลำดับ คำสั่งแรกจะพิมพ์ True เนื่องจากสายอักขระเริ่มด้วย "Hello" ในขณะที่คำสั่งที่สองจะพิมพ์ False เพราะสายอักขระไม่ได้สิ้นสุดด้วย "asdfasdfasdf" แน่นอน

astring = "Hello world!"
afewwords = astring.split(" ")

คำสั่งนี้จะแยกสายอักขระเป็นกลุ่มอักขระหลายสายที่ถูกรวมกันอยู่ในรายการ เนื่องจากตัวอย่างนี้แยกที่ช่องว่าง รายการแรกในรายการจะเป็น "Hello" และรายการที่สองจะเป็น "world!"

Exercise
--------

ลองแก้ไขโค้ดเพื่อพิมพ์ข้อมูลที่ถูกต้องโดยการเปลี่ยนสตริง