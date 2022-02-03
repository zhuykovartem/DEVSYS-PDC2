<ol>
<li><pre>sudo apt install virtualbox</pre></li>
<li><pre>sudo apt install vagrant</pre></li>
<li><pre>Готово</pre></li>
<li><pre>
mkdir /home/artem/vagrant
cd /home/artem/vagrant/
vagrant init
mcedit Vagrantfile
vagrant up
</pre></li>
<li><pre>
Оперативаная память: 1Гб
Процессор: 2 ядра
Жесткий диск: Виртуальный 64Гб, реальный 1,73Гб
Видеопамять: 4Мб
Сеть: Intel PRO/1000MT Desktop (NAT)
</pre></li>
<li><b>mcedit /home/artem/vagrant/Vagrantfile</b>
  <pre>
config.vm.provider "virtualbox" do |vb|
    # объем оперативной памяти
    vb.memory = 2048
    # количество ядер процессора
    vb.cpus = 4
end
</pre></li>
<li><b>vagrant ssh</b>
<pre>vagrant@vagrant:~$ lsb_release -a
No LSB modules are available.
Distributor ID: Ubuntu
Description:    Ubuntu 20.04.3 LTS
Release:        20.04
Codename:       focal
vagrant@vagrant:~$ exit</pre>
</li>
<li><pre>HISTFILESIZE - максимальное число строк в файле истории для сохранения, Cтрока 817<br> 
HISTSIZE - число команд для сохранения Cтрока 833
Директива ignoreboth это объединение параметров ignoredups и ignorespace, отвечающих за отключение записи дубликатов строк в историю и отключение записи строк начанающихся с пробела.
</li>
<li><b>{} - вариант списка выполняемого в среде текущего командного интерпретатора. Строка 228</b>
  <pre>
 { list; }
              list is simply executed in the current shell environment.  list must be terminated with  a  newline  or
              semicolon.  This is known as a group command.  The return status is the exit status of list.  Note that
              unlike the metacharacters ( and ), { and } are reserved words and must occur where a reserved  word  is
              permitted  to be recognized.  Since they do not cause a word break, they must be separated from list by
              whitespace or another shell metacharacter. </pre>
 </li>
<li>
<pre>vagrant@vagrant:~$ touch {1..100000}.txt<br>  
vagrant@vagrant:~$ touch {1..300000}.txt<br>
-bash: /usr/bin/touch: Argument list too long<br>  
vagrant@vagrant:~$ getconf ARG_MAX  <br>
2097152  </pre></li> 
<li><pre>[[ выражение ]]  
Возвращает статус 0 или 1 в зависимости от значения указанного условного выражения -d файл  
Истинно, если файл существует и является каталогом.  
[[-d /tmp]] - возвращает True если каталог существует.</pre></li>
<li><pre>vagrant@vagrant:~$ type -a bash
bash is /usr/bin/bash
bash is /bin/bash
vagrant@vagrant:~$ mkdir  /tmp/new_path_directory
vagrant@vagrant:~$ cp /bin/bash /tmp/new_path_directory/
vagrant@vagrant:~$ PATH=/tmp/new_path_directory/:$PATH
vagrant@vagrant:~$ type -a bash
bash is /tmp/new_path_directory/bash
bash is /usr/bin/bash
bash is /bin/bash</pre></li>
<li><pre>
Команда at - команда запускается в указанное время (в параметре)
Команда batch - запускается когда уровень загрузки системы снизится ниже 1.5.
</pre></li>
<li><pre>vagrant halt</pre></li>
  </ol>
