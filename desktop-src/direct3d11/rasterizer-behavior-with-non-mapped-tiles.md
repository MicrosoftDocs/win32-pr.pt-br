---
title: Comportamento de rasterizador com blocos não mapeados
description: Esta seção descreve o comportamento de rasterizador com blocos não mapeados.
ms.assetid: 3477A621-7051-4585-AB58-523EE64CDC5C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54230321f4286b92a3444e3f74167ee7b8711c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104988516"
---
# <a name="rasterizer-behavior-with-non-mapped-tiles"></a><span data-ttu-id="ea7d1-103">Comportamento de rasterizador com blocos não mapeados</span><span class="sxs-lookup"><span data-stu-id="ea7d1-103">Rasterizer behavior with non-mapped tiles</span></span>

<span data-ttu-id="ea7d1-104">Esta seção descreve o comportamento de rasterizador com blocos não mapeados.</span><span class="sxs-lookup"><span data-stu-id="ea7d1-104">This section describes rasterizer behavior with non-mapped tiles.</span></span>

## <a name="depthstencilview"></a><span data-ttu-id="ea7d1-105">DepthStencilView</span><span class="sxs-lookup"><span data-stu-id="ea7d1-105">DepthStencilView</span></span>

<span data-ttu-id="ea7d1-106">O comportamento de leituras e gravações do modo de exibição de estêncil de profundidade (DSV) depende do nível de suporte de hardware.</span><span class="sxs-lookup"><span data-stu-id="ea7d1-106">Behavior of depth stencil view (DSV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="ea7d1-107">Para obter uma análise dos requisitos, consulte comportamento geral de leitura e gravação para [recursos](tiled-resources-features-tiers.md)de divisão de recursos.</span><span class="sxs-lookup"><span data-stu-id="ea7d1-107">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span>

<span data-ttu-id="ea7d1-108">Aqui está o comportamento ideal:</span><span class="sxs-lookup"><span data-stu-id="ea7d1-108">Here is the ideal behavior:</span></span>

<span data-ttu-id="ea7d1-109">Se um bloco não estiver mapeado no DepthStencilView, o valor de retorno de profundidade de leitura será 0, o que será enviado, em seguida, para todas as operações configuradas para o valor de leitura de profundidade.</span><span class="sxs-lookup"><span data-stu-id="ea7d1-109">If a tile isn't mapped in the DepthStencilView, the return value from reading depth is 0, which is then fed into whatever operations are configured for the depth read value.</span></span> <span data-ttu-id="ea7d1-110">Gravações para blocos de profundidade ausentes serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="ea7d1-110">Writes to the missing depth tile are dropped.</span></span> <span data-ttu-id="ea7d1-111">Essa definição ideal para o tratamento de gravação não é exigida pelo [nível 2](tier-2.md); as gravações em blocos não mapeados podem acabar em um cache que pode ser coletado pelas leituras subsequentes.</span><span class="sxs-lookup"><span data-stu-id="ea7d1-111">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="rendertargetview"></a><span data-ttu-id="ea7d1-112">RenderTargetView</span><span class="sxs-lookup"><span data-stu-id="ea7d1-112">RenderTargetView</span></span>

<span data-ttu-id="ea7d1-113">O comportamento leituras e gravações de modo de exibição de destino de renderização (RTV) depende do nível de suporte de hardware.</span><span class="sxs-lookup"><span data-stu-id="ea7d1-113">Behavior of render target view (RTV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="ea7d1-114">Para obter uma análise dos requisitos, consulte comportamento geral de leitura e gravação para [recursos](tiled-resources-features-tiers.md)de divisão de recursos.</span><span class="sxs-lookup"><span data-stu-id="ea7d1-114">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span>

<span data-ttu-id="ea7d1-115">Em todas as implementações, diferentes RTVs (e DSV) associados ao mesmo tempo podem ter diferentes áreas mapeadas versus não mapeadas e podem ter diferentes formatos de superfície dimensionados (o que significa formas de bloco diferentes).</span><span class="sxs-lookup"><span data-stu-id="ea7d1-115">On all implementations, different RTVs (and DSV) bound simultaneously can have different areas mapped versus non-mapped and can have different sized surface formats (which means different tile shapes).</span></span>

<span data-ttu-id="ea7d1-116">Aqui está o comportamento ideal:</span><span class="sxs-lookup"><span data-stu-id="ea7d1-116">Here is the ideal behavior:</span></span>

<span data-ttu-id="ea7d1-117">Leituras de RTVs retornam 0 em blocos ausentes e gravações são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="ea7d1-117">Reads from RTVs return 0 in missing tiles and writes are dropped.</span></span> <span data-ttu-id="ea7d1-118">Essa definição ideal para o tratamento de gravação não é exigida pelo [nível 2](tier-2.md); as gravações em blocos não mapeados podem acabar em um cache que pode ser coletado pelas leituras subsequentes.</span><span class="sxs-lookup"><span data-stu-id="ea7d1-118">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea7d1-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ea7d1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea7d1-120">Acesso ao pipeline para recursos lado a lado</span><span class="sxs-lookup"><span data-stu-id="ea7d1-120">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




