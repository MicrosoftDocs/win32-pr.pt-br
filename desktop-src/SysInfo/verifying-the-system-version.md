---
description: Isso contém exemplos que usam a função VerifyVersionInfo para determinar se o aplicativo está sendo executado em um sistema operacional específico.
ms.assetid: f39c35ae-9be5-4a03-9079-6fcc63387f6b
title: Verificando a versão do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ddb3562230d0708ddc55d0f8214286ea6c3008
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165427"
---
# <a name="verifying-the-system-version"></a><span data-ttu-id="32aa8-103">Verificando a versão do sistema</span><span class="sxs-lookup"><span data-stu-id="32aa8-103">Verifying the System Version</span></span>

<span data-ttu-id="32aa8-104">\[ O uso da função [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) para verificar se o sistema operacional em execução no momento não é recomendado.</span><span class="sxs-lookup"><span data-stu-id="32aa8-104">\[ Use of the [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) function to verify the currently running operating system is not recommended.</span></span> <span data-ttu-id="32aa8-105">Em vez disso, use as [ **APIs auxiliares de versão**](version-helper-apis.md)\]</span><span class="sxs-lookup"><span data-stu-id="32aa8-105">Instead, use the [**Version Helper APIs**](version-helper-apis.md)\]</span></span>

<span data-ttu-id="32aa8-106">Isso contém exemplos que usam a função [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) para determinar se o aplicativo está sendo executado em um sistema operacional específico.</span><span class="sxs-lookup"><span data-stu-id="32aa8-106">This contains examples that use the [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) function to determine whether the application is running on a specific operating system.</span></span>

<span data-ttu-id="32aa8-107">As etapas principais em cada exemplo são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="32aa8-107">The main steps in each example are as follows:</span></span>

1.  <span data-ttu-id="32aa8-108">Defina os valores apropriados na estrutura [**OSVERSIONINFOEX**](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="32aa8-108">Set the appropriate values in the [**OSVERSIONINFOEX**](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa) structure.</span></span>
2.  <span data-ttu-id="32aa8-109">Defina a máscara de condição apropriada usando a macro de [**\_ \_ condição do conjunto de ver**](/windows/desktop/api/Winnt/nf-winnt-ver_set_condition) .</span><span class="sxs-lookup"><span data-stu-id="32aa8-109">Set the appropriate condition mask using the [**VER\_SET\_CONDITION**](/windows/desktop/api/Winnt/nf-winnt-ver_set_condition) macro.</span></span>
3.  <span data-ttu-id="32aa8-110">Chame [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) para executar o teste.</span><span class="sxs-lookup"><span data-stu-id="32aa8-110">Call [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) to perform the test.</span></span>

## <a name="example-1"></a><span data-ttu-id="32aa8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="32aa8-111">Example 1</span></span>

<span data-ttu-id="32aa8-112">O exemplo a seguir determina se o aplicativo está em execução no Windows XP com Service Pack 2 (SP2) ou uma versão posterior do Windows, como o Windows Server 2003 ou o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="32aa8-112">The following example determines whether the application is running on Windows XP with Service Pack 2 (SP2) or a later version of Windows, such as Windows Server 2003 or Windows Vista.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

BOOL Is_WinXP_SP2_or_Later () 
{
   OSVERSIONINFOEX osvi;
   DWORDLONG dwlConditionMask = 0;
   int op=VER_GREATER_EQUAL;

   // Initialize the OSVERSIONINFOEX structure.

   ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
   osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
   osvi.dwMajorVersion = 5;
   osvi.dwMinorVersion = 1;
   osvi.wServicePackMajor = 2;
   osvi.wServicePackMinor = 0;

   // Initialize the condition mask.

   VER_SET_CONDITION( dwlConditionMask, VER_MAJORVERSION, op );
   VER_SET_CONDITION( dwlConditionMask, VER_MINORVERSION, op );
   VER_SET_CONDITION( dwlConditionMask, VER_SERVICEPACKMAJOR, op );
   VER_SET_CONDITION( dwlConditionMask, VER_SERVICEPACKMINOR, op );

   // Perform the test.

   return VerifyVersionInfo(
      &osvi, 
      VER_MAJORVERSION | VER_MINORVERSION | 
      VER_SERVICEPACKMAJOR | VER_SERVICEPACKMINOR,
      dwlConditionMask);
}

void main()
{
    if(Is_WinXP_SP2_or_Later())
        printf("The system meets the requirements.\n");
    else printf("The system does not meet the requirements.\n");
}
```



## <a name="example-2"></a><span data-ttu-id="32aa8-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="32aa8-113">Example 2</span></span>

<span data-ttu-id="32aa8-114">O código a seguir verifica se o aplicativo está em execução no Windows 2000 Server ou em um servidor posterior, como o Windows Server 2003 ou o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="32aa8-114">The following code verifies that the application is running on Windows 2000 Server or a later server, such as Windows Server 2003 or Windows Server 2008.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

BOOL Is_Win_Server() 
{
   OSVERSIONINFOEX osvi;
   DWORDLONG dwlConditionMask = 0;
   int op=VER_GREATER_EQUAL;

   // Initialize the OSVERSIONINFOEX structure.

   ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
   osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
   osvi.dwMajorVersion = 5;
   osvi.dwMinorVersion = 0;
   osvi.wServicePackMajor = 0;
   osvi.wServicePackMinor = 0;
   osvi.wProductType = VER_NT_SERVER;

   // Initialize the condition mask.

   VER_SET_CONDITION( dwlConditionMask, VER_MAJORVERSION, op );
   VER_SET_CONDITION( dwlConditionMask, VER_MINORVERSION, op );
   VER_SET_CONDITION( dwlConditionMask, VER_SERVICEPACKMAJOR, op );
   VER_SET_CONDITION( dwlConditionMask, VER_SERVICEPACKMINOR, op );
   VER_SET_CONDITION( dwlConditionMask, VER_PRODUCT_TYPE, VER_EQUAL );

   // Perform the test.

   return VerifyVersionInfo(
      &osvi, 
      VER_MAJORVERSION | VER_MINORVERSION | 
      VER_SERVICEPACKMAJOR | VER_SERVICEPACKMINOR |
      VER_PRODUCT_TYPE,
      dwlConditionMask);
}

void main()
{
    if(Is_Win_Server())
        printf("The system meets the requirements.\n");
    else printf("The system does not meet the requirements.\n");
}
```



 

 



