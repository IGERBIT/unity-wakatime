# unity-wakatime
A [WakaTime](https://wakatime.com) plugin for [Unity](https://unity.com).

![Screenshot](https://user-images.githubusercontent.com/7955682/38732057-79cf45b4-3f25-11e8-958f-07ba5290caba.PNG)

## About

Existing solutions (neither https://github.com/josec89/wakatime-unity nor https://github.com/bengsfort/WakaTime-Unity) didn't work for me, so I decided to implement my own variant.

The code has been successfuly tested with following Unity versions:

* 2017.4.0f1
* 2018.1.0b13 (although getting `'UnityEditor.EditorApplication.hierarchyWindowChanged' is obsolete: Use 'EditorApplication.hierarchyChanged'` warning)

## Installation

1. Copy `Plugins` folder into your project Assets
2. Go to `Window/WakaTime` in the Editor and insert your API key (grab one from https://wakatime.com/settings/account)
3. Press `Save Preferences`
4. Check if `"Unity"` editor appears at https://wakatime.com/api/v1/users/current/user_agents (may be a bit delayed)
5. Enjoy!

## Usage

The plugin will automatically send heartbeats to WakaTime after following events:

* DidReloadScripts
* EditorApplication.playModeStateChanged
* EditorApplication.contextualPropertyMenu
* EditorApplication.hierarchyWindowChanged
* EditorSceneManager.sceneSaved
* EditorSceneManager.sceneOpened
* EditorSceneManager.sceneClosing
* EditorSceneManager.newSceneCreated
