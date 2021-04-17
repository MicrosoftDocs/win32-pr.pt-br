---
description: O \_32.dll Ws2 (e protocolos em camadas) chamará WSPCleanup uma vez para cada invocação de WSPStartup.
ms.assetid: c3b7b648-5727-47d6-9ddc-9d9f6511949d
title: Limpeza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc294183f964d00ae9ebb1d74b90b346c2ce8fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813470"
---
# <a name="cleanup"></a><span data-ttu-id="4a696-103">Limpeza</span><span class="sxs-lookup"><span data-stu-id="4a696-103">Cleanup</span></span>

<span data-ttu-id="4a696-104">O \_32.dll Ws2 (e protocolos em camadas) chamará [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) uma vez para cada invocação de [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span><span class="sxs-lookup"><span data-stu-id="4a696-104">The Ws2\_32.dll (and layered protocols) will call [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) once for each invocation of [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span></span> <span data-ttu-id="4a696-105">Em cada invocação, **WSPCleanup** deve decrementar um contador de referência por processo e, quando o contador chega a zero, o provedor de serviços deve se preparar para ser descarregado da memória.</span><span class="sxs-lookup"><span data-stu-id="4a696-105">On each invocation, **WSPCleanup** should decrement a per-process reference counter, and when the counter reaches zero, the service provider must prepare itself to be unloaded from memory.</span></span> <span data-ttu-id="4a696-106">A primeira ordem de negócios é concluir a transmissão de todos os dados não enviados em soquetes configurados para um fechamento normal.</span><span class="sxs-lookup"><span data-stu-id="4a696-106">The first order of business is to finish transmitting any unsent data on sockets that are configured for a graceful close.</span></span> <span data-ttu-id="4a696-107">Depois disso, qualquer um e todos os recursos mantidos pelo provedor serão liberados.</span><span class="sxs-lookup"><span data-stu-id="4a696-107">Thereafter, any and all resources held by the provider are to be freed.</span></span> <span data-ttu-id="4a696-108">O provedor de serviços deve ser deixado em um estado em que possa ser reinicializado imediatamente por uma chamada para **WSPStartup**.</span><span class="sxs-lookup"><span data-stu-id="4a696-108">The service provider must be left in a state where it can be immediately reinitialized by a call to **WSPStartup**.</span></span>

 

 
