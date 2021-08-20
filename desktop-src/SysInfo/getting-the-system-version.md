---
description: O exemplo a seguir usa as funções auxiliares da API de versão para determinar a versão do sistema operacional atual, se for uma versão de Servidor ou Cliente e, em seguida, exibe essas informações no console.
ms.assetid: ae851aef-27d5-4eb7-aeb2-ccdfbf040e5a
title: Obter a versão do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb9cfd0c1a4cfe1ee0789cb609bf22319bdd019bf3310bf439dabf907bfd138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117958521"
---
# <a name="getting-the-system-version"></a>Obter a versão do sistema

O exemplo a seguir usa as funções auxiliares da [API](version-helper-apis.md) de versão para determinar a versão do sistema operacional atual, se for uma versão de Servidor ou Cliente e, em seguida, exibe essas informações no console. Se o modo de compatibilidade estiver em vigor, o exemplo exibirá o sistema operacional selecionado para [compatibilidade do aplicativo.](/previous-versions/bb757005(v=msdn.10))

Depender de informações de versão não é a melhor maneira de testar um recurso. Em vez disso, consulte a documentação do recurso de interesse. Para obter mais informações sobre técnicas comuns para detecção de recursos, consulte [Versão do sistema operacional](operating-system-version.md).


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



 

 
