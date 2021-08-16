---
description: O exemplo a seguir usa a função GetSystemInfo para obter informações de hardware, como o identificador OEM, o tipo de processador, o tamanho da página e assim por diante. O exemplo exibe as informações no console.
ms.assetid: 9f943926-9ca7-4d4c-ad1e-b68c248e0e01
title: Obter informações de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9302e386d3054923f9914fc105c1bc90f380b9b21b869b0d854d6a78af1d81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764451"
---
# <a name="getting-hardware-information"></a>Obter informações de hardware

O exemplo a seguir usa a [**função GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) para obter informações de hardware, como o identificador OEM, o tipo de processador, o tamanho da página e assim por diante. O exemplo exibe as informações no console.


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "user32.lib")

void main()
{
   SYSTEM_INFO siSysInfo;
 
   // Copy the hardware information to the SYSTEM_INFO structure. 
 
   GetSystemInfo(&siSysInfo); 
 
   // Display the contents of the SYSTEM_INFO structure. 

   printf("Hardware information: \n");  
   printf("  OEM ID: %u\n", siSysInfo.dwOemId);
   printf("  Number of processors: %u\n", 
      siSysInfo.dwNumberOfProcessors); 
   printf("  Page size: %u\n", siSysInfo.dwPageSize); 
   printf("  Processor type: %u\n", siSysInfo.dwProcessorType); 
   printf("  Minimum application address: %lx\n", 
      siSysInfo.lpMinimumApplicationAddress); 
   printf("  Maximum application address: %lx\n", 
      siSysInfo.lpMaximumApplicationAddress); 
   printf("  Active processor mask: %u\n", 
      siSysInfo.dwActiveProcessorMask); 
}
```



 

 
