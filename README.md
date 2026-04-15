# BeauUI_UE5_Framework

A Framework developed by your truly, its lightweight and minimalist Unreal Engine 5 User Interface Framework and designed for you to build upon.

## Modifictions:
1. If you patch bugs -> You can submit a pull request to the main branch
2. If you make significant changes and cause you have to share that with the class, please either fork it or create a new branch.
3. DO NOT REMOVE THE COPYRIGHT NOTICE FOR EPIC GAMES, if you do that's on you!

## Copyright
1. My Music is all rights resevered, in General Unless you try to claim it as yours or remove my music attribution, I will not do anything.

2. If you remove my music, you can remove my copyright credit for the music.


### Graphics

**This was all made on an RTX 3050 6-gigabyte model, and it runs 60fps, in editor.**
(If one of y'all could like add an FPS counter, that'd be sick, I'd allow that in the Main branch)

### Doc 1 : Getting started:

Download the release, then drag it into your projects `content` folder,

after this, then enter editor. The font and refs will be broken.

***actual first: make sure you move those assets into a new IN EDITOR CREATED FOLDER!***

First go into Google sans font option (the variable one) with the `[A]` place holders, and switch its font family from `none` to `Google sans variable`
Then go into Google Sans font option (bold), and replace the `none` to `Google Sans Bold`

Then go into all the WBPs and click on each text and change the font family from `none` to `Google Sans` either bold or Normal (variable) 

then Go into your Level BP, and off event begin play do this: 


``` Blueprints

EventBeginPlay() -> setInputModeUIOnly -> Set Show Mouse cursor(True/on) -> Create Widget(filter -> Main menu) -> add to viewport;
    get player controller() ----↑----------------↑

```

once this is done, simply a case inside of the `WBP_MainMenu` graph, changing the `none` on `CreateWidget` to whatever widget fits that buttons text. 

after this, go into every WBP (including combat warning for the font) and change the font family from `none` to `Google Sans` (Bold or Normal, Your choice) than after this change the `none` on `create widget` to `MainMenu` and do this for the MainMenu Widget Blueprints, once this is done, well that's it. (Check the BP for activating the combat warning if the WBP is still referenced, if it isn't set that to combat warning)

For `new game` in the `WBP_MainMenu` do this in the graph:

``` Blueprints

Button() -> SetInputModeGameOnly -> set show cursor(false/off) -> OpenLevelByObjectReference(filter -> **whatever your level is called**)
  getplayercontroller() ---↑---------------↑


```

(Music manager was removed cause it was horribly broken)

