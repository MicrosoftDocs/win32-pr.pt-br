---
description: Um aplicativo pode alterar o diretório atual chamando a função SetCurrentDirectory.
ms.assetid: b08e7739-55d4-4690-9ce5-2a8cb29214e9
title: Alterando o diretório atual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60cf742c872bab7d37e115afa815fff961d2f975bfbd3db75ff61a5e992d64a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632106"
---
# <a name="changing-the-current-directory"></a>Alterando o diretório atual

O diretório no final do caminho ativo é chamado de diretório atual; é o diretório no qual o aplicativo ativo foi iniciado, a menos que tenha sido explicitamente alterado. Um aplicativo pode determinar qual diretório é atual chamando a função [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) . Às vezes, é necessário usar a função [**Getfullpathname**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) para garantir que a letra da unidade seja incluída se o aplicativo exigir.

> [!Note]  
> Embora cada processo possa ter apenas um diretório atual, se o aplicativo alternar os volumes usando a função [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) , o sistema lembrará o último caminho atual para cada volume (letra da unidade). Esse comportamento se manifestará somente ao especificar uma letra de unidade sem um caminho totalmente qualificado ao alterar o ponto de referência do diretório atual para um volume diferente. Isso se aplica a operações Get ou set.

 

Um aplicativo pode alterar o diretório atual chamando a função [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) .

O exemplo a seguir demonstra o uso de [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) e [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory).


```C++
#include <windows.h> 
#include <stdio.h>
#include <tchar.h>

#define BUFSIZE MAX_PATH
 
void _tmain(int argc, TCHAR **argv) 
{ 
   TCHAR Buffer[BUFSIZE];
   DWORD dwRet;

   if(argc != 2)
   {
      _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
      return;
   }

   dwRet = GetCurrentDirectory(BUFSIZE, Buffer);

   if( dwRet == 0 )
   {
      printf("GetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   if(dwRet > BUFSIZE)
   {
      printf("Buffer too small; need %d characters\n", dwRet);
      return;
   }

   if( !SetCurrentDirectory(argv[1]))
   {
      printf("SetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   _tprintf(TEXT("Set current directory to %s\n"), argv[1]);

   if( !SetCurrentDirectory(Buffer) )
   {
      printf("SetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   _tprintf(TEXT("Restored previous directory (%s)\n"), Buffer);
}
```



 

 



