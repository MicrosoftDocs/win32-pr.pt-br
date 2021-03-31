---
description: As interfaces de programação de aplicativo de telefonia da Microsoft dão suporte ao desenvolvimento de aplicativos de comunicação para o Microsoft Windows. As interfaces de telefonia estão listadas na tabela a seguir.
ms.assetid: e7348296-ee2d-4e0a-b274-3563dccea841
title: Interfaces de programação de aplicativo de telefonia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19fd6a520c8a53440967eeef753b7ed8c90ba5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836953"
---
# <a name="telephony-application-programming-interfaces"></a><span data-ttu-id="a972a-104">Interfaces de programação de aplicativo de telefonia</span><span class="sxs-lookup"><span data-stu-id="a972a-104">Telephony Application Programming Interfaces</span></span>

<span data-ttu-id="a972a-105">As interfaces de programação de aplicativo de telefonia da Microsoft dão suporte ao desenvolvimento de aplicativos de comunicação para o Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a972a-105">The Microsoft telephony application programming interfaces support the development of communications applications for Microsoft Windows.</span></span> <span data-ttu-id="a972a-106">As interfaces de telefonia estão listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a972a-106">The telephony interfaces are listed in the following table.</span></span>



| <span data-ttu-id="a972a-107">Interface</span><span class="sxs-lookup"><span data-stu-id="a972a-107">Interface</span></span>                                                  | <span data-ttu-id="a972a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a972a-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a972a-109">TAPI 2. x</span><span class="sxs-lookup"><span data-stu-id="a972a-109">TAPI 2.x</span></span>](./tapi-2-2-start-page.md)               | <span data-ttu-id="a972a-110">Uma API baseada em linguagem C que permite implementar aplicativos de comunicação que vão desde o controle de modem básico até centros de chamadas com vários agentes e comutadores.</span><span class="sxs-lookup"><span data-stu-id="a972a-110">A C-programming language based API that enables you to implement communications applications ranging from basic modem control to call centers with multiple agents and switches.</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="a972a-111">TAPI 3. x</span><span class="sxs-lookup"><span data-stu-id="a972a-111">TAPI 3.x</span></span>](tapi-3-1-start-page.md)                        | <span data-ttu-id="a972a-112">Uma API baseada em COM que mescla a telefonia clássica e IP.</span><span class="sxs-lookup"><span data-stu-id="a972a-112">A COM-based API that merges classic and IP telephony.</span></span>                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="a972a-113">TSPI</span><span class="sxs-lookup"><span data-stu-id="a972a-113">TSPI</span></span>](./telephony-service-providers-start-page.md) | <span data-ttu-id="a972a-114">Um TSP (provedor de serviços de telefonia) é uma DLL (biblioteca de vínculo dinâmico) que dá suporte ao controle de dispositivo de comunicação por meio de um conjunto de funções de serviço exportadas.</span><span class="sxs-lookup"><span data-stu-id="a972a-114">A telephony service provider (TSP) is a dynamic-link library (DLL) that supports communications device control through a set of exported service functions.</span></span> <span data-ttu-id="a972a-115">Um aplicativo TAPI usa comandos padronizados, a TAPI passa informações para o provedor de serviços de telefonia e o TSP lida com os comandos específicos que devem ser trocados pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a972a-115">A TAPI application uses standardized commands, TAPI passes information to the telephony service provider, and the TSP handles the specific commands that must be exchanged with the device.</span></span> |
| [<span data-ttu-id="a972a-116">MSPI</span><span class="sxs-lookup"><span data-stu-id="a972a-116">MSPI</span></span>](media-service-providers-start-page.md)             | <span data-ttu-id="a972a-117">Um MSP (provedor de serviços de mídia) permite um controle considerável do aplicativo sobre a mídia para um mecanismo de transporte específico.</span><span class="sxs-lookup"><span data-stu-id="a972a-117">A media service provider (MSP) allows an application considerable control over the media for a particular transport mechanism.</span></span> <span data-ttu-id="a972a-118">Um MSP é sempre emparelhado com um provedor de serviços de telefonia (TSP).</span><span class="sxs-lookup"><span data-stu-id="a972a-118">An MSP is always paired with a telephony service provider (TSP).</span></span>                                                                                                                                                         |



 

 

 
