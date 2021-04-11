---
title: Personalização de fluxo ALE
description: A filtragem de rede nas camadas ALE (imposição de camada de aplicativo) da WFP (plataforma de filtragem do Windows) pode ser personalizada com a adição de filtros com opções de classificação específicas.
ms.assetid: 123af237-cf42-410b-8a2f-c011cb5f4f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9843a60719f424403139885f24f165c0dd936b
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104293803"
---
# <a name="ale-flow-customization"></a><span data-ttu-id="74c41-103">Personalização de fluxo ALE</span><span class="sxs-lookup"><span data-stu-id="74c41-103">ALE Flow Customization</span></span>

<span data-ttu-id="74c41-104">A filtragem de rede nas camadas ALE (imposição de camada de aplicativo) da WFP (plataforma de filtragem do Windows) pode ser personalizada com a adição de filtros com opções de classificação específicas.</span><span class="sxs-lookup"><span data-stu-id="74c41-104">Network filtering at the Application Layer Enforcement (ALE) layers of the Windows Filtering Platform (WFP) can be customized by adding filters with specific classify options.</span></span>

## <a name="multicastbroadcast-traffic"></a><span data-ttu-id="74c41-105">Tráfego multicast/difusão</span><span class="sxs-lookup"><span data-stu-id="74c41-105">Multicast/Broadcast Traffic</span></span>

<span data-ttu-id="74c41-106">Para bloquear o tráfego de entrada com base em Estados de difusão ou multicast de saída, adicione um filtro que autorize o tráfego de difusão e multicast de saída e que tenha a opção de [**\_ classificação de opção fwp classificar de \_ \_ \_ estado multicast**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) definida como o **valor da \_ opção fwp \_ \_ negar \_ \_ estado multicast**.</span><span class="sxs-lookup"><span data-stu-id="74c41-106">To block inbound traffic based on outbound multicast or broadcast states, add a filter that authorizes outbound multicast and broadcast traffic and that has the [**FWP\_CLASSIFY\_OPTION\_MULTICAST\_STATE**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option set to **FWP\_OPTION\_VALUE\_DENY\_MULTICAST\_STATE**.</span></span>

## <a name="remote-peers"></a><span data-ttu-id="74c41-107">Pares remotos</span><span class="sxs-lookup"><span data-stu-id="74c41-107">Remote Peers</span></span>

<span data-ttu-id="74c41-108">Para adicionar pacotes de resposta de pares diferentes ao mesmo fluxo de ALE, adicione um filtro que tenha a opção de classificação do fwp opção de [**\_ \_ \_ \_ \_ mapeamento de fonte flexível**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) definida como o **valor da \_ opção fwp habilitar o \_ \_ \_ \_ \_ mapeamento de origem flexível**.</span><span class="sxs-lookup"><span data-stu-id="74c41-108">To add response packets from different peers to the same ALE flow, add a filter that has the [**FWP\_CLASSIFY\_OPTION\_LOOSE\_SOURCE\_MAPPING**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option set to **FWP\_OPTION\_VALUE\_ENABLE\_LOOSE\_SOURCE\_MAPPING**.</span></span>

<span data-ttu-id="74c41-109">Consulte [usando opções de classificação](using-classify-options.md) para o exemplo de código.</span><span class="sxs-lookup"><span data-stu-id="74c41-109">See [Using Classify Options](using-classify-options.md) for code sample.</span></span>

## <a name="ale-flow-lifetime"></a><span data-ttu-id="74c41-110">Tempo de vida do fluxo ALE</span><span class="sxs-lookup"><span data-stu-id="74c41-110">ALE Flow Lifetime</span></span>

<span data-ttu-id="74c41-111">Para modificar os valores de tempo limite de ociosidade para um fluxo de ALE, adicione um filtro que tenha a opção [**fwp de \_ classificação \_ \_ mcast \_ BCAST \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) e/ou a opção de tempo de **\_ \_ \_ \_ vida unicast da opção fwp classificar** definida para o valor de timeout de ociosidade desejado.</span><span class="sxs-lookup"><span data-stu-id="74c41-111">To modify the idle timeout values for an ALE flow, add a filter that has the [**FWP\_CLASSIFY\_OPTION\_MCAST\_BCAST\_LIFETIME**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option and/or the **FWP\_CLASSIFY\_OPTION\_UNICAST\_LIFETIME** option set to the desired idle timeout value.</span></span>

<span data-ttu-id="74c41-112">Consulte [usando opções de classificação](using-classify-options.md) para um exemplo de código.</span><span class="sxs-lookup"><span data-stu-id="74c41-112">See [Using Classify Options](using-classify-options.md) for a code sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74c41-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74c41-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74c41-114">Aplicação da camada de aplicativo (EPA)</span><span class="sxs-lookup"><span data-stu-id="74c41-114">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="74c41-115">Camadas ALE</span><span class="sxs-lookup"><span data-stu-id="74c41-115">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="74c41-116">Filtragem de estado de ALE</span><span class="sxs-lookup"><span data-stu-id="74c41-116">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="74c41-117">Tráfego de difusão/multicast ALE</span><span class="sxs-lookup"><span data-stu-id="74c41-117">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="74c41-118">Reautorização de ALE</span><span class="sxs-lookup"><span data-stu-id="74c41-118">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="74c41-119">Usando opções de classificação</span><span class="sxs-lookup"><span data-stu-id="74c41-119">Using Classify Options</span></span>](using-classify-options.md)
</dt> </dl>

 

 




