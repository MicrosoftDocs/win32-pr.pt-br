---
title: Movimentação de processo
description: Um instantâneo que inclui a lista de processos contém informações sobre cada processo em execução no momento.
ms.assetid: 4fb55763-2206-48ad-8b1f-ed2c33b6f56b
keywords:
- enumerando
- Enumerando, processos
- processos
- processos, enumerando processos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc95f0de4021ce3c355286376decbdecef2c883
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454173"
---
# <a name="process-walking"></a>Movimentação de processo

Um instantâneo que inclui a lista de processos contém informações sobre cada processo em execução no momento. Você pode recuperar informações para o primeiro processo na lista usando a função [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) . Depois de recuperar o primeiro processo na lista, você pode atravessar a lista de processos para entradas subsequentes usando a função [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) . **Process32First** e **Process32Next** preenchem uma estrutura [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) com informações sobre um processo no instantâneo. Para obter um exemplo, consulte [fazendo um instantâneo e exibindo processos](taking-a-snapshot-and-viewing-processes.md).

Você pode recuperar um código de status de erro estendido para [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) e [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) usando a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

Você pode ler a memória em um processo específico em um buffer usando a função [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) (ou a função [**VirtualQueryEx**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex) ).

> [!Note]  
> O conteúdo dos membros **th32ProcessID** e **th32ParentProcessID** de [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) são identificadores de processo e pode ser usado por qualquer função que exija um identificador de processo.

 

 

 