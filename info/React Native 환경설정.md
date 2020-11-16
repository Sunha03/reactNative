# React Native 환경설정

https://firework-ham.tistory.com/104

- [x] 1. homebrew 설치

  ```
  brew --version					#homebrew 버전확인
  
  	Homebrew 2.4.11					#현재버전
  	Homebrew/homebrew-core (git revision 7db72a; last commit 2020-08-12)
  	Homebrew/homebrew-cask (git revision 5925ab0; last commit 2020-08-12)
  ```

  ```
  #homebrew 설치
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
  ```

- [x] 2. node 설치

     Node.js : React는 Javascript Runtime인 Node.js를 사용함

     npm : Node.js의 패키지를 관리하는 툴

  https://firework-ham.tistory.com/20

  1) 설치

  ```
  #node 설치
  sudo curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.1/install.sh | bash
  ```

  2) 설정

  ```
  #환경설정
  nano ~/.bashrc
  
  #아래 2줄 .bashrc 파일에 저장
  			export NVM_DIR="$HOME/.nvm"
  			[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
  ```

  ```
  #설정 로딩
  source ~/.bashrc
  ```

  3) 설치 확인

  ```
  nvm ls
  
              N/A												#설치 확인결과
  	node -> stable (-> N/A) (default)
  	iojs -> N/A (default)
  ```

  4) node 설치

  ```
  nvm install 12.14.1
  
  node -v					#node 버전확인
  	v12.14.1				#현재버전
  
  npm -v					#npm 버전확인
  	6.13.4					#현재확인
  ```

  ![image-20201116212117133](/Users/sunhapark/Library/Application Support/typora-user-images/image-20201116212117133.png)

- [x] 3. Watchman 설치

     Watchman : MacOS에서 어떤 파일의 변화를 감지하는데 사용하기 위해 Facebook에서 개발한 툴

  ```
  brew install watchman
  
  watchman --version						#watchman 버전확인
  	4.9.0												#현재버전
  ```

- [x] 4. React Native CLI 설치

     React Native CLI : React Native 앱을 빌드하고 실행하는데 필요한 툴

  ```
  npm install -g react-native-cli
  
  react-native --version				#react-native 버전확인
  	react-native-cli: 2.0.1			#현재버전
  	react-native: n/a - not inside a React Native project directory
  ```

  * react-native cli vs expo cli

    -> expo cli는 불필요한 라이브러리를 설치해야 함

- [x] 5. Xcode 설치

     Xcode : 네이티브 앱 빌드를 위해 필요한 툴

     -> App Store에서 설치

- [x] 6. Cocoapods 설치

     Cocoapods : Swift 및 Objective-C 코코아 프로젝트의 종속성 관리자. RN으로 프로젝트를 initialize할 때 Cocoapods가 설치되어 있으면 Android와 iOS빌드에 필요한 종속된 라이브러리들을 초기화해주며, 추후에도 필요한 라이브러리들을 관리할 때 지속적으로 사용됨

  ```
  brew install cocoapods
  
  pod --version									#cocoapods 버전확인
  1.10.0												#현재버전
  ```

- [x] Java 설치

  ```
  brew tap AdoptOpenJDK/openjdk
  brew cask install adoptopenjdk8
  
  java -version											#java 버전확인
  	openjdk version "1.8.0_265"			#현재버전
  	OpenJDK Runtime Environment (AdoptOpenJDK)(build 1.8.0_265-b01)
  	OpenJDK 64-Bit Server VM (AdoptOpenJDK)(build 25.265-b01, mixed mode)
  ```

  