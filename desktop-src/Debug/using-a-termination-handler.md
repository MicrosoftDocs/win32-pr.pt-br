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
# <a name="using-a-termination-handler"></a><span data-ttu-id="b78b1-103">Usando um manipulador de encerramento</span><span class="sxs-lookup"><span data-stu-id="b78b1-103">Using a Termination Handler</span></span>

<span data-ttu-id="b78b1-104">O exemplo a seguir mostra como um manipulador de terminação é usado para garantir que os recursos sejam liberados quando a execução de um corpo de código protegido for encerrada.</span><span class="sxs-lookup"><span data-stu-id="b78b1-104">The following example shows how a termination handler is used to ensure that resources are released when execution of a guarded body of code terminates.</span></span> <span data-ttu-id="b78b1-105">Nesse caso, um thread usa a função [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) para aguardar a propriedade de um objeto de seção crítica.</span><span class="sxs-lookup"><span data-stu-id="b78b1-105">In this case, a thread uses the [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) function to wait for ownership of a critical section object.</span></span> <span data-ttu-id="b78b1-106">Quando o thread terminar de executar o código protegido pela seção crítica, ele deverá chamar a função [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) para tornar o objeto de seção crítica disponível para outros threads.</span><span class="sxs-lookup"><span data-stu-id="b78b1-106">When the thread is finished executing the code that is protected by the critical section, it must call the [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) function to make the critical section object available to other threads.</span></span> <span data-ttu-id="b78b1-107">O uso de um manipulador de encerramento garante que isso ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="b78b1-107">Using a termination handler guarantees that this will happen.</span></span> <span data-ttu-id="b78b1-108">Para obter mais informações, consulte [objetos de seção crítica](../sync/critical-section-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b78b1-108">For more information, see [critical section objects](../sync/critical-section-objects.md).</span></span>


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



 

 
