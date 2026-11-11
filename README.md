read ai slop sum below: (hope ur day is going great)

## Music tools

- [Note / line](https://github.com/dylancetin/songsterr-to-readable-notation) turns a Songsterr track into letter notes like `C4` and lines up the rhythm and lyrics under the melody. It plays the selected part and highlights the current bar.
- [Hece](https://github.com/dylancetin/cover-songwriting-app) is for writing Turkish covers. You import an Ultimate Guitar chord sheet and write your lyrics under it one syllable at a time. The chords stay above the original syllables. Hece saves songs in your browser, so you don't need an account.
- [Sixfold](https://github.com/dylancetin/sixfold-guitar-composition) is a library of acoustic guitar arrangements. Each one opens in a score viewer with a practice player, and you can download it as PDF or MIDI. AI agents write the arrangements, and the website only displays them.

## Other projects

- [anki-quick-card-gen](https://github.com/dylancetin/anki-quick-card-gen) makes Anki cards from a PDF. You go through the pages and an LLM writes basic, type-in, cloze, and image cloze cards. It works with Claude, OpenAI, and OpenRouter keys. It exports an `.apkg` file, and Anki imports the cards and their images in one step. You can try it at [anki.taylan.co](https://anki.taylan.co).
- [Project Shelf](https://github.com/dylancetin/project-shelf) is the start page for my home server. It lists my local projects and self-hosted services. Clicking a project starts its dev server, waits until it responds, and then opens it. It runs on Bun with Hono and SQLite, and the frontend is React.

## Hardware test lab

[tezgah-lab](https://github.com/aarmert/tezgah-lab) holds three repos that test firmware on real STM32 microcontroller boards. A person or a coding agent runs the tests from the command line, and results can come back as JSON. Every test also runs against something broken on purpose and has to catch it. I built it with [aarmert](https://github.com/aarmert). I'm the main author of the first two repos below, and aarmert is the main author of the third and of tezgah-lab itself.

- [f407-hil-bench](https://github.com/aarmert/f407-hil-bench) flashes and resets an STM32F407 Discovery board, talks to it over serial, and runs test plans written in TOML. It recovers a hung or crashed board by itself. A `--sim` mode runs the plans without hardware.
- [f407-camera-blink](https://github.com/aarmert/f407-camera-blink) measures an LED's blink rate from phone video, frame by frame. The bench uses it to check the board's LEDs without anyone watching. An LED set to 1, 2, and 4 Hz measured 0.995, 1.985, and 4.007 Hz. The board's clock runs 0.5% slow, and each result is within 0.7% of the rate that clock gives.
- [c031-ab-bootloader-stress](https://github.com/aarmert/c031-ab-bootloader-stress) stress-tests an A/B bootloader on an STM32C031. The bootloader writes each update to a second slot, so the running firmware is never touched. The test resets the board during real firmware updates. It found 0 failures in 3103 trials. A deliberately unsafe bootloader booted a corrupt image in 11 of 20 trials, and the test caught every one.

## Setup

My [Neovim config](https://github.com/dylancetin/nvim) started from kickstart.nvim. [suckless-utils-linux](https://github.com/dylancetin/suckless-utils-linux) has my dwm, dmenu, and slstatus builds from 2021, when Arch was my main OS.
