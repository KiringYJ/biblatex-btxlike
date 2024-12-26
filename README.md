# BibLaTeX-btxlike

This repository contains the custom `biblatex-btxlike.sty` package, designed to emulate the output style of BibTeX while retaining the advanced features of BibLaTeX. Below, we highlight key changes made by `biblatex-btxlike` and provide a side-by-side comparison of outputs to demonstrate its effects.

---

## How to Use

### Overleaf Users

Since `biblatex-btxlike.sty` is not yet on CTAN, Overleaf users can include it in their project by:

1. Clicking on **Add Files > From external URL** in Overleaf.
2. Entering the URL to the raw `biblatex-btxlike.sty` file in this repository.
3. Clicking **Add** to include the file in your project.

After adding the file, include it in your LaTeX document with:

```latex
\usepackage{biblatex-btxlike}
```

### Local Users

Download the `biblatex-btxlike.sty` file and place it in the same directory as your `.tex` file. Then include it in your LaTeX document with:

```latex
\usepackage{biblatex-btxlike}
```

---

## Why Choose BibLaTeX Over BibTeX?

While BibTeX has been a standard for bibliographies for decades, BibLaTeX offers modern features that are essential for contemporary academic writing. Here are the key functions that BibLaTeX provides, which are leveraged in `biblatex-btxlike`:

1. **Handling of URLs and DOIs**

   - **BibTeX**: URLs are typically added in the `note` field if needed, and there is no direct DOI handling.
   - **BibLaTeX**: Displays DOI links prominently, along with URLs.

2. **Differentiation Between Volume and Number in Series**

   - **BibTeX**: Often conflates the `volume` field for books in series, which is incorrect for numbered series.
   - **BibLaTeX**: Supports the `number` field to properly identify a book’s position in a series.

3. **Support for Abbreviated Author Initials**

   - BibLaTeX allows automatic abbreviation of author first names to initials, a feature not natively available in BibTeX.

4. **Integration of ArXiv and Preprint References**

   - BibLaTeX includes native support for the `eprint` field to cite ArXiv and other preprints, formatted consistently with academic standards.

5. **Shorthand Field**

   - BibLaTeX supports a `shorthand` field, enabling shorter custom labels for frequently cited works (e.g., "Stacks" for the Stacks Project).

6. **Subtitles Handling**

   - **BibTeX**: Many users include subtitles in the `note` field as BibTeX does not natively support them.
   - **BibLaTeX**: Separates subtitles from main titles by default but allows customization to seamlessly integrate them with the main title.

---

## Key Modifications in `biblatex-btxlike`

1. **URL and DOI Handling**

   - **BibLaTeX**: Displays DOI links prominently, along with URLs.
   - **btxlike**: Displays the URL only when the DOI is missing. This ensures that:
     - For online publications or ebooks, URLs are shown as "Available at ".
     - For published books with a DOI, no URL is displayed, aligning with typical citation norms.

2. **Removed "In:" Prefix for Journal Articles**

   - **BibLaTeX**: Includes the prefix `In:` before journal titles.
   - **btxlike**: Removes this prefix to align with BibTeX output.

3. **Subtitles Handling**

   - **BibLaTeX**: Subtitles are displayed after the main title, separated by a period.
   - **btxlike**: Integrates subtitles seamlessly with the main title, separated by a colon.

4. **Edition Formatting**

   - **BibLaTex** : Displays edition as "Second".
   - **btxlike**: Uses "Second edition" for clarity and consistency with BibTeX.

5. **Page Number Formatting**

   - **BibLaTeX**: Displays pages with "pp.".
   - **btxlike**: Displays pages without "pp.", aligning with BibTeX's simpler format.

---

## Comparison of Outputs

Below is a side-by-side comparison of bibliographic entries rendered with **BibTeX**, **BibLaTeX (with options)**, and **btxlike**.

> **Note:** The "BibLaTeX (with options)" examples use some pre-configured options, but no additional coding or macro customizations were applied.

### Journal Article

#### BibTeX

- [Rei03] Markus Reineke. The Harder-Narasimhan system in quantum groups and cohomology of quiver moduli. *Invent. Math.*, 152(2):349–368, 2003.

#### BibLaTeX (with options)

- [Rei03] M. Reineke. "The Harder-Narasimhan system in quantum groups and cohomology of quiver moduli". In: *Invent. Math.* 152.2 (2003), pp. 349–368.

#### btxlike

- [Rei03] M. Reineke. The Harder-Narasimhan system in quantum groups and cohomology of quiver moduli. *Invent. Math.*, 152(2):349–368, 2003.

---

### Book

#### BibTeX

- [WZ15] Richard L. Wheeden and Antoni Zygmund. *Measure and Integral*. Pure and Applied Mathematics (Boca Raton). CRC Press, Boca Raton, FL, second edition, 2015.

#### BibLaTeX (with options)

- [WZ15] R. L. Wheeden and A. Zygmund. *Measure and Integral. An Introduction to Real Analysis*. Second. Pure and Applied Mathematics (Boca Raton). CRC Press, Boca Raton, FL, 2015, pp. xvii+514.

#### btxlike

- [WZ15] R. L. Wheeden and A. Zygmund. *Measure and Integral: An Introduction to Real Analysis*. Second edition. Pure and Applied Mathematics (Boca Raton). CRC Press, Boca Raton, FL, 2015.

---

### Online Publication

#### BibTeX

- [Kna16] Anthony W. Knapp. *Basic Algebra*. Digital second edition, 2016.

#### BibLaTeX (with options)

- [Kna16] A. W. Knapp. *Basic Algebra*. Digital second. 2016.

#### btxlike

- [Kna16] A. W. Knapp. *Basic Algebra*. Digital second edition. 2016. Available at `https://www.math.stonybrook.edu/~aknapp/download/b2-alg-clickable.pdf`.

---

## Files in This Repository

- **`biblatex-btxlike.sty`**: The custom style file implementing the changes described above.
- **`sample-refs.bib`**: A sample bibliography file used for generating the comparisons.
- **Comparison examples**: The rendered outputs are included in this README for demonstration purposes.

## License

This project is open-source and distributed under the MIT License. Please refer to the `LICENSE` file in this repository for the full license text. We recommend sharing improvements via pull requests.
