---
description: Uma consideração especial deve ser dada a remetentes ou destinatários de PGM de hospedagem múltipla. Esta página descreve as considerações e fornece diretrizes para melhores práticas de programação.
ms.assetid: 10fb56dd-3c96-4944-9b53-aee76c269528
title: Hospedagem múltipla e PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142527c7fdf3e5d34d80c51e4002bc21ad47691c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751030"
---
# <a name="multihoming-and-pgm"></a>Hospedagem múltipla e PGM

Uma consideração especial deve ser dada a remetentes ou destinatários de PGM de hospedagem múltipla. Esta página descreve as considerações e fornece diretrizes para melhores práticas de programação.

## <a name="multihomed-pgm-sender"></a>Remetente de PGM de hospedagem múltipla

Quando um aplicativo falha ao especificar uma interface ao chamar a função [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) , a primeira interface disponível é usada. Se nenhuma interface estiver disponível, a **conexão** falhará.

Quando um aplicativo especifica uma interface usando a [opção \_ set \_ Send \_ If](socket-options.md) Socket do RM, uma tentativa de [**Associação**](/windows/desktop/api/winsock/nf-winsock-bind) é feita implicitamente a essa interface usando TCP/IP e falha se o TCP/IP falha na solicitação de associação. Se a interface for definida usando RM \_ set \_ Send \_ If várias vezes, somente o último conjunto de interface será aplicável com êxito.

O Windows Sockets mantém a interface definida e, se essa interface desaparecer, a sessão é desconectada.

## <a name="multihomed-pgm-receiver"></a>Receptor de PGM de hospedagem múltipla

Quando um aplicativo falha ao especificar uma interface ao chamar a função [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , a interface padrão é usada. Se nenhuma interface estiver disponível, a [**ligação**](/windows/desktop/api/winsock/nf-winsock-bind) falhará.

Quando um aplicativo especifica uma ou mais interfaces para escuta, usando o [RM \_ Add \_ Receive \_ If](socket-options.md), o Windows Sockets tenta se associar à interface ou às interfaces solicitadas usando TCP/IP. Qualquer erro do TCP/IP faz com que essa solicitação falhe. Ao contrário do caso do emissor do PGM, a adição de uma interface de recebimento várias vezes resulta na postagem de escuta em todas as interfaces adicionadas com êxito. Use a \_ opção RM del \_ Receive \_ If Socket para parar de escutar em uma interface.

O Windows Sockets não mantém o estado sobre várias interfaces de escuta especificadas e, em vez disso, depende do TCP/IP para fazer isso. No entanto, quando uma sessão está em andamento, o Windows Sockets rastreia a interface de entrada para essa sessão e, se essa interface desaparecer, o Windows Sockets desconecta a sessão.

 

 



