---
title: SV_TessFactor
description: Define o valor do mosaico em cada borda de um patch.
ms.assetid: 970ff744-da5b-4933-866c-dd38b85fb48d
keywords:
- SV_TessFactor HLSL
topic_type:
- apiref
api_name:
- SV_TessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 308034fe607283ef9f1213cca1cabb4a7229765e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118891"
---
# <a name="sv_tessfactor"></a><span data-ttu-id="4e5cc-104">\_TESSFACTOR VA</span><span class="sxs-lookup"><span data-stu-id="4e5cc-104">SV\_TessFactor</span></span>

<span data-ttu-id="4e5cc-105">Define o valor do mosaico em cada borda de um patch.</span><span class="sxs-lookup"><span data-stu-id="4e5cc-105">Defines the tessellation amount on each edge of a patch.</span></span>

## <a name="type"></a><span data-ttu-id="4e5cc-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="4e5cc-106">Type</span></span>



|  <span data-ttu-id="4e5cc-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="4e5cc-107">Type</span></span>          |  <span data-ttu-id="4e5cc-108">Topologia de entrada</span><span class="sxs-lookup"><span data-stu-id="4e5cc-108">Input topology</span></span>              |
|------------|----------------|
| <span data-ttu-id="4e5cc-109">float \[ 4\]</span><span class="sxs-lookup"><span data-stu-id="4e5cc-109">float\[4\]</span></span> | <span data-ttu-id="4e5cc-110">patch quádruplo</span><span class="sxs-lookup"><span data-stu-id="4e5cc-110">quad patch</span></span>     |
| <span data-ttu-id="4e5cc-111">float \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="4e5cc-111">float\[3\]</span></span> | <span data-ttu-id="4e5cc-112">Tri patch</span><span class="sxs-lookup"><span data-stu-id="4e5cc-112">tri patch</span></span>      |
| <span data-ttu-id="4e5cc-113">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="4e5cc-113">float\[2\]</span></span> | <span data-ttu-id="4e5cc-114">isoline</span><span class="sxs-lookup"><span data-stu-id="4e5cc-114">isoline</span></span>        |



 

<span data-ttu-id="4e5cc-115">Os fatores de mosaico devem ser declarados como uma matriz; Eles não podem ser empacotados em um único vetor.</span><span class="sxs-lookup"><span data-stu-id="4e5cc-115">Tessellation factors must be declared as an array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e5cc-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e5cc-116">Remarks</span></span>

<span data-ttu-id="4e5cc-117">O valor do fator de mosaico deve ser definido durante a função constante patch do sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="4e5cc-117">The value for tessellation factor must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="4e5cc-118">Valor de saída necessário para o sombreador envoltória se estiver usando patches Quad ou tri.</span><span class="sxs-lookup"><span data-stu-id="4e5cc-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="4e5cc-119">Esse valor também é um valor de entrada necessário para o sombreador de domínio corresponder às assinaturas de dados de constante de patch entre os estágios de mosaico.</span><span class="sxs-lookup"><span data-stu-id="4e5cc-119">This value is also a required input value for the domain shader to match the patch-constant data signatures between the tessellation stages.</span></span>

<span data-ttu-id="4e5cc-120">Para um Isoline, o primeiro valor em VA \_ TessFactor é o fator de mosaico de densidade de linha, o segundo valor é o fator de mosaico de detalhes de linha.</span><span class="sxs-lookup"><span data-stu-id="4e5cc-120">For an isoline, the first value in SV\_TessFactor is the line-density tessellation factor, the second value is the line-detail tessellation factor.</span></span>

### <a name="tri-patch-tessellation-factors"></a><span data-ttu-id="4e5cc-121">Três fatores de mosaico de patch</span><span class="sxs-lookup"><span data-stu-id="4e5cc-121">Tri Patch Tessellation Factors</span></span>

<span data-ttu-id="4e5cc-122">O primeiro componente fornece o fator geométrica para a borda u = = 0 do patch.</span><span class="sxs-lookup"><span data-stu-id="4e5cc-122">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="4e5cc-123">O segundo componente fornece o fator geométrica para a borda v = = 0 do patch.</span><span class="sxs-lookup"><span data-stu-id="4e5cc-123">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="4e5cc-124">O terceiro componente fornece o fator geométrica para a borda w = = 0 do patch.</span><span class="sxs-lookup"><span data-stu-id="4e5cc-124">The third component provides the tesselation factor for the w==0 edge of the patch.</span></span>

### <a name="quad-patch-tessellation-factors"></a><span data-ttu-id="4e5cc-125">Fatores de mosaico de patch quádruplo</span><span class="sxs-lookup"><span data-stu-id="4e5cc-125">Quad Patch Tessellation Factors</span></span>

<span data-ttu-id="4e5cc-126">O primeiro componente fornece o fator geométrica para a borda u = = 0 do patch.</span><span class="sxs-lookup"><span data-stu-id="4e5cc-126">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="4e5cc-127">O segundo componente fornece o fator geométrica para a borda v = = 0 do patch.</span><span class="sxs-lookup"><span data-stu-id="4e5cc-127">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="4e5cc-128">O terceiro componente fornece o fator geométrica para a borda u = = 1 do patch.</span><span class="sxs-lookup"><span data-stu-id="4e5cc-128">The third component provides the tesselation factor for the u==1 edge of the patch.</span></span> <span data-ttu-id="4e5cc-129">O quarto componente fornece o fator geométrica para a borda v = = 1 do patch.</span><span class="sxs-lookup"><span data-stu-id="4e5cc-129">The fourth component provides the tesselation factor for the v==1 edge of the patch.</span></span> <span data-ttu-id="4e5cc-130">A ordenação das bordas é no sentido horário, começando na borda u = = 0, que é o lado esquerdo do patch e da borda v = = 0, que é a parte superior do patch.</span><span class="sxs-lookup"><span data-stu-id="4e5cc-130">The ordering of the edges is clockwise, starting from the u==0 edge, which is the left side of the patch, and from the v==0 edge, which is the top of the patch.</span></span>

<span data-ttu-id="4e5cc-131">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="4e5cc-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="4e5cc-132">Vértice</span><span class="sxs-lookup"><span data-stu-id="4e5cc-132">Vertex</span></span> | <span data-ttu-id="4e5cc-133">Envoltória</span><span class="sxs-lookup"><span data-stu-id="4e5cc-133">Hull</span></span> | <span data-ttu-id="4e5cc-134">Domínio</span><span class="sxs-lookup"><span data-stu-id="4e5cc-134">Domain</span></span> | <span data-ttu-id="4e5cc-135">Geometry</span><span class="sxs-lookup"><span data-stu-id="4e5cc-135">Geometry</span></span> | <span data-ttu-id="4e5cc-136">16x16</span><span class="sxs-lookup"><span data-stu-id="4e5cc-136">Pixel</span></span> | <span data-ttu-id="4e5cc-137">Computação</span><span class="sxs-lookup"><span data-stu-id="4e5cc-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="4e5cc-138">x</span><span class="sxs-lookup"><span data-stu-id="4e5cc-138">x</span></span>    | <span data-ttu-id="4e5cc-139">x</span><span class="sxs-lookup"><span data-stu-id="4e5cc-139">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="4e5cc-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e5cc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e5cc-141">Semântica</span><span class="sxs-lookup"><span data-stu-id="4e5cc-141">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="4e5cc-142">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4e5cc-142">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




