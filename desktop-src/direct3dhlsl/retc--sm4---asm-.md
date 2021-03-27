---
title: retc (sm4-ASM)
description: Retorno condicional.
ms.assetid: D936099D-4A75-4AE2-9FE3-70ED213DF4D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e394bc6b947d91fafb09dbfdc075b0c60be2cf8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967123"
---
# <a name="retc-sm4---asm"></a><span data-ttu-id="f0611-103">retc (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f0611-103">retc (sm4 - asm)</span></span>

<span data-ttu-id="f0611-104">Retorno condicional.</span><span class="sxs-lookup"><span data-stu-id="f0611-104">Conditional return.</span></span>



| <span data-ttu-id="f0611-105">retc { \_ z </span><span class="sxs-lookup"><span data-stu-id="f0611-105">retc{\_z</span></span>\|<span data-ttu-id="f0611-106">\_NZ} src0. Select \_ componente</span><span class="sxs-lookup"><span data-stu-id="f0611-106">\_nz} src0.select\_component</span></span> |
|----------------------------------------|



 



| <span data-ttu-id="f0611-107">Item</span><span class="sxs-lookup"><span data-stu-id="f0611-107">Item</span></span>                                                            | <span data-ttu-id="f0611-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f0611-108">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f0611-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f0611-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f0611-110">\[no \] registro para testar a condição.</span><span class="sxs-lookup"><span data-stu-id="f0611-110">\[in\] The register to test the condition against.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f0611-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0611-111">Remarks</span></span>

<span data-ttu-id="f0611-112">Se dentro de uma sub-rotina, essa instrução retorna condicionalmente para a instrução após a chamada.</span><span class="sxs-lookup"><span data-stu-id="f0611-112">If within a subroutine, this instruction conditionally returns to the instruction after the call.</span></span> <span data-ttu-id="f0611-113">Se não estiver dentro de uma sub-rotina, essa instrução encerrará a execução do programa.</span><span class="sxs-lookup"><span data-stu-id="f0611-113">If not inside a subroutine, this instruction terminates program execution.</span></span>

<span data-ttu-id="f0611-114">O exemplo a seguir mostra como usar essa instrução.</span><span class="sxs-lookup"><span data-stu-id="f0611-114">The following example shows how to use this instruction.</span></span>

``` syntax
           ...
           call l3
           ...
           ret
           label l3
               ...
               retc_nz r0.x  // If any bit in r0.x is nonzero, then return
               retc_z  r1.x  // If all bits in r0.x are zero, then return.
               ...
           ret
```

### <a name="restrictions"></a><span data-ttu-id="f0611-115">Restrições</span><span class="sxs-lookup"><span data-stu-id="f0611-115">Restrictions</span></span>

-   <span data-ttu-id="f0611-116">**retc** podem aparecer em qualquer lugar em um programa, várias vezes.</span><span class="sxs-lookup"><span data-stu-id="f0611-116">**retc** can appear anywhere in a program, any number of times.</span></span>
-   <span data-ttu-id="f0611-117">A última instrução em um programa principal ou uma sub-rotina não pode ser um **\_ NZ** **retc \_ z** ou retc.</span><span class="sxs-lookup"><span data-stu-id="f0611-117">The last instruction in a main program or subroutine cannot be a **retc\_z** or **retc\_nz**.</span></span> <span data-ttu-id="f0611-118">Em vez disso, a [RET](ret--sm4---asm-.md) incondicional pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="f0611-118">Instead, the unconditional [ret](ret--sm4---asm-.md) can be used.</span></span>
-   <span data-ttu-id="f0611-119">O registro de 32 bits fornecido pelo *src0* é testado em um nível de bit.</span><span class="sxs-lookup"><span data-stu-id="f0611-119">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="f0611-120">Se algum bit for diferente de zero, a **RET \_ NZ** retornará.</span><span class="sxs-lookup"><span data-stu-id="f0611-120">If any bit is nonzero, **ret\_nz** will return.</span></span> <span data-ttu-id="f0611-121">Se todos os bits forem zero, **retc \_ z** retornará.</span><span class="sxs-lookup"><span data-stu-id="f0611-121">If all bits are zero, **retc\_z** will return.</span></span>

<span data-ttu-id="f0611-122">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="f0611-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f0611-123">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="f0611-123">Vertex Shader</span></span> | <span data-ttu-id="f0611-124">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="f0611-124">Geometry Shader</span></span> | <span data-ttu-id="f0611-125">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="f0611-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f0611-126">x</span><span class="sxs-lookup"><span data-stu-id="f0611-126">x</span></span>             | <span data-ttu-id="f0611-127">x</span><span class="sxs-lookup"><span data-stu-id="f0611-127">x</span></span>               | <span data-ttu-id="f0611-128">x</span><span class="sxs-lookup"><span data-stu-id="f0611-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f0611-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="f0611-129">Minimum Shader Model</span></span>

<span data-ttu-id="f0611-130">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f0611-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f0611-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="f0611-131">Shader Model</span></span>                                              | <span data-ttu-id="f0611-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="f0611-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f0611-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f0611-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f0611-134">sim</span><span class="sxs-lookup"><span data-stu-id="f0611-134">yes</span></span>       |
| [<span data-ttu-id="f0611-135">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="f0611-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f0611-136">sim</span><span class="sxs-lookup"><span data-stu-id="f0611-136">yes</span></span>       |
| [<span data-ttu-id="f0611-137">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="f0611-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f0611-138">sim</span><span class="sxs-lookup"><span data-stu-id="f0611-138">yes</span></span>       |
| [<span data-ttu-id="f0611-139">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f0611-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f0611-140">não</span><span class="sxs-lookup"><span data-stu-id="f0611-140">no</span></span>        |
| [<span data-ttu-id="f0611-141">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f0611-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f0611-142">não</span><span class="sxs-lookup"><span data-stu-id="f0611-142">no</span></span>        |
| [<span data-ttu-id="f0611-143">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f0611-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f0611-144">não</span><span class="sxs-lookup"><span data-stu-id="f0611-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f0611-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f0611-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0611-146">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f0611-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





