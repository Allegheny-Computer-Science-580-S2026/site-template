# Junior Seminar Research Project

[![Build Research Journal Site](../../actions/workflows/main.yml/badge.svg)](../../actions/workflows/main.yml)
[![Release Junior Seminar Research Report](../../actions/workflows/release.yml/badge.svg)](../../actions/workflows/release.yml)

For more information about the course requirements for your Junior Seminar course in
Computer and Information Science, please refer to the syllabus for your course.
To enable you to complete many of the deliverables for the Junior Seminar course,
this repository contains instructions for your research journal and your
junior seminar research report. Quarto, serving as a build system for your site, will
build your research report as a website and a PDF.

## Course Requirements

### Research Journal

Your research journal contains posts reflecting on your experiences completing
your junior seminar research project. For the Spring 2026 semester, you are
responsible for writing the following seven research journal entries:

1. **Research Idea**: What is your research idea? Describe the problem you plan
   to investigate and your initial approach.
1. **Prototype Installation and Use**: How do you install and use your research
   prototype? Provide clear instructions and documentation.
1. **Brainstorming and Prototyping Experience**: What were your experiences with
   brainstorming your idea and then prototyping and presenting it? Reflect on
   the challenges and successes.
1. **Chapter 1 and 2 Reflections**: Combined post reflecting on:
   - What is your reflection from writing Chapter 1: Introduction
   - What is your reflection from writing Chapter 2: Background Related Work
1. **Chapter 3 and 4 Reflections**: Combined post reflecting on:
   - What is your reflection from writing Chapter 3: Methodology
   - What is your reflection from writing Chapter 4: Results
1. **Chapter 5 Reflection**: What is your reflection from writing Chapter 5:
   Conclusions and Future Work
1. **Overall Project Reflection**: What is your overall reflection on the
   research project and what are your next steps?

### Junior Seminar Research Report Chapters

All researchers in the Junior Seminar course in Computer and Information Science
must document their work in the form of a written research report. While
variations on the typical structure and contents of a research report can be
specific to a certain project, a typical Computer and Information Science
research report contains `5` chapters:

1. Introduction
1. Related Work
1. Methods
1. Experiments (Results)
1. Conclusions and Future Work

Students complete all five chapters during the Spring 2026 semester. Each
chapter should be approximately **5 to 7 pages** in length. More details about
the baseline requirements for the junior seminar research report are available
in the course syllabus and in the [CONTRIBUTING.md](CONTRIBUTING.md) file.

## Course Technology Use

### Enabling Site Build

This site deploys via GitHub Pages using the Quarto static site building system.

1. Go to the `Settings` menu on this repository and locate the `Pages` submenu.

![GitHub Settings, Pages submenu](https://raw.githubusercontent.com/ReadyResearchersTemplates/site-template/media/img/600%20-%20Site%20Template%20-%20Github%20Pages%20Menu.png)

2. On the resulting screen, find the `Build and deployment` menu; select `GitHub Actions`

![GitHub pages, Build and Deployment item](https://raw.githubusercontent.com/ReadyResearchersTemplates/site-template/media/img/600%20-%20Site%20Template%20-%20Github%20Actions%20Menu.png)

### `Private` vs. `Public` availability

You retain the choice to make your research journal private or public; the
`Pages` settings menu should allow either. Your URL will change depending on
which selection you make, and you should be able to find the resulting URL of
your journal by visiting the pages section of the repository's `Settings` menu.
Your URL should display at the top of the page:

![GitHub Pages url](https://raw.githubusercontent.com/ReadyResearchersTemplates/site-template/media/img/600%20-%20Site%20Template%20-%20Github%20URL.png)

### Release Tagging

Since this repository primarily contains Markdown and/or LaTeX source code, the
GitHub Actions configuration for it will compile the source code and
automatically release a PDF of the main file whenever the last commit is
associated with a [Git
Tag](https://git-scm.com/book/en/v2/Git-Basics-Tagging).

This will build a PDF file available in the "Releases" listing for this
repository. All release numbers for your writing in this repository should
adhere to the [Semantic Version](http://semver.org/) standard expected of
GitHub projects. Here this means that:

- `Major version` releases feature a tag number change reflecting full
  releases; generally these start at `1.0.0`
- `Minor version` releases indicate small changes or additions to documents;
  typically these increment the second digit in the version (e.g. `1.1.0`)

Please note that your instructor will expect that the PDF generated from
"tagged" releases of the file `JuniorSeminarReport.pdf` that has a version
number greater than `1.0.0` if it contains a final version of Chapter 1. It
should then contain a version number greater than `2.0.0` if it contains a
final version of Chapter 2 and so on. The idea is that each major release of
your junior seminar research project should contain a final version of the
chapter that is signaled by the semantic version number.

That is:

- if your commit is tagged `JuniorSeminarReport-1.0.0`, then
- the file `JuniorSeminarReport.pdf` should be available for download in the
  "Releases" tab in your GitHub repository for this project under the name
  `JuniorSeminarReport-1.0.0`.

To ensure you can create a release appropriately, make a single small change to
the `thesis/index.qmd` and:

1. Use `git` to `commit` your file changes using a `git commit` command
1. Create your first tag for this repository: type `git tag junior_seminar_report-0.1.0`.
1. You are now ready to push your changes with the tag number using `git push -u origin main --tags`

The above steps should build a version of your project and release it on GitHub!
If something does not work correctly, please contact Professor Gregory M.
Kapfhammer to explain the details of the challenges that you faced. You can
schedule an office hours appointment at:
[https://www.gregorykapfhammer.com/schedule/](https://www.gregorykapfhammer.com/schedule/)

It is also important to note that it is possible for a student to perform a
manual release of the PDF of their junior seminar research report. Again, please
communicate with Professor Kapfhammer for more information about the steps you
would take to perform a manual release. With that said, it is important to
stress that you should learn how to perform an automated release of your report
in PDF and only use the manual approach if there is a severe and extenuating
circumstance (e.g., GitHub Actions stops working for a short time) that prevents
you from performing an automated release.

When you make subsequent changes to your files and perform commits and you are
ready to release a new version of `JuniorSeminarReport.pdf`, then you should
again tag your work _before a `push` command_ with a tag that
adheres to the [Semantic Versioning](http://semver.org/) standard.

Each time that you correctly execute this sequence of commands you will release
a new version of your document to GitHub that is easily accessible as a PDF to
you and to your instructor.

While you are able to build copies of your PDF locally using the `quarto render`
command, the only copy that will be evaluated is that released to GitHub following
the procedure outlined above.

## Seeking Assistance

If you are having trouble completing any part of this project, then please talk
with Professor Gregory M. Kapfhammer. In particular, if you have questions about
your research project, please see Professor Kapfhammer during office hours or
schedule an appointment at:

- **Professor Website**: [https://www.gregorykapfhammer.com/](https://www.gregorykapfhammer.com/)
- **Office Hours Scheduling**: [https://www.gregorykapfhammer.com/schedule/](https://www.gregorykapfhammer.com/schedule/)

Students who want to learn more about [Managing releases in a GitHub
repository](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository)
or other topics related to release management on GitHub are encouraged to check
the [GitHub Releases
Documentation](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases).
