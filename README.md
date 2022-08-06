# Projeto 1 - Infrastructura as a Code (IaC)

Para utilizar os scripts é preferível estar logado como root, pois assim o usuário terá todas as permissões necessárias para fazer a exclusão de arquivos e usuários desnecessários ou que tenham sido criados para teste anteriormente.

Para excluir diretórios, o seguinte comando será utilizado:

rm -rf /nome_do_diretorio/

Onde nome_do_diretorio será substituído pelo nome do diretório que deverá ser excluído, o atributo -rf serve para excluir recursivamente (r), ou seja, irá excluir todos os arquivos presentes no diretório a ser excluído, e também de forma forçada (f), para que qualquer confirmação seja ignorada e todos os arquivos sejam excluídos.

Com os diretórios já excluídos, agora será excluído os usuários com o seguinte comando:

userdel -r nome_do_usuario

Onde nome_do_usuario será substituído pelo nome do usuário a ser excluido, caso você não saiba qual, ou quais, usuários existam, basta utilizar o comando:

cat /etc/passwd

Agora se excluirá os grupos com o comando:

groupdel NOME_DO_GRUPO

Onde NOME_DO_GRUPO deverá ser substituído pelo nome do grupo a ser excluído, para consultar os grupos existentes, é utilizado o comando:

cat /etc/group

Com o ambiente do servidos já preparado, o script poderá ser criado e executado.
Para fins de organização, será criada uma pasta script na raiz, onde todos os scripts utilizados serão armazenados.

Utilize o comando "pwd" para ter certeza que você esteja na raiz, caso não esteja, utilize o comando "cd /" e então:

mkdir /scripts
cd scripts

Já dentro da pasta scripts, será criado o arquivo de script deste projeto com o comando:

nano iac1.sh

Onde nano é o editor de textos presente do Linux, o arquivo será criado automaticamente caso ele não exista no diretório.
O código estará presente dentro do script disponibilizado neste repositório.

-------------------------------------------------------------------------------------------------------------

Com o script criado, agora ele poderá ser testado, para isso o ideal é criar um snapshot da máquina ou criar algum ambiente de testes, de forma que você possa dar um rollback para o estado anterior da execução do script caso ocorra algum erro.

Para executar o script, primeiro é necessário dar a permissão de execução do arquivo com o comando:

chmod +x iac1.sh

E então executá-lo com o comando:

./iac1.sh

Nenhum erro, projeto concluído!
