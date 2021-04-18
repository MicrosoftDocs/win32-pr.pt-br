---
description: Como as duplicatas são os descritores de soquete e não os soquetes subjacentes, todos os Estados associados a um soquete são mantidos em comum em todos os descritores.
ms.assetid: f3a2cd5a-bc3a-4aeb-8606-7b8aa6afb105
title: Vários identificadores para um único soquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2356f24a69d132f87e0f6543f61509ff12acba5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807161"
---
# <a name="multiple-handles-to-a-single-socket"></a><span data-ttu-id="e2d7b-103">Vários identificadores para um único soquete</span><span class="sxs-lookup"><span data-stu-id="e2d7b-103">Multiple Handles to a Single Socket</span></span>

<span data-ttu-id="e2d7b-104">Como as duplicatas são os descritores de soquete e não os soquetes subjacentes, todos os Estados associados a um soquete são mantidos em comum em todos os descritores.</span><span class="sxs-lookup"><span data-stu-id="e2d7b-104">Since what are duplicated are the socket descriptors and not the underlying sockets, all of the states associated with a socket are held in common across all the descriptors.</span></span> <span data-ttu-id="e2d7b-105">Por exemplo, uma operação [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) executada usando um descritor é posteriormente visível usando um [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) de qualquer um ou de todos os descritores.</span><span class="sxs-lookup"><span data-stu-id="e2d7b-105">For example a [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) operation performed using one descriptor is subsequently visible using a [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) from any or all descriptors.</span></span>

<span data-ttu-id="e2d7b-106">A notificação em soquetes compartilhados está sujeita às restrições usuais de [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) e [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e2d7b-106">Notification on shared sockets is subject to the usual constraints of [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) and [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span></span> <span data-ttu-id="e2d7b-107">A emissão de qualquer uma dessas chamadas usando qualquer um dos descritores compartilhados cancela qualquer registro de evento anterior para o soquete, independentemente do qual foi usado para fazer esse registro.</span><span class="sxs-lookup"><span data-stu-id="e2d7b-107">Issuing either of these calls using any of the shared descriptors cancels any previous event registration for the socket, regardless of which descriptor was used to make that registration.</span></span> <span data-ttu-id="e2d7b-108">Portanto, por exemplo, não seria possível ter o processo A receber \_ eventos de leitura FD e o processo B receber eventos de gravação FD \_ .</span><span class="sxs-lookup"><span data-stu-id="e2d7b-108">Thus, for example, it would not be possible to have process A receive FD\_READ events and process B receive FD\_WRITE events.</span></span> <span data-ttu-id="e2d7b-109">Para situações em que tal coordenação rígida é necessária, é recomendável que os desenvolvedores considerem o uso de threads em vez de processos separados.</span><span class="sxs-lookup"><span data-stu-id="e2d7b-109">For situations when such tight coordination is required, it is suggested that developers consider using threads instead of separate processes.</span></span>

 

 
