# nardjay.spudgen.oi
# 🥔 SpudGen

> A single-file code & data generator. 60+ operations. Zero setup. Runs entirely in your browser.

Made by DS & Jay

🔗 Try it live: nardjay.github.io/spudgen.html

---

## What is SpudGen?

SpudGen is a tiny browser tool for generating code and data without typing it out by hand.

You give it text or numbers. You click an operation. It spits out exactly what you wanted — 1,000 lines of boilerplate, a numbered list, a JSON array, a range of dates, whatever. Copy it or download it as a file.

It's built for the boring stuff: repeating lines, converting case, generating sequences, wrapping text into code. Everything runs in the browser. Nothing is uploaded. Nothing is tracked. Just one HTML file and a lot of "why am I typing this manually."

It's part of the Spud family alongside SpudLang and SpudGPT.

---

## ✨ Features

- 60+ operations across 5 categories
- Single HTML file — no build step, no dependencies, no backend
- Live preview — output updates as you type
- Auto-save — your input and last-used settings persist in the browser
- Chain operations — swap output back into input with one click
- Copy to clipboard or download as a file
- Handles up to 200,000 lines without crashing the tab
- Same potato theme as the rest of the family

---

## 🚀 How to Use

1. Open the app in your browser
2. Paste or type text into the **input** box (only some ops use this)
3. Pick a category, then click an operation
4. Fill in any parameters that appear
5. Copy the output or download it

Some operations ignore the input entirely — the number and letter generators just make sequences from scratch.

---

## 📚 Operations

### Aa · Case

Everything you'd ever need for converting text case:

- UPPERCASE
- lowercase
- Title Case
- Sentence case
- camelCase
- PascalCase
- snake_case
- SCREAMING_SNAKE
- kebab-case
- dot.case
- reverse text
- fLIP cASE

### ✂ · Text

Surgical operations on text and lines:

- Add spaces between characters (h e l l o)
- Remove all spaces
- Dots → spaces / Spaces → dots
- Remove any character you specify
- Replace X with Y
- Split by delimiter / Join lines with delimiter
- Trim every line
- Remove empty lines
- Unique lines only
- Sort lines A→Z / Z→A / by length
- Reverse line order
- Number every line
- Shuffle lines 🎲

### 123 · Numbers

Generate number sequences:

- 1 → N
- Range with custom step
- Countdown
- Evens, Odds
- Multiples of N
- Powers of 2
- Squares
- Fibonacci
- Primes up to N
- Random numbers 🎲
- Zero-padded numbers (001, 002, ...)
- Roman numerals (I, II, III, ...)
- Binary (0, 1, 10, 11, ...)
- Hex (0x0, 0x1, ...)

### ABC · Letters

Character sequences:

- a → z
- A → Z
- aA bB cC ...
- Cycle letters
- a1 b2 c3 ...
- Custom characters (Greek alphabet by default)
- Keypad style (AA AB ... ZZ)

### 🧩 · Templates

Wrap, repeat, and structure your output:

- Repeat text N times
- Template with {i} placeholder (item_1, item_2, ...)
- Wrap each line with a template
- Add prefix / suffix to every line
- Indent every line
- Comma-separated output
- JSON array
- JS array
- HTML <li> items
- SQL placeholder rows
- SQL INSERT wrapper
- ASCII box

---

## 🔗 Chaining Operations

You don't have to use just one operation. Hit the **⇄ Output → Input** button to move the current output back into the input box, then run another operation on it.

Example chain:

1. Paste 100 product names
2. **snake_case** them
3. Swap output → input
4. **Wrap each line** with `"{x}",`
5. Swap again
6. **JSON array** them
7. Copy → paste into your code

That's a 5-second workflow instead of 10 minutes of manual editing.

---

## 🛠️ How It Works

Every operation is just a JavaScript function that takes your input (and optional parameters) and returns a string. There's no magic — no parser, no runtime, no backend.

- The input box is a `<textarea>`
- Each operation is a function `(input, params) => string`
- Clicking an operation runs it and prints the result
- Parameters are auto-generated from each operation's schema
- State is saved to `localStorage` on every keystroke

The whole app is one HTML file. Read it if you're curious — it's not that long.

---

## 📁 Project Structure

    spudgen/
      index.html    <- the whole app
      README.md     <- you're reading it

---

## 🌐 Hosting

SpudGen is a static HTML file, so it works on any free host:

- GitHub Pages
- Cloudflare Pages
- Netlify
- Vercel
- Or literally double-click the file on your desktop

No backend. No database. No monthly bill.

---

## 🚧 Roadmap

Things that would be nice to add:

- [ ] Pipelines — chain 3-4 operations visually without the swap dance
- [ ] Favorites — star the operations you use daily
- [ ] CSV mode — pick a column, transform just that
- [ ] Regex replace
- [ ] Save/load named recipes
- [ ] Share a chain via URL
- [ ] Dark/light theme toggle
- [ ] More potato jokes

---

## 🤝 Credits

Made with 🥔 by DS & Jay.

Built because typing the same thing 1,000 times is a waste of a perfectly good afternoon.

If you use it and it saves you five minutes, tell a friend. If you find a bug, tell us. If you love it, send a potato.

---

## 📜 License

MIT — do whatever you want with it. Just don't blame us if you accidentally generate 200,000 lines of `console.log("hi")`.
