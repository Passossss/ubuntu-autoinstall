Arquivo de configuração de autoinstall do Ubuntu

Este é um arquivo de exemplo, que pode ser usado como referência para suas próprias instalações.
Na senha use o comando :
mkpasswd (sua senha)

somente assim o linux identificará e criptografará sua senha e voce insere no campo
password: ''

Use o URL do arquivo no Instalador do Ubuntu
Criar um ISO personalizado (alternativa)

    Baixe o ISO oficial do Ubuntu.
    Extraia-o para uma pasta de sua preferência.
    Coloque o arquivo autoinstall.yaml na raiz da pasta do Ubuntu extraído.
    Em seguida, use o seguinte comando para criar o ISO:

xorriso -as mkisofs -r -V "Nome da Imagem" -o ../nome_do_seu_iso_personalizado.iso -J -l -b boot/grub/i386-pc/eltorito.img -c boot.catalog -no-emul-boot -boot-load-size 4 -boot-info-table pasta-com-os-arquivos-do-iso-do-ubuntu/

Para usar os comandos acima, certifique-se de ter instalado xorriso e mkisofs em seu sistema.

Variáveis no comando acima:

    "Nome da Imagem": É o nome que você deseja que apareça no gerenciador de arquivos. Em resumo, é o rótulo do ISO.
    ../nome_do_seu_iso_personalizado.iso: É o nome e o caminho (para ser salvo) do seu ISO personalizado.
    pasta-com-os-arquivos-do-iso-do-ubuntu/: Caminho para a pasta contendo os arquivos do ISO do Ubuntu que você extraiu no passo 2.

Onde encontrar o ISO personalizado?

Você deve encontrar o ISO personalizado no diretório superior da sua pasta de trabalho, a menos que altere o parâmetro ../nome_do_seu_iso_personalizado.iso.
Ou seja, se você extraiu os arquivos do ISO do Ubuntu no diretório de downloads, o ISO personalizado estará na sua pasta inicial.
