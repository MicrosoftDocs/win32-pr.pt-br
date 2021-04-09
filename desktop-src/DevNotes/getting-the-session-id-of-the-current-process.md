---
description: O código do assembly x86 de exemplo a seguir obtém a ID de sessão dos serviços de terminal associada ao processo atual.
ms.assetid: 9fcb35cb-6813-46a5-aa38-e102f1b6b7dc
title: Obtendo a ID de sessão do processo atual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac76865bcfe9144e8b95d4642385804aaf1af8fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089144"
---
# <a name="getting-the-session-id-of-the-current-process"></a><span data-ttu-id="64c1c-103">Obtendo a ID de sessão do processo atual</span><span class="sxs-lookup"><span data-stu-id="64c1c-103">Getting the Session ID of the Current Process</span></span>

<span data-ttu-id="64c1c-104">\[Os endereços de memória especificados por este código de exemplo podem ser alterados em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="64c1c-104">\[The memory addresses specified by this example code may change in future releases of Windows.</span></span> <span data-ttu-id="64c1c-105">Para garantir que seu aplicativo continue a ser executado corretamente no futuro, seu aplicativo deve chamar [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) e, em seguida, [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) , em vez do código de exemplo a seguir.\]</span><span class="sxs-lookup"><span data-stu-id="64c1c-105">To ensure that your application will continue to run correctly in the future, your application must call [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) and then [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) instead of the following sample code.\]</span></span>

<span data-ttu-id="64c1c-106">O código do assembly x86 de exemplo a seguir obtém a ID de sessão dos serviços de terminal associada ao processo atual.</span><span class="sxs-lookup"><span data-stu-id="64c1c-106">The following example x86 assembly code gets the Terminal Services session ID associated with the current process.</span></span>

``` syntax
mov     eax,fs:[00000018]
mov     eax,[eax+0x30]
mov     eax,[eax+0x1d4]
```

 

 
