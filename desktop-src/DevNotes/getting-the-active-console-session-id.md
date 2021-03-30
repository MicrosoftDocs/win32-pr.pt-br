---
description: A definição de Winternl. h a seguir é o endereço de memória estático da ID de sessão do console de serviços de terminal ativa. Essa ID de sessão de console ativa não está definida nas versões do sistema operacional Microsoft Windows anteriores ao Windows XP.
ms.assetid: f3022ab8-60ea-490b-a87d-cc1afc99d26f
title: Obtendo a ID da sessão de console ativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936db3f8038348864fc90fc55eeb4287a67c45d6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826328"
---
# <a name="getting-the-active-console-session-id"></a>Obtendo a ID da sessão de console ativa

A definição de Winternl. h a seguir é o endereço de memória estático da ID de sessão do console de serviços de terminal ativa. Essa ID de sessão de console ativa não está definida nas versões do sistema operacional Microsoft Windows anteriores ao Windows XP.

> [!Note]  
> Essa definição pode ser alterada em versões futuras do Windows. Para garantir que seu aplicativo continue a ser executado corretamente no futuro, seu aplicativo deve chamar [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid).

 

``` syntax
#define INTERNAL_TS_ACTIVE_CONSOLE_ID    
        (*((volatile ULONG*)(0x7ffe02d8)))
```

 

 
