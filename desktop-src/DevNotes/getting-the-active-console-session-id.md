---
description: A definição de Winternl.h a seguir é o endereço de memória estática da ID de sessão ativa do console dos Serviços de Terminal. Essa ID de sessão de console ativa não é definida em versões do sistema operacional Microsoft Windows anteriores ao Windows XP.
ms.assetid: f3022ab8-60ea-490b-a87d-cc1afc99d26f
title: Obter a ID da sessão do Console Ativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f7b23669240f0cd109a48f454ee6f6329f6839221a1677e81b75712430cb42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002296"
---
# <a name="getting-the-active-console-session-id"></a>Obter a ID da sessão do Console Ativo

A definição de Winternl.h a seguir é o endereço de memória estática da ID de sessão ativa do console dos Serviços de Terminal. Essa ID de sessão de console ativa não é definida em versões do sistema operacional Microsoft Windows anteriores ao Windows XP.

> [!Note]  
> Essa definição pode mudar em versões futuras Windows. Para garantir que seu aplicativo continue a ser executado corretamente no futuro, seu aplicativo deve chamar [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid).

 

``` syntax
#define INTERNAL_TS_ACTIVE_CONSOLE_ID    
        (*((volatile ULONG*)(0x7ffe02d8)))
```

 

 
