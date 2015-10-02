

Unbuntu 개발 환경 설정
----------------------
아래와 같이 필요한 package를 설치

~~~bash
	$ sudo apt-get install pandoc nbibtex texlive-latex-base \  
	texlive-latex-recommended texlive-latex-extra \
	preview-latex-style dvipng texlive-fonts-recommended \
	liblatex-driver-perl texlive-fonts-extra ko.tex retext
~~~

- pandoc: markup converter
- retext: 실시간 markdown 편집기


Default Templete 확인 방법
--------------------------

아래와 같이 Templete을 확인할 수 있으며, 각 옵션은 '--variable sansfont=Arial' 과 같은 형태로 설정할 수 있음

~~~bash
    $ pandoc -D latex
    \documentclass[$if(fontsize)$$fontsize$,$endif$$if(lang)$$lang$,$endif$$if(papersize)$$papersize$,$endif$$for(classoption)$$classoption$$sep$,$endfor$]{$documentclass$}
    \usepackage[T1]{fontenc}
    \usepackage{lmodern}
    \usepackage{amssymb,amsmath}
    \usepackage{ifxetex,ifluatex}
    ...
~~~


README.md pdf 변환 방법
-----------------------
	$ pandoc -s -S -H template00/build/pdf.tex -o readme.pdf README.md

## Code block highlight ##

~~~python
import re
print ("this is test")
~~~


markdown cheat-sheet
--------------------
[Download](http://www.transformationswerk.de/transsetter/wp-content/uploads/2014/10/cheat-sheet-page-001.jpg)


