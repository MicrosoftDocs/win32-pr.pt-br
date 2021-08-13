---
title: Process Walking
description: Um instantâneo que inclui a lista de processos contém informações sobre cada processo em execução no momento.
ms.assetid: 4fb55763-2206-48ad-8b1f-ed2c33b6f56b
keywords:
- enumerando
- enumerando,processos
- processos
- processos, enumerando processos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6efa129182da256a6ce62b3754ea422df908248f7b0ecc30d3b690c29ffaf9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419656"
---
# <a name="process-walking"></a>Process Walking

Um instantâneo que inclui a lista de processos contém informações sobre cada processo em execução no momento. Você pode recuperar informações para o primeiro processo na lista usando a [**função Process32First.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) Depois de recuperar o primeiro processo na lista, você pode percorrer a lista de processos para entradas subsequentes usando a [**função Process32Next.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) **Process32First** e **Process32Next** preenchem uma estrutura [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) com informações sobre um processo no instantâneo. Para ver um exemplo, consulte [Tirar um instantâneo e exibir processos](taking-a-snapshot-and-viewing-processes.md).

Você pode recuperar um código de status de erro estendido [**para Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) e [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) usando a [**função GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

Você pode ler a memória em um processo específico em um buffer usando a [**função Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) (ou a [**função VirtualQueryEx).**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex)

> [!Note]  
> O conteúdo dos membros **th32ProcessID** e **th32ParentProcessID** de [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) são identificadores de processo e podem ser usados por qualquer função que exige um identificador de processo.

 

 

 