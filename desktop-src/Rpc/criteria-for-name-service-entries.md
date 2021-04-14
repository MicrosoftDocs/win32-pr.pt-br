---
title: Critérios para entradas de serviço de nome
description: Critérios para entradas de serviço de nome com RPC (chamada de procedimento remoto).
ms.assetid: f9a7b935-7104-489c-93a8-0c3793d17348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb32314dc86b179ea98bdf07000dc5ea359bdc77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453649"
---
# <a name="criteria-for-name-service-entries"></a>Critérios para entradas de serviço de nome

Os critérios a seguir são usados ao processar entradas de serviço de nome:

-   Se você fornecer um nome de entrada não **nulo** para [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), essa entrada será a única entrada pesquisada para identificadores de associação. Se você passar **NULL**, todas as entradas no seu domínio de logon serão pesquisadas. Observe que isso não inclui domínios confiáveis.
-   Se você fornecer um identificador de interface, os identificadores de associação serão retornados de uma entrada somente se a seção de interface da entrada contiver uma versão compatível desse UUID de interface. Ou seja, o número de versão principal deve ser o mesmo que o UUID de interface, enquanto o número de versão secundária deve ser igual ou maior que o seu.
-   Se você fornecer um UUID de objeto, os identificadores de associação serão retornados de uma entrada somente se a seção UUID de objeto da entrada contiver esse UUID de objeto específico.

Se uma entrada de serviço de nome sobreviver aos critérios descritos acima, todos os identificadores de ligação dessas entradas serão coletados. Identificadores com uma sequência de protocolo sem suporte pelo cliente são descartados e os identificadores restantes são retornados para você como a saída de [**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext).

 

 




