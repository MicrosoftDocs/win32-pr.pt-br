---
description: Se um soquete estiver no modo de não bloqueio, qualquer operação de e/s deverá ser concluída imediatamente ou retornar o código de erro WSAEWOULDBLOCK indicando que a operação não pode ser concluída de imediato.
ms.assetid: badd279b-ec71-4761-9066-d501aa2485c2
title: Entrada/saída de não bloqueio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9f6fec896c8daf1998e71a20a23a296b7b5a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501681"
---
# <a name="nonblocking-inputoutput"></a><span data-ttu-id="88ca6-103">Entrada/saída de não bloqueio</span><span class="sxs-lookup"><span data-stu-id="88ca6-103">Nonblocking Input/Output</span></span>

<span data-ttu-id="88ca6-104">Se um soquete estiver no modo de não bloqueio, qualquer operação de e/s deverá ser concluída imediatamente ou retornar o código de erro WSAEWOULDBLOCK indicando que a operação não pode ser concluída de imediato.</span><span class="sxs-lookup"><span data-stu-id="88ca6-104">If a socket is in nonblocking mode, any I/O operation must either complete immediately or return the error code WSAEWOULDBLOCK indicating that the operation cannot be finished right away.</span></span> <span data-ttu-id="88ca6-105">No último caso, um mecanismo é necessário para descobrir quando é apropriado tentar a operação novamente com a expectativa de que a operação terá sucesso.</span><span class="sxs-lookup"><span data-stu-id="88ca6-105">In the latter case, a mechanism is needed to discover when it is appropriate to try the operation again with the expectation that the operation will succeed.</span></span> <span data-ttu-id="88ca6-106">Um conjunto de eventos de rede foi definido para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="88ca6-106">A set of network events has been defined for this purpose.</span></span> <span data-ttu-id="88ca6-107">Esses eventos podem ser sondados ou aguardados usando [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)), ou podem ser registrados para entrega assíncrona chamando [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) ou [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88ca6-107">These events can be polled or waited on by using [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)), or they can be registered for asynchronous delivery by calling [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) or [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span></span> <span data-ttu-id="88ca6-108">Consulte [notificação de eventos de rede](notification-of-network-events-2.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="88ca6-108">See [Notification of Network Events](notification-of-network-events-2.md) for more information.</span></span>

 

 
