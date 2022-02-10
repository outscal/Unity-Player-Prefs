# Introduction

Hi there fellow clanmate, welcome to this short course on Player Preferences or PlayerPrefs in Unity!

![Hi!](https://media.giphy.com/media/3pZipqyo1sqHDfJGtz/giphy.gif)

Have you ever felt like you have played a lot and the game is still going on, so wouldn't it be great to start from a checkpoint tomorrow, saving your current progress. This is called saving and some devices or consoles also uses memory cards to store certain information, like playstations.

![Intro!](https://media.giphy.com/media/98qNB9zZFJrm7xaqsq/giphy.gif)

In order to save the game progress, Unity provides something called “Player Preferences” or ‘PlayerPrefs’ in short. This is a class that stores Player preferences between game sessions. What this means is, say you exit from the game today and re-open it tomorrow, it should be able to save your previous session and start from where you left off and shouldn’t start from the beginning of the game itself, what we call as ‘SAVING’ in games. PlayerPrefs can store string, float and integer values into the user’s platform registry. The location of saving these values will depend on the type of platform being used as mentioned below.

**Standalone Player storage location**

On macOS, PlayerPrefs are stored in

~/Library/Preferences/com.ExampleCompanyName.ExampleProductName.plist

Unity uses the same .plist file for projects in the Editor and standalone Players.

On Windows, PlayerPrefs are stored in HKCU\Software\ExampleCompanyName\ExampleProductNamekey.

On Linux, PlayerPrefs are stored in ~/.config/unity3d/ExampleCompanyName/ExampleProductName

On Windows Store Apps, PlayerPrefs are stored in %userprofile%\AppData\Local\Packages\[ProductPackageId]\LocalState\playerprefs.dat

.On Windows Phone 8, Unity stores PlayerPrefs data in the application's local folder. See [Directory.localFolder](https://docs.unity3d.com/ScriptReference/Windows.Directory-localFolder.html)

for more information.

On Android, PlayerPrefs are stored in /data/data/pkg-name/shared_prefs/pkg-name.v2.playerprefs.xml

. Unity stores PlayerPrefs data on the device, in [SharedPreferences](https://codelabs.developers.google.com/codelabs/android-training-shared-preferences/index.html?index=..%2F..android-training#0)

. C#, JavaScript, Android Java and native code can all access the PlayerPrefs data.

On WebGL, Unity stores PlayerPrefs data using the browser's IndexedDB API. For more information, see [IndexedDB](https://developers.google.com/web/ilt/pwa/lab-indexeddb#overview)

**In-Editor Play mode storage location**

On macOS, PlayerPrefs are stored in /Library/Preferences/[bundle identifier].plist

On Windows, PlayerPrefs are stored in HKCU\Software\Unity\UnityEditor\ExampleCompamyName\ExampleProductName key.

Windows 10 uses the application’s PlayerPrefs names. For example, Unity adds a DeckBase string and converts it into DeckBase_h3232628825. The application ignores the extension. Unity stores PlayerPrefs in a local registry, without encryption. Do not use PlayerPrefs data to store sensitive data.
There are a lot of different data types that can be stored using this class, of course using Get and Set methods they can be fetched and set respectively. The various data types allowed are:
****Float**** 
****Int**** 
****String****

Move on to the next to get more insights on this topic.

![Go On!](https://media.giphy.com/media/LXl3KHf5t90u3uykMJ/giphy.gif)



