---
description: Os objetos de evento do Windows Sockets são construções simples que podem ser criadas e fechadas, definidas e limpas, aguardados e sondados.
ms.assetid: 65a7627e-150e-4ca3-bc17-d2b380ee02d1
title: Usando objetos de evento (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26a9b70ff49bf7d46f2907c04fd8911d55dd623
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811602"
---
# <a name="using-event-objects-windows-sockets-2"></a><span data-ttu-id="6c647-103">Usando objetos de evento (Windows Sockets 2)</span><span class="sxs-lookup"><span data-stu-id="6c647-103">Using Event Objects (Windows Sockets 2)</span></span>

<span data-ttu-id="6c647-104">Os objetos de evento do Windows Sockets são construções simples que podem ser criadas e fechadas, definidas e limpas, aguardados e sondados.</span><span class="sxs-lookup"><span data-stu-id="6c647-104">Windows Sockets event objects are simple constructs that can be created and closed, set and cleared, waited upon and polled.</span></span> <span data-ttu-id="6c647-105">O modelo aceito é para que os clientes criem um objeto de evento e forneçam o identificador como um parâmetro (ou como um componente de uma estrutura de parâmetro) em funções como [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) e [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6c647-105">The accepted model is for clients to create an event object and supply the handle as a parameter (or as a component of a parameter structure) in functions such as [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) and [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span></span> <span data-ttu-id="6c647-106">Quando a condição nomeada ocorreu, o provedor de serviços usa o identificador para definir o objeto de evento chamando [**WPUSetEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent).</span><span class="sxs-lookup"><span data-stu-id="6c647-106">When the nominated condition has occurred, the service provider uses the handle to set the event object by calling [**WPUSetEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent).</span></span> <span data-ttu-id="6c647-107">Enquanto isso, o cliente SPI do Winsock pode bloquear e aguardar ou sondar até que o objeto de evento se torne definido (sinalizado).</span><span class="sxs-lookup"><span data-stu-id="6c647-107">Meanwhile, the Winsock SPI client may either block and wait or poll until the event object becomes set (signaled).</span></span> <span data-ttu-id="6c647-108">O cliente pode, subsequentemente, limpar ou redefinir o objeto de evento e usá-lo novamente.</span><span class="sxs-lookup"><span data-stu-id="6c647-108">The client may subsequently clear or reset the event object and use it again.</span></span>

 

 
