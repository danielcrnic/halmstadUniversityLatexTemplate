# Halmstad University LaTeX thesis template
> **Note**
>
> This LaTeX template is not endorsed by Halmstad University in any way. The only purpoce of this LaTeX template is to facilitate thesis writing in LaTeX while still follow the offical template layout such as paragraph styles and headings format. 

A LaTeX template that was created when writing [my own thesis](https://www.diva-portal.org/smash/record.jsf?pid=diva2:1675317). It is based on the [new template](https://www.hh.se/student-web/content-a-z/thesis-templates.html) from Halmstad University which only exists as a Word template.

The template is configured as following:
- Book style (new chapters start on an odd page)
- Figure-, listing- and table-numbering are seperarated from chapters (1, 2, 3, ...)
- Table caption is above the table
- Uses vancouver format for references

The template also tries to match the Word template as much as possible.

## Setup in Overleaf
### 1. Download *Gill Sans Std* font
The headers in the template use the Gill Sans Std font which does not exists in Overleaf and therefore needs to be downloaded manually. An `.oft` font is required. You can download the font from one of these websites:

- https://www.cufonfonts.com/font/gill-sans-std
- https://freefontsdownload.net/free-gillsansstd-font-136066.htm

...or any other website that you feel comfortable with downloading from.

### 2. Import project into Overleaf
Download the `.zip` file from [the releases (https://github.com/danielcrnic/halmstadUniversityLatexTemplate/releases)](https://github.com/danielcrnic/halmstadUniversityLatexTemplate/releases) and goto *Your Projects* page on Overleaf. Press the *New Project* button and choose *Upload Project*. Select or drag the downloaded `.zip` file and it should start uploading. Once the upload has finished it should automatically open the project in Overleaf.

### 3. Changing compiler
When trying to compile the project it will fail since the default compiler on Overleaf is not compatible with the *fontspec* package which is needed for the use of custom font. 

While inside an project in Overleaf, press the *Menu* button (on the upper left side with the Overleaf logo) and scroll down to the *Settings* section where you should find the *Compiler* option. Choose one of the following compiler:
- XeLaTeX
- LuaLaTeX

> I used *XeLaTeX* for the period of writing my thesis without problem. However, if you encouter any problems, try using *LuaLaTeX*

It should now be possible to compile the project and generate an PDF.

### 4. Adding *Gill Sans Std* font into Overleaf
It is possible to compile the project without the font. However, the chapter, subchapters and subsubchapters will not be visible. 

To add the font, unzip `GillSansStd.otf` from the zip-file you downloaded from the first step. Inside Overleaf, select the upload button which the third button under the *Menu* button and drag or select the font file. 

Make sure that the font is named `GillSansStd.otf`. If you want to change the name of the font you will have to change the name in the `main.tex` file at line `41`.

It should now be possible to compile the project and the chapters should be visible in the generated PDF with the new font.

### 5. Adding University's offical front cover
The project does not include an front cover and has to manually be created. You have to use the University's offical front cover which can be downloaded at:

https://www.hh.se/student-web/content-a-z/thesis-templates.html

at the third step.

You will have to use an word processor (like Microsoft Word or LibreOffice) since it is a `.doc` file. Fill in the information required on the front cover and remove the second page (which only contains the headlines). Thereafter, export the front cover as a PDF named `front-cover.pdf`.

Once you have a PDF of the front cover, go to the Overleaf project and upload the PDF to the project to replace the temporary. When compiling the project the front cover page should exist as the first page.

If you want `front-cover.pdf` to be named something else, make sure to also change the name on line `94` in the `main.tex` file.

