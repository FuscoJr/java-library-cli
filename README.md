# Java Library CLI

An early Java learning project for managing a small library through a terminal interface.

The application uses separate staff and customer menus to practise object-oriented programming, collections and basic lending logic. The interface is currently in German.

## Features

- Add books, music albums, films and video games.
- List available items and current loans.
- Borrow and return items.
- View a customer's borrowed items.
- Display inventory and customer counts.

Customers are identified by name and created when they first borrow an item. Each customer can borrow up to three items at a time.

## Requirements

- JDK 17 or newer, with `java` and `javac` available in your terminal.
- No external libraries.

The commands below were verified with JDK 21.

## Compile and run

From the repository root:

```sh
javac -encoding UTF-8 -d out src/*.java
java -cp out Main
```

The catalogue starts empty. Use the staff menu to add items before borrowing them.

The main menu offers:

- `1` — staff menu (`Mitarbeiter`).
- `2` — customer menu (`Kunde`).
- `0` — exit.

When adding an item, use one of these categories:

```text
BOOK
MUSIC_ALBUM
FILM
VIDEO_GAME
```

## Project structure

```text
src/
├── Main.java       # Terminal menus and user input
├── Library.java    # Catalogue, customers and lending operations
├── Item.java       # Item details and loan state
├── ItemType.java   # Supported item categories
└── User.java       # Customer details and borrowed item IDs
```

## Learning focus

- Classes, objects and encapsulation.
- Enums and ArrayList collections.
- Relationships between items, customers and loans.
- Menu-driven interaction and state changes.

## Current limitations

- Data is stored in memory. Items, customers and loans are lost when the application closes.
- The staff menu has no PIN check or authentication.
- Item removal appears in the menu but is not implemented.
- Non-numeric input at numeric prompts or an unknown item category can terminate the application.
- Some unsuccessful operations do not display feedback.

These improvements are tracked in [issue #1](https://github.com/FuscoJr/java-library-cli/issues/1).

## Licence

MIT. See [LICENSE](LICENSE).
