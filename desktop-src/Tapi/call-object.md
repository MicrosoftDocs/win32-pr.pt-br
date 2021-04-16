---
description: O objeto de chamada representa uma conexão de endereço entre o endereço local e um ou mais endereços.
ms.assetid: 67c063ba-8b12-40d6-9011-923bdee8b214
title: Objeto de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b8ea40b7b2cadece9c89a45f9296995ad92fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768581"
---
# <a name="call-object"></a><span data-ttu-id="5ef65-103">Objeto de chamada</span><span class="sxs-lookup"><span data-stu-id="5ef65-103">Call Object</span></span>

<span data-ttu-id="5ef65-104">O objeto de chamada representa a conexão de um endereço entre o endereço local e um ou mais endereços.</span><span class="sxs-lookup"><span data-stu-id="5ef65-104">The Call object represents an address's connection between the local address and one or more other addresses.</span></span> <span data-ttu-id="5ef65-105">Todo o controle de chamada é feito por meio do objeto de chamada.</span><span class="sxs-lookup"><span data-stu-id="5ef65-105">All call control is done through the Call object.</span></span> <span data-ttu-id="5ef65-106">[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) e [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) são as interfaces usadas com mais frequência no objeto de chamada.</span><span class="sxs-lookup"><span data-stu-id="5ef65-106">[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) and [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) are the most frequently used interfaces on the call object.</span></span> <span data-ttu-id="5ef65-107">Essas interfaces implementam uma variedade de operações e consultas, como a aquisição de ponteiros de interface para fluxos de mídia ou a obtenção da ID do chamador.</span><span class="sxs-lookup"><span data-stu-id="5ef65-107">These interfaces implement a variety of operations and queries, such as acquiring interface pointers for media streams or getting the caller ID.</span></span> <span data-ttu-id="5ef65-108">Consulte as principais seções de visão geral sobre [operações de sessão](session-operations-ovr.md) e [informações de sessão](session-information-ovr.md) para ver as revisões com suporte da TAPI.</span><span class="sxs-lookup"><span data-stu-id="5ef65-108">See the main overview sections on [Session Operations](session-operations-ovr.md) and [Session Information](session-information-ovr.md) for reviews of those supported by TAPI.</span></span>

<span data-ttu-id="5ef65-109">Um provedor de serviços de mídia pode implementar [interfaces específicas do provedor](provider-specific-interfaces.md), que são agregadas em um objeto de chamada pela TAPI.</span><span class="sxs-lookup"><span data-stu-id="5ef65-109">A media service provider can implement [provider-specific interfaces](provider-specific-interfaces.md), which are aggregated on a call object by TAPI.</span></span> <span data-ttu-id="5ef65-110">Para obter informações detalhadas sobre o que um provedor implementou, consulte a documentação do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="5ef65-110">For detailed information on what a provider has implemented, see the service provider's documentation.</span></span>

<span data-ttu-id="5ef65-111">Os exemplos [fazer uma chamada](make-a-call.md) e [receber um](receive-a-call.md) código de chamada mostram algumas ilustrações de como usar um objeto de chamada.</span><span class="sxs-lookup"><span data-stu-id="5ef65-111">The [Make a Call](make-a-call.md) and [Receive a Call](receive-a-call.md) code examples show some illustrations of using a Call object.</span></span>

<span data-ttu-id="5ef65-112">Consulte [interfaces do objeto de chamada](call-object-interfaces.md) para obter uma lista de todas as interfaces associadas ao objeto de chamada.</span><span class="sxs-lookup"><span data-stu-id="5ef65-112">See [Call Object Interfaces](call-object-interfaces.md) for a list of all interfaces associated with the Call object.</span></span>

 

 



