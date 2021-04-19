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
# <a name="creating-and-using-a-temporary-file"></a>Criando e usando um arquivo temporário

Os aplicativos podem obter nomes de arquivo e caminho exclusivos para arquivos temporários usando as funções [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) e [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) . A função **GetTempFileName** gera um nome de arquivo exclusivo e a função **GetTempPath** recupera o caminho para um diretório em que os arquivos temporários devem ser criados.

O procedimento a seguir descreve como um aplicativo cria um arquivo temporário para fins de manipulação de dados.

**Para criar e usar um arquivo temporário**

1.  O aplicativo abre o arquivo de texto de origem fornecido pelo usuário usando [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).
2.  O aplicativo recupera um caminho de arquivo temporário e um nome de arquivo usando as funções [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) e [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) e, em seguida, usa [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para criar o arquivo temporário.
3.  O aplicativo lê blocos de dados de texto em um buffer, converte o conteúdo do buffer em maiúsculas usando a função [CharUpperBuffA](/windows/win32/api/winuser/nf-winuser-charupperbuffa) e grava o buffer convertido no arquivo temporário.
4.  Quando todo o arquivo de origem é gravado no arquivo temporário, o aplicativo fecha os dois arquivos e renomeia o arquivo temporário para "allcaps.txt" usando a função [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) .

Cada uma das etapas anteriores é verificada em busca de sucesso antes de passar para a próxima etapa, e uma descrição de falha será exibida se ocorrer um erro. O aplicativo será encerrado imediatamente após a exibição da mensagem de erro.

Observe que a manipulação do arquivo de texto foi escolhida apenas para facilitar a demonstração e pode ser substituída por qualquer procedimento de manipulação de dados desejado. O arquivo de dados pode ser de qualquer tipo de dados, não apenas texto.

A função [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) recupera uma cadeia de caracteres de caminho totalmente qualificada de uma variável de ambiente, mas não verifica antecipadamente a existência do caminho ou dos direitos de acesso adequados a esse caminho, que é responsabilidade do desenvolvedor do aplicativo. Para obter mais informações, consulte [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha). No exemplo a seguir, um erro é considerado uma condição de terminal e o aplicativo é encerrado após o envio de uma mensagem descritiva para a saída padrão. No entanto, existem muitas outras opções, como solicitar ao usuário um diretório temporário ou simplesmente tentar usar o diretório atual.

> [!Note]  
> A função [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) não requer que a função [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) seja usada.

 

O exemplo de C++ a seguir mostra como criar um arquivo temporário para fins de manipulação de dados.


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



 

 
