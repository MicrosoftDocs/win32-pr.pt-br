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
# <a name="retrieving-and-changing-file-attributes"></a><span data-ttu-id="63f23-103">Recuperando e alterando atributos de arquivo</span><span class="sxs-lookup"><span data-stu-id="63f23-103">Retrieving and Changing File Attributes</span></span>

<span data-ttu-id="63f23-104">Um aplicativo pode recuperar os atributos do arquivo usando a função [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) ou [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) .</span><span class="sxs-lookup"><span data-stu-id="63f23-104">An application can retrieve the file attributes by using the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) or [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) function.</span></span> <span data-ttu-id="63f23-105">As funções [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) e [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) podem definir muitos dos atributos.</span><span class="sxs-lookup"><span data-stu-id="63f23-105">The [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) and [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) functions can set many of the attributes.</span></span> <span data-ttu-id="63f23-106">No entanto, os aplicativos não podem definir todos os atributos.</span><span class="sxs-lookup"><span data-stu-id="63f23-106">However, applications cannot set all attributes.</span></span>

<span data-ttu-id="63f23-107">O exemplo de código neste tópico usa a função [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) para copiar todos os arquivos de texto (. txt) no diretório atual para um novo diretório de arquivos somente leitura.</span><span class="sxs-lookup"><span data-stu-id="63f23-107">The code example in this topic uses the [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) function to copy all text files (.txt) in the current directory to a new directory of read-only files.</span></span> <span data-ttu-id="63f23-108">Os arquivos no novo diretório são alterados para somente leitura, se necessário.</span><span class="sxs-lookup"><span data-stu-id="63f23-108">Files in the new directory are changed to read only, if necessary.</span></span>

<span data-ttu-id="63f23-109">O aplicativo cria o diretório especificado como um parâmetro usando a função [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) .</span><span class="sxs-lookup"><span data-stu-id="63f23-109">The application creates the directory specified as a parameter by using the [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) function.</span></span> <span data-ttu-id="63f23-110">O diretório já não deve existir.</span><span class="sxs-lookup"><span data-stu-id="63f23-110">The directory must not exist already.</span></span>

<span data-ttu-id="63f23-111">O aplicativo pesquisa o diretório atual em busca de todos os arquivos de texto usando as funções [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) e [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) .</span><span class="sxs-lookup"><span data-stu-id="63f23-111">The application searches the current directory for all text files by using the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) functions.</span></span> <span data-ttu-id="63f23-112">Cada arquivo de texto é copiado para o \\ diretório TextRO.</span><span class="sxs-lookup"><span data-stu-id="63f23-112">Each text file is copied to the \\TextRO directory.</span></span> <span data-ttu-id="63f23-113">Depois que um arquivo é copiado, a função [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) determina se um arquivo é somente leitura ou não.</span><span class="sxs-lookup"><span data-stu-id="63f23-113">After a file is copied, the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) function determines whether or not a file is read only.</span></span> <span data-ttu-id="63f23-114">Se o arquivo não for somente leitura, o aplicativo alterará os diretórios para \\ TextRO e converterá o arquivo copiado para somente leitura usando a função [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) .</span><span class="sxs-lookup"><span data-stu-id="63f23-114">If the file is not read only, the application changes directories to \\TextRO and converts the copied file to read only by using the [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) function.</span></span>

<span data-ttu-id="63f23-115">Depois que todos os arquivos de texto no diretório atual são copiados, o aplicativo fecha o identificador de pesquisa usando a função [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .</span><span class="sxs-lookup"><span data-stu-id="63f23-115">After all text files in the current directory are copied, the application closes the search handle by using the [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) function.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="63f23-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="63f23-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63f23-117">**Constantes de atributo de arquivo**</span><span class="sxs-lookup"><span data-stu-id="63f23-117">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> <dt>

[<span data-ttu-id="63f23-118">Nomes de arquivo, caminhos e namespaces</span><span class="sxs-lookup"><span data-stu-id="63f23-118">File Names, Paths, and Namespaces</span></span>](naming-a-file.md)
</dt> </dl>

 

 



