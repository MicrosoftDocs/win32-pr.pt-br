---
description: O código de assembly x86 de exemplo a seguir obtém a ID de sessão dos Serviços de Terminal associada ao processo atual.
ms.assetid: 9fcb35cb-6813-46a5-aa38-e102f1b6b7dc
title: Obter a ID da sessão do processo atual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4326020f145c98544132703611fbd783edac9ae9eb89a5c69f44b67dc997ca30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955975"
---
# <a name="getting-the-session-id-of-the-current-process"></a>Obter a ID da sessão do processo atual

\[Os endereços de memória especificados por este código de exemplo podem mudar em versões futuras do Windows. Para garantir que seu aplicativo continue a ser executado corretamente no futuro, seu aplicativo deve chamar [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) e [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) em vez do código de exemplo a seguir.\]

O código de assembly x86 de exemplo a seguir obtém a ID de sessão dos Serviços de Terminal associada ao processo atual.

``` syntax
mov     eax,fs:[00000018]
mov     eax,[eax+0x30]
mov     eax,[eax+0x1d4]
```

 

 
