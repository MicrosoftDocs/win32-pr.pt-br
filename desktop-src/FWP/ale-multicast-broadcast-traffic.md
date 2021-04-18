---
title: Tráfego de difusão/multicast ALE
description: Todo o tráfego de difusão e multicast de entrada nas camadas de aplicação da camada de aplicativo (EPA) é mapeado para um fluxo de ALE global.
ms.assetid: b10b9758-8fce-4256-a25d-917e01336456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30b56a6e2a27a209baf66d34948b704ae321644
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292116"
---
# <a name="ale-multicastbroadcast-traffic"></a><span data-ttu-id="ce6e2-103">Tráfego de difusão/multicast ALE</span><span class="sxs-lookup"><span data-stu-id="ce6e2-103">ALE Multicast/Broadcast Traffic</span></span>

<span data-ttu-id="ce6e2-104">Todo o tráfego de difusão e multicast de entrada nas camadas de aplicação da camada de aplicativo (EPA) é mapeado para um [fluxo de Ale](ale-stateful-filtering.md)global.</span><span class="sxs-lookup"><span data-stu-id="ce6e2-104">All inbound multicast and broadcast traffic at the Application Layer Enforcement (ALE) layers is mapped to one global [ALE flow](ale-stateful-filtering.md).</span></span> <span data-ttu-id="ce6e2-105">O tráfego de resposta para multicast de entrada e pacotes de difusão é classificado na camada [**FWPM \_ camada de \_ \_ autenticação Ale \_ Connect \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) e os fluxos Ale separados são criados para cada resposta.</span><span class="sxs-lookup"><span data-stu-id="ce6e2-105">Response traffic for inbound multicast and broadcast packets is classified at the [**FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer and separate ALE flows are created for each response.</span></span>

<span data-ttu-id="ce6e2-106">O tráfego de difusão e multicast de saída nas camadas ALE cria um fluxo ALE de 4 segundos.</span><span class="sxs-lookup"><span data-stu-id="ce6e2-106">Outbound multicast and broadcast traffic at the ALE layers creates a 4-second ALE flow.</span></span> <span data-ttu-id="ce6e2-107">Por padrão, a autorização de um pacote de multicast de saída ou de difusão permitirá o tráfego de entrada, seja unicast, multicast ou difusão, de qualquer endereço remoto por até 4 segundos.</span><span class="sxs-lookup"><span data-stu-id="ce6e2-107">By default, the authorization of an outbound multicast or broadcast ALE packet will permit inbound traffic, whether unicast, multicast, or broadcast, from any remote address for up to 4 seconds.</span></span> <span data-ttu-id="ce6e2-108">Tal fluxo ALE só pode ser atualizado ou mantido ativo pelo tráfego de saída subsequente que corresponda ao fluxo da EPA.</span><span class="sxs-lookup"><span data-stu-id="ce6e2-108">Such an ALE flow can only be refreshed or kept alive by subsequent outbound traffic that matches the ALE flow.</span></span>

> [!Note]  
> <span data-ttu-id="ce6e2-109">O tempo de vida de 4 segundos é especificado pelo texto explicativo [**FWPM de texto \_ explicativo interno \_ definir \_ Opções da camada de \_ \_ conexão autenticação \_ \_ V {4 \| 6}**](built-in-callout-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="ce6e2-109">The 4-second lifetime is specified by the built-in callout [**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V{4\|6}**](built-in-callout-identifiers.md).</span></span> <span data-ttu-id="ce6e2-110">Para alterar o tempo de vida padrão de 4 segundos, adicione um filtro que referencie o texto explicativo **FWPM \_ \_ definir \_ opções \_ auth \_ Connect \_ Layer \_ V {4 \| 6}** .</span><span class="sxs-lookup"><span data-stu-id="ce6e2-110">To alter the 4-second default lifetime, add a filter that references the **FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V{4\|6}** callout.</span></span> <span data-ttu-id="ce6e2-111">Consulte [personalização de fluxo Ale](ale-flow-customization.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ce6e2-111">See [ALE Flow Customization](ale-flow-customization.md) for more information.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ce6e2-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ce6e2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce6e2-113">Aplicação da camada de aplicativo (EPA)</span><span class="sxs-lookup"><span data-stu-id="ce6e2-113">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="ce6e2-114">Camadas ALE</span><span class="sxs-lookup"><span data-stu-id="ce6e2-114">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="ce6e2-115">Filtragem de estado de ALE</span><span class="sxs-lookup"><span data-stu-id="ce6e2-115">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="ce6e2-116">Reautorização de ALE</span><span class="sxs-lookup"><span data-stu-id="ce6e2-116">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="ce6e2-117">Personalização de fluxo ALE</span><span class="sxs-lookup"><span data-stu-id="ce6e2-117">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> </dl>

 

 




