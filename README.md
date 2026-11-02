# Construction ERP: my first project

My first full-stack business application, built for a construction company's procurement and accounts team. It later grew into the company's full ERP (project management, billing, procurement, HR and a native Android app), which is private and company-owned.

> This repository has no company code, data, documents or screenshots. It describes what I built and what I learned.

## The problem

Purchase orders, work orders and supplier invoices were tracked in separate Excel sheets. Bills got lost, nobody could see which invoices were pending approval, and POs were typed by hand into a template.

## What I built

A local office server that every PC on the office network could open in a browser:

- **PO bill and WO invoice tracker:** one place to record purchase orders, work-order invoices and their status.
- **PO document generation:** purchase-order PDFs produced from the data in the system, in the company's format.
- **Email notifications** for pending items.
- **File uploads** for scanned bills, stored against the right record.
- **Automatic daily backups** of the database.
- **One-click Windows setup** (install and start scripts) so IT staff without a developer background could run it.

## Tech

| Area | Choice |
|---|---|
| Server | Node.js, Express |
| Database | SQLite (sql.js) |
| PDFs | PDFKit, Python |
| Email | Nodemailer |
| Front end | HTML, CSS, JavaScript |
| Deployment | Windows PC on the office network, batch-file start scripts |

## What I learned

- Turning a manual spreadsheet process into a database-backed workflow.
- Designing for non-technical users: clear status, one-click start, simple backups.
- Why real data and secrets must never be committed to a public repository. This project taught me that, and the original repo is now private.

## What came next

The ERP now covers billing (RA bills, subcontractor bills), procurement, stores, HR and site attendance, with a React web app, a Node.js and PostgreSQL API, a native Android client and CI/CD. See my [profile](https://github.com/asal1989) for more projects.
