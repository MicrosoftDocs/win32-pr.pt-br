---
title: firstbit (SM5-ASM)
description: Localiza o primeiro conjunto de bits em um número, seja de LSB ou MSB.
ms.assetid: E3066676-5218-470A-944A-7B221E1BF64D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b88fa9291ce64fcc8c94510bd09bed31e7b7f96
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293595"
---
# <a name="firstbit-sm5---asm"></a><span data-ttu-id="cb1c2-103">firstbit (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="cb1c2-103">firstbit (sm5 - asm)</span></span>

<span data-ttu-id="cb1c2-104">Localiza o primeiro conjunto de bits em um número, seja de LSB ou MSB.</span><span class="sxs-lookup"><span data-stu-id="cb1c2-104">Finds the first bit set in a number, either from LSB or MSB.</span></span>



| <span data-ttu-id="cb1c2-105">firstbit { \_ Hi </span><span class="sxs-lookup"><span data-stu-id="cb1c2-105">firstbit{\_hi</span></span>\|<span data-ttu-id="cb1c2-106">\_lo</span><span class="sxs-lookup"><span data-stu-id="cb1c2-106">\_lo\</span></span>|<span data-ttu-id="cb1c2-107">\_Shi} dest \[ . Mask \] , src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="cb1c2-107">\_shi} dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="cb1c2-108">Item</span><span class="sxs-lookup"><span data-stu-id="cb1c2-108">Item</span></span>                                                            | <span data-ttu-id="cb1c2-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="cb1c2-109">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb1c2-110"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="cb1c2-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="cb1c2-111">\[na \] posição de inteiro do primeiro conjunto de bits em *src0* começando do LSB para FIRSTBIT \_ lo ou MSB para firstbit \_ Hi.</span><span class="sxs-lookup"><span data-stu-id="cb1c2-111">\[in\] The integer position of the first bit set in *src0* starting from the LSB for firstbit\_lo or MSB for firstbit\_hi.</span></span><br/> |
| <span data-ttu-id="cb1c2-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="cb1c2-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="cb1c2-113">\[no \] número inteiro de entrada.</span><span class="sxs-lookup"><span data-stu-id="cb1c2-113">\[in\] The input integer.</span></span><br/>                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="cb1c2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb1c2-114">Remarks</span></span>

<span data-ttu-id="cb1c2-115">Essa operação retorna a posição de inteiro do primeiro conjunto de bits na entrada de 32 bits, começando do LSB para firstbit \_ lo ou MSB para firstbit \_ Hi.</span><span class="sxs-lookup"><span data-stu-id="cb1c2-115">This operation returns the integer position of the first bit set in the 32-bit input starting from the LSB for firstbit\_lo or MSB for firstbit\_hi.</span></span> <span data-ttu-id="cb1c2-116">Por exemplo, firstbit \_ lo em 0x00000001 retorna 0.</span><span class="sxs-lookup"><span data-stu-id="cb1c2-116">For example firstbit\_lo on 0x00000001 returns 0.</span></span> <span data-ttu-id="cb1c2-117">firstbit \_ Hi em 0x10000000 retorna 3.</span><span class="sxs-lookup"><span data-stu-id="cb1c2-117">firstbit\_hi on 0x10000000 returns 3.</span></span>

<span data-ttu-id="cb1c2-118">firstbit \_ shi (s para assinadas) retornará o primeiro 0 do MSB se o número for negativo; caso contrário, ele retornará o primeiro 1 do MSB.</span><span class="sxs-lookup"><span data-stu-id="cb1c2-118">firstbit\_shi (s for signed) returns the first 0 from the MSB if the number is negative; otherwise it returns the first 1 from the MSB.</span></span>

<span data-ttu-id="cb1c2-119">Todas as variantes da instrução retornam ~ 0 (0xFFFFFFFF no registro de 32 bits) se nenhuma correspondência for encontrada.</span><span class="sxs-lookup"><span data-stu-id="cb1c2-119">All variants of the instruction return ~0 (0xffffffff in 32-bit register) if no match is found.</span></span>

<span data-ttu-id="cb1c2-120">Use essa instrução para enumerar rapidamente os bits de conjunto em um campo de campo ou encontrar a maior potência de 2 em um número.</span><span class="sxs-lookup"><span data-stu-id="cb1c2-120">Use this instruction to quickly enumerate set bits in a bitfield, or find the largest power of 2 in a number.</span></span>

<span data-ttu-id="cb1c2-121">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="cb1c2-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="cb1c2-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="cb1c2-122">Vertex</span></span> | <span data-ttu-id="cb1c2-123">Envoltória</span><span class="sxs-lookup"><span data-stu-id="cb1c2-123">Hull</span></span> | <span data-ttu-id="cb1c2-124">Domínio</span><span class="sxs-lookup"><span data-stu-id="cb1c2-124">Domain</span></span> | <span data-ttu-id="cb1c2-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="cb1c2-125">Geometry</span></span> | <span data-ttu-id="cb1c2-126">16x16</span><span class="sxs-lookup"><span data-stu-id="cb1c2-126">Pixel</span></span> | <span data-ttu-id="cb1c2-127">Computação</span><span class="sxs-lookup"><span data-stu-id="cb1c2-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="cb1c2-128">X</span><span class="sxs-lookup"><span data-stu-id="cb1c2-128">X</span></span>      | <span data-ttu-id="cb1c2-129">X</span><span class="sxs-lookup"><span data-stu-id="cb1c2-129">X</span></span>    | <span data-ttu-id="cb1c2-130">X</span><span class="sxs-lookup"><span data-stu-id="cb1c2-130">X</span></span>      | <span data-ttu-id="cb1c2-131">X</span><span class="sxs-lookup"><span data-stu-id="cb1c2-131">X</span></span>        | <span data-ttu-id="cb1c2-132">X</span><span class="sxs-lookup"><span data-stu-id="cb1c2-132">X</span></span>     | <span data-ttu-id="cb1c2-133">X</span><span class="sxs-lookup"><span data-stu-id="cb1c2-133">X</span></span>       |



 

## <a name="mimimum-shader-model"></a><span data-ttu-id="cb1c2-134">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="cb1c2-134">Mimimum Shader Model</span></span>

<span data-ttu-id="cb1c2-135">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="cb1c2-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="cb1c2-136">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="cb1c2-136">Shader Model</span></span>                                              | <span data-ttu-id="cb1c2-137">Com suporte</span><span class="sxs-lookup"><span data-stu-id="cb1c2-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="cb1c2-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="cb1c2-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="cb1c2-139">sim</span><span class="sxs-lookup"><span data-stu-id="cb1c2-139">yes</span></span>       |
| [<span data-ttu-id="cb1c2-140">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="cb1c2-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="cb1c2-141">não</span><span class="sxs-lookup"><span data-stu-id="cb1c2-141">no</span></span>        |
| [<span data-ttu-id="cb1c2-142">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="cb1c2-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cb1c2-143">não</span><span class="sxs-lookup"><span data-stu-id="cb1c2-143">no</span></span>        |
| [<span data-ttu-id="cb1c2-144">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb1c2-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cb1c2-145">não</span><span class="sxs-lookup"><span data-stu-id="cb1c2-145">no</span></span>        |
| [<span data-ttu-id="cb1c2-146">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb1c2-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cb1c2-147">não</span><span class="sxs-lookup"><span data-stu-id="cb1c2-147">no</span></span>        |
| [<span data-ttu-id="cb1c2-148">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb1c2-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cb1c2-149">não</span><span class="sxs-lookup"><span data-stu-id="cb1c2-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="cb1c2-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cb1c2-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb1c2-151">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb1c2-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





