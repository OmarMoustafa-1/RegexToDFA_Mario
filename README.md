
## RegexToDFA\_Mario

A graphical tool to convert regular expressions (regex) into deterministic finite automata (DFA), with interactive visualization and string testing. Built using Python and PySide6, it aims to simplify understanding of automata theory by providing an intuitive interface and graphical output.

---

### Features

* **Regex Input**: Supports operators `*`, `+`, `?`, `|`, `.`, `ε`, `()`, `[]`, `-`.
* **Virtual Keyboard**: Clickable buttons to insert regex symbols.
* **Direct Regex to DFA Conversion**: Generates DFA directly without intermediate NFA steps.
* **DFA Visualization**: Uses Graphviz to render the DFA as an image.
* **DFA Details Display**: Lists states, alphabet, start state, final states, and transitions.
* **Test Input Strings**: Input a string to check acceptance/rejection by the DFA.
* **Test History**: Keeps record of tested strings and their results.
* **Theme Switching**: Toggle between light and dark Mario-inspired themes.
* **Sound Feedback**: Plays sounds for success, failure, and errors.
* **Fullscreen Interface**: Optimized for fullscreen educational presentations.

---

### Getting Started

#### Prerequisites

* Python 3.10+
* Graphviz installed and added to system PATH.

#### Installation

```bash
# Clone the repository
git clone https://github.com/OmarMoustafa-1/RegexToDFA_Mario.git
cd RegexToDFA_Mario

# Install required Python packages
pip install -r requirements.txt
```

#### Running the Application

```bash
python AppWithIntro.py
```

> ⚠️ Make sure the following directories are present with their assets:
>
> * `assets/` (background images, DFA image placeholder)
> * `sounds/` (sound effect files)
> * `intro/` (intro video `mario_intro.mp4`)

---

### Example Usage

```
Enter regex: a(b|c)*d

Generated DFA displayed.
DFA Details:
States: ['S0', 'S1', 'S2', 'TRAP']
Alphabet: ['a', 'b', 'c', 'd']
Start State: S0
Final States: ['S2']
Transitions:
  S0 --a--> S1
  S1 --b--> S1
  S1 --c--> S1
  S1 --d--> S2

Test string: abcd → Accepted
Test string: abc → Rejected
```

---

### Code Structure

* `AppWithIntro.py`: Handles intro video and transitions into main app.
* `main.py`: Main application UI, theme switching, input handling.
* `dfa_generator.py`: Converts regex to DFA logic.
* `dfa_visualizer.py`: Renders DFA image using Graphviz.
* `theme_styles.py`: Defines light/dark theme stylesheets.
* `utils.py`: Regex validation, preprocessing helpers.
* `assets/`: Background images, DFA placeholder image.
* `sounds/`: Sound files for interaction feedback.
* `intro/`: Intro video shown at startup.


---

### License

MIT License © Omar Moustafa


