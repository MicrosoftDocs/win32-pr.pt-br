---
title: Uso de CMMs (módulos de gerenciamento de cores)
description: CmMs (Módulos de Gerenciamento de Cores) são módulos de código WCS que usam as informações nos perfis de dispositivo para executar a conversão de cores e o mapeamento de cores.
ms.assetid: df119e1a-b6f5-40a3-8852-8a57b21483d0
keywords:
- Windows Sistema de Cores (WCS), CMM (Módulo de Gerenciamento de Cores)
- WCS (Windows color system),CMM (Módulo de Gerenciamento de Cores)
- gerenciamento de cores da imagem, CMM (Módulo de Gerenciamento de Cores)
- gerenciamento de cores,CMM (Módulo de Gerenciamento de Cores)
- colors,CmM (Módulo de Gerenciamento de Cores)
- CmM (Módulo de Gerenciamento de Cores)
- CMM (Módulo de Gerenciamento de Cores)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 147c13a688942d46e400c2158c340fcea58d86616de042e9a44511861b67b802
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442346"
---
# <a name="using-color-management-modules-cmm"></a>Uso de CMMs (módulos de gerenciamento de cores)

CmMs (Módulos de Gerenciamento de Cores) são módulos de código WCS que usam as informações nos perfis de dispositivo para executar a conversão de cores e o mapeamento de cores. Os desenvolvedores de aplicativos não devem ter que implementar CMMs. A Microsoft fornece o CMM padrão. No entanto, se você escrever um software que exija o uso de algoritmos especializados de conversão de cores e mapeamento de cores, você poderá criar um.

> [!Note]  
> Os pontos de entrada do CMM *não são* funções de API e não devem ser chamados por aplicativos.

 

Quando os CMMs são instalados, o programa de instalação os registra no Windows registro. Os aplicativos podem enumerar os CMMs registrados e selecionar um usando a [**função SelectCMM.**](/windows/win32/api/icm/nf-icm-selectcmm) O aplicativo de exemplo a seguir demonstra como enumerar todos os CMMs registrados.


```C++
#include <stdio.h>
#include <stdlib.h>
#include <stddef.h>
#include <string.h>
#include <mbstring.h>
#include <windows.h>
#include <icm.h>

#ifdef WINDOWS_98
TCHAR  gszICMatcher[] = __TEXT(
  "SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\ICM\\ICMatchers");
#else
TCHAR  gszICMatcher[] = __TEXT(
  "SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\ICM\\ICMatchers");
#endif

_CRTAPI1 main (int argc, char *argv[])
{
    DWORD dwNumCMM = 0;

    HANDLE hkCMM;
    DWORD dwErr = RegCreateKey(HKEY_LOCAL_MACHINE,
                 gszICMatcher, &hkCMM);
    DWORD dwMaxName, dwMaxValue;
    DWORD dwInfoErr = RegQueryInfoKey(&hkCMM, NULL, NULL,
                                NULL, NULL, NULL, NULL, NULL,
                                &dwMaxName, &dwMaxValue,
                                NULL, NULL);
    TCHAR chCMM[dwMaxName];
    ULONG cjCMM = sizeof(chCMM)/sizeof(chCMM[0]);
    DWORD dwType;
    TCHAR chCMMFile[dwMaxValue];
    ULONG cjCMMFile = sizeof(chCMMFile)/sizeof(chCMMFile[0]);

    if (dwErr != ERROR_SUCCESS)
    {
        printf("Could not open ICMatcher registry key: %d\n", dwErr);
    }

    if (dwErr == ERROR_SUCCESS)
    {
        while (RegEnumValue(
                   hkCMM,dwNumCMM,chCMM,
                   &cjCMM,NULL,&dwType,
                   chCMMFile,&cjCMMFile) == ERROR_SUCCESS)
        {
            if (dwType == REG_SZ)
            {
                printf("%d: %-80s - %-80s\n",dwNumCMM,chCMM,chCMMFile);
            }
            else
            {
                printf("%d: error\n");
            }

            dwNumCMM++;
            cjCMM = sizeof(chCMM);
            cjCMMFile = sizeof(chCMMFile);
        }
    }

    RegCloseKey(hkCMM);
}
```



 

 




