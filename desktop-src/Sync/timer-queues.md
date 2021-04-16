---
description: A função CreateTimerQueue cria uma fila para temporizadores.
ms.assetid: ee85a6c3-3a1d-4f94-9112-cb8247b2a189
title: Filas de timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ad2f94612c234b3ec0d1d75fa723c4e86e6fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754094"
---
# <a name="timer-queues"></a>Filas de timer

A função [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) cria uma fila para temporizadores. Os temporizadores nessa fila, conhecidos como *temporizadores de fila de temporizador*, são objetos leves que permitem especificar uma função de retorno de chamada a ser chamado quando o tempo de espera especificado chegar. A operação de espera é executada por um thread no [pool de threads](../procthread/thread-pooling.md).

Para adicionar um temporizador à fila, chame a função [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) . Para atualizar um temporizador-Queue timer, chame a função [**ChangeTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) . Você pode especificar uma função de retorno de chamada a ser executada por um thread de trabalho do pool de threads quando o temporizador expirar.

Para cancelar um temporizador pendente, chame a função [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) . Quando terminar com a fila de temporizadores, chame a função [**DeleteTimerQueueEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) para excluir a fila de timer. Todos os temporizadores pendentes na fila são cancelados e excluídos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando filas de temporizador](using-timer-queues.md)
</dt> </dl>

 

 
