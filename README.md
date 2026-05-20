# Klarheit (光澄) — Enterprise-Grade D2C Optical E-Commerce Solution

[![Tech Stack](https://img.shields.io/badge/Stack-React_19_%7C_Spring_Boot_3.4-blue?style=for-the-badge)](https://github.com/your-username/Klarheit)
[![Architecture](https://img.shields.io/badge/Architecture-Fullstack_Decoupled-orange?style=for-the-badge)](#system-architecture)
[![Java](https://img.shields.io/badge/Java-21-red?style=for-the-badge&logo=openjdk)](https://openjdk.org/)
[![React](https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react)](https://react.dev/)

**Klarheit** (German for "Clarity") is a high-performance, full-stack D2C (Direct-to-Consumer) eyewear platform. It bridges the gap between luxury retail and digital convenience by integrating state-of-the-art **AR Virtual Try-On**, **Digital Prescription Management**, and a robust **Enterprise Backend Pipeline**.

---

## 💎 Product Philosophy & Business Value

In the evolving eyewear industry, digital transformation is no longer optional. Klarheit is engineered to solve the core conversion barriers:
- **Trust Engineering**: Real-time 3D AR visualization reduces product uncertainty.
- **Precision Commerce**: Specialized workflows for complex optical prescriptions ensure medical-grade accuracy.
- **Scalable Architecture**: Built on a decoupled foundation, ready for global deployment and high-concurrency traffic.

---

## ✨ Core Feature Set

### 🕶️ AR Virtual Studio
*   **Neural Face Tracking**: Powered by Google MediaPipe Face Landmarker for 468-point sub-millimeter tracking.
*   **PBR Rendering**: Three.js integration for Physically Based Rendering (PBR) of frames, capturing realistic light reflections and material textures.
*   **Biometric Calibration**: Real-time interpupillary distance (PD) estimation to ensure perfect frame scaling.

### 🔬 Optical Config Lab
*   **Dynamic Lens Engine**: Real-time pricing and compatibility logic for lens types, indices, and coatings.
*   **Prescription Vault**: Secure, structured storage for complex ophthalmic data (SPH, CYL, AXIS, ADD).
*   **Seamless Checkout**: A multi-step, conversion-optimized checkout flow with integrated order summary.

### 📧 Enterprise Communication (New)
*   **Asynchronous Notification**: Integrated **Resend API** with Spring Boot `@Async` for transactional emails.
*   **Branded Experience**: Responsive HTML email templates for order confirmations and status updates.

### 👤 Customer Experience (CX) Hub
*   **Verified Accounts**: Secure JWT-based authentication with profile persistence.
*   **Order Intelligence**: Comprehensive order history tracking and status management.

---

## 🏗️ Technical Architecture

### Front-end: Modern UX Stack
- **Framework**: React 19 (Concurrent Mode) & TypeScript.
- **Build Tool**: Vite 6 (Lightning-fast HMR).
- **Styling**: Tailwind CSS 4 (Zero-runtime CSS-in-JS alternative).
- **Motion**: Framer Motion 12 for high-fidelity UI transitions.
- **i18n**: Full internationalization support (English/Chinese) via i18next.

### Back-end: Robust Service Layer
- **Engine**: Java 21 & Spring Boot 3.4.
- **Security**: Spring Security 6 with stateless JWT authentication & CORS hardening.
- **Data**: Spring Data JPA + MySQL 8.0.
- **Migration**: Flyway for version-controlled schema evolution.
- **Resilience**: Bucket4j Token Bucket algorithm for distributed rate limiting.
- **Testing**: Comprehensive JUnit 5 & MockMvc integration test suite.

---

## 📂 Project Structure

```text
Klarheit/
├── backend/                # Spring Boot Micro-monolith
│   ├── src/main/java/      # Domain-driven packages (auth, order, product, etc.)
│   ├── src/main/resources/ # Flyway migrations & config
│   └── src/test/           # Integration & Unit tests
├── front_end/              # React Single Page Application (SPA)
│   ├── src/ar/             # AR & 3D Logic (MediaPipe/Three.js)
│   ├── src/components/     # Atomic UI components
│   └── src/i18n/           # Localization assets
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites
- JDK 21+
- Node.js 20+
- MySQL 8.0+

### Backend Setup
1. Create `backend/.env` from `.env.example`:
   ```env
   SPRING_PROFILES_ACTIVE=local
   DB_URL=jdbc:mysql://localhost:3306/klarheit_db
   DB_USERNAME=root
   DB_PASSWORD=your_password
   APP_JWT_SECRET=your_high_entropy_secret
   APP_RESEND_API_KEY=re_xxx...
   ```
2. Run: `mvn spring-boot:run`

### Frontend Setup
1. `cd front_end`
2. `npm install`
3. `npm run dev` (Access at `http://localhost:3000`)

---

## 🗺️ Strategic Roadmap
- [ ] **Fintech Integration**: Native Stripe/PayPal Checkout API.
- [ ] **AI Recommendation**: Deep learning face-shape analysis for personalized frame suggestions.
- [ ] **Admin Dashboard**: Real-time analytics and CMS for inventory management.
- [ ] **Performance Tuning**: WebWorker-based offscreen rendering for AR tracking.

---

## 📄 License
This project is licensed under the MIT License.

---
**Klarheit — Engineering the Future of Optical Retail.**
*Crafted with precision. Starring is caring!* ⭐️
