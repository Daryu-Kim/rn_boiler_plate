본 템플릿은 React Native CLI 0.72에 Yarn, TypeScript, Redux, DotEnv, TSLint, AsyncStorage, Navigation, ImagePicker, ReAnimated, SafeAreaContext, SVG, StyledComponents가 적용되어 있는 템플릿입니다.

# Getting Started

>**Note**: Intellij IDEA Ultimate 프로그램을 기준으로 작성되었으며, Package명 변경을 위해 부가적으로 Android Studio와 Xcode가 필요합니다.

## Step 1: App 이름 변경하기

<h3>Android App Name 변경하기</h3>
<ol>
   <li>Intellij IDEA Ultimate를 사용하여 받아온 템플릿을 열어주세요.</li>
   <li><code>android/app/src/res/values/strings.xml</code>에 들어가서 <code>app_name</code>에 원하는 App Name을 입력해주세요.</li>
</ol>

<h3>iOS App Name 변경하기</h3>
<ol>
   <li>Intellij IDEA Ultimate를 사용하여 받아온 템플릿을 열어주세요.</li>
   <li><code>ios/rn_boiler_plate/Info.plist</code>에 들어가서 <code>CFBundleDisplayName</code>에 원하는 App Name을 입력해주세요.</li>
</ol>

## Step 2: Package Name 변경하기

<h3>Android Package Name 변경하기</h3>
<ol>
   <li>Android Studio로 <code>rn_boiler_plate/android</code> 폴더를 열어주세요.</li>
   <li><code>rn_boiler_plate/app/java/com.rn_boiler_plate</code> 폴더를 개발자명 또는 조직명으로 Rename 해주시고 Do Refactor를 눌러주세요.</li>
   <li><code>rn_boiler_plate/app/java/com.[개발자명 또는 조직명]</code> 폴더를 우클릭하고 <code>New > Package</code>를 누르셔서 App Name을 입력해서 생성해주세요.</li>
   <li><code>rn_boiler_plate/app/java/com.[개발자명 또는 조직명]</code> 폴더 안에 있는 <code>Java</code> 파일을 모두 <code>rn_boiler_plate/app/java/com.[개발자명 또는 조직명].[App Name]</code> 폴더로 옮겨주세요. 만약, Do Refactor 창이 뜬다면 Do Refactor 버튼을 눌러주세요.</li>
   <li><code>rn_boiler_plate/app/java/com.[개발자명 또는 조직명].[App Name]/MainApplication.java</code> 파일을 열어서 <code>import com.[개발자명 또는 조직명]</code> 코드를 <code>import com.[개발자명 또는 조직명].[App Name]</code>으로 변경해주세요.</li>
   <li><code>rn_boiler_plate/app/manifests</code>에 들어가서 <code>manifest</code> 안에 있는 <code>xmlns:android="http://schemas.android.com/apk/res/android"</code> 코드를 <code>xmlns:android="http://schemas.android.com/apk/res/android" package="com.[개발자명 또는 조직명].[App Name]"</code>으로 변경해주세요.</li>
      <li><code>Gradle Scripts/build.gradle (Module :app)</code>에 들어가셔서 <code>android</code> 안에 있는 <code>namespace</code>와 <code>applicationId</code>의 내용을 <code>com.[개발자명 또는 조직명].[App Name]</code>으로 변경해주세요.</li>
</ol>

<h3>iOS Package Name 변경하기</h3>

## Step 3: Package 가져오고 설정하기
<ol>
   <li>Xcode로 <code>rn_boiler_plate/ios</code> 폴더를 열어주세요.</li>
   <li>좌측 상단 디렉토리 부분에 <code>rn_boiler_plate</code> 폴더를 클릭해주세요.</li>
   <li>TARGETS에 있는 rn_boiler_plate를 클릭 후 Bundle Identifier에 있는 내용을 <code>com.[개발자명 또는 조직명].[App Name]</code>으로 변경해주세요.</li>
   <li>TARGETS에 있는 rn_boiler_plateTests를 클릭 후 Bundle Identifier에 있는 내용을 <code>com.[개발자명 또는 조직명].[App Name]Tests</code>으로 변경해주세요.</li>
</ol>

```bash
cd android && ./gradlew clean && cd ..
cd ios && pod install && cd ..
yarn install
```

## 모든 설정이 끝났습니다! :tada:

이제 즐겁게 개발하시면 됩니다! :partying_face:
