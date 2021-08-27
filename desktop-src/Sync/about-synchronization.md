---
description: Para sincronizar o acesso a um recurso, use um dos objetos de sincronização em uma das funções de espera.
ms.assetid: 0930bf12-6d5f-4f2c-914d-53e6e862d3bd
title: Sobre a sincronização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8bca156eec523b30d8f28df8b18a24d9691a33598f5dfe985e4b6b9756ffe3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886400"
---
# <a name="about-synchronization"></a>Sobre a sincronização

Para sincronizar o acesso a um recurso, use um dos [objetos de sincronização](synchronization-objects.md) em uma das [funções de espera](wait-functions.md). O estado de um objeto de sincronização é *sinalizado* ou não *sinalizado*. As funções Wait permitem que um thread bloqueie sua própria execução até que um objeto não sinalizado especificado seja definido como o estado sinalizado. Para obter mais informações, consulte [sincronização entre processos](interprocess-synchronization.md).

Veja a seguir outros mecanismos de sincronização:

-   [entrada e saída sobrepostas](synchronization-and-overlapped-input-and-output.md)
-   [chamadas de procedimento assíncrono](asynchronous-procedure-calls.md)
-   [objetos de seção crítica](critical-section-objects.md)
-   [variáveis de condição](condition-variables.md)
-   [bloqueios de leitor/gravador reduzidos](slim-reader-writer--srw--locks.md)
-   [inicialização única](one-time-initialization.md)
-   [acesso de variável interbloqueada](interlocked-variable-access.md)
-   [listas vinculadas isoladamente interbloqueadas](interlocked-singly-linked-lists.md)
-   [filas de timer](timer-queues.md)
-   a macro [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier)

Para obter informações adicionais sobre sincronização, consulte [sincronização e problemas de multiprocessador](synchronization-and-multiprocessor-issues.md).

 

 
