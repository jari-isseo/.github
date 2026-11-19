<div align="center">

<img src="https://github.com/jari-isseo.png" width="120" alt="자리있어?! 로고" />

# 자리있어?!

**매장을 한 번 스캔하면, 손님에게 실시간 빈자리가 보인다.**

🏆 신한대학교 소프트웨어중심대학 2026 앱개발 경진대회

 [사장님 앱](https://github.com/jari-isseo/jari-isseo-android) · [서버 · 손님 웹](https://github.com/jari-isseo/jari-isseo-server)

</div>

---

##  어떤 서비스인가요?

손님과 가게가 **같은 매장 지도**를 보는 서비스입니다.

- **손님**: 가보기 전에는 자리가 있는지 알 수 없고, 바쁜 시간에는 전화로 묻기도 어렵습니다.
- **가게**: 빈자리를 알리려면 전화를 받아야 하고, 처음 온 직원은 테이블 번호가 어디인지 모릅니다.

→ **스캔으로 매장 지도를 만들고, 사장님이 한 번 터치하면 손님 화면에 빈자리가 보입니다.**
손님은 앱을 설치하지 않고 링크나 QR로 바로 확인합니다.

## 사용 흐름

| 단계 | 내용 |
| --- | --- |
| 1. 매장 스캔 | ARCore로 바닥과 벽을 잡고, YOLOv8로 테이블 탐지 |
| 2. 탑뷰 보정 | 바닥 모양, 테이블, 의자 배치 다듬기 |
| 3. 배치 업로드 | 보정한 매장 지도를 서버에 저장 |
| 4. 상태 전환 | 테이블을 탭하면 손님 웹에 실시간(SSE) 반영 |

##  Repositories

| 레포 | 설명 |
| --- | --- |
| [jari-isseo-android](https://github.com/jari-isseo/jari-isseo-android) | 사장님용 Android 앱: 매장 스캔, 탑뷰 보정, 테이블 상태 전환 |
| [jari-isseo-server](https://github.com/jari-isseo/jari-isseo-server) | API 서버와 손님 웹: 배치 저장, 실시간 상태 전달, 아이소메트릭 지도 |

## 🛠 Tech Stack

**Android**  
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white)
![ARCore](https://img.shields.io/badge/ARCore-4285F4?style=flat-square&logo=google&logoColor=white)
![YOLOv8](https://img.shields.io/badge/YOLOv8-111F68?style=flat-square)

**Server**  
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![AWS Lightsail](https://img.shields.io/badge/AWS%20Lightsail-FF9900?style=flat-square&logo=amazonwebservices&logoColor=white)

**Customer Web**  
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![SVG](https://img.shields.io/badge/SVG-FFB13B?style=flat-square&logo=svg&logoColor=black)

## 👥 Team

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/LEEMINGU03">
        <img src="https://github.com/LEEMINGU03.png" width="100" alt="LEEMINGU03" /><br />
        <b>이민구</b>
      </a><br />
      Android
    </td>
    <td align="center">
      <a href="https://github.com/sayhoney1023">
        <img src="https://github.com/sayhoney1023.png" width="100" alt="sayhoney1023" /><br />
        <b>sayhoney1023</b>
      </a><br />
      Server · Web
    </td>
  </tr>
</table>
