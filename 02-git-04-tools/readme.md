1. <b>git show -s aefea</b> 

     <pre> aefead220<br>
      Update CHANGELOG.md</pre>

2. <b>git show -s --oneline 85024d3</b>
     <pre>  85024d310 (tag: v0.12.23) v0.12.23</pre>

3. <b>git show --pretty=format:' %P' b8d720</b>
      <pre> 56cd7859e05c36c06b56d013b55a252d0bb7e158 9ea88f22fc6269854151c571162c5bcf958bee2b</pre>

4. <b>git log --oneline v0.12.23..v0.12.24</b>  
 <pre>
      33ff1c03b (tag: v0.12.24) v0.12.24<br>
      b14b74c49 [Website] vmc provider links<br>
      3f235065b Update CHANGELOG.md<br>
      6ae64e247 registry: Fix panic when server is unreachable<br>
      5c619ca1b website: Remove links to the getting started guide's old location<br>
      06275647e Update CHANGELOG.md<br>
      d5f9411f5 command: Fix bug when using terraform login on Windows<br>
      4b6d06cc5 Update CHANGELOG.md<br>
      dd01a3507 Update CHANGELOG.md<br>
      225466bc3 Cleanup after v0.12.23 release<br>
</pre>
5. <b>git log -S 'func providerSource(' --oneline</b>
 <pre>
8c928e835 main: Consult local directories as potential mirrors of providers
</pre>
6. <b>git grep 'func globalPluginDirs'</b>
   <pre>plugins.go<font color="#2AA1B3">:</font><font color="#C01C28"><b>func globalPluginDirs</b></font>() []string {</pre>
   
   <b>git log -L :globalPluginDirs:plugins.go -s --oneline</b>
<pre>
78b122055 Remove config.go and update things using its aliases<br>

52dbf9483 keep .terraform.d/plugins for discovery<br>

41ab0aef7 Add missing OS_ARCH dir to global plugin paths<br>

66ebff90c move some more plugin search path logic to command<br>

8364383c3 Push plugin discovery down into command package<br>
</pre>

7. <b>git log -S 'func synchronizedWriters' --pretty=format:'%h - %an %cd'</b>
<pre>
bdfea50cc - James Bardin Wed Dec 2 13:59:18 2020 -0500<br>

5ac311e2a - Martin Atkins Thu May 4 15:36:51 2017 -0700<br>
Ответ Martin Atkins потому что дата создания коммита раньше чем у James Bardin
</pre>

