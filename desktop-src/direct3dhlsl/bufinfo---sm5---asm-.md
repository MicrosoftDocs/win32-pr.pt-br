---
title: bufinfo (SM5-ASM)
description: Consultar a contagem de elementos em um buffer (mas não no buffer de constantes).
ms.assetid: 3A5C28F3-FE59-4C67-92AC-66B10E1D9692
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8dd33871aa5bd56db6e7375979c6d49f374b74
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988582"
---
# <a name="bufinfo-sm5---asm"></a><span data-ttu-id="8e77a-103">bufinfo (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="8e77a-103">bufinfo (sm5 - asm)</span></span>

<span data-ttu-id="8e77a-104">Consultar a contagem de elementos em um buffer (mas não no buffer de constantes).</span><span class="sxs-lookup"><span data-stu-id="8e77a-104">Query the element count on a buffer (but not the constant buffer).</span></span>



| <span data-ttu-id="8e77a-105">bufinfo dest \[ . Mask \] , srcResource</span><span class="sxs-lookup"><span data-stu-id="8e77a-105">bufinfo dest\[.mask\], srcResource</span></span> |
|------------------------------------|



 



| <span data-ttu-id="8e77a-106">Item</span><span class="sxs-lookup"><span data-stu-id="8e77a-106">Item</span></span>                                                                                                               | <span data-ttu-id="8e77a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e77a-107">Description</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e77a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="8e77a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="8e77a-109">\[no \] endereço dos resultados.</span><span class="sxs-lookup"><span data-stu-id="8e77a-109">\[in\] The address of the results.</span></span><br/>                                         |
| <span data-ttu-id="8e77a-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="8e77a-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="8e77a-111">\[no \] buffer, além de um buffer de constantes, em um SRV (t \# ) ou UAV (u \# ).</span><span class="sxs-lookup"><span data-stu-id="8e77a-111">\[in\] Buffer, other than a constant Buffer, in an SRV (t\#) or UAV (u\#).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8e77a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e77a-112">Remarks</span></span>

<span data-ttu-id="8e77a-113">Todos os componentes no *dest* recebem o número inteiro de elementos na exibição de recursos do sombreador s do buffer.</span><span class="sxs-lookup"><span data-stu-id="8e77a-113">All components in *dest* receive the integer number of elements in the buffer s shader resource view.</span></span> <span data-ttu-id="8e77a-114">O número de elementos depende dos parâmetros de exibição, como o formato de memória.</span><span class="sxs-lookup"><span data-stu-id="8e77a-114">The number of elements depends on the view parameters such as memory format.</span></span>

<span data-ttu-id="8e77a-115">Para um buffer tipado SRV ou UAV, o valor de retorno é o número de elementos na exibição (em que um elemento é uma unidade do formato digitado).</span><span class="sxs-lookup"><span data-stu-id="8e77a-115">For a typed buffer SRV or UAV, the return value is the number of elements in the view (where an element is one unit of the typed format).</span></span>

<span data-ttu-id="8e77a-116">Para um buffer bruto SRV ou UAV, o valor de retorno é o número de bytes na exibição.</span><span class="sxs-lookup"><span data-stu-id="8e77a-116">For a raw buffer SRV or UAV, the return value is the number of bytes in the view.</span></span>

<span data-ttu-id="8e77a-117">Para um buffer estruturado SRV ou UAV, o valor de retorno é o número de estruturas na exibição.</span><span class="sxs-lookup"><span data-stu-id="8e77a-117">For a structured buffer SRV or UAV, the return value is the number of structures in the view.</span></span>

<span data-ttu-id="8e77a-118">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="8e77a-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8e77a-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="8e77a-119">Vertex</span></span> | <span data-ttu-id="8e77a-120">Envoltória</span><span class="sxs-lookup"><span data-stu-id="8e77a-120">Hull</span></span> | <span data-ttu-id="8e77a-121">Domínio</span><span class="sxs-lookup"><span data-stu-id="8e77a-121">Domain</span></span> | <span data-ttu-id="8e77a-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="8e77a-122">Geometry</span></span> | <span data-ttu-id="8e77a-123">16x16</span><span class="sxs-lookup"><span data-stu-id="8e77a-123">Pixel</span></span> | <span data-ttu-id="8e77a-124">Computação</span><span class="sxs-lookup"><span data-stu-id="8e77a-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8e77a-125">X</span><span class="sxs-lookup"><span data-stu-id="8e77a-125">X</span></span>      | <span data-ttu-id="8e77a-126">X</span><span class="sxs-lookup"><span data-stu-id="8e77a-126">X</span></span>    | <span data-ttu-id="8e77a-127">X</span><span class="sxs-lookup"><span data-stu-id="8e77a-127">X</span></span>      | <span data-ttu-id="8e77a-128">X</span><span class="sxs-lookup"><span data-stu-id="8e77a-128">X</span></span>        | <span data-ttu-id="8e77a-129">X</span><span class="sxs-lookup"><span data-stu-id="8e77a-129">X</span></span>     | <span data-ttu-id="8e77a-130">X</span><span class="sxs-lookup"><span data-stu-id="8e77a-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8e77a-131">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="8e77a-131">Minimum Shader Model</span></span>

<span data-ttu-id="8e77a-132">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="8e77a-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="8e77a-133">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="8e77a-133">Shader Model</span></span>                                              | <span data-ttu-id="8e77a-134">Com suporte</span><span class="sxs-lookup"><span data-stu-id="8e77a-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8e77a-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8e77a-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8e77a-136">sim</span><span class="sxs-lookup"><span data-stu-id="8e77a-136">yes</span></span>       |
| [<span data-ttu-id="8e77a-137">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="8e77a-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8e77a-138">não</span><span class="sxs-lookup"><span data-stu-id="8e77a-138">no</span></span>        |
| [<span data-ttu-id="8e77a-139">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="8e77a-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8e77a-140">não</span><span class="sxs-lookup"><span data-stu-id="8e77a-140">no</span></span>        |
| [<span data-ttu-id="8e77a-141">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e77a-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8e77a-142">não</span><span class="sxs-lookup"><span data-stu-id="8e77a-142">no</span></span>        |
| [<span data-ttu-id="8e77a-143">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e77a-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8e77a-144">não</span><span class="sxs-lookup"><span data-stu-id="8e77a-144">no</span></span>        |
| [<span data-ttu-id="8e77a-145">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e77a-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8e77a-146">não</span><span class="sxs-lookup"><span data-stu-id="8e77a-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8e77a-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e77a-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e77a-148">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e77a-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





