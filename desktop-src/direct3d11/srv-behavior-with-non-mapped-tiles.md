---
title: Comportamento de SRV com blocos não mapeados
description: O comportamento de leituras de modo de exibição (SRV) de recurso de sombreador que envolve blocos não mapeados depende do nível de suporte de hardware.
ms.assetid: 9B720BEE-AB0C-4B75-92AD-3F382A107D48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e086a4db869c3204fc560e64002ba04e8bd8ba9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159282"
---
# <a name="srv-behavior-with-non-mapped-tiles"></a><span data-ttu-id="2a635-103">Comportamento de SRV com blocos não mapeados</span><span class="sxs-lookup"><span data-stu-id="2a635-103">SRV behavior with non-mapped tiles</span></span>

<span data-ttu-id="2a635-104">O comportamento de leituras de modo de exibição (SRV) de recurso de sombreador que envolve blocos não mapeados depende do nível de suporte de hardware.</span><span class="sxs-lookup"><span data-stu-id="2a635-104">Behavior of shader resource view (SRV) reads that involve non-mapped tiles depends on the level of hardware support.</span></span> <span data-ttu-id="2a635-105">Para obter uma análise dos requisitos, confira comportamento de leitura para [camadas de recursos de recursos de lado](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="2a635-105">For a breakdown of requirements, see read behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span> <span data-ttu-id="2a635-106">Esta seção resume o comportamento ideal, que o [Nível 2](tier-2.md) requer.</span><span class="sxs-lookup"><span data-stu-id="2a635-106">This section summarizes the ideal behavior, which [Tier 2](tier-2.md) requires.</span></span>

<span data-ttu-id="2a635-107">Considere uma operação de filtro de textura que lê de um conjunto de texels em um SRV.</span><span class="sxs-lookup"><span data-stu-id="2a635-107">Consider a texture filter operation that reads from a set of texels in an SRV.</span></span> <span data-ttu-id="2a635-108">Texels que se enquadram em blocos não mapeados contribuem com 0 em todos os componentes sem perder o formato (e o padrão para componentes que estão faltando) para a operação de filtro geral junto com contribuições de texels mapeadas.</span><span class="sxs-lookup"><span data-stu-id="2a635-108">Texels that fall on non-mapped tiles contribute 0 in all non-missing components of the format (and the default for missing components) into the overall filter operation alongside contributions from mapped texels.</span></span> <span data-ttu-id="2a635-109">Os texels são todos ponderados e combinados juntos independentemente dos dados serem provenientes de blocos mapeados ou não mapeados.</span><span class="sxs-lookup"><span data-stu-id="2a635-109">The texels are all weighted and combined together independent of whether the data came from mapped or non-mapped tiles.</span></span>

<span data-ttu-id="2a635-110">Alguns hardwares de nível de [camada 2](tier-2.md) de primeira geração não atendem a esse requisito de especificação e retorna o 0 com os padrões descritos anteriormente como o resultado de filtro geral se qualquer texels (com peso diferente de zero) cair em blocos não mapeados.</span><span class="sxs-lookup"><span data-stu-id="2a635-110">Some first generation [Tier 2](tier-2.md) level hardware does not meet this spec requirement and returns the 0 with defaults described preceding as the overall filter result if any texels (with nonzero weight) fall on non-mapped tiles.</span></span> <span data-ttu-id="2a635-111">O requisito de incluir todos os texels no filtro (peso diferente de zero) não poderá faltar em nenhum outro hardware.</span><span class="sxs-lookup"><span data-stu-id="2a635-111">No other hardware will be allowed to miss the requirement to include all (nonzero weight) texels in the filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a635-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a635-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a635-113">Acesso ao pipeline para recursos lado a lado</span><span class="sxs-lookup"><span data-stu-id="2a635-113">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




