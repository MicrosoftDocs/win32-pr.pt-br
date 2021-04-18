---
description: Para compartilhar dados, vários processos podem usar arquivos mapeados por memória que o arquivo de paginação do sistema armazena.
ms.assetid: 17458be2-3ef7-42f2-a717-abf73ac4846f
title: Criando a memória compartilhada nomeada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ac708497ceb12ed099c7a9c0b3788d7a05a925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767625"
---
# <a name="creating-named-shared-memory"></a><span data-ttu-id="63f23-103">Criando a memória compartilhada nomeada</span><span class="sxs-lookup"><span data-stu-id="63f23-103">Creating Named Shared Memory</span></span>

<span data-ttu-id="63f23-104">Para compartilhar dados, vários processos podem usar arquivos mapeados por memória que o arquivo de paginação do sistema armazena.</span><span class="sxs-lookup"><span data-stu-id="63f23-104">To share data, multiple processes can use memory-mapped files that the system paging file stores.</span></span>

## <a name="first-process"></a><span data-ttu-id="63f23-105">Primeiro processo</span><span class="sxs-lookup"><span data-stu-id="63f23-105">First Process</span></span>

<span data-ttu-id="63f23-106">O primeiro processo cria o objeto de mapeamento de arquivo chamando a função [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) com um **\_ \_ valor de identificador inválido** e um nome para o objeto.</span><span class="sxs-lookup"><span data-stu-id="63f23-106">The first process creates the file mapping object by calling the [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) function with **INVALID\_HANDLE\_VALUE** and a name for the object.</span></span> <span data-ttu-id="63f23-107">Usando o sinalizador de **página \_ ReadWrite** , o processo tem permissão de leitura/gravação para a memória por meio de qualquer exibição de arquivo que é criada.</span><span class="sxs-lookup"><span data-stu-id="63f23-107">By using the **PAGE\_READWRITE** flag, the process has read/write permission to the memory through any file views that are created.</span></span>

<span data-ttu-id="63f23-108">Em seguida, o processo usa o identificador de objeto de mapeamento de arquivo que [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) retorna em uma chamada para [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) para criar uma exibição do arquivo no espaço de endereço do processo.</span><span class="sxs-lookup"><span data-stu-id="63f23-108">Then the process uses the file mapping object handle that [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) returns in a call to [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) to create a view of the file in the process address space.</span></span> <span data-ttu-id="63f23-109">A função **MapViewOfFile** retorna um ponteiro para a exibição de arquivo, `pBuf` .</span><span class="sxs-lookup"><span data-stu-id="63f23-109">The **MapViewOfFile** function returns a pointer to the file view, `pBuf`.</span></span> <span data-ttu-id="63f23-110">Em seguida, o processo usa a função [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) para gravar uma cadeia de caracteres na exibição que pode ser acessada por outros processos.</span><span class="sxs-lookup"><span data-stu-id="63f23-110">The process then uses the [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) function to write a string to the view that can be accessed by other processes.</span></span>

<span data-ttu-id="63f23-111">A prefixação dos nomes de objeto de mapeamento de arquivo com "global \\ " permite que os processos se comuniquem entre si mesmo se estiverem em sessões do Terminal Server diferentes.</span><span class="sxs-lookup"><span data-stu-id="63f23-111">Prefixing the file mapping object names with "Global\\" allows processes to communicate with each other even if they are in different terminal server sessions.</span></span> <span data-ttu-id="63f23-112">Isso requer que o primeiro processo tenha o privilégio [**SeCreateGlobalPrivilege**](../secauthz/privilege-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="63f23-112">This requires that the first process must have the [**SeCreateGlobalPrivilege**](../secauthz/privilege-constants.md) privilege.</span></span>

<span data-ttu-id="63f23-113">Quando o processo não precisar mais de acesso ao objeto de mapeamento de arquivo, ele deverá chamar a função [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="63f23-113">When the process no longer needs access to the file mapping object, it should call the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="63f23-114">Quando todos os identificadores são fechados, o sistema pode liberar a seção do arquivo de paginação que o objeto usa.</span><span class="sxs-lookup"><span data-stu-id="63f23-114">When all handles are closed, the system can free the section of the paging file that the object uses.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUF_SIZE 256
TCHAR szName[]=TEXT("Global\\MyFileMappingObject");
TCHAR szMsg[]=TEXT("Message from first process.");

int _tmain()
{
   HANDLE hMapFile;
   LPCTSTR pBuf;

   hMapFile = CreateFileMapping(
                 INVALID_HANDLE_VALUE,    // use paging file
                 NULL,                    // default security
                 PAGE_READWRITE,          // read/write access
                 0,                       // maximum object size (high-order DWORD)
                 BUF_SIZE,                // maximum object size (low-order DWORD)
                 szName);                 // name of mapping object

   if (hMapFile == NULL)
   {
      _tprintf(TEXT("Could not create file mapping object (%d).\n"),
             GetLastError());
      return 1;
   }
   pBuf = (LPTSTR) MapViewOfFile(hMapFile,   // handle to map object
                        FILE_MAP_ALL_ACCESS, // read/write permission
                        0,
                        0,
                        BUF_SIZE);

   if (pBuf == NULL)
   {
      _tprintf(TEXT("Could not map view of file (%d).\n"),
             GetLastError());

       CloseHandle(hMapFile);

      return 1;
   }


   CopyMemory((PVOID)pBuf, szMsg, (_tcslen(szMsg) * sizeof(TCHAR)));
    _getch();

   UnmapViewOfFile(pBuf);

   CloseHandle(hMapFile);

   return 0;
}
```



## <a name="second-process"></a><span data-ttu-id="63f23-115">Segundo processo</span><span class="sxs-lookup"><span data-stu-id="63f23-115">Second Process</span></span>

<span data-ttu-id="63f23-116">Um segundo processo pode acessar a cadeia de caracteres gravada na memória compartilhada pelo primeiro processo chamando a função [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) especificando o mesmo nome para o objeto de mapeamento como o primeiro processo.</span><span class="sxs-lookup"><span data-stu-id="63f23-116">A second process can access the string written to the shared memory by the first process by calling the [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) function specifying the same name for the mapping object as the first process.</span></span> <span data-ttu-id="63f23-117">Em seguida, ele pode usar a função [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) para obter um ponteiro para a exibição de arquivo, `pBuf` .</span><span class="sxs-lookup"><span data-stu-id="63f23-117">Then it can use the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) function to obtain a pointer to the file view, `pBuf`.</span></span> <span data-ttu-id="63f23-118">O processo pode exibir essa cadeia de caracteres como faria com qualquer outra cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="63f23-118">The process can display this string as it would any other string.</span></span> <span data-ttu-id="63f23-119">Neste exemplo, a caixa de mensagem exibida contém a mensagem "mensagem do primeiro processo", que foi gravada pelo primeiro processo.</span><span class="sxs-lookup"><span data-stu-id="63f23-119">In this example, the message box displayed contains the message "Message from first process" that was written by the first process.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <tchar.h>
#pragma comment(lib, "user32.lib")

#define BUF_SIZE 256
TCHAR szName[]=TEXT("Global\\MyFileMappingObject");

int _tmain()
{
   HANDLE hMapFile;
   LPCTSTR pBuf;

   hMapFile = OpenFileMapping(
                   FILE_MAP_ALL_ACCESS,   // read/write access
                   FALSE,                 // do not inherit the name
                   szName);               // name of mapping object

   if (hMapFile == NULL)
   {
      _tprintf(TEXT("Could not open file mapping object (%d).\n"),
             GetLastError());
      return 1;
   }

   pBuf = (LPTSTR) MapViewOfFile(hMapFile, // handle to map object
               FILE_MAP_ALL_ACCESS,  // read/write permission
               0,
               0,
               BUF_SIZE);

   if (pBuf == NULL)
   {
      _tprintf(TEXT("Could not map view of file (%d).\n"),
             GetLastError());

      CloseHandle(hMapFile);

      return 1;
   }

   MessageBox(NULL, pBuf, TEXT("Process2"), MB_OK);

   UnmapViewOfFile(pBuf);

   CloseHandle(hMapFile);

   return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="63f23-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="63f23-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63f23-121">Compartilhando arquivos e memória</span><span class="sxs-lookup"><span data-stu-id="63f23-121">Sharing Files and Memory</span></span>](sharing-files-and-memory.md)
</dt> </dl>

 

 
