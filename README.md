- 👋 Hi, I’m william @w62
- 👀 I’m interested in Rust and Operating Systems
- 🌱 I’m currently learning Rust
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me Twitter [@\_w62\_](https://twitter.com/_w62_)

<!---
w62/w62 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->



<!---
[dev-guides](https://cs4118.github.io/dev-guides/)

[OSTEP](https://pages.cs.wisc.edu/~remzi/OSTEP/)
[make-kpkg is (being) retired](https://unix.stackexchange.com/questions/238469/difference-between-make-kpkg-and-make-deb-pkg)
--->


```
bash PS1
export PS1='\[\033[1;34m\]\n\D{}\n[VM \u@\H:$(pwd)]\n:P > \[\033[00m\]'

zsh PS1
export PS1=$'\n%n@%m %T %D{%H:%M %a %d-%b-%Y %Z} %d\n> '

```

Booting an ARM kernel quickly with qemu:

```
qemu-system-aarch64 -machine virt -cpu cortex-a57 -machine \ 
type=virt -nographic -smp 2 -m 4096 \ 
-kernel /boot/<kernel-image>
```

Note: it seems that Ubunut supplied kernels refused to boot in this way. 

https://kasiviswanathanblog.wordpress.com/2020/05/03/arm64-vanilla-kernel-in-qemu/  
  
  
sudo dnf install gcc flex make bison bc openssl openssl-devel elfutils-libelf-devel perl dwarves zstd

Some kernel compilation issues:

Q: make[3]: *** No rule to make target 'debian/certs/benh@debian.org.cert.pem', needed by 'certs/x509_certificate_list'.  Stop.

A: `sed -ri '/CONFIG_SYSTEM_TRUSTED_KEYS/s/=.+/=""/g' .config `

Q: BTF: .tmp_vmlinux.btf: pahole (pahole) is not available

A: `sudo apt install dwarves`

Q: usr/bin/ld: scripts/dtc/dtc-parser.tab.o:(.bss+0x10): multiple definition of 'yylloc'; scripts/dtc/dtc-lexer.lex.o:(.bss+0x0): first defined here

A: Remove YYLTYPE yylloc; in scripts/dtc/dtc-lexer.l

+++ b/scripts/dtc/dtc-lexer.l
@@ -38,7 +38,6 @@ LINECOMMENT	"//".*\n
 #include "srcpos.h"
 #include "dtc-parser.tab.h"
 
-YYLTYPE yylloc;
 extern bool treesource_error;

https://github.com/BPI-SINOVOIP/BPI-M4-bsp/issues/4

https://stackoverflow.com/questions/61657707/btf-tmp-vmlinux-btf-pahole-pahole-is-not-available


minimum qemu command line to boot a kernel

```
 qemu-system-aarch64 -nographic -machine virt -m 512M -cpu max -smp 4  -kernel arch/arm64/boot/Image.gz
 
 ```
