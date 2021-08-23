---
description: SIDs (identificadores de segurança) conhecidos identificam grupos genéricos e usuários genéricos.
ms.assetid: eb2f95c4-9465-409b-b76c-9ccae1d05eda
title: SIDs bem conhecidos
ms.topic: article
ms.date: 03/04/2020
ms.custom: 19H1
ms.openlocfilehash: 17fe8827100f9e3684ac0219fc83f183581017cc5738af5933b7bb7cc4ea3ff8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623086"
---
# <a name="well-known-sids"></a>SIDs bem conhecidos

SIDs ( [*identificadores de segurança*](/windows/desktop/SecGloss/s-gly) ) conhecidos identificam grupos genéricos e usuários genéricos. Por exemplo, há SIDs bem conhecidos para identificar os seguintes grupos e usuários:

-   Todos ou mundo, que é um grupo que inclui todos os usuários.
-   \_Proprietário criador, que é usado como um espaço reservado em uma ACE herdável. Quando a ACE é herdada, o sistema substitui o \_ SID do proprietário criador pelo SID do criador do objeto.
-   O grupo de administradores para o domínio interno no computador local.

Há [*SIDs conhecidas universais*](/windows/desktop/SecGloss/u-gly), que são significativos em todos os sistemas seguros que usam esse modelo de segurança, incluindo sistemas operacionais diferentes de Windows. além disso, há SIDs bem conhecidos que são significativos apenas em sistemas Windows.

a API Windows define um conjunto de constantes para valores de autoridade de identificador e RID ( [*identificador relativo*](/windows/desktop/SecGloss/r-gly) ) conhecidos. Você pode usar essas constantes para criar SIDs bem conhecidos. O exemplo a seguir combina a autoridade de segurança de Sid e as constantes de RID do mundo de segurança \_ \_ \_ \_ \_ para mostrar o SID conhecido Universal para o grupo especial que representa todos os usuários (todos ou mundo):

S-1-1-0

Este exemplo usa a notação de cadeia de caracteres para SIDs em que S identifica a cadeia de caracteres como um SID, o primeiro 1 é o nível de revisão do SID e os dois dígitos restantes são a autoridade de SID do mundo de segurança \_ e as constantes de RID do mundo de \_ \_ segurança \_ \_ .

Você pode usar a função [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) para criar um Sid, combinando um valor de autoridade de identificador com até oito valores de subautoridade. Por exemplo, para determinar se o usuário conectado é membro de um grupo conhecido específico, chame **AllocateAndInitializeSid** para criar um SID para o grupo bem conhecido e use a função [**equalid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid) para comparar esse SID com os SIDs de grupo no [*token de acesso*](/windows/desktop/SecGloss/a-gly)do usuário. Para obter um exemplo, consulte [pesquisando um SID em um token de acesso em C++](searching-for-a-sid-in-an-access-token-in-c--.md). Você deve chamar a função [**FreeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-freesid) para liberar um SID alocado por **AllocateAndInitializeSid**.

O restante desta seção contém tabelas de SIDs e tabelas bem conhecidas de autoridade de identificador e constantes de subautoridade que você pode usar para criar SIDs bem conhecidos.

A seguir estão alguns [*SIDs conhecidos universais*](/windows/desktop/SecGloss/u-gly).



| SID bem conhecido Universal    | Valor da cadeia de caracteres       | Identifica                                                                                                                                               |
|-----------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| SID nulo<br/>         | S-1-0-0<br/> | Um grupo sem membros. Isso geralmente é usado quando um valor de SID não é conhecido.<br/>                                                                    |
| World (Mundo)<br/>            | S-1-1-0<br/> | Um grupo que inclui todos os usuários.<br/>                                                                                                              |
| Local<br/>            | S-1-2-0<br/> | Usuários que fazem logon em [*terminais*](/windows/desktop/SecGloss/t-gly) localmente (fisicamente) conectados ao sistema.<br/> |
| ID do proprietário criador<br/> | S-1-3-0<br/> | Um identificador de segurança a ser substituído pelo identificador de segurança do usuário que criou um novo objeto. Esse SID é usado em ACEs herdáveis.<br/>   |
| ID do grupo criador<br/> | S-1-3-1<br/> | Um identificador de segurança a ser substituído pelo SID do grupo primário do usuário que criou um novo objeto. Use esse SID em ACEs herdáveis.<br/>         |



 

A tabela a seguir lista as constantes de autoridade de identificador predefinidas. Os quatro primeiros valores são usados com SIDs comuns e conhecidos; o último valor é usado com Windows SIDs conhecidos.



| Autoridade de identificador                         | Valor        | Valor da cadeia de caracteres |
|----------------------------------------------|--------------|-------------------|
| \_autoridade de \_ SID \_ nula de segurança<br/>    | 0<br/> | S-1-0<br/>  |
| \_autoridade de \_ SID do mundo de segurança \_<br/>   | 1<br/> | S-1-1<br/>  |
| \_autoridade de \_ SID \_ local de segurança<br/>   | 2<br/> | S-1-2<br/>  |
| \_autoridade de \_ SID do criador de segurança \_<br/> | 3<br/> | S-1-3<br/>  |
| autoridade de segurança \_ NT \_<br/>           | 5<br/> | S-1-5<br/>  |



 

Os valores de [*RID*](/windows/desktop/SecGloss/r-gly) a seguir são usados com [*SIDs comuns conhecidos*](/windows/desktop/SecGloss/u-gly). A coluna autoridade de identificador mostra o prefixo da autoridade de identificador com a qual você pode combinar o RID para criar um SID universal conhecido.



| Autoridade de identificador relativa            | Valor        | Valor da cadeia de caracteres |
|------------------------------------------|--------------|----------------------|
| \_RID nulo de segurança \_<br/>           | 0<br/> | S-1-0<br/>     |
| \_RID do mundo de segurança \_<br/>          | 0<br/> | S-1-1<br/>     |
| \_RID local de segurança \_<br/>          | 0<br/> | S-1-2<br/>     |
| \_RID de \_ logon \_ local de segurança<br/>   | 1<br/> | S-1-2<br/>     |
| \_RID do \_ proprietário do criador de segurança \_<br/> | 0<br/> | S-1-3<br/>     |
| \_RID do \_ grupo \_ criador de segurança<br/> | 1<br/> | S-1-3<br/>     |



 

a \_ autoridade de \_ identificador predefinida da autoridade de segurança NT (S-1-5) produz SIDs que não são universais, mas são significativas apenas em instalações Windowss. Você pode usar os valores de RID a seguir com a \_ \_ Autoridade NT de segurança para criar SIDs bem conhecidos.



| Constante                                          | Valor da cadeia de caracteres               | Identifica                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_RID de discagem de segurança \_<br/>                  | S-1-5-1<br/>         | Usuários que fazem logon em [*terminais*](/windows/desktop/SecGloss/t-gly) usando um modem dial-up. Este é um identificador de grupo.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| \_RID de rede de segurança \_<br/>                 | S-1-5-2<br/>         | Usuários que fazem logon em uma rede. Esse é um identificador de grupo adicionado ao token de um processo quando ele foi conectado em uma rede. O tipo de logon correspondente é \_ rede de logon do LOGON32 \_ .<br/>                                                                                                                                                                                                                                                                                                                      |
| RID \_ DO LOTE DE \_ SEGURANÇA<br/>                   | S-1-5-3<br/>         | Usuários que fazem logoff usando um recurso de fila em lotes. Esse é um identificador de grupo adicionado ao token de um processo quando ele foi registrado como um trabalho em lotes. O tipo de logon correspondente é LOGON32 \_ LOGON \_ BATCH.<br/>                                                                                                                                                                                                                                                                                                                 |
| SECURITY \_ INTERACTIVE \_ RID<br/>             | S-1-5-4<br/>         | Usuários que fizerem logoff para uma operação interativa. Esse é um identificador de grupo adicionado ao token de um processo quando ele foi conectado interativamente. O tipo de logon correspondente é LOGON32 \_ LOGON \_ INTERATIVO.<br/>                                                                                                                                                                                                                                                                                                            |
| \_IDS DE \_ LOGON DE SEGURANÇA \_ RID<br/>              | S-1-5-5-*X* - *Y*<br/> | Uma sessão de logon. Isso é usado para garantir que [*somente*](/windows/desktop/SecGloss/p-gly) os processos em uma determinada sessão de logon possam obter acesso aos objetos de estação de janela para essa sessão. Os *valores X* e *Y* para esses SIDs são diferentes para cada sessão de logon. O valor SECURITY LOGON IDS RID COUNT é o número de \_ \_ RIDs neste \_ \_ identificador (5-*X* - *Y*).<br/>                                                                                                                   |
| SERVIÇO \_ DE \_ SEGURANÇA RID<br/>                 | S-1-5-6<br/>         | Contas autorizadas a fazer logoff como um serviço. Esse é um identificador de grupo adicionado ao token de um processo quando ele foi registrado como um serviço. O tipo de logon correspondente é LOGON32 \_ LOGON \_ SERVICE.<br/>                                                                                                                                                                                                                                                                                                                    |
| SEGURANÇA \_ ANÔNIMA \_ LOGON \_ RID<br/>        | S-1-5-7<br/>         | Logon anônimo ou logon de sessão nulo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| PROXY \_ DE \_ SEGURANÇA RID<br/>                   | S-1-5-8<br/>         | Proxy.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| SECURITY \_ ENTERPRISE \_ CONTROLLERS \_ RID<br/> | S-1-5-9<br/>         | Enterprise controladores.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| AUTO \_ RID DA ENTIDADE DE \_ \_ SEGURANÇA<br/>         | S-1-5-10<br/>        | O \_ identificador de segurança PRINCIPAL SELF pode ser usado na ACL de um objeto de usuário ou grupo. Durante uma verificação de acesso, o sistema substitui o SID pelo SID do objeto . O PRINCIPAL SELF SID é útil para especificar uma ACE herdável que se aplica ao objeto de usuário ou grupo \_ que herda a ACE. É a única maneira de representar o SID de um objeto criado no [*descritor de*](/windows/desktop/SecGloss/s-gly) segurança padrão do esquema.<br/> |
| SEGURANÇA \_ DO USUÁRIO \_ \_ AUTENTICADO RID<br/>     | S-1-5-11<br/>        | Os usuários autenticados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| RID \_ DE CÓDIGO RESTRITO DE \_ \_ SEGURANÇA<br/>        | S-1-5-12<br/>        | Código restrito.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| RID DO \_ SERVIDOR DO TERMINAL DE \_ \_ SEGURANÇA<br/>        | S-1-5-13<br/>        | Serviços de Terminal. Adicionado automaticamente ao token de segurança de um usuário que faz logor em um servidor de terminal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| RID DO \_ SISTEMA LOCAL \_ DE \_ SEGURANÇA<br/>           | S-1-5-18<br/>        | Uma conta especial usada pelo sistema operacional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| SECURITY \_ NT \_ NON \_ UNIQUE<br/>              | S-1-5-21<br/>        | SIDS não são exclusivos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SECURITY \_ BUILTIN \_ DOMAIN \_ RID<br/>         | S-1-5-32<br/>        | O domínio do sistema integrado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| RID \_ DE CÓDIGO RESTRITO DE GRAVAÇÃO DE \_ \_ \_ SEGURANÇA<br/> | S-1-5-33<br/>        | Escrever código restrito.<br/> |


 

Os RIDs a seguir são relativos a cada domínio.



| RID                                                                | Valor       | Identifica                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GRUPO DE ACESSO DCOM RID \_ \_ \_ CERTSVC DO ALIAS \_ \_ DE \_ DOMÍNIO<br/>              | 0x0000023E | O grupo de usuários que podem se conectar a autoridades de certificação usando o DCOM (Distributed Component Object Model).<br/>                                                                                                                          |
| ADMINISTRADOR \_ DE RID DO USUÁRIO DO \_ \_ DOMÍNIO<br/>                                      | 0x000001F4 | A conta de usuário administrativo em um domínio.<br/>                                                                                                                                                                                              |
| CONVIDADO \_ DE RID DO USUÁRIO DO \_ \_ DOMÍNIO<br/>                                      | 0x000001F5 | A conta de usuário convidado em um domínio. Os usuários que não têm uma conta podem fazer logoff automaticamente nessa conta.<br/>                                                                                                                            |
| ADMINISTRADORES \_ RID DO GRUPO DE \_ \_ DOMÍNIO<br/>                                    | 0x00000200 | O grupo de administradores de domínio. Essa conta existe somente em sistemas que executam sistemas operacionais de servidor.<br/>                                                                                                                                   |
| USUÁRIOS \_ RID DO GRUPO DE \_ \_ DOMÍNIO<br/>                                     | 0x00000201 | Um grupo que contém todas as contas de usuário em um domínio. Todos os usuários são adicionados automaticamente a esse grupo.<br/>                                                                                                                                     |
| CONVIDADOS \_ RID DO GRUPO DE \_ \_ DOMÍNIO<br/>                                    | 0x00000202 | A conta do grupo de convidados em um domínio.<br/>                                                                                                                                                                                                      |
| RID \_ COMPUTERS DO GRUPO DE \_ \_ DOMÍNIOS<br/>                                 | 0x00000203 | O grupo de computadores de domínio. Todos os computadores no domínio são membros desse grupo.<br/>                                                                                                                                                       |
| CONTROLADORES \_ RID DO GRUPO DE \_ \_ DOMÍNIO<br/>                               | 0x00000204 | O grupo dos controladores de domínio. Todos os controladores de domínio são membros desse grupo.<br/>                                                                                                                                                           |
| ADMINISTRADORES \_ DE CERTIFICADO RID DO GRUPO DE \_ \_ \_ DOMÍNIO<br/>                              | 0x00000205 | O grupo de editores de certificados. Os computadores que executam os Serviços de Certificados são membros desse grupo.<br/>                                                                                                                                      |
| GRUPO \_ DE \_ \_ DOMÍNIOS RID ENTERPRISE \_ READONLY \_ DOMAIN \_ CONTROLLERS<br/> | 0x000001F2 | O grupo de controladores de domínio somente leitura empresariais.<br/>                                                                                                                                                                                     |
| ADMINISTRADORES DE ESQUEMA DE RID DO GRUPO \_ \_ DE \_ \_ DOMÍNIO<br/>                            | 0x00000206 | O grupo de administradores de esquema. Os membros desse grupo podem modificar o esquema do Active Directory.<br/>                                                                                                                                           |
| GRUPO \_ DE \_ DOMÍNIOS RID ENTERPRISE \_ \_ ADMINS<br/>                        | 0x00000207 | O grupo de administradores corporativos. Os membros desse grupo têm acesso completo a todos os domínios na floresta do Active Directory. Enterprise administradores são responsáveis por operações no nível da floresta, como adicionar ou remover novos domínios.<br/> |
| ADMINISTRADORES \_ DE POLÍTICA DE RID DO GRUPO DE \_ \_ \_ DOMÍNIO<br/>                            | 0x00000208 | O grupo de administradores de política.<br/>                                                                                                                                                                                                         |
| \_CONTROLADORES \_ \_ READONLY RID DO GRUPO \_ DE DOMÍNIO<br/>                     | 0x00000209 | O grupo de controladores de domínio somente leitura.<br/>                                                                                                                                                                                                |                                             
| CONTROLADORES CLONÁVEIS RID DO GRUPO \_ \_ DE \_ \_ DOMÍNIO<br />                   | 0x0000020A | O grupo de controladores de domínio clonáveis.<br/>                                                                                                                                                                                                |
| GRUPO \_ DE DOMÍNIO RID CDC \_ \_ \_ RESERVADO<br />                            | 0x0000020C | O grupo CDC reservado.<br/>                                                                                                                                                                                                                   |
| GRUPO \_ DE \_ DOMÍNIOS RID \_ PROTECTED \_ USERS<br />                         | 0x0000020D | O grupo de usuários protegidos.</br>                                                                                                                                                                                                                |
| ADMINISTRADORES \_ DE CHAVE DE RID DO GRUPO DE \_ \_ \_ DOMÍNIO<br />                              | 0x0000020E | O grupo de administradores principais.<br/>                                                                                                                                                                                                                     |
| GRUPO \_ DE \_ DOMÍNIOS RID ENTERPRISE KEY \_ \_ \_ ADMINS<br />                  | 0x0000020F | O grupo de administradores de chaves corporativas</br>                                                                                                                                                                                                           |



 

Os RIDs a seguir são usados para especificar o nível de integridade obrigatório.



| RID                                                     | Valor                                               | Identifica                        |
|---------------------------------------------------------|-----------------------------------------------------|-----------------------------------|
| RID \_ \_ NÃOTRUSTED OBRIGATÓRIO DE \_ SEGURANÇA<br/>          | 0x00000000<br/>                               | Untrusted.<br/>             |
| LOW \_ \_ RID OBRIGATÓRIO DE \_ SEGURANÇA<br/>                | 0x00001000<br/>                               | Baixa integridade.<br/>         |
| MEIO \_ RID OBRIGATÓRIO DE \_ \_ SEGURANÇA<br/>             | 0x00002000<br/>                               | Integridade média.<br/>      |
| MÍDIA \_ OBRIGATÓRIA DE SEGURANÇA MAIS \_ \_ \_ RID<br/>       | SEGURANÇA \_ OBRIGATÓRIA DE MÉDIA RID + \_ \_ 0x100<br/> | Integridade média alta.<br/> |
| ALTA \_ \_ RID OBRIGATÓRIA DE \_ SEGURANÇA<br/>               | 0X00003000<br/>                               | Alta integridade.<br/>        |
| RID \_ DO SISTEMA OBRIGATÓRIO DE \_ \_ SEGURANÇA<br/>             | 0x00004000<br/>                               | Integridade do sistema.<br/>      |
| PROCESSO \_ \_ PROTEGIDO DE SEGURANÇA OBRIGATÓRIO \_ \_ RID<br/> | 0x00005000<br/>                               | Processo protegido.<br/>     |



 

A tabela a seguir tem exemplos de RIDs relativos ao domínio que você pode usar para formar SIDs conhecidos para grupos locais (aliases). Para obter mais informações sobre grupos locais e globais, consulte [Funções de grupo local](/windows/desktop/NetMgmt/local-group-functions) e Funções de [grupo](/windows/desktop/NetMgmt/group-functions).



| RID                                                              | Valor                 |Valor da cadeia de caracteres  | Identifica                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADMINISTRADORES \_ RID DO ALIAS DE \_ \_ DOMÍNIO<br/>                            | 0x00000220<br/> | S-1-5-32-544<br/> | Um grupo local usado para administração do domínio.<br/>                                                                                                                                                                                                                            |
| USUÁRIOS \_ DE ALIAS DE DOMÍNIO \_ \_ RID<br/>                             | 0x00000221<br/> | S-1-5-32-545<br/> | Um grupo local que representa todos os usuários no domínio.<br/>                                                                                                                                                                                                                          |
| CONVIDADOS \_ DE RID DO ALIAS DE \_ \_ DOMÍNIO<br/>                            | 0x00000222<br/> | S-1-5-32-546<br/> | Um grupo local que representa os convidados do domínio.<br/>                                                                                                                                                                                                                             |
| ALIAS \_ DE DOMÍNIO RID POWER \_ \_ \_ USERS<br/>                      | 0x00000223<br/> | S-1-5-32-547<br/> | Um grupo local usado para representar um usuário ou um conjunto de usuários que esperam tratar um sistema como se fosse seu computador pessoal, em vez de como uma estação de trabalho para vários usuários.<br/>                                                                                                      |
| OPERAÇÕES \_ DE CONTA DE RID DO ALIAS DE \_ \_ \_ DOMÍNIO<br/>                      | 0x00000224<br/> | S-1-5-32-548<br/> | Um grupo local que existe somente em sistemas que executam sistemas operacionais de servidor. Esse grupo local permite o controle sobre contas não administrativas.<br/>                                                                                                                                    |
| OPERAÇÕES \_ DO SISTEMA DE RID DO ALIAS DE \_ \_ \_ DOMÍNIO<br/>                       | 0x00000225<br/> | S-1-5-32-549<br/> | Um grupo local que existe somente em sistemas que executam sistemas operacionais de servidor. Esse grupo local executa funções administrativas do sistema, não incluindo funções de segurança. Ele estabelece compartilhamentos de rede, controla impressoras, desbloqueia estações de trabalho e executa outras operações.<br/> |
| OPERAÇÕES \_ DE IMPRESSÃO DE RID DO ALIAS DE \_ \_ \_ DOMÍNIO<br/>                        | 0x00000226<br/> | S-1-5-32-550<br/> | Um grupo local que existe somente em sistemas que executam sistemas operacionais de servidor. Esse grupo local controla impressoras e filas de impressão.<br/>                                                                                                                                                |
| OPERAÇÕES \_ DE BACKUP DE RID DO ALIAS DE \_ \_ \_ DOMÍNIO<br/>                       | 0x00000227<br/> | S-1-5-32-551<br/> | Um grupo local usado para controlar a atribuição de privilégios de backup e restauração de arquivo.<br/>                                                                                                                                                                                            |
| REPLICADOR \_ DE RID DO ALIAS DE \_ \_ DOMÍNIO<br/>                        | 0x00000228<br/> | S-1-5-32-552<br/> | Um grupo local responsável por copiar bancos de dados de segurança do controlador de domínio primário para os controladores de domínio de backup. Essas contas são usadas apenas pelo sistema.<br/>                                                                                                       |
| \_ \_ Servidores RAS de RID do alias de \_ domínio \_<br/>                      | 0x00000229<br/> | S-1-5-32-553<br/> | Um grupo local que representa servidores RAS e IAS. Esse grupo permite o acesso a vários atributos de objetos de usuário.<br/>                                                                                                                                                             |
| \_PREW2KCOMPACCESS de \_ RID do alias de domínio \_<br/>                  | 0x0000022A<br/> | S-1-5-32-554<br/> | um grupo local que existe somente em sistemas que executam Windows servidor 2000. Para obter mais informações, consulte [permitindo acesso anônimo](allowing-anonymous-access.md).<br/>                                                                                                                    |
| \_ \_ \_ \_ usuário da área de trabalho remota do RID do alias de domínio \_<br/>            | 0x0000022B<br/> | S-1-5-32-555<br/> | Um grupo local que representa todos os usuários da área de trabalho remota.<br/>                                                                                                                                                                                                                         |
| \_operações de \_ configuração de rede de RID de alias de \_ \_ domínio \_<br/>       | 0x0000022C<br/> | S-1-5-32-556<br/> | Um grupo local que representa a configuração de rede. <br/>                                                                                                                                                                                                                       |
| \_construtores de \_ \_ confiança de floresta de entrada de RID \_ de \_ alias de domínio \_<br/> | 0x0000022D<br/> | S-1-5-32-557<br/> | Um grupo local que representa qualquer usuário de relação de confiança de floresta.<br/>                                                                                                                                                                                                                           |
| \_usuários de \_ monitoramento de RID do alias de domínio \_ \_<br/>                 | 0x0000022E<br/> | S-1-5-32-558<br/> | Um grupo local que representa todos os usuários que estão sendo monitorados.<br/>                                                                                                                                                                                                                        |
| \_usuários de \_ log de RID de alias de domínio \_ \_<br/>                    | 0x0000022F<br/> | S-1-5-32-559<br/> | Um grupo local responsável por registrar usuários em log.<br/>                                                                                                                                                                                                                                    |
| \_AUTHORIZATIONACCESS de \_ RID do alias de domínio \_<br/>               | 0x00000230<br/> | S-1-5-32-560<br/> | Um grupo local que representa todo o acesso autorizado.<br/>                                                                                                                                                                                                                            |
| \_servidores de \_ licença do RID do alias de domínio \_ \_ \_<br/>              | 0x00000231<br/> | S-1-5-32-561<br/> | Um grupo local que existe somente em sistemas que executam sistemas operacionais de servidor que permitem serviços de terminal e acesso remoto.<br/>                                                                                                                                                  |
| usuários do RID do alias de domínio \_ \_ \_ DCOM \_<br/>                       | 0x00000232<br/> | S-1-5-32-562<br/> | Um grupo local que representa os usuários que podem usar o Distributed Component Object Model (DCOM).<br/>                                                                                                                                                                                      |
| \_IUSERS de \_ RID do alias de domínio \_<br/>                            | 0X00000238<br/> | S-1-5-32-568<br/> | Um grupo local que representa os usuários da Internet.<br/>                                                                                                                                                                                                                                   |
| \_operadores de \_ \_ criptografia RID do alias \_ de domínio<br/>                 | 0x00000239<br/> | S-1-5-32-569<br/> | Um grupo local que representa o acesso aos operadores de criptografia.<br/>                                                                                                                                                                                                                 |
| \_grupo de \_ entidades de \_ \_ segurança em cache do RID \_ do alias de domínio<br/>      | 0x0000023B<br/> | S-1-5-32-571<br/> | Um grupo local que representa as entidades de segurança que podem ser armazenadas em cache.<br/>                                                                                                                                                                                                                    |
| \_grupo de \_ entidades \_ de \_ segurança não armazenáveis no RID \_ do alias de domínio \_<br/> | 0x0000023C<br/> | S-1-5-32-572<br/> | Um grupo local que representa as entidades que não podem ser armazenadas em cache.<br/>                                                                                                                                                                                                                 |
| \_grupo de \_ \_ leitores de log de eventos do RID \_ de \_ alias de domínio \_<br/>        | 0x0000023D<br/> | S-1-5-32-573<br/> | Um grupo local que representa os leitores do log de eventos.<br/>                                                                                                                                                                                                                                |
| \_grupo de \_ \_ \_ \_ acesso \_ do RID do alias de domínio<br/>      | 0x0000023E<br/> | S-1-5-32-574<br/> | O grupo local de usuários que podem se conectar a autoridades de certificação usando o Distributed Component Object Model (DCOM).<br/>                                                                                                                                                          |
| \_servidor de \_ \_ \_ acesso remoto de \_ RDS \_ do alias de domínio<br />     | 0x0000023F<br/> | S-1-5-32-575<br/> | Um grupo local que representa os servidores de acesso remoto do RDS.<br/> |
| \_servidores de \_ ponto \_ de \_ extremidade \_ RDS do alias de domínio                 | 0x00000240<br/> | S-1-5-32-576<br/> | Um grupo local que representa servidores de ponto de extremidade.<br/> |
| \_servidores de \_ \_ Gerenciamento de \_ RDS \_ do alias de domínio               | 0x00000241<br/> | S-1-5-32-577<br/> | Um grupo local que representa servidores de gerenciamento. <br/>|
| Admins do alias de domínio do \_ \_ Hyper- \_ \_ V \_                       | 0x00000242<br/> | S-1-5-32-578<br/> | Um grupo local que representa administradores do Hyper-v <br/>|
| \_operações de \_ \_ assistência de controle de acesso RID \_ \_ de alias de domínio \_       | 0x00000243<br/> | S-1-5-32-579<br/> | Um grupo local que representa as operações de assistência de controle de acesso.<br/> |
| \_usuários de \_ \_ gerenciamento remoto \_ de RID de alias de \_ domínio              | 0x00000244<br/> | S-1-5-32-580<br/> | Um grupo local que representa usuários de gerenciamento remoto. <br/>|
| \_ \_ conta padrão de RID do alias de \_ domínio \_                       | 0x00000245<br/> | S-1-5-32-581<br/> | Um grupo local que representa a conta padrão. <br/>|
| \_Administradores de \_ réplica de armazenamento de RID do alias de \_ \_ domínio \_               | 0x00000246<br/> | S-1-5-32-582<br/> | Um grupo local que representa administradores de réplica de armazenamento. <br/>|
| \_proprietários do \_ \_ dispositivo RID do alias \_ de domínio                            | 0x00000247<br/> | S-1-5-32-583<br/> | Um grupo local que representa pode fazer as configurações esperadas para Os Proprietários do Dispositivo.<br/>|


 

A [**\_ enumeração WELL KNOWN \_ SID \_ TYPE**](/windows/desktop/api/Winnt/ne-winnt-well_known_sid_type) define a lista de SIDs comumente usados. Além disso, a SDDL [(Linguagem](security-descriptor-definition-language.md) de Definição do Descritor de Segurança) usa cadeias de [caracteres SID](sid-strings.md) para referenciar SIDs conhecidos em um formato de cadeia de caracteres.

 

