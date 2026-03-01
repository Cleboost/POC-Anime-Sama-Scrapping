# POC Anime-Sama Scrapping

This repository is a **Research and Proof of Concept (POC)** project focused on analyzing and scraping anime content from the French platform **Anime-Sama**.

The goal is to understand the site's architecture, its catalog structure, and how it integrates with various third-party video providers.

## 🚀 Purpose

- **Catalog Research**: Exploring how anime, seasons, and languages are indexed.
- **Scraping POC**: Implementing lightweight, dependency-free scripts (JavaScript/Python) to extract data.
- **Stream Analysis**: Investigating how video streams (from providers like Vidmoly, Sendvid, etc.) are embedded and can be extracted.

## 📂 Documentation

For detailed information on the site's architecture and the research findings, please refer to the documentation:

- **[Introduction to Anime-Sama and Video Providers](docs/00-intro.md)**

## 🛠️ Proof of Concept (POC)

You can find the experimental scripts in the `poc/` directory:

- `poc/search.js`: Search for animes on the platform.
- `poc/extract.js`: Extract seasons and scans from an anime page.
- `poc/languages.js`: Discover available languages for a specific season.
- `poc/episodes.js`: Parse episode lists and providers.
- `poc/vidmoly.js`: Extract direct stream links from Vidmoly.

## ⚠️ Disclaimer

This repository is for **educational and research purposes only**. The goal is to analyze the technical aspects of web scraping and stream embedding. Please respect the terms of service of the analyzed platforms.
