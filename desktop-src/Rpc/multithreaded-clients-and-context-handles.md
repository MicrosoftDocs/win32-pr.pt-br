---
title: Clientes multithread e alças de contexto
description: Quando você tem um cliente multi-threaded em que vários threads estão usando a mesma instância de alça de contexto, o acesso à instância do handle de contexto é serializado no servidor por padrão.
ms.assetid: 192be467-b1e0-422b-878a-738cb7d72b5b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e7fed15deacca47754f51869fa0b18b37135586addb7f80b8aa75b9dde63082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928076"
---
# <a name="multithreaded-clients-and-context-handles"></a>Clientes multithread e alças de contexto

Quando você tem um cliente multi-threaded em que vários threads estão usando a mesma instância de alça de contexto, o acesso à instância do handle de contexto é serializado no servidor por padrão. Isso salva o gerenciador do servidor de ter que se proteger contra outro thread do mesmo cliente alterando o contexto ou o contexto em execução enquanto uma chamada é expedida. No entanto, em determinados casos, a serialização pode afetar o desempenho.

Considere o seguinte: dois threads de cliente invocam uma chamada de procedimento remoto que não altera o estado do contexto (por exemplo, a chamada simplesmente obtém alguns valores dela). Essas chamadas não precisam ser serializadas.

Para essas situações, Windows XP oferece um modelo de serialização de modo misto, em que cada método pode ser declarado para ter acesso exclusivo ou compartilhado a um alça de contexto. Confira [ \_ serializar o \_ alça de contexto](/windows/desktop/Midl/context-handle-serialize) e o [ \_ \_ naerialize](/windows/desktop/Midl/context-handle-noserialize) do alça de contexto para obter detalhes.

Em versões do Windows anteriores ao Windows XP, o único meio de permitir o acesso simultâneo a um alça de contexto é chamar a [**função RpcSsDontSerializeContext**](/previous-versions/aa378473(v=vs.80)) para permitir que várias chamadas sejam expedidas em um único handle de contexto. Chamar a **função RpcSsDontSerializeContext** não desabilita totalmente a serialização; quando ocorre um run-down de contexto, a rotina de run down de contexto é executado somente quando todas as solicitações de cliente pendentes são concluídas. Uma chamada para **RpcScDontSerializeContext** afeta todo o processo e não é reverível. O **uso de RpcScDontSerializeContext** no Windows XP e versões posteriores não é recomendado; ele torna o código do servidor muito complicado ao lidar de forma confiável com condições de corrida inerentes a ambientes completamente não serializados.

 

 