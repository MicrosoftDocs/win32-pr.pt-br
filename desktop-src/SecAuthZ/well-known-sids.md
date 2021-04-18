---
description: SIDs (identificadores de segurança) conhecidos identificam grupos genéricos e usuários genéricos.
ms.assetid: eb2f95c4-9465-409b-b76c-9ccae1d05eda
title: SIDs bem conhecidos
ms.topic: article
ms.date: 03/04/2020
ms.custom: 19H1
ms.openlocfilehash: 1fdde933b3e4f844e63785ff130aaf89204fe0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780928"
---
# <a name="well-known-sids"></a>SIDs bem conhecidos

SIDs ( [*identificadores de segurança*](/windows/desktop/SecGloss/s-gly) ) conhecidos identificam grupos genéricos e usuários genéricos. Por exemplo, há SIDs bem conhecidos para identificar os seguintes grupos e usuários:

-   Todos ou mundo, que é um grupo que inclui todos os usuários.
-   \_Proprietário criador, que é usado como um espaço reservado em uma ACE herdável. Quando a ACE é herdada, o sistema substitui o \_ SID do proprietário criador pelo SID do criador do objeto.
-   O grupo de administradores para o domínio interno no computador local.

Há [*SIDs conhecidas universais*](/windows/desktop/SecGloss/u-gly), que são significativos em todos os sistemas seguros que usam esse modelo de segurança, incluindo sistemas operacionais diferentes do Windows. Além disso, há SIDs bem conhecidos que são significativos apenas em sistemas Windows.

A API do Windows define um conjunto de constantes para valores conhecidos de autoridade de identificador e RID ( [*identificador relativo*](/windows/desktop/SecGloss/r-gly) ). Você pode usar essas constantes para criar SIDs bem conhecidos. O exemplo a seguir combina a autoridade de segurança de Sid e as constantes de RID do mundo de segurança \_ \_ \_ \_ \_ para mostrar o SID conhecido Universal para o grupo especial que representa todos os usuários (todos ou mundo):

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



 

A tabela a seguir lista as constantes de autoridade de identificador predefinidas. Os quatro primeiros valores são usados com SIDs comuns e conhecidos; o último valor é usado com SIDs conhecidos do Windows.



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



 

A \_ autoridade de \_ identificador predefinida da autoridade de segurança NT (S-1-5) produz SIDs que não são universais, mas são significativas apenas em instalações do Windows. Você pode usar os valores de RID a seguir com a \_ \_ Autoridade NT de segurança para criar SIDs bem conhecidos.



| Constante                                          | Valor da cadeia de caracteres               | Identifica                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_RID de discagem de segurança \_<br/>                  | S-1-5-1<br/>         | Usuários que fazem logon em [*terminais*](/windows/desktop/SecGloss/t-gly) usando um modem dial-up. Este é um identificador de grupo.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| \_RID de rede de segurança \_<br/>                 | S-1-5-2<br/>         | Usuários que fazem logon em uma rede. Esse é um identificador de grupo adicionado ao token de um processo quando ele foi conectado em uma rede. O tipo de logon correspondente é \_ rede de logon do LOGON32 \_ .<br/>                                                                                                                                                                                                                                                                                                                      |
| \_RID do lote de segurança \_<br/>                   | S-1-5-3<br/>         | Usuários que fazem logon usando um recurso de fila do lote. Esse é um identificador de grupo adicionado ao token de um processo quando ele foi registrado como um trabalho em lotes. O tipo de logon correspondente é LOGON32 \_ logon \_ Batch.<br/>                                                                                                                                                                                                                                                                                                                 |
| \_RID interativo de segurança \_<br/>             | S-1-5-4<br/>         | Usuários que fazem logon para operação interativa. Esse é um identificador de grupo adicionado ao token de um processo quando ele foi conectado interativamente. O tipo de logon correspondente é LOGON32 \_ logon \_ interativo.<br/>                                                                                                                                                                                                                                                                                                            |
| \_RID de \_ IDs de logon de segurança \_<br/>              | S-1-5-5-*X* - *Y*<br/> | Uma sessão de logon. Isso é usado para garantir que somente os [*processos*](/windows/desktop/SecGloss/p-gly) em uma sessão de logon específica possam obter acesso aos objetos de estação de janela para essa sessão. Os valores *X* e *Y* para esses SIDs são diferentes para cada sessão de logon. A contagem de RID das IDs de logon de segurança do valor \_ \_ \_ \_ é o número de RIDs neste identificador (5 *X* - *Y*).<br/>                                                                                                                   |
| \_RID do serviço de segurança \_<br/>                 | S-1-5-6<br/>         | Contas autorizadas a fazer logon como um serviço. Esse é um identificador de grupo adicionado ao token de um processo quando ele foi registrado como um serviço. O tipo de logon correspondente é \_ serviço de logon do LOGON32 \_ .<br/>                                                                                                                                                                                                                                                                                                                    |
| \_RID de \_ logon \_ anônimo de segurança<br/>        | S-1-5-7<br/>         | Logon anônimo ou logon de sessão nula.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_RID do proxy de segurança \_<br/>                   | S-1-5-8<br/>         | Acionista.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| \_RID dos \_ controladores corporativos de segurança \_<br/> | S-1-5-9<br/>         | Controladores corporativos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_auto- \_ \_ RID de entidade de segurança<br/>         | S-1-5-10<br/>        | O \_ identificador de autosegurança principal pode ser usado na ACL de um objeto de usuário ou grupo. Durante uma verificação de acesso, o sistema substitui o SID pelo SID do objeto. O próprio SID de entidade de segurança \_ é útil para especificar uma ACE herdável que se aplica ao objeto de usuário ou grupo que herda a Ace. Ele é a única maneira de representar o SID de um objeto criado no [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) padrão do esquema.<br/> |
| \_RID do usuário autenticado de segurança \_ \_<br/>     | S-1-5-11<br/>        | Os usuários autenticados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_RID de \_ código \_ restrito de segurança<br/>        | S-1-5-12<br/>        | Código restrito.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SEGURANÇA \_ de \_ RID do Terminal Server \_<br/>        | S-1-5-13<br/>        | Serviços de terminal. Adicionado automaticamente ao token de segurança de um usuário que faz logon em um servidor de terminal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_RID do \_ sistema \_ local de segurança<br/>           | S-1-5-18<br/>        | Uma conta especial usada pelo sistema operacional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| SEGURANÇA \_ NT \_ não \_ exclusiva<br/>              | S-1-5-21<br/>        | Os SIDS não são exclusivos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| \_RID de \_ domínio \_ interno de segurança<br/>         | S-1-5-32<br/>        | O domínio do sistema interno.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| \_RID de \_ \_ código restrito de gravação \_ de segurança<br/> | S-1-5-33<br/>        | Escreva código restrito.<br/> |


 

Os RIDs a seguir são relativos a cada domínio.



| RID                                                                | Valor       | Identifica                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_grupo de \_ \_ \_ \_ acesso \_ do RID do alias de domínio<br/>              | 0x0000023E | O grupo de usuários que podem se conectar a autoridades de certificação usando o Distributed Component Object Model (DCOM).<br/>                                                                                                                          |
| \_administrador de \_ RID do usuário de domínio \_<br/>                                      | 0x000001F4 | A conta de usuário administrativo em um domínio.<br/>                                                                                                                                                                                              |
| \_convidado de \_ RID do usuário de domínio \_<br/>                                      | 0x000001F5 | A conta de usuário convidado em um domínio. Os usuários que não têm uma conta podem fazer logon automaticamente nessa conta.<br/>                                                                                                                            |
| \_Administradores de \_ RID do grupo de domínio \_<br/>                                    | 0x00000200 | O grupo de administradores de domínio. Essa conta existe apenas em sistemas que executam sistemas operacionais de servidor.<br/>                                                                                                                                   |
| usuários do grupo de domínio \_ \_ RID \_<br/>                                     | 0x00000201 | Um grupo que contém todas as contas de usuário em um domínio. Todos os usuários são adicionados automaticamente a esse grupo.<br/>                                                                                                                                     |
| grupo de domínio \_ \_ convidados do RID \_<br/>                                    | 0x00000202 | A conta do grupo convidado em um domínio.<br/>                                                                                                                                                                                                      |
| \_ \_ computadores RID do grupo de domínio \_<br/>                                 | 0x00000203 | O grupo de computadores do domínio. Todos os computadores no domínio são membros deste grupo.<br/>                                                                                                                                                       |
| \_ \_ controladores RID do grupo de domínio \_<br/>                               | 0x00000204 | O grupo de controladores de domínio. Todos os DCs no domínio são membros desse grupo.<br/>                                                                                                                                                           |
| \_Administradores de \_ \_ certificado RID do grupo \_ de domínio<br/>                              | 0x00000205 | O grupo de Publicadores de certificado. Os computadores que executam os serviços de certificados são membros deste grupo.<br/>                                                                                                                                      |
| \_controladores de \_ \_ \_ domínio somente leitura \_ \_ do grupo de domínio RID corporativo<br/> | 0x000001F2 | O grupo de controladores de domínio somente leitura corporativos.<br/>                                                                                                                                                                                     |
| \_Administradores de \_ \_ esquema RID do grupo \_ de domínio<br/>                            | 0x00000206 | O grupo de administradores de esquema. Os membros desse grupo podem modificar o esquema do Active Directory.<br/>                                                                                                                                           |
| \_ \_ \_ administradores corporativos de RID do grupo de domínio \_<br/>                        | 0x00000207 | O grupo de administradores corporativos. Os membros desse grupo têm acesso completo a todos os domínios na floresta Active Directory. Os administradores corporativos são responsáveis por operações em nível de floresta, como adicionar ou remover novos domínios.<br/> |
| \_Administradores de \_ política de RID do grupo de domínio \_ \_<br/>                            | 0x00000208 | O grupo de administradores de política.<br/>                                                                                                                                                                                                         |
| \_ \_ \_ controladores somente leitura do RID do grupo de domínio \_<br/>                     | 0x00000209 | O grupo de controladores de domínio somente leitura.<br/>                                                                                                                                                                                                |                                             
| \_controladores de \_ RID \_ clonáveis de grupo \_ de domínio<br />                   | 0x0000020A | O grupo de controladores de domínio clonáveis.<br/>                                                                                                                                                                                                |
| CDC do RID do grupo de domínio \_ \_ \_ \_ reservado<br />                            | 0x0000020C | O grupo CDC reservado.<br/>                                                                                                                                                                                                                   |
| \_ \_ \_ usuários protegidos por RID do grupo de domínio \_<br />                         | 0x0000020D | O grupo de usuários protegidos.</br>                                                                                                                                                                                                                |
| \_Administradores de \_ chave de RID do grupo de domínio \_ \_<br />                              | 0x0000020E | O grupo de administradores de chaves.<br/>                                                                                                                                                                                                                     |
| grupo de domínio \_ \_ RID \_ Enterprise \_ Key \_ Admins<br />                  | 0x0000020F | O grupo Administradores de chave corporativa</br>                                                                                                                                                                                                           |



 

Os RIDs a seguir são usados para especificar o nível de integridade obrigatório.



| RID                                                     | Valor                                               | Identifica                        |
|---------------------------------------------------------|-----------------------------------------------------|-----------------------------------|
| \_ \_ RID não confiável obrigatório de \_ segurança<br/>          | 0x00000000<br/>                               | Não confiável.<br/>             |
| SEGURANÇA \_ \_ baixa de \_ RID obrigatório<br/>                | 0x00001000<br/>                               | Baixa integridade.<br/>         |
| SEGURANÇA \_ de \_ RID médio obrigatório \_<br/>             | 0x00002000<br/>                               | Integridade média.<br/>      |
| SEGURANÇA \_ obrigatória \_ média \_ mais \_ RID<br/>       | SEGURANÇA \_ de \_ RID médio obrigatório \_ + 0x100<br/> | Alta integridade média.<br/> |
| SEGURANÇA \_ \_ alta de \_ RID obrigatório<br/>               | 0X00003000<br/>                               | Alta integridade.<br/>        |
| \_RID de \_ sistema \_ obrigatório de segurança<br/>             | 0x00004000<br/>                               | Integridade do sistema.<br/>      |
| \_RID de \_ \_ processo protegido obrigatório de \_ segurança<br/> | 0x00005000<br/>                               | Processo protegido.<br/>     |



 

A tabela a seguir tem exemplos de RIDs relativos a domínio que você pode usar para formar SIDs conhecidos para grupos locais (aliases). Para obter mais informações sobre grupos locais e globais, consulte funções do grupo [local](/windows/desktop/NetMgmt/local-group-functions) e [funções de grupo](/windows/desktop/NetMgmt/group-functions).



| RID                                                              | Valor                 |Valor da cadeia de caracteres  | Identifica                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ Administradores RID de alias de domínio \_<br/>                            | 0x00000220<br/> | S-1-5-32-544<br/> | Um grupo local usado para administração do domínio.<br/>                                                                                                                                                                                                                            |
| \_ \_ usuários RID do alias de domínio \_<br/>                             | 0x00000221<br/> | S-1-5-32-545<br/> | Um grupo local que representa todos os usuários no domínio.<br/>                                                                                                                                                                                                                          |
| \_convidados de \_ RID do alias de domínio \_<br/>                            | 0x00000222<br/> | S-1-5-32-546<br/> | Um grupo local que representa convidados do domínio.<br/>                                                                                                                                                                                                                             |
| \_ \_ \_ usuários avançados do alias de domínio \_<br/>                      | 0x00000223<br/> | S-1-5-32-547<br/> | Um grupo local usado para representar um usuário ou conjunto de usuários que esperam tratar um sistema como se fosse seu computador pessoal, e não como uma estação de trabalho para vários usuários.<br/>                                                                                                      |
| \_Ops de \_ conta de RID de alias de domínio \_ \_<br/>                      | 0x00000224<br/> | S-1-5-32-548<br/> | Um grupo local que existe somente em sistemas que executam sistemas operacionais de servidor. Esse grupo local permite o controle sobre as contas que não são de administrador.<br/>                                                                                                                                    |
| \_Ops do \_ \_ sistema RID do alias \_ de domínio<br/>                       | 0x00000225<br/> | S-1-5-32-549<br/> | Um grupo local que existe somente em sistemas que executam sistemas operacionais de servidor. Esse grupo local executa funções administrativas do sistema, não incluindo funções de segurança. Ele estabelece compartilhamentos de rede, controla impressoras, desbloqueia estações de trabalho e executa outras operações.<br/> |
| \_operações de \_ \_ impressão RID do alias \_ de domínio<br/>                        | 0x00000226<br/> | S-1-5-32-550<br/> | Um grupo local que existe somente em sistemas que executam sistemas operacionais de servidor. Esse grupo local controla impressoras e filas de impressão.<br/>                                                                                                                                                |
| \_operações de \_ backup de RID de alias de domínio \_ \_<br/>                       | 0x00000227<br/> | S-1-5-32-551<br/> | Um grupo local usado para controlar a atribuição de privilégios de backup e restauração de arquivo.<br/>                                                                                                                                                                                            |
| \_ \_ replicador RID do alias de domínio \_<br/>                        | 0x00000228<br/> | S-1-5-32-552<br/> | Um grupo local responsável por copiar bancos de dados de segurança do controlador de domínio primário para os controladores de domínio de backup. Essas contas são usadas somente pelo sistema.<br/>                                                                                                       |
| \_ \_ Servidores RAS de RID do alias de \_ domínio \_<br/>                      | 0x00000229<br/> | S-1-5-32-553<br/> | Um grupo local que representa servidores RAS e IAS. Esse grupo permite o acesso a vários atributos de objetos de usuário.<br/>                                                                                                                                                             |
| \_PREW2KCOMPACCESS de \_ RID do alias de domínio \_<br/>                  | 0x0000022A<br/> | S-1-5-32-554<br/> | Um grupo local que existe somente em sistemas que executam o Windows 2000 Server. Para obter mais informações, consulte [permitindo acesso anônimo](allowing-anonymous-access.md).<br/>                                                                                                                    |
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
| \_proprietários do \_ \_ dispositivo RID do alias \_ de domínio                            | 0x00000247<br/> | S-1-5-32-583<br/> | Um grupo local que representa o pode tornar as configurações esperadas para os proprietários do dispositivo.<br/>|


 

A enumeração de [**\_ tipo de \_ SID \_ bem conhecida**](/windows/desktop/api/Winnt/ne-winnt-well_known_sid_type) define a lista de SIDs usados com frequência. Além disso, a [linguagem de definição do descritor de segurança](security-descriptor-definition-language.md) (SDDL) usa [cadeias de caracteres de Sid](sid-strings.md) para referenciar SIDs conhecidos em um formato de cadeia de caracteres.

 

