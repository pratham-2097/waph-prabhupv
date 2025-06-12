# WAPH – Web Application Programming and Hacking  
**Instructor:** Dr. Phu Phung  
**Lab 1 – Foundations of the Web**  
**Student:** Pratham Prabhu  
**Email:** prabhupv@mail.uc.edu  



---

## 📌 Overview

This lab explores the foundational layers of the web, emphasizing the HTTP protocol and simple server-side programming. It is divided into two main parts:  

- **Part I:** Capturing and analyzing HTTP traffic using Wireshark and Telnet to understand how web clients and servers exchange data.
- **Part II:** Building basic web applications using **C (CGI programming)** and **PHP**, along with examining the behavior of **GET** and **POST** requests.

Through this lab, I learned how to:
- Inspect low-level HTTP message structure
- Write server-side applications in C and PHP
- Understand client-server interactions through web forms and user input handling

🔗 **GitHub Folder Link:** [https://github.com/prabhupv/waph-prabhupv/tree/main/labs/lab1](https://github.com/prabhupv/waph-prabhupv/tree/main/labs/lab1)

---

## 🔬 Part I – The Web and HTTP Protocol

###  Task 1: Using Wireshark to Analyze HTTP Traffic

**Tools Used:** Wireshark  
**Goal:** Capture and inspect HTTP GET and Response packets to understand request headers, response codes, and payloads.

Steps:
- Enabled Wireshark filtering: `http`
- Opened a webpage in a browser to trigger HTTP activity
- Captured and analyzed packets

**Findings:**
- The HTTP request includes the method (`GET`), resource path, and headers such as `Host`, `User-Agent`, etc.
- The HTTP response includes status codes like `200 OK`, headers (e.g., `Content-Type`, `Content-Length`), and HTML content.

**Screenshots:**
- ![](images/1.png)  
  *Figure 1: HTTP GET request details captured by Wireshark*

- ![](images/2.png)  
  *Figure 2: HTTP response message including headers and HTML content*

- ![](images/3.png)  
  *Figure 3: Full HTTP stream including request and response*

---

### Task 2: Sending HTTP Manually via Telnet and Capturing with Wireshark

**Tools Used:** Telnet + Wireshark  
**Goal:** Manually craft an HTTP request and analyze how it appears in Wireshark.

Command used:
```bash
telnet example.com 80
GET / HTTP/1.0
Host: example.com
