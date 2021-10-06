# Nibbler

_"By far the best ICCF analysis tool for Leela." &mdash; *jhorthos*_

Nibbler is a real-time analysis GUI for [Leela Chess Zero](http://lczero.org/play/quickstart/) (Lc0), which runs Leela in the background and constantly displays opinions about the current position. You can also compel the engine to evaluate one or more specific moves. Nibbler is loosely inspired by [Lizzie](https://github.com/featurecat/lizzie) and [Sabaki](https://github.com/SabakiHQ/Sabaki).

These days, Nibbler more-or-less works with traditional engines like [Stockfish](https://stockfishchess.org/), too.

For prebuilt binary releases, see the [Releases](https://github.com/Jac-Zac/Nibbler_MacOS/releases/tag/2.1.7) section. For help, the [Discord](https://discordapp.com/invite/pKujYxD) may be your best bet, or open an issue here.

![showcase1](https://raw.githubusercontent.com/Jac-Zac/Nibbler_MacOS/main/assets/showcase.png)

## Features

* Display Leela's top choices graphically.
* Winrate graph.
* Optionally shows Leela statistics like N, P, Q, S, U, V, and WDL for each move.
* UCI `searchmoves` functionality.
* Automatic full-game analysis.
* Play against Leela from any position.
* Leela self-play from any position.
* PGN loading via menu, clipboard, or drag-and-drop.
* Supports PGN variations of arbitrary depth.
* FEN loading.
* Chess 960.

## Installation - the simple way

Some MacOS standalone releases are uploaded to the [Releases](https://github.com/Jac-Zac/Nibbler_MacOS/releases/tag/2.1.7) section from time to time.

When you download it you have other things like a version of stokfish and lc0.

## Installation - the most up to date way

##### Change directory, give executable permission and run the file 

    cd src && chmod +x build_mac.sh && ./build_mac.sh`

> I'll try to keep the src file decently up to date but if you want the latest version just switch them out for the one from the [nibbler](https://github.com/rooklift/nibbler) original project.


## My custom configuration

I have customized my App to have it look a bit nicer in my set up, this is how it turned out:

![showcase1](https://raw.githubusercontent.com/Jac-Zac/Nibbler_MacOS/main/assets/my_setup.png)

> The colors I used follow the nord theme. And also got rid of the annoying title bar. 

*Those are the [`default`](src/original_src) src, and you can find [`mine here`](src/app)*

## Advanced engine options

Most people won't need them, but all of Leela's engine options can be set in two ways:

* Leela automatically loads options from a file called `lc0.config` at startup - see [here](https://lczero.org/play/configuration/flags/#config-file).
* Nibbler will send UCI options specified in Nibbler's own `engines.json` file (which you can find via the Dev menu).

## Hints and tips

An option to enable the UCI `searchmoves` feature is available in the Analysis menu. Once enabled, one or more moves can be specified as moves to focus on; Leela will ignore other moves. This is useful when you think Leela isn't giving a certain move enough attention.

Leela forgets much of the evaluation if the position changes. To mitigate this, an option in the Analysis menu allows you to hover over a PV (on the right) and see it play out on the board, without changing the position we're actually analysing. You might prefer to halt Leela while doing this, so that the PVs don't change while you're looking at them.

Leela running out of RAM can be a problem if searches go on too long. You might like to set a reasonable node limit (in the Engine menu), perhaps 10 million or so.

## Thanks

Thanks to everyone in Discord and GitHub who's offered advice and suggestions; and thanks to all Lc0 devs and GPU-hours contributors!

The default pieces are from [Lichess](https://lichess.org/).
On the other hand the one I use in my specific configuration are from [chess.com](https://www.chess.com/).
