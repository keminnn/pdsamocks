# PDSA Mock Interview Timer

A single file HTML countdown timer for the PDSA Mock Interview Program at UCF. It runs full screen on any phone or laptop and keeps every room in sync, since each device figures out the current phase from the actual time of day instead of someone pressing start. No install, no login, works offline once the page is open.

## What it does

Each interview slot is 45 minutes, split into four phases:

- File Review, 5 minutes
- Interview, 25 minutes
- Feedback, 10 minutes
- Buffer, 5 minutes

It cycles through these on its own for however many slots run that day, shows a countdown before the first slot starts, and a closing screen after the last one ends. Open it on six phones in six rooms and they all show the same phase and countdown.

## How to use it

1. Open the timer, either way works:
   - Visit https://keminnn.github.io/pdsamocks/
   - Or open `mock-interview-timer.html` from this repo in any browser
2. Put the browser in full screen
3. Leave it running, it handles the rest

## Changing it for a new event

Open the HTML file and find the config section near the top of the script:

- `DEFAULT_ANCHOR_START`, when the first slot starts
- `DEFAULT_NUM_CYCLES`, how many slots run that day
- `PHASES`, the name, note, length, and color of each phase

## Testing it early

Add parameters to the end of the URL to preview it without waiting for the real time:

```
mock-interview-timer.html?speed=60&cycles=1
```

This will run the timer at 60x speed for one slot, and a yellow test mode banner shows up so you know it's not the live version.

- `speed`, how much faster than real time it runs
- `cycles`, number of slots for the test
- `start`, override the start time
- `preroll`, seconds of the pre start screen to show first
