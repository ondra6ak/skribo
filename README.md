Skribo
======

Dead simple screenplay format.

Installation
------------

Install `python3` and `pip`, `pandoc`, `texlive-luatex` (recomended) and `texlive-latex-extra` via your package manager. And then use these commands to complete the installation:

	# pip3 install unicode-slugify
	# mkdir -p /usr/lib/python3/dist-packages/skribo
	# cp skribo.py /usr/lib/python3/dist-packages/skribo/__init__.py
	# chmod +x skribo-*
	# cp skrib-* /usr/bin/
	# cp -r robot /usr/share/fonts/truetype/roboto

Usage (WIP)
-----------

	skribo-reader -i examples/monty_python.skrb | pandoc -f json --normalize --latex-engine lualatex --template skribo.latex -o examples/monty_python.pdf

Syntax
------

Every screenplay must begin with header like the one bellow and blank line after

	TITLE
	Subtitle
	Alice Doe; Bob Doe


Each scene begins with the scene name in allcaps and blank line

	SCENE EXAMPLE


Replica begins with the character name and a colon following by the actual text and a blank line

	Alice: Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.


Notes can appear anywhere in the text

	Alice: Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. (exits)

	(The room darkens)
