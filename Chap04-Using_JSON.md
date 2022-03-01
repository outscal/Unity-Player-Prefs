# Using JSON file to save data

You can also save the data automatically using a particular type of file. Can you think of any file type that helps us save a list of data?

![Qu!](https://media.giphy.com/media/64afibPa7ySzhFAf00/giphy.gif)

The main three methods in *PlayerPrefs* are “Set”, “Get”, and “Save”.

PlayerPrefs can also be combined with JSON to store even more data. Using script, the following could be included in the code so it does the job:

```
//use Unity's JsonUtility to save the above data.
//JsonUtility.ToJson will return a string so we can use it with player prefs
PlayerPrefs.SetString("SavedPlayer", JsonUtility.ToJson(savedPlayer));

//make sure to save
PlayerPrefs.Save();
```

A more detailed information and reference regarding the above can be found here: [JsonUtility](https://bootcamp.uxdesign.cc/unity-feature-101-basic-saving-using-playerprefs-2fc737d1ac7b)

JSON, derived from JavaScript Object Notation Syntax, is a way of encoding data
When storing data, the data has to be in a certain format, and regardless of where you choose to store it, the text is always one of the legal formats.
JSON makes it possible to store JavaScript objects as text. Think of it as a small database with some data that can be again extracted back to any other system, decoding it.

So, having fun yet? Move on to the next to see how you can share some of your learnings with us!

![Action!](https://media.giphy.com/media/Mgt4Ttvxfp7CmedT5m/giphy.gif)
