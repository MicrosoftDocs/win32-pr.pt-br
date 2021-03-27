---
title: chamada (sm4-ASM)
description: Chama uma sub-rotina marcada por onde o rótulo l \ aparece no programa.
ms.assetid: D6B7C52D-2CF7-44DB-81E3-2945477EF94A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dac86fa52140968443f01050cebc57718fea420
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638868"
---
# <a name="call-sm4---asm"></a><span data-ttu-id="efb7a-103">chamada (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="efb7a-103">call (sm4 - asm)</span></span>

<span data-ttu-id="efb7a-104">Chama uma sub-rotina marcada por onde o rótulo **l \#** aparece no programa.</span><span class="sxs-lookup"><span data-stu-id="efb7a-104">Calls a subroutine marked by where the label **l\#** appears in the program.</span></span>



| <span data-ttu-id="efb7a-105">chamar l\#</span><span class="sxs-lookup"><span data-stu-id="efb7a-105">call l\#</span></span> |
|----------|



 



| <span data-ttu-id="efb7a-106">Item</span><span class="sxs-lookup"><span data-stu-id="efb7a-106">Item</span></span>                                                       | <span data-ttu-id="efb7a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="efb7a-107">Description</span></span>                                    |
|------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="efb7a-108"><span id="l_"></span><span id="L_"></span>*debug\#*</span><span class="sxs-lookup"><span data-stu-id="efb7a-108"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/> | <span data-ttu-id="efb7a-109">\[no \] rótulo da sub-rotina.</span><span class="sxs-lookup"><span data-stu-id="efb7a-109">\[in\] The label of the subroutine.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="efb7a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="efb7a-110">Remarks</span></span>

<span data-ttu-id="efb7a-111">Quando uma [RET](ret--sm4---asm-.md) é encontrada, retorna a execução para a instrução após essa chamada.</span><span class="sxs-lookup"><span data-stu-id="efb7a-111">When a [ret](ret--sm4---asm-.md) is encountered, return execution to the instruction after this call.</span></span>

<span data-ttu-id="efb7a-112">O formato do token contém o deslocamento do rótulo correspondente no sombreador como uma conveniência.</span><span class="sxs-lookup"><span data-stu-id="efb7a-112">The token format contains the offset of the corresponding label in the Shader as a convenience.</span></span>

<span data-ttu-id="efb7a-113">O exemplo a seguir mostra a instrução de chamada.</span><span class="sxs-lookup"><span data-stu-id="efb7a-113">The following example shows the call instruction.</span></span>


```
                ...
                call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret
```



### <a name="restrictions"></a><span data-ttu-id="efb7a-114">Restrições</span><span class="sxs-lookup"><span data-stu-id="efb7a-114">Restrictions</span></span>

-   <span data-ttu-id="efb7a-115">As sub-rotinas podem aninhar 32 de profundidade.</span><span class="sxs-lookup"><span data-stu-id="efb7a-115">Subroutines can nest 32 deep.</span></span>
-   <span data-ttu-id="efb7a-116">A pilha de endereços de retorno é gerenciada de forma transparente pela implementação.</span><span class="sxs-lookup"><span data-stu-id="efb7a-116">The return address stack is managed transparently by the implementation.</span></span>
-   <span data-ttu-id="efb7a-117">Se já houver entradas 32 na pilha de endereços de retorno e uma **chamada** for emitida, a chamada será ignorada.</span><span class="sxs-lookup"><span data-stu-id="efb7a-117">If there are already 32 entries on the return address stack and a **call** is issued, the call is skipped over.</span></span>
-   <span data-ttu-id="efb7a-118">Não há nenhuma pilha de parâmetros automática.</span><span class="sxs-lookup"><span data-stu-id="efb7a-118">There is no automatic parameter stack.</span></span> <span data-ttu-id="efb7a-119">O aplicativo pode usar uma matriz de registro temporário indexável (x \# \[ \] ) para implementar manualmente uma pilha.</span><span class="sxs-lookup"><span data-stu-id="efb7a-119">The application can use an indexable temporary register array (x\#\[\]) to manually implement a stack.</span></span> <span data-ttu-id="efb7a-120">No entanto, os endereços de retorno da chamada de sub-rotina não são visíveis e são ortogonal a qualquer gerenciamento de pilha manual feito pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="efb7a-120">However, the subroutine call return addresses are not visible and are orthogonal to any manual stack management done by the application.</span></span>
-   <span data-ttu-id="efb7a-121">A indexação do *parâmetro \# l* não é permitida.</span><span class="sxs-lookup"><span data-stu-id="efb7a-121">Indexing of the *l\#* parameter is not permitted.</span></span>
-   <span data-ttu-id="efb7a-122">Recursão não é permitida.</span><span class="sxs-lookup"><span data-stu-id="efb7a-122">Recursion is not permitted.</span></span>

<span data-ttu-id="efb7a-123">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="efb7a-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="efb7a-124">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="efb7a-124">Vertex Shader</span></span> | <span data-ttu-id="efb7a-125">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="efb7a-125">Geometry Shader</span></span> | <span data-ttu-id="efb7a-126">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="efb7a-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="efb7a-127">x</span><span class="sxs-lookup"><span data-stu-id="efb7a-127">x</span></span>             | <span data-ttu-id="efb7a-128">x</span><span class="sxs-lookup"><span data-stu-id="efb7a-128">x</span></span>               | <span data-ttu-id="efb7a-129">x</span><span class="sxs-lookup"><span data-stu-id="efb7a-129">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="efb7a-130">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="efb7a-130">Minimum Shader Model</span></span>

<span data-ttu-id="efb7a-131">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="efb7a-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="efb7a-132">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="efb7a-132">Shader Model</span></span>                                              | <span data-ttu-id="efb7a-133">Com suporte</span><span class="sxs-lookup"><span data-stu-id="efb7a-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="efb7a-134">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="efb7a-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="efb7a-135">sim</span><span class="sxs-lookup"><span data-stu-id="efb7a-135">yes</span></span>       |
| [<span data-ttu-id="efb7a-136">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="efb7a-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="efb7a-137">sim</span><span class="sxs-lookup"><span data-stu-id="efb7a-137">yes</span></span>       |
| [<span data-ttu-id="efb7a-138">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="efb7a-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="efb7a-139">sim</span><span class="sxs-lookup"><span data-stu-id="efb7a-139">yes</span></span>       |
| [<span data-ttu-id="efb7a-140">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="efb7a-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="efb7a-141">não</span><span class="sxs-lookup"><span data-stu-id="efb7a-141">no</span></span>        |
| [<span data-ttu-id="efb7a-142">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="efb7a-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="efb7a-143">não</span><span class="sxs-lookup"><span data-stu-id="efb7a-143">no</span></span>        |
| [<span data-ttu-id="efb7a-144">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="efb7a-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="efb7a-145">não</span><span class="sxs-lookup"><span data-stu-id="efb7a-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="efb7a-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="efb7a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efb7a-147">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="efb7a-147">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





