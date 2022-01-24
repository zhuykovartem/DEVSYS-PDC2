[artem@fedora DEVSYS-PDC2]$ mkdir branching

[artem@fedora DEVSYS-PDC2]$ mcedit merge.sh



[artem@fedora DEVSYS-PDC2]$ ll

итого 12

drwxrwxr-x. 1 artem artem 124 янв 18 10:18 01-intro-01

drwxrwxr-x. 1 artem artem  30 янв 18 10:18 03-sysadmin-06-net

drwxrwxr-x. 1 artem artem   0 янв 24 14:20 branching

-rw-rw-r--. 1 artem artem  18 янв 24 14:19 has_been_moved.txt

-rw-rw-r--. 1 artem artem 253 янв 24 14:19 README.md

drwxrwxr-x. 1 artem artem  20 янв 18 10:18 terraform

-rw-rw-r--. 1 artem artem  18 янв 18 10:18 will_be_moved

[artem@fedora DEVSYS-PDC2]$ mcedit branching/merge.sh



[artem@fedora DEVSYS-PDC2]$ mcedit branching/rebase.sh



[artem@fedora DEVSYS-PDC2]$ git commit -m "prepare for merge and rebase"

На ветке main

Ваша ветка обновлена в соответствии с «github/main».



Неотслеживаемые файлы:

  (используйте «git add <файл>…», чтобы добавить в то, что будет включено в коммит)

    branching/



ничего не добавлено в коммит, но есть неотслеживаемые файлы (используйте «git add», чтобы отслеживать их)

[artem@fedora DEVSYS-PDC2]$ git add branching/

[artem@fedora DEVSYS-PDC2]$ git push

Everything up-to-date

[artem@fedora DEVSYS-PDC2]$ git status

На ветке main

Ваша ветка обновлена в соответствии с «github/main».



Изменения, которые будут включены в коммит:

  (используйте «git restore --staged <файл>…», чтобы убрать из индекса)

    новый файл:    branching/merge.sh

    новый файл:    branching/rebase.sh



[artem@fedora DEVSYS-PDC2]$ git push github main

Everything up-to-date

[artem@fedora DEVSYS-PDC2]$ git commit -m "prepare for merge and rebase"

[main 5b15837] prepare for merge and rebase

 2 files changed, 16 insertions(+)

 create mode 100644 branching/merge.sh

 create mode 100644 branching/rebase.sh

[artem@fedora DEVSYS-PDC2]$ git push github main

Перечисление объектов: 5, готово.

Подсчет объектов: 100% (5/5), готово.

При сжатии изменений используется до 2 потоков

Сжатие объектов: 100% (4/4), готово.

Запись объектов: 100% (4/4), 455 байтов | 227.00 КиБ/с, готово.

Всего 4 (изменений 1), повторно использовано 0 (изменений 0), повторно использовано пакетов 0

remote: Resolving deltas: 100% (1/1), completed with 1 local object.

To github.com:zhuykovartem/DEVSYS-PDC2.git

   6605d75..5b15837  main -> main

[artem@fedora DEVSYS-PDC2]$ git switch -c git-merge

Переключено на новую ветку «git-merge»

[artem@fedora DEVSYS-PDC2]$ ll

итого 12

drwxrwxr-x. 1 artem artem 124 янв 18 10:18 01-intro-01

drwxrwxr-x. 1 artem artem  30 янв 18 10:18 03-sysadmin-06-net

drwxrwxr-x. 1 artem artem  34 янв 24 14:23 branching

-rw-rw-r--. 1 artem artem  18 янв 24 14:19 has_been_moved.txt

-rw-rw-r--. 1 artem artem 253 янв 24 14:19 README.md

drwxrwxr-x. 1 artem artem  20 янв 18 10:18 terraform

-rw-rw-r--. 1 artem artem  18 янв 18 10:18 will_be_moved

[artem@fedora DEVSYS-PDC2]$ mcedit branching/merge.sh 



[artem@fedora DEVSYS-PDC2]$ git commit -m "merge: @ instead *"

На ветке git-merge

Изменения, которые не в индексе для коммита:

  (используйте «git add <файл>…», чтобы добавить файл в индекс)

  (используйте «git restore <файл>…», чтобы отменить изменения в рабочем каталоге)

    изменено:      branching/merge.sh



нет изменений добавленных для коммита

(используйте «git add» и/или «git commit -a»)

[artem@fedora DEVSYS-PDC2]$ git add branching/merge.sh 

[artem@fedora DEVSYS-PDC2]$ git commit -m "merge: @ instead *"

[git-merge e1c0acd] merge: @ instead *

 1 file changed, 2 insertions(+), 2 deletions(-)

[artem@fedora DEVSYS-PDC2]$ git push

fatal: Текущая ветка git-merge не имеет вышестоящей ветки.

Чтобы отправить текущую ветку и установить внешнюю ветку как вышестоящую для этой ветки, используйте



    git push --set-upstream origin git-merge



[artem@fedora DEVSYS-PDC2]$ git checkout main

Переключено на ветку «main»

Ваша ветка обновлена в соответствии с «github/main».

[artem@fedora DEVSYS-PDC2]$ git push

Everything up-to-date

[artem@fedora DEVSYS-PDC2]$ git checkout git-merge 

Переключено на ветку «git-merge»

[artem@fedora DEVSYS-PDC2]$ git commit -a -m "merge: @ instead *"

На ветке git-merge

нечего коммитить, нет изменений в рабочем каталоге

[artem@fedora DEVSYS-PDC2]$ mcedit branching/merge.sh 



[artem@fedora DEVSYS-PDC2]$ git commit -a -m "merge: use shift"

[git-merge 9482ec8] merge: use shift

 1 file changed, 3 insertions(+), 2 deletions(-)

[artem@fedora DEVSYS-PDC2]$ git checkout main

Переключено на ветку «main»

Ваша ветка обновлена в соответствии с «github/main».

[artem@fedora DEVSYS-PDC2]$ mcedit branching/rebase.sh 



[artem@fedora DEVSYS-PDC2]$ mcedit branching/rebase.sh 



[artem@fedora DEVSYS-PDC2]$ git commit -a

Отмена коммита из-за пустого сообщения коммита.

[artem@fedora DEVSYS-PDC2]$ git commit -a -m " "

Отмена коммита из-за пустого сообщения коммита.

[artem@fedora DEVSYS-PDC2]$ git commit -a -m "rebase-test"

[main 6eddf00] rebase-test

 1 file changed, 5 insertions(+), 3 deletions(-)

[artem@fedora DEVSYS-PDC2]$ git log --all --grep='prepare for merge and rebase'

commit 5b158374eac5dd0d5bbb6d62216d66357c714442 (github/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:30:56 2022 +0500



    prepare for merge and rebase

[artem@fedora DEVSYS-PDC2]$ git checkout 5b158374eac5dd0d5bbb6d62216d66357c714442

Note: switching to '5b158374eac5dd0d5bbb6d62216d66357c714442'.



You are in 'detached HEAD' state. You can look around, make experimental

changes and commit them, and you can discard any commits you make in this

state without impacting any branches by switching back to a branch.



If you want to create a new branch to retain commits you create, you may

do so (now or later) by using -c with the switch command. Example:



  git switch -c <new-branch-name>



Or undo this operation with:



  git switch -



Turn off this advice by setting config variable advice.detachedHead to false



HEAD сейчас на 5b15837 prepare for merge and rebase

[artem@fedora DEVSYS-PDC2]$ git branch git-rebase 5b158374eac5dd0d5bbb6d62216d66357c714442

[artem@fedora DEVSYS-PDC2]$ git checkout git-rebase 

Переключено на ветку «git-rebase»

[artem@fedora DEVSYS-PDC2]$ mcedit branching/rebase.sh 



[artem@fedora DEVSYS-PDC2]$ git commit -a -m "git-rebase 1"

[git-rebase 7587318] git-rebase 1

 1 file changed, 5 insertions(+), 3 deletions(-)

[artem@fedora DEVSYS-PDC2]$ mcedit branching/rebase.sh 



[artem@fedora DEVSYS-PDC2]$ git commit -a -m "git-rebase 2"

[git-rebase bccbe52] git-rebase 2

 1 file changed, 1 insertion(+), 1 deletion(-)

[artem@fedora DEVSYS-PDC2]$ git push

fatal: Текущая ветка git-rebase не имеет вышестоящей ветки.

Чтобы отправить текущую ветку и установить внешнюю ветку как вышестоящую для этой ветки, используйте



    git push --set-upstream origin git-rebase



[artem@fedora DEVSYS-PDC2]$ git checkout main

Переключено на ветку «main»

Ваша ветка опережает «github/main» на 1 коммит.

  (используйте «git push», чтобы опубликовать ваши локальные коммиты)

[artem@fedora DEVSYS-PDC2]$ git push

Перечисление объектов: 7, готово.

Подсчет объектов: 100% (7/7), готово.

При сжатии изменений используется до 2 потоков

Сжатие объектов: 100% (4/4), готово.

Запись объектов: 100% (4/4), 391 байт | 55.00 КиБ/с, готово.

Всего 4 (изменений 2), повторно использовано 0 (изменений 0), повторно использовано пакетов 0

remote: Resolving deltas: 100% (2/2), completed with 2 local objects.

To github.com:zhuykovartem/DEVSYS-PDC2.git

   5b15837..6eddf00  main -> main

[artem@fedora DEVSYS-PDC2]$ git log

commit 6eddf006804da2b79b0adc73b08a7ad069d9b8d1 (HEAD -> main, github/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:48:36 2022 +0500



    rebase-test



commit 5b158374eac5dd0d5bbb6d62216d66357c714442

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:30:56 2022 +0500



    prepare for merge and rebase



commit 6605d75804f2473686ef1751acd3229105b5c9aa (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:40:29 2022 +0500



    Moved and deleted



commit 20c82d2ce5c324ff199aa4454fd059715b4badab

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:25:35 2022 +0500



:

















































commit 6eddf006804da2b79b0adc73b08a7ad069d9b8d1 (HEAD -> main, github/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:48:36 2022 +0500



    rebase-test



commit 5b158374eac5dd0d5bbb6d62216d66357c714442

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:30:56 2022 +0500



    prepare for merge and rebase



commit 6605d75804f2473686ef1751acd3229105b5c9aa (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:40:29 2022 +0500



    Moved and deleted



commit 20c82d2ce5c324ff199aa4454fd059715b4badab

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:25:35 2022 +0500

:



















































commit 6eddf006804da2b79b0adc73b08a7ad069d9b8d1 (HEAD -> main, github/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:48:36 2022 +0500



    rebase-test



commit 5b158374eac5dd0d5bbb6d62216d66357c714442

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:30:56 2022 +0500



    prepare for merge and rebase



commit 6605d75804f2473686ef1751acd3229105b5c9aa (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:40:29 2022 +0500



    Moved and deleted



commit 20c82d2ce5c324ff199aa4454fd059715b4badab

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:25:35 2022 +0500



:...skipping...

commit 6eddf006804da2b79b0adc73b08a7ad069d9b8d1 (HEAD -> main, github/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:48:36 2022 +0500



    rebase-test



commit 5b158374eac5dd0d5bbb6d62216d66357c714442

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:30:56 2022 +0500



    prepare for merge and rebase



commit 6605d75804f2473686ef1751acd3229105b5c9aa (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:40:29 2022 +0500



    Moved and deleted



commit 20c82d2ce5c324ff199aa4454fd059715b4badab

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:25:35 2022 +0500



    Prepare to delete and move



commit fc358927d8205c3f75cd4b97da5071ddeda1b3a1

:...skipping...

commit 6eddf006804da2b79b0adc73b08a7ad069d9b8d1 (HEAD -> main, github/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:48:36 2022 +0500



    rebase-test



commit 5b158374eac5dd0d5bbb6d62216d66357c714442

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:30:56 2022 +0500



    prepare for merge and rebase



commit 6605d75804f2473686ef1751acd3229105b5c9aa (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:40:29 2022 +0500



    Moved and deleted



commit 20c82d2ce5c324ff199aa4454fd059715b4badab

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:25:35 2022 +0500



    Prepare to delete and move



commit fc358927d8205c3f75cd4b97da5071ddeda1b3a1

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:21:04 2022 +0500

:



























































commit 6eddf006804da2b79b0adc73b08a7ad069d9b8d1 (HEAD -> main, github/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:48:36 2022 +0500



    rebase-test



commit 5b158374eac5dd0d5bbb6d62216d66357c714442

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:30:56 2022 +0500



    prepare for merge and rebase



commit 6605d75804f2473686ef1751acd3229105b5c9aa (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:40:29 2022 +0500



    Moved and deleted



commit 20c82d2ce5c324ff199aa4454fd059715b4badab

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:25:35 2022 +0500



    Prepare to delete and move



commit fc358927d8205c3f75cd4b97da5071ddeda1b3a1

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:21:04 2022 +0500

:

























































commit 6eddf006804da2b79b0adc73b08a7ad069d9b8d1 (HEAD -> main, github/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:48:36 2022 +0500



    rebase-test



commit 5b158374eac5dd0d5bbb6d62216d66357c714442

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:30:56 2022 +0500



    prepare for merge and rebase



commit 6605d75804f2473686ef1751acd3229105b5c9aa (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:40:29 2022 +0500



    Moved and deleted



commit 20c82d2ce5c324ff199aa4454fd059715b4badab

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:25:35 2022 +0500



    Prepare to delete and move



commit fc358927d8205c3f75cd4b97da5071ddeda1b3a1

Author: Artem <zhuykov.artem@gmail.com>

:

























































commit 6eddf006804da2b79b0adc73b08a7ad069d9b8d1 (HEAD -> main, github/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:48:36 2022 +0500



    rebase-test



commit 5b158374eac5dd0d5bbb6d62216d66357c714442

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:30:56 2022 +0500



    prepare for merge and rebase



commit 6605d75804f2473686ef1751acd3229105b5c9aa (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:40:29 2022 +0500



    Moved and deleted



commit 20c82d2ce5c324ff199aa4454fd059715b4badab

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:25:35 2022 +0500



    Prepare to delete and move



commit fc358927d8205c3f75cd4b97da5071ddeda1b3a1

Author: Artem <zhuykov.artem@gmail.com>

:

























































commit 6eddf006804da2b79b0adc73b08a7ad069d9b8d1 (HEAD -> main, github/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:48:36 2022 +0500



    rebase-test



commit 5b158374eac5dd0d5bbb6d62216d66357c714442

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:30:56 2022 +0500



    prepare for merge and rebase



commit 6605d75804f2473686ef1751acd3229105b5c9aa (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:40:29 2022 +0500



    Moved and deleted



commit 20c82d2ce5c324ff199aa4454fd059715b4badab

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:25:35 2022 +0500



    Prepare to delete and move



commit fc358927d8205c3f75cd4b97da5071ddeda1b3a1

Author: Artem <zhuykov.artem@gmail.com>

:























































commit 6eddf006804da2b79b0adc73b08a7ad069d9b8d1 (HEAD -> main, github/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:48:36 2022 +0500



    rebase-test



commit 5b158374eac5dd0d5bbb6d62216d66357c714442

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:30:56 2022 +0500



    prepare for merge and rebase



commit 6605d75804f2473686ef1751acd3229105b5c9aa (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:40:29 2022 +0500



    Moved and deleted



commit 20c82d2ce5c324ff199aa4454fd059715b4badab

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:25:35 2022 +0500



    Prepare to delete and move



commit fc358927d8205c3f75cd4b97da5071ddeda1b3a1

:



















































commit 6eddf006804da2b79b0adc73b08a7ad069d9b8d1 (HEAD -> main, github/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:48:36 2022 +0500



    rebase-test



commit 5b158374eac5dd0d5bbb6d62216d66357c714442

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:30:56 2022 +0500



    prepare for merge and rebase



commit 6605d75804f2473686ef1751acd3229105b5c9aa (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:40:29 2022 +0500



    Moved and deleted



commit 20c82d2ce5c324ff199aa4454fd059715b4badab

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:25:35 2022 +0500



    Prepare to delete and move

:



















































commit 6eddf006804da2b79b0adc73b08a7ad069d9b8d1 (HEAD -> main, github/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:48:36 2022 +0500



    rebase-test



commit 5b158374eac5dd0d5bbb6d62216d66357c714442

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:30:56 2022 +0500



    prepare for merge and rebase



commit 6605d75804f2473686ef1751acd3229105b5c9aa (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:40:29 2022 +0500



    Moved and deleted



commit 20c82d2ce5c324ff199aa4454fd059715b4badab

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:25:35 2022 +0500



    Prepare to delete and move

:

















































commit 6eddf006804da2b79b0adc73b08a7ad069d9b8d1 (HEAD -> main, github/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:48:36 2022 +0500



    rebase-test



commit 5b158374eac5dd0d5bbb6d62216d66357c714442

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:30:56 2022 +0500



    prepare for merge and rebase



commit 6605d75804f2473686ef1751acd3229105b5c9aa (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:40:29 2022 +0500



    Moved and deleted



commit 20c82d2ce5c324ff199aa4454fd059715b4badab

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:25:35 2022 +0500



    Prepare to delete and move

:

















































commit 6eddf006804da2b79b0adc73b08a7ad069d9b8d1 (HEAD -> main, github/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:48:36 2022 +0500



    rebase-test



commit 5b158374eac5dd0d5bbb6d62216d66357c714442

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:30:56 2022 +0500



    prepare for merge and rebase



commit 6605d75804f2473686ef1751acd3229105b5c9aa (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:40:29 2022 +0500



    Moved and deleted



commit 20c82d2ce5c324ff199aa4454fd059715b4badab

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:25:35 2022 +0500



    Prepare to delete and move

:















































commit 6eddf006804da2b79b0adc73b08a7ad069d9b8d1 (HEAD -> main, github/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:48:36 2022 +0500



    rebase-test



commit 5b158374eac5dd0d5bbb6d62216d66357c714442

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:30:56 2022 +0500



    prepare for merge and rebase



commit 6605d75804f2473686ef1751acd3229105b5c9aa (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:40:29 2022 +0500



    Moved and deleted



commit 20c82d2ce5c324ff199aa4454fd059715b4badab

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:25:35 2022 +0500



:















































commit 6eddf006804da2b79b0adc73b08a7ad069d9b8d1 (HEAD -> main, github/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:48:36 2022 +0500



    rebase-test



commit 5b158374eac5dd0d5bbb6d62216d66357c714442

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:30:56 2022 +0500



    prepare for merge and rebase



commit 6605d75804f2473686ef1751acd3229105b5c9aa (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:40:29 2022 +0500



    Moved and deleted



commit 20c82d2ce5c324ff199aa4454fd059715b4badab

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:25:35 2022 +0500



:















































commit 6eddf006804da2b79b0adc73b08a7ad069d9b8d1 (HEAD -> main, github/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:48:36 2022 +0500



    rebase-test



commit 5b158374eac5dd0d5bbb6d62216d66357c714442

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:30:56 2022 +0500



    prepare for merge and rebase



commit 6605d75804f2473686ef1751acd3229105b5c9aa (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:40:29 2022 +0500



    Moved and deleted



commit 20c82d2ce5c324ff199aa4454fd059715b4badab

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:25:35 2022 +0500



:















































commit 6eddf006804da2b79b0adc73b08a7ad069d9b8d1 (HEAD -> main, github/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:48:36 2022 +0500



    rebase-test



commit 5b158374eac5dd0d5bbb6d62216d66357c714442

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:30:56 2022 +0500



    prepare for merge and rebase



commit 6605d75804f2473686ef1751acd3229105b5c9aa (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:40:29 2022 +0500



    Moved and deleted



commit 20c82d2ce5c324ff199aa4454fd059715b4badab

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:25:35 2022 +0500



:















































commit 6eddf006804da2b79b0adc73b08a7ad069d9b8d1 (HEAD -> main, github/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:48:36 2022 +0500



    rebase-test



commit 5b158374eac5dd0d5bbb6d62216d66357c714442

Author: Artem <zhuykov.artem@gmail.com>

Date:   Mon Jan 24 14:30:56 2022 +0500



    prepare for merge and rebase



commit 6605d75804f2473686ef1751acd3229105b5c9aa (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main)

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:40:29 2022 +0500



    Moved and deleted



commit 20c82d2ce5c324ff199aa4454fd059715b4badab

Author: Artem <zhuykov.artem@gmail.com>

Date:   Tue Jan 11 21:25:35 2022 +0500



[artem@fedora DEVSYS-PDC2]$ git status

На ветке main

Ваша ветка обновлена в соответствии с «github/main».



нечего коммитить, нет изменений в рабочем каталоге

[artem@fedora DEVSYS-PDC2]$ git checkout git-rebase 

Переключено на ветку «git-rebase»

[artem@fedora DEVSYS-PDC2]$ git checkout main

Переключено на ветку «main»

Ваша ветка обновлена в соответствии с «github/main».

[artem@fedora DEVSYS-PDC2]$ git push -u github git-merge 

Перечисление объектов: 11, готово.

Подсчет объектов: 100% (11/11), готово.

При сжатии изменений используется до 2 потоков

Сжатие объектов: 100% (8/8), готово.

Запись объектов: 100% (8/8), 818 байтов | 163.00 КиБ/с, готово.

Всего 8 (изменений 3), повторно использовано 0 (изменений 0), повторно использовано пакетов 0

remote: Resolving deltas: 100% (3/3), completed with 2 local objects.

remote: 

remote: Create a pull request for 'git-merge' on GitHub by visiting:

remote:      https://github.com/zhuykovartem/DEVSYS-PDC2/pull/new/git-merge

remote: 

To github.com:zhuykovartem/DEVSYS-PDC2.git

 * [new branch]      git-merge -> git-merge

Ветка «git-merge» отслеживает внешнюю ветку «git-merge» из «github».

[artem@fedora DEVSYS-PDC2]$ git push -u github git-rebase 

Перечисление объектов: 11, готово.

Подсчет объектов: 100% (11/11), готово.

При сжатии изменений используется до 2 потоков

Сжатие объектов: 100% (8/8), готово.

Запись объектов: 100% (8/8), 777 байтов | 77.00 КиБ/с, готово.

Всего 8 (изменений 3), повторно использовано 0 (изменений 0), повторно использовано пакетов 0

remote: Resolving deltas: 100% (3/3), completed with 1 local object.

remote: 

remote: Create a pull request for 'git-rebase' on GitHub by visiting:

remote:      https://github.com/zhuykovartem/DEVSYS-PDC2/pull/new/git-rebase

remote: 

To github.com:zhuykovartem/DEVSYS-PDC2.git

 * [new branch]      git-rebase -> git-rebase

Ветка «git-rebase» отслеживает внешнюю ветку «git-rebase» из «github».

[artem@fedora DEVSYS-PDC2]$ git merge git-merge 

Merge made by the 'recursive' strategy.

 branching/merge.sh | 5 +++--

 1 file changed, 3 insertions(+), 2 deletions(-)

[artem@fedora DEVSYS-PDC2]$ git push

Перечисление объектов: 7, готово.

Подсчет объектов: 100% (7/7), готово.

При сжатии изменений используется до 2 потоков

Сжатие объектов: 100% (3/3), готово.

Запись объектов: 100% (3/3), 363 байта | 72.00 КиБ/с, готово.

Всего 3 (изменений 1), повторно использовано 0 (изменений 0), повторно использовано пакетов 0

remote: Resolving deltas: 100% (1/1), completed with 1 local object.

To github.com:zhuykovartem/DEVSYS-PDC2.git

   6eddf00..fd4688d  main -> main

[artem@fedora DEVSYS-PDC2]$ git checkout git-rebase 

Переключено на ветку «git-rebase»

Ваша ветка обновлена в соответствии с «github/git-rebase».

[artem@fedora DEVSYS-PDC2]$ git rebase -i main

error: could not parse 'pick'

error: неправильная строка 2: fixup pick bccbe52 git-rebase 2

Вы можете исправить это с помощью «git rebase --edit-todo», а потом запустив «git rebase --continue».

Или вы можете прервать процесс перемещения, выполнив «git rebase --abort»

[artem@fedora DEVSYS-PDC2]$ git rebase --edit-todo

error: could not parse 'pick'

error: неправильная строка 2: fixup pick bccbe52 git-rebase 2

error: could not parse 'pick'

error: неправильная строка 2: fixup pick bccbe52 git-rebase 2

Вы можете исправить это с помощью «git rebase --edit-todo», а потом запустив «git rebase --continue».

Или вы можете прервать процесс перемещения, выполнив «git rebase --abort»

[artem@fedora DEVSYS-PDC2]$ git rebase --edit-todo

error: could not parse 'pick'

error: неправильная строка 2: fixup pick bccbe52 git-rebase 2

error: could not parse 'pick'

error: неправильная строка 1: fixup pick bccbe52 git-rebase 2

Вы можете исправить это с помощью «git rebase --edit-todo», а потом запустив «git rebase --continue».

Или вы можете прервать процесс перемещения, выполнив «git rebase --abort»

[artem@fedora DEVSYS-PDC2]$ mcedit branching/rebase.sh 



[artem@fedora DEVSYS-PDC2]$ git log --graph --all

*   commit fd4688dbd1972935036e33572d275806aac0fdf1 (HEAD, github/main, main)

|\  Merge: 6eddf00 9482ec8

| | Author: Artem <zhuykov.artem@gmail.com>

| | Date:   Mon Jan 24 15:22:41 2022 +0500

| | 

| |     Merge branch 'git-merge'

| | 

| * commit 9482ec82bb66355208ff6bf1dd09833c125b84ce (github/git-merge, git-merge)

| | Author: Artem <zhuykov.artem@gmail.com>

| | Date:   Mon Jan 24 14:42:02 2022 +0500

| | 

| |     merge: use shift

| | 

| * commit e1c0acd906eb5c1e608e9571c306a33e1668fad1

| | Author: Artem <zhuykov.artem@gmail.com>

| | Date:   Mon Jan 24 14:36:37 2022 +0500

| | 

| |     merge: @ instead *

| | 

* | commit 6eddf006804da2b79b0adc73b08a7ad069d9b8d1

|/  Author: Artem <zhuykov.artem@gmail.com>

[artem@fedora DEVSYS-PDC2]$ git branch

* (no branch, rebasing git-rebase)

  fix

  git-merge

  git-rebase

  main

[artem@fedora DEVSYS-PDC2]$ git rebase --edit-todo

error: could not parse 'pick'

error: неправильная строка 1: fixup pick bccbe52 git-rebase 2

[artem@fedora DEVSYS-PDC2]$ git rebase --edit-todo

[artem@fedora DEVSYS-PDC2]$ mcedit branching/rebase.sh 

[artem@fedora DEVSYS-PDC2]$ git rebase --edit-todo

[artem@fedora DEVSYS-PDC2]$ git rebase -i main

fatal: It seems that there is already a rebase-merge directory, and

I wonder if you are in the middle of another rebase.  If that is the

case, please try

    git rebase (--continue | --abort | --skip)

If that is not the case, please

    rm -fr ".git/rebase-merge"

and run me again.  I am stopping in case you still have something

valuable there.

[artem@fedora DEVSYS-PDC2]$ git rebase --edit-todo

[artem@fedora DEVSYS-PDC2]$ git reflog

fd4688d (HEAD, github/main, main) HEAD@{0}: rebase (start): checkout main

bccbe52 (github/git-rebase, git-rebase) HEAD@{1}: checkout: moving from main to git-rebase

fd4688d (HEAD, github/main, main) HEAD@{2}: merge git-merge: Merge made by the 'recursive' strategy.

6eddf00 HEAD@{3}: checkout: moving from git-rebase to main

bccbe52 (github/git-rebase, git-rebase) HEAD@{4}: checkout: moving from main to git-rebase

6eddf00 HEAD@{5}: checkout: moving from git-rebase to main

bccbe52 (github/git-rebase, git-rebase) HEAD@{6}: commit: git-rebase 2

7587318 HEAD@{7}: commit: git-rebase 1

5b15837 HEAD@{8}: checkout: moving from 5b158374eac5dd0d5bbb6d62216d66357c714442 to git-rebase

5b15837 HEAD@{9}: checkout: moving from main to 5b158374eac5dd0d5bbb6d62216d66357c714442

6eddf00 HEAD@{10}: commit: rebase-test

5b15837 HEAD@{11}: checkout: moving from git-merge to main

9482ec8 (github/git-merge, git-merge) HEAD@{12}: commit: merge: use shift

e1c0acd HEAD@{13}: checkout: moving from main to git-merge

5b15837 HEAD@{14}: checkout: moving from git-merge to main

e1c0acd HEAD@{15}: commit: merge: @ instead *

5b15837 HEAD@{16}: checkout: moving from main to git-merge

5b15837 HEAD@{17}: commit: prepare for merge and rebase

6605d75 (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main) HEAD@{18}: checkout: moving from fix to main

79709f1 (github/fix, fix) HEAD@{19}: commit: New stroke

20c82d2 HEAD@{20}: checkout: moving from 20c82d2ce5c324ff199aa4454fd059715b4badab to fix

:...skipping...

fd4688d (HEAD, github/main, main) HEAD@{0}: rebase (start): checkout main

bccbe52 (github/git-rebase, git-rebase) HEAD@{1}: checkout: moving from main to git-rebase

fd4688d (HEAD, github/main, main) HEAD@{2}: merge git-merge: Merge made by the 'recursive' strategy.

6eddf00 HEAD@{3}: checkout: moving from git-rebase to main

bccbe52 (github/git-rebase, git-rebase) HEAD@{4}: checkout: moving from main to git-rebase

6eddf00 HEAD@{5}: checkout: moving from git-rebase to main

bccbe52 (github/git-rebase, git-rebase) HEAD@{6}: commit: git-rebase 2

7587318 HEAD@{7}: commit: git-rebase 1

5b15837 HEAD@{8}: checkout: moving from 5b158374eac5dd0d5bbb6d62216d66357c714442 to git-rebase

5b15837 HEAD@{9}: checkout: moving from main to 5b158374eac5dd0d5bbb6d62216d66357c714442

6eddf00 HEAD@{10}: commit: rebase-test

5b15837 HEAD@{11}: checkout: moving from git-merge to main

9482ec8 (github/git-merge, git-merge) HEAD@{12}: commit: merge: use shift

e1c0acd HEAD@{13}: checkout: moving from main to git-merge

5b15837 HEAD@{14}: checkout: moving from git-merge to main

e1c0acd HEAD@{15}: commit: merge: @ instead *

5b15837 HEAD@{16}: checkout: moving from main to git-merge

5b15837 HEAD@{17}: commit: prepare for merge and rebase

6605d75 (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main) HEAD@{18}: checkout: moving from fix to main

79709f1 (github/fix, fix) HEAD@{19}: commit: New stroke

20c82d2 HEAD@{20}: checkout: moving from 20c82d2ce5c324ff199aa4454fd059715b4badab to fix

20c82d2 HEAD@{21}: checkout: moving from main to 20c82d2ce5c324ff199aa4454fd059715b4badab

:...skipping...

fd4688d (HEAD, github/main, main) HEAD@{0}: rebase (start): checkout main

bccbe52 (github/git-rebase, git-rebase) HEAD@{1}: checkout: moving from main to git-rebase

fd4688d (HEAD, github/main, main) HEAD@{2}: merge git-merge: Merge made by the 'recursive' strategy.

6eddf00 HEAD@{3}: checkout: moving from git-rebase to main

bccbe52 (github/git-rebase, git-rebase) HEAD@{4}: checkout: moving from main to git-rebase

6eddf00 HEAD@{5}: checkout: moving from git-rebase to main

bccbe52 (github/git-rebase, git-rebase) HEAD@{6}: commit: git-rebase 2

7587318 HEAD@{7}: commit: git-rebase 1

5b15837 HEAD@{8}: checkout: moving from 5b158374eac5dd0d5bbb6d62216d66357c714442 to git-rebase

5b15837 HEAD@{9}: checkout: moving from main to 5b158374eac5dd0d5bbb6d62216d66357c714442

6eddf00 HEAD@{10}: commit: rebase-test

5b15837 HEAD@{11}: checkout: moving from git-merge to main

9482ec8 (github/git-merge, git-merge) HEAD@{12}: commit: merge: use shift

e1c0acd HEAD@{13}: checkout: moving from main to git-merge

5b15837 HEAD@{14}: checkout: moving from git-merge to main

e1c0acd HEAD@{15}: commit: merge: @ instead *

5b15837 HEAD@{16}: checkout: moving from main to git-merge

5b15837 HEAD@{17}: commit: prepare for merge and rebase

6605d75 (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main) HEAD@{18}: checkout: moving from fix to main

79709f1 (github/fix, fix) HEAD@{19}: commit: New stroke

20c82d2 HEAD@{20}: checkout: moving from 20c82d2ce5c324ff199aa4454fd059715b4badab to fix

20c82d2 HEAD@{21}: checkout: moving from main to 20c82d2ce5c324ff199aa4454fd059715b4badab

6605d75 (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main) HEAD@{22}: checkout: moving from main to main

:...skipping...

fd4688d (HEAD, github/main, main) HEAD@{0}: rebase (start): checkout main

bccbe52 (github/git-rebase, git-rebase) HEAD@{1}: checkout: moving from main to git-rebase

fd4688d (HEAD, github/main, main) HEAD@{2}: merge git-merge: Merge made by the 'recursive' strategy.

6eddf00 HEAD@{3}: checkout: moving from git-rebase to main

bccbe52 (github/git-rebase, git-rebase) HEAD@{4}: checkout: moving from main to git-rebase

6eddf00 HEAD@{5}: checkout: moving from git-rebase to main

bccbe52 (github/git-rebase, git-rebase) HEAD@{6}: commit: git-rebase 2

7587318 HEAD@{7}: commit: git-rebase 1

5b15837 HEAD@{8}: checkout: moving from 5b158374eac5dd0d5bbb6d62216d66357c714442 to git-rebase

5b15837 HEAD@{9}: checkout: moving from main to 5b158374eac5dd0d5bbb6d62216d66357c714442

6eddf00 HEAD@{10}: commit: rebase-test

5b15837 HEAD@{11}: checkout: moving from git-merge to main

9482ec8 (github/git-merge, git-merge) HEAD@{12}: commit: merge: use shift

e1c0acd HEAD@{13}: checkout: moving from main to git-merge

5b15837 HEAD@{14}: checkout: moving from git-merge to main

e1c0acd HEAD@{15}: commit: merge: @ instead *

5b15837 HEAD@{16}: checkout: moving from main to git-merge

5b15837 HEAD@{17}: commit: prepare for merge and rebase

6605d75 (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main) HEAD@{18}: checkout: moving from fix to main

79709f1 (github/fix, fix) HEAD@{19}: commit: New stroke

20c82d2 HEAD@{20}: checkout: moving from 20c82d2ce5c324ff199aa4454fd059715b4badab to fix

20c82d2 HEAD@{21}: checkout: moving from main to 20c82d2ce5c324ff199aa4454fd059715b4badab

6605d75 (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main) HEAD@{22}: checkout: moving from main to main

6605d75 (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main) HEAD@{23}: clone: from https://github.com/zhuykovar:...skipping...

fd4688d (HEAD, github/main, main) HEAD@{0}: rebase (start): checkout main

bccbe52 (github/git-rebase, git-rebase) HEAD@{1}: checkout: moving from main to git-rebase

fd4688d (HEAD, github/main, main) HEAD@{2}: merge git-merge: Merge made by the 'recursive' strategy.

6eddf00 HEAD@{3}: checkout: moving from git-rebase to main

bccbe52 (github/git-rebase, git-rebase) HEAD@{4}: checkout: moving from main to git-rebase

6eddf00 HEAD@{5}: checkout: moving from git-rebase to main

bccbe52 (github/git-rebase, git-rebase) HEAD@{6}: commit: git-rebase 2

7587318 HEAD@{7}: commit: git-rebase 1

5b15837 HEAD@{8}: checkout: moving from 5b158374eac5dd0d5bbb6d62216d66357c714442 to git-rebase

5b15837 HEAD@{9}: checkout: moving from main to 5b158374eac5dd0d5bbb6d62216d66357c714442

6eddf00 HEAD@{10}: commit: rebase-test

5b15837 HEAD@{11}: checkout: moving from git-merge to main

9482ec8 (github/git-merge, git-merge) HEAD@{12}: commit: merge: use shift

e1c0acd HEAD@{13}: checkout: moving from main to git-merge

5b15837 HEAD@{14}: checkout: moving from git-merge to main

e1c0acd HEAD@{15}: commit: merge: @ instead *

5b15837 HEAD@{16}: checkout: moving from main to git-merge

5b15837 HEAD@{17}: commit: prepare for merge and rebase

6605d75 (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main) HEAD@{18}: checkout: moving from fix to main

79709f1 (github/fix, fix) HEAD@{19}: commit: New stroke

20c82d2 HEAD@{20}: checkout: moving from 20c82d2ce5c324ff199aa4454fd059715b4badab to fix

20c82d2 HEAD@{21}: checkout: moving from main to 20c82d2ce5c324ff199aa4454fd059715b4badab

6605d75 (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main) HEAD@{22}: checkout: moving from main to main

6605d75 (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main) HEAD@{23}: clone: from https://github.com/zhuykovartem/DEVSYS-PDC2.git

:...skipping...

fd4688d (HEAD, github/main, main) HEAD@{0}: rebase (start): checkout main

bccbe52 (github/git-rebase, git-rebase) HEAD@{1}: checkout: moving from main to git-rebase

fd4688d (HEAD, github/main, main) HEAD@{2}: merge git-merge: Merge made by the 'recursive' strategy.

6eddf00 HEAD@{3}: checkout: moving from git-rebase to main

bccbe52 (github/git-rebase, git-rebase) HEAD@{4}: checkout: moving from main to git-rebase

6eddf00 HEAD@{5}: checkout: moving from git-rebase to main

bccbe52 (github/git-rebase, git-rebase) HEAD@{6}: commit: git-rebase 2

7587318 HEAD@{7}: commit: git-rebase 1

5b15837 HEAD@{8}: checkout: moving from 5b158374eac5dd0d5bbb6d62216d66357c714442 to git-rebase

5b15837 HEAD@{9}: checkout: moving from main to 5b158374eac5dd0d5bbb6d62216d66357c714442

6eddf00 HEAD@{10}: commit: rebase-test

5b15837 HEAD@{11}: checkout: moving from git-merge to main

9482ec8 (github/git-merge, git-merge) HEAD@{12}: commit: merge: use shift

e1c0acd HEAD@{13}: checkout: moving from main to git-merge

5b15837 HEAD@{14}: checkout: moving from git-merge to main

e1c0acd HEAD@{15}: commit: merge: @ instead *

5b15837 HEAD@{16}: checkout: moving from main to git-merge

5b15837 HEAD@{17}: commit: prepare for merge and rebase

6605d75 (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main) HEAD@{18}: checkout: moving from fix to main

79709f1 (github/fix, fix) HEAD@{19}: commit: New stroke

20c82d2 HEAD@{20}: checkout: moving from 20c82d2ce5c324ff199aa4454fd059715b4badab to fix

20c82d2 HEAD@{21}: checkout: moving from main to 20c82d2ce5c324ff199aa4454fd059715b4badab

6605d75 (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main) HEAD@{22}: checkout: moving from main to main

6605d75 (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main) HEAD@{23}: clone: from https://github.com/zhuykovartem/DEVSYS-PDC2.git

~

(END)...skipping...

fd4688d (HEAD, github/main, main) HEAD@{0}: rebase (start): checkout main

bccbe52 (github/git-rebase, git-rebase) HEAD@{1}: checkout: moving from main to git-rebase

fd4688d (HEAD, github/main, main) HEAD@{2}: merge git-merge: Merge made by the 'recursive' strategy.

6eddf00 HEAD@{3}: checkout: moving from git-rebase to main

bccbe52 (github/git-rebase, git-rebase) HEAD@{4}: checkout: moving from main to git-rebase

6eddf00 HEAD@{5}: checkout: moving from git-rebase to main

bccbe52 (github/git-rebase, git-rebase) HEAD@{6}: commit: git-rebase 2

7587318 HEAD@{7}: commit: git-rebase 1

5b15837 HEAD@{8}: checkout: moving from 5b158374eac5dd0d5bbb6d62216d66357c714442 to git-rebase

5b15837 HEAD@{9}: checkout: moving from main to 5b158374eac5dd0d5bbb6d62216d66357c714442

6eddf00 HEAD@{10}: commit: rebase-test

5b15837 HEAD@{11}: checkout: moving from git-merge to main

9482ec8 (github/git-merge, git-merge) HEAD@{12}: commit: merge: use shift

e1c0acd HEAD@{13}: checkout: moving from main to git-merge

5b15837 HEAD@{14}: checkout: moving from git-merge to main

e1c0acd HEAD@{15}: commit: merge: @ instead *

5b15837 HEAD@{16}: checkout: moving from main to git-merge

5b15837 HEAD@{17}: commit: prepare for merge and rebase

6605d75 (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main) HEAD@{18}: checkout: moving from fix to main

79709f1 (github/fix, fix) HEAD@{19}: commit: New stroke

20c82d2 HEAD@{20}: checkout: moving from 20c82d2ce5c324ff199aa4454fd059715b4badab to fix

20c82d2 HEAD@{21}: checkout: moving from main to 20c82d2ce5c324ff199aa4454fd059715b4badab

6605d75 (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main) HEAD@{22}: checkout: moving from main to main

6605d75 (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main) HEAD@{23}: clone: from https://github.com/zhuykovartem/DEVSYS-PDC2.git

~

~

(END)...skipping...

fd4688d (HEAD, github/main, main) HEAD@{0}: rebase (start): checkout main

bccbe52 (github/git-rebase, git-rebase) HEAD@{1}: checkout: moving from main to git-rebase

fd4688d (HEAD, github/main, main) HEAD@{2}: merge git-merge: Merge made by the 'recursive' strategy.

6eddf00 HEAD@{3}: checkout: moving from git-rebase to main

bccbe52 (github/git-rebase, git-rebase) HEAD@{4}: checkout: moving from main to git-rebase

6eddf00 HEAD@{5}: checkout: moving from git-rebase to main

bccbe52 (github/git-rebase, git-rebase) HEAD@{6}: commit: git-rebase 2

7587318 HEAD@{7}: commit: git-rebase 1

5b15837 HEAD@{8}: checkout: moving from 5b158374eac5dd0d5bbb6d62216d66357c714442 to git-rebase

5b15837 HEAD@{9}: checkout: moving from main to 5b158374eac5dd0d5bbb6d62216d66357c714442

6eddf00 HEAD@{10}: commit: rebase-test

5b15837 HEAD@{11}: checkout: moving from git-merge to main

9482ec8 (github/git-merge, git-merge) HEAD@{12}: commit: merge: use shift

e1c0acd HEAD@{13}: checkout: moving from main to git-merge

5b15837 HEAD@{14}: checkout: moving from git-merge to main

e1c0acd HEAD@{15}: commit: merge: @ instead *

5b15837 HEAD@{16}: checkout: moving from main to git-merge

5b15837 HEAD@{17}: commit: prepare for merge and rebase

6605d75 (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main) HEAD@{18}: checkout: moving from fix to main

79709f1 (github/fix, fix) HEAD@{19}: commit: New stroke

20c82d2 HEAD@{20}: checkout: moving from 20c82d2ce5c324ff199aa4454fd059715b4badab to fix

20c82d2 HEAD@{21}: checkout: moving from main to 20c82d2ce5c324ff199aa4454fd059715b4badab

6605d75 (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main) HEAD@{22}: checkout: moving from main to main

6605d75 (tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab-ssh/main, bitbucket-ssh/main) HEAD@{23}: clone: from https://github.com/zhuykovartem/DEVSYS-PDC2.git

~

~

~

[artem@fedora DEVSYS-PDC2]$ git branch backup

[artem@fedora DEVSYS-PDC2]$ git reset --hard HEAD@{2}

HEAD сейчас на fd4688d Merge branch 'git-merge'

[artem@fedora DEVSYS-PDC2]$ git branch -D backup

Ветка backup удалена (была fd4688d).

[artem@fedora DEVSYS-PDC2]$ git branch

* (no branch, rebasing git-rebase)

  fix

  git-merge

  git-rebase

  main

[artem@fedora DEVSYS-PDC2]$ git checkout git-rebase 

Предыдущая позиция HEAD была fd4688d Merge branch 'git-merge'

Переключено на ветку «git-rebase»

Ваша ветка обновлена в соответствии с «github/git-rebase».

[artem@fedora DEVSYS-PDC2]$ git rebase -i main

fatal: It seems that there is already a rebase-merge directory, and

I wonder if you are in the middle of another rebase.  If that is the

case, please try

    git rebase (--continue | --abort | --skip)

If that is not the case, please

    rm -fr ".git/rebase-merge"

and run me again.  I am stopping in case you still have something

valuable there.



[artem@fedora DEVSYS-PDC2]$ git rebase --abort

[artem@fedora DEVSYS-PDC2]$ git branch

  fix

  git-merge

* git-rebase

  main

[artem@fedora DEVSYS-PDC2]$ git rebase -i main

Автослияние branching/rebase.sh

КОНФЛИКТ (содержимое): Конфликт слияния в branching/rebase.sh

error: не удалось применить коммит 7587318… git-rebase 1

Resolve all conflicts manually, mark them as resolved with

"git add/rm <conflicted_files>", then run "git rebase --continue".

You can instead skip this commit: run "git rebase --skip".

To abort and get back to the state before "git rebase", run "git rebase --abort".

Could not apply 7587318... git-rebase 1

[artem@fedora DEVSYS-PDC2]$ mcedit branching/rebase.sh 



[artem@fedora DEVSYS-PDC2]$ git add branching/rebase.sh 

[artem@fedora DEVSYS-PDC2]$ git rebase --continue

Автослияние branching/rebase.sh

КОНФЛИКТ (содержимое): Конфликт слияния в branching/rebase.sh

error: не удалось применить коммит bccbe52… git-rebase 2

Resolve all conflicts manually, mark them as resolved with

"git add/rm <conflicted_files>", then run "git rebase --continue".

You can instead skip this commit: run "git rebase --skip".

To abort and get back to the state before "git rebase", run "git rebase --abort".

Could not apply bccbe52... git-rebase 2

[artem@fedora DEVSYS-PDC2]$ mcedit branching/rebase.sh 



[artem@fedora DEVSYS-PDC2]$ git add branching/rebase.sh 

[artem@fedora DEVSYS-PDC2]$ git rebase --continue

[отделённый HEAD 8a5928b] Merge branch 'git-merge'

 Date: Mon Jan 24 15:22:41 2022 +0500

Successfully rebased and updated refs/heads/git-rebase.

[artem@fedora DEVSYS-PDC2]$ git push

To github.com:zhuykovartem/DEVSYS-PDC2.git

 ! [rejected]        git-rebase -> git-rebase (non-fast-forward)

error: не удалось отправить некоторые ссылки в «github.com:zhuykovartem/DEVSYS-PDC2.git»

подсказка: Обновления были отклонены, так как верхушка вашей текущей ветки

подсказка: позади ее внешней части. Заберите и слейте внешние изменения 

подсказка: (например, с помощью «git pull …») перед повторной попыткой отправки

подсказка: изменений.

подсказка: Для дополнительной информации, смотрите «Note about fast-forwards»

подсказка: в «git push --help».

[artem@fedora DEVSYS-PDC2]$ git push -u github git-rebase -f

Перечисление объектов: 10, готово.

Подсчет объектов: 100% (10/10), готово.

При сжатии изменений используется до 2 потоков

Сжатие объектов: 100% (4/4), готово.

Запись объектов: 100% (4/4), 432 байта | 216.00 КиБ/с, готово.

Всего 4 (изменений 2), повторно использовано 0 (изменений 0), повторно использовано пакетов 0

remote: Resolving deltas: 100% (2/2), completed with 2 local objects.

To github.com:zhuykovartem/DEVSYS-PDC2.git

 + bccbe52...8a5928b git-rebase -> git-rebase (forced update)

Ветка «git-rebase» отслеживает внешнюю ветку «git-rebase» из «github».

[artem@fedora DEVSYS-PDC2]$ git checkout main

Переключено на ветку «main»

Ваша ветка обновлена в соответствии с «github/main».

[artem@fedora DEVSYS-PDC2]$ git merge git-rebase 

Merge made by the 'recursive' strategy.

 branching/rebase.sh | 2 +-

 1 file changed, 1 insertion(+), 1 deletion(-)

[artem@fedora DEVSYS-PDC2]$ git push

Перечисление объектов: 1, готово.

Подсчет объектов: 100% (1/1), готово.

Запись объектов: 100% (1/1), 226 байтов | 56.00 КиБ/с, готово.

Всего 1 (изменений 0), повторно использовано 0 (изменений 0), повторно использовано пакетов 0

To github.com:zhuykovartem/DEVSYS-PDC2.git

   fd4688d..8469b36  main -> main

