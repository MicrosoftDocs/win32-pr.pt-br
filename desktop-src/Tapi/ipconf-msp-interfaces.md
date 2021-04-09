---
description: O IP Conferencing MSP implementa várias interfaces específicas do provedor para o controle de participante. Essas interfaces são expostas no objeto de chamada, se este MSP estiver associado à chamada.
ms.assetid: 01af2452-de2d-42ce-970d-82a83ae0b428
title: Interfaces MSP IPConf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edb3c04a93909d237ae25e06c3ed2e0fcc5db9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091318"
---
# <a name="ipconf-msp-interfaces"></a><span data-ttu-id="c4991-104">Interfaces MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="c4991-104">IPConf MSP Interfaces</span></span>

<span data-ttu-id="c4991-105">\[ As interfaces IPConf MSP não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c4991-105">\[ The IPConf MSP Interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c4991-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="c4991-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c4991-107">O IP Conferencing MSP implementa várias interfaces específicas do provedor para o controle de participante.</span><span class="sxs-lookup"><span data-stu-id="c4991-107">The IP conferencing MSP implements several provider-specific interfaces for participant control.</span></span> <span data-ttu-id="c4991-108">Essas interfaces são expostas no objeto de chamada, se este MSP estiver associado à chamada.</span><span class="sxs-lookup"><span data-stu-id="c4991-108">These interfaces are exposed on the call object, if this MSP is associated with the call.</span></span>

<span data-ttu-id="c4991-109">As interfaces [**ITParticipantEvent**](itparticipantevent.md) e [**IEnumParticipant**](ienumparticipant.md) são objetos autônomos e são listadas aqui para conveniência de referência.</span><span class="sxs-lookup"><span data-stu-id="c4991-109">The [**ITParticipantEvent**](itparticipantevent.md) and [**IEnumParticipant**](ienumparticipant.md) interfaces are stand-alone objects, and are listed here for reference convenience.</span></span>



| <span data-ttu-id="c4991-110">Interface</span><span class="sxs-lookup"><span data-stu-id="c4991-110">Interface</span></span>                                            | <span data-ttu-id="c4991-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4991-111">Description</span></span>                                                                                                                                               |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4991-112">**IMulticastControl**</span><span class="sxs-lookup"><span data-stu-id="c4991-112">**IMulticastControl**</span></span>](imulticastcontrol.md)       | <span data-ttu-id="c4991-113">Permite que um aplicativo defina e obtenha o modo de loopback [**( \_ \_ modo de loopback multicast**](multicast-loopback-mode.md)) para um objeto de conferência multicast.</span><span class="sxs-lookup"><span data-stu-id="c4991-113">Allows an application to set and get the loopback mode ( [**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md)) for a multicast conference object.</span></span> |
| [<span data-ttu-id="c4991-114">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="c4991-114">**ITParticipant**</span></span>](itparticipant.md)               | <span data-ttu-id="c4991-115">Permite que um aplicativo recupere informações sobre os participantes da conferência e obtenha ponteiros para os fluxos associados a esses participantes.</span><span class="sxs-lookup"><span data-stu-id="c4991-115">Allows an application to retrieve information on conference participants, and get pointers to the streams associated with those participants.</span></span>             |
| [<span data-ttu-id="c4991-116">**ITParticipantControl**</span><span class="sxs-lookup"><span data-stu-id="c4991-116">**ITParticipantControl**</span></span>](itparticipantcontrol.md) | <span data-ttu-id="c4991-117">Permite que um aplicativo recupere ponteiros para os participantes em uma conferência.</span><span class="sxs-lookup"><span data-stu-id="c4991-117">Allows an application to retrieve pointers to the participants in a conference.</span></span>                                                                           |
| [<span data-ttu-id="c4991-118">**ITParticipantEvent**</span><span class="sxs-lookup"><span data-stu-id="c4991-118">**ITParticipantEvent**</span></span>](itparticipantevent.md)     | <span data-ttu-id="c4991-119">Permite que um aplicativo recupere informações de evento relacionadas a um participante da conferência.</span><span class="sxs-lookup"><span data-stu-id="c4991-119">Allows an application to retrieve event information concerning a conference participant.</span></span>                                                                  |
| [<span data-ttu-id="c4991-120">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="c4991-120">**IEnumParticipant**</span></span>](ienumparticipant.md)         | <span data-ttu-id="c4991-121">Enumera [**ITParticipant**](itparticipant.md).</span><span class="sxs-lookup"><span data-stu-id="c4991-121">Enumerates [**ITParticipant**](itparticipant.md).</span></span>                                                                                                        |



 

 

 



