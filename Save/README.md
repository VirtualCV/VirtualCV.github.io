# OurVirtualCV

A collection of static CVs and portfolio pages. The site is built with HTML and can be served from any static web host. If GitHub Pages is enabled for the repository, it publishes the site from the configured branch and folder.

## Pages

- [Home page](./index.html) - project landing page.
- [Ben Tran portfolio](./BenTran/) - interactive portfolio.
- [Ly Nguyen CV](./LyNguyen/) - printable CV.
- [Ben Tran CV](./BenTran.html)
- [Ben Binh Tran CV](./BenBinhTran.html)
- [Ly Nguyen CV](./LyNguyen.html)
- [CV editor](./CVbuilder/) - customize a sample CV, upload a photo, save a draft locally, and download HTML or print/save as PDF.

The root-level HTML files and profile folders are separate pages; update the intended page when changing profile content.

## Using the CV template

Open `CVbuilder/index.html`, click the CV text to edit it, and use **Choose photo** to add a profile picture. **Save draft** stores the current CV in that browser on that device; it is not uploaded. **Download HTML** exports a standalone HTML file with the current formatting and embedded photo. Use **Print / Save PDF** and choose **Save as PDF** in the browser's print dialog. Select A4 paper and enable background graphics for the sidebar colors. **Reset** restores the original template and removes the locally saved draft.

## Repository layout

```text
.
├── index.html
├── BenTran.html
├── LyNguyen.html
├── BenTran/
│   ├── index.html
│   ├── Certificates/
│   │   └── Automate in a Day certificate for Ben Tran.pdf
│   ├── Resumes/
│   │   └── BenBinhTran_CV_PE.html
│   └── images/
├── LyNguyen/
│   ├── index.html
│   └── images/
└── Save/
    └── index.html
```

## Viewing locally

Open `index.html` in a browser, or serve the repository directory with a local static web server. No build step or package installation is required.

## Privacy

Do not treat unlisted URLs or the absence of a public directory as access control. Pages and files published on a public static host may be accessed by anyone who knows or discovers their URLs. Do not publish sensitive personal information; use authenticated hosting if access must be restricted.
