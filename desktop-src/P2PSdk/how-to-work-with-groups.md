---
description: O Grouping ponto a ponto é uma tecnologia que permite que um desenvolvedor crie uma rede de pares segura de maneira rápida e eficaz.
ms.assetid: ee72f60b-1e5b-4b69-bda0-2ae80734c144
title: Como trabalhar com grupos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bce7280afe226fea20cde633a3971f62f606e1814ad4ab62bcc09025a125e72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519386"
---
# <a name="how-to-work-with-groups"></a>Como trabalhar com grupos

O Grouping ponto a ponto é uma tecnologia que permite que um desenvolvedor crie uma rede de pares segura de maneira rápida e eficaz. A lista a seguir identifica as principais considerações na criação de um aplicativo de grupo de pares.

-   [Obtendo uma identidade de par](#obtaining-a-peer-identity)
-   [Iniciando um grupo de pares](#starting-up-the-peer-grouping-infrastructure)
-   [Registrando para agrupar eventos](#registering-for-peer-grouping-events)
-   [Conectando-se a um grupo](#obtaining-a-group-handle)
-   [Criando funções de administrador e membro](#creating-administrator-and-member-roles)
-   [Encontrando um par](#finding-a-peer)
-   [Conectando-se diretamente a um par](#connecting-directly-to-a-peer)
-   [Fechando e desligando um grupo](#closing-and-shutting-down-a-peer-group)

## <a name="obtaining-a-peer-identity"></a>Obtendo uma identidade de par

Antes de criar ou se conectar a um grupo, um par deve obter uma identidade de par, que é um nome usado para identificar exclusivamente um par a um grupo. Para obter uma lista enumerada de todas as identidades de par definidas no par, chame [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities), que retorna um handle para a enumeração . Para obter as identidades de par, [**chame PeerGetNextItem com**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) o alça de enumeração e o número de membros a recuperar. Continue chamando **PeerGetNextItem** até que o parâmetro *pCount* retorne um valor menor que o número de identidades de par solicitadas.

Se uma identidade de par para o par não existir, ela poderá ser criada chamando [**PeerIdentityCriar**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate). Depois de criar uma identidade de par, o par gera um blob XML de identidade que contém a chave pública atribuída a ele

As informações de identidade de par são obtidas chamando [**PeerIdentityGetXML.**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) Essas informações de identidade de par são usadas pelo criador do grupo ou um administrador para emitir as credenciais necessárias para ingressar no grupo, como um blob XML de convite.

Para obter mais informações sobre identidades de pares, consulte a [documentação](identity-manager-api.md) da API do Identity Manager

## <a name="starting-up-the-peer-grouping-infrastructure"></a>Iniciando a infraestrutura de grupo de pares

Antes que qualquer função na API de Grupo de Pares seja chamada por um aplicativo, [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) deve ser chamado. Essa função inicializa a Infraestrutura de Grupo de Pares para o aplicativo e define a versão com suporte.

## <a name="obtaining-a-group-handle"></a>Obtendo um alçamento de grupo

Para se conectar a um grupo e começar a participar, é necessário obter um handle para um grupo par. A lista a seguir identifica as três maneiras de se conectar a um grupo par:

-   Criando um grupo de pares chamando [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), que inicializa um novo grupo de pares e retorna um manipular válido com o par como o proprietário e o administrador exclusivo.
-   Ingressar em um grupo de pares chamando [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin). Para ingressar em um grupo par, um par deve receber um convite de um administrador de grupo par. Para obter um convite, envie o blob XML de informações de identidade para o administrador que cria um convite e envia-o a você por um mecanismo externo, como email ou FTP. O convite e a identidade de par são passados **para PeerGroupJoin**, que retorna um handle válido para o grupo.
-   Abrir um grupo de pares que um par ingressou anteriormente chamando [**PeerGroupA abrir**](/windows/desktop/api/P2P/nf-p2p-peergroupopen). Nessa situação, não é necessário obter um convite.

Depois de obter um alça de grupo de pares válido de uma das funções acima, você pode se conectar a um grupo de pares chamando [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) com o novo handle.

> [!Note]  
> Se a conexão com um grupo par falhar, ocorrerá o evento PEER \_ GROUP \_ EVENT CONNECTION \_ \_ FAILED. O manipulador pode tentar restabelecer a conexão com o grupo par.

 

## <a name="registering-for-peer-grouping-events"></a>Registrando-se para eventos de grupo de pares

Antes que um par participe de um grupo de pares, o par deve se registrar para eventos de grupo par. Para se registrar para eventos de pares específicos, chame [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)e passe um ou mais dos tipos de evento de par definidos em PEER \_ GROUP EVENT \_ \_ TYPE. Você deve se registrar para cada evento par que se aplica ao seu aplicativo; por exemplo, para receber dados por uma conexão direta, registre-se para os eventos CONEXÃO DIRETA DE EVENTO DE GRUPO PAR e DADOS DE ENTRADA DE EVENTO \_ \_ DE GRUPO \_ \_ \_ \_ \_ \_ PAR. Cada chamada recebe um handle de evento e retorna um handle **HPEEREVENT** para esse evento de par.

Manipuladores de eventos podem obter os dados associados a um evento par passando o manipulador para eventos de par registrados para [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata). Esses dados de evento par são retornados como uma união DE DADOS DE EVENTO DE GRUPO \_ \_ \_ PAR. Se a fila de eventos par estiver vazia, essa função retornará PEER \_ S \_ NO EVENT \_ \_ DATA.

Você pode fazer o registro de eventos de par chamando [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) e fornecendo o handle para o evento de par que você deseja desarmá-lo. Depois que a função é chamada, os eventos de par associados ao handle não são mais registrados.

## <a name="creating-administrator-and-member-roles"></a>Criando funções de administrador e membro

O par que cria o grupo de pares é conhecido como o criador do grupo de pares e tem a função de administrador por padrão. Somente o criador do grupo par pode definir as propriedades do grupo.

Os pares convidados para o grupo de pares podem ser um administrador ou um membro. Se eles receberem uma função de administrador pelo administrador que emissão do convite, eles poderão convidar novos membros para o grupo par e atribuir a função de administrador a outros membros.

As funções de membros do grupo de pares são definidas nos convites que o administrador fornece a um membro. Para adicionar mais administradores, de definido o valor do parâmetro *pRoles* [**de PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) como PEER GROUP ROLE ADMIN ao \_ criar um \_ \_ convite.

Os membros podem participar de um grupo par, mas não podem convidar e autorizar novos membros, definir propriedades de grupo ou atualizar ou excluir registros de grupo que eles não criam especificamente. Para atribuir o status de membro a um par participante, de definido o valor do parâmetro **pRoles** de [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) como PEER GROUP ROLE MEMBER ao criar um convite para \_ esse \_ \_ par.

Para alterar a função de um membro, novas credenciais que contêm a nova função devem ser emitidas para esse membro. Para fazer isso, obtenha a estrutura [**PEER \_ CREDENTIAL \_ INFO**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) para esse membro da estrutura PEER \_ MEMBER retornada por [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers). Altere **o campo pRoles** em **PEER CREDENTIAL \_ \_ INFO** para a nova função e passe a estrutura para [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials).

As novas credenciais não entrarão em vigor para o par até que se conectem ao grupo par. Se eles estão conectados no momento, eles devem fechar o grupo e reconectar-se para obter as credenciais atualizadas.

## <a name="finding-a-peer"></a>Encontrando um par

Para obter uma lista enumerada de todos os pares que participam do grupo par, chame [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) com o alça de grupo, que retorna um alça para a enumeração. Para obter os membros, chame [**PeerGetNextItem com**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) o alça de enum e o número de membros a recuperar. Continue chamando **PeerGetNextItem** até que o *parâmetro pCount* retorne um valor menor que o número de membros solicitados. Observe que a lista completa de membros disponíveis pode não ser retornada.

Cada membro é representado como uma estrutura [**PEER \_ MEMBER,**](/windows/desktop/api/P2P/ns-p2p-peer_member) que contém a identidade do par, IDs de nó e endereços IP para pares ativos.

Quando terminar, feche a enumeração e libere a memória associada chamando [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration).

## <a name="connecting-directly-to-a-peer"></a>Conectando-se diretamente a um par

Quando um par está conectado a um grupo de pares, as trocas diretas um-para-um com outros membros conectados são iniciadas chamando [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) e fornecendo a identidade do outro par. Essa chamada é assíncrona e retorna uma ID de conexão de 64 bits. Se a chamada for bem-sucedida, você receberá o evento par PEER \_ GROUP EVENT DIRECT CONNECTION EVENT para indicar que a conexão foi \_ \_ \_ \_ bem-sucedida. Se a conexão for bem-sucedida, a ID da conexão será válida e poderá ser usada para enviar e receber dados por meio da conexão direta.

Para poder receber conexões diretas, o outro par também deve ter sido registrado anteriormente para o evento par PEER \_ GROUP \_ EVENT DIRECT \_ \_ CONNECTION.

Para enviar dados para um par, chame [**PeerGroupSendData com**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) uma ID de conexão válida. Para receber dados, o outro par deve ser registrado para o evento par PEER \_ GROUP \_ EVENT INCOMING \_ \_ DATA. Da mesma forma, se o par de envio quiser receber dados por sua vez, ele também deverá ser registrado para o evento par PEER \_ GROUP \_ EVENT INCOMING \_ \_ DATA.

Para receber o conjunto total de conexões diretas ativas no momento com outros pares em um grupo, chame [**PeerGroupEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections) para abrir a enumeração e iterar pela lista de conexões usando [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem).

Para fechar uma conexão direta, chame [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) e passe a ID da conexão.

## <a name="closing-and-shutting-down-a-peer-group"></a>Fechando e desligando um grupo de pares

Para fechar uma conexão com um grupo de pares, chame [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose), que invalida o alçamento do grupo, mas não desliga a infraestrutura de grupo de pares. Os dados de grupo ponto a ponto são excluídos chamando [**PeerGroupDelete**](/windows/desktop/api/P2P/nf-p2p-peergroupdelete).

Quando o aplicativo for concluído usando a Infraestrutura de Grupo de Pares, ele deverá chamar [**PeerGroupShutdown**](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown).

 

 



