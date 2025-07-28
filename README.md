# Sistem-Monitoring-Kebocoran-Gas-Berbasis-Internet-Of-Things
project skripsi 

# Sistem Monitoring Kebocoran Gas Berbasis Internet of Things (IoT)

📡 Sistem ini dirancang untuk mendeteksi kebocoran gas secara real-time menggunakan sensor gas (MQ-135), mikrokontroler ESP8266, serta teknologi Internet of Things. Sistem ini mengirimkan data ke platform monitoring online (seperti ThingSpeak) dan memberikan notifikasi lokal (LED, buzzer) serta online jika terdeteksi kebocoran gas.

## 🛠️ Fitur Utama

* Deteksi kadar gas secara real-time menggunakan sensor MQ-135
* Notifikasi peringatan melalui buzzer dan LED saat gas melebihi ambang batas
* Monitoring data secara online melalui ThingSpeak
* Pengiriman data secara berkala via jaringan Wi-Fi (ESP8266)
* Kompatibel dengan sistem monitoring berbasis website

---

## 🔧 Teknologi & Komponen

### Perangkat Keras:

* ESP8266 NodeMCU
* Sensor Gas MQ-135 
* LED indikator (Hijau/Merah)
* Buzzer aktif 5V
* Breadboard & kabel jumper
* Power supply 5V

### Perangkat Lunak:

* Arduino IDE
* ThingSpeak (platform IoT untuk visualisasi data)
* Website Frontend (Opsional: HTML, Weebly, atau lainnya)
* Library Arduino:

  * `ESP8266WiFi.h`
  * `WiFiClient.h`
  * `ThingSpeak.h`

---

## 📡 Diagram Sistem

```
[MQ-135 Sensor] --> [ESP8266] --> [WiFi] --> [ThingSpeak Server]
                        |
                        +--> [LED & Buzzer Alert]
```

---

## 📁 Struktur Folder

```
Sistem-Monitoring-Kebocoran-Gas-Berbasis-Internet-Of-Things/
│
├── kode_arduino/
│   └── gas_monitoring.ino
│
├── dokumentasi/
│   ├── diagram_flowchart.png
│   └── laporan_skripsi.pdf
│
├── website_monitoring/
│   └── index.html
│
└── README.md
```

---

## 🚀 Cara Instalasi

1. **Siapkan Perangkat Keras**

   * Hubungkan sensor MQ-135 ke pin analog ESP8266
   * Hubungkan LED dan buzzer sesuai skema

2. **Konfigurasi Kode Arduino**

   * Ganti `ssid` dan `password` dengan Wi-Fi milik Anda
   * Masukkan API Key dari ThingSpeak

3. **Upload ke ESP8266**

   * Gunakan Arduino IDE dan pilih board “NodeMCU 1.0 (ESP8266)”
   * Upload file `gas_monitoring.ino`

4. **Monitoring Data**

   * Buka channel ThingSpeak Anda untuk melihat grafik kadar gas

---


## ⚠️ Ambang Batas Peringatan

```cpp
if (ppm >= 300) {
  // Trigger LED merah dan buzzer
}
```

---
## Skema Sistem
Pengembangan sistem monitoring kebocoran gas berbasis IoT di SPBE Wonotunggal, skema sistem dirancang menggunakan aplikasi Fritzing untuk memvisualisasikan hubungan antara komponen-komponen perangkat keras yang digunakan. Skema ini menunjukkan bagaimana sensor MQ-135 dan sensor api terhubung dengan modul ESP8266 sebagai mikrokontroler utama yang bertugas untuk mengolah data deteksi dan mengirimkannya ke website secara real-time melalui koneksi Wi-Fi. 

<div align="center">
  <img width="432" height="235" src="https://github.com/user-attachments/assets/ca4f933a-f365-4a62-8aef-af89f4c1cf63" alt="image" />
</div>

<div align="center">
 <img width="458" height="202" alt="image" src="https://github.com/user-attachments/assets/9e70ac77-5d46-4797-9951-0fb2978649e5" alt="image" />
</div>

---

## 📈 Contoh Visualisasi di ThingSpeak

* Login

<div align="center">
 <img width="458" height="216" alt="image" src="https://github.com/user-attachments/assets/8ac9d7ef-e35f-4af0-974a-fc9627621319" alt="image" />
</div>

* Dashboard

<div align="center">
 <<img width="462" height="210" alt="image" src="https://github.com/user-attachments/assets/033575a5-b0d0-4710-b0fa-215660f2d312" alt="image" />
</div>
   
*  Gauge tingkat konsentrasi gas per waktu

<div align="center">
 <img width="458" height="192" alt="image" src="https://github.com/user-attachments/assets/e9180316-7042-4cef-a3c5-1ad7d74bb9e5" alt="image" />
</div>

* Riwayat maksimum PPM dalam 24 jam terakhir

<div align="center">
  <img width="458" height="160" alt="image" src="https://github.com/user-attachments/assets/7c850b3f-8df1-4abd-afec-65388d27cdb6" alt="image" />
</div>

* Trigger alert otomatis (jika disetting)

---

## ✅ Manfaat Sistem

* Meningkatkan keamanan lingkungan dari risiko kebocoran gas
* Monitoring jarak jauh secara efisien dan cepat
* Solusi hemat biaya dan mudah diimplementasikan

---

## 🤝 Kontribusi

Kontribusi sangat diterima! Silakan fork repositori ini, buat fitur baru atau perbaikan, dan kirimkan pull request.

---

## 🙋‍♂️ Tim Pengembang

| Nama                     | Peran                | LinkedIn            |
| -------------------------| -------------------- | ------------------- |
| Tengku Ryan AB           | Programmer & IoT Dev | [LinkedIn Teuku](#) |


---

Jika kamu ingin saya bantu menambahkan diagram alur atau contoh file `.ino`, tinggal bilang saja ya!
