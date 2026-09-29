🔍 Vibecode Auditor

> 100% Local & Offline Security & Quality Audit Tool for Mobile Apps, Web Code, and Archives. 
> Developed by MIKATÉ PRODUCTION

🌟 Overview

Vibecode Auditor is a zero-dependency, single-file browser application designed to audit source code, binaries (`.apk`, `.aab`), and project archives against 160 "vibecoding" red flags and anti-patterns. 

It runs completely in your browser—no backend servers, no code uploads, and no data tracking. Your code never leaves your local machine unless you explicitly opt to use the optional AI Chat assistant.

✨ Key Features

 🛡️ 100% Client-Side Audit: All static analysis and archive extractions occur directly inside your browser using JavaScript and `JSZip`.
 📱 Native APK / AAB Decompression: Inspect Android manifests, asset files, and JavaScript bundles without installing external CLI tools.
 📋 160-Point Comprehensive Checklist:
   110 UI/UX & Design Points: Covers responsive design, layout bugs, navigation flaws, loading states, auth flows, permissions, i18n, and asset leaks.
50 Code & Backend Points: Evaluates API endpoints, database Row Level Security (RLS), CI/CD pipelines, supply chain security, vulnerable dependencies, and software architecture.
 📊 Automated Health Score: Computes a dynamic score starting from `100`, penalized by weighted severities (Critical, Warning, Info).
 🌐 **Bilingual Interface: Built-in support for English and French.
 🤖 **Optional AI Assistant: Connect your own API key for interactive refactoring and fix suggestions.

 🚀 Quick Start

Since Vibecode Auditor is packaged as a standalone HTML web application, setup takes seconds:

 Option 1: Direct Usage
1. Download or clone this repository:
   ```bash
   git clone [https://github.com/mikateproduction-wq/Vibecode-auditor-.git](https://github.com/mikateproduction-wq/Vibecode-auditor-.git)
   Open vibecode-auditor.html in any modern web browser (Chrome, Firefox, Edge, Safari).
2. Open vibecode-auditor.html in any modern web browser (Chrome, Firefox, Edge, Safari).
3. Start auditing!

Category,Supported Extensions
Mobile Binaries & Bundles,".apk, .aab"
Project Archives,.zip
Web & Frontend,".html, .css, .js, .jsx, .ts"
Mobile & Backend Code,".java, .kt, .swift, .py, .cpp, .c, .h, .hpp"
Configs & Manifests,".json, .xml"

📊 How the Audit Score WorksThe scoring algorithm evaluates your uploaded files against the 160-point rule matrix:$$\text{Final Score} = \max\left(0,\, 100 - \sum \text{Red Flag Penalties}\right)$$🔴 Critical Severity: High security risks, broken database RLS, hardcoded credentials, severe crashes.🟡 Warning Severity: UI inconsistencies, missing error boundaries, suboptimal asset loading, missing validation.🔵 Info / Best Practices: Missing documentation, non-standard naming conventions, minor accessibility gaps.

🔒 Privacy & Security First
Zero Network Footprint: Files uploaded to the dropzone stay strictly in browser memory.

Air-Gapped Ready: You can save the HTML file locally and run it entirely without an internet connection.

API Key Safety: If you use the optional AI chat tab, your API key is stored strictly in localStorage on your machine.

🧰 Tech Stack
Frontend Framework: Bootstrap 5.3

Archive Parsing: JSZip 3.10

Icons & UI: Custom Inline SVG Library

Execution: Vanilla ES6+ JavaScript (Web Workers / File API)
