---
title: dcl_tessellator_output_primitive (SM5-ASM)
description: Declare o tipo primitivo de saída Tessellator em uma seção de declaração de sombreador envoltória.
ms.assetid: 95F074C5-6012-4160-B78E-440C33C1ECC3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 390f22cdafe3b0d078bf8a502623a1c741e34e34
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006924"
---
# <a name="dcl_tessellator_output_primitive-sm5---asm"></a><span data-ttu-id="d4ec4-103">\_Tessellator \_ de saída \_ do DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="d4ec4-103">dcl\_tessellator\_output\_primitive (sm5 - asm)</span></span>

<span data-ttu-id="d4ec4-104">Declare o tipo primitivo de saída Tessellator em uma seção de declaração de sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="d4ec4-104">Declare the tessellator output primitive type in a hull shader declaration section.</span></span>



| <span data-ttu-id="d4ec4-105">Tessellator de saída do DCL ( \_ \_ \_ ponto de saída \_ )</span><span class="sxs-lookup"><span data-stu-id="d4ec4-105">dcl\_tessellator\_output\_primitive {output\_point \</span></span>| <span data-ttu-id="d4ec4-106">linha de saída \_ </span><span class="sxs-lookup"><span data-stu-id="d4ec4-106">output\_line </span></span>\| <span data-ttu-id="d4ec4-107">triangloutput \_ e \_ PV </span><span class="sxs-lookup"><span data-stu-id="d4ec4-107">triangloutput\_e\_cw </span></span>\| <span data-ttu-id="d4ec4-108">triangular de saída \_ \_ CCW}</span><span class="sxs-lookup"><span data-stu-id="d4ec4-108">output\_triangle\_ccw}</span></span> |
|----------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="d4ec4-109">Item</span><span class="sxs-lookup"><span data-stu-id="d4ec4-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="d4ec4-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4ec4-110">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="d4ec4-111"><span id="output_point___output_line_____________________________________triangloutput_e_cw___output_triangle_ccw"></span><span id="OUTPUT_POINT___OUTPUT_LINE_____________________________________TRIANGLOUTPUT_E_CW___OUTPUT_TRIANGLE_CCW"></span>*linha de saída do ponto de saída \_ \| \_ \| triangloutput e o \_ \_ triângulo de saída do CW \| \_ \_*</span><span class="sxs-lookup"><span data-stu-id="d4ec4-111"><span id="output_point___output_line_____________________________________triangloutput_e_cw___output_triangle_ccw"></span><span id="OUTPUT_POINT___OUTPUT_LINE_____________________________________TRIANGLOUTPUT_E_CW___OUTPUT_TRIANGLE_CCW"></span>*output\_point \| output\_line \| triangloutput\_e\_cw \| output\_triangle\_ccw*</span></span><br/> | <span data-ttu-id="d4ec4-112">\[no \] tipo primitivo de saída.</span><span class="sxs-lookup"><span data-stu-id="d4ec4-112">\[in\] The output primitive type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d4ec4-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4ec4-113">Remarks</span></span>

<span data-ttu-id="d4ec4-114">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="d4ec4-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d4ec4-115">Vértice</span><span class="sxs-lookup"><span data-stu-id="d4ec4-115">Vertex</span></span> | <span data-ttu-id="d4ec4-116">Envoltória</span><span class="sxs-lookup"><span data-stu-id="d4ec4-116">Hull</span></span>                 | <span data-ttu-id="d4ec4-117">Domínio</span><span class="sxs-lookup"><span data-stu-id="d4ec4-117">Domain</span></span> | <span data-ttu-id="d4ec4-118">Geometria</span><span class="sxs-lookup"><span data-stu-id="d4ec4-118">Geometry</span></span> | <span data-ttu-id="d4ec4-119">16x16</span><span class="sxs-lookup"><span data-stu-id="d4ec4-119">Pixel</span></span> | <span data-ttu-id="d4ec4-120">Computação</span><span class="sxs-lookup"><span data-stu-id="d4ec4-120">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="d4ec4-121">Seção de declarações</span><span class="sxs-lookup"><span data-stu-id="d4ec4-121">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d4ec4-122">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="d4ec4-122">Minimum Shader Model</span></span>

<span data-ttu-id="d4ec4-123">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="d4ec4-123">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d4ec4-124">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="d4ec4-124">Shader Model</span></span>                                              | <span data-ttu-id="d4ec4-125">Com suporte</span><span class="sxs-lookup"><span data-stu-id="d4ec4-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d4ec4-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d4ec4-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d4ec4-127">sim</span><span class="sxs-lookup"><span data-stu-id="d4ec4-127">yes</span></span>       |
| [<span data-ttu-id="d4ec4-128">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="d4ec4-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d4ec4-129">não</span><span class="sxs-lookup"><span data-stu-id="d4ec4-129">no</span></span>        |
| [<span data-ttu-id="d4ec4-130">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="d4ec4-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d4ec4-131">não</span><span class="sxs-lookup"><span data-stu-id="d4ec4-131">no</span></span>        |
| [<span data-ttu-id="d4ec4-132">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d4ec4-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d4ec4-133">não</span><span class="sxs-lookup"><span data-stu-id="d4ec4-133">no</span></span>        |
| [<span data-ttu-id="d4ec4-134">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d4ec4-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d4ec4-135">não</span><span class="sxs-lookup"><span data-stu-id="d4ec4-135">no</span></span>        |
| [<span data-ttu-id="d4ec4-136">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d4ec4-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d4ec4-137">não</span><span class="sxs-lookup"><span data-stu-id="d4ec4-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d4ec4-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4ec4-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4ec4-139">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d4ec4-139">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





