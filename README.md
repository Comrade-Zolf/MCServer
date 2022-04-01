# Informações do Minecraft Cloud Shell

Neste projeto, ensinaremos você a hospedar seu próprio servidor Java/Bedrock Minecraft usando o `Google Cloud Shell`. Isso funciona sob o sistema operacional Linux baseado em `Ubuntu/Debian`. Este projeto requer **NENHUM CARTÃO DE CRÉDITO** e todo o projeto é inteiramente **GRATUITO**! Você pode fazer um servidor sem lhe custar nada.

**Os seguintes recursos são adicionados a este projeto:**
- Suporta diferentes tipos de servidores Bedrock
- Interface limpa e amigável
- Suporta tipo adicional de servidor Java * (por exemplo, esponja, papel, tecido etc) *
- Adicionado gerenciamento de servidor
- Scripts funcionais mais fáceis *(ex. [**./uninstall**](https://github.com/Comrade-Zolf/MCServer/blob/main/README.md#uninstallremove-the-server) permite que você exclua seu servidor facilmente)*
- Configuração instantânea do script EULA *(Pular completamente esta parte, o que torna a vida de outras pessoas muito mais fácil de gerenciar)*
- Instalação de servidor mais rápida *(Você provavelmente levaria cerca de 30 segundos para configurar um servidor)*


### Lista de afazeres
- [x] Perguntando ao usuário a versão específica que deseja executar do java.
- [x] Adicione fontes de terceiros na lista.
- [x] Digitador automático de mensagens para digitar algo no servidor. (APLICATIVO AFK)
- [x] Maneira mais fácil de fazer upload de arquivos no google drive. (use o editor cloud-shell)
- [x] Script de atualização.
### Especificações do servidor:
- **SO:** Debian GNU/Linux 10 (buster) x86_64
- **RAM:** 8 GB a 16 GB
- **Localização:** com base na sua localização física.
- **Armazenamento:** Aproximadamente 5 GB
- **CPU:** AMD EPYC (2) 7B12 @ 2,249 GHz ou Intel Xeon (4) @ 2,199 GHz

Você pode ver suas especificações exatas fazendo `./specinfo`

### Serviço usado:
- [playit.gg](https://playit.gg)
- [console.cloud.google.com](https://console.cloud.google.com)

## Instalação
* Ative um [Google Cloud Shell](https://console.cloud.google.com/) no Google Cloud.
* Clone este projeto do GitHub no console:
```
git clone https://github.com/Comrade-Zolf/MCServer
```
* Vá para o diretório `MCServer`:
```
cd MCServer
```
* Permitir todos os comandos executáveis:
```
chmod + x *
```
* Execute o script de instalação:
```
./instalar
```
Siga a etapa de instalação mostrada no console
* Execute o script do servidor de inicialização:
```
./startserver
```
(Você só precisa fazer isso se escolher 'Não'.)

## Configuração Adicional do Servidor Java (Você pode pular esta parte)
*(Isso se aplica apenas a servidores Java, incluindo Nukkit ou o script EULA não funcionou para você.)*

Se você inicializar seu servidor pela primeira vez, ele falhará ao iniciar porque você precisa aceitar o **EULA** para funcionar corretamente.

* Vá para o diretório do servidor e aceite o [EULA](https://www.minecraft.net/en-us/eula)
```
servidor de cd
```
```
nano eula.txt
```
* Certifique-se de que `eula.txt` contenha o seguinte texto abaixo:
```
eula=verdadeiro
```
Faça `Ctrl + W` e pressione `Y` para salvar e pressione `Enter` para sair do editor de texto.
* Volte para o diretório principal:
```
CD ..
```
- E [Reinicie o Servidor](https://github.com/Comrade-Zolf/MCServer/blob/main/README.md#restarting-your-server).
* Agora tudo deve estar funcional e pronto. Você pode verificar se o seu servidor está funcionando fazendo `screen -r server`.
## Entrando no seu servidor
* Para entrar no seu servidor, inicie seu servidor fazendo `./startserver` *(Se você ainda não o iniciou)* e execute este comando:
```
tela -r playit
```
- Agora clique no **Reivindicar URL** e ele deve mostrar o IP do seu host e o servidor de túnel.
- Uma vez nessa página, role para baixo e clique em **Add Tunnel** no Minecraft Java/Bedrock e ao lado do **Local server address**, clique em **Add**.
- Agora copie o IP dedicado gerado junto com `auto.playit.gg` e copie-o para o Endereço do Servidor no Minecraft e agora você pode jogar no servidor.

*(Observação: Se você quiser alterar o URL de reivindicação, precisará Parar o servidor. Isso redefinirá o IP do servidor.)*

## Acessando o Console do Servidor
* Para acessar o console do servidor, abra a seguinte sessão:
```
tela -r servidor
```
Para parar completamente o servidor, você pode fazer `./stopserver` no console do Linux ou `exit` ou `stop` no console do Minecraft

## Desanexando tela/sessão
* Para desanexar a sessão, você pode fazê-lo usando os seguintes atalhos de teclado
`CTRL + A` e pressione `D`

## Iniciador de terceiros
* Se você estiver usando como uma versão crackeada do **Minecraft Java Edition**

Exemplo: [Tlauncher](https://tlauncher.org/en/)

- Vá para `server.properties` e encontre as propriedades `online-mode`:
```
nano server.propriedades
```
- Mude de `true` para `false`
```
modo online=falso
```
Faça `Ctrl + W` e pressione `Y` para salvar e pressione `Enter` para sair do editor de texto.

- [Reinicie](https://github.com/Comrade-Zolf/MCServer/blob/main/README.md#restarting-your-server) seu servidor depois de aplicar essas alterações.

## Acessar arquivos do servidor
Se você deseja acessar o arquivo do servidor
