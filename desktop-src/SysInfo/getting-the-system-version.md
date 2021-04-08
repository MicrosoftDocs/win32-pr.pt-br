---
description: O exemplo a seguir usa as funções auxiliares de API de versão para determinar a versão do sistema operacional atual, se for uma versão de servidor ou cliente e, em seguida, exibir essas informações para o console.
ms.assetid: ae851aef-27d5-4eb7-aeb2-ccdfbf040e5a
title: Obtendo a versão do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0fa259378b81f9255846694927ee2b68e6f38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837485"
---
# <a name="getting-the-system-version"></a>Obtendo a versão do sistema

O exemplo a seguir usa as [funções auxiliares de API de versão](version-helper-apis.md) para determinar a versão do sistema operacional atual, se for uma versão de servidor ou cliente e, em seguida, exibir essas informações para o console. Se o modo de compatibilidade estiver em vigor, o exemplo exibirá o sistema operacional selecionado para [compatibilidade de aplicativos](/previous-versions/bb757005(v=msdn.10)).

Depender de informações de versão não é a melhor maneira de testar um recurso. Em vez disso, consulte a documentação do recurso de interesse. Para obter mais informações sobre técnicas comuns de detecção de recursos, consulte [versão do sistema operacional](operating-system-version.md).


```C++
#include <windows.h>
#include <stdio.h>
#include <VersionHelpers.h>

int 
__cdecl
wmain(
    __in int argc, 
    __in_ecount(argc) PCWSTR argv[]
    )
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);

    if (IsWindowsXPOrGreater())
    {
        printf("XPOrGreater\n");
    }

    if (IsWindowsXPSP1OrGreater())
    {
        printf("XPSP1OrGreater\n");
    }

    if (IsWindowsXPSP2OrGreater())
    {
        printf("XPSP2OrGreater\n");
    }

    if (IsWindowsXPSP3OrGreater())
    {
        printf("XPSP3OrGreater\n");
    }

    if (IsWindowsVistaOrGreater())
    {
        printf("VistaOrGreater\n");
    }

    if (IsWindowsVistaSP1OrGreater())
    {
        printf("VistaSP1OrGreater\n");
    }

    if (IsWindowsVistaSP2OrGreater())
    {
        printf("VistaSP2OrGreater\n");
    }

    if (IsWindows7OrGreater())
    {
        printf("Windows7OrGreater\n");
    }

    if (IsWindows7SP1OrGreater())
    {
        printf("Windows7SP1OrGreater\n");
    }

    if (IsWindows8OrGreater())
    {
        printf("Windows8OrGreater\n");
    }

    if (IsWindows8Point1OrGreater())
    {
        printf("Windows8Point1OrGreater\n");
    }

    if (IsWindows10OrGreater())
    {
        printf("Windows10OrGreater\n");
    }

    if (IsWindowsServer())
    {
        printf("Server\n");
    }
    else
    {
        printf("Client\n");
    }
}
```



 

 
