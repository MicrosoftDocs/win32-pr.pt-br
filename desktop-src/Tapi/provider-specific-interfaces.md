---
description: A TAPI 3 dá suporte à integração de interfaces específicas do provedor de serviço nos objetos padrão, permitindo que os aplicativos tirem proveito da funcionalidade específica do provedor.
ms.assetid: 8077c9a7-3235-41a7-97dc-ca5f3c291ee6
title: Interfaces Provider-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f95499f005c8c3b3e854f33835b9c9b183416d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011548"
---
# <a name="provider-specific-interfaces"></a><span data-ttu-id="a1548-103">Interfaces Provider-Specific</span><span class="sxs-lookup"><span data-stu-id="a1548-103">Provider-Specific Interfaces</span></span>

<span data-ttu-id="a1548-104">A TAPI 3 dá suporte à integração de interfaces específicas do provedor de serviço nos objetos padrão, permitindo que os aplicativos tirem proveito da funcionalidade específica do provedor.</span><span class="sxs-lookup"><span data-stu-id="a1548-104">TAPI 3 supports integration of service provider-specific interfaces into the standard objects, allowing applications to take advantage of provider-specific functionality.</span></span> <span data-ttu-id="a1548-105">Além disso, a TAPI 3 permite que os provedores de serviços forneçam eventos específicos do fornecedor a aplicativos como objetos COM na mesma interface em que o aplicativo recebe eventos padrão.</span><span class="sxs-lookup"><span data-stu-id="a1548-105">Additionally, TAPI 3 allows service providers to deliver vendor-specific events to applications as COM objects over the same interface on which the application receives standard events.</span></span>

<span data-ttu-id="a1548-106">A TAPI alcança essa integração por meio da agregação de objetos específicos do provedor com os objetos padrão – TAPI, endereço, terminal, chamada e CallHub – e expedição ou delegação de métodos desconhecidos a esses objetos específicos do provedor.</span><span class="sxs-lookup"><span data-stu-id="a1548-106">TAPI achieves this integration by aggregating provider-specific objects with the standard objects – TAPI, Address, Terminal, Call, and CallHub – and dispatching or delegating unknown methods to these provider-specific objects.</span></span>

<span data-ttu-id="a1548-107">Por exemplo, um provedor de serviços pode permitir que os aplicativos obtenham informações sobre uma chamada além do que é exposto pela interface [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .</span><span class="sxs-lookup"><span data-stu-id="a1548-107">For example, a service provider may allow applications to obtain information about a call beyond what is exposed by the [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) interface.</span></span> <span data-ttu-id="a1548-108">O fornecedor deve definir uma interface que permita que os aplicativos façam essas consultas adicionais e implementem essa interface em um objeto.</span><span class="sxs-lookup"><span data-stu-id="a1548-108">The vendor must define an interface that allows applications to make these extra queries and implement that interface on an object.</span></span> <span data-ttu-id="a1548-109">Esse objeto também implementa uma interface de consulta de informações de fornecedor para que um aplicativo possa descobrir quais tipos de funções específicas do provedor podem estar disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a1548-109">This object also implements a vendor information-querying interface so that an application can discover what sorts of provider-specific functions might be available.</span></span>

<span data-ttu-id="a1548-110">Quando o aplicativo obtém uma referência a um objeto de chamada, o aplicativo pode usar a nova interface específica do provedor e seus métodos como se eles estivessem implementados pelo próprio objeto de chamada.</span><span class="sxs-lookup"><span data-stu-id="a1548-110">When the application obtains a reference to a call object, the application can use the new provider-specific interface and its methods as if they were implemented by the call object itself.</span></span>

<span data-ttu-id="a1548-111">Consulte [referência da MSPI (interface do provedor de serviços de mídia)](media-service-provider-interface-mspi-reference.md) para obter uma lista de todas as interfaces padrão msp.</span><span class="sxs-lookup"><span data-stu-id="a1548-111">See [Media Service Provider Interface (MSPI) Reference](media-service-provider-interface-mspi-reference.md) for a list of all standard MSP interfaces.</span></span>

<span data-ttu-id="a1548-112">Consulte [IPConf MSP interfaces](ipconf-msp-interfaces.md) para obter uma lista de todas as interfaces específicas para o IPConf msp.</span><span class="sxs-lookup"><span data-stu-id="a1548-112">See [IPConf MSP Interfaces](ipconf-msp-interfaces.md) for a list of all interfaces specific to the IPConf MSP.</span></span>

 

 



