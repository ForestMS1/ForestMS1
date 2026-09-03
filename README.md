<div align="center">

# 김대성 | Game Programmer

### 문제를 측정하고, 구조로 해결합니다.

상용 엔진의 기능을 **C++ · DirectX**로 직접 구현하며  
렌더링, 애니메이션, 에디터, 게임 플레이 시스템의 내부 원리를 공부하고 있습니다.

</div>

---

## 👋 About Me

- 게임 기능 구현을 넘어 **데이터 수명주기, 성능, 팀의 작업 흐름**까지 고민합니다.
- 개인 프로젝트에서는 렌더링·애니메이션·에디터를, 팀 프로젝트에서는 맵 시스템과 렌더링 최적화를 경험했습니다.
- 다른 작업자가 실제로 사용할 수 있는 API와 제작 도구를 설계하는 데 관심이 있습니다.

```text
C++ · DirectX 11 · HLSL · Rendering · Optimization · Tools
```

## 🧰 Tech Stack

<p>
  <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=c%2B%2B&logoColor=white" alt="C++" />
  <img src="https://img.shields.io/badge/DirectX_11-107C10?style=flat-square&logo=windows&logoColor=white" alt="DirectX 11" />
  <img src="https://img.shields.io/badge/HLSL-222222?style=flat-square" alt="HLSL" />
  <img src="https://img.shields.io/badge/ImGui-1F6FEB?style=flat-square" alt="ImGui" />
  <img src="https://img.shields.io/badge/Tracy-8A2BE2?style=flat-square" alt="Tracy" />
  <img src="https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=csharp&logoColor=white" alt="C#" />
  <img src="https://img.shields.io/badge/Unity-000000?style=flat-square&logo=unity&logoColor=white" alt="Unity" />
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git" />
</p>

## 🎮 Projects

### 🏰 [호그와트 레거시 모작](https://app.notion.com/p/3cbeeaf2f36e81ea96aae565645d0b6a) `Team · DirectX 11`

> 넓은 오픈월드를 구현한 C++·DirectX 11 자체 프레임워크 팀 프로젝트

**담당:** 맵 시스템 · 렌더링 최적화 · 컷신 에디터 · 스크린 스페이스 데칼

- 플레이어 주변 청크만 비동기로 유지하는 **월드 청크 스트리밍** 구현
- GPU 상주 인스턴스 데이터와 **Frustum · Hi-Z 오클루전 컬링** 구축
- GPU 컬링 작업을 단일 배치로 통합하고 CPU Readback 없이 Indirect Draw 수행
- Deferred Context 병렬 기록과 **Command List 캐시**로 반복 CPU 작업 제거
- 팀원이 코드 수정 없이 사용할 수 있는 카메라 컷신 에디터 제작

| 측정 항목 | Before | After |
|:---|---:|---:|
| GPU 컬링 배치 · Debug | 13.11 ms | **4.78 ms** |
| GPU 컬링 배치 · Release | 5.15 ms | **0.48 ms** |
| Deferred Context 기록 | 13–14 ms | **약 5.5 ms** |

[▶ 플레이 영상](https://youtu.be/2ldoq8TVPvw) · [📂 GitHub](https://github.com/limits1214/JUSIN_160_FINAL_TEAM_PROJECT) · [📘 상세 기술 문서](https://app.notion.com/p/3afeeaf2f36e818ead66d5669b163338)

---

### ⚡ [젠레스 존 제로 모작](https://app.notion.com/p/367eeaf2f36e80ac9628c22a42ef688b) `Personal · DirectX 11`

> 자체 프레임워크 위에 3D 액션 RPG와 콘텐츠 제작 도구를 구현한 개인 프로젝트

`C++` `DirectX 11` `HLSL` `ImGui` `ImNodes` `Assimp` `Boost.Asio`

- G-Buffer 기반 **Deferred Rendering** 및 Shadow Mapping
- ImGui·ImNodes 기반 노드형 **Animation FSM Editor**와 XML 직렬화
- Catmull-Rom 보간을 활용한 카메라 키프레임 에디터
- Root Motion, GameObject–Component 생명주기 및 레벨 직렬화
- Boost.Asio 기반 UDP 객체·애니메이션·전투 상태 동기화 프로토타입

[▶ 플레이 영상](https://www.youtube.com/watch?v=vQrka05_PnI) · [📂 GitHub](https://github.com/ForestMS1/ZZZ_DX11)

---

### 🌊 [데이브 더 다이버 모작](https://app.notion.com/p/364eeaf2f36e80f18935c896bb100c3c) `Team · DirectX 9`

> DirectX 9 기반 2D 액션 어드벤처 팀 프로젝트

**담당:** 플레이어 · UI · 보스 · 아이템

- 이동·낚시·공격·피격·사망을 독립된 클래스로 분리한 **State Pattern**
- 플레이어와 UI의 결합도를 낮춘 **Observer Pattern**
- 조준, 충돌, 당기기 입력으로 구성된 낚시 시스템
- 상태 패턴으로 관리되는 2페이즈 보스 AI

[▶ 플레이 영상](https://youtu.be/y0byNYJvyqE)

---

### 🧸 [Toyland Trials](https://app.notion.com/p/cc0eeaf2f36e82619f41016fe5d37e88) `Team · Unity`

> 실시간 동기화와 탈출 미션을 지원하는 4인 협동 멀티플레이 게임

**담당:** 게임 상태 관리 · 플레이어 동기화 · 미션 시스템 · 미니맵

- PhotonView 소유권을 기반으로 로컬·원격 플레이어 분리
- 방 상태, 플레이어 상태, 미션 및 기믹의 클라이언트 간 동기화
- 원격 캐릭터 생성 시 발생한 카메라 간섭 문제를 단일 씬 카메라 구조로 해결

[▶ 플레이 영상](https://www.youtube.com/watch?v=IZmefdNwFZw) · [📂 GitHub](https://github.com/kookmin-sw/capstone-2025-17)

---

<details>
<summary><b>🕹️ Early & Short Projects</b></summary>
<br />

### [던그리드 모작](https://app.notion.com/p/364eeaf2f36e80a2bb1efbfc2f944f46) `Personal · WinAPI`

- 상용 엔진 없이 렌더링, 충돌, 전투, UI를 구현한 2D 로그라이크 액션 게임
- 타일 옵션, 파일 저장·불러오기를 지원하는 맵 에디터
- 확장 가능한 무기 구조와 드래그 앤 드롭 인벤토리·상점 시스템

[▶ 플레이 영상](https://www.youtube.com/watch?v=E3azsZResLk)

### [LinkControl](https://app.notion.com/p/c45eeaf2f36e82f6aced01e35d295145) `Game Jam · Unity`

- 2박 3일 동안 완성한 2D 탑뷰 디펜스 게임
- 플레이어 이동·애니메이션, Zone 기반 무기 강화, 몬스터 상태 관리 구현
- 레드브릭 게임잼 완성작 코엑스 전시

[🎮 플레이](https://redbrick.land/detail-play?pid=f869453f-5a61-4e49-a3e9-73f025da6565) · [📂 GitHub](https://github.com/mingyu243/RedbrickGamejam_2024_11)

</details>

## 📊 GitHub

<div align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=ForestMS1&show_icons=true&theme=tokyonight&hide_border=true&bg_color=00000000&rank_icon=github" alt="ForestMS1's GitHub stats" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=ForestMS1&layout=compact&theme=tokyonight&hide_border=true&bg_color=00000000" alt="ForestMS1's most used languages" />
</div>

---

<div align="center">

기능을 구현하는 데서 멈추지 않고, 원인을 측정하고 구조를 개선하는 개발자가 되겠습니다.

</div>
