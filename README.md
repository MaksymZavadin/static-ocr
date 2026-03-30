# Browser-Only OCR App

This is a static, browser-only OCR web app for scanned PDF and image files.

## What the app does

- Extracts text from scanned PDFs and images directly in the browser
- Supports multi-page PDF processing
- Shows merged output and page-by-page OCR results
- Displays page thumbnails and recognition confidence
- Allows image preprocessing before OCR (grayscale and contrast)
- Lets you select OCR languages and save your preferences in the browser

## How it works

- PDF rendering is done in the browser using PDF.js
- OCR is done in the browser using Tesseract.js (WebAssembly)
- No backend server is required for OCR processing
- No files are sent by default by this static package

## Supported inputs

- PDF: `.pdf`
- Images: `.png`, `.jpg`, `.jpeg`, `.webp`, `.tiff`

## Languages

Built-in language options include:

- `eng` (English)
- `deu` (German)
- `ukr` (Ukrainian)
- `fra` (French)
- `spa` (Spanish)

You can also add custom Tesseract language codes from the UI (for example `pol`).

## Use the app

1. Open the app URL in your browser.
2. Upload a PDF or image file.
3. Select one or more OCR languages.
4. Optionally enable preprocessing (grayscale/contrast).
5. Click Run OCR.
6. Review output, then copy text or download `.txt`.

## Deployment (static hosting)

Upload this folder content as static files to:

- SharePoint static site location
- GitHub Pages
- Any static web hosting

Required files in this package:

- `index.html`
- `assets/`
- `.nojekyll`

## Notes and limitations

- First run may be slower while OCR models initialize.
- Large PDFs can use significant memory and CPU in the browser.
- OCR quality depends on scan quality, language selection, and preprocessing.
- Browser support is best on modern Chrome/Edge/Safari/Firefox versions.
