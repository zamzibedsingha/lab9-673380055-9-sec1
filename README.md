# Lab 9 — Transaction in Spring Boot

โปรเจกต์นี้เป็นการทดลองใช้งาน **Transaction ใน Spring Boot** 
โดยพัฒนา REST API สำหรับระบบฝากเงินอย่างง่าย 
ใช้ Spring Boot, Spring Data JPA และ PostgreSQL

จุดประสงค์หลักของ Lab นี้คือการศึกษาการทำงานของ `@Transactional`
และการทำงานแบบ **Commit / Rollback** เมื่อเกิดข้อผิดพลาดระหว่างการฝากเงิน

---

## 📌 Objectives

โปรเจกต์นี้มีวัตถุประสงค์เพื่อศึกษา

- การสร้าง REST API ด้วย Spring Boot
- การเชื่อมต่อ PostgreSQL ผ่าน Spring Data JPA
- การสร้าง Entity และความสัมพันธ์ระหว่าง Entity
- การใช้งาน `@Transactional`
- การทำงานของ Transaction แบบ **All or Nothing**
- ความแตกต่างระหว่างการทำงานที่มีและไม่มี `@Transactional`
- การทำงานของ **COMMIT** และ **ROLLBACK**

---

## 🛠 Technologies

- Java 17+
- Spring Boot 3.x
- Spring Web
- Spring Data JPA
- PostgreSQL
- Maven
- Postman

---

## 📂 Project Structure

```text
src/main/java/com/example/lab9
├── controller
│   └── AccountController.java
│
├── service
│   ├── AccountService.java
│   └── DepositService.java
│
├── repository
│   ├── AccountRepository.java
│   └── DepositRepository.java
│
└── model
    ├── Account.java
    └── DepositTransaction.java
