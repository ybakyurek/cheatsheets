# GIT



- **untracked (izlenmeyen):** GIT tarafından henüz takip edilmeyen, yani yeni oluşturulmuş dosyaları ifade eder.
- **unstaged (hazırlanmamış):** Güncellenmiş ancak *commit*’lenmek için hazırlanmamış dosyaları ifade eder.
- **staged (hazırlanmış):** *Commit*’lenmeye hazır olan dosyaları ifade eder.
- **deleted (silinmiş):** Projeden silinmiş ama GIT üzerinden kaldırılmamış dosyaları ifade eder.

### config

```bash
$ git config --global user.name "Name Surname"
$ git config --global user.email "test@email.com"
$ git config --list //ayarlarin butunu
```

### rm

```bash
'dosyanin untracked (izlenmeyen) hale getirilmesi 
$ git rm  --cached <dosya veya klasor_name>
```

dosyayi silme islemi

```bash
$ git rm <dosya veya klasor_name>
```

### init:

```bash
git init //kodu baslatma
```

### add

```bash
git add <file name> // file selection
git add . //selection all file
```

### commit

```bash
git commit -m "comment"
'son commit uzerinde degisiklik
git commit —amend -m “master2-Bu amend ile eklendi”
```

### revert

```bash
'commit’i geri alir. geri alinan commit’i tekrar geri alirsak eski haline gelir ama o islemin id’si farkli olacak.
git revert <commit id>
```

### reset

```bash
'bu sayede bunun sonrasindaki butun commitler yok edilir. ve en son commitin bu commit’in oldugu hale gelir. bundan eski commitler kalir. 
git reset -hard <commitId>
git reset —hard 9c953cf3cfacaa8da86f6ac36cba3ef68272dad3
```

### diff

```bash
'Repository üzerinde yapılan değişikliklerden sonra dosyalar arasında oluşan farklılıkları göterir.
'Çalışma dizini ile repository (HEAD) arasındaki farklılıkları görmek için:
$ git diff HEAD
'commitler arasi farki verir
git diff <commitId>..<commitId> [file(optional)]
git diff 3ea814cdc3eb266c7fa1378b78c2423286057a33..ae09d983aa8af1d891b7aea1d500000e225da841 index.md
'aradaki tum farklari gosterir
git diff 3ea814cdc3eb266c7fa1378b78c2423286057a33..ae09d983aa8af1d891b7aea1d500000e225da841
'Çalışma dizini ve staged ortamı arasındaki farkları görmek için:
$ git diff --staged
```

### log

```bash
'commit kayitlari ve ayrintilari
git log
'son commiti getirir. 1 2 3 dedikce o kadar son olani getirir
git log -n 1
```

### status

```bash
git status
```

### branch

```bash
'Yeni branch ekleme
$ git branch <branch_name>
'Tüm uzak ve yerel branchlari listelemek için;
$ git branch -a
'branch silme
$ git branch -d <branch_name>
```

### checkout

```bash
'varolan branche gitme
$ git checkout <branch_name>
'yeni bir branch olusturup ona gecmek
$ git checkout -b <branch_name>
'commitler arasi gecis yapmak
$ git checkout <commit_ID>
```

### merge

```bash
'baska bir branchle birlestirmek istedigimizde
$ git merge <branch_name>
```

### clone

```bash
'Mevcut bir Remote Repositoryde bulunan dosyaların bilgisayarımızda bir kopyasının oluşturulmasını sağlar.
$ git clone <remote_URL>
```

### push

```bash
'repositorye gonderme. Burada bahsi geçen origin remote repository’nin kök dizinini belirtir ve sabit bir isimdir. master ise sizin çalıştığınız branch (dal)’ı belirtir.'
$ git push origin master
```

### remote

```bash
$ git remote add origin http://uzak_deponun_adresi.git
```
