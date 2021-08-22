---
description: O código a seguir demonstra como recuperar um nome de símbolo indecoerdo de um nome de símbolo usando UnDecorateSymbolName.
ms.assetid: fcb0591a-dac3-45eb-b4c0-4a35c42450e5
title: Recuperando nomes de símbolos não rateados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f18a1cbdf51c64134489850343b466e49d9867fab483699a719997c3be9b5798
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076340"
---
# <a name="retrieving-undecorated-symbol-names"></a>Recuperando nomes de símbolos não rateados

O código a seguir demonstra como recuperar um nome de símbolo indecoerdo de um nome de símbolo usando [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname). O nome decorado é armazenado em `szName` . O exemplo pressu que você inicializou o manipulador de símbolos usando o código em [Inicializando o Manipulador de Símbolos](initializing-the-symbol-handler.md).


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



 

 



