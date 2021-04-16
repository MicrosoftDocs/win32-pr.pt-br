---
description: Cada processo tem um bloco de ambiente associado a ele.
ms.assetid: b428688c-7b16-48c7-8d89-55d066496d1c
title: Alterando variáveis de ambiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e13054afff996c4f8128fdc58f9d6dfadc35cc84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779590"
---
# <a name="changing-environment-variables"></a><span data-ttu-id="c2227-103">Alterando variáveis de ambiente</span><span class="sxs-lookup"><span data-stu-id="c2227-103">Changing Environment Variables</span></span>

<span data-ttu-id="c2227-104">Cada processo tem um bloco de ambiente associado a ele.</span><span class="sxs-lookup"><span data-stu-id="c2227-104">Each process has an environment block associated with it.</span></span> <span data-ttu-id="c2227-105">O bloco de ambiente consiste em um bloco terminado em nulo de cadeias de caracteres terminadas em nulo (o que significa que há dois bytes nulos no final do bloco), onde cada cadeia de caracteres está no formato:</span><span class="sxs-lookup"><span data-stu-id="c2227-105">The environment block consists of a null-terminated block of null-terminated strings (meaning there are two null bytes at the end of the block), where each string is in the form:</span></span>

<span data-ttu-id="c2227-106">*nome* = do *valor* do</span><span class="sxs-lookup"><span data-stu-id="c2227-106">*name*=*value*</span></span>

<span data-ttu-id="c2227-107">Todas as cadeias de caracteres no bloco de ambiente devem ser classificadas alfabeticamente por nome.</span><span class="sxs-lookup"><span data-stu-id="c2227-107">All strings in the environment block must be sorted alphabetically by name.</span></span> <span data-ttu-id="c2227-108">A classificação não diferencia maiúsculas de minúsculas, ordem Unicode, sem considerar a localidade.</span><span class="sxs-lookup"><span data-stu-id="c2227-108">The sort is case-insensitive, Unicode order, without regard to locale.</span></span> <span data-ttu-id="c2227-109">Como o sinal de igual é um separador, ele não deve ser usado no nome de uma variável de ambiente.</span><span class="sxs-lookup"><span data-stu-id="c2227-109">Because the equal sign is a separator, it must not be used in the name of an environment variable.</span></span>

## <a name="example-1"></a><span data-ttu-id="c2227-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c2227-110">Example 1</span></span>

<span data-ttu-id="c2227-111">Por padrão, um processo filho herda uma cópia do bloco de ambiente do processo pai.</span><span class="sxs-lookup"><span data-stu-id="c2227-111">By default, a child process inherits a copy of the environment block of the parent process.</span></span> <span data-ttu-id="c2227-112">O exemplo a seguir demonstra como criar um novo bloco de ambiente para passar para um processo filho usando [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="c2227-112">The following example demonstrates how to create a new environment block to pass to a child process using [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span>

<span data-ttu-id="c2227-113">Este exemplo usa o código no exemplo três como o processo filho, Ex3.exe.</span><span class="sxs-lookup"><span data-stu-id="c2227-113">This example uses the code in example three as the child process, Ex3.exe.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

#define BUFSIZE 4096

int _tmain()
{
    TCHAR chNewEnv[BUFSIZE];
    LPTSTR lpszCurrentVariable; 
    DWORD dwFlags=0;
    TCHAR szAppName[]=TEXT("ex3.exe");
    STARTUPINFO si;
    PROCESS_INFORMATION pi;
    BOOL fSuccess; 
 
    // Copy environment strings into an environment block. 
 
    lpszCurrentVariable = (LPTSTR) chNewEnv;
    if (FAILED(StringCchCopy(lpszCurrentVariable, BUFSIZE, TEXT("MySetting=A"))))
    {
        printf("String copy failed\n"); 
        return FALSE;
    }

    lpszCurrentVariable += lstrlen(lpszCurrentVariable) + 1; 
    if (FAILED(StringCchCopy(lpszCurrentVariable, BUFSIZE, TEXT("MyVersion=2")))) 
    {
        printf("String copy failed\n"); 
        return FALSE;
    }
 
    // Terminate the block with a NULL byte. 
 
    lpszCurrentVariable += lstrlen(lpszCurrentVariable) + 1; 
    *lpszCurrentVariable = (TCHAR)0; 

    // Create the child process, specifying a new environment block. 
 
    SecureZeroMemory(&si, sizeof(STARTUPINFO));
    si.cb = sizeof(STARTUPINFO);

#ifdef UNICODE
    dwFlags = CREATE_UNICODE_ENVIRONMENT;
#endif

    fSuccess = CreateProcess(szAppName, NULL, NULL, NULL, TRUE, dwFlags,
        (LPVOID) chNewEnv,   // new environment block
        NULL, &si, &pi); 
 
    if (! fSuccess) 
    {
        printf("CreateProcess failed (%d)\n", GetLastError());
        return FALSE;
    }
    WaitForSingleObject(pi.hProcess, INFINITE);
    return TRUE;
}
```



## <a name="example-2"></a><span data-ttu-id="c2227-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c2227-114">Example 2</span></span>

<span data-ttu-id="c2227-115">Alterar as variáveis de ambiente de um processo filho durante a criação do processo é a única maneira como um processo pode alterar diretamente as variáveis de ambiente de outro processo.</span><span class="sxs-lookup"><span data-stu-id="c2227-115">Altering the environment variables of a child process during process creation is the only way one process can directly change the environment variables of another process.</span></span> <span data-ttu-id="c2227-116">Um processo nunca pode alterar diretamente as variáveis de ambiente de outro processo que não seja um filho desse processo.</span><span class="sxs-lookup"><span data-stu-id="c2227-116">A process can never directly change the environment variables of another process that is not a child of that process.</span></span>

<span data-ttu-id="c2227-117">Se você quiser que o processo filho herde a maior parte do ambiente pai com apenas algumas alterações, recupere os valores atuais usando [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable), salve esses valores, crie um bloco atualizado para que o processo filho herde, crie o processo filho e, em seguida, restaure os valores salvos usando [**SetEnvironmentVariable não**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable), conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="c2227-117">If you want the child process to inherit most of the parent's environment with only a few changes, retrieve the current values using [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable), save these values, create an updated block for the child process to inherit, create the child process, and then restore the saved values using [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable), as shown in the following example.</span></span>

<span data-ttu-id="c2227-118">Este exemplo usa o código no exemplo três como o processo filho, Ex3.exe.</span><span class="sxs-lookup"><span data-stu-id="c2227-118">This example uses the code in example three as the child process, Ex3.exe.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUFSIZE 4096
#define VARNAME TEXT("MyVariable")

int _tmain()
{
    DWORD dwRet, dwErr;
    LPTSTR pszOldVal; 
    TCHAR szAppName[]=TEXT("ex3.exe");
    DWORD dwFlags=0;
    STARTUPINFO si;
    PROCESS_INFORMATION pi;
    BOOL fExist, fSuccess; 
 
    // Retrieves the current value of the variable if it exists.
    // Sets the variable to a new value, creates a child process,
    // then uses SetEnvironmentVariable to restore the original
    // value or delete it if it did not exist previously. 
 
    pszOldVal = (LPTSTR) malloc(BUFSIZE*sizeof(TCHAR));
    if(NULL == pszOldVal)
    {
        printf("Out of memory\n");
        return FALSE;
    }

    dwRet = GetEnvironmentVariable(VARNAME, pszOldVal, BUFSIZE);

    if(0 == dwRet)
    {
        dwErr = GetLastError();
        if( ERROR_ENVVAR_NOT_FOUND == dwErr )
        {
            printf("Environment variable does not exist.\n");
            fExist=FALSE;
        }
    }
    else if(BUFSIZE < dwRet)
    {
        pszOldVal = (LPTSTR) realloc(pszOldVal, dwRet*sizeof(TCHAR));   
        if(NULL == pszOldVal)
        {
            printf("Out of memory\n");
            return FALSE;
        }
        dwRet = GetEnvironmentVariable(VARNAME, pszOldVal, dwRet);
        if(!dwRet)
        {
            printf("GetEnvironmentVariable failed (%d)\n", GetLastError());
            return FALSE;
        }
        else fExist=TRUE;
    }
    else fExist=TRUE;

    // Set a value for the child process to inherit. 
 
    if (! SetEnvironmentVariable(VARNAME, TEXT("Test"))) 
    {
        printf("SetEnvironmentVariable failed (%d)\n", GetLastError()); 
        return FALSE;
    }
 
    // Create a child process. 

    SecureZeroMemory(&si, sizeof(STARTUPINFO));
    si.cb = sizeof(STARTUPINFO);
 
#ifdef UNICODE
    dwFlags = CREATE_UNICODE_ENVIRONMENT;
#endif

    fSuccess = CreateProcess(szAppName, NULL, NULL, NULL, TRUE, dwFlags, 
        NULL,     // inherit parent's environment 
        NULL, &si, &pi); 
    if (! fSuccess) 
    {
        printf("CreateProcess failed (%d)\n", GetLastError()); 
    }
    WaitForSingleObject(pi.hProcess, INFINITE);

    // Restore the original environment variable. 
 
    if(fExist)
    {
        if (! SetEnvironmentVariable(VARNAME, pszOldVal)) 
        {
            printf("SetEnvironmentVariable failed (%d)\n", GetLastError()); 
            return FALSE;
        }
    }
    else SetEnvironmentVariable(VARNAME, NULL);

    free(pszOldVal);
    
    return fSuccess;
}
```



## <a name="example-3"></a><span data-ttu-id="c2227-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c2227-119">Example 3</span></span>

<span data-ttu-id="c2227-120">O exemplo a seguir recupera o bloco de ambiente do processo usando [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) e imprime o conteúdo no console.</span><span class="sxs-lookup"><span data-stu-id="c2227-120">The following example retrieves the process's environment block using [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) and prints the contents to the console.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

int _tmain()
{
    LPTSTR lpszVariable; 
    LPTCH lpvEnv; 
 
    // Get a pointer to the environment block. 
 
    lpvEnv = GetEnvironmentStrings();

    // If the returned pointer is NULL, exit.
    if (lpvEnv == NULL)
    {
        printf("GetEnvironmentStrings failed (%d)\n", GetLastError()); 
        return 0;
    }
 
    // Variable strings are separated by NULL byte, and the block is 
    // terminated by a NULL byte. 

    lpszVariable = (LPTSTR) lpvEnv;

    while (*lpszVariable)
    {
        _tprintf(TEXT("%s\n"), lpszVariable);
        lpszVariable += lstrlen(lpszVariable) + 1;
    }
    FreeEnvironmentStrings(lpvEnv);
    return 1;
}
```



 

 
