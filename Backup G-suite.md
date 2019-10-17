## Procedimento para realização de backup de e-mail no G-Suite

- Para realizar o backup de contas é necessario acessar a planilha do Google que contem os usuários suspensos (Desligados).

- Após acessar a planilha, deve-se copiar o endereço de e-mail do usuário que deseja realizar o backup. 

- Como um usuário em mãos, acesse o Google Admin para reativação do usuário e reset de senha. 

[Google Admin Console](http://admin.google.com)

- No Admin Console, pesquise e acesse o usuário que ira realizar o backup. 

![](https://github.com/grupozap/squad-service-desk/blob/master/Documentation/Backup/G-Suite/FILES/G_Suite_Backup_01.png)

- Na pagina do usuário clique em "MAIS" e em seguida "REATIVAR

![](https://github.com/grupozap/squad-service-desk/blob/master/Documentation/Backup/G-Suite/FILES/G_Suite_Backup_02.png)

![](https://github.com/grupozap/squad-service-desk/blob/master/Documentation/Backup/G-Suite/FILES/G_Suite_Backup_03.png)

![](https://github.com/grupozap/squad-service-desk/blob/master/Documentation/Backup/G-Suite/FILES/G_Suite_Backup_04.png)

- Defina uma nova senha para o usuário que foi reativado clicando em "REDEFINIR SENHA".

![](https://github.com/grupozap/squad-service-desk/blob/master/Documentation/Backup/G-Suite/FILES/G_Suite_Backup_05.png)

![](https://github.com/grupozap/squad-service-desk/blob/master/Documentation/Backup/G-Suite/FILES/G_Suite_Backup_06.png)

    * OBS: Desmarque a opção de trocar a senha no proximo login caso ela esteja ativa. 
  
- Verifique se as opções de Autenticação de Duplo Fator não estão ativas, e se não estão preenchidas as opções de recuperação de conta. Caso estejam, desative e remova os dados de recuperação.  

![](https://github.com/grupozap/squad-service-desk/blob/master/Documentation/Backup/G-Suite/FILES/G_Suite_Backup_07.png)

    * OBS: Nas opções de recuperação voce pode optar por colocar um telefone que você possui acesso, pois, em algumas contas é solicitada essa informação no momento do login.

- O proximo passo sera acessar o Google Takeout com o usuário que reativou.

[Google Takeout](https://accounts.google.com/signin/v2/identifier?passive=1209600&osid=1&continue=https%3A%2F%2Ftakeout.google.com%2F&followup=https%3A%2F%2Ftakeout.google.com%2F&flowName=GlifWebSignIn&flowEntry=ServiceLogin)

- Digite o e-mail da conta e clique em "Proximo" e em seguida digite a senha e clique em "Proximo" novamente. 

![](https://github.com/grupozap/squad-service-desk/blob/master/Documentation/Backup/G-Suite/FILES/G_Suite_Backup_08.png)

![](https://github.com/grupozap/squad-service-desk/blob/master/Documentation/Backup/G-Suite/FILES/G_Suite_Backup_09.png)

- No painel do Takeout, selecione a opção "Desmarcar tudo", em seguida localize na lista o "E-mail" e remarque ele. Feito isso, desça até o fim da pagina e clique em "Proxima etapa". 

![](https://github.com/grupozap/squad-service-desk/blob/master/Documentation/Backup/G-Suite/FILES/G_Suite_Backup_10.png)

![](https://github.com/grupozap/squad-service-desk/blob/master/Documentation/Backup/G-Suite/FILES/G_Suite_Backup_11.png)

![](https://github.com/grupozap/squad-service-desk/blob/master/Documentation/Backup/G-Suite/FILES/G_Suite_Backup_12.png)

- No proxima pagina, selecione as opções: 

  * Tipo de Exportação: Apenas um arquivo
  * Formato: .tgz
  * Tamanho: 50GB

E clique em "Criar arquivo" e aguarde.

![](https://github.com/grupozap/squad-service-desk/blob/master/Documentation/Backup/G-Suite/FILES/G_Suite_Backup_13.png)

    * OBS: A criação do arquivo pode demorar, minutos, horas ou até mesmo dias para ser concluida dependendo da quantidade de dados que o ex-colaborador possuia no e-mail. 

- Após aguardar um tempo depois da solicitação para criar o arquivo, acesse o Takeout novamente. 

[Google Takeout](https://accounts.google.com/signin/v2/identifier?passive=1209600&osid=1&continue=https%3A%2F%2Ftakeout.google.com%2F&followup=https%3A%2F%2Ftakeout.google.com%2F&flowName=GlifWebSignIn&flowEntry=ServiceLogin)

- Digite o e-mail da conta e clique em "Proximo" e em seguida digite a senha e clique em "Proximo" novamente. 

![](https://github.com/grupozap/squad-service-desk/blob/master/Documentation/Backup/G-Suite/FILES/G_Suite_Backup_08.png)

![](https://github.com/grupozap/squad-service-desk/blob/master/Documentation/Backup/G-Suite/FILES/G_Suite_Backup_09.png)

- Quando o arquivo for concluído sera liberada a opção "Fazer o download". Clique nela para baixar o backup e em seguida digite a senha do usuário novamente. 

![](https://github.com/grupozap/squad-service-desk/blob/master/Documentation/Backup/G-Suite/FILES/G_Suite_Backup_14.png)

![](https://github.com/grupozap/squad-service-desk/blob/master/Documentation/Backup/G-Suite/FILES/G_Suite_Backup_09.png)

    * OBS: O download do arquivo iniciara automaticamente após a confirmação da senha. 

- Após a conclusão do Download na sua própria máquina, o arquivo deve ser renomeado com o nome.sobrenome@grupozap.com da conta e movido para o diretório: 

\\\pd-bkpexp-bcw01.grupozap.net\Backups

   * O usuário utilizado para conectar no diretório é o "a.seunome.sobrenome"

- Terminada a copia para o diretório, o backup estará concluido. 


## Informações importantes

- Todos os dias, às 18h00, o task scheduler do Windows roda um Scritp responsável por copiar os Backups do servidor para o S3 da AWS, e em seguida esvazeia o diretório para que novos backups sejam adiocionados lá

- O Scritp .bat está localizado no disco d:\Scritps dentro do servidor. 
