---
description: As funções a seguir são usadas com depuração.
ms.assetid: 95a838a2-f138-4682-b733-3f363b6c4a4b
title: Funções de depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39bf5f81b08e3a7b324f276fc1a7b5d256d40819
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749064"
---
# <a name="debugging-functions"></a>Funções de depuração

As funções a seguir são usadas com depuração.



| Função                                                           | Descrição                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**CheckRemoteDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)   | Determina se o processo especificado está sendo depurado.                         |
| [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent)                   | Permite que um depurador continue um thread que reportou anteriormente um evento de depuração. |
| [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)                   | Permite que um depurador anexe a um processo ativo e o depure.                     |
| [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop)           | Interrompe o depurador de depurar o processo especificado.                            |
| [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak)                                   | Faz com que uma exceção de ponto de interrupção ocorra no processo atual.                      |
| [**DebugBreakProcess**](/windows/desktop/api/WinBase/nf-winbase-debugbreakprocess)                     | Faz com que uma exceção de ponto de interrupção ocorra no processo especificado.                    |
| [**DebugSetProcessKillOnExit**](/windows/desktop/api/WinBase/nf-winbase-debugsetprocesskillonexit)     | Define a ação a ser executada quando o thread de chamada é encerrado.                      |
| [**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit)                                     | Transfere o controle de execução para o depurador.                                        |
| [**FlushInstructionCache**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushinstructioncache)             | Libera o cache de instruções para o processo especificado.                            |
| [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext)                       | Recupera o contexto do thread especificado.                                      |
| [**GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-getthreadselectorentry)           | Recupera uma entrada de tabela de descritor para o seletor e o thread especificados.           |
| [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)                     | Determina se o processo de chamada está sendo depurado por um depurador de modo de usuário.   |
| [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)                     | Envia uma cadeia de caracteres para o depurador para exibição.                                         |
| [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory)                     | Lê dados de uma área de memória em um processo especificado.                           |
| [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)                       | Define o contexto para o thread especificado.                                          |
| [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent)                     | Aguarda a ocorrência de um evento de depuração em um processo que está sendo depurado.                   |
| [**Wow64GetThreadContext**](/windows/desktop/api/WinBase/nf-winbase-wow64getthreadcontext)             | Recupera o contexto do thread WOW64 especificado.                                |
| [**Wow64GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-wow64getthreadselectorentry) | Recupera uma entrada de tabela de descritor para o seletor especificado e o thread WOW64.     |
| [**Wow64SetThreadContext**](/windows/desktop/api/WinBase/nf-winbase-wow64setthreadcontext)             | Define o contexto do thread WOW64 especificado.                                     |
| [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory)                   | Grava dados em uma área de memória em um processo especificado.                            |



 

 

 
