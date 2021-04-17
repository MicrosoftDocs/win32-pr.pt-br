---
title: Uso de CMMs (módulos de gerenciamento de cores)
description: Os CMMs (módulos de gerenciamento de cores) são módulos de código WCS que usam as informações em perfis de dispositivo para executar a conversão de cores e o mapeamento de cores.
ms.assetid: df119e1a-b6f5-40a3-8852-8a57b21483d0
keywords:
- WCS (sistema de cores do Windows), módulo de gerenciamento de cores (CMM)
- WCS (sistema de cores do Windows), módulo de gerenciamento de cores (CMM)
- gerenciamento de cores de imagem, módulo de gerenciamento de cores (CMM)
- gerenciamento de cores, módulo de gerenciamento de cores (CMM)
- cores, módulo de gerenciamento de cores (CMM)
- Módulo de gerenciamento de cores (CMM)
- CMM (módulo de gerenciamento de cores)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518558305639f0699358f22fb3544698741cfedf
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/02/2021
ms.locfileid: "105766594"
---
# <a name="using-color-management-modules-cmm"></a><span data-ttu-id="6dee5-110">Uso de CMMs (módulos de gerenciamento de cores)</span><span class="sxs-lookup"><span data-stu-id="6dee5-110">Using Color Management Modules (CMM)</span></span>

<span data-ttu-id="6dee5-111">Os CMMs (módulos de gerenciamento de cores) são módulos de código WCS que usam as informações em perfis de dispositivo para executar a conversão de cores e o mapeamento de cores.</span><span class="sxs-lookup"><span data-stu-id="6dee5-111">Color Management Modules (CMMs) are modules of WCS code that use the information in device profiles to perform color conversion and color mapping.</span></span> <span data-ttu-id="6dee5-112">Os desenvolvedores de aplicativos não devem implementar o CMMs.</span><span class="sxs-lookup"><span data-stu-id="6dee5-112">Application developers should not have to implement CMMs.</span></span> <span data-ttu-id="6dee5-113">A Microsoft fornece o CMM padrão.</span><span class="sxs-lookup"><span data-stu-id="6dee5-113">Microsoft provides the default CMM.</span></span> <span data-ttu-id="6dee5-114">No entanto, se você escrever software que exija o uso de algoritmos de conversão de cores especializadas e de mapeamento de cores, poderá criar um.</span><span class="sxs-lookup"><span data-stu-id="6dee5-114">However, if you do write software that requires the use of specialized color conversion and color mapping algorithms, you may create one.</span></span>

> [!Note]  
> <span data-ttu-id="6dee5-115">Os pontos de entrada do CMM *não* são funções de API e não devem ser chamados por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6dee5-115">CMM entry points are *not* API functions and should not be called by applications.</span></span>

 

<span data-ttu-id="6dee5-116">Quando CMMs são instalados, o programa de instalação os registra no registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="6dee5-116">When CMMs are installed, the installation program registers them in the Windows registry.</span></span> <span data-ttu-id="6dee5-117">Os aplicativos podem enumerar o CMMs registrado e selecionar um usando a função [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) .</span><span class="sxs-lookup"><span data-stu-id="6dee5-117">Applications can enumerate the registered CMMs and select one using the [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) function.</span></span> <span data-ttu-id="6dee5-118">O aplicativo de exemplo a seguir demonstra como enumerar todos os CMMs registrados.</span><span class="sxs-lookup"><span data-stu-id="6dee5-118">The following sample application demonstrates how to enumerate all registered CMMs.</span></span>


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
                 gszICMatcher, &amp;hkCMM);
    DWORD dwMaxName, dwMaxValue;
    DWORD dwInfoErr = RegQueryInfoKey(&amp;hkCMM, NULL, NULL,
                                NULL, NULL, NULL, NULL, NULL,
                                &amp;dwMaxName, &amp;dwMaxValue,
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
                   &amp;cjCMM,NULL,&amp;dwType,
                   chCMMFile,&amp;cjCMMFile) == ERROR_SUCCESS)
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



 

 




