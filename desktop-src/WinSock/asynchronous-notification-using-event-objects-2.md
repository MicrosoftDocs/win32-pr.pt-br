---
description: As funções WSAEventSelect e WSAEnumNetworkEvents são fornecidas para acomodar aplicativos como daemons e serviços que não têm nenhuma interface do usuário (e, portanto, não usam identificadores do Windows).
ms.assetid: 4254937c-7ee6-49a3-9f30-09aebaf2265b
title: Notificação assíncrona usando objetos de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0495507eacf0960dc98f31594d7f4881d51488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827125"
---
# <a name="asynchronous-notification-using-event-objects"></a><span data-ttu-id="24eb4-103">Notificação assíncrona usando objetos de evento</span><span class="sxs-lookup"><span data-stu-id="24eb4-103">Asynchronous Notification Using Event Objects</span></span>

<span data-ttu-id="24eb4-104">As funções [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) e [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnetworkevents) são fornecidas para acomodar aplicativos como daemons e serviços que não têm nenhuma interface do usuário (e, portanto, não usam identificadores do Windows).</span><span class="sxs-lookup"><span data-stu-id="24eb4-104">The [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) and [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnetworkevents) functions are provided to accommodate applications such as daemons and services that have no user interface (and hence do not use Windows handles).</span></span> <span data-ttu-id="24eb4-105">A função **WSAEventSelect** se comporta exatamente como a função [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) .</span><span class="sxs-lookup"><span data-stu-id="24eb4-105">The **WSAEventSelect** function behaves exactly like the [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) function.</span></span> <span data-ttu-id="24eb4-106">No entanto, em vez de fazer com que uma mensagem do Windows seja enviada na ocorrência de um \_ evento de rede FD xxx (por exemplo, FD \_ Read e FD \_ Write), um objeto de evento designado pelo aplicativo é definido.</span><span class="sxs-lookup"><span data-stu-id="24eb4-106">However, instead of causing a Windows message to be sent on the occurrence of an FD\_XXX network event (for example, FD\_READ and FD\_WRITE), an application-designated event object is set.</span></span>

<span data-ttu-id="24eb4-107">Além disso, o fato de que um \_ evento de rede FD xxx específico ocorreu é lembrado pelo provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="24eb4-107">Also, the fact that a particular FD\_XXX network event has occurred is remembered by the service provider.</span></span> <span data-ttu-id="24eb4-108">O aplicativo pode chamar [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) para que o conteúdo atual da memória de evento de rede seja copiado para um buffer fornecido pelo aplicativo e que a memória do evento de rede seja automaticamente limpa.</span><span class="sxs-lookup"><span data-stu-id="24eb4-108">The application can call [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) to have the current contents of the network event memory copied to an application-supplied buffer and to have the network event memory automatically cleared.</span></span> <span data-ttu-id="24eb4-109">Se necessário, o aplicativo também pode designar um objeto de evento específico que é limpo junto com a memória de evento de rede.</span><span class="sxs-lookup"><span data-stu-id="24eb4-109">If needed, the application can also designate a particular event object that is cleared along with the network event memory.</span></span>

 

 



