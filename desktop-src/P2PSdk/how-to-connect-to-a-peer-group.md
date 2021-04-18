---
description: Este tópico discute como um aplicativo se conecta a um grupo de pares usando as APIs de agrupamento de pares.
ms.assetid: 56fa28d8-3b3a-4cd5-8448-c8c4ce8d0b2c
title: Como se conectar a um grupo de pares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bb3f41342573742e634a6e7ebce283188f3ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758291"
---
# <a name="how-to-connect-to-a-peer-group"></a>Como se conectar a um grupo de pares

Este tópico discute como um aplicativo se conecta a um grupo de pares usando as APIs de agrupamento de pares.

## <a name="joining-a-peer-group"></a>Ingressando em um grupo de pares

Para ingressar em um grupo de pares, chame [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), passando o nome da identidade do par e o convite (e um nome de nuvem PNRP opcional, se o nome da nuvem no convite for ambíguo).

Se for bem-sucedido, [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) retornará um identificador para o grupo de pares.

Se o par tiver ingressado anteriormente no grupo par e, em seguida, fechar o identificador, o grupo par deverá ser reaberto chamando [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) e passando o nome do grupo par. Essa chamada retorna um novo identificador de grupo de pares.

Depois que o grupo de pares for Unido com êxito, o par poderá se conectar diretamente ao grupo de pares e começar a interagir chamando [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect). Após a conexão, o par é considerado "online".

Se um aplicativo não for interagir com o grupo no momento, ele poderá permanecer "offline". Se ele optar por participar diretamente do grupo de pares em uma instância posterior, uma chamada subsequente para [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) o colocará online. Depois que um par tiver ingressado no grupo par, ele deverá se conectar pelo menos uma vez antes de poder publicar registros no grupo par.

## <a name="opening-a-peer-group-without-connecting-offline"></a>Abrindo um grupo de pares sem se conectar (offline)

Muitas vezes, talvez você queira fazer com que um aplicativo se conecte a um grupo de mesmo nível, mas não o participe diretamente, recebendo e publicando atualizações de registro, mas não enviando nem recebendo mensagens de dados. Um aplicativo está nesse estado "offline" imediatamente após [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)ou [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) ter sido chamado.

Um aplicativo offline pode ficar online a qualquer momento chamando [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect). Uma vez conectado, um grupo de pares não pode ficar offline até que todos os outros aplicativos associados a essa identidade e o compartilhamento desse grupo tenham conexões fechadas também.

Um grupo de pares é um recurso compartilhado, com o mesmo grupo de pares disponível para vários aplicativos. Se mais de um aplicativo para a mesma identidade e usuário do Windows estiver usando o mesmo grupo de pares, eles também compartilharão o mesmo banco de dados e conexões subjacentes (vizinho e direto). Se qualquer um desses aplicativos chamar [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect), todos os outros aplicativos para esta identidade/usuário que participa do grupo também se conectarão ao grupo. Se um registro for adicionado por um aplicativo enquanto o grupo estiver offline, outros aplicativos também poderão vê-lo. Como resultado, um aplicativo deve estar pronto para ficar online a qualquer momento.

## <a name="connecting-to-a-peer-group-online"></a>Conectando a um grupo par (online)

Para começar a participar de um grupo, chame [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) depois de criar, ingressar ou abrir o grupo. Nesse estado, as conexões diretas podem ser abertas com outros pares que participam do mesmo grupo chamando [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection).

Para detectar se uma tentativa de conexão falhou, registre-se para o evento de falha na conexão de evento do grupo de pares \_ \_ \_ \_ . Esse evento será gerado se a infraestrutura de agrupamento não puder encontrar outro membro ao qual se conectar, ou se a conexão falhar antes de o banco de dados do grupo ser sincronizado e outra conexão não puder ser estabelecida.

Embora vários aplicativos em execução no mesmo nível e que participam do mesmo grupo com a mesma identidade de mesmo nível possam estar offline, uma chamada para [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) por qualquer um dos aplicativos resulta em todos os aplicativos que se tornam online.

Além disso, se um aplicativo no par tiver se conectado ao grupo, todos os outros aplicativos que chamarem [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) ou [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) também serão conectados imediatamente. Se um aplicativo chamar [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose), o identificador será fechado somente para esse aplicativo. Assim, uma chamada subsequente para **PeerGroupOpen** pelo aplicativo retorna um novo identificador de grupo, e o aplicativo será colocado online imediatamente se qualquer outro aplicativo que participa do mesmo grupo ainda estiver conectado.

## <a name="sending-and-receiving-data"></a>Enviando e recebendo dados

Para enviar e receber dados entre nós de membro específicos no grupo, as conexões diretas devem ser estabelecidas com os membros com os quais você pretende interagir. O estabelecimento de uma conexão direta é uma chamada assíncrona para [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection), passando o identificador para um grupo conectado, bem como a identidade do par no grupo ao qual você deseja se conectar. Esse método retornará uma ID de conexão. Se a chamada for bem-sucedida, um \_ evento de conexão direta de evento de grupo de pares \_ \_ \_ será gerado no par, validando a ID de conexão.

Para receber conexões diretas de outros pares online, registre-se para o \_ evento de conexão direta de evento de grupo de pares \_ \_ \_ com uma chamada para [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent).

Depois que uma conexão direta tiver sido estabelecida com êxito, o aplicativo poderá começar a enviar dados com chamadas para [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata), passando a ID de conexão válida. A ordenação de transmissões de dados com várias partes é tratada pelo **PeerGroupSendData**. No entanto, os aplicativos devem implementar uma pilha de protocolos apropriada para manipular os dados opacos retornados por essa chamada à API.

Para receber dados em uma conexão direta, o aplicativo deve se registrar para o \_ evento de entrada de evento do grupo de pares \_ \_ \_ com [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent). O manipulador de eventos é responsável por obter e ordenar os dados opacos e passá-los para o aplicativo. Esses dados são obtidos no manipulador de eventos chamando [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) com o identificador para os eventos registrados.

Uma conexão direta é fechada chamando [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) e passando a ID de conexão obtida por uma chamada anterior para [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) ou recebida nos dados de evento para \_ \_ conexão direta do grupo de eventos de pares \_ \_ .

 

 



