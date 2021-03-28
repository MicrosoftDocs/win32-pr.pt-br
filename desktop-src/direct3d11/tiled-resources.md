---
title: Recursos em ladrilho
description: Os recursos ao lado dos ladrilhos podem ser considerados como recursos lógicos grandes que usam pequenas quantidades de memória física.
ms.assetid: 03083460-192b-40cb-8ee1-76df6d95f72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c7e6aaf60f58f55274c9d7a135b9107933f640
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822334"
---
# <a name="tiled-resources"></a><span data-ttu-id="e9cca-103">Recursos em ladrilho</span><span class="sxs-lookup"><span data-stu-id="e9cca-103">Tiled resources</span></span>

<span data-ttu-id="e9cca-104">Os recursos ao lado dos ladrilhos podem ser considerados como recursos lógicos grandes que usam pequenas quantidades de memória física.</span><span class="sxs-lookup"><span data-stu-id="e9cca-104">Tiled resources can be thought of as large logical resources that use small amounts of physical memory.</span></span>

<span data-ttu-id="e9cca-105">Esta seção descreve o motivo pelo qual os recursos do lado do xadrez são necessários e como você cria e usa recursos em ladrilho.</span><span class="sxs-lookup"><span data-stu-id="e9cca-105">This section describes why tiled resources are needed and how you create and use tiled resources.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e9cca-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="e9cca-106">In this section</span></span>



| <span data-ttu-id="e9cca-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="e9cca-107">Topic</span></span>                                                                                   | <span data-ttu-id="e9cca-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9cca-108">Description</span></span>                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9cca-109">Por que os recursos do lado do xadrez são necessários?</span><span class="sxs-lookup"><span data-stu-id="e9cca-109">Why are tiled resources needed?</span></span>](why-are-tiled-resources-needed-.md)<br/>       | <span data-ttu-id="e9cca-110">Os recursos do lado do ladrilho são necessários, portanto, menos memória de GPU (unidade de processamento gráfico) é desperdiçada armazenando regiões de superfícies que o aplicativo sabe que não será acessado, e o hardware pode entender como filtrar por blocos adjacentes.</span><span class="sxs-lookup"><span data-stu-id="e9cca-110">Tiled resources are needed so less graphics processing unit (GPU) memory is wasted storing regions of surfaces that the application knows will not be accessed, and the hardware can understand how to filter across adjacent tiles.</span></span><br/>     |
| [<span data-ttu-id="e9cca-111">Criando recursos em ladrilhos</span><span class="sxs-lookup"><span data-stu-id="e9cca-111">Creating tiled resources</span></span>](creating-tiled-resources.md)<br/>                     | <span data-ttu-id="e9cca-112">Os recursos em ladrilho são criados especificando-se o sinalizador de [**\_ \_ \_ lado diverso do recurso D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) ao criar um recurso.</span><span class="sxs-lookup"><span data-stu-id="e9cca-112">Tiled resources are created by specifying the [**D3D11\_RESOURCE\_MISC\_TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag when you create a resource.</span></span><br/>                                                                                          |
| [<span data-ttu-id="e9cca-113">APIs de recursos de lado</span><span class="sxs-lookup"><span data-stu-id="e9cca-113">Tiled Resource APIs</span></span>](tiled-resource-apis.md)<br/>                               | <span data-ttu-id="e9cca-114">As APIs descritas nesta seção funcionam com os recursos de lado e o pool de blocos.</span><span class="sxs-lookup"><span data-stu-id="e9cca-114">The APIs described in this section work with tiled resources and tile pool.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="e9cca-115">Acesso ao pipeline para recursos lado a lado</span><span class="sxs-lookup"><span data-stu-id="e9cca-115">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)<br/> | <span data-ttu-id="e9cca-116">Os recursos do lado do xadrez podem ser usados em modos de exibição de recurso de sombreador (SRV), exibições de destino de renderização (RTV), exibições de estêncil de profundidade (DSV) e exibições de acesso não ordenado (UAV), bem como alguns pontos de ligação em que as exibições não são usadas, como associações de buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="e9cca-116">Tiled resources can be used in shader resource views (SRV), render target views (RTV), depth stencil views (DSV) and unordered access views (UAV), as well as some bind points where views aren't used, such as vertex buffer bindings.</span></span> <br/> |
| [<span data-ttu-id="e9cca-117">Recursos de azulejos recursos camadas</span><span class="sxs-lookup"><span data-stu-id="e9cca-117">Tiled resources features tiers</span></span>](tiled-resources-features-tiers.md)<br/>         | <span data-ttu-id="e9cca-118">O Direct3D 11,2 expõe os recursos com suporte de ladrilhos em duas camadas com os valores de [**\_ \_ \_ camada de recursos lado**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) -a-D3D11.</span><span class="sxs-lookup"><span data-stu-id="e9cca-118">Direct3D 11.2 exposes tiled resources support in two tiers with the [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) values.</span></span> <br/>                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="e9cca-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e9cca-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9cca-120">Recursos</span><span class="sxs-lookup"><span data-stu-id="e9cca-120">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





