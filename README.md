# Phishing para Captura de Senhas do Facebook

Este tutorial orienta a configuração de um ataque de phishing para capturar credenciais do Facebook utilizando Kali Linux e o *Social Engineering Toolkit (SET)*.

## Ferramentas Utilizadas
- **Sistema Operacional**: Kali Linux
- **Ferramenta Principal**: setoolkit (Social Engineering Toolkit)

## Etapas de Configuração

### 1. Acesso Root
O primeiro passo é obter acesso root. Isso é necessário para executar a maioria das ferramentas no Kali Linux.

sudo su
2. Iniciando o Social Engineering Toolkit (SET)
Após obter acesso root, você pode iniciar o SET executando o seguinte comando:


setoolkit
3. Selecionando o Tipo de Ataque
Após iniciar o SET, será apresentado um menu interativo. Selecione a opção correspondente ao ataque de engenharia social:

Social-Engineering Attacks: Para realizar ataques de engenharia social.
Web Site Attack Vectors: Para utilizar vetores de ataque através de sites.


Social-Engineering Attacks > Web Site Attack Vectors
4. Selecionando o Método de Ataque
Escolha a opção para capturar as credenciais através da clonagem de um site legítimo:

Credential Harvester Attack Method: Método de captura de credenciais.
Site Cloner: Clonar um site legítimo para a coleta de credenciais.

Credential Harvester Attack Method > Site Cloner

5. Obtendo o Endereço da Máquina
Em seguida, você precisará do endereço IP da máquina que será usada para hospedar o site de phishing. Use o comando abaixo para obter o IP:



ifconfig
Anote o endereço IP da interface de rede que será utilizada.

6. Clonando o Site do Facebook
Agora, o SET pedirá para você fornecer a URL do site que deseja clonar. Neste exemplo, utilizaremos a página de login do Facebook.

Digite a URL a ser clonada:

http://www.facebook.com

O SET irá então clonar a página de login do Facebook e hospedar no endereço IP da sua máquina.

Resultados
Após configurar o phishing com sucesso, o SET registrará todas as credenciais inseridas pelos alvos na página clonada. As credenciais capturadas serão armazenadas no sistema para consulta posterior.
