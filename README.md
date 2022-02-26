<h1 align="center"><img src="https://user-images.githubusercontent.com/42619122/155006230-75e7e844-97f6-4cfa-93c1-f0aa20eeaf7f.png" height="30" weight="30" alt="GitHub forks"> <b>updaate</b></h1>
<p align="center"><b>A Minimalist App Update Checker for Android</b></p>

<br/>

<p align="center">
<a href="https://www.android.com"><img src="https://img.shields.io/badge/platform-Android-yellow.svg" alt="platform"></a>
 <a href="https://android-arsenal.com/api?level=21"><img src="https://img.shields.io/badge/API-21%2B-brightgreen.svg?style=flat" alt="API"></a> <a href="https://jitpack.io/#instaal-io/updaate"><img src="https://jitpack.io/v/instaal-io/updaate.svg" alt="JitPack"></a> <a href="https://github.com/instaal-io/updaate/blob/master/LICENSE"><img src="https://img.shields.io/github/license/instaal-io/updaate" alt="GitHub license"></a>
 </p>
 <p align="center">
 <a href="https://github.com/instaal-io/updaate/issues"><img src="https://img.shields.io/github/issues/instaal-io/updaate" alt="GitHub issues"></a> <a href="https://github.com/instaal-io/updaate/network"><img src="https://img.shields.io/github/forks/instaal-io/updaate" alt="GitHub forks"></a> <a href="https://github.com/instaal-io/updaate/stargazers"><img src="https://img.shields.io/github/stars/instaal-io/updaate" alt="GitHub stars"></a> <a href="https://github.com/instaal-io/updaate/graphs/contributors"> <img src="https://img.shields.io/github/contributors/instaal-io/updaate" alt="GitHub contributors"></a> <img src="https://img.shields.io/github/languages/code-size/instaal-io/updaate" alt="Code Size"> 
  </p>

## Purpose

<b>updaate</b> is a Smart Android Library for checking your Android App Updates on <b>Google Play Store</b>. <b>updaate</b> checks the updates and notifies with beautiful <b>material design dialogs</b>. You can <b>customize</b> the dialog in various ways.

## Demo
Download and Check out the demo app for more

<a href="https://github.com/instaal-io/updaate/blob/master/test_demo.apk"> <img src="https://user-images.githubusercontent.com/42619122/155009169-c92bbebb-7e96-452e-956b-b5905d2cdcdc.png" height="100" width="200" alt="Download"/> </a>


## What's New
(Changes in 1.1)
- We have our brand new name "updaate".
- New 3 Different Layout Designs.
- Cool Looking **Editable** Animations.
- Easy Customization Options.

Check out `Releases` Tab for Info. Check out old documentation <a href="https://github.com/instaal-io/updaate/blob/master/old_readme.md">here</a>.

## Features
MiniUpdateChecker has these features:
- Checking Update for Your Android App on Google Play Store
- Material Design UI
- 3 Themes
- Highly Customizable

## Build Info
This library is built by this conifg:
- Compile SDK 32
- Minimum SDK 21
- Target SDK 32
- Built on Java 1.8
- Material Design using Androidx Library
- Jsoup for Parsing
- Lottiefiles for Animations

## Screenshot
Here is some screenshots of the library

| Default | Smart | Fancy |
|---------|--------|------|
| ![default](https://user-images.githubusercontent.com/42619122/155828397-f27780c7-db86-42b0-ac2d-e7a439f2ffc7.png) | ![smart](https://user-images.githubusercontent.com/42619122/155828399-deee9cb7-be9e-466a-b34d-1cc5aa693073.png) | ![fancy](https://user-images.githubusercontent.com/42619122/155828401-c3ece947-c03a-444f-a77a-9502961f279f.png) |



## Prerequisites

### Old
If you're using old gradle versions then follow this.
Add this in your root `build.gradle` file (**not** your module `build.gradle` file):

```gradle
allprojects {
	repositories {
		...
		maven { url "https://jitpack.io" }
	}
}
```

### New
If you're using new gradle versions then follow this.
Add this in your `settings.gradle` file:

```gradle
dependencyResolutionManagement {
    repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
    repositories {
       ...
        maven { url 'https://jitpack.io' }

    }
}
```

## Dependencies
Add this to your module's `build.gradle` file (make sure the version matches the JitPack badge above):

(Always use the latest version. Current Latest version is <a href="https://jitpack.io/#instaal-io/updaate"><img src="https://jitpack.io/v/instaal-io/updaate.svg" alt="JitPack"></a> )

```gradle
dependencies {
	...
		implementation 'com.github.instaal-io:updaate:1.1'

}
```


## Usage
MiniUpdateChecker has plenty of Options. Use Default theme or you can customize as much as you want. Here the usages for MiniUpdateChecker:

### Basic
#### Default Theme

```java
	new updaate(this).check();
```
```java
	new updaate(this)
		.setTheme(updaate.DEFAULT_THEME)
		.check();	
```
(Selecting no theme will automatically pick default theme)

#### Smart Theme
```java
	new updaate(this)
		.setTheme(updaate.SMART_THEME)
		.check();
```

#### Fancy Theme
```java
	new updaate(this)
		.setTheme(updaate.FANCY_THEME)
		.check();
```


### Customized

```java
	new updaate(this)
		.setTheme(updaate.DEFAULT_THEME)
		.setAppIcon(R.drawable.ic_baseline_account_balance_24)
		.setIconColor(R.color.colorPrimary)
		.setTitle("A New Update Available")
		.setPositiveLabel("Update Now")
		.setNegativeLabel("Maybe Later")
		.setBackgroundColor(R.color.white)
		.setPrimaryColor(R.color.colorPrimary)
		.setSecondaryColor(Color.parseColor("#888888"))
		.setPositiveTextColor(Color.parseColor("#eeeeee"))
		.setNegativeButtonColor(Color.parseColor("#eeeeee"))
		.shouldCheckAfterLaunch(1)
		.check();
```


## Customizations

### Themes
There different themese with pre desgined layouts, but you can customize them as well. If no theme defined then `Default Theme` will be used.

#### Default Theme
```Java
.setTheme(updaate.DEFAULT_THEME)
```
(If you don't select any theme, then default will be choosed automatically)

#### Smart Theme
```Java
.setTheme(updaate.SMART_THEME)
```

#### Fancy Theme
```Java
.setTheme(updaate.FANCY_THEME)
```

### Text (Title, Description, App Name, Positive Button Text, Negative Button Text)

Change different text on the layout by using these snippets.

```Java
.setTitle("")
.setDescription("")
.setAppName("")
.setPositiveLabel("")
.setNegativeLabel("")
```


### Image (App Icon, Close Icon)
Change the icons on the layout by using these snippets.

```Java
.setAppIcon(R.drawable.ic_baseline_10mp_24)
.setCloseIcon(R.drawable.ic_android_black_24dp)
```

### Colors (Background, Positive Button BG, Negative Button BG, Primary Text, Secondary Text, Positive Text Color, Negative Text Color)
Change the colors on the layout by using these snippets.
```Java
.setBackgroundColor(Color.parseColor("#ffffff"))
.setPositiveButtonColor(Color.parseColor("#00ACC1"))
.setNegativeButtonColor(Color.parseColor("#DDDDDD"))
.setPrimaryTextColor(Color.parseColor("#00ACC1"))
.setSecondaryTextColor(Color.parseColor("#444444"))
.setPositiveTextColor(Color.parseColor("#FFFFFF"))
.setNegativeTextColor(Color.parseColor("#444444"))
```
### Recheck
You can set check again for next launches, like after 5 app launch. If nothing set then it will check on Every Launch.
```Java
.shouldCheckAfterLaunch(1)

```

## Attributes

| Keyword | Attribute | Description
|---------------|---------|----------------------|
| `setTheme` | DEFAULT , MINI, SIMPLE | Select From Prebuilt Theme |
| `setTitle` | String | Dialog Title |
| `setAppIcon` | Drawable | Dialog Top Icon |
| `setCloseIcon` | Drawable | Dialog Close Icon |
| `setAppName` | String | Set App Name |
| `setPositiveLabel` | String | Positive Button Text |
| `setNegativeLabel` | String | Negative Button Text |
| `setBackgroundColor` | Int | Dialog Background Color |
| `setPositiveButtonColor` | Int | Positive Button Background Color |
| `setNegativeButtonColor` | Int | Negative Button Background Color |
| `setPrimaryTextColor` | Int | Color for Primary Texts |
| `setSecondaryTextColor` | Int | Color for Secondary Texts |
| `setPositiveTextColor` | Int | Color for Positive Button Text |
| `setNegativeTextColor` | Int | Color For Negative Button Text |
| `shouldCheckAfterLaunch` | Int | Again Check Settings |
| `check` |  | Start Checking for update |


## Notes
Here are some things you should remember:
- Always call `check()` at the end. Library won't work without it.
- If you don't set any them then the Default Theme will be selected automatically.
- If you don't set App name then it will be picked automatically. 
- If `shouldCheckAfterLaunch` is not used then lib will check for update in every launch.
- If the app is not live on store, then it won't show any dialog
- If the app is already latest version, then it won't show any dialog.

## Contribute
Please fork this repository and contribute back using [pull requests](https://github.com/instaal-io/updaate/pulls).

Any contributions, large or small, major features, bug fixes, are welcomed and appreciated.

Let me know which features you want in the future in `Request Feature` tab. 

If this project helps you a little bit, then give a to Star ⭐ the Repo. 

## Credits

Created with Love by <a href="https://github.com/instaal-io"> Instaal Studio </a> & <a href="https://github.com/ahmmedrejowan"> K M Rejowan Ahmmed </a>

## License
* [Apache Version 2.0](http://www.apache.org/licenses/LICENSE-2.0.html)

```
Copyright 2022 Instaal Studio

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

 http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

```
