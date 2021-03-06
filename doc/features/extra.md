# DeckDeckGo - Extra Features

The [DeckDeckGo] deck expose a couple of extra features which could be added to your presentation too.

## Table of contents

- [Extra features](#extra-features)
  - [Toggle on/off the full screen mode](#toggle-onoff-the-full-screen-mode)
  - [Print the presentation](#print-the-presentation)
  - [Mobile](#mobile)
- [Extra events](#extra-events)

## Extra features

[DeckDeckGo] offers currently two extra features available on the deck element `<deckgo-deck>`.
                                                 
For example, in Vanilla Javascript, we would get a reference to the deck using the following selector:

```
const deck = document.getElementsByTagName('deckgo-deck');
```

### Toggle on/off the full screen mode

```
await deck.toggleFullScreen();
```

### Print the presentation

```
await deck.print();
```

### Mobile

A util method to know if the current presentation is browsed on a mobile device or not.

```
await deck.isMobile(); // resolve a boolean
```

## Extra events

[DeckDeckGo] triggers the following events:

| Event                     | Emitted value | Description |
| -------------------------- |:-----------------:|:-----------------:|
| slidesDidLoad | string[] | Emitted when the deck and all slides have loaded. Emit the an ordered list of all the tag names of the slides. |
| slideNextDidChange | number | Emitted when the next slide has started. Emit the index of the new active slide. |
| slidePrevDidChange | number | Emitted when the previous slide has ended. Emit the index of the new active slide. |
| slideToChange | number | Emitted when a specific slide has been selected. Emit the index of the new selected slide. |
| slideDrag | number | Emitted when the slider is actively being moved. Emit the transformX value of the deck. |
| slideWillChange | number | Emitted before the active slide has changed. Emit the transformX value of the deck. |

[DeckDeckGo]: https://deckdeckgo.com
