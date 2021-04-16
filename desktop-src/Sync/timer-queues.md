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
# <a name="timer-queues"></a><span data-ttu-id="ea6a8-103">Filas de timer</span><span class="sxs-lookup"><span data-stu-id="ea6a8-103">Timer Queues</span></span>

<span data-ttu-id="ea6a8-104">A função [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) cria uma fila para temporizadores.</span><span class="sxs-lookup"><span data-stu-id="ea6a8-104">The [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) function creates a queue for timers.</span></span> <span data-ttu-id="ea6a8-105">Os temporizadores nessa fila, conhecidos como *temporizadores de fila de temporizador*, são objetos leves que permitem especificar uma função de retorno de chamada a ser chamado quando o tempo de espera especificado chegar.</span><span class="sxs-lookup"><span data-stu-id="ea6a8-105">Timers in this queue, known as *timer-queue timers*, are lightweight objects that enable you to specify a callback function to be called when the specified due time arrives.</span></span> <span data-ttu-id="ea6a8-106">A operação de espera é executada por um thread no [pool de threads](../procthread/thread-pooling.md).</span><span class="sxs-lookup"><span data-stu-id="ea6a8-106">The wait operation is performed by a thread in the [thread pool](../procthread/thread-pooling.md).</span></span>

<span data-ttu-id="ea6a8-107">Para adicionar um temporizador à fila, chame a função [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) .</span><span class="sxs-lookup"><span data-stu-id="ea6a8-107">To add a timer to the queue, call the [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function.</span></span> <span data-ttu-id="ea6a8-108">Para atualizar um temporizador-Queue timer, chame a função [**ChangeTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) .</span><span class="sxs-lookup"><span data-stu-id="ea6a8-108">To update a timer-queue timer, call the [**ChangeTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) function.</span></span> <span data-ttu-id="ea6a8-109">Você pode especificar uma função de retorno de chamada a ser executada por um thread de trabalho do pool de threads quando o temporizador expirar.</span><span class="sxs-lookup"><span data-stu-id="ea6a8-109">You can specify a callback function to be executed by a worker thread from the thread pool when the timer expires.</span></span>

<span data-ttu-id="ea6a8-110">Para cancelar um temporizador pendente, chame a função [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) .</span><span class="sxs-lookup"><span data-stu-id="ea6a8-110">To cancel a pending timer, call the [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) function.</span></span> <span data-ttu-id="ea6a8-111">Quando terminar com a fila de temporizadores, chame a função [**DeleteTimerQueueEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) para excluir a fila de timer.</span><span class="sxs-lookup"><span data-stu-id="ea6a8-111">When you are finished with the queue of timers, call the [**DeleteTimerQueueEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) function to delete the timer queue.</span></span> <span data-ttu-id="ea6a8-112">Todos os temporizadores pendentes na fila são cancelados e excluídos.</span><span class="sxs-lookup"><span data-stu-id="ea6a8-112">Any pending timers in the queue are canceled and deleted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea6a8-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ea6a8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea6a8-114">Usando filas de temporizador</span><span class="sxs-lookup"><span data-stu-id="ea6a8-114">Using Timer Queues</span></span>](using-timer-queues.md)
</dt> </dl>

 

 
