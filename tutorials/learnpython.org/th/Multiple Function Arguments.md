Every function in Python สามารถรับจำนวนอาร์กิวเมนต์ที่กำหนดไว้ล่วงหน้า ถ้าประกาศในรูปแบบปกติเช่นนี้:

เป็นไปได้ที่จะประกาศฟังก์ชันที่สามารถรับจำนวนอาร์กิวเมนต์ที่เปลี่ยนแปลงได้ โดยใช้ไวยากรณ์ต่อไปนี้:

ตัวแปร "therest" คือ รายการของตัวแปรที่จะรับอาร์กิวเมนต์ทั้งหมดที่ถูกส่งเข้าสู่ฟังก์ชัน "foo" หลังจาก 3 อาร์กิวเมนต์แรก ดังนั้นการเรียกใช้ `foo(1, 2, 3, 4, 5)` จะพิมพ์ออกมาตามนี้:

ยังสามารถส่งอาร์กิวเมนต์ไปยังฟังก์ชันโดยใช้คีย์เวิร์ด เพื่อที่ว่าลำดับของอาร์กิวเมนต์จะไม่สำคัญ โดยใช้ไวยากรณ์ต่อไปนี้ โค้ดต่อไปนี้จะให้ผลลัพธ์ดังนี้: 
```The sum is: 6
    Result: 1```

ฟังก์ชัน "bar" รับ 3 อาร์กิวเมนต์ หากได้รับอาร์กิวเมนต์ "action" เพิ่มเติม และอาร์กิวเมนต์นั้นแนะนำให้ทำการบวกตัวเลข จะทำการพิมพ์ผลรวมออกมา มิฉะนั้น ฟังก์ชันยังรู้ว่าต้องส่งคืนอาร์กิวเมนต์ตัวแรก หากค่าของพารามิเตอร์ "number" ที่ถูกส่งเข้าฟังก์ชันเท่ากับ "first"

Exercise
--------

เติมฟังก์ชัน `foo` และ `bar` เพื่อให้สามารถรับจำนวนอาร์กิวเมนต์ที่เปลี่ยนแปลงได้ (3 อาร์กิวเมนต์หรือมากกว่า)
ฟังก์ชัน `foo` ต้องส่งคืนจำนวนของอาร์กิวเมนต์เพิ่มเติมที่ได้รับ
ฟังก์ชัน `bar` ต้องส่งคืน `True` หากอาร์กิวเมนต์ที่มีคีย์เวิร์ด `magicnumber` มีค่าเป็น 7 และ `False` หากไม่ใช่