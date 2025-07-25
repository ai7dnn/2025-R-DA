# 2025-R-DA
- (2024학년도 겨율방학) [2025 학생 특강] R 활용한 데이터분석 (25.01.20월 ~ 01.24금)
- (2025학년도 여름방학) [2025 학생 특강] R 활용한 데이터분석 (25.07.16수 ~ 07.22화)

## 다운로드
- [R source code](http://www.hanbit.co.kr/src/4653)
- [R 다운로드](https://www.r-project.org/)
- [RStudio 다운로드](https://posit.co/download/rstudio-desktop)

## 특정 버전 패키지 설치
```
install.packages("https://cran.r-project.org/src/contrib/Archive/arules/arules_1.7-0.tar.gz",
                 repos = NULL, type = "source")
```

## 깃허브 데이터 내려받기
- *.zip 파일 내려받기
- $ git clone https://github.com/ai7dnn/2025-R-DA.git

## 설문 조사
- (수강전) 
- (수강후) https://forms.office.com/r/bkWk5yH54n

## 주요 단축키
# RStudio 자주 사용하는 단축키 정리

> 아래는 **Windows 기준** 단축키입니다.  
> **Mac 사용자는** `Ctrl` → `Cmd`, `Alt` → `Option`으로 치환하면 됩니다.

| 기능 범주       | 동작 설명                        | Windows/Linux 단축키      | Mac 단축키             |
|----------------|----------------------------------|----------------------------|-------------------------|
| **스크립트 실행** | 현재 줄 또는 선택 영역 실행       | `Ctrl + Enter`             | `Cmd + Enter`           |
|                | 전체 스크립트 실행                | `Ctrl + Shift + Enter`     | `Cmd + Shift + Enter`   |
| **편집 기능**   | 자동 들여쓰기                     | `Ctrl + I`                 | `Cmd + I`               |
|                | 주석 처리 / 해제                 | `Ctrl + Shift + C`         | `Cmd + Shift + C`       |
|                | 자동완성 제안                     | `Ctrl + Space`             | `Cmd + Space`           |
|                | 코드 접기 / 펼치기                | `Alt + L` / `Alt + Shift + L` | `Cmd + Alt + L` / `Cmd + Alt + Shift + L` |
| **이동/탐색**   | 함수 정의로 이동                  | `F2`                       | `F2`                    |
|                | 이전 커서 위치로 이동             | `Ctrl + .`                 | `Cmd + .`               |
|                | 다음 커서 위치로 이동             | `Ctrl + ,`                 | `Cmd + ,`               |
| **검색/바꾸기** | 찾기                              | `Ctrl + F`                 | `Cmd + F`               |
|                | 전역 검색 (파일 전체)             | `Ctrl + Shift + F`         | `Cmd + Shift + F`       |
| **콘솔 조작**   | 콘솔 지우기                       | `Ctrl + L`                 | `Cmd + L`               |
|                | 이전/다음 명령 탐색               | `↑` / `↓`                  | `↑` / `↓`               |
| **파일 탐색**   | 객체/함수/파일 탐색               | `Ctrl + .`                 | `Cmd + .`               |
|                | 환경창에서 변수 열기              | `Enter` 또는 더블클릭      | 동일                    |
| **작업 제어**   | 실행 중지 (Interrupt)             | `Esc`                      | `Esc`                   |
| **창 전환**     | 스크립트 ↔ 콘솔 전환              | `Ctrl + 1`, `Ctrl + 2`     | `Cmd + 1`, `Cmd + 2`     |

---

## 🎯 유용한 단축키 요약

- `Ctrl + Shift + M`: `%>%` 파이프 연산자 자동 삽입  
- `Tab`: 코드 자동완성 트리거  
- `Ctrl + Shift + N`: 새 스크립트 생성  
- `Ctrl + S`: 저장 (기본 중의 기본!)  
- `Ctrl + Shift + K`: R Markdown 문서 knit

---

💡 *단축키에 익숙해지면 마우스를 거의 쓰지 않아도 됩니다. 익숙해질수록 당신은 진정한 RStudio 장인…!*


## 주여 명령 문장
- 설치된 패키지 목록 확인
  - installed.packages()
- 현재 메모리에 올린 패키지 목록
  - library()
- 패키지 설치
  - install.packages("ggplot2")
- 설치된 패키지를 로드하려면:
  - library(ggplot2)
- 설치된 패키지를 메모리에서 내리려면:
  - detach("package:ggplot2")
- 설치된 패키지 삭제
  - remove.packages("ggplot2")

## 공공데이터 사이트
- 국내의 공공데이터 사이트는 다양한 분야의 데이터를 제공하여 연구, 정책 수립, 비즈니스 등 여러 용도로 활용될 수 있습니다. 아래는 주요 공공데이터 사이트 목록입니다.

1. 한국 공공데이터 포털 data.go.kr
    - 한국 정부가 제공하는 공공데이터를 통합적으로 제공하는 플랫폼으로, 다양한 분야의 데이터셋을 검색하고 다운로드할 수 있습니다.

2. 통계청 kostat.go.kr
    - 국가 통계에 대한 정보를 제공하며, 인구, 경제, 사회 등 다양한 통계 데이터를 제공합니다.

3. KOSIS (한국통계정보시스템) kosis.kr
    - 통계청에서 제공하는 통계 데이터의 통합 플랫폼으로, 다양한 통계 자료를 검색하고 활용할 수 있습니다.

4. 서울 열린 데이터 광장 data.seoul.go.kr
    - 서울시에서 제공하는 공공데이터로, 서울시의 다양한 정보와 데이터를 제공합니다.

5. AI HUB aihub.or.kr
    - 인공지능 관련 데이터셋을 제공하는 플랫폼으로, AI 연구 및 개발에 필요한 데이터를 찾을 수 있습니다.

6. 지역 데이터 포털 localdata.go.kr
    - 지역별 공공데이터를 제공하여 지역 발전 및 정책 수립에 활용할 수 있는 데이터를 제공합니다.

7. 건강보험심사평가원 opendata.hira.or.kr
    - 건강보험 관련 데이터를 제공하며, 의료 및 건강 관련 연구에 유용합니다.

8. 빅데이터 플랫폼 bigdata.seoul.go.kr
    - 서울시의 빅데이터를 활용한 다양한 서비스와 데이터를 제공합니다.
  
9. 기상자료 개방포털 data.kma.go.kr
    - 기상청 날씨데이터 서비스를 제공합니다.

10. 통합데이터지도 www.bigdata-map.kr
    - 통합 데이터지도는 공공과 민간에서 제공하는 데이터를 쉽게 검색∙활용할 수 있도록 지원합니다.

