<h1 style="border: 0px solid transparent;margin-bottom:-10px;">ElegantFin Theme <p style="font-size:15px;margin-top:6px;">(Modified)</p></h1>
This is a Jellyfin theme inspired from JellySeerr to improve the overall look and experience with various fixes to the UI and behaviour.

#### **Original Author:** [lscambo13](https://github.com/lscambo13)

#### **Modiifed By:** [Zach J Murphy](https://github.com/zacjmurphy)

### ✨ Key Features
- modern layouts and colors
- new animations on some elements
- reduced clutter by hiding unimportant buttons and elements
- overall rounded design
- stylish borders, hover effects and shadows
- various fixes to the user experience

### 👇 How to install/setup this theme?

<b>Paste the following in Custom CSS code box:</b>

```
@import url("https://cdn.jsdelivr.net/gh/zacjmurphy/Docker-Backup@main/configs/Jellyfin/jellyfin-custom.css");
```

<details>
  <summary><i>Detailed steps for server-side implementation</i></summary>

1. Open Dashboard from Administration tab in Settings.
2. Select General tab from the side bar.
3. Scroll down to find Custom CSS code box under Branding section.
4. Paste the custom css in Custom CSS code box.
5. Click save
</details>

<details>
  <summary><i>Detailed steps for client-side implementation</i></summary>

1. Open Display tab in Settings.
2. Scroll down to find Custom CSS code box.
3. Paste the custom css in Custom CSS code box.
4. Click save.
</details>

### 🧩 How to customize this theme?

<details>
  <summary><i>1. Custom media covers for user media libraries</i></summary>

- [Previews](https://github.com/lscambo13/ElegantFin/blob/main/custom-media-covers.md#%EF%B8%8F-presets-modify-these-styles-according-to-your-own-liking)
- Read more about this experimental add-on [here](https://github.com/lscambo13/ElegantFin/blob/main/custom-media-covers.md)

</details>

<details>
  <summary><i>2. Custom background image for the login page</i></summary>

- [Preview](https://user-images.githubusercontent.com/16425113/129554147-6ac7ba51-43e7-4c8e-ba77-e646a3ef6b12.jpg)
- To enable the background wallpaper on the login screen, first tick the 'Enable the splash screen' option in your Jellyfin Dashboard below the Custom CSS Box.
- Second, copy and paste the following code at the end in Custom CSS box but don't save yet.
  ```
  :root {
    --loginPageBgUrl: url('<YOUR-JELLYFIN-SERVER-ADDRESS>/Branding/Splashscreen?format=webp&foregroundLayer=1&quality=33&width=3840&height=2160&blur=2');
  }
  ```
- Third, replace `<YOUR-JELLYFIN-SERVER-ADDRESS>` with your Jellyfin server address, for example, `http://192.168.0.1:8097`.
- Don't forget the correct http or https in your domain.
- You can also modify the parameters, for example blur size or the resolution, according to your liking.
- Once done, save and refresh your apps and webpages.
</details>

<details>
  <summary><i>3. Bring back the home button in the app header</i></summary>

- Read more about steps [here](https://github.com/lscambo13/ElegantFin/issues/51)

</details>

### 🆗 Tested on
- Jellyfin Server v10.10.7
- Jellyfin Android App v2.6.2
- Jellyfin Windows App v10.10.7

### 🛠️ Troubleshooting
<details>
  <summary>1️⃣ - <i>How do I check if I am using the latest version on ElegantFin?</i></summary>

- To make sure that you are using the latest version of ElegantFin, check the version number at the bottom in the Dashboard screen.
- It should be something like ElegantFin v25.03.XX
</details>

<details>
  <summary>2️⃣ - <i>I see that a newer version is available, but I have not received it yet. Why?</i></summary>

- If Dashboard footer shows an old version, it means that your app is still using an old cache.
- Once that cache is updated, the new version will be loaded.
- To get the latest version, you will need to clear cache. There are multiple ways to do it.
- On web version, force a hard refresh of the page using CTRL + F5.
- On apps, try signing out and back in again. OR in case of Jellyfin Media Player on windows, you might need to delete the cache folder. That should definitely pull the latest version.
</details>

<details>
  <summary>3️⃣ - <i>Why do I notice visual bugs and inconsistencies on Jellyfin Media Player?</i></summary>

- Currently JMP uses Qt 5.x which uses an outdated web engine, so many new CSS features do not work. Once they release a new version based on Qt 6.x, most issues should automatically be resolved. Until then, I advise using the web app instead.
</details>

<details>
  <summary>4️⃣ - <i>All the icons on my LG TV seem to be broken. How to fix them?</i></summary>

- It seems that modern Material Icons which this theme uses are [not compatible on some WebOS TVs](https://github.com/lscambo13/ElegantFin/issues/39). There is a [huge similar thread](https://www.reddit.com/r/youtubetv/comments/e27go3/chinese_symbols_instead_of_icons_on_lg_tv/) about this.
- This bug can be fixed by using the older icons, so I have implemented the following workaround to bring back older, supported icons.
- Simply add the following code at the end in Custom CSS box and save, then refresh your apps and webpages:

  ```
  :root {
    --iconPack: 'Material Icons';
  }
  ```
</details>

<details>
  <summary>5️⃣ - <i>How do I report bugs/issues?</i></summary>

- First check [here](https://github.com/lscambo13/ElegantFin/issues?q=) whether a similar issue has been reported already. If it exists, upvote and comment there to let me know.
- Alternatively, create a new issue [here](https://github.com/lscambo13/ElegantFin/issues/new/choose).


</details>
<details>
  <summary>6️⃣ - <i>When can I expect another update?</i></summary>

- 🤷
</details>
