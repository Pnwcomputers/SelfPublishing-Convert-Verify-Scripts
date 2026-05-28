# Security Policy

Thank you for helping keep **SelfPublishing-Convert-Verify-Scripts** safe, reliable, and responsible.

This repository contains scripts and documentation for building print-ready PDF files and validating or repairing EPUB files for self-publishing workflows. Because these scripts process local book files, Markdown chapters, images, EPUB archives, XML/XHTML content, fonts, and publishing build artifacts, security and data-safety concerns are taken seriously.

Please do **not** report security vulnerabilities through public GitHub issues, discussions, or pull requests if the report includes sensitive details, private manuscripts, unpublished book content, credentials, personal files, exploitable code behavior, or other confidential information.

---

## Supported Versions

The current `main` branch is considered the actively maintained version of this repository.

| Version / Branch | Security Support |
| --- | --- |
| `main` / current repository content | Supported |
| Older commits | Not officially supported |
| Forks or modified copies | Not officially supported |
| Personal deployments based on modified scripts | Not officially supported |

If formal versioned releases are added later, this section will be updated to identify which versions are actively supported.

---

## Reporting a Security Issue

To report a security issue, please email:

**support@pnwcomputers.com**

Use a subject line similar to:

**Security Report: SelfPublishing-Convert-Verify-Scripts Vulnerability**

Please include as much detail as safely possible, including:

- A clear description of the issue.
- The affected script, function, configuration value, dependency, or documentation section.
- Why the issue may create a security, privacy, or data-loss risk.
- Steps to reproduce the issue using safe sample files, if applicable.
- The potential impact.
- Suggested remediation, if you have one.
- Your operating system and Python version.
- Relevant versions of Pandoc, XeLaTeX, MiKTeX, TeX Live, MacTeX, Pillow, lxml, or other related tools.
- Whether the issue involves unsafe file handling, path traversal, command execution, malicious EPUB content, unsafe archive extraction, dependency risk, data loss, or exposure of unpublished manuscript content.

Please do **not** include private manuscripts, unpublished books, copyrighted material you do not have permission to share, passwords, API keys, publishing account credentials, private customer files, or sensitive personal information in your report.

---

## Examples of Security Issues to Report

Please report issues such as:

- Path traversal when extracting, validating, repairing, or repacking EPUB files.
- Unsafe handling of ZIP/EPUB archives.
- Command injection through filenames, folder names, metadata, image paths, Markdown content, or configuration values.
- Unsafe subprocess calls to Pandoc, XeLaTeX, Java, EPUBCheck, or other external tools.
- Accidental deletion, overwrite, or corruption of source manuscripts or images.
- Scripts writing build artifacts outside the expected output folder.
- Scripts following unsafe symlinks or processing files outside the intended project directory.
- Insecure handling of temporary folders or extracted EPUB contents.
- Exposure of unpublished manuscript content, metadata, author details, or private publishing material.
- Unsafe XML/XHTML parsing behavior.
- Dependency vulnerabilities that materially affect the scripts.
- Documentation that recommends unsafe publishing, file-handling, or dependency-installation practices.
- Build logs that may expose private file paths, author details, manuscript titles, or personal information.
- Any behavior that could cause unexpected execution, file overwrite, data loss, or disclosure of private content.

---

## Issues That Are Not Security Vulnerabilities

The following should normally be opened as regular GitHub issues instead of private security reports:

- Typos or formatting issues.
- Broken links.
- General documentation improvements.
- Feature requests.
- Non-sensitive script bugs.
- KDP layout tuning requests.
- EPUB validation errors that do not create a security risk.
- PDF margin, image scaling, font, or formatting problems.
- Questions about Pandoc, XeLaTeX, EPUBCheck, Pillow, or lxml setup.
- Requests for additional publishing platforms or output formats.

If you are unsure whether something is a security issue, please report it privately first.

---

## Sensitive Information Policy

Do not commit sensitive information to this repository.

This includes, but is not limited to:

- Private manuscripts.
- Unpublished books.
- Draft chapters.
- Paid or licensed book content.
- Private images or illustrations.
- Author tax, payment, royalty, or publishing account information.
- Amazon KDP account details.
- Google Play Books Partner Center account details.
- Passwords.
- API keys.
- Access tokens.
- Private file paths containing usernames or client names.
- Customer publishing projects.
- Copyrighted content that is not approved for publication.
- Private ISBN records or publishing documents.
- Contracts, invoices, or payment information.
- Build logs containing sensitive project details.
- Screenshots showing private account dashboards or unpublished content.

If sensitive information is accidentally committed, it should be treated as exposed. Remove it from the repository, rotate any affected credentials, and review the commit history as needed.

---

## Responsible Disclosure

We ask that all reporters follow responsible disclosure practices:

1. Report security concerns privately.
2. Allow reasonable time for review and remediation.
3. Do not publicly disclose the issue before a fix or mitigation is available.
4. Do not exploit the issue beyond what is necessary to confirm it.
5. Do not access, copy, modify, delete, or disclose manuscripts or files that do not belong to you.
6. Do not test against another person’s publishing files, private documents, or system without explicit authorization.
7. Do not submit malicious EPUB, Markdown, image, XML, or archive samples that could harm systems unless they are clearly identified and safely contained.

Reports involving unauthorized access, data theft, malware, credential theft, copyright abuse, or misuse of private publishing material will not be supported.

---

## File Processing Safety

This project processes files that may contain untrusted content. EPUB files are ZIP-based archives and may contain XHTML, XML, CSS, images, metadata, and internal references. Markdown files may contain image paths, links, HTML fragments, code blocks, and metadata.

Use caution when processing files from unknown or untrusted sources.

Recommended safety practices:

- Keep original manuscripts and source files backed up before running scripts.
- Run scripts on copies of files, not the only original copy.
- Review output files before uploading to any publishing platform.
- Avoid running scripts with administrator or root privileges.
- Avoid processing files from unknown sources on production systems.
- Use a dedicated working folder for each book project.
- Keep build output separate from source content.
- Review temporary folders and generated files before sharing.
- Scan suspicious files before opening or processing them.
- Do not assume that EPUB, image, XML, or Markdown files are safe just because they appear to open normally.

---

## Dependency and Toolchain Security

This repository may rely on external tools and Python packages, including:

- Python.
- Pandoc.
- XeLaTeX.
- MiKTeX, TeX Live, or MacTeX.
- Pillow.
- lxml.
- Java-based EPUBCheck or similar validation tools.

Recommended safeguards:

- Install dependencies from official sources.
- Keep Python and dependencies updated.
- Review package names carefully before installation.
- Avoid installing random packages from unofficial sources.
- Use virtual environments where practical.
- Verify downloaded installers and tools when possible.
- Avoid running unknown LaTeX, EPUB, or script content with elevated privileges.
- Be careful with TeX/LaTeX shell escape features.
- Keep publishing build environments separate from sensitive production systems when possible.

---

## Script Safety Standards

Scripts in this repository should follow these standards whenever possible:

- Avoid hardcoded credentials.
- Avoid unsafe shell command construction.
- Prefer argument lists over shell strings when using subprocess calls.
- Validate input paths.
- Normalize and constrain output paths.
- Avoid writing outside the intended project or build directory.
- Avoid deleting source files automatically.
- Avoid overwriting files without clear warnings or backup behavior.
- Use temporary directories safely.
- Clean up temporary files without deleting unrelated data.
- Handle filenames with spaces, Unicode characters, and special characters safely.
- Treat EPUB archives as untrusted input.
- Prevent archive extraction from writing outside the intended extraction folder.
- Log enough information for troubleshooting without exposing sensitive manuscript content.
- Provide clear errors when manual review is required.
- Use check-only or dry-run modes where practical.

---

## Publishing and Privacy Considerations

Publishing files may contain metadata that users do not intend to disclose.

Before uploading or distributing generated PDF or EPUB files, users should review:

- Book title.
- Subtitle.
- Author name.
- Publisher name.
- Language metadata.
- Identifier metadata.
- Embedded image metadata.
- File names.
- Internal paths.
- Comments or hidden content.
- Generated logs.
- Build timestamps.
- Unused or accidentally included files.
- Cover images and included media.

Users are responsible for verifying that generated files contain only the content they intend to publish.

---

## Copyright and Content Responsibility

This repository is intended to help users convert, validate, and prepare their own publishing files.

Users are responsible for:

- Ensuring they have the rights to all text, images, fonts, and other included materials.
- Reviewing generated files before publishing.
- Complying with Amazon KDP, Google Play Books, and other publishing platform requirements.
- Complying with copyright, licensing, trademark, privacy, and distribution rules.
- Avoiding the accidental inclusion of private, licensed, or third-party material.

Security reports related to accidental disclosure of private or copyrighted content should be reported privately.

---

## Build Artifact Safety

Generated PDF and EPUB files should be treated as important output artifacts.

Recommended safeguards:

- Store generated files in a dedicated `build/` or output folder.
- Review generated files before publishing or sharing.
- Do not assume automated fixes are perfect.
- Keep source files backed up separately.
- Keep final publishing files versioned or archived when appropriate.
- Do not commit large generated files unless the repository intentionally tracks them.
- Do not commit private or unpublished generated files unless they are intended to be public.
- Add build output folders to `.gitignore` when appropriate.

---

## Configuration Safety Standards

Configuration examples in this repository should follow these standards whenever possible:

- Use placeholders instead of real author, client, or publishing account information.
- Avoid hardcoded absolute paths tied to a real user account.
- Avoid including private manuscript folder names.
- Avoid including real unpublished book titles unless intended.
- Clearly mark sample values as examples.
- Avoid embedding private font paths, publishing account details, or customer project names.
- Document which settings users should review before publishing.

Example placeholders:

- `Your Book Title`
- `Author Name`
- `example-book.epub`
- `your_book_googleplay.epub`
- `build/Your_Book_KDP.pdf`
- `C:\Path\To\Your\Book`
- `/path/to/your/book`

---

## Response Timeline

Pacific Northwest Computers will make a best effort to follow this timeline:

| Stage | Target Timeline |
| --- | --- |
| Initial acknowledgment | Within 3 business days |
| Initial review | Within 7 business days |
| Fix, mitigation, or status update | As soon as reasonably practical |
| Public disclosure, if appropriate | After a fix or mitigation is available |

Response times may vary depending on workload, report complexity, dependency testing, and whether additional review is required.

---

## Security Fix Process

When a valid issue is confirmed, maintainers may take one or more of the following actions:

- Remove exposed sensitive information.
- Patch affected scripts.
- Rewrite unsafe documentation.
- Add warnings, validation, or safer defaults.
- Improve path handling, archive extraction, or subprocess behavior.
- Improve temporary directory handling.
- Add `.gitignore` rules for generated files, build folders, or local configuration.
- Recommend credential rotation if exposure is suspected.
- Add sanitization guidance for logs, screenshots, manuscripts, and examples.
- Open a private or public advisory when appropriate.
- Credit the reporter if requested and appropriate.

---

## Legal and Ethical Use

This project is intended for lawful, ethical, personal, professional, and authorized publishing workflows.

Users are responsible for:

- Complying with all applicable laws and publishing platform rules.
- Ensuring they own or have permission to use all included content.
- Protecting unpublished manuscripts and private publishing files.
- Reviewing output before publication.
- Avoiding misuse of copyrighted, private, or third-party material.
- Respecting author, publisher, client, and customer confidentiality.

Do not use this project to process, distribute, publish, or conceal unauthorized, stolen, copyrighted, or private content.

---

## No Warranty

This repository is provided for educational, publishing workflow, and reference purposes.

Security reports and fixes are handled on a best-effort basis. This policy does not create a warranty, service-level agreement, support contract, publishing guarantee, or legal obligation.

Use this project at your own risk. Always keep backups and verify output before publishing.

---

## Contact

For security reports:

**support@pnwcomputers.com**

For general documentation feedback, non-sensitive bugs, publishing workflow questions, or feature requests, please use the normal GitHub issue process.
