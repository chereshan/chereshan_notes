Jupyter
============================

Источники
---------

0. https://jupyter-notebook.readthedocs.io/en/stable/examples/Notebook/Working%20With%20Markdown%20Cells.html
1. https://www.markdownguide.org/cheat-sheet/
2. https://www.markdownguide.org/tools
3. https://www.markdownguide.org/tools/google-docs-to-markdown/
4. https://daringfireball.net/projects/markdown/
5. https://www.ibm.com/docs/en/watson-studio-local/1.2.3?topic=notebooks-markdown-jupyter-cheatsheet
6. https://makeabilitylab.github.io/physcomp/signals/jupyter-notebook.html
7. [How and why should you export reports from Jupyter Notebook to PDF](https://en.leftjoin.ru/all/export-jupyter-notebook-to-pdf/)

1. Quantecon:  

Jupyter notebooks - это один из возможных способов взаимодействия с Python и его научными библиотеками.

Jupyter Notebook - это браузерный интерфейс с: 

* Способность писать и запускать команды Python
* Форматированный вывод в браузере, включая таблицы, фигуры, анимации и т.д.
* Опция совмещать форматированный текст и математические выражения

Notebook-файлы - это всего лишь файлы структурированные в JSON и типично имеющие формат ``.ipynb``. Их можно расшаривать как любые другие файлы, а таккэе заливать в репозиторий Git. Они могут просматриваться с помощью web-сервисов, вроде nbviewer. Notebook-файлы на этом сайте - это статические html репрезентации. Чтобы воспроизвести ее, ее надо будет загрузить. 


Установка Jupyter Notebook
--------------------------

Команда в CMD::

    pip install jupyter notebook

После этого Jupyter Notebook может быть вызван командой в CMD ``jupyter notebook``


.. code:: ipython3

    # Магические команды Jupyter
    %matplotlib notebook #Интерактивный режим
    %matplotlib qt
    %matplotlib inline #Вывод в Jupyter'е

Команды режима редактирования (Enter - Вход в режим редактирования)
* ``ctrl+/`` - Закончить строку
* ``ctrl+L`` - AutoPeP клетки
* ``ctrl+shift+L`` - AutoPeP всего
* ``Tab`` - подсказкми

Установка сторонних пакетов:
1. Anaconda prompt
2. conda info --envs
3. conda activate <envs names (base)>
4. pip install package

Команды командного режима (Esc - командный режим)
* ``X`` - Вырезать ячейку
* ``M``/ ``Y`` - Markdown/Код
* ``B`` - Вставить ячейку
* ``Z`` - Отменить удаление ячейки
* ``D`` - Удалитьвыбранную ячейку
* ``shift+M`` - Объединить выбранные ячейки
* ``shift+L`` - Показать номера строк всех ячеек

Magic-команды
----------------

``%colors`` - оформление окна ошибок (``rocolocrs``, ``Linux``, ``LightBG``)
``%conda install package`` - Установка пакета из Jupyter
``%env`` - Переменные среды
``%ismagic`` - перечисление magic-команд
``%pip install package`` - pip из среды jupyter
``%pwd`` - активная директория
``%reset - f или -s`` - удалить все имена из пространства имен
``%reset-selective -f`` - удалить выбранные имена
``%who (тип)`` - все переменные данного типа
``%who_is (тип)`` - возвращает все переменные данного типа
``%whos`` - подробно обо всех переменных

Исправление проблемы с некорректным отображением изображений в Jupyter Notebook
-------------------------------------------------------------------------------

Суть проблемы: Я копирую скриншоты в JN-документы. В JN они отображаются корректно, однако в html формате на Read the Docs корректно отображается лишь первое изображение, а остальные повтоярют тоже самое первое изображение.

Решение: необходимо после вставки скриншота в JN переименовывать ``image.png`` на уникальное не повторяющееся в документе имя::
    ![image.png](attachment:image.png)


Основной синтаксис
------------------

1. Заголовки


