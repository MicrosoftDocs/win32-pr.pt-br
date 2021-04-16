---
description: O exemplo a seguir usa a função VerifyVersionInfo para determinar se os pacotes de produto especificados estão instalados no computador local.
ms.assetid: 9f405e99-28f5-4415-a274-682b87ae6842
title: Detectando um pacote de produtos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594acbe22283e1c2a3be3ce60116076b2de6f3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750417"
---
# <a name="detecting-a-product-suite"></a><span data-ttu-id="e3388-103">Detectando um pacote de produtos</span><span class="sxs-lookup"><span data-stu-id="e3388-103">Detecting a Product Suite</span></span>

<span data-ttu-id="e3388-104">O exemplo a seguir usa a função [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) para determinar se os pacotes de produto especificados estão instalados no computador local.</span><span class="sxs-lookup"><span data-stu-id="e3388-104">The following example uses the [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) function to determine whether the specified product suite(s) are installed on the local computer.</span></span>

<span data-ttu-id="e3388-105">Este exemplo usa a VER \_ e o sinalizador.</span><span class="sxs-lookup"><span data-stu-id="e3388-105">This example uses the VER\_AND flag.</span></span> <span data-ttu-id="e3388-106">Se dois sinalizadores forem especificados na máscara do conjunto, a função retornará **true** somente se ambos os pacotes de produto estiverem presentes.</span><span class="sxs-lookup"><span data-stu-id="e3388-106">If two flags are specified in the suite mask, the function returns **TRUE** only if both product suites are present.</span></span> <span data-ttu-id="e3388-107">Se o exemplo tiver sido alterado para usar o VER \_ ou sinalizar, [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) retornará **true** se o pacote de produtos estivesse presente.</span><span class="sxs-lookup"><span data-stu-id="e3388-107">If the example were changed to use the VER\_OR flag, [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) would return **TRUE** if either product suite were present.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

BOOL CheckProductSuite ( WORD wSuite ) 
{
  OSVERSIONINFOEX osvi;
  DWORDLONG dwlConditionMask = 0;

  // Initialize the OSVERSIONINFOEX structure.

  ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
  osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
  osvi.wSuiteMask = wSuite;

  // Set up the condition mask.

  VER_SET_CONDITION( dwlConditionMask, 
          VER_SUITENAME, VER_AND );

  // Perform the test.

  return VerifyVersionInfo(
          &osvi, 
          VER_SUITENAME,
          dwlConditionMask);
}

void main()
{
    if( CheckProductSuite(VER_SUITE_ENTERPRISE) )
        printf( "The system meets the requirements.\n" );
    else printf( "The system does not meet the requirements.\n");
}
```



 

 



