# rk1

## Short description of the main task
 ```shell
 Analysis of github sourse
 ```
## Tasks, their code and output
1.  Количество файлов
    ```shell
    $ git clone https://github.com/mortennobel/cpp-cheatsheet
    $ find . -type f | wc -l
    30
    ```

2.  Объем всех файлов
    ```shell
    $ find . -type f -exec du -h {} + >'/Users/daniilsamsonov/cpp-cheatsheet/3.txt'
    Ответ в файле 3.txt в репозитории
    ```

3.  Объем исходного кода: cpp, c, h, hpp, cxx, py, pl, php, java, cs, rb, rs, hs
    ```shell
    $ cloc /Users/daniilsamsonov/cpp-cheatsheet
       3 text files.
       2 unique files.                              
       3 files ignored.

    github.com/AlDanial/cloc v 2.00  T=0.01 s (176.0 files/s, 97343.4 lines/s)
    -------------------------------------------------------------------------------
    Language                     files          blank        comment           code
    -------------------------------------------------------------------------------
    Markdown                         1             76              0            500
    C++                              1             80             69            381
    -------------------------------------------------------------------------------
    SUM:                             2            156             69            881
    -------------------------------------------------------------------------------
    ```

4.  Найти, если есть файл .clang-format
    ```shell
    $ find . -type f -name "*.clang-format" | wc -l
    0
    ```

5.  Если есть каталог src, то общее количество файлов в каталоге src
    ```shell
    $ [ ! -d "/src/" ] && echo "no such directory"
    no such directory
    ```

6.  Выписать количество файлов, содержащих слово socket независимо от написания строчными или прописными буквами во всех файлах репозитория.
    ```shell
    $ find . -type f  -iname "*socket*" | wc -l
    0
    ```

7.  Выписать количество файлов, содержащих слово select независимо от написания строчными или прописными буквами во всех файлах репозитория.
    ```shell
    $ find . -type f  -iname "*select*" | wc -l
    0
    ```

8.  Выписать количество раз, сколько, содержится слово Microsoft, Google или Intel независимо от написания строчными или прописными буквами во всех файлах репозитория.
    ```shell
    $ find /home/vboxuser/WhiteSunOfSpace/workspace/folly -type f -exec grep -iEo 'microsoft|google|intel' {} + | wc -l
    grep: /home/vboxuser/WhiteSunOfSpace/workspace/folly/.git/index: binary file matches
    0
    ```

9.  Найти расположение файла LICENSE относительно начала репозитория.
    ```shell
    $ find $(pwd) -name "LICENSE*"
    ```

10. Вывести строку для файла LICENSE (если он есть), содержащую следующие подпоследовательности символов: BSD, GNU, MIT, APSL, Apache, GPL, AGPL, LGPL
    ```shell
    Файла LICENSE нет
    ```
