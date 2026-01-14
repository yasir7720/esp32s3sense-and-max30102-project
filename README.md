# esp32s3sense-and-max30102-project
A hybrid health monitoring system combining real-time AI emotion analysis with biometric data (BPM &amp; SpO2) using ESP32S3 Sense and MAX30102.

# AI-Powered Physiological & Emotional Health Monitor

![Project Status](https://img.shields.io/badge/Status-Completed-success)
![Python](https://img.shields.io/badge/Python-3.10+-blue)
![Hardware](https://img.shields.io/badge/Hardware-ESP32--S3-red)
![AI](https://img.shields.io/badge/AI-Roboflow-purple)

## About the Project

Bu proje,Nabız & SpO2 ve yapay zeka destekli duygu analizini birleştiren hibrit bir sağlık izleme sistemidir.

Sistem, Seeed Studio XIAO ESP32S3 Sense kartı kullanarak Wi-Fi üzerinden görüntü aktarımı yapar ve aynı anda MAX30102 sensörü ile parmaktan nabız verisi okur. Bilgisayarda çalışan Python yazılımı, bu verileri işler, Roboflow tabanlı yapay zeka modeli ile yüz ifadesinden duygu analizi yapar ve fiziksel + duygusal stresi ölçerek modern bir arayüzde sunar.

This project is a hybrid health monitoring system that combines biometric data (BPM & SpO2) with AI-powered emotion analysis.

## Features

* ** Gerçek Zamanlı Fizyolojik Takip
    * Nabız (BPM) ölçümü.
    * Kandaki Oksijen (SpO2) ölçümü.
* ** Yapay Zeka Duygu Analizi:
    * Yüz ifadelerinden anlık duygu tespiti (Mutlu, Üzgün, Kızgın, Korku, Şaşkın, Nötr).
    * **Roboflow Inference motoru entegrasyonu.
* ** Kablosuz Görüntü Aktarımı:
    * ESP32-S3 Sense üzerinden MJPEG video akışı.
* ** Modern Arayüz (Medical HUD):
    * OpenCV tabanlı "Glassmorphism" tasarımı.
    * Dinamik ilerleme çubukları (Progress Bars).
    * Anti-Flicker (Görüntü Sabitleme) teknolojisi.
* ** Hibrit Stres Analizi:
    * Yüksek nabız ve negatif yüz ifadelerini birleştirerek stres seviyesi tahmini.


## Hardware Requirements

1.  **Seeed Studio XIAO ESP32S3 Sense (Kamera Modülü Dahil)
2.  **MAX30102 (Nabız ve Oksijen Sensörü)
3.  **SSD1306 OLED Ekran (0.96 inch - I2C)
4.  Bağlantı Kabloları (Jumper Wires)
5.  Breadboard


## Installation

### 1. Arduino (ESP32) 
1.  `Arduino IDE` üzerinden gerekli kütüphaneleri yükleyin:
    * `SparkFun MAX3010x Pulse and Proximity Sensor Library`
    * `Adafruit SSD1306` & `Adafruit GFX`
2.  `kutuphaneli_final.ino` dosyasını açın.
3.  Wi-Fi bilgilerinizi (`ssid`, `password`) güncelleyin.
4.  Kodu **XIAO ESP32S3** kartına yükleyin.
   * *Not: PSRAM: "OPI PSRAM" seçili olmalıdır.

### 2. Python (PC) 
1.  Python 3.10 veya daha yeni bir sürüm yükleyin.
2.  Gerekli kütüphaneleri terminalden yükleyin:
    ```bash
    pip install opencv-python numpy pyserial inference roboflow
    ```
3.  `script.py` dosyasını açın.
4.  `URL` kısmına OLED ekranda yazan IP adresini girin.
5.  `ROBOFLOW_API_KEY` kısmına kendi API anahtarınızı girin.
6.  Kodu çalıştırın:
    ```bash
    python script.py
    ```
## Screenshots

<img width="962" height="753" alt="Ekran görüntüsü 2026-01-14 180242" src="https://github.com/user-attachments/assets/bb481c7c-4906-49d4-adec-4a8332ec3c8f" />

<img width="974" height="758" alt="Ekran görüntüsü 2026-01-14 180146" src="https://github.com/user-attachments/assets/965f81b9-d641-4b5c-9531-09ec938f9fd2" />

## Disclaimer

Bu proje eğitim ve hobi amaçlıdır. Tıbbi bir cihaz değildir. Gerçek tıbbi teşhis ve tedavi için kullanılmamalıdır.
This project is for educational purposes only. It is not a medical device.


## Author

**[Yasir GÜNEY / Kağan HACIOSMANOĞLU]**
