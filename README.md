

## Connect_Wifi()
กรุณาไปเติมโค้ดให้ครบด้วย
``` c
// src/main.cpp
const char *ssid = "Your Wifi Name";
const char *password = "Your Wifi Password";
```

## Define
ไปเปลี่ยนตาม pin ที่น้องต่อด้วย
``` c
// src/main.cpp
#define red <led red pin>
#define yellow <led yellow pin>
#define green <led green pin>
#define ldr <ldr pin>
#define button <button pin>

#define light <แสดงมันมืด มีค่าเท่าไหร่>
```

## Point
ไปเปลี่ยนตาม point ของเราด้วย (point == กลุ่มที่)
``` c
// src/traffic.h
const String point = "กลุ่มที่";
const int nearby_1 = "กลุ่มใกล้เคียง (กลุ่มที่ +-1)";
const int nearby_2 = "กลุ่มใกล้เคียง (กลุ่มที่ +-1)";
```

## GET_traffic
อยู่ใน `src/traffic.h`

จะขาดส่วน แสดงผล ซึ่งอาจจะต้องใช้ `JsonArray`, `JsonObject`, `JsonPair` (แล้วแต่กลุ่มเลย บางกลุ่มอาจไม่ต้องใช้ก็ได้)

สามารถดูตัวอย่างและนำมาปรับใช้ได้จาก[ที่นี่](https://stackoverflow.com/questions/71023794/getting-json-keys-from-an-array-from-an-object-using-arduinojson)

## POST_traffic
อยู่ใน `src/traffic.h`

แทบไม่ต่างจากในตัวอย่างเลย เพิ่มเติมคือมันจะรับตัวแปร `String led` ที่เป็นตัวบอกว่า led ตอนนี้สีอะไร ดังนั้นน้องเหลือแค่เติมการใส่ข้อมูลลง `doc` ให้ถูกต้องก็เพียงพอ

เวลานำไปใช้งานก็จะใช้ เช่น `POST_traffic("green");` เพื่อ POST บอกว่าตอนนี้สีเขียวนะ (ทั้งนี้ก็แล้วแต่การออกแบบของแต่ละกลุ่ม เปลี่ยนแปลงได้เลยตามใจชอบ)

## void loop
อยู่ใน `src/main.cpp`
พี่ออกแบบเป็นการทำ state 1 2 3 (แต่ละอันแทนอะไรลองคิดเอานะครับ)

ทั้งนี้น้องๆสามารถเปลี่ยนแปลงได้ตามใจชอบเลย อาจไม่ใช้ state ก็ได้เช่นกัน

# DOC
[Google Doc](https://docs.google.com/document/d/1WDnPvVdG5Sv5STsbMxcOpFad4R2GMMGk-eMUh6Ukz0c/edit?usp=sharing)
