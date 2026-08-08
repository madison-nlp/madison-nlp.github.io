# Madison NLP Website (GitHub Pages)

This repository contains the source code for the lab website, hosted via GitHub Pages and built using Jekyll. 

The site is data-driven where possible, so most people updates do not require editing HTML.

The website can currently be accessed at:
```
https://madison-nlp.github.io/
```

## Deployment (One-Time)

The site is deployed via GitHub Pages.
- Repository: `madison-nlp.github.io`
- Deployment: `Settings` → `Pages` → `Build and deployment` → `Source: GitHub Actions`

**Important:** This site depends on Jekyll. Do not add a `.nojekyll` file.

## Repository Structure

```
_config.yml
Gemfile
index.md
people.md
research.md
courses.md
/_layouts
/_includes
/_data
/.github/workflows
/assets
```

### Root Files
- `_config.yml`: Global site configuration. Update this if: Changing domain, updating site title.
- `assets/css/style.css`: Contains all custom styling. Only edit if changing visual design.
- `index.md`: Homepage. Contains: Research themes, Carousel.
- `people.md`: People page. Contains: Faculty (hero block), Current students (2-column grid), Alumni (3-column grid).
   - Uses data from `_data/people.yml`. Do not hardcode people here.
- `research.md`: Research overview page.
- `courses.md`: Courses page.


### Data Files (Update These Regularly)

All dynamic content lives in `_data/`.

- `_data/people.yml`
  - Controls: Faculty, PhD students, Masters and Undergraduate Students, Alumni
  - Update this when: Adding faculty, Adding a student, Moving a student to alumni, Updating role/title/website links/photos
  - Example structure:
    ```
    pis:
      - name: "Prof. X"
        title: "Assistant Professor, Dept of X"
        affiliation: "University of Y"
        photo: "assets/photos/prof-x.png"
        website: "website"

    students:
      - name: "Student A"
        role: "PhD in CS, Fall 2025-"
        photo: "assets/photos/student-a.jpg"
        website: "..."

    masters_undergrads:
      - name: "Student B"
        role: "MS in CS"
        photo: "assets/photos/student-b.jpg"
        website: "..."
  
    alumni:
      - name: "Alum A"
        text: "PhD 2020-25, now at Company"
        website: "..."
    ```

- `assets/photos/`
  - Contains: Faculty, Student, Alumni photos, Carousel images
  - All image paths in YAML are relative to repository root.
  - Use lowercase filenames and avoid spaces.
  - Example: `assets/photos/lab-2024-spring.jpg`
   
  
