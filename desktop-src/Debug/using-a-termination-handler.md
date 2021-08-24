---
description: O exemplo a seguir mostra como um manipulador de encerramento é usado para garantir que os recursos sejam liberados quando a execução de um corpo protegido de código é encerrada.
ms.assetid: 442af2a3-d62a-4dd8-a934-da69c1d2a738
title: Usando um manipulador de encerramento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6fe2d2ba8a7b8443eb164571a42347ce6cfb7e99c44f90da25c6fd57863e0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655076"
---
# <a name="using-a-termination-handler"></a>Usando um manipulador de encerramento

O exemplo a seguir mostra como um manipulador de encerramento é usado para garantir que os recursos sejam liberados quando a execução de um corpo protegido de código é encerrada. Nesse caso, um thread usa a [**função EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) para aguardar a propriedade de um objeto de seção crítico. Quando o thread terminar de executar o código protegido pela seção crítica, ele deverá chamar a função [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) para disponibilizar o objeto de seção crítico para outros threads. O uso de um manipulador de encerramento garante que isso aconteça. Para obter mais informações, consulte [objetos de seção críticos.](../sync/critical-section-objects.md)


```C++
LPTSTR lpBuffer = NULL; 
CRITICAL_SECTION CriticalSection; 

// EnterCriticalSection synchronizes code with other threads. 
EnterCriticalSection(&CriticalSection); 
 
__try 
{ 
    // Perform a task that may cause an exception. 
    lpBuffer = (LPTSTR) LocalAlloc(LPTR, 10); 
    StringCchCopy(lpBuffer, 10, TEXT("Hello"));

    _tprintf(TEXT("%s\n"),lpBuffer); 
    LocalFree(lpBuffer); 
} 
__finally 
{ 
    // LeaveCriticalSection is called even if an exception occurred. 
    LeaveCriticalSection(&CriticalSection); 
}
```



 

 
