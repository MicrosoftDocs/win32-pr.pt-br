---
title: Tirar um instantâneo e exibir processos
description: O aplicativo de console simples a seguir obtém uma lista de processos em execução.
ms.assetid: 318d166f-858f-4f33-9422-977e0c4beb3f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdf74ec3d0d0d47e91b385598b06a672ee17e63681f2c82305474db06993ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603789"
---
# <a name="taking-a-snapshot-and-viewing-processes"></a>Tirar um instantâneo e exibir processos

O aplicativo de console simples a seguir obtém uma lista de processos em execução. Primeiro, a função tira um instantâneo dos processos atualmente em execução no sistema usando `GetProcessList` [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)e, em seguida, percorre a lista registrada no instantâneo usando [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) e [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next). Para cada processo, por sua vez, chama a função descrita em Atravessando a lista de módulos e a função descrita em Atravessando a `GetProcessList` `ListProcessModules` lista de [](traversing-the-module-list.md) `ListProcessThreads` [threads](traversing-the-thread-list.md).

Uma função de relatório de erros simples, , exibe o motivo das falhas, que `printError` geralmente resultam de restrições de segurança. Por exemplo, [**o OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) falha nos processos Ocioso e CSRSS porque suas restrições de acesso impedem que o código no nível do usuário os abra.


```C++
#include <windows.h>
#include <tlhelp32.h>
#include <tchar.h>

//  Forward declarations:
BOOL GetProcessList( );
BOOL ListProcessModules( DWORD dwPID );
BOOL ListProcessThreads( DWORD dwOwnerPID );
void printError( TCHAR* msg );

int main( void )
{
  GetProcessList( );
  return 0;
}

BOOL GetProcessList( )
{
  HANDLE hProcessSnap;
  HANDLE hProcess;
  PROCESSENTRY32 pe32;
  DWORD dwPriorityClass;

  // Take a snapshot of all processes in the system.
  hProcessSnap = CreateToolhelp32Snapshot( TH32CS_SNAPPROCESS, 0 );
  if( hProcessSnap == INVALID_HANDLE_VALUE )
  {
    printError( TEXT("CreateToolhelp32Snapshot (of processes)") );
    return( FALSE );
  }

  // Set the size of the structure before using it.
  pe32.dwSize = sizeof( PROCESSENTRY32 );

  // Retrieve information about the first process,
  // and exit if unsuccessful
  if( !Process32First( hProcessSnap, &pe32 ) )
  {
    printError( TEXT("Process32First") ); // show cause of failure
    CloseHandle( hProcessSnap );          // clean the snapshot object
    return( FALSE );
  }

  // Now walk the snapshot of processes, and
  // display information about each process in turn
  do
  {
    _tprintf( TEXT("\n\n=====================================================" ));
    _tprintf( TEXT("\nPROCESS NAME:  %s"), pe32.szExeFile );
    _tprintf( TEXT("\n-------------------------------------------------------" ));

    // Retrieve the priority class.
    dwPriorityClass = 0;
    hProcess = OpenProcess( PROCESS_ALL_ACCESS, FALSE, pe32.th32ProcessID );
    if( hProcess == NULL )
      printError( TEXT("OpenProcess") );
    else
    {
      dwPriorityClass = GetPriorityClass( hProcess );
      if( !dwPriorityClass )
        printError( TEXT("GetPriorityClass") );
      CloseHandle( hProcess );
    }

    _tprintf( TEXT("\n  Process ID        = 0x%08X"), pe32.th32ProcessID );
    _tprintf( TEXT("\n  Thread count      = %d"),   pe32.cntThreads );
    _tprintf( TEXT("\n  Parent process ID = 0x%08X"), pe32.th32ParentProcessID );
    _tprintf( TEXT("\n  Priority base     = %d"), pe32.pcPriClassBase );
    if( dwPriorityClass )
      _tprintf( TEXT("\n  Priority class    = %d"), dwPriorityClass );

    // List the modules and threads associated with this process
    ListProcessModules( pe32.th32ProcessID );
    ListProcessThreads( pe32.th32ProcessID );

  } while( Process32Next( hProcessSnap, &pe32 ) );

  CloseHandle( hProcessSnap );
  return( TRUE );
}


BOOL ListProcessModules( DWORD dwPID )
{
  HANDLE hModuleSnap = INVALID_HANDLE_VALUE;
  MODULEENTRY32 me32;

  // Take a snapshot of all modules in the specified process.
  hModuleSnap = CreateToolhelp32Snapshot( TH32CS_SNAPMODULE, dwPID );
  if( hModuleSnap == INVALID_HANDLE_VALUE )
  {
    printError( TEXT("CreateToolhelp32Snapshot (of modules)") );
    return( FALSE );
  }

  // Set the size of the structure before using it.
  me32.dwSize = sizeof( MODULEENTRY32 );

  // Retrieve information about the first module,
  // and exit if unsuccessful
  if( !Module32First( hModuleSnap, &me32 ) )
  {
    printError( TEXT("Module32First") );  // show cause of failure
    CloseHandle( hModuleSnap );           // clean the snapshot object
    return( FALSE );
  }

  // Now walk the module list of the process,
  // and display information about each module
  do
  {
    _tprintf( TEXT("\n\n     MODULE NAME:     %s"),   me32.szModule );
    _tprintf( TEXT("\n     Executable     = %s"),     me32.szExePath );
    _tprintf( TEXT("\n     Process ID     = 0x%08X"),         me32.th32ProcessID );
    _tprintf( TEXT("\n     Ref count (g)  = 0x%04X"),     me32.GlblcntUsage );
    _tprintf( TEXT("\n     Ref count (p)  = 0x%04X"),     me32.ProccntUsage );
    _tprintf( TEXT("\n     Base address   = 0x%08X"), (DWORD) me32.modBaseAddr );
    _tprintf( TEXT("\n     Base size      = %d"),             me32.modBaseSize );

  } while( Module32Next( hModuleSnap, &me32 ) );

  CloseHandle( hModuleSnap );
  return( TRUE );
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
  te32.dwSize = sizeof(THREADENTRY32); 
 
  // Retrieve information about the first thread,
  // and exit if unsuccessful
  if( !Thread32First( hThreadSnap, &te32 ) ) 
  {
    printError( TEXT("Thread32First") ); // show cause of failure
    CloseHandle( hThreadSnap );          // clean the snapshot object
    return( FALSE );
  }

  // Now walk the thread list of the system,
  // and display information about each thread
  // associated with the specified process
  do 
  { 
    if( te32.th32OwnerProcessID == dwOwnerPID )
    {
      _tprintf( TEXT("\n\n     THREAD ID      = 0x%08X"), te32.th32ThreadID ); 
      _tprintf( TEXT("\n     Base priority  = %d"), te32.tpBasePri ); 
      _tprintf( TEXT("\n     Delta priority = %d"), te32.tpDeltaPri ); 
      _tprintf( TEXT("\n"));
    }
  } while( Thread32Next(hThreadSnap, &te32 ) ); 

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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instantâneos do sistema](snapshots-of-the-system.md)
</dt> </dl>

 

 