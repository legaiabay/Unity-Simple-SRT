# Unity-Simple-SRT (Modified)
A modified super simple SRT subtitle parser

Original by roguecode and Modified by Legaiabay.

It'll parse most sane SRT's, and will display them in a `Text` element, crossfading between lines depending on a `Fade Time` you set.

## To use it
- Add the `Subtitle Displayer` component to something in the world. 
- Create two `Text` UI elements, both the same, and drag their references to the `Subtitle Displayer` component.
- With this modified script, now you can choose between `Text Asset` or `SRT` mode in `Subtitle Displayer` component. `Text Asset` mode will use same method as original by renaming `.srt` file to `.txt`. With `SRT` mode, you can directly use `.srt` file without renaming it by putting `.srt` file to `StreamingAssets` folder and add file path to `Subtitle Path` in `Subtitle Displayer` component.
- Simply Call `BeginSubtitle()` to start the subtitles.

A sub file like this:
```
1
00:00:00,000 --> 00:00:02,500
Mary had

2
00:00:02,500 --> 00:00:04,500
a little <i>lamb</i>

3
00:00:04,500 --> 00:00:06,500
little <b>lamb</b>

4
00:00:06,500 --> 00:00:08,500
little <size=40>lamb</size>

5
00:00:09,000 --> 00:00:12,000
<b><i><color=red>Until she didn't.</color></i></b>
```
Will result in this:

![Totally the best gif evar](https://github.com/roguecode/Unity-Simple-SRT/blob/master/Preview.gif?raw=true)

A good program to make subs is [SubtitleEdit](https://github.com/SubtitleEdit/subtitleedit/releases)
