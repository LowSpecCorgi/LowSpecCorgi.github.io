## Devlog 2 <!-- {docsify-ignore-all} -->

## Simple graphical interface
Like your average ~~skid~~ developer, I decided to go with a Java port for the popular single header library **Dear ImGui**

This allows me to make extreemely simple interfaces, without the need for **LWJGL** or masses of boilerplate code, rather:

```java
imGui.text("test");
```

Which will push some text to the screen.

**ImGui** is also customizable, with variables, like so:

```java
imGui.pushStyleColor(JImStyleColors.WindowBg, BACKGROUND_COLOUR);
imGui.pushStyleColor(JImStyleColors.SliderGrab, FOREGROUND_COLOUR);
imGui.pushStyleColor(JImStyleColors.SliderGrabActive, LIGHT_FOREGROUND_COLOUR);
imGui.pushStyleColor(JImStyleColors.Text, FOREGROUND_COLOUR);
imGui.pushStyleColor(JImStyleColors.TabActive, SECONDARY_COLOUR);
imGui.pushStyleColor(JImStyleColors.TabUnfocused, FOREGROUND_COLOUR);
imGui.pushStyleColor(JImStyleColors.TabHovered, LIGHT_FOREGROUND_COLOUR);
imGui.pushStyleColor(JImStyleColors.Separator, SECONDARY_COLOUR);
```

## Steps of development
Getting the basics, up and running, I decided to make the first basic settings and the title, which utilized a custom font for it's size and boldness.

Subsequently, I also added:
1. Framed the settings for style
2. Tooltips; You hover over some text like shown: `(?)`, and some text will display giving information about the proceeding action.

## Remarks
One thing that is *annoying* is *NativeInt*, as it requires the initialization to be deffered after **ImGui** has initialized, like so:

```java
this.leftBindCPS = new NativeInt();
this.leftBindCPS.modifyValue(leftBaseCPS);

this.rightBindCPS = new NativeInt();
this.rightBindCPS.modifyValue(rightBaseCPS);

this.maxLeftJitter = new NativeInt();
this.maxLeftJitter.modifyValue(leftMaxJitterCFG);

this.maxRightJitter = new NativeInt();
this.maxRightJitter.modifyValue(rightMaxJitterCFG);

this.maxRightInterpolation = new NativeInt();
this.maxRightInterpolation.modifyValue(rightMaxInterpCFG);

this.maxLeftInterpolation = new NativeInt();
this.maxLeftInterpolation.modifyValue(leftMaxInterpCFG);
```