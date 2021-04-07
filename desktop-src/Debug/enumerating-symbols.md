---
description: O código a seguir exibe o nome, o endereço e o tamanho de cada símbolo carregado no módulo especificado.
ms.assetid: 6ecdbd1e-406a-453e-9037-707ceb72074a
title: Enumerando símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33f9a98f37ca5ef2249f68ffa9b8ef73198de242
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920116"
---
# <a name="enumerating-symbols"></a><span data-ttu-id="ee415-103">Enumerando símbolos</span><span class="sxs-lookup"><span data-stu-id="ee415-103">Enumerating Symbols</span></span>

<span data-ttu-id="ee415-104">O código a seguir exibe o nome, o endereço e o tamanho de cada símbolo carregado no módulo especificado.</span><span class="sxs-lookup"><span data-stu-id="ee415-104">The following code displays the name, address, and size of each loaded symbol in the specified module.</span></span> <span data-ttu-id="ee415-105">A função [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) requer uma função de retorno de chamada, que é chamada uma vez para cada módulo carregado.</span><span class="sxs-lookup"><span data-stu-id="ee415-105">The [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) function requires a callback function, which is called once for each module loaded.</span></span> <span data-ttu-id="ee415-106">Neste exemplo, EnumSymProc é uma implementação da função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="ee415-106">In this example, EnumSymProc is an implementation of the callback function.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <dbghelp.h>

BOOL CALLBACK EnumSymProc( 
    PSYMBOL_INFO pSymInfo,   
    ULONG SymbolSize,      
    PVOID UserContext)
{
    UNREFERENCED_PARAMETER(UserContext);
    
    printf("%08X %4u %s\n", 
           pSymInfo->Address, SymbolSize, pSymInfo->Name);
    return TRUE;
}

void main()
{
    HANDLE hProcess = GetCurrentProcess();
    DWORD64 BaseOfDll;
    char *Mask = "*";
    BOOL status;

    status = SymInitialize(hProcess, NULL, FALSE);
    if (status == FALSE)
    {
        return;
    }
    
    BaseOfDll = SymLoadModuleEx(hProcess,
                                NULL,
                                "foo.dll",
                                NULL,
                                0,
                                0,
                                NULL,
                                0);
                                
    if (BaseOfDll == 0)
    {
        SymCleanup(hProcess);
        return;
    }                                
        
    if (SymEnumSymbols(hProcess,     // Process handle from SymInitialize.
                        BaseOfDll,   // Base address of module.
                        Mask,        // Name of symbols to match.
                        EnumSymProc, // Symbol handler procedure.
                        NULL))       // User context.
    {
        // SymEnumSymbols succeeded
    }
    else
    {
        // SymEnumSymbols failed
        printf("SymEnumSymbols failed: %d\n", GetLastError());
    }
    
    SymCleanup(hProcess);
}
```



 

 



