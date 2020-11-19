# Test Project

1. Test Project 생성

   ```
   react-native init testApp					#프로젝트 생성
   ```

   - index.js : 기기 or 시뮬레이터에서 1번째로 호출하는 entry point. App.js를 호출함.
   - app.json : index.js에서 호출되며 앱의 이름을 정의하는데 사용함
   - App.js : 모바일 디바이스 화면에 출력되는 1번째 파일
   - android/ : 안드로이드 앱을 위한 코드와 관련 파일들이 포함되어 있음
   - ios/ : ios 앱을 위한 코드와 관련 파일들이 포함되어 있음

2. 앱 실행

   ```
   react-native run-ios
   ```

   ** Xcode > Preference > Location > Command Line Tools : Xcode 10.2.1(10E1001)으로 설정!!

<img src="/Users/sunhapark/Library/Application Support/typora-user-images/image-20201119231543514.png" alt="image-20201119231543514" style="zoom: 25%;" />

<img src="/Users/sunhapark/Library/Application Support/typora-user-images/image-20201119231659535.png" alt="image-20201119231659535" style="zoom:25%;" />

<img src="/Users/sunhapark/Library/Application Support/typora-user-images/image-20201116225433646.png" alt="image-20201116225433646" style="zoom:25%;" />

!! ERROR

 Xcode 빌드 에러 - 'React/RCTBridgeDelegate.h' file not found

	> 프로젝트 폴더 > ios 폴더 > 
	>
	> ```
	> pod install
	> ```
	>
	> 

3. Hello World! 

   App.js 파일 수정

   ```
   import React from 'react';
   import {SafeAreaView, StyleSheet, Text} from 'react-native';
   
   const App = () => {
     return (
       <SafeAreaView style={styles.container}>
         <Text>Hello World</Text>
       </SafeAreaView>
     );
   };
   
   const styles = StyleSheet.create({
     container: {
       flex: 1,
       backgroundColor: '#fff',
       alignItems: 'center',
       justifyContent: 'center',
     },
   });
   
   export default App;
   ```

   <img src="/Users/sunhapark/Library/Application Support/typora-user-images/image-20201120000347982.png" alt="image-20201120000347982" style="zoom:25%;" />

   (참고) https://jeffgukang.github.io/react-native-tutorial/docs/basic-tutorial/basic-features(todolist)/01-getting-started/getting-started-kr.html

