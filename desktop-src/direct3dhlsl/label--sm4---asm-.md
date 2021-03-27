---
title: rótulo (sm4-ASM)
description: Indica o início de uma sub-rotina.
ms.assetid: B966AE64-47CA-4A13-A26F-184D9FD26C26
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff4c2d73db5d776c75b6d6339cecb7748a9868d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638874"
---
# <a name="label-sm4---asm"></a><span data-ttu-id="2c34c-103">rótulo (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="2c34c-103">label (sm4 - asm)</span></span>

<span data-ttu-id="2c34c-104">Indica o início de uma sub-rotina.</span><span class="sxs-lookup"><span data-stu-id="2c34c-104">Indicates the beginning of a subroutine.</span></span>



| <span data-ttu-id="2c34c-105">rótulo l\#</span><span class="sxs-lookup"><span data-stu-id="2c34c-105">label l\#</span></span> |
|-----------|



 



| <span data-ttu-id="2c34c-106">Item</span><span class="sxs-lookup"><span data-stu-id="2c34c-106">Item</span></span>                                                       | <span data-ttu-id="2c34c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c34c-107">Description</span></span>                         |
|------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="2c34c-108"><span id="l_"></span><span id="L_"></span>*debug\#*</span><span class="sxs-lookup"><span data-stu-id="2c34c-108"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/> | <span data-ttu-id="2c34c-109">\[no \] número do rótulo.</span><span class="sxs-lookup"><span data-stu-id="2c34c-109">\[in\] The label number.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2c34c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c34c-110">Remarks</span></span>

<span data-ttu-id="2c34c-111">Um **rótulo** só pode aparecer diretamente após uma instrução [**RET**](ret--sm4---asm-.md) que não está aninhada em nenhuma declaração de controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="2c34c-111">A **label** can only appear directly after a [**ret**](ret--sm4---asm-.md) instruction which is not nested in any flow control statements.</span></span>

<span data-ttu-id="2c34c-112">O código antes do primeiro **rótulo** em um programa é o programa principal.</span><span class="sxs-lookup"><span data-stu-id="2c34c-112">The code before the first **label** in a program is the main program.</span></span> <span data-ttu-id="2c34c-113">Todas as sub-rotinas aparecem no final do programa, indicado por instruções de **rótulo** .</span><span class="sxs-lookup"><span data-stu-id="2c34c-113">All subroutines appear at the end of the program, indicated by **label** statements.</span></span>

<span data-ttu-id="2c34c-114">O exemplo a seguir mostra como usar essa instrução.</span><span class="sxs-lookup"><span data-stu-id="2c34c-114">The following example shows how to use this instruction.</span></span>

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                    if_nz r0.x
                        ret
                    endif
                    ...
                ret
```

<span data-ttu-id="2c34c-115">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="2c34c-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2c34c-116">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="2c34c-116">Vertex Shader</span></span> | <span data-ttu-id="2c34c-117">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="2c34c-117">Geometry Shader</span></span> | <span data-ttu-id="2c34c-118">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="2c34c-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2c34c-119">x</span><span class="sxs-lookup"><span data-stu-id="2c34c-119">x</span></span>             | <span data-ttu-id="2c34c-120">x</span><span class="sxs-lookup"><span data-stu-id="2c34c-120">x</span></span>               | <span data-ttu-id="2c34c-121">x</span><span class="sxs-lookup"><span data-stu-id="2c34c-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2c34c-122">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="2c34c-122">Minimum Shader Model</span></span>

<span data-ttu-id="2c34c-123">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2c34c-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2c34c-124">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="2c34c-124">Shader Model</span></span>                                              | <span data-ttu-id="2c34c-125">Com suporte</span><span class="sxs-lookup"><span data-stu-id="2c34c-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2c34c-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2c34c-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2c34c-127">sim</span><span class="sxs-lookup"><span data-stu-id="2c34c-127">yes</span></span>       |
| [<span data-ttu-id="2c34c-128">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="2c34c-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2c34c-129">sim</span><span class="sxs-lookup"><span data-stu-id="2c34c-129">yes</span></span>       |
| [<span data-ttu-id="2c34c-130">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="2c34c-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2c34c-131">sim</span><span class="sxs-lookup"><span data-stu-id="2c34c-131">yes</span></span>       |
| [<span data-ttu-id="2c34c-132">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c34c-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2c34c-133">não</span><span class="sxs-lookup"><span data-stu-id="2c34c-133">no</span></span>        |
| [<span data-ttu-id="2c34c-134">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c34c-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2c34c-135">não</span><span class="sxs-lookup"><span data-stu-id="2c34c-135">no</span></span>        |
| [<span data-ttu-id="2c34c-136">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c34c-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2c34c-137">não</span><span class="sxs-lookup"><span data-stu-id="2c34c-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2c34c-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c34c-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c34c-139">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c34c-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





