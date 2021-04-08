---
description: A função CreateProcess cria um novo processo, que é executado independentemente do processo de criação. No entanto, para simplificar, a relação é referida como uma relação pai-filho.
ms.assetid: 4c3f76a3-e9f5-4d73-b5ef-eabfa9d6e4d4
title: Criando processos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75606a3006bf63359b3e52cf2172b8bc2d77ed56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921711"
---
# <a name="creating-processes"></a><span data-ttu-id="fd08d-104">Criando processos</span><span class="sxs-lookup"><span data-stu-id="fd08d-104">Creating Processes</span></span>

<span data-ttu-id="fd08d-105">A função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) cria um novo processo, que é executado independentemente do processo de criação.</span><span class="sxs-lookup"><span data-stu-id="fd08d-105">The [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function creates a new process, which runs independently of the creating process.</span></span> <span data-ttu-id="fd08d-106">No entanto, para simplificar, a relação é referida como uma relação pai-filho.</span><span class="sxs-lookup"><span data-stu-id="fd08d-106">However, for simplicity, the relationship is referred to as a parent-child relationship.</span></span>

<span data-ttu-id="fd08d-107">O código a seguir demonstra como criar um processo.</span><span class="sxs-lookup"><span data-stu-id="fd08d-107">The following code demonstrates how to create a process.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

void _tmain( int argc, TCHAR *argv[] )
{
    STARTUPINFO si;
    PROCESS_INFORMATION pi;

    ZeroMemory( &si, sizeof(si) );
    si.cb = sizeof(si);
    ZeroMemory( &pi, sizeof(pi) );

    if( argc != 2 )
    {
        printf("Usage: %s [cmdline]\n", argv[0]);
        return;
    }

    // Start the child process. 
    if( !CreateProcess( NULL,   // No module name (use command line)
        argv[1],        // Command line
        NULL,           // Process handle not inheritable
        NULL,           // Thread handle not inheritable
        FALSE,          // Set handle inheritance to FALSE
        0,              // No creation flags
        NULL,           // Use parent's environment block
        NULL,           // Use parent's starting directory 
        &si,            // Pointer to STARTUPINFO structure
        &pi )           // Pointer to PROCESS_INFORMATION structure
    ) 
    {
        printf( "CreateProcess failed (%d).\n", GetLastError() );
        return;
    }

    // Wait until child process exits.
    WaitForSingleObject( pi.hProcess, INFINITE );

    // Close process and thread handles. 
    CloseHandle( pi.hProcess );
    CloseHandle( pi.hThread );
}
```



<span data-ttu-id="fd08d-108">Se [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) for bem sucedido, ele retornará uma estrutura de [**\_ informações do processo**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) que contém identificadores e identificadores para o novo processo e seu thread principal.</span><span class="sxs-lookup"><span data-stu-id="fd08d-108">If [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) succeeds, it returns a [**PROCESS\_INFORMATION**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) structure containing handles and identifiers for the new process and its primary thread.</span></span> <span data-ttu-id="fd08d-109">Os identificadores de thread e processo são criados com direitos de acesso completo, embora o acesso possa ser restringido se você especificar descritores de segurança.</span><span class="sxs-lookup"><span data-stu-id="fd08d-109">The thread and process handles are created with full access rights, although access can be restricted if you specify security descriptors.</span></span> <span data-ttu-id="fd08d-110">Quando você não precisar mais desses identificadores, feche-os usando a função [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="fd08d-110">When you no longer need these handles, close them by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="fd08d-111">Você também pode criar um processo usando a função [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) ou [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw) .</span><span class="sxs-lookup"><span data-stu-id="fd08d-111">You can also create a process using the [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw) function.</span></span> <span data-ttu-id="fd08d-112">Isso permite que você especifique o contexto de segurança da conta de usuário na qual o processo será executado.</span><span class="sxs-lookup"><span data-stu-id="fd08d-112">This allows you to specify the security context of the user account in which the process will execute.</span></span>

 

 
