# Content Verification Findings

**Date:** 2026-03-05
**Content type:** Workshop (hands-on lab)
**Content directory:** `content/modules/ROOT/pages/`
**Total issues found:** 27 (4 Critical, 18 High, 5 Medium)
**Status:** ALL 27 ISSUES RESOLVED

---

## Critical Issues (4) - RESOLVED

### 1. Broken xref to non-existent `appendix.adoc` - RESOLVED

- **File:** `index.adoc:57`
- **Was:** `xref:appendix.adoc[Appendix]` pointed to a non-existent file
- **Resolution:** Created `appendix.adoc` with troubleshooting guidance and a useful commands reference table

### 2. Broken xref to non-existent `environment-details.adoc` (10+ files) - RESOLVED

- **Files affected:** `00-introduction.adoc`, `11-vscode-collection.adoc`, `12-ade.adoc`, `13-module.adoc`, `21-molecule.adoc`, `22-pytest-ansible.adoc`, `23-tox-ansible.adoc`, `31-ansible-builder.adoc`, `32-ansible-sign.adoc`, `99-conclusion.adoc`
- **Resolution:** Created `environment-details.adoc` with access credentials and lab environment components

### 3. Typo `hhttps://` in conclusion link - RESOLVED

- **File:** `99-conclusion.adoc:30`
- **Resolution:** Fixed to `https://`

### 4. Duplicate task numbering in ansible-sign module - RESOLVED

- **File:** `32-ansible-sign.adoc`
- **Was:** Two "Task 2" and two "Task 3" headings
- **Resolution:** Merged intro paragraph into Task 2, renumbered all tasks sequentially (Tasks 1-6). Also fixed "REAME" typo to "README" on line 112

---

## Scaffold Issues (7) - RESOLVED

### 5. `site.title` stale template value - RESOLVED

- **File:** `site.yml:3`
- **Resolution:** Changed from `Showroom Template Demo` to `Introduction to Ansible Development Tools`

### 6. `site.url` points to template repo - RESOLVED

- **File:** `site.yml:4`
- **Resolution:** Changed from `https://github.com/rhpds/showroom_template_nookbag` to `https://github.com/rhpds/ansible-dev-tools-showroom`

### 7. `runtime.fetch` not set in site.yml - RESOLVED

- **File:** `site.yml`
- **Resolution:** Added `runtime: fetch: true` section

### 8. `antora.yml` title stale template value - RESOLVED

- **File:** `content/antora.yml:2`
- **Resolution:** Changed from `Showroom Collection` to `Introduction to Ansible Development Tools`

### 9. `start_page` missing from `antora.yml` - RESOLVED

- **File:** `content/antora.yml`
- **Resolution:** Added `start_page: index.adoc`

### 10. `{lab_name}` attribute not defined - RESOLVED

- **File:** `content/antora.yml`
- **Resolution:** Added `asciidoc.attributes.lab_name: "Introduction to Ansible Development Tools"`

### 11. All functional tabs commented out in `ui-config.yml` - RESOLVED

- **File:** `ui-config.yml`
- **Resolution:** Removed Llamastack Docs tab, added Terminal (`/wetty:443`) and OCP Console tabs

---

## Structure and Learning Design Issues (4) - RESOLVED

### 12. Learning objectives missing from 7 of 9 modules - RESOLVED

- **Files:** `11-vscode-collection.adoc`, `12-ade.adoc`, `13-module.adoc`, `22-pytest-ansible.adoc`, `23-tox-ansible.adoc`, `31-ansible-builder.adoc`, `32-ansible-sign.adoc`
- **Resolution:** Added `== Learning Objectives` section with 3-5 bullet points to each module

### 13. References section in individual module - RESOLVED

- **File:** `00-introduction.adoc`
- **Resolution:** Removed `== Helpful Links` section, moved links to conclusion

### 14. No References section in conclusion - RESOLVED

- **File:** `99-conclusion.adoc`
- **Resolution:** Added `== References` section with consolidated links from all modules. Updated repo URL from `ansible-super-lab-showroom` to `ansible-dev-tools-showroom`

### 15. `index.adoc` not listed in `nav.adoc` - RESOLVED

- **File:** `content/modules/ROOT/nav.adoc`
- **Resolution:** Added `* xref:index.adoc[Home]` at the top of navigation

---

## Typos and Text Errors (7) - RESOLVED

### 16. Double word "have have" - RESOLVED

- **File:** `00-introduction.adoc:80`
- **Resolution:** Changed to `we have provided`

### 17. Misspelling "workspacs" - RESOLVED

- **File:** `00-introduction.adoc:116`
- **Resolution:** Changed to `This workspace provides`

### 18. Misspelling "fileds" - RESOLVED

- **File:** `12-ade.adoc:89`
- **Resolution:** Changed to `the following fields:`

### 19. Double numbering prefix - RESOLVED

- **File:** `12-ade.adoc:95`
- **Resolution:** Removed duplicate `.` prefix

### 20. Duplicate `== Lab Briefing` heading - RESOLVED

- **File:** `21-molecule.adoc`
- **Resolution:** Removed first `== Lab Briefing` (was redundant with new Learning Objectives section), kept only the second one with briefing content

### 21. Duplicate "Task 4" heading - RESOLVED

- **File:** `22-pytest-ansible.adoc`
- **Resolution:** Renamed second "Task 4" to `=== Task 5: Verify the test results`

### 22. "it's" used as possessive - RESOLVED

- **File:** `31-ansible-builder.adoc:276`
- **Resolution:** Changed to `its dependencies`

---

## AsciiDoc Formatting Issues (3) - RESOLVED

### 23. No images have `link=self,window=blank` (~28 images) - RESOLVED

- **Files:** `00-introduction.adoc`, `11-vscode-collection.adoc`, `12-ade.adoc`, `13-module.adoc`, `21-molecule.adoc`, `31-ansible-builder.adoc`
- **Resolution:** Added `link=self,window=blank` to all 28 block `image::` macros

### 24. Title Case headings - RESOLVED

- **Resolution:** Fixed `== Enhanced Developer Experience` to `== Enhanced developer experience` in `31-ansible-builder.adoc`. Fixed 4 task headings in `13-module.adoc` to sentence case. Kept `== Lab Guide: Hands-On Tasks` as-is (consistent structural heading across modules)

### 25. Expected output marked as executable code block - RESOLVED

- **File:** `22-pytest-ansible.adoc:196-210`
- **Resolution:** Changed `[source,bash,role=execute]` to `[source,text]` for expected output block

---

## Red Hat Style Guide Issues (4) - RESOLVED

### 26. Stray bare link and old repo references - RESOLVED

- **Resolution:** Removed stray link from `23-tox-ansible.adoc:205`. Updated `ansible-super-lab-showroom` references to `ansible-dev-tools-showroom` in `00-introduction.adoc` and `99-conclusion.adoc`

### 27. Bare acronyms without first-use expansion - RESOLVED

- **Resolution:**
  - `32-ansible-sign.adoc`: Expanded "AAP" to "Ansible Automation Platform (AAP)" and "GPG" to "GNU Privacy Guard (GPG)"
  - `31-ansible-builder.adoc`: Expanded "UBI" to "Universal Base Image (UBI)"

### 28. Prohibited term "powerful" - RESOLVED

- **Files:** `index.adoc:49`, `99-conclusion.adoc:48`
- **Resolution:** Replaced "powerful terminal-based user interface" with "feature-rich terminal-based user interface"

### 29. Missing expected output after commands - RESOLVED

- **Resolution:**
  - `11-vscode-collection.adoc`: Added NOTE describing expected output after `ls -lha` command
  - `32-ansible-sign.adoc`: Added expected output block after `ansible-sign project gpg-verify .` command

---

## Files Changed

| File | Changes Made |
|------|-------------|
| `site.yml` | Updated title, URL, added `runtime.fetch` |
| `content/antora.yml` | Updated title, added `start_page`, added `lab_name` attribute |
| `ui-config.yml` | Replaced Llamastack tab with Terminal and OCP Console tabs |
| `content/modules/ROOT/nav.adoc` | Added Home link for `index.adoc` |
| `content/modules/ROOT/pages/appendix.adoc` | **NEW** - Troubleshooting and useful commands |
| `content/modules/ROOT/pages/environment-details.adoc` | **NEW** - Access credentials and lab components |
| `content/modules/ROOT/pages/index.adoc` | Replaced "powerful" with "feature-rich" |
| `content/modules/ROOT/pages/00-introduction.adoc` | Fixed typos ("have have", "workspacs"), removed Helpful Links, updated repo URL, added `link=self,window=blank` to images |
| `content/modules/ROOT/pages/11-vscode-collection.adoc` | Added learning objectives, added `link=self,window=blank` to images, added NOTE for `ls` output |
| `content/modules/ROOT/pages/12-ade.adoc` | Added learning objectives, fixed "fileds" typo, fixed double numbering, added `link=self,window=blank` to images |
| `content/modules/ROOT/pages/13-module.adoc` | Added learning objectives, fixed Title Case headings, added `link=self,window=blank` to images |
| `content/modules/ROOT/pages/21-molecule.adoc` | Removed duplicate `== Lab Briefing`, added `link=self,window=blank` to images |
| `content/modules/ROOT/pages/22-pytest-ansible.adoc` | Added learning objectives, renamed duplicate Task 4 to Task 5, fixed executable output block |
| `content/modules/ROOT/pages/23-tox-ansible.adoc` | Added learning objectives, removed stray bare link |
| `content/modules/ROOT/pages/31-ansible-builder.adoc` | Added learning objectives, fixed Title Case heading, expanded "UBI", fixed "it's" to "its", added `link=self,window=blank` to images |
| `content/modules/ROOT/pages/32-ansible-sign.adoc` | Added learning objectives, restructured tasks (1-6), expanded "AAP" and "GPG", fixed "REAME" typo, added expected output for verify command |
| `content/modules/ROOT/pages/99-conclusion.adoc` | Fixed `hhttps://` typo, added References section, replaced "powerful", updated repo URL |
