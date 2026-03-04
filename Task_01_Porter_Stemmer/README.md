# Task 01: Porter Stemmer Implementation

## Overview
This task involves a custom implementation of the **Porter Stemming Algorithm**, a foundational technique in Information Retrieval used for term normalization. The goal is to reduce words to their base or root form by removing common morphological and inflectional endings.

## Features implemented
* **Vowel & Consonant Identification:** Logic to handle English character patterns, including the special rules for the letter 'y'.
* **Measure ($m$) Calculation:** Determines the "weight" of a word stem based on vowel-consonant sequences.
* **Multi-Phase Stemming:**
    * **Phase 1:** Handles basic plurals and simple suffixes (e.g., `ies` → `i`, `sses` → `ss`).
    * **Phase 2:** Maps complex relational suffixes to simpler forms (e.g., `ational` → `ate`).
    * **Phase 3:** Implements weight-sensitive rules that only apply if the stem measure $m > 1$.

## Example Results
* `caresses` → `caress`
* `ponies` → `poni`
* `operational` → `operate`
* `replacement` → `replac`

## Author
**Yousef Shihade**
Information Retrieval Course | University of Haifa
