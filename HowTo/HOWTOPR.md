## 새로운 주제와 자료를 추가하는 방법
#### 하나의 파일로 모든 파일을 관리합니다.
<img src="CONTENTSCREENSHOT.png" width="720">

## 새로운 주제와 자료를 추가하는 방법
1. fork한 레포의 `RoadmapProject/Script/Content.yml`를 엽니다.
2. 주제나 자료의 링크를 추가합니다.
3. commit한 뒤 `Content.yml`의 변경사항을 깃헙에 push합니다.
4. pull request를 보냅니다.

#### 변경사항이 적용되는 시기

1. pull request가 merge되는 것을 기다립니다.
2. Travis CI가 로드맵의 이미지와 텍스트버전을 재생성하기까지 약 5분을 기다립니다.

#### 요구사항

1. 깃
1. fork한 레포
2. [Sublime Text](https://www.sublimetext.com/)과 같은 YAML 에디터.

### 로컬에서 생성 스크립트를 실행하는 방법 (옵션)

생성 스크립트는 로드맵의 이미지와 텍스트 버전을 자동으로 생성합니다.
1. `./generateAll.sh`을 실행합니다.

**또는**

1. `RoadmapProject/Script`로 이동한 뒤
2. `./main.swift`를 실행합니다.

##### 스크립트를 로컬에서 돌리기 위한 요구사항
1. Latest Swift/Xcode
1. Prepare PlantUML:
	1. Install [JDK](http://www.oracle.com/technetwork/java/javase/downloads/jdk9-downloads-3848520.html)
	1. Install Homebrew:
		- `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
	1. Install GraphViz:
		- `brew install libtool`
		- `brew link libtool`
		- `brew install graphviz`
		- `brew link --overwrite graphviz`
	1. Go to `Roadmap Project/Script/` 
	1. Run `java -jar plantuml.jar -testdot` to check if installed correctly.
1. 최신버전의 Swift/Xcode
2. PlantUML
	1.[JDK](http://www.oracle.com/technetwork/java/javase/downloads/jdk9-downloads-3848520.html)설치
	2.  Homebrew 설치
			- `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
	1. GraphViz 설치:
		- `brew install libtool`
		- `brew link libtool`
		- `brew install graphviz`
		- `brew link --overwrite graphviz`
	1. `Roadmap Project/Script/` 으로 이동
	1. `java -jar plantuml.jar -testdot`실행해서 이상없이 설치되었는지 확인합니다.

##### 스크립트를 디버깅하는 방법 (옵션)
`Roadmap Project/Roadmap.xcodeproj`을 이용해 스크립트를 실행하고 디버깅합니다.

Xcode 는 실행가능한 바이너리파일을 실행하고 디버깅하기 때문에 결과물은 바이너리 파일 옆에 생성될 것입니다.

PR을 보내기 전에 항상 터미널로 스크립트를 실행해보세요.
