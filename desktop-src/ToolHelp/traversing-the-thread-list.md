---
title: Atravessando a lista de threads
description: A função de exemplo a seguir lista os threads em execução para um processo especificado.
ms.assetid: 67194627-8239-46d2-93e7-eb8e5f6c56e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 300b162af296b0c556cce3d3d62e59bd4278b1d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636721"
---
# <a name="traversing-the-thread-list"></a><span data-ttu-id="3e230-103">Atravessando a lista de threads</span><span class="sxs-lookup"><span data-stu-id="3e230-103">Traversing the Thread List</span></span>

<span data-ttu-id="3e230-104">A função de exemplo a seguir lista os threads em execução para um processo especificado.</span><span class="sxs-lookup"><span data-stu-id="3e230-104">The following example function lists running threads for a specified process.</span></span> <span data-ttu-id="3e230-105">Primeiro, a `ListProcessThreads` função tira um instantâneo dos threads atualmente em execução no sistema usando [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)e, em seguida, percorre a lista registrada no instantâneo usando as funções [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) e [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) .</span><span class="sxs-lookup"><span data-stu-id="3e230-105">First, the `ListProcessThreads` function takes a snapshot of the currently executing threads in the system using [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot), and then it walks through the list recorded in the snapshot using the [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) and [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) functions.</span></span> <span data-ttu-id="3e230-106">O parâmetro para `ListProcessThreads` é o identificador do processo do processo cujos threads devem ser listados.</span><span class="sxs-lookup"><span data-stu-id="3e230-106">The parameter for `ListProcessThreads` is the process identifier of the process whose threads are to be listed.</span></span>


```C++
#include <windows.h>
#include <tlhelp32.h>
#include <tchar.h>

//  Forward declarations:
BOOL ListProcessThreads( DWORD dwOwnerPID );
void printError( TCHAR* msg );

int main( void )
{
  ListProcessThreads(GetCurrentProcessId() );
  return 0;
}

BOOL ListProcessThreads( DWORD dwOwnerPID ) 
{ 
  HANDLE hThreadSnap = INVALID_HANDLE_VALUE; 
  THREADENTRY32 te32; 
 
  // Take a snapshot of all running threads  
  hThreadSnap = CreateToolhelp32Snapshot( TH32CS_SNAPTHREAD, 0 ); 
  if( hThreadSnap == INVALID_HANDLE_VALUE ) 
    return( FALSE ); 
 
  // Fill in the size of the structure before using it. 
  te32.dwSize = sizeof(THREADENTRY32 ); 
 
  // Retrieve information about the first thread,
  // and exit if unsuccessful
  if( !Thread32First( hThreadSnap, &te32 ) ) 
  {
    printError( TEXT("Thread32First") );  // Show cause of failure
    CloseHandle( hThreadSnap );     // Must clean up the snapshot object!
    return( FALSE );
  }

  // Now walk the thread list of the system,
  // and display information about each thread
  // associated with the specified process
  do 
  { 
    if( te32.th32OwnerProcessID == dwOwnerPID )
    {
      _tprintf( TEXT("\n     THREAD ID      = 0x%08X"), te32.th32ThreadID ); 
      _tprintf( TEXT("\n     base priority  = %d"), te32.tpBasePri ); 
      _tprintf( TEXT("\n     delta priority = %d"), te32.tpDeltaPri ); 
    }
  } while( Thread32Next(hThreadSnap, &te32 ) );

  _tprintf( TEXT("\n"));

//  Don't forget to clean up the snapshot object.
  CloseHandle( hThreadSnap );
  return( TRUE );
}

void printError( TCHAR* msg )
{
  DWORD eNum;
  TCHAR sysMsg[256];
  TCHAR* p;

  eNum = GetLastError( );
  FormatMessage( FORMAT_MESSAGE_FROM_SYSTEM | FORMAT_MESSAGE_IGNORE_INSERTS,
         NULL, eNum,
         MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), // Default language
         sysMsg, 256, NULL );

  // Trim the end of the line and terminate it with a null
  p = sysMsg;
  while( ( *p > 31 ) || ( *p == 9 ) )
    ++p;
  do { *p-- = 0; } while( ( p >= sysMsg ) &&
                          ( ( *p == '.' ) || ( *p < 33 ) ) );

  // Display the message
  _tprintf( TEXT("\n  WARNING: %s failed with error %d (%s)"), msg, eNum, sysMsg );
}
```



## <a name="related-topics"></a><span data-ttu-id="3e230-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e230-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e230-108">Movimentação de thread</span><span class="sxs-lookup"><span data-stu-id="3e230-108">Thread Walking</span></span>](thread-walking.md)
</dt> </dl>

 

 




