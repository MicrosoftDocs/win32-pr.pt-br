---
title: Clientes multithread e identificadores de contexto
description: Quando você tem um cliente multi-threaded em que vários threads estão usando a mesma instância de identificador de contexto, o acesso à instância de identificador de contexto é serializado no servidor por padrão.
ms.assetid: 192be467-b1e0-422b-878a-738cb7d72b5b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c621d75d8cc48ca1f71719066f455e0efce39f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007861"
---
# <a name="multithreaded-clients-and-context-handles"></a>Clientes multithread e identificadores de contexto

Quando você tem um cliente multi-threaded em que vários threads estão usando a mesma instância de identificador de contexto, o acesso à instância de identificador de contexto é serializado no servidor por padrão. Isso evita que o Gerenciador de servidores tenha que se proteger contra outro thread do mesmo cliente que está alterando o contexto ou o contexto que está sendo executado enquanto uma chamada é expedida. No entanto, em determinados casos, a serialização pode afetar o desempenho.

Considere o seguinte: dois threads de cliente invocam uma chamada de procedimento remoto que não altera o estado do contexto (por exemplo, a chamada simplesmente obtém alguns valores dele). Essas chamadas não precisam ser serializadas.

Para essas situações, o Windows XP oferece um modelo de serialização de modo misto, onde cada método pode ser declarado para ter acesso exclusivo ou compartilhado a um identificador de contexto. Confira a [ \_ \_ serialização de identificador](/windows/desktop/Midl/context-handle-serialize) de contexto e o [identificador de contexto \_ \_ noserializate](/windows/desktop/Midl/context-handle-noserialize) para obter detalhes.

Nas versões do Windows anteriores ao Windows XP, o único meio de permitir o acesso simultâneo a um identificador de contexto é chamar a função [**RpcSsDontSerializeContext**](/previous-versions/aa378473(v=vs.80)) para permitir que várias chamadas sejam expedidas em um único identificador de contexto. Chamar a função **RpcSsDontSerializeContext** não desabilita totalmente a serialização; Quando ocorre uma execução de contexto, a rotina de execução de contexto é executada somente quando todas as solicitações de cliente pendentes são concluídas. Uma chamada para **RpcScDontSerializeContext** afeta todo o processo e não é reversível. O uso do **RpcScDontSerializeContext** no Windows XP e em versões posteriores não é recomendado; Ele torna o código do servidor muito complicado ao lidar de forma confiável com as condições de corrida inerentes a ambientes completamente não serializados.

 

 