# Example Use case Lock/Unlock Levels

A very important use case of PlayerPrefs is for Locking levels. You can create an enum of different statuses as shown below, based on the requirements of your game:

![Status_levels](https://user-images.githubusercontent.com/44625252/152965223-e7756f9b-1acc-429b-a276-2a1562a47253.PNG)

As shown in the example above, every time a level is completed, you have the status as “Completed”, levels that are unlocked will have the “Unlocked” status, and levels that have not been played yet will be kept as “Locked”. The following shows the buttons for levels, you can design in a similar way: 

![AllLevels](https://user-images.githubusercontent.com/44625252/152965287-d83b8a3f-8911-4919-bd0c-c97681c303b8.PNG)

Then, for each button, the status can be set based on its state, of course, levels such as the lobby (menu screen) and Level 1 (the very first level) needs to be kept at ‘Unlocked’ status from the beginning so that they can be accessed by the user in the Start itself. The below shows an example of a switch case statement that allows the button click function to work only when the level is in ‘Unlocked’ status:

![Button_locks](https://user-images.githubusercontent.com/44625252/152965450-deae1e6b-f46e-47ca-bfd1-71db73389143.PNG)

Finally, the PlayerPrefs can be set and fetched as required as shown below:

![Prefs_levelValue](https://user-images.githubusercontent.com/44625252/152965502-abd34388-1fab-4c26-8c2d-901656df8eb2.PNG)

You can always find the values in your local device in places, for example, the below shows the storage location on a Windows PC (in the registry editor): 

![Reg_ed](https://user-images.githubusercontent.com/44625252/152965555-8ef2a77e-4d98-454f-8c03-10d008671446.PNG)

---
<aside>

> 💡 🚀 **[Join Discord Server](https://discord.gg/J5zDscnzms) → Get your doubts solved by experts instantly**
</aside>

![discord_png](https://user-images.githubusercontent.com/44625252/152948137-97167a02-bba1-47b9-b33c-fb2ac41f11fc.png)

---
