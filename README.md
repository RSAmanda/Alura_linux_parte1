# Alura_linux_parte1

# Link do Curso

[Curso Online Linux I: conhecendo e utilizando o terminal | Alura](https://cursos.alura.com.br/course/linux-ubuntu)

# Materiais de Apoio

# Comandos Básicos

```bash
pwd # caminho onde se está
ls # lista de diretórios
ls -l # mostra detalhes
ls -a # mostra arquivos ocultos
echo # retorna o texto escrito depois do comando
echo "bem vindo" > bemvindo.txt # direciona o texto para o arquivo
# se o arquivo existe, o conteúdo será sobrescrito
echo "bem vindo" >> bemvindo.txt # concatena o texto no arquivo
cat <nome do arquivo> # imprime no terminal o conteúdo do arquivo
cat <nome do arquivo> - n # mostra as linhas também
man # manual
whoami # nome do usuário
clear # limpar a tela ou crtl+l
cd # raiz
cd <nomedir> # entra na pasta (diretório)
cd .. # volta um diretório
mkdir nomeNovoDiretorio # cria um diretório
rmdir <nomedir> # remove diretório vazio
rm <nomearq> # remove arquivo
rm -r # remove recurdivamente
cp nomearqui.txt nomearquinovo.txt # copia o conteudo de nomearqui para nomearquinovo
cp -r # copia recursivamente, para usar em diretórios
mv nomearqui.txt nomearquinovo.txt # renomeia arquivo
mv nomearqui.txt subpasta/ # move arquivo
touch nomrarqui # 'encosta' no arquivo, ou seja, altera a data
```

# Caracteres coringas

```bash
#caracteres coringas
# ? -> quando não se sabe um caractere
cat bra?il.txt # assim, ele vai ler arquivos chamados brasil.txt ou brazil.txt
# * -> quando não se sabe vários e quantos caracteres se tem antes ou depois de *
cat nomearquivo*.txt # assim retorna o nomearquivo1.txt nomearquivo 20.txt, etc 
cat *.txt # abre todos os arquivos .txr
```

# Compactar e descompactar

```bash
zip -r nomedoarqzip nomedir # zipar uma pasta
zip -r work.zip workspace/ # exemplo
unzip # descompacta 
unzip -q #quiet # sem retornar no terminal
unzip -l work.zip #para listar os arquivos e diretórios que se encontram compactados

tar -cz nomedoarq > arqcompac.tar.gz # -c compactar; z zip
tar -czf arqcompac.tar.gz nomepasta/
tar -xz < work.tar.gz #-x extrair, z zip
tar -xzf work.tar.gz
tar -vxzf work.tar.gz # v - verbose, mais infos 
```

# Arquivo

```bash
echo "bem vindo" > bemvindo.txt # direciona o texto para o arquivo
# se o arquivo existe, o conteúdo será sobrescrito
echo "bem vindo" >> bemvindo.txt # concatena o texto no arquivo
cat <nome do arquivo> # imprime no terminal o conteúdo do arquivo
cat <nome do arquivo> - n # mostra as linhas também
head <nome do arquivo> # mostra no terminal as 10 primeiras linhas
head -n 3 <nome do arquivo> # mostra no terminal as 3 primeiras linhas
tail <nome do arquivo> #últimas linhas
less <nome do arquivo> #abre no terminal e consegue navegar com setas

```

# VI/VIM

```bash
# edição do texto
i # insere na posição atual
a # insere no caracter seguinte
A # insere no final da linha
dd # deleta linha, se inserir um número N antes, deleta N linhas
5dd # deleta cinco linhas
x # remove caracter, se inserir um número N antes, remove N caracteres
tecla ESC # sai do modo de edição

# sair e salvar
:w # salva
:wq # salva e sai
:q # sai
:q! # sai sem salvar

# movimentação
#pode-se usar as setas
$ # vai para o final da linha atual
0 # vai para o início da linha atual
G # vai para a última linha
3G #vai para a terceira linha

#pesquisar no aquivo
/<o que se quer pesquisar>
# exemplo:
/print
#navegando na pesquisa
n # vai para a próxima ocorrência
N # vai para a ocorrência anterior

#copiar e colar
yy # copia a linha, se inserir um número N antes, copia N linhas
p # cola a linha copiada, se inserir um número N antes, cola N vezes o conteúdo copiado
```
