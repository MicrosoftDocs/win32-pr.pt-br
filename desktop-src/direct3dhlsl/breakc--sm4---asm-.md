---
title: breakc (sm4-ASM)
description: Move condicionalmente o ponto de execução para a instrução após o próximo loop Endou endswitch.
ms.assetid: 5735EF88-1E8C-4142-8442-9328D78999A7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a1c859f7d1e0ee6368f5b9984775ef9bfaba1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365243"
---
# <a name="breakc-sm4---asm"></a><span data-ttu-id="95cd8-103">breakc (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="95cd8-103">breakc (sm4 - asm)</span></span>

<span data-ttu-id="95cd8-104">Move condicionalmente o ponto de execução para a instrução após o próximo [loop](endloop--sm4---asm-.md) Endou [endswitch](endswitch--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="95cd8-104">Conditionally moves the point of execution to the instruction after the next [endloop](endloop--sm4---asm-.md) or [endswitch](endswitch--sm4---asm-.md).</span></span>



| <span data-ttu-id="95cd8-105">breakc { \_ z </span><span class="sxs-lookup"><span data-stu-id="95cd8-105">breakc{\_z</span></span>\|<span data-ttu-id="95cd8-106">\_NZ} src0. Select \_ componente</span><span class="sxs-lookup"><span data-stu-id="95cd8-106">\_nz} src0.select\_component</span></span> |
|------------------------------------------|



 



| <span data-ttu-id="95cd8-107">Item</span><span class="sxs-lookup"><span data-stu-id="95cd8-107">Item</span></span>                                                            | <span data-ttu-id="95cd8-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="95cd8-108">Description</span></span>                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="95cd8-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="95cd8-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="95cd8-110">\[no \] componente no qual testar a condição.</span><span class="sxs-lookup"><span data-stu-id="95cd8-110">\[in\] The component on which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="95cd8-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="95cd8-111">Remarks</span></span>

<span data-ttu-id="95cd8-112">O formato do token contém o deslocamento da instrução **ENDLOOP** correspondente no sombreador como uma conveniência.</span><span class="sxs-lookup"><span data-stu-id="95cd8-112">The token format contains the offset of the corresponding **endloop** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="95cd8-113">O exemplo a seguir mostra a instrução **breakc** .</span><span class="sxs-lookup"><span data-stu-id="95cd8-113">The following example shows the **breakc** instruction.</span></span>


```
                loop
                    // example of termination condition
                    breakc_z  r0.x // break if all bits in r0.x are 0
                    breakc_nz r1.x // break if any bit in r1.x is nonzero
                    ...
                endloop

```



<span data-ttu-id="95cd8-114">Essa instrução deve aparecer em um **loop** / **ENDLOOP** ou **alternar** / **endswitch**.</span><span class="sxs-lookup"><span data-stu-id="95cd8-114">This instruction must appear within a **loop**/**endloop** or **switch**/**endswitch**.</span></span>

<span data-ttu-id="95cd8-115">O registro de 32 bits fornecido pelo *src0* é testado em um nível de bit.</span><span class="sxs-lookup"><span data-stu-id="95cd8-115">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="95cd8-116">Se algum bit for diferente de zero, **breakc \_ NZ** executará a interrupção.</span><span class="sxs-lookup"><span data-stu-id="95cd8-116">If any bit is nonzero, **breakc\_nz** will perform the break.</span></span> <span data-ttu-id="95cd8-117">Se todos os bits forem zero, o **breakc \_ z** executará a interrupção.</span><span class="sxs-lookup"><span data-stu-id="95cd8-117">If all bits are zero, **breakc\_z** will perform the break.</span></span>

<span data-ttu-id="95cd8-118">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="95cd8-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="95cd8-119">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="95cd8-119">Vertex Shader</span></span> | <span data-ttu-id="95cd8-120">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="95cd8-120">Geometry Shader</span></span> | <span data-ttu-id="95cd8-121">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="95cd8-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="95cd8-122">x</span><span class="sxs-lookup"><span data-stu-id="95cd8-122">x</span></span>             | <span data-ttu-id="95cd8-123">x</span><span class="sxs-lookup"><span data-stu-id="95cd8-123">x</span></span>               | <span data-ttu-id="95cd8-124">x</span><span class="sxs-lookup"><span data-stu-id="95cd8-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="95cd8-125">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="95cd8-125">Minimum Shader Model</span></span>

<span data-ttu-id="95cd8-126">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="95cd8-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="95cd8-127">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="95cd8-127">Shader Model</span></span>                                              | <span data-ttu-id="95cd8-128">Com suporte</span><span class="sxs-lookup"><span data-stu-id="95cd8-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="95cd8-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="95cd8-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="95cd8-130">sim</span><span class="sxs-lookup"><span data-stu-id="95cd8-130">yes</span></span>       |
| [<span data-ttu-id="95cd8-131">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="95cd8-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="95cd8-132">sim</span><span class="sxs-lookup"><span data-stu-id="95cd8-132">yes</span></span>       |
| [<span data-ttu-id="95cd8-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="95cd8-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="95cd8-134">sim</span><span class="sxs-lookup"><span data-stu-id="95cd8-134">yes</span></span>       |
| [<span data-ttu-id="95cd8-135">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="95cd8-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="95cd8-136">não</span><span class="sxs-lookup"><span data-stu-id="95cd8-136">no</span></span>        |
| [<span data-ttu-id="95cd8-137">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="95cd8-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="95cd8-138">não</span><span class="sxs-lookup"><span data-stu-id="95cd8-138">no</span></span>        |
| [<span data-ttu-id="95cd8-139">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="95cd8-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="95cd8-140">não</span><span class="sxs-lookup"><span data-stu-id="95cd8-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="95cd8-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="95cd8-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95cd8-142">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="95cd8-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





