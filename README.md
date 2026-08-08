# OrbitBike Mobile Wrapper

웹사이트 `https://orbitbike.com`을 Android와 iOS 앱 내부에서 여는 WebView 래퍼입니다.

## 포함 기능
- Android / iOS WebView
- JavaScript + Local Storage
- GPS 위치 권한
- 웹 `navigator.geolocation` 사용 지원
- 외부 `tel:`, `mailto:`, 지도 앱 링크 처리
- Android 뒤로가기 = 웹 뒤로가기

## Android APK 만들기
1. Android Studio에서 `android` 폴더를 엽니다.
2. Gradle Sync가 끝날 때까지 기다립니다.
3. `Build > Build Bundle(s) / APK(s) > Build APK(s)`를 누릅니다.
4. 생성된 APK는 보통 `android/app/build/outputs/apk/debug/app-debug.apk`에 있습니다.

앱 ID: `com.orbitbike.app`
앱 이름: `OrbitBike`


## Android Studio 없이 APK 받기
1. 이 ZIP을 풀어 내용 전체를 GitHub 저장소에 올립니다.
2. GitHub의 `Actions` 탭에서 `Build OrbitBike APK`를 엽니다.
3. `Run workflow`를 누릅니다.
4. 완료되면 `Artifacts`의 `OrbitBike-APK`를 내려받습니다.

GitHub에 push할 때도 자동으로 APK 빌드가 실행됩니다.

## iPhone 앱 만들기
1. Mac에서 `ios/OrbitBikeIOS/OrbitBikeIOS.xcodeproj`를 Xcode로 엽니다.
2. Target `OrbitBikeIOS` > `Signing & Capabilities`에서 본인의 Apple Team을 선택합니다.
3. iPhone을 연결하거나 Simulator를 선택한 뒤 Run 합니다.

앱의 실제 `.ipa` 설치 파일은 Apple 서명이 필요해 Mac/Xcode에서 빌드해야 합니다.

## 사이트 주소를 바꾸려면
현재 두 프로젝트 모두 `https://orbitbike.com`으로 고정해 두었습니다.
- Android: `MainActivity.java`의 `HOME_URL`
- iOS: `ViewController.swift`의 `homeURL`
