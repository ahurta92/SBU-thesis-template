# The latex template for Stony Brook University Ph.D. and MS Thesis

## Motivation 

I am not shocked by the [lack of proper LaTeX templates](https://grad.stonybrook.edu/_data/documents/forms/2020-forms/Dissertation_template-PHD_EW.pdf) for the Ph.D. thesis at Stony Brook graduate school page. 

This template is modified from [the SBU template provided by](https://github.com/urfdvw/SBU-thesis-template), which was modified from [the thesis of Avi Srivastava](https://github.com/k3yavi/thesis). Thank both of them.

I've made some minor changes to the previous version:

1. I've added a preface environment to include a preface page in the frontmatter.
2. I prefer to use the subfile latex package instead of the standard input package
3. I've also added `yourcommands.sty` a standalone file to include custom commands.

## How to use

### Get started
1. Download this repository from GitHub website as a `.zip` file.
2. Go to [Overleaf website](https://www.overleaf.com/) and log in.
3. When clicking on `New Project` button, choose `Upload Project`.
4. Upload the downloaded `.zip` file
5. (optional but suggested) Connect this Overleaf document to a new Github repository. See [This page](https://www.overleaf.com/learn/how-to/How_do_I_connect_an_Overleaf_project_with_a_repo_on_GitHub,_GitLab_or_BitBucket%3F)

### Start to write
- The `main.tex` file
    - (*The line numbers mentioned here are line numbers in the template. They might change once you fill in your content.*)
    - Head directly to line 80 and fill in `THESIS INFORMATION`
    - In `TITLE PAGE`, you might only want to change line 138, the date.
    - `THESIS CONTENT - CHAPTERS` at line 280 is the main body
        - NEVER write any content here
        - Write your main body in separated `.tex` files and `\input` them here.
    - Appendixes should be `\input`ed in `THESIS CONTENT - APPENDICES` at line 297
    - If you need any extra packages, `\usepackage` them in `Your Packages` at line 55
    - For any other parts of the `main.tex` file, you need to modify them at your own risk.
- The `Chapters` folder
    - All the text parts should be in this folder.
    - You can divide the text by `\chapter` or `\section`
        - The rule of thumb is a file should not exceed 500 lines. If so, break it
    - You can also create subfolders for each Chapter for a better organization.
- The `Figures` folder
    - All the Figure files should be in this folder.
    - If you have figures created by LaTex code (Highly not suggested), put them here as separated `.tex` files.
- The `Tables` folder
    - If you have tables, put them here as separated `.tex` files.
    - If you generated your tables from [tablesgenerator.com](https://www.tablesgenerator.com/) (Highly suggested), put the source file of the table here as well.
- The `Appendices` folder
    - If you have appendices, put them here as separated `.tex` files.
- The `main.bib` file
    - All citations should be here,

## Additional tools
- [Bib file merge tool](https://urfdvw.github.io/bibmerge/)
    - In case you never used any citation management software and you have many `.bib` files from previous papers, you can use to merge them into one.
- `CiatationChecker.py` file
    - This Python script locates at the root directory of this repository.
    - It will count how many times you cited each paper by scaning your `.tex` and `.bib` files.
        - This will be helpful to identify un-cited papers in the `.bib` file
    - **How to use**: 
        - You need to download your Overleaf project to local and unzip.
        - You also need to have a python distribution installed
        - By running the script, it will generate a `.csv` table showing the countings.
- [LaTex table generator](https://www.tablesgenerator.com/)

