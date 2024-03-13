## 30 комманд

1. Создал учетную запись
2. Создал локальный репозиторий:
    ```
    git init
    ```
3. Создал пустой текстовый документ в папке:
   
   ![](/photoes/create_txt.png)
4. Добавил первый абзац в текстовый документ:
  ```
  git add privet.txt
  ```
  ![](/photoes/first_add.png)
  
  Закоммитил:
  ```
  git commit -m "1 paragraph"
  ```
  ![](/photoes/first_commit.png)
  
  и так повторил 5 раз:
  
  ![](/photoes/second_paragraph.png)
    
  ![](/photoes/third_paragraph.png)
    
  ![](/photoes/fourth_paragraph.png)
    
  ![](/photoes/fifth_paragraph.png)
    
5. Просмотрел статус текущего репозитория:
    ```
    git status
    ```
    ![](/photoes/git_status.png)
6. Добавил еще один файл:

    ![](/photoes/create_txt2.png)
8. Создал коммит:
    ```
    git commit -m "txt"
    ```
    ![](/photoes/git_commit2.png)
9. Посмотрел протокол коммитов:
    ```
    git log
    ```
    ![](/photoes/git_log.png)
10. Посмотрел изменения в файле по сравнению с последним коммитом:
    ```
    git diff HEAD~1 kaktak.txt
    ```
     ![](/photoes/git_diff.png)
11. Убрал изменения относительно последнего коммита из файла:
    ```
    git checkout -- kaktak.txt
    ```
12. Посмотрел существующие ветки:
    ```
    git branch
    ```
    ![](/photoes/git_branch.png)
13. Создал новую ветку:
    ```
    git branch test1
    ```
14. Переключился на новую ветку:
    ```
    git checkout test1
    ```
    ![](/photoes/git_checkout_test1.png)
15. Создал новую ветку и сразу же переключилися на нее:
    ```
    git checkout -b test2
    ```
    ![](/photoes/git_checkout_test2.png)
16. Удалил ветку:
    ```
    git branch -d test1
    ```
    ![](/photoes/git_branch_delete_test1.png)
17. Добавил merge изменения из указанной ветки в текущую:
    ```
    git checkout test2
    git merge master
    ```
    ![](/photoes/git_merge1.png)
19. Создал конфликт:
    Переключился на ветку master
    ```
    git checkout master
    ```
    Изменил файл privet.txt стерев все и добавил текст: "new text"
    Добавил и закоммитил
      
      ```
      git add privet.txt
      git commit -m "new text"
      ```
      ![](/photoes/git_conflict1.png)

    Переключился на ветку test2
    ```
    git checkout master
    ```
    Изменил файл privet.txt стерев все и добавил текст: "new text2"
    Добавил и закоммитил
    
      ```
      git add privet.txt
      git commit -m "new text2"
      ```
      ![](/photoes/git_conflict2.png)
    Переключился на ветку master и попытался выполнить merge:
      
      ```
      git checkout master
      git merge test2
      ```
      ![](/photoes/git_conflict3.png)
21. Посмотрел в каких файлах есть конфликты:
    ```
    git status
    ```
    ![](/photoes/git_status2.png)
22. Устранил конфликт:
    Выбрал текст, который хочу оставить в документе privet.txt, удалил разметку Git
    Добавил и закоммитил
      
      ```
      git add privet.txt
      git commit -m "remove conflict"
      ```
      ![](/photoes/remove_conflict.png)
19. Переключился на указанный коммит:
    ```
    git checkout 1d3e8bf
    ```
    ![](/photoes/switch_to_commit.png)
18. Сделал rebase текущей ветки:
    ```
    git rebase master
    ```
18. Удалил ветку:
    ```
    git branch -d test2
    ```
19. Пропустил текущий конфликтный коммит и перешел к следующему:
    ```
    git rebase --skip
    ```
    ![](/photoes/rebase_skip.png)
20. Отправил изменения из локального репозитория для указанной ветки в удаленный (дистанционный):
    ```
    git remote add origin https://github.com/atom196/30command.git
    git branch -M main
    git push -u origin main
    ```
21. Забрал изменения из репозитория, для которого были созданы удаленные ветки по умолчанию:
    ```
    git pull origin main
    ```
22. Забрал изменения удаленной ветки из репозитория основной ветки по умолчанию:
    
23. Клонировал репозиторий:
    ```
    git clone https://github.com/atom196/30command.git
    ```
