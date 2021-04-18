---
description: O código a seguir demonstra como recuperar um nome de símbolo não decorado de um nome de símbolo usando UnDecorateSymbolName.
ms.assetid: fcb0591a-dac3-45eb-b4c0-4a35c42450e5
title: Recuperando nomes de símbolo não decorados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b0f21c884a0a58f0546ef275f2f3096abe2c50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751356"
---
# <a name="retrieving-undecorated-symbol-names"></a><span data-ttu-id="55354-103">Recuperando nomes de símbolo não decorados</span><span class="sxs-lookup"><span data-stu-id="55354-103">Retrieving Undecorated Symbol Names</span></span>

<span data-ttu-id="55354-104">O código a seguir demonstra como recuperar um nome de símbolo não decorado de um nome de símbolo usando [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname).</span><span class="sxs-lookup"><span data-stu-id="55354-104">The following code demonstrates how to retrieve an undecorated symbol name from a symbol name using [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname).</span></span> <span data-ttu-id="55354-105">O nome decorado é armazenado em `szName` .</span><span class="sxs-lookup"><span data-stu-id="55354-105">The decorated name is stored in `szName`.</span></span> <span data-ttu-id="55354-106">O exemplo supõe que você tenha inicializado o manipulador de símbolo usando o código na [inicialização do manipulador de símbolo](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="55354-106">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
if (UnDecorateSymbolName(szName, szUndName, sizeof(szUndName), UNDNAME_COMPLETE))
{
    // UnDecorateSymbolName returned success
    printf ("Symbol : %s\n", szUndName);
}
else
{
    // UnDecorateSymbolName failed
    DWORD error = GetLastError();
    printf("UnDecorateSymbolName returned error %d\n", error);
}
```



 

 



