# ldid

Mach-O는 Apple의 iOS와 macOS에서 사용되는 실행 파일 형식입니다. 

모든 iOS 앱과 라이브러리는 Mach-O 형식으로 패키징됩니다. 

Apple의 보안 정책에 따라, 
이러한 Mach-O 파일들은 Apple에서 발급한 유효한 개발자 인증서로 서명되어야 합니다.

그러나 Link Identity Editor를 사용하면 
개발자 인증서 없이도 Mach-O 파일에 서명을 추가할 수 있습니다. 
이 도구를 통해 실제 서명을 삽입할 수도 있고, 가짜 서명을 만들어 삽입할 수도 있습니다.

이는 주로 다음과 같은 상황에서 사용됩니다:

탈옥된 기기에서 서명되지 않은 앱이나 라이브러리를 실행하고자 할 때

앱 분석 또는 보안 연구 목적으로 Mach-O 파일을 수정해야 할 때

개발자 인증서 없이 iOS 앱을 배포하고자 할 때 (엔터프라이즈 배포 등)



Changes from https://git.saurik.com/ldid.git:
- Add manpages (`en`, `zh_TW` and `zh_CN`) (@CRKatri & @asdfugil)
- Support OpenSSL 3 (@sunflsks)
- Allow p12 keys to have a password (@sunflsks)
- Add a `-arch arch_type` flag so that typing the raw CPU type is not needed
- Proper error messages
  
ldid -Sentitlements.xml  file

ldid -S file

ldid -p file
