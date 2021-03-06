# visualCode---Latex-Workshop-
Instruction on how to use VSCode in order to use Latex (TeXLive)

1. Add the extension LaTeX Workshop to VSCode
2. Using keyboard shortcut (ctrl/cmd+,) to quick open Settings;
3. Add the following .json code into the Settings:

{
    
    "latex-workshop.view.pdf.viewer": "tab",
    "latex-workshop.kpsewhich.enabled": true,
    "latex-workshop.intellisense.package.enabled":true,
    "latex-workshop.latex.recipes": [
        {
            "name": "lulatexmk 🔃",
            "tools": [
                "lualatexmk"
            ]
        },
        {
            "name": "latexmk 🔃",
            "tools": [
                "latexmk"
            ]
        },
        {
            "name": "xelatexmk 🔃",
            "tools": [
                "xelatexmk"
            ]
        },
        {
            "name": "platexmk 🔃",
            "tools": [
                "platexmk"
            ]
        },
        {
            "name": "pdflatex ➞ bibtex ➞ pdflatex ×2",
            "tools": [
                "pdflatex",
                "bibtex",
                "pdflatex",
                "pdflatex"
            ]
        },
        {
            "name": "xelatex ➞ biber ➞ xelatex",
            "tools": [
                "xelatex",
                "biber",
                "xelatex"
            ]
        },
        {
            "name": "pdflatex -> mkglo -> pdflatex -> makeindex -> bibtex -> pdflatex",
            "tools": [
                "pdflatex",
                "makeglossaries",
                "pdflatex",
                "makeindex",
                "bibtex",
                "pdflatex"
            ]
        },
        {
            "name": "pdfLatex -> makeglossaries -> latex -> bitex -> dvips",
            "tools": [
                "pdflatex",
                "makeglossaries",
                "latex",
                "bibtex",
                "dvips"
            ]
        }
    ],
    "latex-workshop.latex.tools": [
        {
            "name": "latexmk",
            "command": "latexmk",
            "args": [
                "-synctex=1",
                "-file-line-error",
                "-latex",
                "-outdir=%OUTDIR%",
                "%DOC%"
            ],
            "env": {}
        },
        {
            "name": "platexmk",
            "command": "latexmk",
            "args": [
                "-synctex=1",
                "-file-line-error",
                "-pdf",
                "-outdir=%OUTDIR%",
                "%DOC%"
            ],
            "env": {}
        },
        {
            "name": "xelatexmk",
            "command": "latexmk",
            "args": [
                "-synctex=1",
                "-file-line-error",
                "-xelatex",
                "-outdir=%OUTDIR%",
                "-interaction=nonstopmode",
                "-halt-on-error",
                "%DOC%"
            ],
            "env": {}
        },
        {
            "name": "latex",
            "command": "latex",
            "args": [
                "%DOC%"
            ],
            "env": {}
        },
        {
            "name": "makeglossaries",
            "command": "makeglossaries",
            "args": [
              "%DOCFILE%"
            ]
        },
        {
            "name": "dvips",
            "command": "dvips",
            "args": [
              "%DOCFILE%"
            ]
        },
        {
            "name": "ps2pdf",
            "command": "ps2pdf",
            "args": [
              "%DOC%"
            ]
        },
        {
            "name": "lualatexmk",
            "command": "latexmk",
            "args": [
                "-synctex=1",
                "-file-line-error",
                "-lualatex",
                "-outdir=%OUTDIR%",
                "-interaction=nonstopmode",
                "-halt-on-error",
                "%DOC%"
            ],
            "env": {}
        },
        {
            "name": "pdflatex",
            "command": "pdflatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-halt-on-error",
                "-file-line-error",
                "%DOC%"
            ],
            "env": {}
        },
        {
            "name": "xelatex",
            "command": "xelatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-halt-on-error",
                "-file-line-error",
                "%DOC%"
            ],
            "env": {}
        },
        {
            "name": "bibtex",
            "command": "bibtex",
            "args": [
                "%DOCFILE%"
            ],
            "env": {}
        },
        {
            "name": "makeindex",
            "command": "makeindex",
            "args": [
                "%DOCFILE%"
            ],
            "env": {}
        },
        {
            "name": "biber",
            "command": "biber",
            "args": [
                "%DOCFILE%"
            ],
            "env": {}
        }
    ],
    "latex-workshop.latex.recipe.default": "pdflatex",
}

4. Restart VSCode !
