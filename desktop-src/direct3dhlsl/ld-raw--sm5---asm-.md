---
title: ld_raw (SM5-ASM)
description: Leitura aleatória-acesso de componentes de 1-4 32 bits de um buffer bruto.
ms.assetid: F7DBA80D-4DD5-4271-B571-24FB6188ABFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd4a9480ef60098b394e0eff2b06043fd9a32e45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967112"
---
# <a name="ld_raw-sm5---asm"></a><span data-ttu-id="4e7f8-103">LD \_ bruto (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="4e7f8-103">ld\_raw (sm5 - asm)</span></span>

<span data-ttu-id="4e7f8-104">Leitura aleatória-acesso de componentes de 1-4 32 bits de um buffer bruto.</span><span class="sxs-lookup"><span data-stu-id="4e7f8-104">Random-access read of 1-4 32bit components from a raw buffer.</span></span>



| <span data-ttu-id="4e7f8-105">LD \_ dst0 \[ . Mask \] , srcByteOffset \[ . Select bruto \_ \] , src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="4e7f8-105">ld\_raw dst0\[.mask\], srcByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------|



 



| <span data-ttu-id="4e7f8-106">Item</span><span class="sxs-lookup"><span data-stu-id="4e7f8-106">Item</span></span>                                                                                                                       | <span data-ttu-id="4e7f8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e7f8-107">Description</span></span>                                                   |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="4e7f8-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="4e7f8-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="4e7f8-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="4e7f8-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="4e7f8-110"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span><span class="sxs-lookup"><span data-stu-id="4e7f8-110"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span></span><br/> | <span data-ttu-id="4e7f8-111">\[em \] especifica o deslocamento do qual ler.</span><span class="sxs-lookup"><span data-stu-id="4e7f8-111">\[in\] Specifies the offset to read from.</span></span><br/>          |
| <span data-ttu-id="4e7f8-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4e7f8-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="4e7f8-113">\[no \] componente a ser lido.</span><span class="sxs-lookup"><span data-stu-id="4e7f8-113">\[in\] The component to read.</span></span> <br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="4e7f8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e7f8-114">Remarks</span></span>

<span data-ttu-id="4e7f8-115">*src0* deve ser:</span><span class="sxs-lookup"><span data-stu-id="4e7f8-115">*src0* must be:</span></span>

-   <span data-ttu-id="4e7f8-116">Qualquer estágio do sombreador: SRV (t \# ) LD St</span><span class="sxs-lookup"><span data-stu-id="4e7f8-116">Any shader stage: SRV (t\#)ld st</span></span>
-   <span data-ttu-id="4e7f8-117">Sombreador de computação ou sombreador de pixel: UAV (u \# )</span><span class="sxs-lookup"><span data-stu-id="4e7f8-117">Compute shader or pixel shader: UAV (u\#)</span></span>
-   <span data-ttu-id="4e7f8-118">Sombreador de computação: memória compartilhada do grupo de threads (g \# )</span><span class="sxs-lookup"><span data-stu-id="4e7f8-118">Compute shader: thread group shared memory (g\#)</span></span>

<span data-ttu-id="4e7f8-119">*srcByteOffset* especifica o valor de base de 32 bits na memória para uma janela de 4 valores sequenciais de 32 bits nos quais os dados podem ser lidos, dependendo do swizzle e da máscara em outros parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4e7f8-119">*srcByteOffset* specifies the base 32-bit value in memory for a window of 4 sequential 32-bit values in which data may be read, depending on the swizzle and mask on other parameters.</span></span>

<span data-ttu-id="4e7f8-120">Os dados lidos do buffer bruto são equivalentes ao seguinte pseudocódigo: onde temos o deslocamento, o endereço, o ponteiro para o conteúdo do buffer, o stride da origem e os dados armazenados linearmente.</span><span class="sxs-lookup"><span data-stu-id="4e7f8-120">The data read from the raw buffer is equivalent to the following pseudocode: where we have the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;         // from src0
                    UINT srcByteOffset;           // from srcRegister
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + srcByteOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

<span data-ttu-id="4e7f8-121">O endereçamento fora dos limites em u \# /t \# de qualquer componente de 32 bits especificado retorna 0 para esse componente.</span><span class="sxs-lookup"><span data-stu-id="4e7f8-121">Out of bounds addressing on u\#/t\# of any given 32-bit component returns 0 for that component.</span></span>

<span data-ttu-id="4e7f8-122">O endereçamento fora dos limites em g \# (os limites desse g específico \# , em oposição a toda a memória compartilhada) para qualquer componente de 32 bits determinado retorna um resultado indefinido.</span><span class="sxs-lookup"><span data-stu-id="4e7f8-122">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component returns an undefined result.</span></span>

<span data-ttu-id="4e7f8-123">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 dão suporte a essa instrução para UAV e SRV.</span><span class="sxs-lookup"><span data-stu-id="4e7f8-123">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

<span data-ttu-id="4e7f8-124">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="4e7f8-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4e7f8-125">Vértice</span><span class="sxs-lookup"><span data-stu-id="4e7f8-125">Vertex</span></span> | <span data-ttu-id="4e7f8-126">Envoltória</span><span class="sxs-lookup"><span data-stu-id="4e7f8-126">Hull</span></span> | <span data-ttu-id="4e7f8-127">Domínio</span><span class="sxs-lookup"><span data-stu-id="4e7f8-127">Domain</span></span> | <span data-ttu-id="4e7f8-128">Geometria</span><span class="sxs-lookup"><span data-stu-id="4e7f8-128">Geometry</span></span> | <span data-ttu-id="4e7f8-129">16x16</span><span class="sxs-lookup"><span data-stu-id="4e7f8-129">Pixel</span></span> | <span data-ttu-id="4e7f8-130">Computação</span><span class="sxs-lookup"><span data-stu-id="4e7f8-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4e7f8-131">X</span><span class="sxs-lookup"><span data-stu-id="4e7f8-131">X</span></span>      | <span data-ttu-id="4e7f8-132">X</span><span class="sxs-lookup"><span data-stu-id="4e7f8-132">X</span></span>    | <span data-ttu-id="4e7f8-133">X</span><span class="sxs-lookup"><span data-stu-id="4e7f8-133">X</span></span>      | <span data-ttu-id="4e7f8-134">X</span><span class="sxs-lookup"><span data-stu-id="4e7f8-134">X</span></span>        | <span data-ttu-id="4e7f8-135">X</span><span class="sxs-lookup"><span data-stu-id="4e7f8-135">X</span></span>     | <span data-ttu-id="4e7f8-136">X</span><span class="sxs-lookup"><span data-stu-id="4e7f8-136">X</span></span>       |



 

<span data-ttu-id="4e7f8-137">Como UAVs estão disponíveis em todos os estágios de sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios de sombreador para UAVs para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4e7f8-137">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for UAVs for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="4e7f8-138">Vértice</span><span class="sxs-lookup"><span data-stu-id="4e7f8-138">Vertex</span></span> | <span data-ttu-id="4e7f8-139">Envoltória</span><span class="sxs-lookup"><span data-stu-id="4e7f8-139">Hull</span></span> | <span data-ttu-id="4e7f8-140">Domínio</span><span class="sxs-lookup"><span data-stu-id="4e7f8-140">Domain</span></span> | <span data-ttu-id="4e7f8-141">Geometria</span><span class="sxs-lookup"><span data-stu-id="4e7f8-141">Geometry</span></span> | <span data-ttu-id="4e7f8-142">16x16</span><span class="sxs-lookup"><span data-stu-id="4e7f8-142">Pixel</span></span> | <span data-ttu-id="4e7f8-143">Computação</span><span class="sxs-lookup"><span data-stu-id="4e7f8-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4e7f8-144">X</span><span class="sxs-lookup"><span data-stu-id="4e7f8-144">X</span></span>      | <span data-ttu-id="4e7f8-145">X</span><span class="sxs-lookup"><span data-stu-id="4e7f8-145">X</span></span>    | <span data-ttu-id="4e7f8-146">X</span><span class="sxs-lookup"><span data-stu-id="4e7f8-146">X</span></span>      | <span data-ttu-id="4e7f8-147">X</span><span class="sxs-lookup"><span data-stu-id="4e7f8-147">X</span></span>        | <span data-ttu-id="4e7f8-148">X</span><span class="sxs-lookup"><span data-stu-id="4e7f8-148">X</span></span>     | <span data-ttu-id="4e7f8-149">X</span><span class="sxs-lookup"><span data-stu-id="4e7f8-149">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4e7f8-150">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="4e7f8-150">Minimum Shader Model</span></span>

<span data-ttu-id="4e7f8-151">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="4e7f8-151">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="4e7f8-152">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="4e7f8-152">Shader Model</span></span>                                              | <span data-ttu-id="4e7f8-153">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4e7f8-153">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4e7f8-154">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4e7f8-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4e7f8-155">sim</span><span class="sxs-lookup"><span data-stu-id="4e7f8-155">yes</span></span>       |
| [<span data-ttu-id="4e7f8-156">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="4e7f8-156">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4e7f8-157">não</span><span class="sxs-lookup"><span data-stu-id="4e7f8-157">no</span></span>        |
| [<span data-ttu-id="4e7f8-158">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="4e7f8-158">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4e7f8-159">não</span><span class="sxs-lookup"><span data-stu-id="4e7f8-159">no</span></span>        |
| [<span data-ttu-id="4e7f8-160">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e7f8-160">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4e7f8-161">não</span><span class="sxs-lookup"><span data-stu-id="4e7f8-161">no</span></span>        |
| [<span data-ttu-id="4e7f8-162">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e7f8-162">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4e7f8-163">não</span><span class="sxs-lookup"><span data-stu-id="4e7f8-163">no</span></span>        |
| [<span data-ttu-id="4e7f8-164">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e7f8-164">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4e7f8-165">não</span><span class="sxs-lookup"><span data-stu-id="4e7f8-165">no</span></span>        |



 

<span data-ttu-id="4e7f8-166">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 dão suporte a essa instrução para UAV e SRV.</span><span class="sxs-lookup"><span data-stu-id="4e7f8-166">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e7f8-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e7f8-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e7f8-168">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e7f8-168">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





