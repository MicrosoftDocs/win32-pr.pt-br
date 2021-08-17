---
description: Um thread pode suspender e retomar a execução de outro thread. Enquanto um thread é suspenso, ele não é agendado para tempo no processador.
ms.assetid: b76d7af7-e3ec-4663-a9e7-832c01733c8c
title: Suspendendo a execução do thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf3ecf2bee1f14ae8571cb7e7402e32a636f4a35ca5c182d32a2a636ed85dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793153"
---
# <a name="suspending-thread-execution"></a>Suspendendo a execução do thread

Um thread pode suspender e retomar a execução de outro thread. Enquanto um thread é suspenso, ele não é agendado para tempo no processador.

Se um thread for criado em um estado suspenso (com o sinalizador [**Create \_ SUSPENDED**](process-creation-flags.md) ), ele não começará a ser executado até que outro thread chame a função [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) com um identificador para o thread suspenso. Isso pode ser útil para inicializar o estado do thread antes que ele comece a ser executado. A suspensão de um thread na criação pode ser útil para sincronização única, pois isso garante que o thread suspenso executará o ponto inicial do código quando você chamar **ResumeThread**.

A função [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) não se destina a ser usada para sincronização de threads porque não controla o ponto no código no qual a execução do thread é suspensa. Essa função é projetada principalmente para uso por depuradores.

Um thread pode gerar temporariamente sua execução para um intervalo especificado chamando as funções [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) ou [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) isso é útil principalmente nos casos em que o thread responde à interação do usuário, pois pode atrasar a execução por tempo suficiente para permitir que os usuários observem os resultados de suas ações. Durante o intervalo de suspensão, o thread não é agendado para tempo no processador.

A função [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) é semelhante a [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) e [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex), exceto que não é possível especificar o intervalo. **SwitchToThread** permite que o thread revele sua fatia de tempo.

 

 
