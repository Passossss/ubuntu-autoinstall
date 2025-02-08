# Arquivo de Configuração de Autoinstalação do Ubuntu

Este arquivo serve como exemplo e pode ser usado como referência para suas próprias **instalações automatizadas** no Ubuntu.

---

## **Personalização do Ubuntu 20.04**

Após a instalação, você pode conferir como personalizei o meu ambiente no **Ubuntu 20.04** para criar uma interface mais intuitiva e personalizada.

👉 **Veja como fiz a personalização** [aqui](https://www.notion.so/Personalizando-a-interface-do-linux-194bd166ce5280478ccfdcc42a595887?pvs=4).

---


### **Gerando a Senha Criptografada**
Para que o Linux identifique e criptografe sua senha corretamente, utilize o seguinte comando para gerar uma senha criptografada:

```bash
mkpasswd (sua senha)

Após gerar a senha criptografada, insira-a no campo password: '' no arquivo autoinstall.yaml.
Usando o URL do Arquivo no Instalador do Ubuntu

Você pode usar o arquivo de configuração diretamente no Instalador do Ubuntu (Subiquity), configurando o URL do arquivo em sua instalação.
Criar um ISO Personalizado (Alternativa)

Se você preferir criar um ISO personalizado para suas instalações, siga os passos abaixo:
Passos para Criar o ISO Personalizado:

    Baixe o ISO Oficial do Ubuntu: Baixe a versão oficial do Ubuntu a partir do site oficial.

    Extraia o ISO: Extraia o conteúdo do arquivo ISO para uma pasta de sua preferência.

    Adicione o Arquivo de Autoinstalação: Coloque o arquivo autoinstall.yaml na raiz da pasta extraída do Ubuntu.

    Criação do ISO Personalizado: Após adicionar o arquivo autoinstall.yaml, utilize o seguinte comando para criar o ISO personalizado:

xorriso -as mkisofs -r -V "Nome da Imagem" -o ../nome_do_seu_iso_personalizado.iso -J -l -b boot/grub/i386-pc/eltorito.img -c boot.catalog -no-emul-boot -boot-load-size 4 -boot-info-table pasta-com-os-arquivos-do-iso-do-ubuntu/

Pré-requisitos

Certifique-se de ter os pacotes xorriso e mkisofs instalados em seu sistema antes de executar o comando acima.
Explicação das Variáveis:

    "Nome da Imagem": Este é o nome que aparecerá no gerenciador de arquivos. Em resumo, é o rótulo do ISO.
    ../nome_do_seu_iso_personalizado.iso: O nome e o caminho onde o ISO personalizado será salvo.
    pasta-com-os-arquivos-do-iso-do-ubuntu/: O caminho para a pasta contendo os arquivos extraídos do ISO oficial do Ubuntu.

Onde Encontrar o ISO Personalizado?

Após criar o ISO personalizado, ele será salvo no diretório superior da sua pasta de trabalho (a menos que você altere o parâmetro ../nome_do_seu_iso_personalizado.iso).

Por exemplo, se você extraiu os arquivos do ISO do Ubuntu na pasta de downloads, o ISO personalizado será salvo em sua pasta inicial.
