Поместить эту строчку в `vim ~/.bashrc` для дуфолтного терминал или `vim ~/.zshrc` для iTerm:

`(echo "your_password" | sudo -S purge); clear; cd Desktop`

sudo -S purge - очищает ненужные процессы.

