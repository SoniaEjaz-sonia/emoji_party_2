# emoji_party_2

Developments on top of [emoji_party_1](https://github.com/SpiRaiL/emoji_party_1)

* Drag and drop emojis on the screen.
* Add, select and delete
* When selected, all emojis will drag together
* Reorder the heights of emojis
* Resize any emoji by dragging edges and corners
* Selecting an emoji will recursively select emojis on-top of it
* Clicking info wills show some debug data about the emoji indexes and heights
* In debug (info icon) you can view some of the calculated data

## Latest screen shot

![In app screenshot](./screenshots/Screenshot.png?raw=true "Screenshot")

## Some features

### Debug

Shows debug mode (top right icon)
i: stack index
h: height (ie: number of emojis under in a stack)
p: number of "parent" emojis (ie: directly below)
c: number of "child" emojis, (ie: directly above)
Note, this is not the same as "parent" and "child" in flutter.

This also shows some more data in the debug console

![screenshot2](./screenshots/Screenshot2.png?raw=true "Screenshot")

### Recursive select/deselect

Recursive select will select all emojis above the selected one.
This allows for quickly selecting and moving a group of emojis, simply by selecting the bottom one.
In this case we click rock-climber (which is at height 0)
Dice is selected as it is immediately above it.
Wizard is not selected as it is at height 2 due to the truck that the exclamation mark. Therefore the wizard is not really sitting on the rock-climber.
![screenshot3](./screenshots/Screenshot3.png?raw=true "Screenshot")

### Auto height

When a large emoji is dragged or scaled over a smaller one, it will automatically fall below that emoji

![screenshot4](./screenshots/Screenshot4.png?raw=true "Screenshot")

Here we see airplane-arrival fall under book and yo-yo, but not under fast-forward.

![screenshot5](./screenshots/Screenshot5.png?raw=true "Screenshot")

Similarly, dragging a small emoji completely under a large one will cause it to pop on top of the larger one. Here we see the fast-forward icon jump on-top of airplane arrival, but not the yo-yo.

![screenshot6](./screenshots/Screenshot6.png?raw=true "Screenshot")

## Known issues

* Rotate function is experimental and causes drag and scale to behave badly. There is not plan to fix this at this time.
* Some Emojis don't render
* Android has an issue with scaling emojis above a certain size. [Stackoverflow question here](https://stackoverflow.com/questions/74240624/does-flutter-have-a-way-around-androids-size-limit-on-emojis). The workaround here is just to limit the size of the boxes.

## What is this project?

“Emoji party” is an open-source project that I am working on.

It is not intended to provide any direct value as an app or a game. (Although it would be funny if it turns into something like that).

All of the demonstrated functions in this repository are made freely available for other developers to use in their projects. As such all works in the Lib directory are licensed under creative commons CC0 1.0 Other files are generated by the flutter framework and associated plugins and packages are under whatever licenses are connected to those projects.

The project is a personal learning exercise, as well as, an easy-to-share project that demonstrates some functionality that I require in other private projects. This allows the occasional voluntary contributor or even a contractor to achieve some nice-to-have ideas, without any need for NDA’s, access rights, or red-tape. Hopefully this also contributes something to the open-source community.

Feel free to fork and pull request for minor changes. Happy to get feedback.

Feel free to fork and make your own video tutorials based on this code. No attribution is required.( But, I’m always glad to hear about it).
