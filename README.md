# 🚨 재난 대응 통합 관리 시스템

## 📌 프로젝트 개요

소방 차량 및 출동 자원을 중앙에서 관리하기 위한 시스템이다.  
차량 등록, 출동 관리, 활동 추적, 통계 및 보고서 기능을 제공한다.

🔗 **배포 주소**  
https://fire.rjsgud.com/

---

## 🧩 주요 기능

### 🏠 메인
- 실시간 현황 정보 표시
  - 소방관 수
  - 운영 중 소방서 수
  - 가용 소방차 수
- 기상 정보 제공
  - 지역별 현재 날씨 (기온, 강수확률, 풍속 등)
<img width="1897" height="906" alt="image" src="https://github.com/user-attachments/assets/3e6e4ed3-9718-40db-a27e-5cd572fa7783" />

---

### 📥 자원등록
- 차량 신규 등록
  - 시도, 소방서, 차종, 호출명, 용량, 인원
  - AVL 단말기, PS-LTE 번호 입력
  - 자원집결지 주소 입력
- 엑셀 업로드를 통한 일괄 등록
- 등록 차량 목록 관리
<img width="1917" height="908" alt="image" src="https://github.com/user-attachments/assets/0ea233bb-188c-47b7-8e83-a46f2d59354d" />

---

### 🚒 자원배분
- 대기 차량 기반 출동 편성
- 차량 / 인원 / 차종별 집계 자동 표시
- 출동 정보 입력
  - 제목, 내용, 출동 주소
- 선택 차량 기반 출동 명령 생성
<img width="1899" height="904" alt="image" src="https://github.com/user-attachments/assets/36b35a13-0199-406a-8aff-1d9b50af4b20" />

---

### 📊 자원관리
- 전체 차량 조회 및 검색
- 차량 정보 확인
  - 위치, 출동 내용, 상태 등
- 상태 기반 관리 및 조치
<img width="1919" height="408" alt="image" src="https://github.com/user-attachments/assets/18fe07bf-eb1d-46ea-a3e4-e1e0c5ba1c5f" />

---

### 🗺 지도
- 차량 위치 기반 지도 표시
- 위치 및 분포 확인
<img width="1919" height="910" alt="image" src="https://github.com/user-attachments/assets/84997ab4-0afd-4bcb-b996-deb92e5b565e" />

---

### 📈 통계
- 차량 / 인원 / 차종별 집계 데이터 제공
<img width="1919" height="906" alt="image" src="https://github.com/user-attachments/assets/4d90df61-edd5-49da-87bd-6d5d81b8f44e" />

---

### 📄 보고서
- 출동 및 자원 데이터 기반 보고서 생성
<img width="1917" height="907" alt="image" src="https://github.com/user-attachments/assets/d7459e64-4901-4c64-8086-00edc160f8fe" />

---

## ⚙️ 특징

- 자원등록 / 자원배분 / 자원관리 메뉴에서 재난모드 전환 지원
- 차량 정보, 출동 정보, 위치 데이터를 통합 관리
- 실시간 데이터 기반 현황 확인 가능

---

## 🧠 핵심 설계

### 상태 관리
- 차량 상태: `대기 / 활동 / 철수`
- 출동 상태: `DRAFT → SENT → ENDED`
- 상태 전이 검증 로직 적용

### GPS 처리
- AVL 단말기 → 서버 → DB 저장
- 현재 위치 / 이력 분리 관리

---

## 🗂️ 주요 테이블

- `vehicles`
- `dispatch_orders`
- `dispatch_vehicle_map`
- `vehicle_current_location`
- `vehicle_gps_log`

---

## ⚙️ 기술 스택

- Backend: Spring Boot, JPA
- Database: MySQL
- Frontend: React
- External: 카카오맵 API, GPS(AVL)

---
