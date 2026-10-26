# Amazon Data Converter

Turn your Amazon data export (ZIP) into clear spending insights and an Excel file.
Runs 100% in your browser: no server, no tracking, no data ever leaves your device.

> **Status: early development.** Nothing is usable yet. This README describes what is being built and will be updated as the project progresses.

---

## Why

Amazon lets you request a copy of your personal data, but what you get is a ZIP with hundreds of raw CSV files. Amazon itself offers no real overview of your own spending: no totals across years, no monthly trends, no breakdown by category or time of day.

This tool reads that export and turns it into a readable overview.

## Planned features

- **Total spending** across your entire order history
- **Spending per month, quarter and year**
- **Spending by product category**, based on Amazon's department field plus keyword matching where it is missing
- **Shopping times**: by hour of day and day of week
- **Top items** and largest orders
- **Interactive charts** with a date-range filter
- **Excel export (.xlsx)** with the cleaned data and one sheet per analysis
- Correct handling of cancellations and refunds

## Privacy by design

Your Amazon export contains sensitive data such as addresses, payment details and order history. This project is built so that you do not have to trust it, because you can verify it yourself:

- **No backend.** The app is a static website. Your ZIP is opened and processed locally in your browser.
- **No external requests.** All libraries are bundled in this repository. Nothing is loaded from third-party servers, and there are no analytics, cookies or trackers.
- **Enforced by the browser.** A strict Content Security Policy blocks every outgoing network connection, so data cannot be sent anywhere, even by mistake.
- **Works offline.** Once the page is loaded, you can disconnect from the internet and it still works.
- **Fully readable source.** Every line of code that runs on the website is in this repository.

A step-by-step guide on how to verify this yourself will be added before the first release.

## Roadmap

- [ ] **1. Core:** project setup, read the ZIP in the browser, parse and clean order data
- [ ] **2. Insights:** analyses and charts
- [ ] **3. Excel export**
- [ ] **4. Verifiable privacy and release:** Content Security Policy, offline support, "verify it yourself" guide, hosting via GitHub Pages

## How to get your Amazon data

1. Go to Amazon's "Request Your Data" page (Account > Privacy / Data requests).
2. Request your data. Amazon will email you a download link, which can take a few days.
3. Download the ZIP file. Later, you will simply drop this file into the app.

## Tech

Plain HTML, CSS and JavaScript. No build step, no framework, no server.

## License

Source available under the [PolyForm Strict License 1.0.0](https://polyformproject.org/licenses/strict/1.0.0). You may read and verify the code and use it for noncommercial purposes. Modification and redistribution are not permitted.

This project is not affiliated with or endorsed by Amazon.
