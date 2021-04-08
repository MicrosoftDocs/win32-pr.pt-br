---
description: O depurador usa a função WaitForDebugEvent no início de seu loop principal.
ms.assetid: 5a45854e-2711-49d5-982b-6b85248ec632
title: Gravando o loop principal do depurador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f21c56364c314c676c5fd5dbb1cd6e9d1acd63e6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920351"
---
# <a name="writing-the-debuggers-main-loop"></a><span data-ttu-id="a43a2-103">Gravando o loop principal do depurador</span><span class="sxs-lookup"><span data-stu-id="a43a2-103">Writing the Debugger's Main Loop</span></span>

<span data-ttu-id="a43a2-104">O depurador usa a função [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent) no início de seu loop principal.</span><span class="sxs-lookup"><span data-stu-id="a43a2-104">The debugger uses the [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent) function at the beginning of its main loop.</span></span> <span data-ttu-id="a43a2-105">Essa função bloqueia o depurador até que ocorra um evento de depuração.</span><span class="sxs-lookup"><span data-stu-id="a43a2-105">This function blocks the debugger until a debugging event occurs.</span></span> <span data-ttu-id="a43a2-106">Quando ocorre o evento de depuração, o sistema suspende todos os threads no processo que está sendo depurado e notifica o depurador do evento.</span><span class="sxs-lookup"><span data-stu-id="a43a2-106">When the debugging event occurs, the system suspends all threads in the process being debugged and notifies the debugger of the event.</span></span>

<span data-ttu-id="a43a2-107">O depurador pode interagir com o usuário ou manipular o estado do processo que está sendo depurado, usando as funções [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext), [**GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-getthreadselectorentry), [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory), [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)e [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) .</span><span class="sxs-lookup"><span data-stu-id="a43a2-107">The debugger can interact with the user, or manipulate the state of the process being debugged, by using the [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext), [**GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-getthreadselectorentry), [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory), [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext), and [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) functions.</span></span> <span data-ttu-id="a43a2-108">**GetThreadSelectorEntry** retorna a entrada da tabela de descritores para um seletor e um thread especificados.</span><span class="sxs-lookup"><span data-stu-id="a43a2-108">**GetThreadSelectorEntry** returns the descriptor table entry for a specified selector and thread.</span></span> <span data-ttu-id="a43a2-109">Os depuradores usam a entrada da tabela de descritores para converter um endereço relativo ao segmento em um endereço virtual linear.</span><span class="sxs-lookup"><span data-stu-id="a43a2-109">Debuggers use the descriptor table entry to convert a segment-relative address to a linear virtual address.</span></span> <span data-ttu-id="a43a2-110">As funções **ReadProcessMemory** e **WriteProcessMemory** exigem endereços virtuais lineares.</span><span class="sxs-lookup"><span data-stu-id="a43a2-110">The **ReadProcessMemory** and **WriteProcessMemory** functions require linear virtual addresses.</span></span>

<span data-ttu-id="a43a2-111">Os depuradores frequentemente lêem a memória do processo que está sendo depurado e gravam a memória que contém instruções para o cache de instruções.</span><span class="sxs-lookup"><span data-stu-id="a43a2-111">Debuggers frequently read the memory of the process being debugged and write the memory that contains instructions to the instruction cache.</span></span> <span data-ttu-id="a43a2-112">Depois que as instruções são gravadas, o depurador chama a função [**FlushInstructionCache**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushinstructioncache) para executar as instruções armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="a43a2-112">After the instructions are written, the debugger calls the [**FlushInstructionCache**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushinstructioncache) function to execute the cached instructions.</span></span>

<span data-ttu-id="a43a2-113">O depurador usa a função [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent) no final de seu loop principal.</span><span class="sxs-lookup"><span data-stu-id="a43a2-113">The debugger uses the [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent) function at the end of its main loop.</span></span> <span data-ttu-id="a43a2-114">Essa função permite que o processo que está sendo depurado continue em execução.</span><span class="sxs-lookup"><span data-stu-id="a43a2-114">This function allows the process being debugged to continue executing.</span></span>

<span data-ttu-id="a43a2-115">O exemplo a seguir usa as funções [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent) e [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent) para ilustrar como um depurador simples pode ser organizado.</span><span class="sxs-lookup"><span data-stu-id="a43a2-115">The following example uses the [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent) and [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent) functions to illustrate how a simple debugger might be organized.</span></span>


```C++
#include <windows.h>

DWORD OnCreateThreadDebugEvent(const LPDEBUG_EVENT);
DWORD OnCreateProcessDebugEvent(const LPDEBUG_EVENT);
DWORD OnExitThreadDebugEvent(const LPDEBUG_EVENT);
DWORD OnExitProcessDebugEvent(const LPDEBUG_EVENT);
DWORD OnLoadDllDebugEvent(const LPDEBUG_EVENT);
DWORD OnUnloadDllDebugEvent(const LPDEBUG_EVENT);
DWORD OnOutputDebugStringEvent(const LPDEBUG_EVENT);
DWORD OnRipEvent(const LPDEBUG_EVENT);

void EnterDebugLoop(const LPDEBUG_EVENT DebugEv)
{
   DWORD dwContinueStatus = DBG_CONTINUE; // exception continuation 
 
   for(;;) 
   { 
   // Wait for a debugging event to occur. The second parameter indicates
   // that the function does not return until a debugging event occurs. 
 
      WaitForDebugEvent(DebugEv, INFINITE); 

   // Process the debugging event code. 
 
      switch (DebugEv->dwDebugEventCode) 
      { 
         case EXCEPTION_DEBUG_EVENT: 
         // Process the exception code. When handling 
         // exceptions, remember to set the continuation 
         // status parameter (dwContinueStatus). This value 
         // is used by the ContinueDebugEvent function. 
 
            switch(DebugEv->u.Exception.ExceptionRecord.ExceptionCode)
            { 
               case EXCEPTION_ACCESS_VIOLATION: 
               // First chance: Pass this on to the system. 
               // Last chance: Display an appropriate error. 
                  break;
 
               case EXCEPTION_BREAKPOINT: 
               // First chance: Display the current 
               // instruction and register values. 
                  break;
 
               case EXCEPTION_DATATYPE_MISALIGNMENT: 
               // First chance: Pass this on to the system. 
               // Last chance: Display an appropriate error. 
                  break;
 
               case EXCEPTION_SINGLE_STEP: 
               // First chance: Update the display of the 
               // current instruction and register values. 
                  break;
 
               case DBG_CONTROL_C: 
               // First chance: Pass this on to the system. 
               // Last chance: Display an appropriate error. 
                  break;
 
               default:
               // Handle other exceptions. 
                  break;
            } 

            break;
 
         case CREATE_THREAD_DEBUG_EVENT: 
         // As needed, examine or change the thread's registers 
         // with the GetThreadContext and SetThreadContext functions; 
         // and suspend and resume thread execution with the 
         // SuspendThread and ResumeThread functions. 

            dwContinueStatus = OnCreateThreadDebugEvent(DebugEv);
            break;

         case CREATE_PROCESS_DEBUG_EVENT: 
         // As needed, examine or change the registers of the
         // process's initial thread with the GetThreadContext and
         // SetThreadContext functions; read from and write to the
         // process's virtual memory with the ReadProcessMemory and
         // WriteProcessMemory functions; and suspend and resume
         // thread execution with the SuspendThread and ResumeThread
         // functions. Be sure to close the handle to the process image
         // file with CloseHandle.

            dwContinueStatus = OnCreateProcessDebugEvent(DebugEv);
            break;
 
         case EXIT_THREAD_DEBUG_EVENT: 
         // Display the thread's exit code. 

            dwContinueStatus = OnExitThreadDebugEvent(DebugEv);
            break;
 
         case EXIT_PROCESS_DEBUG_EVENT: 
         // Display the process's exit code. 

            dwContinueStatus = OnExitProcessDebugEvent(DebugEv);
            break;
 
         case LOAD_DLL_DEBUG_EVENT: 
         // Read the debugging information included in the newly 
         // loaded DLL. Be sure to close the handle to the loaded DLL 
         // with CloseHandle.

            dwContinueStatus = OnLoadDllDebugEvent(DebugEv);
            break;
 
         case UNLOAD_DLL_DEBUG_EVENT: 
         // Display a message that the DLL has been unloaded. 

            dwContinueStatus = OnUnloadDllDebugEvent(DebugEv);
            break;
 
         case OUTPUT_DEBUG_STRING_EVENT: 
         // Display the output debugging string. 

            dwContinueStatus = OnOutputDebugStringEvent(DebugEv);
            break;

         case RIP_EVENT:
            dwContinueStatus = OnRipEvent(DebugEv);
            break;
      } 
 
   // Resume executing the thread that reported the debugging event. 
 
   ContinueDebugEvent(DebugEv->dwProcessId, 
                      DebugEv->dwThreadId, 
                      dwContinueStatus);
   }
}
```



 

 
