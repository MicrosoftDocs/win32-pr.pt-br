---
description: Código de exemplo que mostra como criar um arquivo temporário para fins de manipulação de dados usando as funções GetTempFileName e GetTempPath.
ms.assetid: 6254c67d-5d34-499d-b1a4-8cac526dd294
title: Criando e usando um arquivo temporário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca18b7b72aab7c53bea95c38147af66f2b7fef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812960"
---
# <a name="creating-and-using-a-temporary-file"></a><span data-ttu-id="e1543-103">Criando e usando um arquivo temporário</span><span class="sxs-lookup"><span data-stu-id="e1543-103">Creating and Using a Temporary File</span></span>

<span data-ttu-id="e1543-104">Os aplicativos podem obter nomes de arquivo e caminho exclusivos para arquivos temporários usando as funções [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) e [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) .</span><span class="sxs-lookup"><span data-stu-id="e1543-104">Applications can obtain unique file and path names for temporary files by using the [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) and [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) functions.</span></span> <span data-ttu-id="e1543-105">A função **GetTempFileName** gera um nome de arquivo exclusivo e a função **GetTempPath** recupera o caminho para um diretório em que os arquivos temporários devem ser criados.</span><span class="sxs-lookup"><span data-stu-id="e1543-105">The **GetTempFileName** function generates a unique file name, and the **GetTempPath** function retrieves the path to a directory where temporary files should be created.</span></span>

<span data-ttu-id="e1543-106">O procedimento a seguir descreve como um aplicativo cria um arquivo temporário para fins de manipulação de dados.</span><span class="sxs-lookup"><span data-stu-id="e1543-106">The following procedure describes how an application creates a temporary file for data manipulation purposes.</span></span>

<span data-ttu-id="e1543-107">**Para criar e usar um arquivo temporário**</span><span class="sxs-lookup"><span data-stu-id="e1543-107">**To create and use a temporary file**</span></span>

1.  <span data-ttu-id="e1543-108">O aplicativo abre o arquivo de texto de origem fornecido pelo usuário usando [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).</span><span class="sxs-lookup"><span data-stu-id="e1543-108">The application opens the user-provided source text file by using [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).</span></span>
2.  <span data-ttu-id="e1543-109">O aplicativo recupera um caminho de arquivo temporário e um nome de arquivo usando as funções [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) e [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) e, em seguida, usa [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para criar o arquivo temporário.</span><span class="sxs-lookup"><span data-stu-id="e1543-109">The application retrieves a temporary file path and file name by using the [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) and [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) functions, and then uses [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) to create the temporary file.</span></span>
3.  <span data-ttu-id="e1543-110">O aplicativo lê blocos de dados de texto em um buffer, converte o conteúdo do buffer em maiúsculas usando a função [CharUpperBuffA](/windows/win32/api/winuser/nf-winuser-charupperbuffa) e grava o buffer convertido no arquivo temporário.</span><span class="sxs-lookup"><span data-stu-id="e1543-110">The application reads blocks of text data into a buffer, converts the buffer contents to uppercase using the [CharUpperBuffA](/windows/win32/api/winuser/nf-winuser-charupperbuffa) function, and writes the converted buffer to the temporary file.</span></span>
4.  <span data-ttu-id="e1543-111">Quando todo o arquivo de origem é gravado no arquivo temporário, o aplicativo fecha os dois arquivos e renomeia o arquivo temporário para "allcaps.txt" usando a função [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) .</span><span class="sxs-lookup"><span data-stu-id="e1543-111">When all of the source file is written to the temporary file, the application closes both files, and renames the temporary file to "allcaps.txt" by using the [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) function.</span></span>

<span data-ttu-id="e1543-112">Cada uma das etapas anteriores é verificada em busca de sucesso antes de passar para a próxima etapa, e uma descrição de falha será exibida se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="e1543-112">Each of the previous steps is checked for success before moving to the next step, and a failure description is displayed if an error occurs.</span></span> <span data-ttu-id="e1543-113">O aplicativo será encerrado imediatamente após a exibição da mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="e1543-113">The application will terminate immediately after displaying the error message.</span></span>

<span data-ttu-id="e1543-114">Observe que a manipulação do arquivo de texto foi escolhida apenas para facilitar a demonstração e pode ser substituída por qualquer procedimento de manipulação de dados desejado.</span><span class="sxs-lookup"><span data-stu-id="e1543-114">Note that text file manipulation was chosen for ease of demonstration only and can be replaced with any desired data manipulation procedure required.</span></span> <span data-ttu-id="e1543-115">O arquivo de dados pode ser de qualquer tipo de dados, não apenas texto.</span><span class="sxs-lookup"><span data-stu-id="e1543-115">The data file can be of any data type, not only text.</span></span>

<span data-ttu-id="e1543-116">A função [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) recupera uma cadeia de caracteres de caminho totalmente qualificada de uma variável de ambiente, mas não verifica antecipadamente a existência do caminho ou dos direitos de acesso adequados a esse caminho, que é responsabilidade do desenvolvedor do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e1543-116">The [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) function retrieves a fully qualified path string from an environment variable but does not check in advance for the existence of the path or adequate access rights to that path, which is the responsibility of the application developer.</span></span> <span data-ttu-id="e1543-117">Para obter mais informações, consulte [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha).</span><span class="sxs-lookup"><span data-stu-id="e1543-117">For more information, see [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha).</span></span> <span data-ttu-id="e1543-118">No exemplo a seguir, um erro é considerado uma condição de terminal e o aplicativo é encerrado após o envio de uma mensagem descritiva para a saída padrão.</span><span class="sxs-lookup"><span data-stu-id="e1543-118">In the following example, an error is regarded as a terminal condition and the application exits after sending a descriptive message to standard output.</span></span> <span data-ttu-id="e1543-119">No entanto, existem muitas outras opções, como solicitar ao usuário um diretório temporário ou simplesmente tentar usar o diretório atual.</span><span class="sxs-lookup"><span data-stu-id="e1543-119">However, many other options exist, such as prompting the user for a temporary directory or simply attempting to use the current directory.</span></span>

> [!Note]  
> <span data-ttu-id="e1543-120">A função [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) não requer que a função [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) seja usada.</span><span class="sxs-lookup"><span data-stu-id="e1543-120">The [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) function does not require that the [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) function be used.</span></span>

 

<span data-ttu-id="e1543-121">O exemplo de C++ a seguir mostra como criar um arquivo temporário para fins de manipulação de dados.</span><span class="sxs-lookup"><span data-stu-id="e1543-121">The following C++ example shows how to create a temporary file for data manipulation purposes.</span></span>


```C++
//
//  This application opens a file specified by the user and uses
//  a temporary file to convert the file to upper case letters.
//  Note that the given source file is assumed to be an ASCII text file
//  and the new file created is overwritten each time the application is
//  run.
//

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUFSIZE 1024

void PrintError(LPCTSTR errDesc);

int _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile     = INVALID_HANDLE_VALUE;
    HANDLE hTempFile = INVALID_HANDLE_VALUE; 

    BOOL fSuccess  = FALSE;
    DWORD dwRetVal = 0;
    UINT uRetVal   = 0;

    DWORD dwBytesRead    = 0;
    DWORD dwBytesWritten = 0; 

    TCHAR szTempFileName[MAX_PATH];  
    TCHAR lpTempPathBuffer[MAX_PATH];
    char  chBuffer[BUFSIZE]; 

    LPCTSTR errMsg;

    if(argc != 2)
    {
        _tprintf(TEXT("Usage: %s <file>\n"), argv[0]);
        return -1;
    }

    //  Opens the existing file. 
    hFile = CreateFile(argv[1],               // file name 
                       GENERIC_READ,          // open for reading 
                       0,                     // do not share 
                       NULL,                  // default security 
                       OPEN_EXISTING,         // existing file only 
                       FILE_ATTRIBUTE_NORMAL, // normal file 
                       NULL);                 // no template 
    if (hFile == INVALID_HANDLE_VALUE) 
    { 
        PrintError(TEXT("First CreateFile failed"));
        return (1);
    } 

     //  Gets the temp path env string (no guarantee it's a valid path).
    dwRetVal = GetTempPath(MAX_PATH,          // length of the buffer
                           lpTempPathBuffer); // buffer for path 
    if (dwRetVal > MAX_PATH || (dwRetVal == 0))
    {
        PrintError(TEXT("GetTempPath failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (2);
    }

    //  Generates a temporary file name. 
    uRetVal = GetTempFileName(lpTempPathBuffer, // directory for tmp files
                              TEXT("DEMO"),     // temp file name prefix 
                              0,                // create unique name 
                              szTempFileName);  // buffer for name 
    if (uRetVal == 0)
    {
        PrintError(TEXT("GetTempFileName failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (3);
    }

    //  Creates the new file to write to for the upper-case version.
    hTempFile = CreateFile((LPTSTR) szTempFileName, // file name 
                           GENERIC_WRITE,        // open for write 
                           0,                    // do not share 
                           NULL,                 // default security 
                           CREATE_ALWAYS,        // overwrite existing
                           FILE_ATTRIBUTE_NORMAL,// normal file 
                           NULL);                // no template 
    if (hTempFile == INVALID_HANDLE_VALUE) 
    { 
        PrintError(TEXT("Second CreateFile failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (4);
    } 

    //  Reads BUFSIZE blocks to the buffer and converts all characters in 
    //  the buffer to upper case, then writes the buffer to the temporary 
    //  file. 
    do 
    {
        if (ReadFile(hFile, chBuffer, BUFSIZE, &dwBytesRead, NULL)) 
        {
            //  Replaces lower case letters with upper case
            //  in place (using the same buffer). The return
            //  value is the number of replacements performed,
            //  which we aren't interested in for this demo.
            CharUpperBuffA(chBuffer, dwBytesRead); 

            fSuccess = WriteFile(hTempFile, 
                                 chBuffer, 
                                 dwBytesRead,
                                 &dwBytesWritten, 
                                 NULL); 
            if (!fSuccess) 
            {
                PrintError(TEXT("WriteFile failed"));
                return (5);
            }
        } 
        else
        {
            PrintError(TEXT("ReadFile failed"));
            return (6);
        }
    //  Continues until the whole file is processed.
    } while (dwBytesRead == BUFSIZE); 

    //  The handles to the files are no longer needed, so
    //  they are closed prior to moving the new file.
    if (!CloseHandle(hFile)) 
    {
       PrintError(TEXT("CloseHandle(hFile) failed"));
       return (7);
    }
    
    if (!CloseHandle(hTempFile)) 
    {
       PrintError(TEXT("CloseHandle(hTempFile) failed"));
       return (8);
    }

    //  Moves the temporary file to the new text file, allowing for differnt
    //  drive letters or volume names.
    fSuccess = MoveFileEx(szTempFileName, 
                          TEXT("AllCaps.txt"), 
                          MOVEFILE_REPLACE_EXISTING | MOVEFILE_COPY_ALLOWED);
    if (!fSuccess)
    { 
        PrintError(TEXT("MoveFileEx failed"));
        return (9);
    }
    else 
        _tprintf(TEXT("All-caps version of %s written to AllCaps.txt\n"), argv[1]);
    return (0);
}

//  ErrorMessage support function.
//  Retrieves the system error message for the GetLastError() code.
//  Note: caller must use LocalFree() on the returned LPCTSTR buffer.
LPCTSTR ErrorMessage(DWORD error) 
{ 
    LPVOID lpMsgBuf;

    FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER 
                   | FORMAT_MESSAGE_FROM_SYSTEM 
                   | FORMAT_MESSAGE_IGNORE_INSERTS,
                  NULL,
                  error,
                  MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
                  (LPTSTR) &lpMsgBuf,
                  0,
                  NULL);

    return((LPCTSTR)lpMsgBuf);
}

//  PrintError support function.
//  Simple wrapper function for error output.
void PrintError(LPCTSTR errDesc)
{
        LPCTSTR errMsg = ErrorMessage(GetLastError());
        _tprintf(TEXT("\n** ERROR ** %s: %s\n"), errDesc, errMsg);
        LocalFree((LPVOID)errMsg);
}
```



 

 
