<div align="center">

# 오성식 · Game Client Programmer

### 게임 규칙을 구조화하고, 끝까지 검증하는 개발자

[![Portfolio](https://img.shields.io/badge/Portfolio-profile.blackvrice.com-0f766e?style=for-the-badge&logo=googlechrome&logoColor=white)](https://profile.blackvrice.com)
[![Blog](https://img.shields.io/badge/Blog-Tistory-e76f51?style=for-the-badge&logo=tistory&logoColor=white)](https://blackvrice.tistory.com)
[![Velog](https://img.shields.io/badge/Velog-20C997?style=for-the-badge&logo=velog&logoColor=white)](https://velog.io/@blackvrice/posts)
[![Email](https://img.shields.io/badge/Email-blackvrice@naver.com-18211f?style=for-the-badge&logo=maildotru&logoColor=white)](mailto:blackvrice@naver.com)

</div>

C# 장비 제어 실무의 **상태 · 비동기 · 복구** 경험을 C++ · Unity · Unreal 프로젝트의 게임 루프 설계로 확장했습니다.
웹 백엔드 실무에서 쌓은 데이터 처리와 성능 개선 경험도 함께 가지고 있습니다.

| | |
|---|---|
| 💼 | 소프트웨어 개발 실무 **4년** (웹 백엔드 → 장비 제어) |
| 🎮 | 플레이 가능한 상태까지 완성한 게임 프로젝트 **3개** |
| 🧪 | 자동화 테스트로 검증 — PlotterCanvas 223개 · Tycoon 78개 · RTS Smoke |
| 🔍 | 현재 **게임 클라이언트 포지션 구직 중** |

<br>

## 🎮 Game Projects

<table>
<tr>
<td width="33%" align="center">

[<img src="https://img.youtube.com/vi/g9drIxSF76o/mqdefault.jpg" width="100%">](https://youtu.be/g9drIxSF76o)

### [RTS](https://github.com/blackvrice/rts)
`C++23` `SFML3` `CMake`

자원 채집 → 건설 → 유닛 생산
고정 30Hz 틱 · A* · Replay

**A\* 점유 조회 O(n) → O(1)**

</td>
<td width="33%" align="center">

[<img src="https://img.youtube.com/vi/VSVncw0xsNU/mqdefault.jpg" width="100%">](https://youtu.be/VSVncw0xsNU)

### [Tycoon](https://github.com/blackvrice/Tycoon)
`Unity 6` `C#` `UI Toolkit`

경작 → 수확 → 판매 → 재투자
3–5분 경영 루프 완성

**테스트 78개 · 더블 미사용**

</td>
<td width="33%" align="center">

[<img src="https://img.youtube.com/vi/qMS_WJlHeEc/mqdefault.jpg" width="100%">](https://youtu.be/qMS_WJlHeEc)

### [ArenaShooter](https://github.com/blackvrice/ArenaShooter)
`Unreal Engine 5.6` `C++`

4라운드 → 5 Phase Boss
3인칭 웨이브 슈터

**Hitscan 404 hit / 0 miss**

</td>
</tr>
</table>

> 썸네일을 누르면 플레이 영상이 열립니다. 수치는 직접 실행하고 기록한 결과이며, 확인하지 않은 범위는 완성된 기능으로 표기하지 않았습니다.

<br>

## 🔍 문제 해결 기록

| 프로젝트 | 문제 | 해결 |
|---|---|---|
| **RTS** | 대형 맵에서 A* 요청이 한 틱에 몰려 시뮬레이션 정체 | 유닛 점유 조회를 O(n) 선형 탐색 → O(1) 캐시 조회로 전환, 경로 요청을 여러 틱·워커 스레드에 분산 |
| **RTS** | 안개 시야 밖 전투 연출로 적 위치 노출 | 피해·사망·폭발 피드백을 가시 지역에서만 재생 |
| **Tycoon** | 작물 추가 시마다 농장 규칙 코드 수정 필요 | GameDatabase + ScriptableObject로 데이터 분리, 규칙 수정 없이 콘텐츠만 추가 |
| **ArenaShooter** | 라운드별 탄약 충분 여부를 감으로 판단 | 명중률 70% 가정 필요 578발 vs 확보 600발로 수치 검증 |

<br>

## 🧰 Other Projects

| 프로젝트 | 스택 | 내용 |
|---|---|---|
| [**PlotterCanvas**](https://github.com/blackvrice/PlotterCanvas) | `C# 12` `.NET 8` `WPF/MVVM` `C++17` | 드로잉 → 기계 명령 변환 → 가상 플로터 실행. View→VM→Service→Device→Transport 단방향 계층, Virtual/TCP/Serial 교체 가능 구현. **xUnit 223개 통과**, 경로 포인트 92% 감소 |
| [**StarCraft Map Editor**](https://github.com/blackvrice/starcraft_map_editor) | `Flutter` `Dart` `StormLib` `euddraft` | StarCraft: Remastered용 오픈소스 UMS 맵 에디터. CHK 포맷을 원본 바이트 보존하며 파싱, MPQ·EUD 서브프로세스 어댑터. **개발 중 (M6.2)** |
| [**backjoon**](https://github.com/blackvrice/backjoon) | `Next.js` `PostgreSQL` `Prisma` `Docker` | 문제·제출·사용자·로그 관리 어드민. 샘플 배열 → Prisma API 마이그레이션 시 채점 워커 참조 필드 보존 |

<br>

## 🛠 Tech Stack

**게임 클라이언트**

![C++](https://img.shields.io/badge/C%2B%2B23-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=csharp&logoColor=white)
![Unreal](https://img.shields.io/badge/Unreal%20Engine%205-0E1128?style=flat-square&logo=unrealengine&logoColor=white)
![Unity](https://img.shields.io/badge/Unity%206-000000?style=flat-square&logo=unity&logoColor=white)
![SFML](https://img.shields.io/badge/SFML%20%2F%20OpenGL-8CC445?style=flat-square&logo=opengl&logoColor=white)
![CMake](https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white)

**실무 개발**

![WPF](https://img.shields.io/badge/WPF%20%2F%20.NET%208-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-087EA4?style=flat-square&logo=react&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle-F80000?style=flat-square&logo=oracle&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=flat-square&logo=postgresql&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)

<br>

## 💼 Career

| 기간 | 회사 | 역할 |
|---|---|---|
| 2025.01 ~ 2026.08 | **(주)앤서레이** 연구개발부 | C# / WPF 기반 형광–라만 계측 장비 제어 소프트웨어<br>Camera · Laser · Stage · Raman 통합 제어, 5계층 구조 설계 |
| 2023.04 ~ 2024.12 | **노리시스템(주)** 운영팀 | Java / Spring 웹 애플리케이션 개발·운영<br>Oracle 실행 계획 분석 기반 성능 개선, 장애 원인 추적 |
| 2022.08 ~ 2023.03 | **위시정보기술** 파견부 | Java / Spring 기업용 웹 시스템 개발<br>요구사항 분석, DB 연동, 웹 보안 처리 |

<br>

## 📐 개발 원칙

```
STATE      무엇이 바뀌는가 — 상태와 전이를 먼저 정의
BOUNDARY   책임을 어디서 끊는가 — 로직/UI, 장치/시퀀스 분리
VERIFY     어떻게 재현하는가 — 자동화 테스트, Replay, WorldHash
EVIDENCE   무엇으로 증명하는가 — Git 기록, 로그, 문서
```

<br>

<div align="center">

[![GitHub stats](https://github-readme-stats.vercel.app/api?username=blackvrice&show_icons=true&hide_border=true&title_color=0f766e&icon_color=e76f51&bg_color=00000000)](https://github.com/blackvrice)

**더 자세한 내용은 → [profile.blackvrice.com](https://profile.blackvrice.com)**

</div>
