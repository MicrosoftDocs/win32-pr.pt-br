---
description: O código a seguir limpa toda a memória associada ao tratamento de símbolos para o processo especificado, usando SymCleanup.
ms.assetid: 270a1984-9e66-4dd2-accb-d715287f1ec0
title: Encerrando o manipulador de símbolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9147ed15c0dc03b76c822a38ccd7ac3c5d326454
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089213"
---
# <a name="terminating-the-symbol-handler"></a><span data-ttu-id="350a6-103">Encerrando o manipulador de símbolo</span><span class="sxs-lookup"><span data-stu-id="350a6-103">Terminating the Symbol Handler</span></span>

<span data-ttu-id="350a6-104">O código a seguir limpa toda a memória associada ao tratamento de símbolos para o processo especificado, usando [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup).</span><span class="sxs-lookup"><span data-stu-id="350a6-104">The following code cleans up all memory associated with symbol handling for the specified process, using [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup).</span></span>


```C++
if (SymCleanup(hProcess))
{
    // SymCleanup returned success
}
else
{
    // SymCleanup failed
    DWORD error = GetLastError();
    printf("SymCleanup returned error : %d\n", error);
}
```



 

 



