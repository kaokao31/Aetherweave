# AetherWeave 2.0
**Adaptive Overlay Network System**
**Version:** 2.0 | **Phase:** 1 — Core Foundation (2025)

---

## ภาพรวม / Overview

AetherWeave 2.0 คือระบบเครือข่ายแบบ **Overlay** ที่ทำงานบน Internet เดิม โดยเปลี่ยนจาก Network แบบ "Reactive" ให้กลายเป็น **"Adaptive + Predictive Network"**

ระบบสามารถ:
- 🔀 **ปรับเส้นทาง (Routing) แบบ Dynamic** — วิเคราะห์และเลือกเส้นทางที่ดีที่สุดอัตโนมัติ
- 🛡️ **Reliable Path** — หลีกเลี่ยงเส้นทางที่ไม่เสถียรโดยคำนึงถึง Reliability Score + Packet Loss
- 🔁 **Auto Reroute** — เมื่อ Node ล่ม ระบบ Reroute อัตโนมัติภายใน 5 วินาที
- 🔐 **Security by Design** — รองรับการเข้ารหัสด้วย AES-256 + RSA (Phase 3)
- 📊 **Monitoring & Telemetry** — วัด Latency, Packet Loss แบบ Real-time

---

## การใช้งาน / Quick Start

### ติดตั้ง Dependencies

```bash
pip install networkx matplotlib
```

### รัน Demo หลัก (Shortest Path + Node Failure + Auto Reroute)

```bash
python aetherweave_demo.py
```

กด **Enter** เพื่อดูแต่ละ Step:

| Step | สิ่งที่เกิดขึ้น |
|------|----------------|
| 1 | แสดง Network ทั้งหมด — ทุก Node Active |
| 2 | ส่ง Packet Alpha → Eta ผ่านเส้นทาง Optimal |
| 3 | Node Epsilon ล่ม 💀 |
| 4 | ระบบ Reroute อัตโนมัติ 🔄 |
| 5 | Node Recover → กลับมาใช้เส้นทางที่ดีที่สุด ✅ |

### รัน Simulation เปรียบเทียบ Shortest vs Reliable Path

```bash
python aetherweave_reliable.py
```

พิมพ์ Source และ Destination Node ที่ต้องการ แล้วระบบจะแสดงกราฟเปรียบเทียบ 2 เส้นทางเคียงกัน

---

## โครงสร้างโปรเจค / Project Structure

```
AetherWeave-2.0/
├── aetherweave_demo.py          # Demo หลัก — Node Simulation + Auto Reroute
├── aetherweave_reliable.py      # Simulation เปรียบเทียบ Shortest vs Reliable Path
├── README.md                    # ไฟล์นี้
│
├── docs/
│   └── AetherWeave_Slides.pptx  # Presentation Slides
│
└── tests/
    └── test_aetherweave.py       # Unit Tests (pytest)
```

---

## องค์ประกอบหลักของระบบ / System Components

| Component | หน้าที่ |
|-----------|--------|
| **Overlay Node Layer** | Node จำลองที่เชื่อมต่อกันเป็น Network Graph |
| **Adaptive Routing Engine** | วิเคราะห์ Network State + เลือกเส้นทางด้วย Dijkstra's Algorithm |
| **Reliable Path Engine** | คำนวณเส้นทางโดยคำนึงถึง Reliability Score + Packet Loss |
| **Secure Packet Layer** | เข้ารหัสด้วย AES-256 + RSA *(Phase 3)* |
| **Privacy Policy Engine** | ควบคุม Access Control + ลด Metadata Leakage *(Phase 4)* |
| **Monitoring & Telemetry** | วัด Latency, Packet Loss, Traffic Load แบบ Real-time *(Phase 5)* |

---

## Key Concepts

| Term | คำอธิบาย |
|------|----------|
| **Shortest Path** | เส้นทางที่มี Latency รวมน้อยที่สุด (Dijkstra's Algorithm) |
| **Reliable Path** | เส้นทางที่น่าเชื่อถือที่สุด คำนวณจาก Latency + Reliability Score + Packet Loss |
| **Reliability Score** | ค่าความเสถียรของแต่ละ Node (0.0 – 1.0) |
| **Auto Reroute** | การหาเส้นทางใหม่อัตโนมัติเมื่อ Node ล่ม |
| **Overlay Network** | เครือข่ายเสมือนที่ทำงานซ้อนบน Internet เดิม |
| **Adaptive** | ระบบปรับตัวตาม Network State แบบ Real-time โดยไม่ต้องมีคน Config |

---

## ผลการทดสอบ / Test Results

| KPI | เป้าหมาย | ผลจริง |
|-----|----------|--------|
| Route Efficiency | ≥ 20–25% | ✅ ระบบเลือกเส้นทาง Optimal ได้ |
| Packet Validation | ≥ 99% | ✅ ส่งสำเร็จทุก Packet |
| Recovery Time | ≤ 5 วินาที | ✅ Reroute ทันทีหลัง Node ล่ม |
| Test Coverage | ≥ 80% | ✅ ครอบคลุมทุก Component |

---

## Roadmap

| Phase | สิ่งที่ทำ | สถานะ |
|-------|----------|-------|
| **Phase 1: Core Foundation** | Node Simulation, Shortest Path, Reliable Path, Logging, Unit Tests | 🔵 NOW |
| **Phase 2: Adaptive System** | Dynamic Weight Adjustment, Self-optimization | ○ Planned |
| **Phase 3: Security Layer** | AES-256 Encryption, RSA Key Exchange, Packet Signature | ○ Planned |
| **Phase 4: Privacy Policy** | Access Control, Policy Enforcement, Metadata Leakage Reduction | ○ Planned |
| **Phase 5: Monitoring** | Dashboard, Performance Analytics, System Optimization | ○ Planned |

---

## Tech Stack

- **Python 3.x** — Core Simulation
- **NetworkX** — Graph & Routing Algorithm
- **Matplotlib** — Network Visualization
- **pytest** — Unit Testing
- **GitHub Actions** — CI/CD *(Phase 2+)*

---

## License

© AetherWeave 2.0 — Research Prototype
Built with Python + NetworkX + Matplotlib — Phase 1 Core Foundation
