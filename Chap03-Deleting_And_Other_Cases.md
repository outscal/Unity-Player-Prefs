# Deleting PlayerPrefs

Now that you know these values need to be stored somewhere so that your system knows where the game is saved, you might also be wondering if these can be deleted as well.

![huh!](https://media.giphy.com/media/KGSxFwJJHQPsKzzFba/giphy.gif)

The answer is yes. Anything that is stored, can also be removed from system. So the tricks below can help you delete any of your saved game checkpoints if you want to.

You can come inside the storage location and delete the values manually if you want to not have the saved values for any reason (for example, When the User wants to delete all saves and start a New Game) otherwise, there are 2 other ways to clear all values: Y

- Use DeleteAll or DeleteKey functions using the C# script
- Use Clear All PlayerPrefs option under Edit category:

![ClearAllPrefs](https://user-images.githubusercontent.com/44625252/152966093-102293b5-95fd-481c-b7de-ebc99e6d6bf1.png)

# Other Use Cases

Some other ways of using PlayerPrefs are shown below with use cases:

- High Scores

![High_score](https://user-images.githubusercontent.com/44625252/152966393-a3e0dec6-8254-4b9f-82e0-7e7fbf011631.png)

```
public void UpdateHighScore(float finalTime)
{
  float previousHighScore = float.Maxvalue;
  
  if(PlayerPrefs.HasKey(HIGHSCORE_KEY))
  {
    previousHighScore = PlayerPrefs.GetFloat(HIGHSCORE_KEY);
  }
  if(finalTime < previousHighScore)
  {
    PlayerPrefs.SetFloat(HIGHSCORE_KEY, finalTime;
    PlayerPrefs.Save();
  }
}
```

- Scores of individual players in a multiplayer game
- Creating multiple saves for a game at certain checkpoints

```
public void OnTriggerEnter2D(Collider2D collision)
{
  if(collision.CompareTag("Player"))
  {
    PlayerPrefs.SetFloat("x", posX);
    PlayerPrefs.SetFloat("y", posY);
    PlayerPrefs.SetFloat("z", posZ);
  }
}
```

- Levelling up stats for the player
- Timestamps

```
//Save the current system time as a string in the player prefs class
PlayerPrefs.SetString("sysString", System.DateTime.now.ToBinary().ToString());

print("Saving this date to prefs: " + System.DateTime.Now);
```

- Saving Game settings
- Clearing/removing specific PlayerPref values

Think of some other use cases of PlayerPrefs, then try to implement them in your game. Come on, you can do more!

![More!](https://media.giphy.com/media/3oKIPEh5Lk3RGSIFEI/giphy.gif)
