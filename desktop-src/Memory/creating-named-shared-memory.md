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
# <a name="creating-named-shared-memory"></a>Criando a memória compartilhada nomeada

Para compartilhar dados, vários processos podem usar arquivos mapeados por memória que o arquivo de paginação do sistema armazena.

## <a name="first-process"></a>Primeiro processo

O primeiro processo cria o objeto de mapeamento de arquivo chamando a função [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) com um **\_ \_ valor de identificador inválido** e um nome para o objeto. Usando o sinalizador de **página \_ ReadWrite** , o processo tem permissão de leitura/gravação para a memória por meio de qualquer exibição de arquivo que é criada.

Em seguida, o processo usa o identificador de objeto de mapeamento de arquivo que [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) retorna em uma chamada para [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) para criar uma exibição do arquivo no espaço de endereço do processo. A função **MapViewOfFile** retorna um ponteiro para a exibição de arquivo, `pBuf` . Em seguida, o processo usa a função [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) para gravar uma cadeia de caracteres na exibição que pode ser acessada por outros processos.

A prefixação dos nomes de objeto de mapeamento de arquivo com "global \\ " permite que os processos se comuniquem entre si mesmo se estiverem em sessões do Terminal Server diferentes. Isso requer que o primeiro processo tenha o privilégio [**SeCreateGlobalPrivilege**](../secauthz/privilege-constants.md) .

Quando o processo não precisar mais de acesso ao objeto de mapeamento de arquivo, ele deverá chamar a função [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) . Quando todos os identificadores são fechados, o sistema pode liberar a seção do arquivo de paginação que o objeto usa.


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



## <a name="second-process"></a>Segundo processo

Um segundo processo pode acessar a cadeia de caracteres gravada na memória compartilhada pelo primeiro processo chamando a função [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) especificando o mesmo nome para o objeto de mapeamento como o primeiro processo. Em seguida, ele pode usar a função [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) para obter um ponteiro para a exibição de arquivo, `pBuf` . O processo pode exibir essa cadeia de caracteres como faria com qualquer outra cadeia de caracteres. Neste exemplo, a caixa de mensagem exibida contém a mensagem "mensagem do primeiro processo", que foi gravada pelo primeiro processo.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Compartilhando arquivos e memória](sharing-files-and-memory.md)
</dt> </dl>

 

 
