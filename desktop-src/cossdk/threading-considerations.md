---
description: Considerações de thread
ms.assetid: 4d27f0b3-3e30-4e88-b2b2-d57218da4ffa
title: Considerações de thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acde9a06802a867cb6a93e7c52be8066ad483c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010282"
---
# <a name="threading-considerations"></a><span data-ttu-id="1565b-103">Considerações de thread</span><span class="sxs-lookup"><span data-stu-id="1565b-103">Threading Considerations</span></span>

<span data-ttu-id="1565b-104">O gravador de componentes em fila do COM+ é capaz de ser executado no MTA (multithreaded apartment) do processo ou em um STA (single-threaded apartment).</span><span class="sxs-lookup"><span data-stu-id="1565b-104">The COM+ queued components recorder is capable of running in the process's multithreaded apartment (MTA) or in a single-threaded apartment (STA).</span></span> <span data-ttu-id="1565b-105">Quando o gravador é executado no STA, o COM+ requer que cada apartamento contendo objetos deva ter uma fila de [enfileiramento de mensagens](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) para manipular chamadas de outros processos e Apartments dentro do mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="1565b-105">When the recorder is run in the STA, COM+ requires that each apartment containing objects must have a [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) queue to handle calls from other processes and apartments within the same process.</span></span> <span data-ttu-id="1565b-106">Isso significa que a função de trabalho do thread deve ter um loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1565b-106">This means that the thread's work function must have a message loop.</span></span> <span data-ttu-id="1565b-107">Quando um componente em fila é instanciado, o ponteiro de interface retornado é sempre um ponteiro de interface proxy em vez de um ponteiro de interface direta.</span><span class="sxs-lookup"><span data-stu-id="1565b-107">When a queued component is instantiated, the interface pointer returned is always a proxy interface pointer rather than a direct interface pointer.</span></span> <span data-ttu-id="1565b-108">O ponteiro é, na verdade, uma referência a uma instância do gravador.</span><span class="sxs-lookup"><span data-stu-id="1565b-108">The pointer is actually a reference to an instance of the recorder.</span></span> <span data-ttu-id="1565b-109">Se essa referência da interface do gravador for passada para outro thread, o thread original ainda deverá estar executando o loop de mensagem do Windows para que o thread receptor possa desempacotar a interface.</span><span class="sxs-lookup"><span data-stu-id="1565b-109">If this recorder interface reference is passed to another thread, the original thread must still be running the Windows message loop so that the receiving thread can unmarshal the interface.</span></span> <span data-ttu-id="1565b-110">Se esse não for o caso, o thread de recebimento travará em uma chamada para [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span><span class="sxs-lookup"><span data-stu-id="1565b-110">If this is not the case, the receiving thread hangs in a call to [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span></span>

<span data-ttu-id="1565b-111">Se você estiver usando primitivos para sincronizar os threads, considere usar [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) em vez de outras funções de sincronização.</span><span class="sxs-lookup"><span data-stu-id="1565b-111">If you are using primitives to synchronize the threads, consider using [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) instead of other synchronization functions.</span></span> <span data-ttu-id="1565b-112">Isso verifica as mensagens na fila, bem como o estado do objeto de sincronização.</span><span class="sxs-lookup"><span data-stu-id="1565b-112">This checks for messages in the queue as well as the state of the synchronization object.</span></span>

 

 
