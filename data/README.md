# Dataset - Phishing URL Detection
This directory contains the dataset used for the project on **detecting phishing URLs using machine learning techniques**.

The dataset consists of multiple records, where each row represents a URL along with a set of **features extracted from the URL, domain, and webpage content**.
---
## Dataset Structure
Each row corresponds to an example (URL) with the following columns:


| # | Feature |
|---|--------|
| 1 | FILENAME |
| 2 | URL |
| 3 | URLLength |
| 4 | Domain |
| 5 | DomainLength |
| 6 | IsDomainIP |
| 7 | TLD |
| 8 | URLSimilarityIndex |
| 9 | CharContinuationRate |
| 10 | TLDLegitimateProb |
| 11 | URLCharProb |
| 12 | TLDLength |
| 13 | NoOfSubDomain |
| 14 | HasObfuscation |
| 15 | NoOfObfuscatedChar |
| 16 | ObfuscationRatio |
| 17 | NoOfLettersInURL |
| 18 | LetterRatioInURL |
| 19 | NoOfDegitsInURL |
| 20 | DegitRatioInURL |
| 21 | NoOfEqualsInURL |
| 22 | NoOfQMarkInURL |
| 23 | NoOfAmpersandInURL |
| 24 | NoOfOtherSpecialCharsInURL |
| 25 | SpacialCharRatioInURL |
| 26 | IsHTTPS |
| 27 | LineOfCode |
| 28 | LargestLineLength |
| 29 | HasTitle |
| 30 | Title |
| 31 | DomainTitleMatchScore |
| 32 | URLTitleMatchScore |
| 33 | HasFavicon |
| 34 | Robots |
| 35 | IsResponsive |
| 36 | NoOfURLRedirect |
| 37 | NoOfSelfRedirect |
| 38 | HasDescription |
| 39 | NoOfPopup |
| 40 | NoOfiFrame |
| 41 | HasExternalFormSubmit |
| 42 | HasSocialNet |
| 43 | HasSubmitButton |
| 44 | HasHiddenFields |
| 45 | HasPasswordField |
| 46 | Bank |
| 47 | Pay |
| 48 | Crypto |
| 49 | HasCopyrightInfo |
| 50 | NoOfImage |
| 51 | NoOfCSS |
| 52 | NoOfJS |
| 53 | NoOfSelfRef |
| 54 | NoOfEmptyRef |
| 55 | NoOfExternalRef |
| 56 | label |
---

## Feature Description

### Basic URL Information

| Feature | Description |
|--------|------------|
| `FILENAME` | File name associated with the sample |
| `URL` | Full URL |
| `URLLength` | Total length of the URL |
| `Domain` | Domain of the URL |
| `DomainLength` | Domain lengtg |
| `IsDomainIP` | 1 if the domain is an IP address, 0 otherwise |
| `TLD` | Top-Level Domain (eg. `.com`, `.org`) |
| `TLDLength` | TLD length |
| `NoOfSubDomain` | Number of subdomains |

---

### Lexical Features (URL-based)

| Feature | Description |
|--------|------------|
| `URLSimilarityIndex` | Similarity to known legitimate URLs |
| `CharContinuationRate` | Character continuity in the URL |
| `URLCharProb` | PStatistical probability of URL characters |
| `NoOfLettersInURL` | Number of letters in the URL |
| `LetterRatioInURL` | Proportion of letters |
| `NoOfDegitsInURL` | Number of digits |
| `DegitRatioInURL` | Proportion of digits |
| `NoOfEqualsInURL` | Number of `=` |
| `NoOfQMarkInURL` | Number of `?` |
| `NoOfAmpersandInURL` | Number of `&` |
| `NoOfOtherSpecialCharsInURL` | Number of special characters |
| `SpacialCharRatioInURL` | Ratio of special characters |

---

### Obfuscation and Security

| Feature | Description |
|--------|------------|
| `HasObfuscation` | Indicates whether the URL is obfuscated |
| `NoOfObfuscatedChar` | Number of obfuscated characters |
| `ObfuscationRatio` | Obfuscation ratio |
| `IsHTTPS` | 1 if HTTPS is used |

---

### Domain Characteristics

| Feature | Description |
|--------|------------|
| `TLDLegitimateProb` | Probability of TLD legitimacy |

---

### Page Content (HTML/Structure)

| Feature | Description |
|--------|------------|
| `LineOfCode` | Number of lines of code |
| `LargestLineLength` | Length of the longest line |
| `HasTitle` | Whether the page has a title |
| `Title` | Title content |
| `DomainTitleMatchScore` | Similarity between domain and title |
| `URLTitleMatchScore` | Similarity between URL and title |
| `HasDescription` | Presence of meta description |

---

### Page Elements

| Feature | Description |
|--------|------------|
| `HasFavicon` | Presence of a favicon |
| `Robots` | Use of robots.txt |
| `IsResponsive` | Whether the site is responsive |
| `HasSocialNet` | Links to social media |
| `HasSubmitButton` | Presence of a submit button |
| `HasHiddenFields` | Hidden fields |
| `HasPasswordField` | Password field |
| `HasExternalFormSubmit` | Form that submits to an external domain |

---

### Behavior and Redirects

| Feature | Description |
|--------|------------|
| `NoOfURLRedirect` | Number of redirects |
| `NoOfSelfRedirect` | Internal redirects |
| `NoOfPopup` | Number of popups |
| `NoOfiFrame` | Number of iframes |

---

### Specific phishing indicators

| Feature | Description |
|--------|------------|
| `Bank` | Banking-related content |
| `Pay` | Payment-related |
| `Crypto` | Cryptocurrency-related |

---

### Page Resources

| Feature | Description |
|--------|------------|
| `NoOfImage` | Number of images |
| `NoOfCSS` | CSS files |
| `NoOfJS` | JavaScript files |
| `NoOfSelfRef` | Internal references |
| `NoOfEmptyRef` | Empty references |
| `NoOfExternalRef` | External references |

---

### Target Variable

| Feature | Description |
|--------|------------|
| `label` | 1 = phishing, 0 = legitimate |

---

## Using the Dataset

This dataset allows you to:

- Train classification models (ML/DL)
- Analyze patterns in phishing URLs
- Evaluate important features
- Build real-time detection systems

---

## Important Notes

- Some features are derived from HTML analysis → requires access to the webpage
- The data may be imbalanced → consider balancing techniques
- Avoid directly accessing phishing URLs without a secure environment

---

