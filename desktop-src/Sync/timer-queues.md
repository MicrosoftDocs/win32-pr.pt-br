---
description: A função CreateTimerQueue cria uma fila para temporizadores.
ms.assetid: ee85a6c3-3a1d-4f94-9112-cb8247b2a189
title: Filas de temporizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16e0ae30e02ad9fbc8889c0d7b1094895ebec27c3db8b67acf509ee02e9da85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885874"
---
# <a name="timer-queues"></a>Filas de temporizador

A [**função CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) cria uma fila para temporizadores. Temporizadores nessa fila, conhecidos como *temporizadores* de fila de temporizador, são objetos leves que permitem especificar uma função de retorno de chamada a ser chamada quando o tempo de vencimento especificado chegar. A operação de espera é executada por um thread no [pool de threads](../procthread/thread-pooling.md).

Para adicionar um temporizador à fila, chame a [**função CreateTimerQueueTimer.**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) Para atualizar um temporizador de fila, chame a [**função ChangeTimerQueueTimer.**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) Você pode especificar uma função de retorno de chamada a ser executada por um thread de trabalho do pool de threads quando o temporizador expirar.

Para cancelar um temporizador pendente, chame a [**função DeleteTimerQueueTimer.**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) Quando terminar a fila de temporizadores, chame a [**função DeleteTimerQueueEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) para excluir a fila do temporizador. Todos os temporizadores pendentes na fila são cancelados e excluídos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando filas de temporizador](using-timer-queues.md)
</dt> </dl>

 

 
