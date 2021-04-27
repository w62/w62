- 👋 Hi, I’m @w62
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
w62/w62 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
[Compile Vanilla kernel on Ubunutu](https://veithen.io/2013/12/19/ubuntu-vanilla-kernel.html)

`sed -ri '/CONFIG_SYSTEM_TRUSTED_KEYS/s/=.+/=""/g' .config `

[dev-guides](https://cs4118.github.io/dev-guides/)

[OSTEP](https://pages.cs.wisc.edu/~remzi/OSTEP/)
[make-kpkg is (being) retired](https://unix.stackexchange.com/questions/238469/difference-between-make-kpkg-and-make-deb-pkg)

sudo dnf install gcc flex make bison bc openssl openssl-devel elfutils-libelf-devel perl dwarves zstd

https://linuxconfig.org/how-to-install-configure-and-use-mutt-with-a-gmail-account-on-linux
~/.muttrc

set ssl_force_tls = yes
set abort_nosubject = no
set mail_check = 60
set timeout = 10
set sort = "reverse-date-received"
set signature = "~/.mutt/signature"
set copy = no
set from = "foo.bar@gmail.com"
set realname = "Foo Bar"

# Imap settings
set imap_user = "foo.bar@gmail.com"
set imap_pass = "<mutt-app-specific-password>"

# Smtp settings
set smtp_url = "smtps://foo.bar@smtp.gmail.com"
set smtp_pass = "<mutt-app-specific-password>"

# Remote gmail folders
set folder = "imaps://imap.gmail.com/"
set spoolfile = "+INBOX"
set postponed = "+[Gmail]/Drafts"
set record = "+[Gmail]/Sent Mail"
set trash = "+[Gmail]/Trash"
