---
title: Movimentação de thread
description: Um instantâneo que inclui a lista de threads contém informações sobre cada thread de cada processo em execução no momento.
ms.assetid: 2440b781-652d-4d73-b173-87504e7b49b5
keywords:
- enumerando
- Enumerando, threads
- threads
- threads, enumerando threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32eff584aedaa3f6124cc358a4ee9d2a94962843
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105779874"
---
# <a name="thread-walking"></a>Movimentação de thread

Um instantâneo que inclui a lista de threads contém informações sobre cada thread de cada processo em execução no momento. Você pode recuperar informações para o primeiro thread na lista usando a função [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) . Depois de recuperar o primeiro thread na lista, você pode recuperar informações para threads subsequentes usando a função [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) . **Thread32First** e **Thread32Next** preenchem uma estrutura [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) com informações sobre threads individuais no instantâneo.

Você pode enumerar os threads de um processo específico tirando um instantâneo que inclui os threads e, em seguida, atravessando a lista de threads, mantendo informações sobre os threads que têm o mesmo identificador de processo que o processo especificado.

Você pode recuperar um código de status de erro estendido para [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) e [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) usando a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

> [!Note]  
> O conteúdo do membro **th32ThreadID** de [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) é um identificador de thread e pode ser usado por qualquer função que exija um identificador de thread.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atravessando a lista de threads](traversing-the-thread-list.md)
</dt> </dl>

 

 