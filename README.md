# Shepherd Tampermonkey Scripts

Originally by Bryan Robinson.

This repository contains browser userscripts for improving day-to-day workflows in Shepherd.

## Included Scripts

### In-House Lab Manager

- File: `labResults.txt`
- Purpose: Adds a polished lab workflow modal and helper controls inside Shepherd.
- Highlights:
	- Scoped styles to avoid interfering with the host app
	- Cleaner action buttons and selection UI
	- Focused, in-page workflow for lab result handling

### Bulletproof Radiograph Upload

- File: `radiologyUpload.txt`
- Purpose: Adds a one-click radiograph upload helper that batches images for the active patient.
- Highlights:
	- Attempts to detect patient ID from the page
	- Requests matching image files from a local bridge service
	- Injects files into the Imaging upload area automatically

## Quick Start

1. Install the Tampermonkey browser extension.
2. Open Tampermonkey and create a new script.
3. Copy and paste script contents from either file in this repo.
4. Save and enable the script.
5. Open Shepherd and verify the new button/UI appears.

## Local Bridge Requirement (Radiograph Upload)

The radiograph uploader calls a local endpoint:

- `http://localhost:5000/get-latest-image?patient_id=...`

Make sure your local service is running and reachable at port 5000 before using the upload button.

## Notes

- Scripts target Shepherd domains.
- Keep script versions in sync with your Tampermonkey installs.
- Test in a non-production workflow before broad rollout.

