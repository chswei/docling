# Docling PDF to Markdown Converter

This project uses the Docling library to convert PDF files to Markdown format, extracting text content and images.

## Official Documentation

For detailed information about the Docling library, please refer to the official documentation:
[https://github.com/docling-project/docling](https://github.com/docling-project/docling)

## Requirements

*   **`docling`**: The core Python library.
*   **`accelerate`**: Required.

### Installation

Install `docling` and `accelerate` using `uv` or `pip`:

**Using `uv`:**

```bash
uv add docling accelerate
```

**Using `pip`:**

```bash
pip install docling accelerate
```

## How to Use

The `docling_basic.py` script converts a single PDF file to Markdown.

1.  **Run the Script**: Execute the script from your terminal, providing the path to the PDF file you want to convert as a command-line argument:

    ```bash
    python docling_basic.py <path_to_your_pdf_file.pdf>
    ```
    Replace `<path_to_your_pdf_file.pdf>` with the actual path to your PDF file.

2.  **Output**:
    *   The script will create an `output` directory in the same folder where you run the script (if it doesn't already exist).
    *   Inside the `output` directory, it will save the converted Markdown file (e.g., `your_pdf_file.md`).
    *   It will also create a directory named `<your_pdf_file>_images` inside `output` to store any images extracted from the PDF. The Markdown file will contain relative links to these images.

Example:
```bash
python docling_basic.py documents/my_report.pdf
```

This command will process `documents/my_report.pdf` and create:
*   `output/my_report.md`
*   `output/my_report_images/` (containing extracted images)
