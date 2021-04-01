---
description: A TAPI 2,2 básica pode ser usada para gerenciar os centros de chamadas e outros elementos da infraestrutura de rede de telefonia (como servidores de IVR e de correio de voz) por meio de controle de chamada de terceiros.
ms.assetid: e920dc4a-adb4-4a36-ac04-f265538531eb
title: Controle do Call Center
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4200ff434249856507109915f41f7f1479eddfd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829294"
---
# <a name="call-center-control"></a><span data-ttu-id="59a84-103">Controle do Call Center</span><span class="sxs-lookup"><span data-stu-id="59a84-103">Call Center Control</span></span>

<span data-ttu-id="59a84-104">A TAPI 2,2 básica pode ser usada para gerenciar os centros de chamadas e outros elementos da infraestrutura de rede de telefonia (como servidores de IVR e de correio de voz) por meio de controle de chamada de terceiros.</span><span class="sxs-lookup"><span data-stu-id="59a84-104">Basic TAPI 2.2 can be used to manage call centers and other elements of Telephony network infrastructure (such as IVR and voice mail servers) through third-party call control.</span></span> <span data-ttu-id="59a84-105">Para ajudar a criar proxies AD que serão executados em servidores, as funções foram adicionadas à TAPI 2,2 para fornecer assistência adicional aos desenvolvedores de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="59a84-105">To help create ACD proxies that will run on servers, functions have been added to TAPI 2.2 to provide additional assistance to application developers.</span></span>

<span data-ttu-id="59a84-106">Os tópicos a seguir descrevem os recursos TAPI 2,2 que você pode usar para implementar controles de Call Center:</span><span class="sxs-lookup"><span data-stu-id="59a84-106">The following topics describe the TAPI 2.2 features that you can use to implement call center controls:</span></span>

-   [<span data-ttu-id="59a84-107">Modelagem de um Call Center</span><span class="sxs-lookup"><span data-stu-id="59a84-107">Modeling of a Call Center</span></span>](modeling-of-a-call-center.md)
-   [<span data-ttu-id="59a84-108">Rádio</span><span class="sxs-lookup"><span data-stu-id="59a84-108">Stations</span></span>](stations.md)
-   [<span data-ttu-id="59a84-109">Discagem preditiva</span><span class="sxs-lookup"><span data-stu-id="59a84-109">Predictive Dialing</span></span>](predictive-dialing.md)
-   [<span data-ttu-id="59a84-110">Filas de chamadas e pontos de rota</span><span class="sxs-lookup"><span data-stu-id="59a84-110">Call Queues and Route Points</span></span>](call-queues-and-route-points.md)
-   [<span data-ttu-id="59a84-111">Monitoramento e controle do AD Agent</span><span class="sxs-lookup"><span data-stu-id="59a84-111">ACD Agent Monitoring and Control</span></span>](acd-agent-monitoring-and-control.md)
-   [<span data-ttu-id="59a84-112">Controle de status de estação</span><span class="sxs-lookup"><span data-stu-id="59a84-112">Station Status Control</span></span>](station-status-control.md)
-   [<span data-ttu-id="59a84-113">Controle de status de estação</span><span class="sxs-lookup"><span data-stu-id="59a84-113">Station Status Control</span></span>](station-status-control.md)
-   [<span data-ttu-id="59a84-114">Temporizador de estado de chamada</span><span class="sxs-lookup"><span data-stu-id="59a84-114">Call State Timer</span></span>](call-state-timer.md)
-   [<span data-ttu-id="59a84-115">Temporizadores de eventos de mídia</span><span class="sxs-lookup"><span data-stu-id="59a84-115">Media Event Timers</span></span>](media-event-timers.md)

<span data-ttu-id="59a84-116">A TAPI 3. x é a API preferida de escrever aplicativos de agente AD.</span><span class="sxs-lookup"><span data-stu-id="59a84-116">TAPI 3.x is the preferred API of writing ACD Agent applications.</span></span> <span data-ttu-id="59a84-117">Consulte a seção [controles do Call Center](./about-call-center-controls.md) para obter informações sobre como usar essas interfaces e métodos.</span><span class="sxs-lookup"><span data-stu-id="59a84-117">Please see the [Call Center Controls](./about-call-center-controls.md) section for information on using these interfaces and methods.</span></span> <span data-ttu-id="59a84-118">No entanto, a TAPI 2,2 permanece utilizável para conjuntos de aplicativos ad completos, se desejado.</span><span class="sxs-lookup"><span data-stu-id="59a84-118">However, TAPI 2.2 remains usable for full ACD application suites if desired.</span></span>

 

 
