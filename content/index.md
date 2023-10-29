# Document Semantic

_Inspired by SemVer, tailored for clear and concise document management in Markdown format._

The inception of Document Semantic was driven by the need to maintain effective document control within GIT, specifically for Markdown files. While GIT is adept at tracking code changes, traditional document formats aren't always suitable for text-based diffing. Markdown, being text-based, integrates seamlessly with GIT, allowing for precise tracking of changes. The introduction of concise short codes ensures that document updates are both meaningful and GIT-friendly. While GIT and Markdown were the primary motivations, this approach is versatile and can benefit a range of documentation use cases.

## New Document

- **New Document (ND)**: Indicates that the document is newly created and has not been subject to any updates or changes.

## Major Semantic Increment

Significant changes that might confuse readers familiar with a previous version.

- **Content Change (CC)**: Substantial alterations to the main content.
- **Structure Change (SC)**: Significant reorganization of the layout.
- **Format Change (FC)**: Major changes to the visual presentation.

## Minor Semantic Increment

Additions or updates that don't modify the core content but enhance its comprehensiveness.

- **New Content (NC)**: Addition of new sections or material.
- **Clarity and Enhancement (CE)**: Minor structural adjustments and improved explanations.

## Patch Semantic Increment

Corrections and enhancements that focus on refining the document's quality.

- **Text Fixes (TF)**: Corrections to spelling, grammar, or punctuation.
- **Data and Link Fixes (DLF)**: Minor updates to footnotes and fixing broken links.

### Short Codes
The short codes, concise in nature, capture the essence of each change, simplifying communication about document updates. Adopting a standardized semantic system for documents ensures clarity, efficiency, and collaboration.

----

## Example

### 1. New Document (v1.0.0)

You create a fresh example.md document:

```markdown

---
title: "Security Protocols"
version: "1.0.0"
---

## Introduction
This document outlines the security protocols for our organization.

## Data Encryption
Data must be encrypted using AES-256 algorithm.

## Password Policy
Use stromg passwords that are at least 12 characters long.
```

Git commit message:

```bash
git commit -m "New Document: Initial creation. [ND]"
```

### 2. Minor Update (v1.1.0)

Adding a new section about Two-Factor Authentication:

```markdown
## Two-Factor Authentication
Enable two-factor authentication for all critical systems.
```

Commit message:

```bash
git commit -m "Added section on Two-Factor Authentication. [NC]
```

### 3. Major Update (v2.0.0)

You radically change the meaning of the Data Encryption section, which could confuse readers familiar with the previous version:

```markdown
## Data Encryption
Data must be encrypted using RSA algorithm.
```

Commit message:

```bash
git commit -m "Changed encryption algorithm from AES-256 to RSA. [CC]
```

### 4. Patch Update (v2.0.1)

You correct some typos and fix a broken link:

```markdown
## Password Policy
Use strong passwords that are a minimum of 12 characters long.
```

Commit message:

```bash
git commit -m "Fixed typos and clarified password requirements. [TF]"
```

### 5. Minor Update (v2.1.0)

Updated Two-Factor Authentication section for better clarity:

```markdown
## Two-Factor Authentication
Two-Factor Authentication (2FA) should be enabled for all critical systems. 2FA provides an extra layer of security beyond just passwords.
```

Git commit message:

```bash
git commit -m "Improved clarity in Two-Factor Authentication section. [CE]"
```

