---
title: continuec (sm4-ASM)
description: Continua a execução condicionalmente no início do loop atual.
ms.assetid: 1A5B1951-CE1E-479C-AE0F-FC5FB93E0DE9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d480d8828f8f68af1f6a2ff4f52224041d5241df
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967104"
---
# <a name="continuec-sm4---asm"></a><span data-ttu-id="34057-103">continuec (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="34057-103">continuec (sm4 - asm)</span></span>

<span data-ttu-id="34057-104">Continua a execução condicionalmente no início do loop atual.</span><span class="sxs-lookup"><span data-stu-id="34057-104">Conditionally continues execution at the beginning of the current loop.</span></span>



| <span data-ttu-id="34057-105">continuec { \_ z </span><span class="sxs-lookup"><span data-stu-id="34057-105">continuec{\_z</span></span>\|<span data-ttu-id="34057-106">\_NZ} src0. Select \_ componente</span><span class="sxs-lookup"><span data-stu-id="34057-106">\_nz} src0.select\_component</span></span> |
|---------------------------------------------|



 



| <span data-ttu-id="34057-107">Termo</span><span class="sxs-lookup"><span data-stu-id="34057-107">Term</span></span>                                                            | <span data-ttu-id="34057-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="34057-108">Description</span></span>                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="34057-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="34057-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="34057-110">\[no \] componente em relação a qual testar a condição.</span><span class="sxs-lookup"><span data-stu-id="34057-110">\[in\] The component against which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="34057-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="34057-111">Remarks</span></span>

<span data-ttu-id="34057-112">**continuec** pode ser usado somente dentro de um [loop](loop--sm4---asm-.md) ou [ENDLOOP](endloop--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="34057-112">**continuec** can be used only inside a [loop](loop--sm4---asm-.md) or [endloop](endloop--sm4---asm-.md).</span></span>

<span data-ttu-id="34057-113">O exemplo a seguir mostra como usar a instrução **continuec** .</span><span class="sxs-lookup"><span data-stu-id="34057-113">The following example shows how to use the **continuec** instruction.</span></span>


```
                loop
                    if_na r0.x
                        break
                    endif
                    continuec_z r1.x  // if all bits of r1.x are zero then
                                      // continue at beginning of loop.
                    ...
                    continuec_nz r3.y // if any bit in r3.y is set then
                                      // continue at beginning of loop.

                    ...
                endloop

```



<span data-ttu-id="34057-114">O formato do token contém o deslocamento da instrução de loop correspondente no sombreador como uma conveniência.</span><span class="sxs-lookup"><span data-stu-id="34057-114">The token format contains the offset of the corresponding loop instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="34057-115">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="34057-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="34057-116">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="34057-116">Vertex Shader</span></span> | <span data-ttu-id="34057-117">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="34057-117">Geometry Shader</span></span> | <span data-ttu-id="34057-118">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="34057-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="34057-119">x</span><span class="sxs-lookup"><span data-stu-id="34057-119">x</span></span>             | <span data-ttu-id="34057-120">x</span><span class="sxs-lookup"><span data-stu-id="34057-120">x</span></span>               | <span data-ttu-id="34057-121">x</span><span class="sxs-lookup"><span data-stu-id="34057-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="34057-122">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="34057-122">Minimum Shader Model</span></span>

<span data-ttu-id="34057-123">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="34057-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="34057-124">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="34057-124">Shader Model</span></span>                                              | <span data-ttu-id="34057-125">Com suporte</span><span class="sxs-lookup"><span data-stu-id="34057-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="34057-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="34057-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="34057-127">sim</span><span class="sxs-lookup"><span data-stu-id="34057-127">yes</span></span>       |
| [<span data-ttu-id="34057-128">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="34057-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="34057-129">sim</span><span class="sxs-lookup"><span data-stu-id="34057-129">yes</span></span>       |
| [<span data-ttu-id="34057-130">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="34057-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="34057-131">sim</span><span class="sxs-lookup"><span data-stu-id="34057-131">yes</span></span>       |
| [<span data-ttu-id="34057-132">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="34057-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="34057-133">não</span><span class="sxs-lookup"><span data-stu-id="34057-133">no</span></span>        |
| [<span data-ttu-id="34057-134">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="34057-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="34057-135">não</span><span class="sxs-lookup"><span data-stu-id="34057-135">no</span></span>        |
| [<span data-ttu-id="34057-136">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="34057-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="34057-137">não</span><span class="sxs-lookup"><span data-stu-id="34057-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="34057-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="34057-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34057-139">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="34057-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





