## 개발환경구성 - L3 일괄 분석 프로그램

### 1. [Visual Studio 설치](https://visualstudio.microsoft.com/ko/free-developer-offers/)

### 2. vcpkg

-   C++ 프로젝트를 위한 패키지 관리 도구로, C++ 라이브러리 및 종속성을 쉽게 설치하고 관리할 수 있는 도구
-   [설치 링크](https://vcpkg.io/en/getting-started)
-   패키지 설치 방법
    -   `vcpkg install [packages to install]`
    -   예: `vcpkg install boost:x64-windows`
    -   :x64-windows를 붙여서 64bit 윈도우 환경에 맞는 패키지 설치
-   연동
    -   visual studio와 vcpkg와의 연동
    -   `vcpkg integrate install`

### 3. Visual Studio 프로젝트 설정

-   탐색기의 프로젝트 우클릭 - 속성 클릭
    1. 구성 속성 - C/C++ - 일반
        - 추가 포함 디렉터리: `include 폴더` 및 `다른 프로젝트 위치` 등 참조 위치 추가
    2. 구성 속성 - 링커 - 일반
        - 추가 라이브러리 디렉터리: `lib 폴더` 및 `include 폴더` 추가
    3. 구성 속성 - 링커 - 입력
        - 추가 종속성: `lib 파일` 명 추가
