# Day-09_10
MongoDB

Database:UniDB
Collection:students

![Screenshot 2025-04-28 003017](https://github.com/user-attachments/assets/a29aa453-7a94-4f98-9649-a4b79aa9c8b9)


01/Insert one data set using db.students.insertOne() query.

![Screenshot 2025-04-28 005905](https://github.com/user-attachments/assets/ddba584e-ab67-4096-9905-ec3c66e15598)


02/Insert data set using db.studentsMany() query.

![Screenshot 2025-04-28 010744](https://github.com/user-attachments/assets/8a0bd840-fd85-47a4-948c-34334f6ccec7)
![Screenshot 2025-04-28 010801](https://github.com/user-attachments/assets/da3a7693-1ac6-4c3c-b628-ac9fe0eb83d7)

# Updated data collection

![Screenshot 2025-04-28 011217](https://github.com/user-attachments/assets/eb0a90ac-c78a-4fb5-984d-ad88413c8f78)
![Screenshot 2025-04-28 011253](https://github.com/user-attachments/assets/efc8db93-24ab-493d-b8a3-6a213e53246e)


# db.students.find() query

1/Filter only name and age.

Project --> {name:1,age:1,_id:0}

![Screenshot 2025-04-28 011831](https://github.com/user-attachments/assets/91b20cd7-24dd-4c9f-a248-8989c0dc79ae)


2/Find the details whose regno is "2021IT002".

{regno:"2021IT002"}

![Screenshot 2025-04-28 012122](https://github.com/user-attachments/assets/3158c649-6400-4d79-ac55-4b5a8b217760)

shell query:

db.students.find({"regno":"2021IT002"})

![Screenshot 2025-04-28 012453](https://github.com/user-attachments/assets/048aef24-9b47-4d5d-ac5f-eb541e94f062)



3/Find female students details.

{gender:"Female"}

![Screenshot 2025-04-28 012248](https://github.com/user-attachments/assets/7b3edde1-f8b4-443d-8a22-dad5f1676e6f)

shell query:

db.students.find({gender:"Female"})

![Screenshot 2025-04-28 012544](https://github.com/user-attachments/assets/b5624ac4-d73e-4c39-b3ce-4a3a9261a58f)



4/Find the students whose age is greater than 24.

{age:{$gt:24}}

![Screenshot 2025-04-28 012744](https://github.com/user-attachments/assets/d639b75c-0ae8-45b4-a4b8-a743c6cdea35)

shell query:

db.students.find({age:{$gt:24}})

![Screenshot 2025-04-28 012822](https://github.com/user-attachments/assets/cde21cdf-1e5f-4cfc-b3e1-c638b0484e8b)




5/Find the details of students that have skills in "MongoDB".

{skills:{$in:['MongoDB']}}

![Screenshot 2025-04-28 013003](https://github.com/user-attachments/assets/ec964d64-00ad-4f6b-ab70-40d743ab152f)


shell query:

db.students.find({skills:{$in:['MongoDB']}})

![Screenshot 2025-04-28 013103](https://github.com/user-attachments/assets/c1271784-b511-4bae-b336-74c32d6610bd)


6/Find the students that have skills in "MongoDB" or "PHP".

{skills:{$in:['MongoDB','PHP']}}

![Screenshot 2025-04-28 013255](https://github.com/user-attachments/assets/ab269a91-5f81-447d-8c95-98b588753915)
![Screenshot 2025-04-28 013314](https://github.com/user-attachments/assets/6c8b07ea-19fd-4951-af27-be48307c1a71)


shell query:

db.students.find({skills:{$in:['MongoDB','PHP']}})

![Screenshot 2025-04-28 013437](https://github.com/user-attachments/assets/b71ee987-cfd2-47e3-bee3-f2a4dd6fdbe2)



7/Find the details of first female student.

shell query:

db.students.findOne({gender:"Female"})

![Screenshot 2025-04-28 013613](https://github.com/user-attachments/assets/3ce2cfe9-3294-4dd0-9bcf-8775602bb704)



8/Sort the details by gpa ascending order.

sort --> {gpa:1}

![Screenshot 2025-04-28 013908](https://github.com/user-attachments/assets/a687f239-d0a2-44bf-baa3-1270a3901c82)
![Screenshot 2025-04-28 013934](https://github.com/user-attachments/assets/9d468caf-c66e-4f7c-8905-11566c33d216)


shell query:
db.students.find().sort({gpa:1})

![Screenshot 2025-04-28 014121](https://github.com/user-attachments/assets/41db1ea7-bf8c-41c6-97eb-3945a4142243)
![Screenshot 2025-04-28 014138](https://github.com/user-attachments/assets/b2a8fb79-0c26-45bb-a985-44c0e982adb7)
![Screenshot 2025-04-28 014153](https://github.com/user-attachments/assets/25009d62-71fc-4d9c-aac0-7ec6628612ce)




9/Sort the details by gpa descending order.

sort --> {gpa:-1}

![Screenshot 2025-04-28 021929](https://github.com/user-attachments/assets/21e1adba-7026-485b-9edd-82cedf04a826)
![Screenshot 2025-04-28 021859](https://github.com/user-attachments/assets/95d6d5ab-5e3c-499d-b35b-ae503e55d223)

shell query:
db.students.find().sort({gpa:-1})

![Screenshot 2025-04-28 022127](https://github.com/user-attachments/assets/245412df-9036-4869-9ebe-98cfd274ccf3)
![Screenshot 2025-04-28 022142](https://github.com/user-attachments/assets/2bf54039-a33e-410a-94e5-d8b0b191105c)
![Screenshot 2025-04-28 022201](https://github.com/user-attachments/assets/5df6a91a-ddce-435c-9a8c-e692b57233b0)



10/Sort details by GPA and name in ascending order.

sort --> {gpa:1,name:1}

![Screenshot 2025-04-28 022401](https://github.com/user-attachments/assets/f195afab-7244-48c4-972d-44894761b273)
![Screenshot 2025-04-28 022419](https://github.com/user-attachments/assets/4ed846f5-527c-4f69-8922-31adf93d1c8d)
![Screenshot 2025-04-28 022437](https://github.com/user-attachments/assets/4f169aa7-8607-4d8d-860c-184bd6b190a0)


shell query:

db.students.find().sort({gpa:1,name:1})

![Screenshot 2025-04-28 022503](https://github.com/user-attachments/assets/d861af76-573a-40c2-927a-524618f7bdd9)
![Screenshot 2025-04-28 022518](https://github.com/user-attachments/assets/39a558c0-23cf-4805-b26f-24e60104709c)
![Screenshot 2025-04-28 022532](https://github.com/user-attachments/assets/8289340d-8bc7-4c9c-93a4-6a264d846b23)




11/Sort by gpa ascending order who are stydying "IT" as degree.

query --> {degree:"IT"}

sort--> {gpa:1}

![Screenshot 2025-04-28 022818](https://github.com/user-attachments/assets/65731840-90ed-4219-9b5c-ea16dd6abd59)
![Screenshot 2025-04-28 022650](https://github.com/user-attachments/assets/cfd98add-1ac1-4f44-80b5-294255d129cc)


shell query:

db.students.find({degree:"IT"}).sort({gpa:1})

![Screenshot 2025-04-28 022731](https://github.com/user-attachments/assets/d8d6e0d5-ec43-4099-844b-fa2a45a874c4)
![Screenshot 2025-04-28 022743](https://github.com/user-attachments/assets/c60cc6f4-42da-4368-98a5-8ac9a11c5cc2)




12/Sort by gpa ascending order who are stydying "IT" as the degree and gender is "Male".

query --> {degree:"IT",gender:"Male"}

sort--> {gpa:1}

![Screenshot 2025-04-28 022917](https://github.com/user-attachments/assets/0a12383d-252a-4fa9-adf6-32e3aaa2be8c)
![Screenshot 2025-04-28 022932](https://github.com/user-attachments/assets/bfcf87b7-5614-45c9-a06b-0d932511b7c7)

shell query:

db.students.find({degree:"IT",gender:"Male"}).sort({gpa:1})

![Screenshot 2025-04-28 023100](https://github.com/user-attachments/assets/e3958dc7-4f0f-4769-9950-84a0b17d0fbc)
![Screenshot 2025-04-28 023121](https://github.com/user-attachments/assets/1a3ad5a9-5970-4c64-a524-c5fefbbdcd8c)


















