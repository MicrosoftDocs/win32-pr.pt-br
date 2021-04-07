---
description: O exemplo a seguir mostra como um manipulador de terminação é usado para garantir que os recursos sejam liberados quando a execução de um corpo de código protegido for encerrada.
ms.assetid: 442af2a3-d62a-4dd8-a934-da69c1d2a738
title: Usando um manipulador de encerramento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cbe73eda8533ed5805159d5386b69daa4d03194
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920354"
---
# <a name="using-a-termination-handler"></a>Usando um manipulador de encerramento

O exemplo a seguir mostra como um manipulador de terminação é usado para garantir que os recursos sejam liberados quando a execução de um corpo de código protegido for encerrada. Nesse caso, um thread usa a função [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) para aguardar a propriedade de um objeto de seção crítica. Quando o thread terminar de executar o código protegido pela seção crítica, ele deverá chamar a função [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) para tornar o objeto de seção crítica disponível para outros threads. O uso de um manipulador de encerramento garante que isso ocorrerá. Para obter mais informações, consulte [objetos de seção crítica](../sync/critical-section-objects.md).


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



 

 
