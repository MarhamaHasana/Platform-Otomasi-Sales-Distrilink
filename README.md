# System Analyst Case Study — Sales Automation Platform

A system analysis case study focused on improving the reliability and traceability of sales visit and order data within a Sales Automation Platform (SAP).

## Candidate

**Nama:** Marhama Hasana  
**Role:** System Analyst  

## Project Overview

Case study ini membahas analisis proses bisnis dan kebutuhan sistem pada **Distrilink Sales Automation Platform (SAP)**, dengan fokus pada validasi kunjungan outlet dan keterlacakan pesanan.

Analisis mencakup proses **New Outlet Onboarding (NOO)** serta **Order Management**, termasuk pesanan yang dibuat saat kunjungan dan **Order Without Visit (OOS)**.

Fokus utama case study adalah menghubungkan data lokasi, aktivitas kunjungan, sumber pesanan, serta kondisi pengecualian agar dapat mendukung monitoring dan proses review oleh Supervisor.

## Analysis Scope

- Business Process Analysis
- Requirements Analysis
- Business Rules
- User Story & Acceptance Criteria
- Use Case Analysis
- Data Requirements & ERD
- Edge Case Analysis
- Offline & Synchronization Flow
- Requirement Traceability

## Key Analysis

### 1. Visit & Location Validation

Proses To-Be mengusulkan pengambilan koordinat GPS saat check-in dan perhitungan jarak antara posisi Sales dengan lokasi outlet.

Aktivitas dalam radius yang dikonfigurasi dapat diproses secara normal, sedangkan aktivitas di luar radius tetap dicatat dan diberikan indikator untuk proses review.

### 2. Visit Duration

Waktu check-in dan check-out digunakan untuk menghitung durasi kunjungan.

Informasi durasi kemudian dapat digunakan sebagai salah satu indikator dalam monitoring aktivitas kunjungan.

### 3. Order Traceability

Pesanan dibedakan berdasarkan sumbernya:

- **Visit** — pesanan yang dibuat sebagai bagian dari kunjungan dan terhubung dengan data visit.
- **OOS (Order Without Visit)** — pesanan yang dibuat tanpa kunjungan aktif dan memerlukan alasan serta metadata pendukung.

Pemisahan ini membantu memberikan konteks yang lebih jelas terhadap setiap transaksi.

### 4. Offline Operation

Case study juga mempertimbangkan kondisi ketika Sales bekerja tanpa koneksi jaringan.

Data dapat disimpan secara lokal dengan status **Pending Sync** dan disinkronkan kembali ketika koneksi tersedia. Status sinkronisasi dipisahkan dari status bisnis aktivitas.

## Edge Case Analysis

Beberapa kondisi khusus yang dianalisis meliputi:

- Aktivitas di luar radius outlet
- GPS tidak tersedia
- Aktivitas dalam kondisi offline
- Checkout tidak dilakukan
- Concurrent check-in
- Duplicate New Outlet Onboarding
- GPS spoofing / mock location
- Unusual OOS pattern

Pendekatan yang digunakan adalah mempertahankan data aktivitas dan memberikan informasi yang cukup untuk monitoring atau review, daripada langsung menolak aktivitas yang dianggap tidak normal.

## Analyst's Note

### Is the 100-meter radius a final requirement?

Tidak. Radius **100 meter digunakan sebagai asumsi awal**, karena belum terdapat ketentuan bisnis yang mengonfirmasi angka tersebut sebagai threshold final.

Sebelum implementasi, parameter tersebut perlu divalidasi bersama **Product Owner atau stakeholder terkait**, dengan mempertimbangkan kondisi operasional di lapangan.

Hal ini membedakan antara **analyst assumption** dan **confirmed business requirement**.

## Deliverables

- As-Is & To-Be Business Process
- Business Rules
- User Stories & Acceptance Criteria
- Use Case Diagram & Specification
- Data Requirements
- Entity Relationship Diagram (ERD)
- Process Flow
- Edge Case Analysis
- Status Definitions
- Requirement Traceability
- Assumptions & Validation Notes

## Documentation

Dokumen lengkap case study tersedia pada file:

`MarhamaHasana_SystemAnalyst_CaseStudy.pdf`

[View Full Case Study](./MarhamaHasana_SystemAnalyst_Portofolio.pdf)

## Project Information

| Category | Details |
|---|---|
| **Project Type** | System Analyst Case Study |
| **Role** | System Analyst |
| **Domain** | Sales Automation Platform |
| **Focus** | Business Process & Requirements Analysis |
| **Key Areas** | Geotagging, Outlet Visit, NOO, Order Management, OOS |

## Contact

**Marhama Hasana**

System Analyst | Business Process | Requirements Analysis

[LinkedIn](YOUR_LINKEDIN_URL)  
[GitHub](YOUR_GITHUB_URL)
