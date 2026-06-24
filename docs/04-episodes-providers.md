# Chapter 4: Episode List & Providers Analysis

The heart of the streaming data on Anime-Sama is contained within a separate `episodes.js` file for each season or movie.

## Endpoint
- **URL**: `https://anime-sama.to/catalogue/{anime}/{season}/{language}/episodes.js`
- **Method**: `GET`

## Mechanism
The `episodes.js` file contains global variables for each available video player (provider):
- `var eps1 = [...]`: A list of episode URLs for the first provider (e.g., Smoothpre).
- `var eps2 = [...]`: A list of episode URLs for the second provider (e.g., Vidmoly).
- `var eps3 = [...]`: A list of episode URLs for the third provider (e.g., Sibnet).

## POC Implementation
The script `poc/episodes.js` implements this by:
1. Fetching the raw JS code from the `episodes.js` file.
2. Using a global Regex to match the `epsX` array definitions.
3. Extracting and cleaning the episode URLs.
4. Identifying the provider's name (e.g., `vidmoly.to`, `sendvid.com`) from the first link in the array.

### Special Handling: Vidmoly
For **Vidmoly**, the site's default `.to` links are sometimes blocked or broken. The script automatically replaces `.to` with `.biz` for these URLs to ensure compatibility.
