# Chemistry Foundations Quiz - Week 2

A single-page, browser-based chemistry quiz application for practicing introductory chemistry concepts related to atomic structure, ions, isotopes, periodicity, and nuclear symbol notation.

This app was designed specifically for Midlands Technical College Chemistry 110 (CHM-110) taught by Professor Gordon.

The quiz generates randomized questions and answer choices rather than relying on a fixed question bank. It gives immediate feedback, detailed step-by-step explanations, and keeps a running score so students can practice the same concepts repeatedly with different values and elements.

<img width="335" alt="image" src="https://github.com/user-attachments/assets/88d76a01-c2ca-4cf6-a1a5-45a2ffaf98a2" />

Live link to app: https://realityexpander.github.io/Chemistry_Foundations_Quiz_CHM-110/

## Main Purpose

The purpose of this project is to provide an interactive study tool for foundational chemistry topics commonly introduced in high school and college-level introductory chemistry courses.

Instead of presenting the same static questions every time, the app creates new combinations of elements, atomic numbers, mass numbers, ion charges, electron counts, and answer choices. This makes it useful for repeated practice and concept reinforcement rather than simple memorization of a fixed answer set.

The app is designed to help students practice both:

- recognizing important chemistry definitions and periodic-table relationships; and
- performing basic calculations involving protons, neutrons, electrons, ions, isotopes, and atomic notation.

## Features

- Randomly generated chemistry questions and values
- Multiple-choice answer choices with randomized ordering
- Mixed quiz mode containing all supported question types
- Individual practice mode for selecting a specific question type
- Immediate correct/incorrect feedback
- Detailed explanations after answering
- A matching visual study diagram appears only after an answer is submitted
- 16 study diagrams stored locally in the repository under `images/`
- Running score for:
  - correct answers
  - incorrect answers
  - total answered
  - percentage correct
- Score persistence using browser `localStorage`
- MathJax rendering for chemical ions, isotopes, nuclear notation, superscripts, subscripts, and equations
- Responsive single-page interface
- No server-side code or database required
- Static front-end application: `index.html` plus the local `images/` asset folder

## Chemistry Concepts Covered

The quiz currently includes the following major concepts.

### 1. Valence Electrons and the Octet Rule

Students determine how many electrons an element will normally gain or lose to reach a stable outer-shell configuration.

Example concept:

- Nitrogen has 5 valence electrons.
- A full octet requires 8.
- Nitrogen therefore tends to gain 3 electrons.

### 2. Determining an Element from Electron Count and Ion Charge

Students use the number of electrons and an ion's charge to determine its number of protons and therefore identify the element.

For a positive ion:

```text
protons = electrons + positive charge
```

For a negative ion:

```text
protons = electrons - magnitude of negative charge
```

### 3. Atomic Structure Terminology

Matching questions cover definitions such as:

- atomic number
- mass number
- isotope
- atomic mass
- cation
- number of protons

### 4. Comparing Isotopes

Students identify which properties remain the same and which change between isotopes of the same element.

Isotopes of the same element have:

- the same number of protons;
- the same atomic number; and
- different numbers of neutrons.

For neutral isotopes, the number of electrons is also the same.

### 5. Nuclear / Isotope Symbol Notation

The quiz generates questions involving notation such as:

\[
{}^{52}_{23}\mathrm{V}
\]

Students identify:

- element symbol
- atomic number
- mass number
- proton count
- neutron count

The fundamental relationship used is:

```text
mass number = protons + neutrons
```

### 6. Electron Counts of Stable Main-Group Ions

Students determine the electron count of common ions based on periodic-table group behavior.

Examples include concepts such as:

- Group 1 elements commonly forming `1+` ions
- Group 2 elements commonly forming `2+` ions
- Group 16 elements commonly forming `2-` ions
- Group 17 elements commonly forming `1-` ions

### 7. Protons, Neutrons, and Electrons in Ions

Questions use complete nuclear/ion notation such as:

\[
{}^{97}_{42}\mathrm{Mo}^{2+}
\]

Students calculate:

```text
protons = atomic number
neutrons = mass number - atomic number
electrons = protons - positive charge
```

For negative ions, electrons are added instead.

### 8. Isotope Concepts

Students practice the key principle that isotopes of the same element differ in their number of **neutrons**, not protons.

### 9. Periodicity and Chemical Similarity

Questions test the relationship between periodic-table groups and chemical behavior.

Elements in the same group generally have similar chemical properties because they have similar valence-electron configurations.

For example, oxygen and sulfur are both members of Group 16.

### 10. Periodic Table Classification

The quiz covers classifications including:

- representative/main-group elements: Groups 1-2 and 13-18
- transition metals: Groups 3-12

### 11. Cations

Students identify a cation as an atom or species that has **lost electrons** and therefore has a **positive charge**.

### 12. Atomic Number

Students identify the atomic number as the number of protons in the nucleus of an atom.

### 13. Anions

Students identify an anion as an atom or species that has **gained electrons** and therefore has a **negative charge**.

### 14. Group 2 and +2 Ions

Students recognize that Group 2 (alkaline earth) elements commonly lose two valence electrons and form `2+` ions.

### 15. Counting Neutrons from an Isotope Name

Students determine neutron count using:

```text
neutrons = mass number - atomic number
```

### 16. Chalcogens and Isotope Identification

Students identify Group 16 (chalcogen) isotopes from proton and neutron information using:

```text
mass number = protons + neutrons
```

## Question Modes

The question selector provides two ways to use the quiz.

### Mixed Mode

`Mixed — all question types`

Questions are randomly selected from all available generators. This is useful for general review and test preparation.

### Individual Question-Type Practice

A specific question type can be selected from the drop-down menu. This is useful when concentrating on one concept, such as isotope notation or ion electron counts.

The two isotope-related formats originally identified as Question Type 4 are represented separately in the application as:

- **Type 4A — Compare isotopes**
- **Type 4B — Nuclear symbol notation**

## Libraries Used

### MathJax 4

[MathJax](https://www.mathjax.org/) is used to render mathematical and chemical notation written with LaTeX syntax.

The application loads MathJax from the jsDelivr CDN:

```html
<script defer src="https://cdn.jsdelivr.net/npm/mathjax@4/tex-mml-chtml.js"></script>
```

MathJax is used for notation such as ions and isotope symbols, for example:

```latex
\(\mathrm{Sr}^{2+}\)
```

and:

```latex
\({}^{97}_{42}\mathrm{Mo}^{2+}\)
```

Because MathJax is loaded from a CDN, an internet connection is normally required when the page is first opened unless MathJax is modified to be hosted locally.

## Technologies Used

The project intentionally has very few dependencies.

- HTML5
- CSS3
- Vanilla JavaScript
- MathJax 4
- Browser `localStorage`

No framework, build system, package manager, web server, or database is required.

## Installation

### Option 1: Download and Open Directly

The simplest installation method is to download the repository and open the HTML file in a modern web browser.

1. Clone or download this repository.
2. Locate `index.html`.
3. Double-click the file or open it with a browser such as Chrome, Firefox, Edge, or Safari.

For example:

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
cd YOUR-REPOSITORY
open index.html
```

On macOS, the `open` command launches the file in the default browser.

On Windows, the file can simply be opened from File Explorer.

On Linux, a command such as the following can be used:

```bash
xdg-open index.html
```

## Option 2: Run with a Local Web Server

Although the app does not require a server, using a small local server can be convenient during development.

If Python 3 is installed, run:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000/chemistry_quiz.html
```

This method is especially useful while modifying the application and testing changes.

## Option 3: Host with GitHub Pages

Because the project is a static HTML application, it can be hosted directly with GitHub Pages.

1. Push the project to a GitHub repository.
2. Open the repository's **Settings**.
3. Select **Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the branch containing the HTML file, normally `main`.
6. Select the root `/` directory and save.

If you want the quiz to load automatically from the root GitHub Pages URL, rename:

```text
chemistry_quiz.html
```

to:

```text
index.html
```

The application can then be served as a completely static GitHub Pages site.

## Score Tracking

The quiz maintains a running record of:

```text
Correct
Incorrect
Answered
Percent Correct
```

Score information is saved using browser `localStorage` when available. This means the current score can survive a page refresh or browser restart on the same browser/device.

No score information is transmitted to a server.

The score can also be reset from within the application.

## Random Question Generation

The application uses JavaScript question-generator functions rather than a single static list of questions.

Depending on the question type, the generator can randomize values such as:

- element
- atomic number
- mass number
- neutron count
- electron count
- ion charge
- isotope pair
- periodic-table group relationships
- correct and incorrect answer choices
- answer-choice order

This allows the same chemistry rule to be practiced repeatedly with different examples.

## Project Structure

The quiz is a static front-end site. The HTML/CSS/JavaScript remain in `index.html`, while the 16 visual study diagrams are stored as repository assets in `images/`:

```text
Chemistry_Foundations_Quiz_CHM-110/
├── index.html
├── README.md
└── images/
    ├── type01-stable-ion.png
    ├── type02-identify-element.png
    ├── type03-chemistry-terms.png
    ├── type04-isotopes-nuclear-symbols.png
    ├── type05-stable-cation-electrons.png
    ├── type06-ion-pne-notation.png
    ├── type07-stable-anion-electrons.png
    ├── type08-isotopes-neutrons.png
    ├── type09-periodicity.png
    ├── type10-periodic-table-groups.png
    ├── type11-cation.png
    ├── type12-atomic-number.png
    ├── type13-anion.png
    ├── type14-group2-ions.png
    ├── type15-counting-neutrons.png
    └── type16-chalcogen-isotope.png
```

The image paths in `index.html` are relative paths such as `images/type01-stable-ion.png`. This makes the same files work when opened locally or deployed through GitHub Pages. The diagrams are inserted into the page only after the student submits an answer, so they act as visual explanations rather than revealing the answer in advance.

## Browser Requirements

A modern browser with JavaScript enabled is required.

Recommended browsers include current versions of:

- Google Chrome
- Mozilla Firefox
- Microsoft Edge
- Apple Safari

Internet access is required for the default MathJax CDN configuration.

## Educational Use

This application is intended as a practice and study aid for introductory chemistry. The generated explanations are designed to reinforce the reasoning behind each answer rather than simply identify whether an answer is correct.

It is particularly useful for practicing relationships among:

```text
atomic number -> protons
mass number -> protons + neutrons
ion charge -> relationship between protons and electrons
periodic-table group -> common valence behavior
```

## Customization

Because the project uses plain HTML, CSS, and JavaScript, additional question generators can be added directly to the source without requiring a compilation or build step.

Possible future additions include:

- electron configurations
- Lewis dot structures
- periodic trends
- ionic compound formulas
- molecular naming
- significant figures
- dimensional analysis
- molar mass calculations
- balancing chemical equations

## License

No license is included by default. If this repository will be distributed publicly, add an appropriate open-source license such as the MIT License.
