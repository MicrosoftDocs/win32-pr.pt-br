---
description: O exemplo a seguir ilustra o uso de nomes de objeto criando e abrindo um mutex nomeado.
ms.assetid: 06199f83-8fe0-42b9-9db1-58fe1443db4e
title: Usando objetos nomeados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e31d21af713a28d5bee501349e818327750cba15a961ebd0f6a5295be91e0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765125"
---
# <a name="using-named-objects"></a>Usando objetos nomeados

O exemplo a seguir ilustra o uso de [nomes de objeto](object-names.md) criando e abrindo um mutex nomeado.

## <a name="first-process"></a>Primeiro processo

O primeiro processo usa a função [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) para criar o objeto mutex. Observe que essa função é realizada com sucesso mesmo se houver um objeto existente com o mesmo nome.


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



## <a name="second-process"></a>Segundo processo

O segundo processo usa a função [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) para abrir um identificador para o mutex existente. Essa função falhará se um objeto mutex com o nome especificado não existir. O parâmetro Access solicita acesso completo ao objeto mutex, que é necessário para que o identificador seja usado em qualquer uma das funções Wait.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Nomes de objeto](object-names.md)
</dt> <dt>

[Usando objetos mutex](using-mutex-objects.md)
</dt> </dl>

 

 
