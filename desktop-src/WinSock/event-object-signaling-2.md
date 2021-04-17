---
description: WSPEventSelect se comporta exatamente como WSPAsyncSelect, exceto que, em vez de fazer com que uma mensagem do Windows seja enviada na ocorrência de qualquer \_ evento de rede do FD xxx indicado (por exemplo, FD \_ Read, FD \_ Write, etc.), um objeto de evento designado é definido.
ms.assetid: 28f6eb78-1bb8-4eda-aac5-017975890502
title: Sinalização de objeto de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42854a1f4e116c8dba100025007362898d183f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811673"
---
# <a name="event-object-signaling"></a><span data-ttu-id="d4395-103">Sinalização de objeto de evento</span><span class="sxs-lookup"><span data-stu-id="d4395-103">Event Object Signaling</span></span>

<span data-ttu-id="d4395-104">[**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) se comporta exatamente como [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) , exceto que, em vez de fazer com que uma mensagem do Windows seja enviada na ocorrência de qualquer \_ evento de rede do FD xxx indicado (por exemplo, FD \_ Read, FD \_ Write, etc.), um objeto de evento designado é definido.</span><span class="sxs-lookup"><span data-stu-id="d4395-104">[**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) behaves exactly like [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) except that, rather than cause a Windows message to be sent upon the occurrence of any nominated FD\_XXX network event (for example, FD\_READ, FD\_WRITE, etc.), a designated event object is set.</span></span>

<span data-ttu-id="d4395-105">Além disso, o fato de que um \_ evento de rede FD xxx específico ocorreu é lembrado pelo provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="d4395-105">Also, the fact that a particular FD\_XXX network event has occurred is remembered by the service provider.</span></span> <span data-ttu-id="d4395-106">Isso é necessário, pois a ocorrência de qualquer e todos os eventos de rede indicados resultarão em um único objeto de evento sendo sinalizado.</span><span class="sxs-lookup"><span data-stu-id="d4395-106">This is needed since the occurrence of any and all nominated network events will result in a single event object becoming signaled.</span></span> <span data-ttu-id="d4395-107">Uma chamada para [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) faz com que o conteúdo atual da memória de evento de rede seja copiado para um buffer fornecido pelo cliente e a memória de evento de rede seja apagada.</span><span class="sxs-lookup"><span data-stu-id="d4395-107">A call to [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) causes the current contents of the network event memory to be copied to a client-supplied buffer and the network event memory to be cleared.</span></span> <span data-ttu-id="d4395-108">O cliente também pode designar um objeto de evento específico para ser limpo atomicamente junto com a memória de evento de rede.</span><span class="sxs-lookup"><span data-stu-id="d4395-108">The client may also designate a particular event object to be cleared atomically along with the network event memory.</span></span>

 

 
