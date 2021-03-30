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
# <a name="getting-the-active-console-session-id"></a><span data-ttu-id="915e5-104">Obtendo a ID da sessão de console ativa</span><span class="sxs-lookup"><span data-stu-id="915e5-104">Getting the Active Console Session ID</span></span>

<span data-ttu-id="915e5-105">A definição de Winternl. h a seguir é o endereço de memória estático da ID de sessão do console de serviços de terminal ativa.</span><span class="sxs-lookup"><span data-stu-id="915e5-105">The following Winternl.h definition is the static memory address of the active Terminal Services console session ID.</span></span> <span data-ttu-id="915e5-106">Essa ID de sessão de console ativa não está definida nas versões do sistema operacional Microsoft Windows anteriores ao Windows XP.</span><span class="sxs-lookup"><span data-stu-id="915e5-106">This active console session ID is not defined in versions of the Microsoft Windows operating system earlier than Windows XP.</span></span>

> [!Note]  
> <span data-ttu-id="915e5-107">Essa definição pode ser alterada em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="915e5-107">This definition may change in future releases of Windows.</span></span> <span data-ttu-id="915e5-108">Para garantir que seu aplicativo continue a ser executado corretamente no futuro, seu aplicativo deve chamar [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid).</span><span class="sxs-lookup"><span data-stu-id="915e5-108">To ensure that your application will continue to run correctly in the future, your application must call [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid).</span></span>

 

``` syntax
#define INTERNAL_TS_ACTIVE_CONSOLE_ID    
        (*((volatile ULONG*)(0x7ffe02d8)))
```

 

 
