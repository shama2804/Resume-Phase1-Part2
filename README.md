# 🧾 Job Description (JD) Builder — HR Portal

This is **Part 2 of Phase 1** of the Resume Ranking project.  
It allows HRs or recruiters to create structured, customizable Job Descriptions through a clean web interface.

✅ Generates 2 PDFs (internal + public)  
✅ Stores JD info in MongoDB  

---

## 📌 Features

- 🖊️ Fillable JD form with optional sections:
  - Reporting size, stipend/salary, number of openings, certifications
- 🔒 Internal-only fields:
  - Gender preference, preferred colleges, GitHub requirement, interview count
- 💾 Stores JD in MongoDB (`resume_ranking_db → jd_extractions`)
- 📄 Generates:
  - `JD_<id>_internal.pdf` → full JD with internal info
  - `JD_<id>_public.pdf` → public JD with **Apply Now** link
- 🧭 Simple preview page for saved JD

---

## 🗂️ Folder Structure
```
hr/
├── hr_app.py # Main Flask application
├── routes.py # All backend routes and DB logic
├── templates/ # HTML/Jinja templates
│ ├── jd_form.html # JD creation form
│ ├── jd_template_internal.html # Full internal JD layout
│ └── jd_template_public.html # Public JD layout with apply link
├── pdfs/ # Output folder for generated PDFs
```

## Installations required
pip install flask pymongo pdfkit
Install wkhtmltopdf
Required for PDF generation
Download and install from: https://wkhtmltopdf.org/downloads.html
After installing, add the path to your system’s environment variables.
