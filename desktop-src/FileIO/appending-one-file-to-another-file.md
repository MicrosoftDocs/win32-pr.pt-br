---
description: Código de exemplo que mostra como um aplicativo pode acrescentar um arquivo ao final de outro arquivo, incluindo como abrir e fechar arquivos, ler e gravar em arquivos, e bloquear e desbloquear arquivos.
ms.assetid: e4d1f842-16a1-47e4-84b4-9bb44aaa1dc5
title: Anexando um arquivo a outro arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 585521c1d0bb85c41806ba83c2c0940dc3523035731279d4da3f06af45334984
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766217"
---
# <a name="appending-one-file-to-another-file"></a>Anexando um arquivo a outro arquivo

O exemplo de código neste tópico mostra como abrir e fechar arquivos, ler e gravar em arquivos, e bloquear e desbloquear arquivos.

No exemplo, o aplicativo anexa um arquivo ao final de outro arquivo. Primeiro, o aplicativo abre o arquivo que está sendo anexado com permissões que permitem que apenas o aplicativo grave nele. No entanto, durante o processo de acréscimo, outros processos podem abrir o arquivo com permissão somente leitura, que fornece uma exibição de instantâneo do arquivo que está sendo anexado. Em seguida, o arquivo é bloqueado durante o processo de acréscimo real para garantir a integridade dos dados que estão sendo gravados no arquivo.

Este exemplo não usa transações. Se você estivesse usando operações transacionadas, só poderá ter acesso somente leitura. Nesse caso, você veria apenas os dados acrescentados após a conclusão da operação de confirmação de transação.

O exemplo também mostra que o aplicativo abre dois arquivos usando [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea):

-   One.txt é aberto para leitura.
-   Two.txt é aberto para gravação e leitura compartilhada.

Em seguida, o aplicativo usa [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) para acrescentar o conteúdo de One.txt ao final de Two.txt lendo e gravando os blocos de 4 KB. No entanto, antes de gravar no segundo arquivo, o aplicativo usa [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) para definir o ponteiro do segundo arquivo para o final desse arquivo e usa o [**lockfile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) para bloquear a área a ser gravada. Isso impede que outro thread ou processo com um identificador duplicado acesse a área enquanto a operação de gravação está em andamento. Quando cada operação de gravação é concluída, o [**desbloqueiofile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) é usado para desbloquear a área bloqueada.


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



 

 



