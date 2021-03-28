---
title: store_uav_typed (SM5-ASM)
description: Gravação aleatória-acesso de um elemento em uma exibição de acesso não ordenado tipado (UAV).
ms.assetid: AD8E035B-DACD-4241-A05B-7D6DC8E3222C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6243e6fbb2092bac699dbbce04cb3c3478880866
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006878"
---
# <a name="store_uav_typed-sm5---asm"></a><span data-ttu-id="afae4-103">armazenar \_ UAV \_ tipados (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="afae4-103">store\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="afae4-104">Gravação aleatória-acesso de um elemento em uma exibição de acesso não ordenado tipado (UAV).</span><span class="sxs-lookup"><span data-stu-id="afae4-104">Random-access write of an element into a typed unordered access view (UAV).</span></span>



| <span data-ttu-id="afae4-105">Store \_ UAV \_ tipada dstUAV. Xyzw, dstAddress \[ . swizzle \] , src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="afae4-105">store\_uav\_typed dstUAV.xyzw, dstAddress\[.swizzle\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------|



 



| <span data-ttu-id="afae4-106">Item</span><span class="sxs-lookup"><span data-stu-id="afae4-106">Item</span></span>                                                                                                           | <span data-ttu-id="afae4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="afae4-107">Description</span></span>                                             |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="afae4-108"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="afae4-108"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/>                 | <span data-ttu-id="afae4-109">\[in \] contém o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="afae4-109">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="afae4-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="afae4-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="afae4-111">\[no \] endereço no qual gravar.</span><span class="sxs-lookup"><span data-stu-id="afae4-111">\[in\] The address at which to write.</span></span><br/>        |
| <span data-ttu-id="afae4-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="afae4-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="afae4-113">\[nos \] componentes a serem gravados.</span><span class="sxs-lookup"><span data-stu-id="afae4-113">\[in\] The components to write.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="afae4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="afae4-114">Remarks</span></span>

<span data-ttu-id="afae4-115">Essa instrução executa um elemento de 4 componentes de \* 32 bits gravado de *Src0* para *DstUAV* no endereço em *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="afae4-115">This instruction performs a 4 component \*32-bit element written from *src0* to *dstUAV* at the address in *dstAddress*.</span></span> <span data-ttu-id="afae4-116">*dstUAV* é um UAV tipado (u \# ).</span><span class="sxs-lookup"><span data-stu-id="afae4-116">*dstUAV* is a typed UAV (u\#).</span></span>

<span data-ttu-id="afae4-117">O formato de UAV determina a conversão de formato.</span><span class="sxs-lookup"><span data-stu-id="afae4-117">The format of the UAV determines format conversion.</span></span>

<span data-ttu-id="afae4-118">O número de componentes inteiros sem sinal de 32 bits obtidos do endereço são determinados pela dimensionalidade do recurso declarado em *dstUAV*.</span><span class="sxs-lookup"><span data-stu-id="afae4-118">The number of 32-bit unsigned integer components taken from the address are determined by the dimensionality of the resource declared at *dstUAV*.</span></span> <span data-ttu-id="afae4-119">Esse endereço está em elementos.</span><span class="sxs-lookup"><span data-stu-id="afae4-119">This address is in elements.</span></span>

<span data-ttu-id="afae4-120">O endereçamento fora dos limites significa que nada é gravado na memória.</span><span class="sxs-lookup"><span data-stu-id="afae4-120">Out of bounds addressing means nothing gets written to memory.</span></span>

<span data-ttu-id="afae4-121">*dstUAV* sempre tem uma máscara de gravação. xyzw.</span><span class="sxs-lookup"><span data-stu-id="afae4-121">*dstUAV* always has a .xyzw write mask.</span></span> <span data-ttu-id="afae4-122">Todos os componentes devem ser gravados.</span><span class="sxs-lookup"><span data-stu-id="afae4-122">All components must be written.</span></span>

<span data-ttu-id="afae4-123">Ele é inválido e não está definido para usar essa instrução em um UAV que não seja declarado como tipado.</span><span class="sxs-lookup"><span data-stu-id="afae4-123">It is invalid and undefined to use this instruction on a UAV that is not declared as typed.</span></span> <span data-ttu-id="afae4-124">Ou seja, fazer isso em um UAV estruturado ou de tipo não é válido.</span><span class="sxs-lookup"><span data-stu-id="afae4-124">That is, doing this on a structured or typeless UAV is invalid.</span></span>

<span data-ttu-id="afae4-125">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="afae4-125">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="afae4-126">Vértice</span><span class="sxs-lookup"><span data-stu-id="afae4-126">Vertex</span></span> | <span data-ttu-id="afae4-127">Envoltória</span><span class="sxs-lookup"><span data-stu-id="afae4-127">Hull</span></span> | <span data-ttu-id="afae4-128">Domínio</span><span class="sxs-lookup"><span data-stu-id="afae4-128">Domain</span></span> | <span data-ttu-id="afae4-129">Geometria</span><span class="sxs-lookup"><span data-stu-id="afae4-129">Geometry</span></span> | <span data-ttu-id="afae4-130">16x16</span><span class="sxs-lookup"><span data-stu-id="afae4-130">Pixel</span></span> | <span data-ttu-id="afae4-131">Computação</span><span class="sxs-lookup"><span data-stu-id="afae4-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="afae4-132">X</span><span class="sxs-lookup"><span data-stu-id="afae4-132">X</span></span>     | <span data-ttu-id="afae4-133">X</span><span class="sxs-lookup"><span data-stu-id="afae4-133">X</span></span>       |



 

<span data-ttu-id="afae4-134">Como UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios do sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="afae4-134">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="afae4-135">Vértice</span><span class="sxs-lookup"><span data-stu-id="afae4-135">Vertex</span></span> | <span data-ttu-id="afae4-136">Envoltória</span><span class="sxs-lookup"><span data-stu-id="afae4-136">Hull</span></span> | <span data-ttu-id="afae4-137">Domínio</span><span class="sxs-lookup"><span data-stu-id="afae4-137">Domain</span></span> | <span data-ttu-id="afae4-138">Geometria</span><span class="sxs-lookup"><span data-stu-id="afae4-138">Geometry</span></span> | <span data-ttu-id="afae4-139">16x16</span><span class="sxs-lookup"><span data-stu-id="afae4-139">Pixel</span></span> | <span data-ttu-id="afae4-140">Computação</span><span class="sxs-lookup"><span data-stu-id="afae4-140">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="afae4-141">X</span><span class="sxs-lookup"><span data-stu-id="afae4-141">X</span></span>      | <span data-ttu-id="afae4-142">X</span><span class="sxs-lookup"><span data-stu-id="afae4-142">X</span></span>    | <span data-ttu-id="afae4-143">X</span><span class="sxs-lookup"><span data-stu-id="afae4-143">X</span></span>      | <span data-ttu-id="afae4-144">X</span><span class="sxs-lookup"><span data-stu-id="afae4-144">X</span></span>        | <span data-ttu-id="afae4-145">X</span><span class="sxs-lookup"><span data-stu-id="afae4-145">X</span></span>     | <span data-ttu-id="afae4-146">X</span><span class="sxs-lookup"><span data-stu-id="afae4-146">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="afae4-147">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="afae4-147">Minimum Shader Model</span></span>

<span data-ttu-id="afae4-148">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="afae4-148">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="afae4-149">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="afae4-149">Shader Model</span></span>                                              | <span data-ttu-id="afae4-150">Com suporte</span><span class="sxs-lookup"><span data-stu-id="afae4-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="afae4-151">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="afae4-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="afae4-152">sim</span><span class="sxs-lookup"><span data-stu-id="afae4-152">yes</span></span>       |
| [<span data-ttu-id="afae4-153">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="afae4-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="afae4-154">não</span><span class="sxs-lookup"><span data-stu-id="afae4-154">no</span></span>        |
| [<span data-ttu-id="afae4-155">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="afae4-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="afae4-156">não</span><span class="sxs-lookup"><span data-stu-id="afae4-156">no</span></span>        |
| [<span data-ttu-id="afae4-157">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="afae4-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="afae4-158">não</span><span class="sxs-lookup"><span data-stu-id="afae4-158">no</span></span>        |
| [<span data-ttu-id="afae4-159">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="afae4-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="afae4-160">não</span><span class="sxs-lookup"><span data-stu-id="afae4-160">no</span></span>        |
| [<span data-ttu-id="afae4-161">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="afae4-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="afae4-162">não</span><span class="sxs-lookup"><span data-stu-id="afae4-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="afae4-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="afae4-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afae4-164">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="afae4-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





