---
title: Critérios para entradas de serviço de nome
description: Critérios para Entradas de Serviço de Nome com RPC (Chamada de Procedimento Remoto).
ms.assetid: f9a7b935-7104-489c-93a8-0c3793d17348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609c545c72687a0b9b73db56d2f08654941e464c790e091ee886159d9e9593ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931115"
---
# <a name="criteria-for-name-service-entries"></a>Critérios para entradas de serviço de nome

Os critérios a seguir são usados ao processar entradas de serviço de nome:

-   Se você fornecer um nome de entrada não **NULL** para [**RpcNsBindingLookupBegin,**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)essa entrada será a única entrada pesquisada por alças de associação. Se você passar **NULL,** todas as entradas em seu domínio de logon serão pesquisadas. Observe que isso não inclui domínios confiáveis.
-   Se você fornecer um alça de interface, os alças de associação serão retornados de uma entrada somente se a seção de interface da entrada contiver uma versão compatível dessa interface UUID. Ou seja, o número de versão principal deve ser igual ao UUID da interface, enquanto o número de versão secundária deve ser igual ou maior que o seu.
-   Se você fornecer um UUID de objeto, os identificador de associação serão retornados de uma entrada somente se a seção UUID do objeto da entrada contiver esse UUID de objeto específico.

Se uma entrada de serviço de nome sobreviver aos critérios descritos acima, todos os alças de associação dessas entradas serão coletados. Os tratamentos com uma sequência de protocolo sem suporte do cliente são descartados e os alças restantes são retornados para você como a saída de [**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext).

 

 




