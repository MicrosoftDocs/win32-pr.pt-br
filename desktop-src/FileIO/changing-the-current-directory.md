---
description: Um aplicativo pode alterar o diretório atual chamando a função SetCurrentDirectory.
ms.assetid: b08e7739-55d4-4690-9ce5-2a8cb29214e9
title: Alterando o diretório atual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e507d206bcd988a7c00f557bde2b8a0ad39c79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758818"
---
# <a name="changing-the-current-directory"></a><span data-ttu-id="d6d17-103">Alterando o diretório atual</span><span class="sxs-lookup"><span data-stu-id="d6d17-103">Changing the Current Directory</span></span>

<span data-ttu-id="d6d17-104">O diretório no final do caminho ativo é chamado de diretório atual; é o diretório no qual o aplicativo ativo foi iniciado, a menos que tenha sido explicitamente alterado.</span><span class="sxs-lookup"><span data-stu-id="d6d17-104">The directory at the end of the active path is called the current directory; it is the directory in which the active application started, unless it has been explicitly changed.</span></span> <span data-ttu-id="d6d17-105">Um aplicativo pode determinar qual diretório é atual chamando a função [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) .</span><span class="sxs-lookup"><span data-stu-id="d6d17-105">An application can determine which directory is current by calling the [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) function.</span></span> <span data-ttu-id="d6d17-106">Às vezes, é necessário usar a função [**Getfullpathname**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) para garantir que a letra da unidade seja incluída se o aplicativo exigir.</span><span class="sxs-lookup"><span data-stu-id="d6d17-106">It is sometimes necessary to use the [**GetFullPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) function to ensure the drive letter is included if the application requires it.</span></span>

> [!Note]  
> <span data-ttu-id="d6d17-107">Embora cada processo possa ter apenas um diretório atual, se o aplicativo alternar os volumes usando a função [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) , o sistema lembrará o último caminho atual para cada volume (letra da unidade).</span><span class="sxs-lookup"><span data-stu-id="d6d17-107">Although each process can have only one current directory, if the application switches volumes by using the [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) function, the system remembers the last current path for each volume (drive letter).</span></span> <span data-ttu-id="d6d17-108">Esse comportamento se manifestará somente ao especificar uma letra de unidade sem um caminho totalmente qualificado ao alterar o ponto de referência do diretório atual para um volume diferente.</span><span class="sxs-lookup"><span data-stu-id="d6d17-108">This behavior will manifest itself only when specifying a drive letter without a fully qualified path when changing the current directory point of reference to a different volume.</span></span> <span data-ttu-id="d6d17-109">Isso se aplica a operações Get ou set.</span><span class="sxs-lookup"><span data-stu-id="d6d17-109">This applies to either Get or Set operations.</span></span>

 

<span data-ttu-id="d6d17-110">Um aplicativo pode alterar o diretório atual chamando a função [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) .</span><span class="sxs-lookup"><span data-stu-id="d6d17-110">An application can change the current directory by calling the [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) function.</span></span>

<span data-ttu-id="d6d17-111">O exemplo a seguir demonstra o uso de [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) e [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory).</span><span class="sxs-lookup"><span data-stu-id="d6d17-111">The following example demonstrates the use of [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) and [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory).</span></span>


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



 

 



