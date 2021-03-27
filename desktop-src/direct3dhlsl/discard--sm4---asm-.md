---
title: descartar (sm4-ASM)
description: Sinaliza condicionalmente os resultados do sombreador de pixel a serem descartados quando o fim do programa for atingido.
ms.assetid: 566C4A9A-B32A-4AA6-A888-70F6965B1B5A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d98365ae6d80710f15cf7204f98d810be30a13
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103916871"
---
# <a name="discard-sm4---asm"></a><span data-ttu-id="bbc5b-103">descartar (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="bbc5b-103">discard (sm4 - asm)</span></span>

<span data-ttu-id="bbc5b-104">Sinaliza condicionalmente os resultados do sombreador de pixel a serem descartados quando o fim do programa for atingido.</span><span class="sxs-lookup"><span data-stu-id="bbc5b-104">Conditionally flag results of Pixel Shader to be discarded when the end of the program is reached.</span></span>



| <span data-ttu-id="bbc5b-105">descartar { \_ z </span><span class="sxs-lookup"><span data-stu-id="bbc5b-105">discard{\_z</span></span>\|<span data-ttu-id="bbc5b-106">\_NZ} src0. Select \_ componente</span><span class="sxs-lookup"><span data-stu-id="bbc5b-106">\_nz} src0.select\_component</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="bbc5b-107">Item</span><span class="sxs-lookup"><span data-stu-id="bbc5b-107">Item</span></span>                                                            | <span data-ttu-id="bbc5b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbc5b-108">Description</span></span>                                                                                       |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc5b-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="bbc5b-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="bbc5b-110">\[no \] valor que determina se deve-se descartar o pixel atual que está sendo processado.</span><span class="sxs-lookup"><span data-stu-id="bbc5b-110">\[in\] The value that determines whether to discard the current pixel being processed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bbc5b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbc5b-111">Remarks</span></span>

<span data-ttu-id="bbc5b-112">Essa instrução sinaliza o pixel atual como encerrado, enquanto continua a execução, para que outros pixels em execução em paralelo possam obter derivações, se necessário.</span><span class="sxs-lookup"><span data-stu-id="bbc5b-112">This instruction flags the current pixel as terminated, while continuing execution, so that other pixels executing in parallel may obtain derivatives if necessary.</span></span> <span data-ttu-id="bbc5b-113">Embora a execução Continue, toda a saída do sombreador de pixel grava antes ou depois que a instrução de **descarte** é descartada.</span><span class="sxs-lookup"><span data-stu-id="bbc5b-113">Even though execution continues, all Pixel Shader output writes before or after the **discard** instruction are discarded.</span></span>

<span data-ttu-id="bbc5b-114">Para **descarte \_ z**, se todos os bits no *\_ componente src0. Select* forem zero, o pixel será Descartado.</span><span class="sxs-lookup"><span data-stu-id="bbc5b-114">For **discard\_z**, if all bits in *src0.select\_component* are zero, then the pixel is discarded.</span></span>

<span data-ttu-id="bbc5b-115">Para **descartar \_ NZ**, se qualquer um dos bits no *\_ componente src0. Select* for diferente de zero, o pixel será Descartado.</span><span class="sxs-lookup"><span data-stu-id="bbc5b-115">For **discard\_nz**, if any bits in *src0.select\_component* are nonzero, then the pixel is discarded.</span></span>

<span data-ttu-id="bbc5b-116">Além disso, a instrução de **descarte** pode estar presente dentro de qualquer construção de controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="bbc5b-116">In addition, the **discard** instruction can be present inside any flow control construct.</span></span>

<span data-ttu-id="bbc5b-117">Várias instruções de **descarte** podem estar presentes em um sombreador e, se alguma for executada, o pixel será encerrado.</span><span class="sxs-lookup"><span data-stu-id="bbc5b-117">Multiple **discard** instructions may be present in a Shader, and if any is executed, the pixel is terminated.</span></span>

<span data-ttu-id="bbc5b-118">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="bbc5b-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bbc5b-119">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="bbc5b-119">Vertex Shader</span></span> | <span data-ttu-id="bbc5b-120">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="bbc5b-120">Geometry Shader</span></span> | <span data-ttu-id="bbc5b-121">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="bbc5b-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="bbc5b-122">x</span><span class="sxs-lookup"><span data-stu-id="bbc5b-122">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bbc5b-123">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="bbc5b-123">Minimum Shader Model</span></span>

<span data-ttu-id="bbc5b-124">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bbc5b-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bbc5b-125">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="bbc5b-125">Shader Model</span></span>                                              | <span data-ttu-id="bbc5b-126">Com suporte</span><span class="sxs-lookup"><span data-stu-id="bbc5b-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bbc5b-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="bbc5b-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bbc5b-128">sim</span><span class="sxs-lookup"><span data-stu-id="bbc5b-128">yes</span></span>       |
| [<span data-ttu-id="bbc5b-129">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="bbc5b-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bbc5b-130">sim</span><span class="sxs-lookup"><span data-stu-id="bbc5b-130">yes</span></span>       |
| [<span data-ttu-id="bbc5b-131">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="bbc5b-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bbc5b-132">sim</span><span class="sxs-lookup"><span data-stu-id="bbc5b-132">yes</span></span>       |
| [<span data-ttu-id="bbc5b-133">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bbc5b-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bbc5b-134">não</span><span class="sxs-lookup"><span data-stu-id="bbc5b-134">no</span></span>        |
| [<span data-ttu-id="bbc5b-135">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bbc5b-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bbc5b-136">não</span><span class="sxs-lookup"><span data-stu-id="bbc5b-136">no</span></span>        |
| [<span data-ttu-id="bbc5b-137">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bbc5b-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bbc5b-138">não</span><span class="sxs-lookup"><span data-stu-id="bbc5b-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bbc5b-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bbc5b-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbc5b-140">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bbc5b-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





