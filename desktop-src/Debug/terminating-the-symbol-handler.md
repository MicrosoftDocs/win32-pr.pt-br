---
description: O código a seguir limpa toda a memória associada ao tratamento de símbolos para o processo especificado, usando SymCleanup.
ms.assetid: 270a1984-9e66-4dd2-accb-d715287f1ec0
title: Encerrando o manipulador de símbolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af49c26ffe1a80fad3bf7b03fc18699c07e9b025e8b07b5f6bb6c377cde743b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956935"
---
# <a name="terminating-the-symbol-handler"></a>Encerrando o manipulador de símbolo

O código a seguir limpa toda a memória associada ao tratamento de símbolos para o processo especificado, usando [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup).


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



 

 



