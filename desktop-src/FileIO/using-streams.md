---
description: Código de exemplo que mostra como usar fluxos básicos do sistema de arquivos NTFS.
ms.assetid: 9cd5f418-404c-40f5-aa51-ef4d2a5f238e
title: usando Fluxos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23ebb6e2297c82e8643eb79ce66991b32fdf27e46fc723113a2866c79b2f8377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078386"
---
# <a name="using-streams"></a>usando Fluxos

O exemplo neste tópico demonstra como usar fluxos básicos do sistema de arquivos NTFS.

Este exemplo cria um arquivo, chamado "Testfile", com um tamanho de 16 bytes. No entanto, o arquivo também tem um tipo de fluxo adicional:: $DATA, chamado "Stream", que adiciona mais 23 bytes que não são relatados pelo sistema operacional. Portanto, ao exibir a propriedade tamanho do arquivo para o arquivo, você verá apenas o tamanho do fluxo padrão:: $DATA para o arquivo.


```C++
#include <windows.h>
#include <stdio.h>

void main( )
 {
  HANDLE hFile, hStream;
  DWORD dwRet;

  hFile = CreateFile( TEXT("TestFile"), // Filename
                      GENERIC_WRITE,    // Desired access
                      FILE_SHARE_WRITE, // Share flags
                      NULL,             // Security Attributes
                      OPEN_ALWAYS,      // Creation Disposition
                      0,                // Flags and Attributes
                      NULL );           // OVERLAPPED pointer
  if( hFile == INVALID_HANDLE_VALUE )
   {
    printf( "Cannot open TestFile\n" );
    return;
   }
  else
   {
    WriteFile( hFile,              // Handle
               "This is TestFile", // Data to be written
               16,                 // Size of data, in bytes
               &dwRet,             // Number of bytes written
               NULL );             // OVERLAPPED pointer
    CloseHandle( hFile );
    hFile = INVALID_HANDLE_VALUE;
   }

  hStream = CreateFile( TEXT("TestFile:Stream"), // Filename
                        GENERIC_WRITE,           // Desired access
                        FILE_SHARE_WRITE,        // Share flags
                        NULL,                    // Security Attributes
                        OPEN_ALWAYS,             // Creation Disposition
                        0,                       // Flags and Attributes
                        NULL );                  // OVERLAPPED pointer
  if( hStream == INVALID_HANDLE_VALUE )
    printf( "Cannot open TestFile:Stream\n" );
  else
   {
    WriteFile( hStream,                   // Handle
               "This is TestFile:Stream", // Data to be written
               23,                        // Size of data
               &dwRet,                    // Number of bytes written
               NULL);                     // OVERLAPPED pointer
    CloseHandle( hStream );
    hStream = INVALID_HANDLE_VALUE;
   }
}
```



Se você digitar **Type Testfile** em um prompt de comando, ele exibirá a seguinte saída:

``` syntax
This is TestFile
```

No entanto, se você digitar o tipo de palavras **Testfile: Stream**, ele gerará o seguinte erro:

"A sintaxe de nome de arquivo, de diretório ou de rótulo de volume está incorreta".

Para exibir o que está em Testfile: Stream, use um dos seguintes comandos:

**Mais < Testfile: Stream**

**Mais < Testfile: Stream: $DATA**

O texto exibido é o seguinte:

``` syntax
This is TestFile:Stream
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fluxos de arquivo](file-streams.md)
</dt> </dl>

 

 



