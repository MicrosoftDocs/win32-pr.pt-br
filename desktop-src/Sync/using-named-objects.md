---
description: O exemplo a seguir ilustra o uso de nomes de objeto criando e abrindo um mutex nomeado.
ms.assetid: 06199f83-8fe0-42b9-9db1-58fe1443db4e
title: Usando objetos nomeados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a349e3e26f661ca988bc5c5ebbc7b3c6ea622956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811264"
---
# <a name="using-named-objects"></a><span data-ttu-id="d64e7-103">Usando objetos nomeados</span><span class="sxs-lookup"><span data-stu-id="d64e7-103">Using Named Objects</span></span>

<span data-ttu-id="d64e7-104">O exemplo a seguir ilustra o uso de [nomes de objeto](object-names.md) criando e abrindo um mutex nomeado.</span><span class="sxs-lookup"><span data-stu-id="d64e7-104">The following example illustrates the use of [object names](object-names.md) by creating and opening a named mutex.</span></span>

## <a name="first-process"></a><span data-ttu-id="d64e7-105">Primeiro processo</span><span class="sxs-lookup"><span data-stu-id="d64e7-105">First Process</span></span>

<span data-ttu-id="d64e7-106">O primeiro processo usa a função [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) para criar o objeto mutex.</span><span class="sxs-lookup"><span data-stu-id="d64e7-106">The first process uses the [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) function to create the mutex object.</span></span> <span data-ttu-id="d64e7-107">Observe que essa função é realizada com sucesso mesmo se houver um objeto existente com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="d64e7-107">Note that this function succeeds even if there is an existing object with the same name.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>

// This process creates the mutex object.

int main(void)
{
    HANDLE hMutex; 

    hMutex = CreateMutex( 
        NULL,                        // default security descriptor
        FALSE,                       // mutex not owned
        TEXT("NameOfMutexObject"));  // object name

    if (hMutex == NULL) 
        printf("CreateMutex error: %d\n", GetLastError() ); 
    else 
        if ( GetLastError() == ERROR_ALREADY_EXISTS ) 
            printf("CreateMutex opened an existing mutex\n"); 
        else printf("CreateMutex created a new mutex.\n");

    // Keep this process around until the second process is run
    _getch();

    CloseHandle(hMutex);

    return 0;
}
```



## <a name="second-process"></a><span data-ttu-id="d64e7-108">Segundo processo</span><span class="sxs-lookup"><span data-stu-id="d64e7-108">Second Process</span></span>

<span data-ttu-id="d64e7-109">O segundo processo usa a função [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) para abrir um identificador para o mutex existente.</span><span class="sxs-lookup"><span data-stu-id="d64e7-109">The second process uses the [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) function to open a handle to the existing mutex.</span></span> <span data-ttu-id="d64e7-110">Essa função falhará se um objeto mutex com o nome especificado não existir.</span><span class="sxs-lookup"><span data-stu-id="d64e7-110">This function fails if a mutex object with the specified name does not exist.</span></span> <span data-ttu-id="d64e7-111">O parâmetro Access solicita acesso completo ao objeto mutex, que é necessário para que o identificador seja usado em qualquer uma das funções Wait.</span><span class="sxs-lookup"><span data-stu-id="d64e7-111">The access parameter requests full access to the mutex object, which is necessary for the handle to be used in any of the wait functions.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

// This process opens a handle to a mutex created by another process.

int main(void)
{
    HANDLE hMutex; 

    hMutex = OpenMutex( 
        MUTEX_ALL_ACCESS,            // request full access
        FALSE,                       // handle not inheritable
        TEXT("NameOfMutexObject"));  // object name

    if (hMutex == NULL) 
        printf("OpenMutex error: %d\n", GetLastError() );
    else printf("OpenMutex successfully opened the mutex.\n");

    CloseHandle(hMutex);

    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="d64e7-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d64e7-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d64e7-113">Nomes de objeto</span><span class="sxs-lookup"><span data-stu-id="d64e7-113">Object Names</span></span>](object-names.md)
</dt> <dt>

[<span data-ttu-id="d64e7-114">Usando objetos mutex</span><span class="sxs-lookup"><span data-stu-id="d64e7-114">Using Mutex Objects</span></span>](using-mutex-objects.md)
</dt> </dl>

 

 
