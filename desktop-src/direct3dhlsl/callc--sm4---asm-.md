---
title: callc (sm4-ASM)
description: Chama condicionalmente uma sub-rotina marcada por onde o rótulo l \ aparece no programa.
ms.assetid: 7F6E81CE-0C38-499B-B83E-FA76FA154451
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6bc8c9d1e4a99ce25f99253518482181cdb74d8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988581"
---
# <a name="callc-sm4---asm"></a><span data-ttu-id="19196-103">callc (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="19196-103">callc (sm4 - asm)</span></span>

<span data-ttu-id="19196-104">Chama condicionalmente uma sub-rotina marcada por onde o rótulo **l \#** aparece no programa.</span><span class="sxs-lookup"><span data-stu-id="19196-104">Conditionally calls a subroutine marked by where the label **l\#** appears in the program.</span></span>



| <span data-ttu-id="19196-105">callc { \_ z </span><span class="sxs-lookup"><span data-stu-id="19196-105">callc{\_z</span></span>\|<span data-ttu-id="19196-106">\_NZ} src0. Select \_ componente, l\#</span><span class="sxs-lookup"><span data-stu-id="19196-106">\_nz} src0.select\_component, l\#</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="19196-107">Item</span><span class="sxs-lookup"><span data-stu-id="19196-107">Item</span></span>                                                            | <span data-ttu-id="19196-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="19196-108">Description</span></span>                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="19196-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="19196-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="19196-110">\[no \] componente no qual testar a condição.</span><span class="sxs-lookup"><span data-stu-id="19196-110">\[in\] The component on which to test the condition.</span></span><br/> |
| <span data-ttu-id="19196-111"><span id="l_"></span><span id="L_"></span>*debug\#*</span><span class="sxs-lookup"><span data-stu-id="19196-111"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/>      | <span data-ttu-id="19196-112">\[no \] rótulo da sub-rotina.</span><span class="sxs-lookup"><span data-stu-id="19196-112">\[in\] The label of the subroutine.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="19196-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="19196-113">Remarks</span></span>

<span data-ttu-id="19196-114">Quando uma [RET](ret--sm4---asm-.md) é encontrada, retorna a execução para a instrução após essa chamada.</span><span class="sxs-lookup"><span data-stu-id="19196-114">When a [ret](ret--sm4---asm-.md) is encountered, return execution to the instruction after this call.</span></span>

<span data-ttu-id="19196-115">O formato do token contém o deslocamento do rótulo correspondente no sombreador como uma conveniência.</span><span class="sxs-lookup"><span data-stu-id="19196-115">The token format contains the offset of the corresponding label in the Shader as a convenience.</span></span>

<span data-ttu-id="19196-116">O exemplo a seguir mostra a instrução de chamada.</span><span class="sxs-lookup"><span data-stu-id="19196-116">The following example shows the call instruction.</span></span>


```
                ...
                callc_z  r1.y, l3 // if all bits in r0.x are 0, call l3
                callc_nz r2.z, l3 // if any bit in r0.x is nonzero, call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret

```



### <a name="restrictions"></a><span data-ttu-id="19196-117">Restrições</span><span class="sxs-lookup"><span data-stu-id="19196-117">Restrictions</span></span>

-   <span data-ttu-id="19196-118">As sub-rotinas podem aninhar 32 de profundidade.</span><span class="sxs-lookup"><span data-stu-id="19196-118">Subroutines can nest 32 deep.</span></span>
-   <span data-ttu-id="19196-119">A pilha de endereços de retorno é gerenciada de forma transparente pela implementação.</span><span class="sxs-lookup"><span data-stu-id="19196-119">The return address stack is managed transparently by the implementation.</span></span>
-   <span data-ttu-id="19196-120">Se já houver entradas 32 na pilha de endereços de retorno e uma **chamada** for emitida, a chamada será ignorada.</span><span class="sxs-lookup"><span data-stu-id="19196-120">If there are already 32 entries on the return address stack and a **call** is issued, the call is skipped over.</span></span>
-   <span data-ttu-id="19196-121">Não há nenhuma pilha de parâmetros automática.</span><span class="sxs-lookup"><span data-stu-id="19196-121">There is no automatic parameter stack.</span></span> <span data-ttu-id="19196-122">O aplicativo pode usar uma matriz de registro temporário indexável (x \# \[ \] ) para implementar manualmente uma pilha.</span><span class="sxs-lookup"><span data-stu-id="19196-122">The application can use an indexable temporary register array (x\#\[\]) to manually implement a stack.</span></span> <span data-ttu-id="19196-123">No entanto, os endereços de retorno da chamada de sub-rotina não são visíveis e são ortogonal a qualquer gerenciamento de pilha manual feito pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="19196-123">However, the subroutine call return addresses are not visible and are orthogonal to any manual stack management done by the application.</span></span>
-   <span data-ttu-id="19196-124">A indexação do *parâmetro \# l* não é permitida.</span><span class="sxs-lookup"><span data-stu-id="19196-124">Indexing of the *l\#* parameter is not permitted.</span></span>
-   <span data-ttu-id="19196-125">O registro de 32 bits fornecido pelo *src0* é testado em um nível de bit.</span><span class="sxs-lookup"><span data-stu-id="19196-125">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="19196-126">Se algum bit for diferente de zero, **callc \_ NZ** executará a chamada.</span><span class="sxs-lookup"><span data-stu-id="19196-126">If any bit is nonzero, **callc\_nz** will perform the call.</span></span> <span data-ttu-id="19196-127">Se todos os bits forem zero, o **callc \_ z** executará a chamada.</span><span class="sxs-lookup"><span data-stu-id="19196-127">If all bits are zero, **callc\_z** will perform the call.</span></span>
-   <span data-ttu-id="19196-128">Recursão não é permitida.</span><span class="sxs-lookup"><span data-stu-id="19196-128">Recursion is not permitted.</span></span>

<span data-ttu-id="19196-129">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="19196-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="19196-130">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="19196-130">Vertex Shader</span></span> | <span data-ttu-id="19196-131">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="19196-131">Geometry Shader</span></span> | <span data-ttu-id="19196-132">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="19196-132">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="19196-133">x</span><span class="sxs-lookup"><span data-stu-id="19196-133">x</span></span>             | <span data-ttu-id="19196-134">x</span><span class="sxs-lookup"><span data-stu-id="19196-134">x</span></span>               | <span data-ttu-id="19196-135">x</span><span class="sxs-lookup"><span data-stu-id="19196-135">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="19196-136">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="19196-136">Minimum Shader Model</span></span>

<span data-ttu-id="19196-137">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="19196-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="19196-138">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="19196-138">Shader Model</span></span>                                              | <span data-ttu-id="19196-139">Com suporte</span><span class="sxs-lookup"><span data-stu-id="19196-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="19196-140">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="19196-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="19196-141">sim</span><span class="sxs-lookup"><span data-stu-id="19196-141">yes</span></span>       |
| [<span data-ttu-id="19196-142">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="19196-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="19196-143">sim</span><span class="sxs-lookup"><span data-stu-id="19196-143">yes</span></span>       |
| [<span data-ttu-id="19196-144">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="19196-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="19196-145">sim</span><span class="sxs-lookup"><span data-stu-id="19196-145">yes</span></span>       |
| [<span data-ttu-id="19196-146">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="19196-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="19196-147">não</span><span class="sxs-lookup"><span data-stu-id="19196-147">no</span></span>        |
| [<span data-ttu-id="19196-148">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="19196-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="19196-149">não</span><span class="sxs-lookup"><span data-stu-id="19196-149">no</span></span>        |
| [<span data-ttu-id="19196-150">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="19196-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="19196-151">não</span><span class="sxs-lookup"><span data-stu-id="19196-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="19196-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="19196-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19196-153">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="19196-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





