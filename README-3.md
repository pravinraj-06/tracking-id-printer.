# Tracking ID Label Printer

A static, browser-based Excel-to-Zebra barcode label printer.

## Features
- Imports `.xlsx`, `.xls`, or `.csv` in the browser.
- Reads the `ShipmentId` column from the first worksheet.
- Removes duplicate IDs.
- Search, select one ID, or tick multiple IDs.
- Prints labels containing **only** the Tracking ID and its Code 128 barcode.
- Does not upload the Excel file to a server.

## Run locally
1. Extract the ZIP.
2. Open `index.html` in Chrome or Edge while connected to the internet.
3. Select your Excel file.
4. Select one or more IDs and print.

## Publish using GitHub Pages
1. Sign in to GitHub and create a new **Public** repository, for example `tracking-id-printer`.
2. Upload `index.html` and `README.md` to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch `main` and folder `/ (root)`, then Save.
6. Wait for GitHub to publish. The website URL will look like:
   `https://YOUR-GITHUB-USERNAME.github.io/tracking-id-printer/`

## Zebra printer setup
- The page currently uses a 100 mm × 50 mm label. Change the `@page` size and `.label` dimensions in `index.html` if your stock is different.
- In the print dialog choose the Zebra printer, set scale to 100% / Actual size, disable browser headers and footers, and choose the matching label stock.
- If the printer advances extra blank labels, calibrate the media size/sensor in the Zebra printer driver or printer settings.

## Important
This is a personal label-printing utility. It creates Code 128 barcodes from the IDs in your own spreadsheet. It is not connected to Ekart or any courier's official tracking system, and it does not create or validate official carrier labels.
