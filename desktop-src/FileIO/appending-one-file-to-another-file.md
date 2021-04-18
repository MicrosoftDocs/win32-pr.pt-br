---
description: Código de exemplo que mostra como um aplicativo pode acrescentar um arquivo ao final de outro arquivo, incluindo como abrir e fechar arquivos, ler e gravar em arquivos, e bloquear e desbloquear arquivos.
ms.assetid: e4d1f842-16a1-47e4-84b4-9bb44aaa1dc5
title: Anexando um arquivo a outro arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 546d24fe88a2bbf22c190a0caca3b3f98e753720
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810373"
---
# <a name="appending-one-file-to-another-file"></a><span data-ttu-id="3063d-103">Anexando um arquivo a outro arquivo</span><span class="sxs-lookup"><span data-stu-id="3063d-103">Appending One File to Another File</span></span>

<span data-ttu-id="3063d-104">O exemplo de código neste tópico mostra como abrir e fechar arquivos, ler e gravar em arquivos, e bloquear e desbloquear arquivos.</span><span class="sxs-lookup"><span data-stu-id="3063d-104">The code example in this topic shows you how to open and close files, read and write to files, and lock and unlock files.</span></span>

<span data-ttu-id="3063d-105">No exemplo, o aplicativo anexa um arquivo ao final de outro arquivo.</span><span class="sxs-lookup"><span data-stu-id="3063d-105">In the example, the application appends one file to the end of another file.</span></span> <span data-ttu-id="3063d-106">Primeiro, o aplicativo abre o arquivo que está sendo anexado com permissões que permitem que apenas o aplicativo grave nele.</span><span class="sxs-lookup"><span data-stu-id="3063d-106">First, the application opens the file being appended with permissions that allow only the application to write to it.</span></span> <span data-ttu-id="3063d-107">No entanto, durante o processo de acréscimo, outros processos podem abrir o arquivo com permissão somente leitura, que fornece uma exibição de instantâneo do arquivo que está sendo anexado.</span><span class="sxs-lookup"><span data-stu-id="3063d-107">However, during the append process other processes can open the file with read-only permission, which provides a snapshot view of the file being appended.</span></span> <span data-ttu-id="3063d-108">Em seguida, o arquivo é bloqueado durante o processo de acréscimo real para garantir a integridade dos dados que estão sendo gravados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="3063d-108">Then, the file is locked during the actual append process to ensure the integrity of the data being written to the file.</span></span>

<span data-ttu-id="3063d-109">Este exemplo não usa transações.</span><span class="sxs-lookup"><span data-stu-id="3063d-109">This example does not use transactions.</span></span> <span data-ttu-id="3063d-110">Se você estivesse usando operações transacionadas, só poderá ter acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3063d-110">If you were using transacted operations, you would only be able have read-only access.</span></span> <span data-ttu-id="3063d-111">Nesse caso, você veria apenas os dados acrescentados após a conclusão da operação de confirmação de transação.</span><span class="sxs-lookup"><span data-stu-id="3063d-111">In this case, you would only see the appended data after the transaction commit operation completed.</span></span>

<span data-ttu-id="3063d-112">O exemplo também mostra que o aplicativo abre dois arquivos usando [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea):</span><span class="sxs-lookup"><span data-stu-id="3063d-112">The example also shows that the application opens two files by using [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea):</span></span>

-   <span data-ttu-id="3063d-113">One.txt é aberto para leitura.</span><span class="sxs-lookup"><span data-stu-id="3063d-113">One.txt is opened for reading.</span></span>
-   <span data-ttu-id="3063d-114">Two.txt é aberto para gravação e leitura compartilhada.</span><span class="sxs-lookup"><span data-stu-id="3063d-114">Two.txt is opened for writing and shared reading.</span></span>

<span data-ttu-id="3063d-115">Em seguida, o aplicativo usa [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) para acrescentar o conteúdo de One.txt ao final de Two.txt lendo e gravando os blocos de 4 KB.</span><span class="sxs-lookup"><span data-stu-id="3063d-115">Then the application uses [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) and [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) to append the contents of One.txt to the end of Two.txt by reading and writing the 4 KB blocks.</span></span> <span data-ttu-id="3063d-116">No entanto, antes de gravar no segundo arquivo, o aplicativo usa [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) para definir o ponteiro do segundo arquivo para o final desse arquivo e usa o [**lockfile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) para bloquear a área a ser gravada.</span><span class="sxs-lookup"><span data-stu-id="3063d-116">However, before writing to the second file, the application uses [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) to set the pointer of the second file to the end of that file, and uses [**LockFile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) to lock the area to be written.</span></span> <span data-ttu-id="3063d-117">Isso impede que outro thread ou processo com um identificador duplicado acesse a área enquanto a operação de gravação está em andamento.</span><span class="sxs-lookup"><span data-stu-id="3063d-117">This prevents another thread or process with a duplicate handle from accessing the area while the write operation is in progress.</span></span> <span data-ttu-id="3063d-118">Quando cada operação de gravação é concluída, o [**desbloqueiofile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) é usado para desbloquear a área bloqueada.</span><span class="sxs-lookup"><span data-stu-id="3063d-118">When each write operation is complete, [**UnlockFile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) is used to unlock the locked area.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

void main()
{
  HANDLE hFile;
  HANDLE hAppend;
  DWORD  dwBytesRead, dwBytesWritten, dwPos;
  BYTE   buff[4096];

  // Open the existing file.

  hFile = CreateFile(TEXT("one.txt"), // open One.txt
            GENERIC_READ,             // open for reading
            0,                        // do not share
            NULL,                     // no security
            OPEN_EXISTING,            // existing file only
            FILE_ATTRIBUTE_NORMAL,    // normal file
            NULL);                    // no attr. template

  if (hFile == INVALID_HANDLE_VALUE)
  {
     printf("Could not open One.txt."); 
     return;
  }

  // Open the existing file, or if the file does not exist,
  // create a new file.

  hAppend = CreateFile(TEXT("two.txt"), // open Two.txt
              FILE_APPEND_DATA,         // open for writing
              FILE_SHARE_READ,          // allow multiple readers
              NULL,                     // no security
              OPEN_ALWAYS,              // open or create
              FILE_ATTRIBUTE_NORMAL,    // normal file
              NULL);                    // no attr. template

  if (hAppend == INVALID_HANDLE_VALUE)
  {
     printf("Could not open Two.txt."); 
     return;
  }

  // Append the first file to the end of the second file.
  // Lock the second file to prevent another process from
  // accessing it while writing to it. Unlock the
  // file when writing is complete.

  while (ReadFile(hFile, buff, sizeof(buff), &dwBytesRead, NULL)
      && dwBytesRead > 0)
    {
    dwPos = SetFilePointer(hAppend, 0, NULL, FILE_END);
    LockFile(hAppend, dwPos, 0, dwBytesRead, 0);
    WriteFile(hAppend, buff, dwBytesRead, &dwBytesWritten, NULL);
    UnlockFile(hAppend, dwPos, 0, dwBytesRead, 0);
    }

  // Close both files.

  CloseHandle(hFile);
  CloseHandle(hAppend);
}
```



 

 



