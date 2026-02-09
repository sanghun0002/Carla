# CARLA Simulator 설치 가이드
Carla 시뮬레이터 설치 및 활용 정리

## 1. 사전 세팅

- **OS:**  Ubuntu 22.04
- **Python_version:** 3.10

---

## 2. 필수 소프트웨어 설치

### **Linux (Ubuntu)**

```bash
sudo apt-get update
sudo apt-get install apt-transport-https ca-certificates curl gnupg-agent software-properties-common
pip3 install --upgrade pip
```

 ---

## 3. CARLA 패키지 다운로드 및 설치

1. **GitHub 릴리즈 페이지 접속:** [CARLA GitHub Releases](https://github.com/carla-simulator/carla/releases)
2. **버전** : `0.9.15`
3. **파일 다운로드:**
    - **Linux:** `CARLA_0.9.15.tar.gz`
4. **압축 해제:** 

---

## 4. 파이썬 클라이언트 라이브러리 설정

시뮬레이터를 제어하기 위해 API 라이브러리를 설치해야 합니다.

```Bash
# 압축을 푼 폴더 내 PythonAPI/examples 폴더로 이동 후 실행
pip install carla
pip install -r requirements.txt
```

---

## 5. 시뮬레이터 실행 테스트

실행 명령어

- **Linux:**
```bash
./CarlaUE4.sh
```

> **참조:**  `W, A, S, D` 키와 마우스를 이용해 맵을 확인 가능.

---

### [📂 PythonAPI 세팅 및 활용](./docs/PythonAPI.md)

---
주의사항 및 참조사항

- **방화벽 설정:** 통신을 위해 2000번, 2001번 포트가 열려 있어야 합니다.
- **저사양 모드 실행 명령어**
```bash
./CarlaUE4.exe -quality-level=Low
```
- 화면 없이 서버만 실행하는 명령어
```bash
./CarlaUE4.sh -RenderOffScreen
```
- 프레임수 제한
```bash
./CarlaUE4.sh  -fps=15
```
