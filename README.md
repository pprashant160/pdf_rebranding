# Guidely PDF Branding Studio (JavaScript-only)

Static Vercel website. PDF processing runs in the visitor's browser using PDF-Lib and JSZip; files are not uploaded to Vercel. Maximum 10 PDFs per batch.

## Deploy to Vercel (beginner-friendly)
1. Unzip `Guidely_PDF_Branding_Vercel.zip` on your laptop.
2. Create a GitHub repository, for example `guidely-pdf-branding`.
3. Upload `index.html` and the `public` folder to the repository root. Keep the folder structure unchanged.
4. In Vercel, select **Add New → Project**, import that GitHub repository, and deploy. No build command or Python runtime is required for this static site.
5. Open the deployed URL and test with copies of 1–2 PDFs first. Then use batches of up to 10.

## Important limitations
- The tool adds a first-page header and adds a diagonal Guidely logo watermark to pages 2 onward. It does not erase existing third-party watermarks. Removal varies by PDF (text/vector watermark vs flattened image) and should be implemented/tested separately per source layout to avoid damaging questions, diagrams, or tables.
- Header details entered in the form apply to all PDFs in one batch; use separate batches when exam name/date/shift differ.
- PDFs with password protection, unsupported encryption, unusual PDF structures, or very large page counts may fail in browser processing.
- PDF-Lib and JSZip are loaded from jsDelivr CDN, so the browser needs internet access.
- Use only documents you are authorized to modify and redistribute.
