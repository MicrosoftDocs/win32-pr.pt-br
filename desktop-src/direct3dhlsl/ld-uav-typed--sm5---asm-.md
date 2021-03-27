---
title: ld_uav_typed (SM5-ASM)
description: Acesso aleatório-a leitura de um elemento de uma exibição de acesso não ordenado tipado (UAV).
ms.assetid: E5E03311-3596-4497-9271-FE6445DBFC62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61b22392c802378c094b443c8ff2f2282909bd1f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293573"
---
# <a name="ld_uav_typed-sm5---asm"></a><span data-ttu-id="2fd4a-103">LD \_ UAV \_ tipada (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2fd4a-103">ld\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="2fd4a-104">Acesso aleatório-a leitura de um elemento de uma exibição de acesso não ordenado tipado (UAV).</span><span class="sxs-lookup"><span data-stu-id="2fd4a-104">Random-access read of an element from a typed unordered access view (UAV).</span></span>



| <span data-ttu-id="2fd4a-105">LD \_ UAV \_ digitou dst0 \[ . Mask \] , srcAddress \[ . swizzle \] , srcUAV \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="2fd4a-105">ld\_uav\_typed dst0\[.mask\], srcAddress\[.swizzle\], srcUAV\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="2fd4a-106">Item</span><span class="sxs-lookup"><span data-stu-id="2fd4a-106">Item</span></span>                                                                                                           | <span data-ttu-id="2fd4a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2fd4a-107">Description</span></span>                                                    |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="2fd4a-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="2fd4a-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="2fd4a-109">\[no \] endereço dos resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="2fd4a-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="2fd4a-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="2fd4a-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/> | <span data-ttu-id="2fd4a-111">\[em \] especifica o endereço do qual ler.</span><span class="sxs-lookup"><span data-stu-id="2fd4a-111">\[in\] Specifies the address to read from.</span></span><br/>          |
| <span data-ttu-id="2fd4a-112"><span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcUAV*</span><span class="sxs-lookup"><span data-stu-id="2fd4a-112"><span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcUAV*</span></span><br/>                 | <span data-ttu-id="2fd4a-113">\[na \] origem da qual ler.</span><span class="sxs-lookup"><span data-stu-id="2fd4a-113">\[in\] The source to read from.</span></span> <br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="2fd4a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2fd4a-114">Remarks</span></span>

<span data-ttu-id="2fd4a-115">Essa instrução executa um elemento de 4 componentes com leitura de *srcUAV* no endereço inteiro não assinado no *srcAddress*, convertido em 32 bits por componente com base no formato e gravado em *dst0* no sombreador.</span><span class="sxs-lookup"><span data-stu-id="2fd4a-115">This instruction performs a 4-component element read from *srcUAV* at the unsigned integer address in *srcAddress*, converted to 32bit per component based on the format, then written to *dst0* in the shader.</span></span>

<span data-ttu-id="2fd4a-116">*srcUAV* é um UAV (u \# ) declarado como tipado.</span><span class="sxs-lookup"><span data-stu-id="2fd4a-116">*srcUAV* is a UAV (u\#) declared as typed.</span></span> <span data-ttu-id="2fd4a-117">No entanto, o tipo de recurso associado deve ser R32 \_ uint/Santo/float.</span><span class="sxs-lookup"><span data-stu-id="2fd4a-117">However, the type of the bound resource must be R32\_UINT/SINT/FLOAT.</span></span>

<span data-ttu-id="2fd4a-118">O número de componentes inteiros sem sinal de 32 bits obtidos do endereço são determinados pela dimensionalidade do recurso declarado em *srcUAV*.</span><span class="sxs-lookup"><span data-stu-id="2fd4a-118">The number of 32-bit unsigned integer components taken from the address are determined by the dimensionality of the resource declared at *srcUAV*.</span></span> <span data-ttu-id="2fd4a-119">O endereçamento é o mesmo que a instrução [LD](ld--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="2fd4a-119">Addressing is the same as the [ld](ld--sm4---asm-.md) instruction.</span></span>

<span data-ttu-id="2fd4a-120">O endereçamento fora dos limites é o mesmo que a instrução **LD** .</span><span class="sxs-lookup"><span data-stu-id="2fd4a-120">Out of bounds addressing is the same as the **ld** instruction.</span></span>

<span data-ttu-id="2fd4a-121">O comportamento dessa instrução é idêntico à instrução **LD** se for chamado de **LD dst0 \[ . Mask \] , srcAddress \[ . swizzle \] , srcUAV \[ . swizzle \]**</span><span class="sxs-lookup"><span data-stu-id="2fd4a-121">The behavior of this instruction is identical to the **ld** instruction if called as **ld dst0\[.mask\], srcAddress\[.swizzle\], srcUAV\[.swizzle\]**</span></span>

<span data-ttu-id="2fd4a-122">Ele é inválido e não está definido para usar essa instrução em um UAV que não seja declarado como tipado.</span><span class="sxs-lookup"><span data-stu-id="2fd4a-122">It is invalid and undefined to use this instruction on a UAV that is not declared as typed.</span></span> <span data-ttu-id="2fd4a-123">Fazer isso em um UAV estruturado ou de tipo não é válido.</span><span class="sxs-lookup"><span data-stu-id="2fd4a-123">Doing this on a structured or typeless UAV is invalid.</span></span>

<span data-ttu-id="2fd4a-124">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="2fd4a-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2fd4a-125">Vértice</span><span class="sxs-lookup"><span data-stu-id="2fd4a-125">Vertex</span></span> | <span data-ttu-id="2fd4a-126">Envoltória</span><span class="sxs-lookup"><span data-stu-id="2fd4a-126">Hull</span></span> | <span data-ttu-id="2fd4a-127">Domínio</span><span class="sxs-lookup"><span data-stu-id="2fd4a-127">Domain</span></span> | <span data-ttu-id="2fd4a-128">Geometria</span><span class="sxs-lookup"><span data-stu-id="2fd4a-128">Geometry</span></span> | <span data-ttu-id="2fd4a-129">16x16</span><span class="sxs-lookup"><span data-stu-id="2fd4a-129">Pixel</span></span> | <span data-ttu-id="2fd4a-130">Computação</span><span class="sxs-lookup"><span data-stu-id="2fd4a-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2fd4a-131">X</span><span class="sxs-lookup"><span data-stu-id="2fd4a-131">X</span></span>     | <span data-ttu-id="2fd4a-132">X</span><span class="sxs-lookup"><span data-stu-id="2fd4a-132">X</span></span>       |



 

<span data-ttu-id="2fd4a-133">Como UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios do sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2fd4a-133">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="2fd4a-134">Vértice</span><span class="sxs-lookup"><span data-stu-id="2fd4a-134">Vertex</span></span> | <span data-ttu-id="2fd4a-135">Envoltória</span><span class="sxs-lookup"><span data-stu-id="2fd4a-135">Hull</span></span> | <span data-ttu-id="2fd4a-136">Domínio</span><span class="sxs-lookup"><span data-stu-id="2fd4a-136">Domain</span></span> | <span data-ttu-id="2fd4a-137">Geometria</span><span class="sxs-lookup"><span data-stu-id="2fd4a-137">Geometry</span></span> | <span data-ttu-id="2fd4a-138">16x16</span><span class="sxs-lookup"><span data-stu-id="2fd4a-138">Pixel</span></span> | <span data-ttu-id="2fd4a-139">Computação</span><span class="sxs-lookup"><span data-stu-id="2fd4a-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2fd4a-140">X</span><span class="sxs-lookup"><span data-stu-id="2fd4a-140">X</span></span>      | <span data-ttu-id="2fd4a-141">X</span><span class="sxs-lookup"><span data-stu-id="2fd4a-141">X</span></span>    | <span data-ttu-id="2fd4a-142">X</span><span class="sxs-lookup"><span data-stu-id="2fd4a-142">X</span></span>      | <span data-ttu-id="2fd4a-143">X</span><span class="sxs-lookup"><span data-stu-id="2fd4a-143">X</span></span>        | <span data-ttu-id="2fd4a-144">X</span><span class="sxs-lookup"><span data-stu-id="2fd4a-144">X</span></span>     | <span data-ttu-id="2fd4a-145">X</span><span class="sxs-lookup"><span data-stu-id="2fd4a-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2fd4a-146">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="2fd4a-146">Minimum Shader Model</span></span>

<span data-ttu-id="2fd4a-147">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="2fd4a-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2fd4a-148">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="2fd4a-148">Shader Model</span></span>                                              | <span data-ttu-id="2fd4a-149">Com suporte</span><span class="sxs-lookup"><span data-stu-id="2fd4a-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2fd4a-150">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2fd4a-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2fd4a-151">sim</span><span class="sxs-lookup"><span data-stu-id="2fd4a-151">yes</span></span>       |
| [<span data-ttu-id="2fd4a-152">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="2fd4a-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2fd4a-153">não</span><span class="sxs-lookup"><span data-stu-id="2fd4a-153">no</span></span>        |
| [<span data-ttu-id="2fd4a-154">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="2fd4a-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2fd4a-155">não</span><span class="sxs-lookup"><span data-stu-id="2fd4a-155">no</span></span>        |
| [<span data-ttu-id="2fd4a-156">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2fd4a-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2fd4a-157">não</span><span class="sxs-lookup"><span data-stu-id="2fd4a-157">no</span></span>        |
| [<span data-ttu-id="2fd4a-158">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2fd4a-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2fd4a-159">não</span><span class="sxs-lookup"><span data-stu-id="2fd4a-159">no</span></span>        |
| [<span data-ttu-id="2fd4a-160">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2fd4a-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2fd4a-161">não</span><span class="sxs-lookup"><span data-stu-id="2fd4a-161">no</span></span>        |



 

<span data-ttu-id="2fd4a-162">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 dão suporte a essa instrução para UAV, SRV e TGSM.</span><span class="sxs-lookup"><span data-stu-id="2fd4a-162">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV and TGSM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fd4a-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2fd4a-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fd4a-164">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2fd4a-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





