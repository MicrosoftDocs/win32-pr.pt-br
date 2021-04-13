---
description: O código a seguir lista os módulos que foram carregados pela função SymLoadModule64 ou SymInitialize.
ms.assetid: 8c7fdfaa-d4d3-42d6-ad19-23e8ffda7bf4
title: Enumerando módulos de símbolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43623a7409116450fccc822bbc0bef1a309fbd2a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456876"
---
# <a name="enumerating-symbol-modules"></a>Enumerando módulos de símbolo

O código a seguir lista os módulos que foram carregados pela função [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) ou [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) . A função [**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) requer uma função de retorno de chamada, que será chamada uma vez para cada módulo carregado. Neste exemplo, EnumModules é uma implementação da função de retorno de chamada. O exemplo supõe que você tenha inicializado o manipulador de símbolo usando o código na [inicialização do manipulador de símbolo](initializing-the-symbol-handler.md).


```C++
BOOL CALLBACK EnumModules(
    PCTSTR  ModuleName, 
    DWORD64 BaseOfDll,  
    PVOID   UserContext )
{
    UNREFERENCED_PARAMETER(UserContext);
    
    _tprintf(TEXT("%08X %s\n"), BaseOfDll, ModuleName);
    return TRUE;
}


if (SymEnumerateModules64(hProcess, EnumModules, NULL))
{
    // SymEnumerateModules64 returned success
}
else
{
    // SymEnumerateModules64 failed
    error = GetLastError();
    _tprintf(TEXT("SymEnumerateModules64 returned error : %d\n"), error);
}
```



 

 



