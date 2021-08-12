---
description: Este tópico discute como um aplicativo se conecta a um grupo de pares usando as APIs de Grupo de Pares.
ms.assetid: 56fa28d8-3b3a-4cd5-8448-c8c4ce8d0b2c
title: Como Conexão um grupo par
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb1cfd08fde0fc733873648dfae1ffb4f86b713b3ed790430686b641a893d23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612762"
---
# <a name="how-to-connect-to-a-peer-group"></a>Como Conexão um grupo par

Este tópico discute como um aplicativo se conecta a um grupo de pares usando as APIs de Grupo de Pares.

## <a name="joining-a-peer-group"></a>Ingressar em um grupo de pares

Para ingressar em um grupo de pares, chame [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), passando o nome de identidade do par e o convite (e um nome de nuvem PNRP opcional, se o nome da nuvem no convite for ambíguo).

Se for [**bem-sucedido, PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) retornará um handle para o grupo de pares.

Se o par tiver ingressado anteriormente no grupo de pares e fechado o handle, o grupo de pares deverá ser reaberto chamando [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) e passando o nome do grupo par. Essa chamada retorna um novo alça de grupo par.

Depois que o grupo de pares for ingressado com êxito, o par poderá se conectar diretamente ao grupo par e começar a interagir chamando [**PeerGroupConnect.**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) Após a conexão, o par é considerado "online".

Se um aplicativo não interagir com o grupo no momento, ele poderá permanecer "offline". Se ele optar por participar diretamente do grupo de pares em uma instância posterior, uma chamada subsequente para [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) o colocará online. Depois que um par ingressar no grupo de pares, ele deverá se conectar pelo menos uma vez antes de poder publicar registros no grupo par.

## <a name="opening-a-peer-group-without-connecting-offline"></a>Abrir um grupo de pares sem conexão (offline)

Geralmente, talvez você queira que um aplicativo se conecte a um grupo par, mas não participe diretamente dele, recebendo e publicando atualizações de registro, mas não enviando ou recebendo mensagens de dados. Um aplicativo está nesse estado "offline" imediatamente depois que [**PeerGroupCreate,**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)ou [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) foram chamados.

Um aplicativo offline pode ficar online a qualquer momento chamando [**PeerGroupConnect.**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) Uma vez conectado, um grupo de pares não pode ficar offline até que todos os outros aplicativos associados a essa identidade e o compartilhamento desse grupo também tenham fechado conexões com ele.

Um grupo de pares é um recurso compartilhado, com o mesmo grupo de pares disponível para vários aplicativos. Se mais de um aplicativo para a mesma identidade e Windows usuário estiver usando o mesmo grupo par, ele também compartilhará o mesmo banco de dados e conexões subjacentes (vizinho e direto). Se qualquer um desses aplicativos chamar [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect), todos os outros aplicativos para essa identidade/usuário que participam do grupo também se conectarão ao grupo. Se um registro for adicionado por um aplicativo enquanto o grupo estiver offline, outros aplicativos também poderão vê-lo. Como resultado, um aplicativo deve estar pronto para ficar online a qualquer momento.

## <a name="connecting-to-a-peer-group-online"></a>Conectando-se a um grupo par (online)

Para começar a participar de um grupo, chame [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) depois de criar, ingressar ou abrir o grupo. Nesse estado, as conexões diretas podem ser abertas com outros pares que participam do mesmo grupo chamando [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection).

Para detectar se uma tentativa de conexão falhou, registre-se para o evento PEER \_ GROUP \_ EVENT CONNECTION \_ \_ FAILED. Esse evento será gerado se a infraestrutura de agrupação não puder encontrar outro membro para se conectar ou se a conexão falhar antes que o banco de dados de grupo seja sincronizado e outra conexão não possa ser estabelecida.

Embora vários aplicativos em execução no par e que participam do mesmo grupo com a mesma identidade par possam estar offline, uma chamada para [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) por qualquer um dos aplicativos resulta na online de todos os aplicativos.

Além disso, se um aplicativo no par tiver se conectado ao grupo, todos os outros aplicativos que chamam [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) ou [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) também serão conectados imediatamente. Se um aplicativo chamar [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose), o handle será fechado apenas para esse aplicativo. Assim, uma chamada subsequente para **PeerGroupOpen** pelo aplicativo retornará um novo alçamento de grupo e o aplicativo será online imediatamente se quaisquer outros aplicativos que participam do mesmo grupo ainda estão conectados.

## <a name="sending-and-receiving-data"></a>Enviando e recebendo dados

Para enviar e receber dados entre nós de membro específicos no grupo, as conexões diretas devem ser estabelecidas com os membros com os que você pretende interagir. Estabelecer uma conexão direta é uma chamada assíncrona para [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection), passando o handle para um grupo conectado, bem como a identidade do par dentro do grupo ao que você deseja se conectar. Esse método retornará uma ID de conexão. Se a chamada for bem-sucedida, um evento PEER GROUP EVENT DIRECT CONNECTION será gerado no \_ \_ par, validando a \_ \_ ID da conexão.

Para receber conexões diretas de outros pares online, registre-se para o evento PEER GROUP EVENT DIRECT CONNECTION com uma chamada \_ \_ para \_ \_ [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent).

Depois que uma conexão direta for estabelecida com êxito, o aplicativo poderá começar a enviar dados com chamadas para [**PeerGroupSendData,**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)passando a ID de conexão válida. A ordenação de transmissões de dados de várias partes é manipulada **por PeerGroupSendData.** No entanto, os aplicativos devem implementar uma pilha de protocolo adequada para lidar com os dados opacos retornados por essa chamada à API.

Para receber dados por uma conexão direta, o aplicativo deve se registrar para o evento PEER \_ GROUP EVENT INCOMING DATA com \_ \_ \_ [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent). O manipulador de eventos é responsável por obter e ordenar os dados opacos e passá-los para o aplicativo. Esses dados são obtidos no manipulador de eventos chamando [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) com o manipulador para os eventos registrados.

Uma conexão direta é fechada chamando [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) e passando a ID de conexão obtida por uma chamada anterior para [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) ou recebida nos dados de evento para PEER \_ EVENT GROUP DIRECT \_ \_ \_ CONNECTION.

 

 



