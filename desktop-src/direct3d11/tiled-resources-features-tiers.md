---
title: Recursos de azulejos recursos camadas
description: O Direct3D 11,2 expõe os recursos com suporte de ladrilhos em duas camadas com os valores de camada de recursos lado-a-D3D11 \_ \_ \_ .
ms.assetid: E6A6565B-079B-47DB-A80C-CA5B5413BA32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2282cde1dfc8c4249672d18e303a4529338d4fbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916026"
---
# <a name="tiled-resources-features-tiers"></a><span data-ttu-id="70028-103">Recursos de azulejos recursos camadas</span><span class="sxs-lookup"><span data-stu-id="70028-103">Tiled resources features tiers</span></span>

<span data-ttu-id="70028-104">O Direct3D 11,2 expõe os recursos com suporte de ladrilhos em duas camadas com os valores de [**\_ \_ \_ camada de recursos lado**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) -a-D3D11.</span><span class="sxs-lookup"><span data-stu-id="70028-104">Direct3D 11.2 exposes tiled resources support in two tiers with the [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) values.</span></span>

<span data-ttu-id="70028-105">Para consultar se o hardware e o driver dão suporte a recursos de lado e em qual nível de camada, passe o valor de [**D3D11 do \_ recurso \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) para o parâmetro *Feature* de [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="70028-105">To query whether the hardware and driver support tiled resources and at what tier level, pass the [**D3D11\_FEATURE\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) value to the *Feature* parameter of [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport).</span></span> <span data-ttu-id="70028-106">Além disso, passe um ponteiro para a estrutura [**D3D11 de \_ dados do recurso \_ \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) para o parâmetro *pFeatureSupportData* e passe o tamanho da estrutura D3D11 D3D11 de **\_ \_ dados de \_ \_ recursos** OPTIONS1 para o parâmetro *FeatureSupportDataSize* .</span><span class="sxs-lookup"><span data-stu-id="70028-106">Also, pass a pointer to the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) structure to the *pFeatureSupportData* parameter, and pass the size of the **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1** structure to the *FeatureSupportDataSize* parameter.</span></span> <span data-ttu-id="70028-107">**CheckFeatureSupport** retorna o nível de camada como um valor de [**camada de recursos com lado de D3D11 \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) no membro **TiledResourcesTier** de **D3D11 de dados de \_ recursos \_ \_ D3D11 \_ OPTIONS1**.</span><span class="sxs-lookup"><span data-stu-id="70028-107">**CheckFeatureSupport** returns the tier level as a [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) value in the **TiledResourcesTier** member of **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**.</span></span>

<span data-ttu-id="70028-108">Esta seção descreve essas duas camadas.</span><span class="sxs-lookup"><span data-stu-id="70028-108">This section describes these two tiers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="70028-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="70028-109">In this section</span></span>



| <span data-ttu-id="70028-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="70028-110">Topic</span></span>                           | <span data-ttu-id="70028-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="70028-111">Description</span></span>                                       |
|---------------------------------|---------------------------------------------------|
| [<span data-ttu-id="70028-112">Camada 1</span><span class="sxs-lookup"><span data-stu-id="70028-112">Tier 1</span></span>](tier-1.md)<br/> | <span data-ttu-id="70028-113">Esta seção descreve o suporte de nível 1.</span><span class="sxs-lookup"><span data-stu-id="70028-113">This section describes tier 1 support.</span></span><br/> |
| [<span data-ttu-id="70028-114">Camada 2</span><span class="sxs-lookup"><span data-stu-id="70028-114">Tier 2</span></span>](tier-2.md)<br/> | <span data-ttu-id="70028-115">Esta seção descreve o suporte de camada 2.</span><span class="sxs-lookup"><span data-stu-id="70028-115">This section describes tier 2 support.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="70028-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70028-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70028-117">Recursos em ladrilho</span><span class="sxs-lookup"><span data-stu-id="70028-117">Tiled resources</span></span>](tiled-resources.md)
</dt> </dl>

 

 





