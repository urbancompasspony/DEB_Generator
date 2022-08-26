# DEB_Generator
# Version 1.2

-----------------------------------------------------

# Gerador de Pacotes .DEB 1.2 #
Desenvolvido por NathanDrake

-----------------------------------------------------

Conteúdo:

- Arquivo Controle: Control
- Atalho de Desktop: Bonobo
- Script Gerador do Pacote .deb
- Script Gerador do Atalho: Shortcut
- Este LEIA ME

-----------------------------------------------------

Dependencias:
- Python 3
- Wine-Stable
- Plugins Utilizados pelo Python:

os
sys
time
tkinter
datetime
fileinput

-----------------------------------------------------

-------------------- Preparando ---------------------

Utilize a pasta onde encontra-se este LEIA-ME como raíz.
Reúna o seguinte material aqui dentro:

- icon.png: ícone do jogo em formato .png
- wineprefix: pasta com o jogo instalado
- wine-version: pasta com o Wine utilizado pelo jogo
- postinst: Caso este exista

- Apague a pasta DOSDEVICES e todos os 5 Links Simbolicos em .../drive_c/users/nathandrake do Wineprefix!

------------------- Modo de Usar --------------------

Execute o script Gerador
Preencha os campos conforme necessário.
Esteja ciente que:

> DEB NAME - Nome do pacote deb com a versão do pacote no nome.
Exemplo: bnb-gtasa-1.0.0

> WINE Prefix - Nome do prefixo do jogo.
Exemplo: bnb-gtasa

> WINE Version - Nome da versão do Wine
Exemplo: bnb-gtasa-2.7

> Size in Bytes - Tamanho do pacote instalado em Bytes!
Exemplo: 4GB => 4194304

> Package Description - Descrição do pacote, quando ele é aberto no GDEBI.
Um texto não muito longo com até 3 linhas é o ideal.
A string aqui é reconhecida por completo e inserida no arquivo CONTROL

> Desktop Name - Nome do atalho quando ele for criado no Desktop!
Exemplo: GTA San Andreas

> Dir Root - Diretório raíz do jogo depois de C:/Program Files/.
Dê o caminho semi-completo.
Exemplo: Grand Theft Auto San Andreas
Não feche a barra, como em /Rockstar Games/.
O programa fechará essas barras inicial e final.

> Soft Exec - É o executável do game no Wine.
Exemplo: gta_sa.exe

> Post-Inst - Define se o script existe ou não.
Se não houver um PostInst a ser inserido, preencha com 0.
Se houver, preencha com 1.
Caso deixe em branco o valor default é 0.

> SUDO - Ponha sua senha de usuário root para mudar as permissões 
do arquivo CONTROL e/ou do postinst. Ela é usada somente no script.

> BOTÃO GERAR RAÍZ - Gera a pasta game-1.0.0 e deixa-a preparada para
ser revisada e posteriormente empacotada em formato .deb.

> BOTÃO GERAR DEB - Pega a pasta game-1.0.0 e fecha em formato .deb.

Uma vez preenchido, pressione Gerar Raíz.
Uma pasta será gerada. Verifique se está tudo Ok dentro dela.
Quando estiver pronto, aperte Gerar Deb.
O processo demora! Depois, um arquivo .deb surgirá dentro desta pasta.
