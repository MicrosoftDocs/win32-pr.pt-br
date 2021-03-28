---
title: switch (sm4-ASM)
description: Transfere o controle para um bloco de instruções diferente dentro do corpo do comutador, dependendo do valor de um seletor.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feed346b8aa33feecc13fe2a6ffad59c961b0173
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006892"
---
# <a name="switch-sm4---asm"></a><span data-ttu-id="1ab5f-103">switch (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="1ab5f-103">switch (sm4 - asm)</span></span>

<span data-ttu-id="1ab5f-104">Transfere o controle para um bloco de instruções diferente dentro do corpo do comutador, dependendo do valor de um seletor.</span><span class="sxs-lookup"><span data-stu-id="1ab5f-104">Transfers control to a different statement block within the switch body depending on the value of a selector.</span></span>



| <span data-ttu-id="1ab5f-105">alternar src0. \_ componente selecionado</span><span class="sxs-lookup"><span data-stu-id="1ab5f-105">switch src0.selected\_component</span></span> |
|---------------------------------|



 



| <span data-ttu-id="1ab5f-106">Item</span><span class="sxs-lookup"><span data-stu-id="1ab5f-106">Item</span></span>                                                            | <span data-ttu-id="1ab5f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ab5f-107">Description</span></span>                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="1ab5f-108"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1ab5f-108"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1ab5f-109">\[no \] seletor da instrução switch.</span><span class="sxs-lookup"><span data-stu-id="1ab5f-109">\[in\] The selector for the switch statement.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1ab5f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ab5f-110">Remarks</span></span>

<span data-ttu-id="1ab5f-111">Uma construção **de** / [comutador](endswitch--sm4---asm-.md) endswitch se comporta exatamente como uma construção de **comutador** na linguagem C, com a seguinte exceção: para instruções padrão D3D11 [Case](case--sm4---asm-.md) / [](default--sm4---asm-.md) que se enquadram no próximo **caso**, o / **padrão** sem uma [interrupção](break--sm4---asm-.md) não pode ter nenhum código.</span><span class="sxs-lookup"><span data-stu-id="1ab5f-111">A **switch**/[endswitch](endswitch--sm4---asm-.md) construct behaves exactly as a **switch** construct in the C language, with the following exception: for D3D11 [case](case--sm4---asm-.md)/[default](default--sm4---asm-.md) statements that fall through to the next **case**/**default** without a [break](break--sm4---asm-.md) cannot have any code in them.</span></span> <span data-ttu-id="1ab5f-112">Ele é permitido para várias instruções **Case** , incluindo **Default**, para aparecer sequencialmente, compartilhando o mesmo bloco de código.</span><span class="sxs-lookup"><span data-stu-id="1ab5f-112">It is permitted for multiple **case** statements, including **default**, to appear sequentially, sharing the same code block.</span></span>

<span data-ttu-id="1ab5f-113">A condição deve ser um componente de registro de 32 bits ou uma quantidade imediata.</span><span class="sxs-lookup"><span data-stu-id="1ab5f-113">The condition must be a 32-bit register component or immediate quantity.</span></span> <span data-ttu-id="1ab5f-114">A comparação de igualdade é bit-a-bit (Integer).</span><span class="sxs-lookup"><span data-stu-id="1ab5f-114">The equality comparison is bitwise (integer).</span></span>

<span data-ttu-id="1ab5f-115">Como com qualquer instrução de sombreador no D3D11, o hardware pode ou não implementar o constructo de **comutador** diretamente.</span><span class="sxs-lookup"><span data-stu-id="1ab5f-115">As with any Shader instruction in the D3D11, hardware may or may not implement the **switch** construct directly.</span></span>

<span data-ttu-id="1ab5f-116">As instruções **switch** podem ser aninhadas.</span><span class="sxs-lookup"><span data-stu-id="1ab5f-116">**Switch** statements can be nested.</span></span> <span data-ttu-id="1ab5f-117">Cada bloco **switch** conta como um nível em relação ao limite de profundidade de aninhamento de controle de fluxo de 64 por sub-rotina e Main, independentemente do número de instruções **Case** .</span><span class="sxs-lookup"><span data-stu-id="1ab5f-117">Each **switch** block counts as 1 level against the flow control nesting depth limit of 64 per subroutine and main, independent of the number of **case** statements.</span></span> <span data-ttu-id="1ab5f-118">O compilador HLSL não gerará sub-rotinas que excedam esse limite.</span><span class="sxs-lookup"><span data-stu-id="1ab5f-118">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="1ab5f-119">O comportamento das instruções de fluxo de controle além de 64 níveis de profundidade por sub-rotina é indefinido.</span><span class="sxs-lookup"><span data-stu-id="1ab5f-119">Behavior of control flow instructions beyond 64 levels deep per subroutine is undefined.</span></span>

<span data-ttu-id="1ab5f-120">O exemplo a seguir mostra como usar essa instrução.</span><span class="sxs-lookup"><span data-stu-id="1ab5f-120">The following example shows how to use this instruction.</span></span>

``` syntax
                ...
                switch r0.x
                default: // falling through
                case 3
                    switch r1.x
                    case 4
                        ...
                        break
                    case 5
                        ...
                        break
                    endswitch
                    break
                case 0
                    break
                endswitch
```

<span data-ttu-id="1ab5f-121">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="1ab5f-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1ab5f-122">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="1ab5f-122">Vertex Shader</span></span> | <span data-ttu-id="1ab5f-123">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="1ab5f-123">Geometry Shader</span></span> | <span data-ttu-id="1ab5f-124">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="1ab5f-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1ab5f-125">x</span><span class="sxs-lookup"><span data-stu-id="1ab5f-125">x</span></span>             | <span data-ttu-id="1ab5f-126">x</span><span class="sxs-lookup"><span data-stu-id="1ab5f-126">x</span></span>               | <span data-ttu-id="1ab5f-127">x</span><span class="sxs-lookup"><span data-stu-id="1ab5f-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1ab5f-128">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="1ab5f-128">Minimum Shader Model</span></span>

<span data-ttu-id="1ab5f-129">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1ab5f-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1ab5f-130">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="1ab5f-130">Shader Model</span></span>                                              | <span data-ttu-id="1ab5f-131">Com suporte</span><span class="sxs-lookup"><span data-stu-id="1ab5f-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1ab5f-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="1ab5f-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1ab5f-133">sim</span><span class="sxs-lookup"><span data-stu-id="1ab5f-133">yes</span></span>       |
| [<span data-ttu-id="1ab5f-134">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="1ab5f-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1ab5f-135">sim</span><span class="sxs-lookup"><span data-stu-id="1ab5f-135">yes</span></span>       |
| [<span data-ttu-id="1ab5f-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="1ab5f-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1ab5f-137">sim</span><span class="sxs-lookup"><span data-stu-id="1ab5f-137">yes</span></span>       |
| [<span data-ttu-id="1ab5f-138">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1ab5f-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1ab5f-139">não</span><span class="sxs-lookup"><span data-stu-id="1ab5f-139">no</span></span>        |
| [<span data-ttu-id="1ab5f-140">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1ab5f-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1ab5f-141">não</span><span class="sxs-lookup"><span data-stu-id="1ab5f-141">no</span></span>        |
| [<span data-ttu-id="1ab5f-142">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1ab5f-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1ab5f-143">não</span><span class="sxs-lookup"><span data-stu-id="1ab5f-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1ab5f-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ab5f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ab5f-145">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1ab5f-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





