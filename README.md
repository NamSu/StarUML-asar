## StarUML asar

StarUML Hacked for JS

### How-To-Do?

#### Windows 기준

1. StarUML 최신버전 설치
2. Node.JS 설치 [NODEJS 설치](https://nodejs.org/dist/v10.15.3/node-v10.15.3-x64.msi)
3. Powershell 관리자 권한으로 열기 (Win + X) -> powershell 관리자 권한으로 열기 클릭
4. **cd "C:\Program Files\StarUML\resources"**
5. **npm install -g asar**
6. **asar extract app.asar apps**
7. C:\Program Files\StarUML\resources\apps\src\engine\으로 이동
8. 관리자 권한으로 열린 아무 텍스트 에디터로 ~~그렇다고 메모장 말고~~ license-manager.js 수정.
9. 다음과 같이 수정
```javascript
  checkLicenseValidity () {
    this.validate().then(() => {
      setStatus(this, true)
    }, () => {
      setStatus(this, true) // 이 구문 과 똑같이 수정
    })
  }
```
10. powershell 창에서 **asar pack apps apps.asar** 입력
11. app.asar 삭제후 apps.asar 이름 app.asar로 변경
12. GG