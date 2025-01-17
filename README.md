![Gamemela Logo](docs/images/Gamememla Signature Size Logo.png)
# Gamemela SDK
_Copyright (c) 2016 Funizen Inc. All rights reserved._

## Overview

The GAMEMELA SDK allows you to access the GAMEMELA Services API.
The plugin provides support for the following features of the GAMEMELA API:<br/>
* sign up
* sign in
* sign out

All features are available on Android.

Installation of GamemelaSDK
-----------------------

1. [[Download GamemelaSDK Plugin for Unity.](ARCHIVE.md)]
2. Open your project for Unity.
3. Import downloaded package [gamemela-unity-sdk.x.y.z.unitypackage].
4. Gamemela -> Edit Settings
  * ![MainMenu->Gamemela->Edit Settings](docs/images/GamemelaScreenShot-GamemelaSettings.jpg)
5. Google Play Games
  * ![MainMenu->Google Play Games->Setup->Android setup...](docs/images/GamemelaScreenShot-AndroidSetup.jpg)

GamemelaSDK Built with
-----------------------
1. Unity 5.3.5f1 
2. Android SDK Manager Settings (*)
	* Tools
		* Install Android SDK Build-tools 23.0.3
		* Install Android SDK Tools 25.1.7
		* Install Android SDK Platform-tools 24
		* Uninstall all the rest in Tools category.
	* None of [Android N] and [preview] things...
	* ![](docs/images/android-sdk-manager.jpg)
	


Usage for social features.
-----------------------
### Namespace
	using GamemelaSdk.Unity;

### Initialize
		GM.Init();

### Check sign in
		if (GM.IsSignedIn())
		{
			Debug.Log("Gamemela signed in.");
		}
		else
		{
			Debug.Log("Gamemela signed out.");
		}

### Sign in
		GM.LoadPageSignIn((success, message)=> {
			Debug.Log("OnButtonSignInGamemela: " + success + " / " + message);
		});

### Show Notices and Events after check them exists.
		GM.ShowNoticePopup((success, message)=> {
			Debug.Log("Notices: " + success + " / " + message);
		});

### Customer Service
		GM.LoadPageCustomerService();

### Sign out
		GM.SignOut();

# References
-----------------------

_[Facebook SDK for Unity](https://github.com/facebook/facebook-sdk-for-unity)_

_[Google Play Games plugin for Unity](https://github.com/playgameservices/play-games-plugin-for-unity)_

_[Google Analytics Plugin for Unity](https://github.com/googleanalytics/google-analytics-plugin-for-unity)_

_[unity-webview](https://github.com/gree/unity-webview)_

_[Unity HTTP](https://github.com/andyburke/UnityHTTP)_

......


