Instalação

Ative um Google Cloud Shell no Google Cloud.
Clone este projeto do GitHub no console:
git clone https://github.com/lordofwizard/mcserver

Entre no diretório mcserver:
cd mcserver

Permitir todos os comandos executáveis:
chmod + x *

Execute o script de instalação:
./instalar

Siga a etapa de instalação mostrada no console

Execute o script de servidor de inicialização:
./startserver
(Você só precisa fazer isso se escolher Não.)

Configuração Adicional do Servidor Java (Você pode pular esta parte)
(Isso se aplica apenas a servidores Java, incluindo Nukkit ou o script EULA não funcionou para você.)

Se você inicializar seu servidor pela primeira vez, ele falhará ao iniciar porque você precisa aceitar o EULA para funcionar corretamente.

Vá para o diretório do servidor e aceite o EULA
servidor de cd
nano eula.txt
Certifique-se de que eula.txt contém o seguinte texto abaixo:
eula=verdadeiro
Faça Ctrl + W e pressione Y para salvar e pressione Enter para sair do editor de texto.

Volte para o diretório principal:
CD ..
E reinicie o servidor.
Agora tudo deve estar funcional e pronto. Você pode verificar se o seu servidor está funcionando fazendo screen -r server.
Entrando no seu servidor
Para ingressar em seu servidor, inicie seu servidor fazendo ./startserver (se você ainda não o iniciou) e execute este comando:
tela -r playit
Agora clique no URL de reivindicação e ele deve mostrar o IP do host e o servidor de túnel.
Quando estiver nessa página, role para baixo e clique em Adicionar túnel no Minecraft Java/Bedrock e ao lado do endereço do servidor local, clique em Adicionar.
Agora copie o IP dedicado gerado junto com auto.playit.gg e copie-o para o endereço do servidor no Minecraft e agora você pode jogar o servidor.
(Observação: se você quiser alterar o URL de reivindicação, precisará Parar o servidor. Isso redefinirá o IP do servidor.)

Acessando o console do servidor
Para acessar o console do servidor, abra esta sessão a seguir:
tela -r servidor
Para parar completamente o servidor, você pode fazer ./stopserver no console do Linux ou sair ou parar no console do Minecraft

Desanexando tela/sessão
Para desanexar a sessão, você pode fazê-lo usando os seguintes atalhos de teclado CTRL + A e pressione D
Iniciador de terceiros
Se você estiver usando como uma versão quebrada do Minecraft Java Edition
Exemplo: Tlauncher

Acesse server.properties e localize as propriedades online-mode:
nano server.propriedades
Mude de verdadeiro para falso
modo online=falso
Faça Ctrl + W e pressione Y para salvar e pressione Enter para sair do editor de texto.

Reinicie o servidor depois de aplicar essas alterações.
Acessar arquivos do servidor
Se você quiser acessar os arquivos do servidor, vá para Open Editor no canto superior direito.

Uma vez lá, se você não vir nenhuma pasta no lado esquerdo, você pode abrir a pasta e escolher mcserver e ir para o servidor para visualizar e modificar qualquer coisa dentro.
Se você fez alguma alteração no servidor, reinicie o servidor. Depois de reiniciar o servidor, todas as alterações são salvas no servidor.
Alterando/Personalizando Variáveis
Se você quiser alterar as variáveis ​​dentro do script ou apenas ajustar algo para o seu servidor funcionar, você pode alterar e editar as variáveis/

Para fazer isso, acesse /JavaInstallScripts ou /BedrockInstallScripts no Cloud Shell Editor
Os seguintes servidores Java são compatíveis com variáveis ​​personalizadas:

Tecido
Forja
Papel
Baunilha
Os seguintes servidores Bedrock são compatíveis com variáveis ​​personalizadas:

Nukkit
PocketmineMP
Baunilha
Estes servidores não são compatíveis com variáveis ​​personalizadas:

Sponge Java (Este tipo de servidor é muito antigo e só suporta download direto)
GoMint Bedrock (Nenhuma variável necessária para este tipo de servidor)
Versão mais antiga
Se você estiver usando uma versão mais antiga do Minecraft confira esta documentação e instale de acordo com sua necessidade:

Você pode entrar nos scripts do servidor e editar SOMENTE nesta seção do código:

 {EDITAR AQUI | NÃO EDITAR ACIMA}
 
 EXAMPLE_VARIBALES=VARIABLES # NOTA SOBRE VARIABLES
 
 
(Observação: não edite o código abaixo e acima, pois isso interromperá a instalação e você terá que excluir o projeto novamente.)

Reiniciando seu servidor
Se você não sabe o que significa reiniciar seu servidor, aqui está o passo.

Vá para o diretório mcserver ou ../mcserver/ e execute este comando.
Pare o servidor que interrompe o sistema de encapsulamento do Minecraft Server e do Playit.gg:
./stopserver
E agora inicie seu servidor novamente:
./startserver

Agora seu servidor foi totalmente reiniciado.
