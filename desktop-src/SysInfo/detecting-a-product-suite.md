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
# <a name="detecting-a-product-suite"></a>Detectando um pacote de produtos

O exemplo a seguir usa a função [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) para determinar se os pacotes de produto especificados estão instalados no computador local.

Este exemplo usa a VER \_ e o sinalizador. Se dois sinalizadores forem especificados na máscara do conjunto, a função retornará **true** somente se ambos os pacotes de produto estiverem presentes. Se o exemplo tiver sido alterado para usar o VER \_ ou sinalizar, [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) retornará **true** se o pacote de produtos estivesse presente.


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



 

 



