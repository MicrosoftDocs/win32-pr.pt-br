---
description: O agrupamento ponto a ponto é uma tecnologia que permite que um desenvolvedor crie uma rede de mesmo nível seguro de maneira rápida e eficaz.
ms.assetid: ee72f60b-1e5b-4b69-bda0-2ae80734c144
title: Como trabalhar com grupos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7bebf958d0c3fdee6ad0dc400d495c54ec2e6fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505885"
---
# <a name="how-to-work-with-groups"></a>Como trabalhar com grupos

O agrupamento ponto a ponto é uma tecnologia que permite que um desenvolvedor crie uma rede de mesmo nível seguro de maneira rápida e eficaz. A lista a seguir identifica as principais considerações na criação de um aplicativo de agrupamento de mesmo nível.

-   [Obtendo uma identidade de par](#obtaining-a-peer-identity)
-   [Iniciando um grupo de pares](#starting-up-the-peer-grouping-infrastructure)
-   [Registrando para eventos de agrupamento](#registering-for-peer-grouping-events)
-   [Conectando a um grupo](#obtaining-a-group-handle)
-   [Criando funções de administrador e membro](#creating-administrator-and-member-roles)
-   [Encontrando um par](#finding-a-peer)
-   [Conectando diretamente a um par](#connecting-directly-to-a-peer)
-   [Fechando e desligando um grupo](#closing-and-shutting-down-a-peer-group)

## <a name="obtaining-a-peer-identity"></a>Obtendo uma identidade de par

Antes de criar ou se conectar a um grupo, um par deve obter uma identidade de par, que é um nome usado para identificar exclusivamente um ponto a um grupo. Para obter uma lista enumerada de todas as identidades de pares definidas no par, chame [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities), que retorna um identificador para a enumeração. Para obter as identidades de par, chame [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) com o identificador de enumeração e o número de membros a serem recuperados. Continue chamando **PeerGetNextItem** até que o parâmetro *pCount* retorne um valor menor que o número de identidades de pares solicitadas.

Se uma identidade de par para o par não existir, ela poderá ser criada chamando [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate). Depois de criar uma identidade de par, o par gera um blob XML de identidade que contém a chave pública atribuída a ele

As informações de identidade do par são obtidas chamando [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml). Essas informações de identidade de par são usadas pelo criador do grupo ou por um administrador para emitir as credenciais necessárias para ingressar no grupo, como um blob XML de convite.

Para obter mais informações sobre identidades de pares, consulte a documentação da [API do Identity Manager](identity-manager-api.md)

## <a name="starting-up-the-peer-grouping-infrastructure"></a>Iniciando a infraestrutura de agrupamento de pares

Antes que qualquer função na API de agrupamento de mesmo nível seja chamada por um aplicativo, [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) deve ser chamado. Essa função inicializa a infraestrutura de agrupamento de pares para o aplicativo e define a versão com suporte.

## <a name="obtaining-a-group-handle"></a>Obtendo um identificador de grupo

Para se conectar a um grupo e começar a participar, é necessário obter um identificador para um grupo de pares. A lista a seguir identifica as três maneiras de se conectar a um grupo de pares:

-   Criar um grupo de pares chamando [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), que inicializa um novo grupo de pares e retorna um identificador válido com o par como o proprietário e o único administrador.
-   Ingressando em um grupo de pares chamando [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin). Para ingressar em um grupo par, um par deve receber um convite de um administrador de grupo de mesmo nível. Para obter um convite, envie o blob XML de informações de identidade para o administrador que cria um convite e o envia para você por um mecanismo externo, como email ou FTP. O convite e a identidade do par são passados para **PeerGroupJoin**, que retorna um identificador válido para o grupo.
-   Abrindo um grupo de pares ao qual um par ingressou anteriormente chamando [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen). Nessa situação, não é necessário obter um convite.

Depois de obter um identificador de grupo de pares válido de uma das funções acima, você pode se conectar a um grupo de pares chamando [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) com o novo identificador.

> [!Note]  
> Se a conexão a um grupo de pares falhar, \_ ocorrerá o evento de falha na conexão de evento do grupo de pares \_ \_ \_ . O manipulador pode tentar restabelecer a conexão com o grupo de pares.

 

## <a name="registering-for-peer-grouping-events"></a>Registrando para eventos de agrupamento de pares

Antes que um par participe de um grupo de pares, o par deve se registrar em eventos de grupo de pares. Para se registrar para eventos de mesmo nível específicos, chame [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)e passe um ou mais dos tipos de evento de pares definidos no tipo de evento de grupo de pares \_ \_ \_ . Você deve se registrar para cada evento de mesmo nível que se aplica ao seu aplicativo; por exemplo, para receber dados em uma conexão direta, registre-se para \_ os \_ eventos conexão direta de evento de grupo de pares \_ \_ e dados de entrada de evento de grupo de pares \_ \_ \_ \_ . Cada chamada usa um identificador de evento e retorna um identificador **HPEEREVENT** para esse evento de mesmo nível.

Os manipuladores de eventos podem obter os dados associados a um evento de mesmo nível passando o identificador para eventos de pares registrados para [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata). Esses dados de evento de mesmo nível são retornados como uma União de dados de evento de grupo de pares \_ \_ \_ . Se a fila de eventos de pares estiver vazia, essa função \_ retornará \_ nenhum \_ dado de evento de pares \_ .

Você pode cancelar o registro de eventos de pares chamando [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) e fornecendo o identificador para o evento de mesmo nível que deseja cancelar o registro. Depois que a função for chamada, os eventos de pares associados ao identificador não serão mais registrados.

## <a name="creating-administrator-and-member-roles"></a>Criando funções de administrador e membro

O ponto que cria o grupo de pares é conhecido como criador do grupo de pares e tem a função de administrador por padrão. Somente o criador do grupo de pares pode definir as propriedades do grupo.

Os colegas convidados para o grupo de pares podem ser um administrador ou um membro. Se eles forem atribuídos a uma função de administrador pelo administrador que emite o convite, eles poderão convidar novos membros para o grupo de mesmo nível e, da mesma forma, atribuir a função de administrador a outros membros.

As funções dos membros do grupo de pares são definidas nos convites que o administrador fornece a um membro. Para adicionar mais administradores, defina o valor do parâmetro *pRoles* de [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) como administrador da \_ função de grupo par \_ \_ ao criar um convite.

Os membros podem participar de um grupo de pares, mas não podem convidar e autorizar novos membros, definir propriedades de grupo ou atualizar ou excluir registros de grupo que não criam especificamente. Para atribuir o status de membro a um par participante, defina o valor do parâmetro **pRoles** de [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) como \_ membro da função de grupo par \_ \_ ao criar um convite para esse par.

Para alterar a função de um membro, novas credenciais contendo a nova função devem ser emitidas para esse membro. Para fazer isso, obtenha a estrutura de [**\_ \_ informações de credenciais de par**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) para esse membro da estrutura de membro par \_ retornada por [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers). Altere o campo **pRoles** nas **\_ \_ informações de credencial de par** para a nova função e passe a estrutura para [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials).

As novas credenciais não entrarão em vigor para o par até que se conectem ao grupo de pares. Se eles estiverem conectados no momento, eles deverão fechar o grupo e se reconectar para obter as credenciais atualizadas.

## <a name="finding-a-peer"></a>Encontrando um par

Para obter uma lista enumerada de todos os pares que participam do grupo par, chame [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) com o identificador de grupo, que retorna um identificador para a enumeração. Para obter os membros, chame [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) com o identificador de enumeração e o número de membros a serem recuperados. Continue chamando **PeerGetNextItem** até que o parâmetro *pCount* retorne um valor menor que o número de membros solicitados. Observe que a lista completa de membros disponíveis não pode ser retornada.

Cada membro é representado como uma estrutura de [**\_ membro par**](/windows/desktop/api/P2P/ns-p2p-peer_member) , que contém a identidade do par, IDs de nó e endereços IP para pares ativos.

Quando terminar, feche a enumeração e libere a memória associada chamando [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration).

## <a name="connecting-directly-to-a-peer"></a>Conectando diretamente a um par

Quando um par está conectado a um grupo de pares, o direcionamento de trocas de um para um com outros membros conectados é iniciado chamando [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) e fornecendo a identidade do outro par. Essa chamada é assíncrona e retorna uma ID de conexão de 64 bits. Se a chamada for bem-sucedida, você receberá o \_ evento \_ peer de conexão direta de evento de grupo par \_ \_ \_ para indicar que a conexão foi bem-sucedida. Se a conexão for bem-sucedida, a ID de conexão será válida e poderá ser usada para enviar e receber dados por meio da conexão direta.

Para poder receber conexões diretas, o outro par também deve ter sido registrado anteriormente para o \_ \_ \_ evento peer de conexão direta de evento de grupo par \_ .

Para enviar dados para um par, chame [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) com uma ID de conexão válida. Para receber dados, o outro par deve ser registrado para o evento de pares de dados de entrada de evento de grupo de pares \_ \_ \_ \_ . Da mesma forma, se o ponto de envio quiser receber dados por vez, ele também deverá ser registrado para o evento de pares de dados de entrada do evento de grupo de pares \_ \_ \_ \_ .

Para receber o conjunto total de conexões diretas atualmente ativas com outros pares em um grupo, chame [**PeerGroupEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections) para abrir a enumeração e iterar na lista de conexões usando [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem).

Para fechar uma conexão direta, chame [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) e passe a ID da conexão.

## <a name="closing-and-shutting-down-a-peer-group"></a>Fechando e desligando um grupo de pares

Para fechar uma conexão com um grupo de pares, chame [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose), que invalida o identificador de grupo, mas não encerra a infraestrutura de agrupamento de pares. Os dados do grupo ponto a ponto são excluídos chamando [**PeerGroupDelete**](/windows/desktop/api/P2P/nf-p2p-peergroupdelete).

Quando o aplicativo for concluído usando a infraestrutura de agrupamento de pares, ele deverá chamar [**PeerGroupShutdown**](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown).

 

 



