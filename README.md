# :penguin: Linux Experience - Projeto 01
Projeto do Bootcamp Linux Experience - Script de Criação de Estrutura de Usuários, Diretórios e Permissões.


## :page_with_curl:

#!/bin/bash

(Script de Criação de Usuários, Diretórios e Permissões)

echo "Script de Criação de Usuários, Diretórios e Permissões"

echo "Criando os Diretórios"

mkdir /pub
mkdir /r.h
mkdir /fin
mkdir /t.i
mkdir /ven

echo "Criando Grupos"

groupadd GUP_VEN groupadd GUP_R.H groupadd GUP_FIN groupadd GUP_T.I

echo "Criando Usuários"

echo "Usuários Setor Vendas"

useradd julio -c "Julio Cesar" -m -s /bin/bash -p $(openssl passwd 012345) -G GUP_VEN passwd julio -e useradd Deise -c "Deise Doria" -m -s /bin/bash -p $(openssl passwd 012345) -G GUP_VEN passwd deise -e useradd juliana -c "Juliana Silva" -m -s /bin/bash -p $(openssl passwd 012345) -G GUP_VEN passwd juliana -e

echo "Usuários Setor R.H"

useradd karina -c "Karina Silva" -m -s /bin/bash -p $(openssl passwd 012345) -G GUP_R.H passwd karina -e useradd Manuela -c "Manuela Jorge" -m -s /bin/bash -p $(openssl passwd 012345) -G GUP_R.H passwd manuela -e useradd conceicao -c "Conceição Silva" -m -s /bin/bash -p $(openssl passwd 012345) -G GUP_R.H passwd conceicao -e

echo "Usuários Setor Financeiro"

useradd rafael -c "Rafael Jorge" -m -s /bin/bash -p $(openssl passwd 012345) -G GUP_FIN passwd rafael -e useradd lorenzo -c "Lorenzo Jorge" -m -s /bin/bash -p $(openssl passwd 012345) -G GUP_FIN passwd lorenzo -e useradd maria -c "Maria Ceres" -m -s /bin/bash -p $(openssl passwd 012345) -G GUP_FIN passwd maria -e

echo "Usuários Setor T.I"

useradd daniel -c "Daniel Pinheiro" -m -s /bin/bash -p $(openssl passwd 012345) -G GUP_T.I passwd daniel -e useradd edna -c "Edna Silva" -m -s /bin/bash -p $(openssl passwd 012345) -G GUP_T.I passwd edna -e useradd pietro -c "Pietro Pinheiro" -m -s /bin/bash -p $(openssl passwd 012345) -G GUP_T.I passwd pietro -e

echo "Definindo permissões de diretórios"

chown root:GUP_VEN /ven chown root:GUP_R.H /r.h chown root:GUP_FIN /fin chown root:GUP_T.I /t.i

chmod 770 /ven chmod 770 /r.h chmod 770 /fin chmod 770 /t.i chmod 777 /publico

echo "Finalizado."
