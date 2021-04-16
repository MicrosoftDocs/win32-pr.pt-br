---
description: Para mover um diretório para outro local, juntamente com os arquivos e subdiretórios contidos nele, chame a função MoveFileEx, MoveFileWithProgress ou MoveFileTransacted.
ms.assetid: ca56c109-d6a3-456e-956c-126ce4aee8ba
title: Movendo diretórios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56167f0831894350a044104bce1f41ef3c5770ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750864"
---
# <a name="moving-directories"></a>Movendo diretórios

Para mover um diretório para outro local, juntamente com os arquivos e subdiretórios contidos nele, chame a função [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa), [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)ou [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) . A função [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa) tem a mesma funcionalidade que [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa), exceto que **MoveFileWithProgress** permite que você especifique uma rotina de retorno de chamada que recebe notificações sobre o andamento da operação. A função [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) permite que você execute a operação como uma operação transacionada.

O exemplo a seguir demonstra o uso da função [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) com um diretório.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

int __cdecl _tmain(int argc, TCHAR *argv[])
{
    printf("\n");
    if( argc != 3 )
    {
        printf("ERROR:  Incorrect number of arguments\n\n");
        printf("Description:\n");
        printf("  Moves a directory and its contents\n\n");
        printf("Usage:\n");
        _tprintf(TEXT("  %s [source_dir] [target_dir]\n\n"), argv[0]);
        printf("  The target directory cannot exist already.\n\n");
        return;
    }

    // Move the source directory to the target directory location.
    // The target directory must be on the same drive as the source.
    // The target directory cannot already exist.

    if (!MoveFileEx(argv[1], argv[2], MOVEFILE_WRITE_THROUGH))
    { 
        printf ("MoveFileEx failed with error %d\n", GetLastError());
        return;
    }
    else _tprintf(TEXT("%s has been moved to %s\n"), argv[1], argv[2]);
}
```



 

 



