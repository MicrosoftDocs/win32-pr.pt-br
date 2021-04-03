---
title: Funções de ajuda da ferramenta
description: Lista as funções da biblioteca de ajuda da ferramenta.
ms.assetid: 83732bd6-f4cf-409d-ad17-86503d408dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f9d95598f9b48343ea9731e1a826fb147a73a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006023"
---
# <a name="tool-help-functions"></a>Funções de ajuda da ferramenta

As funções a seguir fazem parte da biblioteca de ajuda da ferramenta.



| Função                                                           | Descrição                                                                                                      |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)       | Tira um instantâneo dos processos especificados, bem como os heaps, módulos e threads usados por esses processos. |
| [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)                                 | Recupera informações sobre o primeiro bloco de um heap que foi alocado por um processo.                      |
| [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst)                         | Recupera informações sobre o primeiro heap que foi alocado por um processo especificado.                       |
| [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext)                           | Recupera informações sobre o próximo heap que foi alocado por um processo.                                  |
| [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)                                   | Recupera informações sobre o próximo bloco de um heap que foi alocado por um processo.                       |
| [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first)                             | Recupera informações sobre o primeiro módulo associado a um processo.                                          |
| [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next)                               | Recupera informações sobre o próximo módulo associado a um processo ou thread.                                 |
| [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first)                           | Recupera informações sobre o primeiro processo encontrado em um instantâneo do sistema.                                  |
| [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next)                             | Recupera informações sobre o próximo processo registrado em um instantâneo do sistema.                                      |
| [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first)                             | Recupera informações sobre o primeiro thread de qualquer processo encontrado em um instantâneo do sistema.                    |
| [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next)                               | Recupera informações sobre o próximo thread de qualquer processo encontrado no instantâneo de memória do sistema.            |
| [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) | Copia a memória alocada para outro processo em um buffer fornecido pelo aplicativo.                                  |



 

 

 




