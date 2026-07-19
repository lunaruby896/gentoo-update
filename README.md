como instalar ?

use esse comando: chmod +x ~/gentoo-update-main/script-install

ou

chmod +x ~/Downloads/gentoo-update-main/script-install

você tem que executar o script de instalação !

~/gentoo-update-main/script-install

ou 

~/Downloads/gentoo-update-main/script-install

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Solução de Erros: Chaves GnuPG e Permissões no Gentoo (Pacotes Binários)

se caso ocorreu quando você colocou o comando: "sudo gentoo-update", ocorreu esses erros que estão em baixo

❌ *gpg: failed to create temporary file '/etc/portage/gnupg/...': Permission denied*

❌ *gpg: Can't check signature: No public key*

❌ *Binary package is not usable (verification failed)*

1 Entre como root no sistema

sudo su -

2 Remova a pasta de chaves antiga que está com problemas

rm -rf /etc/portage/gnupg

3 Peça para o Portage reconstruir a pasta com as permissões nativas perfeitas

emerge --config sys-apps/portage

4 Inicialize e baixe as chaves oficiais semanais da equipe do Gentoo

getuto
