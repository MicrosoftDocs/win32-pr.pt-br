---
title: Causal ordenação de chamadas assíncronas
description: Em um aplicativo RPC assíncrono, é possível que um thread de cliente faça uma segunda chamada assíncrona em um identificador de associação antes que uma chamada anterior feita nesse identificador seja concluída.
ms.assetid: 69beb3a4-39ae-4e3f-bb7d-31519278334d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754ae4733e5a3936bdd28fef72b9560fb9c9dfcd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005439"
---
# <a name="causal-ordering-of-asynchronous-calls"></a>Causal ordenação de chamadas assíncronas

Em um aplicativo RPC assíncrono, é possível que um thread de cliente faça uma segunda chamada assíncrona em um identificador de associação antes que uma chamada anterior feita nesse identificador seja concluída. A biblioteca de tempo de execução RPC trata dessa situação da seguinte maneira:

-   O mecanismo de RPC assíncrono garante que as chamadas assíncronas feitas no mesmo identificador de ligação, no mesmo thread, no mesmo nível de segurança, sejam expedidas na ordem em que foram feitas. A execução real das chamadas pode ocorrer fora de ordem.
-   Assim como acontece com chamadas síncronas, as chamadas de procedimento remoto assíncronas de diferentes threads de cliente são executadas simultaneamente.
-   Se uma chamada assíncrona de um aplicativo cliente for seguida por uma ou mais chamadas síncronas, a chamada assíncrona poderá ser executada enquanto as chamadas síncronas estiverem em execução. Independentemente do status da chamada assíncrona, as chamadas síncronas são executadas na ordem em que são recebidas pelo servidor.
-   Se um aplicativo cliente selecionar a ordenação noncausal para um identificador de ligação específico, ele desabilitará a serialização para esse identificador. Os aplicativos habilitam a ordenação de noncausal chamando [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) com o parâmetro *Option* definido como RPC \_ C \_ opt \_ Binding \_ Noncausal e o parâmetro *optionvalue* definido como **true**. Para obter detalhes, consulte [constantes de opção de associação](binding-option-constants.md).

 

 




