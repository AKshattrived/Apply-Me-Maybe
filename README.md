# Apply-Me-Maybe

An AI-powered resume tailoring platform, planned to help candidates turn their existing experience into clear, role-relevant resumes.

## Status

This repository contains the initial project scaffold only. All features and architecture described below are plans; no application code, dependencies, or tooling have been selected or implemented.

## Vision

Make it easier to adapt a resume to a specific opportunity while preserving factual accuracy and a consistent, professional layout. Tailoring should emphasize relevant experience without inventing qualifications or accomplishments, and users should be able to review the result before exporting it.

## Planned core features

- A frontend for providing a job description and source resume content.
- AI-assisted resume tailoring through the OpenAI API using a Codex-based workflow, with the integration approach to be defined.
- PDF generation from LaTeX templates.
- A dedicated formatting skill to enforce layout constraints, margins, typography, and styling rules.
- A mathematical utility to measure unused page space and guide content density adjustments while preserving readability.
- User review of tailored content and download of the final PDF.

## Proposed workflow

1. The user provides their source resume content and a target job description through the frontend.
2. The backend coordinates analysis of the role and tailoring of the supplied experience through the planned OpenAI API workflow.
3. Tailored content is placed into a LaTeX template under the formatting skill's constraints.
4. The document is compiled to PDF, and the page-space utility measures unused space within the usable page area.
5. Content and layout are refined within the formatting constraints, with a bounded refinement process to be designed.
6. The user reviews the tailored resume and exports the PDF.

## Planned architecture

The initial directories define responsibilities without selecting languages, frameworks, storage, deployment infrastructure, or build tools.

| Path | Planned responsibility |
| --- | --- |
| `frontend/` | Job description and resume input, review, and PDF download experience. |
| `backend/` | Request orchestration, OpenAI API integration, and document generation coordination. |
| `skills/resume-formatting/` | Formatting instructions and layout validation rules. |
| `templates/latex/` | Resume templates and shared LaTeX styling. |
| `utilities/page-space/` | Measurement of usable page area, occupied content, and unused space. |

Each directory currently contains only a placeholder. API contracts, the Codex integration, LaTeX compilation environment, measurement method, testing strategy, and handling of personal data remain design decisions. Implementation and setup instructions will be added once tooling is selected.
