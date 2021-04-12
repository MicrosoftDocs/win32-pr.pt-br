---
description: Código de exemplo que mostra como usar fluxos básicos do sistema de arquivos NTFS.
ms.assetid: 9cd5f418-404c-40f5-aa51-ef4d2a5f238e
title: Usando fluxos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04edc73a3524d45eeead4cd6c0d508925e6caa5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170856"
---
# <a name="using-streams"></a><span data-ttu-id="b65a0-103">Usando fluxos</span><span class="sxs-lookup"><span data-stu-id="b65a0-103">Using Streams</span></span>

<span data-ttu-id="b65a0-104">O exemplo neste tópico demonstra como usar fluxos básicos do sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="b65a0-104">The example in this topic demonstrates how to use basic NTFS file system streams.</span></span>

<span data-ttu-id="b65a0-105">Este exemplo cria um arquivo, chamado "Testfile", com um tamanho de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="b65a0-105">This example creates a file, called "TestFile," with a size of 16 bytes.</span></span> <span data-ttu-id="b65a0-106">No entanto, o arquivo também tem um tipo de fluxo adicional:: $DATA, chamado "Stream", que adiciona mais 23 bytes que não são relatados pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b65a0-106">However, the file also has an additional ::$DATA stream type, named "Stream" which adds an additional 23 bytes that is not reported by the operating system.</span></span> <span data-ttu-id="b65a0-107">Portanto, ao exibir a propriedade tamanho do arquivo para o arquivo, você verá apenas o tamanho do fluxo padrão:: $DATA para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="b65a0-107">Therefore, when you view the file size property for the file, you see only the size of default ::$DATA stream for the file.</span></span>


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



<span data-ttu-id="b65a0-108">Se você digitar **Type Testfile** em um prompt de comando, ele exibirá a seguinte saída:</span><span class="sxs-lookup"><span data-stu-id="b65a0-108">If you type **Type TestFile** at a command prompt, it displays the following output:</span></span>

``` syntax
This is TestFile
```

<span data-ttu-id="b65a0-109">No entanto, se você digitar o tipo de palavras **Testfile: Stream**, ele gerará o seguinte erro:</span><span class="sxs-lookup"><span data-stu-id="b65a0-109">However, if you type the words **Type TestFile:Stream**, it generates the following error:</span></span>

<span data-ttu-id="b65a0-110">"A sintaxe de nome de arquivo, de diretório ou de rótulo de volume está incorreta".</span><span class="sxs-lookup"><span data-stu-id="b65a0-110">"The filename, directory name, or volume label syntax is incorrect."</span></span>

<span data-ttu-id="b65a0-111">Para exibir o que está em Testfile: Stream, use um dos seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="b65a0-111">To view what is in TestFile:stream, use one of the following commands:</span></span>

<span data-ttu-id="b65a0-112">**Mais < Testfile: Stream**</span><span class="sxs-lookup"><span data-stu-id="b65a0-112">**More < TestFile:Stream**</span></span>

<span data-ttu-id="b65a0-113">**Mais < Testfile: Stream: $DATA**</span><span class="sxs-lookup"><span data-stu-id="b65a0-113">**More < TestFile:Stream:$DATA**</span></span>

<span data-ttu-id="b65a0-114">O texto exibido é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b65a0-114">The text displayed is as follows:</span></span>

``` syntax
This is TestFile:Stream
```

## <a name="related-topics"></a><span data-ttu-id="b65a0-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b65a0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b65a0-116">Fluxos de arquivos</span><span class="sxs-lookup"><span data-stu-id="b65a0-116">File Streams</span></span>](file-streams.md)
</dt> </dl>

 

 



