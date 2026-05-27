# Decipher Dashboard Generator

## Overview

The **Decipher Dashboard Generator** is a lightweight, browser-based utility designed to instantly convert Decipher survey XML into a clean, interactive HTML dashboard.

Survey programmers and data analysts often spend hours manually converting XML structures into readable data tables for client reporting. This tool automates that pipeline. By simply pasting Decipher `<radio>` or `<checkbox>` XML nodes into the interface, the generator securely parses the data, sanitizes formatting quirks, and outputs a production-ready, single-file HTML dashboard with built-in percentage calculations and toggleable sections.

### Key Features

* **Dual Question Support:** Automatically detects and formats both standard 1D questions (vertical lists) and 2D grid matrix questions (horizontal scales).
* **Advanced XML Sanitizer:** Acts as a shield against common survey platform quirks. It actively neutralizes smart quotes, invisible zero-width characters, em-dashes, and strict XML namespace errors (like `ss:questionClassNames`) before parsing, preventing fatal browser crashes and UTF-8 rendering issues.
* **Zero Dependencies:** The output is 100% vanilla HTML, CSS, and JavaScript. There are no external libraries, APIs, or database connections required, making the generated dashboards highly portable and secure.
* **Pre-configured Data Filters:** Automatically prepends required reporting filters (e.g., `filter id=db-9 default=1 "status.qualified"`) to the top of the generated code to ensure only clean, qualified respondent data is displayed.
* **Interactive UI:** The generated dashboards feature a modern, minimalist aesthetic with clickable headers to expand/collapse specific data tables, keeping large reports manageable.
* **One-Click Export:** Includes a native Clipboard API integration for instantly copying the fully compiled dashboard code.

### How it Works

1. **Input:** Paste your raw Decipher XML directly into the left-hand text area.
2. **Sanitize & Parse:** The tool cleans the XML of legacy formatting and extracts the question IDs, titles, rows, and columns.
3. **Generate:** It maps the extracted data into pre-defined, styled HTML tables.
4. **Deploy:** Click **Copy Code** and paste the resulting string into your Decipher dashboard environment or a standalone `.html` file.
