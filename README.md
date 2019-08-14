# Introduction to the micro:bit

## Get Started
- Open https://makecode.microbit.org/
- Connect the micro:bit via USB
- Save file to "USB Drive"

## Show icon ♥
onstart
	showicon

## Hello, World
onstart
	show string

## Forever
forever
	showicon
	showicon

## Shake
on shake
	showicon

## Buttons
on button A pressed
	showstring A
on button B pressed
	showstring B

## Counter (variable)
counter (variable)
	on start
		n = 0
	forever
		show number n

## Dice (random number)
<img src="images/dice.png" width="512" />

```
input.onGesture(Gesture.Shake, function () {
    basic.showNumber(Math.randomRange(1, 6))
})
```

Or with a variable

<img src="images/dice-with-variable.png" width="512" />


```
let result = 0
input.onGesture(Gesture.Shake, function () {
    result = Math.randomRange(1, 6)
    basic.showNumber(result)
})
```

## Rock, Paper, Scissors
<img src="images/rock-paper-scissors.png" width="512" />

```
let hand = 0
input.onGesture(Gesture.Shake, function () {
    hand = Math.randomRange(0, 2)
    if (hand == 0) {
        basic.showIcon(IconNames.SmallSquare) // Rock
    } else if (hand == 1) {
        basic.showIcon(IconNames.Square) // Paper
    } else { // hand == 2
        basic.showIcon(IconNames.Scissors)
    }
})
```

=> make two, see who wins

## Beep
sound
	how to connect the hardware
	on shake
		set pin

## Radio Alert
radio
	on shake
		send alarm
	on radio
		ring the alarm

## List
list
	?
## More
- See https://makecode.microbit.org/projects
