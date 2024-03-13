# Linux para Iniciantes.
Para entender melhor as distribuições Linux, é importante lembrar que o Linux é um sistema operacional semelhante ao Windows ou MacOS, mas é notável por sua estabilidade e segurança. Sua principal característica distintiva é ser open source, ou seja, seu código-fonte é aberto e pode ser modificado e distribuído por qualquer pessoa. Isso levou ao surgimento de várias versões do Linux, que são conhecidas como distribuições.

Conheça as características de algumas das distribuições Linux mais populares:

- **Ubuntu:** possivelmente a distribuição mais conhecida e um excelente ponto de partida para compreender as diferenças entre as distribuições do Linux. O Ubuntu é renomado por sua facilidade de uso e uma comunidade de suporte ativa. É uma escolha ideal para iniciantes no Linux, graças à sua instalação simples e à interface gráfica intuitiva. Além disso, o Ubuntu oferece uma vasta seleção de programas e aplicativos disponíveis para instalação direta por meio da Central de Programas Ubuntu.
- **Fedora:** uma opção popular, especialmente entre desenvolvedores de software. O Fedora é conhecido por incorporar as últimas tecnologias e inovações. Além disso, o Fedora serve como base para o desenvolvimento do sistema Red Hat Enterprise Linux, amplamente utilizado em empresas em todo o mundo.
- **Debian:** uma excelente escolha especialmente para servidores. Sua reputação é construída em torno de sua estabilidade e segurança. O Debian também serviu como base para o desenvolvimento de outras distribuições, incluindo o Ubuntu.
- **Arch Linux:** muito popular entre usuários experientes. Ele oferece total personalização durante a instalação, mas requer um conhecimento profundo do funcionamento do sistema operacional.

Para ilustrar como estas diferenças se traduzem na prática, vamos ver como a instalação do programa `htop` (um monitor de sistema interativo) é feita em cada uma dessas distribuições:

- Ubuntu: `sudo apt install htop`
- Fedora: `sudo dnf install htop`
- Debian: `sudo apt-get install htop`
- Arch Linux: `sudo pacman -S htop`

Note que o comando para instalar um programa é diferente em cada distribuição. Isso ocorre porque cada uma usa um sistema de gerenciamento de pacotes diferente.

Lembrando que o Linux é comumente utilizado por devs, pois muitas linguagens de programação e ferramentas de desenvolvimento são mais compatíveis ou mais fáceis de serem configuradas nesse sistema operacional.

O Linux é uma ótima escolha para quem quer se aprofundar em desenvolvimento de software. Treinar em casa, em um ambiente seguro e estável como o Linux pode ser um ótimo primeiro passo na sua jornada de aprendizado em programação!

Limpar o terminal e deixar o ambiente mais organizado com o comando `clear`
Utilizar comandos básicos no terminal, como `ls`, `cd` e `pwd`
Criar pastas via terminal, utilizando o comando `mkdir`
Criar e editar arquivos de texto utilizando os comandos `touch` e `echo`
Visualizar os dados de um arquivo utilizando o comando `cat` e sem a necessidade de abri-lo através de um editor
Excluir arquivos indesejados através do comando `rm`
Renomear arquivos com o comando `mv`

## Editando arquivos

Então, nesses casos onde utilizamos _Linux_ e _Ubuntu_, por exemplo, é comum usarmos o _**VI**_, um editor que já vem instalado por padrão nessas distribuições.

Para ter acesso a ele, vamos digitar o comando `vi` no terminal.

```console
vi
```

Ao teclar "Enter", será aberto o editor que, a princípio, não é muito intuitivo. Não temos os comandos práticos que temos por costume, nem uma lista. Então, pode ser que no início haja alguma dificuldade, mas vamos tentar passar os principais ao longo deste vídeo.

Por exemplo: o cursor está presente no editor, mas não conseguimos digitar imediatamente; precisamos entrar no modo de linha de comando para poder inserir.

Vamos apertar a tecla "I" para conseguir fazer uma digitação nesta tela. Se simplesmente começarmos a digitar, não vai aparecer nada. Feito isso, vamos digitar "Estudos sobre terminal". Para pular para a linha de baixo, usamos "Enter" normalmente. Na linha seguinte, vamos escrever "Estamos utilizando Ubuntu".

Se quisermos salvar esse arquivo, precisamos sair do modo edição apertando a tecla "Esc", e em seguida digitar o comando `:w`. O `:w` é o comando que salva o arquivo, e após ele, temos que dizer o nome do arquivo. Podemos chamá-lo de `arquivo.txt`, por exemplo.

```console
:w arquivo.txt
```

Enviado o comando, temos como retorno que o arquivo foi salvo com duas linhas. Agora, como fazemos para sair do editor?

Vamos começar com as operações simples. Teclamos "I" para começar a escrever, apertamos "Esc" para ir para os comandos, com o comando `:w` conseguimos salvar, e agora, se quisermos sair do editor, usamos o comando `:q`, que é o comando para sair já salvando.

Nesse caso, não temos alterações. Se houvesse alguma alteração, o editor avisaria.

```console
:q
```

Para abrir o VI com esse `arquivo.txt`, digitamos o seguinte comando:
```console
vi arquivo.txt
```
Se quisermos voltar a escrever no arquivo, devemos teclar "I" de novo? Não necessariamente. Se quisermos escrever depois da palavra "Ubuntu", por exemplo, vamos para a linha de baixo e digito "A" maiúsculo. O "A" maiúsculo já nos posiciona ao final da última palavra dessa linha.

Uma vez na última posição, ao teclar "Enter", podemos continuar digitando.
Digitamos uma nova linha. Agora, se quisermos salvar, dessa vez não precisaremos digitar o nome do arquivo novamente. Vamos apertar a tecla "Esc" e usar simplesmente o comando `:w`. Feito isso, se de novo usarmos `:q`, ele vai sair salvando.

Agora, vamos conferir uma situação em que fizemos uma alteração e queremos sair sem salvar, por exemplo. Para isso, vamos novamente ao arquivo com o comando `vi arquivo.txt`.

Agora vamos pressionar a tecla "O" para inserir uma nova linha abaixo da atual, que é a primeira do arquivo. Vamos inserir um exemplo de algo incorreto e queremos sair sem salvar. Para isso, pressionamos a tecla "Esc" e digitamos o comando `:q!`.
```console
:q!
```
O comando `:q!` indica que desejamos sair sem salvar as alterações realizadas. Assim, ao sair e retornar ao arquivo, estará tudo correto como antes.

Outras operações que podemos fazer incluem copiar, colar e recortar. Para **copiar**, utilizamos o comando "**yy**". Quando usamos o "yy", indicamos que estamos copiando a linha onde o cursor está localizado.

Vamos posicionar o cursor na linha 3 e pressionar "O" para criar uma nova linha abaixo. Agora, como colar o conteúdo copiado? Precisamos de um comando para colar, e esse comando é o **"p"**.

### Usando o Nano

Para usar o Nano, utilize o seguinte comando no terminal:
```undefined
nano
```
Alguns comandos úteis do Nano:

- Para colar no nano um texto copiado: `CTRL+U`.
- Para copiar um texto dentro do nano: `ALT+6.
- Para recortar um texto dentro do nano: `CTRL+K`.
- Para salvar: `CTRL+O`.
- Para sair: `CTRL+X`.

Com o terminal aberto, podemos **visualizar o começo de um arquivo**, usando o comando:
```bash
head -c 300 texto_java.txt
```
Este comando indica que desejamos visualizar os 300 primeiros caracteres.

Podemos também **visualizar o fim de um arquivo**, usando o comando:
```bash
tail -n 2 texto_java.txt
```
Este comando indica que desejamos visualizar as 2 últimas linhas.

Você sabia que existem outros métodos bastante úteis que você pode explorar neste incrível sistema operacional? Além do `.zip` e `.tar`, existem outros métodos de compactação e descompactação no Linux que podem ser mais adequados dependendo do seu objetivo.

Cada método tem suas próprias características, como a velocidade de compressão, a eficiência de compressão e a portabilidade entre diferentes sistemas:

- Velocidade de compressão: quão rápido um arquivo pode ser comprimido.
- Eficiência de compressão: quão pequeno o arquivo pode se tornar.
- Portabilidade: se a compactação é suportada em diferentes sistemas operacionais.

### Gzip

O comando `gzip` é frequentemente usado para compressão em sistemas Linux. Ele faz uma boa compressão, mas mantém a velocidade. É utilizado para compactar apenas um único arquivo. Para compactar diretórios, geralmente é combinado com `.tar`.

Para compactar um arquivo usando gzip, você pode usar o seguinte comando:
```undefined
gzip file.txt
```
Para descompactar um arquivo `.gzip`, você pode usar o comando a seguir:
```undefined
gunzip file.txt.gz
```
### Bzip2

O comando `bzip2` gera arquivos menores em comparação ao gzip, no entanto, é mais lento. Assim como o gzip, o bzip2 só comprime arquivos individuais e precisa ser usado com o tar para diretórios.

Para compactar um arquivo usando bzip2, você pode usar o seguinte comando:
```undefined
bzip2 file.txt
```
Para descompactar um arquivo `.bzip2`, você pode usar o seguinte comando:
```undefined
bunzip2 file.txt.bz2
```
### XZ

O comando `xz` tem a melhor taxa de compressão se comparado com gzip e bzip2. No entanto, é o mais lento entre eles. Assim como os outros, também precisa ser usado com tar para diretórios.

Para compactar um arquivo usando xz, você pode usar o seguinte comando:
```undefined
xz file.txt
```
Para descompactar um arquivo `.xz`, você pode usar o seguinte comando:
```undefined
unxz file.txt.xz
```


# Formas de executar script:

No Ubuntu, quando se trata de executar scripts no terminal, há duas maneiras comuns de fazê-lo: usando `bash script.sh` ou `./script.sh`. Ambas as opções têm suas diferenças e podem ser úteis em diferentes situações. Vamos explorar essas diferenças.

### `bash script.sh`

- Com `bash script.sh`, você pode executar um script sem a necessidade de conceder permissão de execução ao arquivo.
- Essa abordagem é útil quando você não deseja ou não pode alterar as permissões do arquivo de script.

### `./script.sh`

- Com `./script.sh`, o arquivo de script deve ter permissão de execução concedida (você pode fazer isso com o comando `chmod +x script.sh`).


Variáveis de ambiente são uma série de parâmetros do sistema operacional que podem ser usados pelos programas. Em outras palavras, são informações que estão armazenadas no seu computador e que são utilizadas pelos programas para realizar tarefas específicas. Mas por que precisamos delas?

Parte da mágica dos computadores é que programas diferentes precisam se comunicar em um nível básico. As variáveis de ambiente facilitam essa comunicação, pois ajudam os programas a saberem onde procurar certos recursos, como arquivos de dados, além de fornecerem informações sobre o sistema operacional e o hardware do computador.

Agora que sabemos o que são e por que são importantes, vamos explorar suas diferenças no Linux e no Windows.

## Variáveis de ambiente no Linux

No linux, as variáveis de ambiente são case-sensitive, o que significa que `Variavel` é diferente de `variavel`. Elas são geralmente armazenadas em arquivos bash, como `~/.bashrc` ou `~/.bash_profile`. Para exibi-las, você pode digitar `printenv` no terminal e apertar Enter. Veja um exemplo para definir uma nova variável de ambiente:
```bash
export NEW_VARIABLE="Hello, World!"
```
Para acessar essa variável, você usaria o comando `echo $NEW_VARIABLE`.

## Variáveis de ambiente no Windows

No Windows, as variáveis de ambiente não são case-sensitive, o que significa que `Variavel` é a mesma coisa que `variavel`. Elas são normalmente armazenadas em Propriedades do Sistema -> Configurações Avançadas do Sistema -> Variáveis de Ambiente. Para exibi-las, você pode digitar `set` no prompt de comando. Confira um exemplo de como definir uma nova variável de ambiente:
```cmd
set NEW_VARIABLE="Hello, World!"
```
Para acessar essa variável no prompt de comando, você usaria o comando `echo %NEW_VARIABLE%`.

O WSL não é utilizado em ambientes de produção, onde temos que rodar uma aplicação o tempo todo, já que o próprio Windows não é muito utilizado, e o WSL é uma ferramenta exclusiva do Windows. O Windows não é muito utilizado em servidores por alguns motivos, sendo os principais:

- A necessidade de uma licença paga por servidor, igual temos nos computadores pessoais, porém para o Windows Server;
- A instabilidade, principalmente nos sistemas que ficam ligados 24 horas por dia, onde vários pequenos serviços acabam acumulando erros e forçando uma reinicialização do servidor;
- As atualizações constantes que dependem de uma reinicialização do sistema para serem concluídas;
- Não ter o código aberto, impedindo que modificações legítimas sejam feitas para correção de erros, desativação de recursos ou melhorias de desempenho, atrapalhando e dificultando a execução de certas aplicações.

Com todas essas limitações, o WSL não é uma ferramenta muito comum para pessoas de DevOps, já que sua utilização em servidores não é recomendada e devemos sempre rodar e testar códigos com o ambiente mais próximo do real, porém ele acaba sendo muito popular entre pessoas que desenvolvem softwares, já que o WSL consegue rodar a maioria dos comandos padrão do Linux e é mais rápido e leve que uma máquina virtual, como as do VirtualBox.


# SSH no Windows

_Security Shell_ (SSH) é um protocolo de rede utilizado para oferecer acesso remoto seguro a um computador ou servidor. Para isso, o SSH estabelece uma comunicação criptografada entre um cliente e um servidor, garantindo que dados sensíveis, tais como informações pessoais e senhas, sejam protegidas contra espionagem virtual.

Podemos usar o SSH em tarefas como acesso a arquivos armazenados em outros computadores, como: execução remota de programas e gerenciamento de servidores remotos. Logo, essa ferramenta é muito usada por administradores de sistemas, desenvolvedores e profissionais de segurança.

Dessa forma, para estabelecermos uma conexão remota segura entre dois computadores, usamos o comando SSH. A sintaxe básica do comando é:

ssh [options] [user@]hostname [command]

Algumas opções [options] comuns são: -p port: usada para especificar o número da porta adotada para a conexão. Por default, o comando SSH utiliza a porta 22. -i identity_file: indica o arquivo de chave privada a ser usado na autenticação. -l login_name: utilizada na especificação do nome de usuário a ser usado na conexão.

Se quisermos acessar um servidor remoto, por exemplo, o comando é bem simples:

ssh username@remote_server_ip_address

Basta inserirmos o usuário de acesso ao servidor no campo _username_ e o endereço de IP do servidor no campo _remote_server_ip_address_. Ao confirmarmos o comando apertando _enter_, deveremos digitar a senha de acesso do usuário indicado para estabelecermos a conexão ao servidor. Estabelecida a sessão de acesso, poderemos buscar arquivos e executar comandos no servidor. Podemos encerrar a conexão a qualquer momento digitando o comando _exit_.

Apesar de ser um procedimento simples, podemos encontrar algumas dificuldades na execução do comando SSH em algumas versões do sistema operacional Windows. Infelizmente, em algumas versões o comando não está disponível, no entanto podemos contornar esse entrave seguindo alguns passos de acordo com a versão instalada em nosso computador.

Caso estejamos utilizando o Windows 10, podemos seguir os passos abaixo:

1. Vamos abrir as configurações do Windows;
2. Acessar a aba Aplicativos;
3. Procurar por Aplicativos e Recursos;
4. Clicar na opção Recursos Opcionais;
5. Identificar se o recurso OpenSSH está incluído na lista exibida. Caso não esteja, devemos clicar na opção Adicionar um Recurso;
6. Vamos procurar a opção “Cliente SSH” e instalar o recurso em nosso computador.

Após esses passos, o comando SSH estará prontamente disponível no terminal de comando do Windows. Caso não esteja, uma boa alternativa é usarmos a próxima estratégia (acesso SSH com programa PuTTY), indicada para versões anteriores do Windows.

Pode ser que estejamos utilizando uma versão anterior do Windows, neste caso vamos instalar um programa chamado PuTTY para conseguir usar o protocolo SSH em nosso computador. Listamos uma breve sequência de passos para facilitar a utilização do PuTTY para acesso remoto:

1. Vamos acessar o website oficial do [PuTTY] ([https://www.putty.org](https://www.putty.org)) para fazermos o download do programa. Basta acessarmos a opção “Download PuTTY” e aguardar;
2. Concluído o download do programa, vamos fazer sua instalação utilizando as configurações padrão;
3. Após a instalação, vamos abrir o programa e procurar as caixas de texto “Host name” e “Port” para configurarmos o acesso remoto. No campo “Host name” devemos inserir o IP do dispositivo que iremos acessar remotamente (computador, servidor ou máquina virtual), já no campo “Port” usamos a porta default do protocolo SSH (porta 22);
4. Uma vez configurado as opções de acesso, vamos clicar na opção “Open” que exibirá em nossa tela uma solicitação do nome do usuário de acesso. Fornecemos então o nome de usuário de acesso ao servidor ou máquina virtual e, na sequência, nos será solicitada também a senha de acesso;
5. Depois da verificação de acesso (usuário e senha), poderemos acessar o servidor ou máquina virtual de modo remoto via protocolo SSH.
