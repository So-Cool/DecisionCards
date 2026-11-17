# Decision Cards

<!-- [![arXiv][arxiv-shield]][arxiv] -->
[![Website][website-shield]][website]

An interactive companion to the
> Decision Cards:
> An Analytical Tool for Mapping Decision Problems and Designing AI Support Systems

research paper by Michaela Benk and Kacper Sokol.

Decision Cards help researchers, designers and decision-makers map a decision problem across three levels
* how the problem is **framed**,
* which **strategy** is used to decide and
* the final **choice**

and record what role AI plays and how its support is evaluated.
The [**live demo**][website] available at <https://so-cool.github.io/DecisionCards/> lets you fill in a card in the browser and save it as a PDF or export it for later as JSON.

## Features

- Fill in all parts of a Decision Card:
  context, frame (level 3), strategy (level 2), choice (level 1), role of AI and evaluation, with a live preview.
- Load the worked examples from the paper:
  the hiking vignette, *Lee and Moray*'s orange juice pasteurisation study and *Salimzadeh et al.*'s route selection study.
- Add any of the eight second-order strategies described by *Sunstein and Ullmann-Margalit*, add custom rows and mark rows with ✓ or ✗.
- Switch to decision-maker mode, which hides the role of AI and evaluation so the card can serve as a reusable guide for recurring decisions.
- Save the card as a PDF with your browser's print dialogue.
- Keep a draft in your browser, export and import cards as JSON or copy a share link that contains the whole card.

## Privacy

Everything runs in your browser.
The page has no backend and sends nothing anywhere.
Drafts are stored in your browser's local storage and share links carry the card's contents in the URL itself, so anyone with the link can read the card.

## Saving a card as a PDF

Click **Save as PDF**, choose **Save as PDF** as the destination in the print dialogue and turn off headers and footers for a clean page.
The page is formatted for A4.

## The web application

The file structure is as follows:
```text
index.html               One-file app (HTML, CSS and JavaScript)
examples/
  examples.json          List of examples for the "Load an example" menu
  hiking.json
  orange-juice.json
  route-selection.json
```

To add a new example:
1. Fill in a card on the page and click **Export JSON**.
2. Save the file in `examples/`.
3. Add an entry to `examples/examples.json`.

To run locally:
```sh
python3 -m http.server
open http://localhost:8000
```

## Citation

Please cite the following paper when referring to Decision Cards:
```bibtex
@article{benk2026decision,
  title={Decision {Cards}: {An} analytical tool for mapping
         decision problems and designing {AI} support systems},
  author={Benk, Michaela and Sokol, Kacper},
  year={2026},
}
```
<!--
  journal={arXiv Preprint},
  pages={1--43},
  eprint={XXXX.XXXXX},
  archivePrefix={arXiv},
  doi={10.48550/arXiv.XXXX.XXXXX}

[arxiv]: https://arxiv.org/abs/XXXX.XXXXX
[arxiv-shield]: https://img.shields.io/badge/arXiv-XXXX.XXXXX-b31b1b.svg
-->
[website-shield]: https://img.shields.io/badge/website-Decision%20Cards-3a4fa0.svg
[website]: https://so-cool.github.io/DecisionCards/
