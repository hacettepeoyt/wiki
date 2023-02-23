Git, orijinal olarak Linus Torvalds tarafından yazılmış bir versiyon kontrol programıdır. Bir versiyon kontrol programı olarak git, yazılımcıların programların kaynak kodları üzerinde yaptıkları değişikliklerin kayıtlarını tutar. Bu sayede yazılımcıların kaynak kodlarının geçmişteki herhangi bir hâlini görmeleri ve bu kayıtları birleştirerek birden fazla yazılımcının projelerde birbirinden bağımsız bir şekilde çalışabilmesi gibi özellikler sağlar.

Git'teki ana çalışma birimi **commit**'lerdir. Commit'ler kaynak kodda yapılmış herhangi bir değişikliği simgeler. Commit'ler birbirine zincir gibi bağlıdır ve her commit'in bir veya birden fazla üst/parent commit'i bulunur. Her commit'in kendine özel bir id'si bulunur, bu id kısa veya uzun şekilde hexadecimal olarak (`85a9207920037d0e9e9cfe019a909b8bddb565ca`/`85a92079`) gösterilir. Bu commit zincirlerine **branch** denir. Branch'lar kaynak koda herhangi bir özellik eklemek için veya hata çözmek için kullanılabilir. Branch'lar işleri bittiklerinde genellikle tekrar ana branch ile birleştirilir. Yeni sürüm yayımlamak için branch'tan ziyade **tag** denilen etiketler kullanılır. Bir proje için bütün bu branch, commit, tag vs.'leri saklayan git birimine **repository/repo** denir.

# Kullanım

Git kullanırken commit oluşturmak için tek seferlik git'e bir isim ve e-posta vermeniz gerekmektedir. Bunu bütün repo'lar için: (`--global` argümanına dikkat edin)

```
git config --global user.name <Kullanıcı İsmi>
git config --global user.email <E-posta>
```

veya tek bir repo için(`--local` argümanı varsayılan olduğu için belirtmeseniz de olur):

```
git config --local user.name <Kullanıcı İsmi>
git config --local user.email <E-posta>
```

şeklinde belirtebilirsiniz. Eğer GitHub/Gitlab/Gitea gibi bir sistem kullanıyorsanız, sistemdeki kullanıcı adı ve özellikle GitHub için sistemde verilen e-posta'yı kullanmanız tavsiye edilir. Onun dışında `git config` komutuna ikinci argümanı vermeyip argümanın değerini de görebilirsiniz (`git config user.name` gibi). Genel olarak `git config` komutu git'in nasıl davranmasını belirtmek istediğiniz ayarları yapmanızı sağlar. Mesela Windows ve Linux karışık development yapıyorsanız `core.eol`, `core.autocrlf` gibi ayarlar ile git'in satır sonlarını standardize etmesini sağlayabilirsiniz. Daha fazla bilgi için `git config --help` komutunu kullanabilirsiniz.

Sıfırdan bir proje için git repository'si oluşturacaksanız proje dizinine girip `git init` komutunu kullanabilirsiniz. Bu şekilde repository oluşturduğunuz repo'yu online bir sunucuya bağlamak istiyorsanız:

```
git remote add <Kaynak ismi> <URL>
```

komutunu kullanabilirsiniz. Kaynak ismi olarak genelde origin kullanılır, birden fazla sunucu ile uğraşmıyorsanız origin olarak bırakmanız tavsiye edilir. Var olan bir sunucunun adresini değiştirmek istiyorsanız `git remote set-url <kaynak> <url>` komutunu kullanabilirsiniz.

Var olan bir repo'yu bilgisayarınıza çekmek istiyorsanız:

```
git clone <URL>
```

komutunu kullanabilirsiniz. `git clone` komutu dizin olarak URL'in sonunda belirtilen ismi seçer. İkinci bir argüman olarak hangi dizine çekmek istediğinizi belirtebilirsiniz. `git clone` komutu çoğunlukla her proje için sadece bir kere kullanılır.
