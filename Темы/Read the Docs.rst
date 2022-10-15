Read the Docs
**************
Read the Docs упрощает документирование ПО, автоматизируя создание, управление версиями и хранение документации.
Полезные ссылки:
https://readthedocs.org/ - 

https://nbconvert.readthedocs.io/en/latest/usage.html

https://docutils.sourceforge.io/rst.html

https://www.sphinx-doc.org/en/master/

Подготовка к работе с Read the Docs
===================================
1. Устанавливаем sphinx 
2. Устанавливаем pandoc

Добавление Jupyter Notebook'ов build приводит к ошибкам при сборке на хостинге Read the Docs.
Данная проблема может быть решена в результате реализации следующих шагов:
1.Добавить корень проекта файл requirements.txt, в котором прописано следующее содержание:: 
        sphinx>=1.4
        ipykernel
        nbsphinx

Jupyter Notebbok и Read the Docs
=================================
Файлы Jupyter Notebook (т.е. формата  ``.ipynb``) могут читаться Read the Docs. 
Для конвертации формата Jupyter Notebook ``.ipynb`` в RESTuctured Text ``.rst`` необходимо применить к выбранному файлу команду::
        nbconvert your_file.ipynb --to rst

Для того, чтобы sphix парсил ``.ipynb`` формат в файле config нужно добавить следующий::
        extensions = ["nbsphinx",]
А в файл requirements.txt::
        sphinx>=1.4
        ipykernel
        nbsphinx

