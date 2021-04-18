---
description: Código de exemplo que mostra como usar a função GetFileAttributesEx para recuperar atributos de arquivo.
ms.assetid: f6eaea8a-0cc2-4fb6-bec5-7fb12b20c075
title: Recuperando e alterando atributos de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c980ddd6390f016b2057392f42f6bf645859307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767655"
---
# <a name="retrieving-and-changing-file-attributes"></a>Recuperando e alterando atributos de arquivo

Um aplicativo pode recuperar os atributos do arquivo usando a função [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) ou [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) . As funções [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) e [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) podem definir muitos dos atributos. No entanto, os aplicativos não podem definir todos os atributos.

O exemplo de código neste tópico usa a função [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) para copiar todos os arquivos de texto (. txt) no diretório atual para um novo diretório de arquivos somente leitura. Os arquivos no novo diretório são alterados para somente leitura, se necessário.

O aplicativo cria o diretório especificado como um parâmetro usando a função [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) . O diretório já não deve existir.

O aplicativo pesquisa o diretório atual em busca de todos os arquivos de texto usando as funções [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) e [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) . Cada arquivo de texto é copiado para o \\ diretório TextRO. Depois que um arquivo é copiado, a função [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) determina se um arquivo é somente leitura ou não. Se o arquivo não for somente leitura, o aplicativo alterará os diretórios para \\ TextRO e converterá o arquivo copiado para somente leitura usando a função [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) .

Depois que todos os arquivos de texto no diretório atual são copiados, o aplicativo fecha o identificador de pesquisa usando a função [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

void _tmain(int argc, TCHAR* argv[])
{
   WIN32_FIND_DATA FileData;
   HANDLE          hSearch;
   DWORD           dwAttrs;
   TCHAR           szNewPath[MAX_PATH];   
 
   BOOL            fFinished = FALSE; 

   if(argc != 2)
   {
      _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
      return;
   }
 
// Create a new directory. 
 
   if (!CreateDirectory(argv[1], NULL)) 
   { 
      printf("CreateDirectory failed (%d)\n", GetLastError()); 
      return;
   } 
 
// Start searching for text files in the current directory. 
 
   hSearch = FindFirstFile(TEXT("*.txt"), &FileData); 
   if (hSearch == INVALID_HANDLE_VALUE) 
   { 
      printf("No text files found.\n"); 
      return;
   } 
 
// Copy each .TXT file to the new directory 
// and change it to read only, if not already. 
 
   while (!fFinished) 
   { 
      StringCchPrintf(szNewPath, sizeof(szNewPath)/sizeof(szNewPath[0]), TEXT("%s\\%s"), argv[1], FileData.cFileName);

      if (CopyFile(FileData.cFileName, szNewPath, FALSE))
      { 
         dwAttrs = GetFileAttributes(FileData.cFileName); 
         if (dwAttrs==INVALID_FILE_ATTRIBUTES) return; 

         if (!(dwAttrs & FILE_ATTRIBUTE_READONLY)) 
         { 
            SetFileAttributes(szNewPath, 
                dwAttrs | FILE_ATTRIBUTE_READONLY); 
         } 
      } 
      else 
      { 
         printf("Could not copy file.\n"); 
         return;
      } 
 
      if (!FindNextFile(hSearch, &FileData)) 
      {
         if (GetLastError() == ERROR_NO_MORE_FILES) 
         { 
            _tprintf(TEXT("Copied *.txt to %s\n"), argv[1]); 
            fFinished = TRUE; 
         } 
         else 
         { 
            printf("Could not find next file.\n"); 
            return;
         } 
      }
   } 
 
// Close the search handle. 
 
   FindClose(hSearch);
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Constantes de atributo de arquivo**](file-attribute-constants.md)
</dt> <dt>

[Nomes de arquivo, caminhos e namespaces](naming-a-file.md)
</dt> </dl>

 

 



