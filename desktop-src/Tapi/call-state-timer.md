---
description: Atualmente, todo o tempo de chamadas é deixado para aplicativos.
ms.assetid: 9eb98b48-4bee-4f6d-b818-2f81b36591da
title: Temporizador de estado de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d273d7f8439ebfee9d6668565745ed2c209f70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754201"
---
# <a name="call-state-timer"></a><span data-ttu-id="24315-103">Temporizador de estado de chamada</span><span class="sxs-lookup"><span data-stu-id="24315-103">Call State Timer</span></span>

<span data-ttu-id="24315-104">Atualmente, todo o tempo de chamadas é deixado para aplicativos.</span><span class="sxs-lookup"><span data-stu-id="24315-104">Currently, all timing of calls is left up to applications.</span></span> <span data-ttu-id="24315-105">Isso pode ser um tanto cansativo se o aplicativo estiver monitorando um grande número de chamadas, e se vários aplicativos estiverem presentes, possivelmente em vários servidores, poderá ser necessário para todos eles manter temporizadores nas mesmas chamadas.</span><span class="sxs-lookup"><span data-stu-id="24315-105">This can be burdensome if the application is monitoring a large number of calls, and if multiple applications are present, possibly on multiple servers, it can be necessary for them to all maintain timers on the same calls.</span></span> <span data-ttu-id="24315-106">Portanto, faz mais sentido para o tempo de estado de chamada ser manipulado pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="24315-106">It therefore makes more sense for call state timing to be handled by the server.</span></span>

<span data-ttu-id="24315-107">O membro **tStateEntryTime** no [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) permite o tempo de chamadas em Estados a serem relatados.</span><span class="sxs-lookup"><span data-stu-id="24315-107">The **tStateEntryTime** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) allows timing of calls in states to be reported.</span></span> <span data-ttu-id="24315-108">O membro (do tipo **SYSTIME**) indica a hora em que o estado atual foi inserido.</span><span class="sxs-lookup"><span data-stu-id="24315-108">The member (of type **SYSTIME**) indicates the time at which the current state was entered.</span></span>

 

 



