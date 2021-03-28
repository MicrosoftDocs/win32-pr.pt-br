---
title: ld_structured (SM5-ASM)
description: Leitura de acesso aleatório de 1-4 de componentes de 32 bits de um buffer estruturado.
ms.assetid: ED572B76-FF6C-405E-9110-4B12AD5E5AE6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a34bafdcfbe0658723dd83d62507e255ff4bfa
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365249"
---
# <a name="ld_structured-sm5---asm"></a><span data-ttu-id="9d38f-103">LD \_ estruturada (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="9d38f-103">ld\_structured (sm5 - asm)</span></span>

<span data-ttu-id="9d38f-104">Leitura de acesso aleatório de 1-4 de componentes de 32 bits de um buffer estruturado.</span><span class="sxs-lookup"><span data-stu-id="9d38f-104">Random-access read of 1-4 32bit components from a structured buffer.</span></span>



| <span data-ttu-id="9d38f-105">: LD \_ dst0 \[ . Mask \] , srcAddress \[ . Selecione \_ componente \] , srcByteOffset \[ . Select \_ componente \] , src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9d38f-105">: ld\_structured dst0\[.mask\], srcAddress\[.select\_component\], srcByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="9d38f-106">Item</span><span class="sxs-lookup"><span data-stu-id="9d38f-106">Item</span></span>                                                                                                                       | <span data-ttu-id="9d38f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d38f-107">Description</span></span>                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d38f-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="9d38f-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="9d38f-109">\[no \] endereço dos resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="9d38f-109">\[in\] The address of the results of the operation.</span></span><br/>                                                                                             |
| <span data-ttu-id="9d38f-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="9d38f-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>             | <span data-ttu-id="9d38f-111">\[in \] especifica o índice da estrutura a ser lida.</span><span class="sxs-lookup"><span data-stu-id="9d38f-111">\[in\] Specifies the index of the structure to read.</span></span><br/>                                                                                            |
| <span data-ttu-id="9d38f-112"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span><span class="sxs-lookup"><span data-stu-id="9d38f-112"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span></span><br/> | <span data-ttu-id="9d38f-113">\[em \] especifica o deslocamento de bytes na estrutura da qual começar a ler.</span><span class="sxs-lookup"><span data-stu-id="9d38f-113">\[in\] Specifies the byte offset in the structure to start reading from.</span></span> <br/>                                                                       |
| <span data-ttu-id="9d38f-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9d38f-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="9d38f-115">O buffer do qual ler.</span><span class="sxs-lookup"><span data-stu-id="9d38f-115">The buffer to read from.</span></span> <span data-ttu-id="9d38f-116">Esse parâmetro deve ser um SRV (t \# ), UAV (u \# ).</span><span class="sxs-lookup"><span data-stu-id="9d38f-116">This parameter must be a SRV (t\#), UAV (u\#).</span></span> <span data-ttu-id="9d38f-117">No sombreador de computação, ele também pode ser a memória compartilhada do grupo de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="9d38f-117">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="9d38f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d38f-118">Remarks</span></span>

<span data-ttu-id="9d38f-119">Os dados lidos da estrutura são equivalentes ao seguinte pseudocódigo: onde temos o deslocamento, o endereço, o ponteiro para o conteúdo do buffer, o stride da fonte e os dados armazenados linearmente.</span><span class="sxs-lookup"><span data-stu-id="9d38f-119">The data read from the structure is equivalent to the following pseudocode: where we have the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;         // from SRV or UAV
                    UINT BufferStride;            // from base resource
                    UINT srcAddress, srcByteOffset;   // from source registers
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + BufferStride * srcByteOffset
                                + srcOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

<span data-ttu-id="9d38f-120">Esse pseudocódigo mostra como a operação funciona, mas os dados reais não precisam ser armazenados linearmente.</span><span class="sxs-lookup"><span data-stu-id="9d38f-120">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="9d38f-121">Se os dados não forem armazenados linearmente, a operação real da instrução precisará corresponder ao comportamento da operação acima.</span><span class="sxs-lookup"><span data-stu-id="9d38f-121">If the data is not stored linearly, the actual operation of the instruction needs to match the behavior of the above operation.</span></span>

<span data-ttu-id="9d38f-122">O endereçamento fora dos limites em u \# /t \# de qualquer componente de 32 bits especificado retorna 0 para esse componente, exceto *se srcByteOffset*, além de swizzle for o que faz com que o acesso a você/t seja \# \# indefinido, o valor retornado para todos os componentes é indefinida.</span><span class="sxs-lookup"><span data-stu-id="9d38f-122">Out of bounds addressing on u\#/t\# of any given 32-bit component returns 0 for that component, except if *srcByteOffset*, plus swizzle is what causes out of bounds access to u\#/t\#, the returned value for all component(s) is undefined.</span></span>

<span data-ttu-id="9d38f-123">O endereçamento fora dos limites em g \# (os limites desse g específico \# , em oposição a toda a memória compartilhada) para qualquer componente de 32 bits determinado retorna um resultado indefinido.</span><span class="sxs-lookup"><span data-stu-id="9d38f-123">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component returns an undefined result.</span></span>

<span data-ttu-id="9d38f-124">*srcByteOffset* é um argumento separado de *srcAddress* porque é normalmente um literal.</span><span class="sxs-lookup"><span data-stu-id="9d38f-124">*srcByteOffset* is a separate argument from *srcAddress* because it is commonly a literal.</span></span> <span data-ttu-id="9d38f-125">Essa separação de parâmetro não foi feita para Atomics na memória estruturada.</span><span class="sxs-lookup"><span data-stu-id="9d38f-125">This parameter separation has not been done for atomics on structured memory.</span></span>

<span data-ttu-id="9d38f-126">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 dão suporte a essa instrução para UAV, SRV e TGSM.</span><span class="sxs-lookup"><span data-stu-id="9d38f-126">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV, and TGSM.</span></span>

<span data-ttu-id="9d38f-127">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="9d38f-127">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9d38f-128">Vértice</span><span class="sxs-lookup"><span data-stu-id="9d38f-128">Vertex</span></span> | <span data-ttu-id="9d38f-129">Envoltória</span><span class="sxs-lookup"><span data-stu-id="9d38f-129">Hull</span></span> | <span data-ttu-id="9d38f-130">Domínio</span><span class="sxs-lookup"><span data-stu-id="9d38f-130">Domain</span></span> | <span data-ttu-id="9d38f-131">Geometria</span><span class="sxs-lookup"><span data-stu-id="9d38f-131">Geometry</span></span> | <span data-ttu-id="9d38f-132">16x16</span><span class="sxs-lookup"><span data-stu-id="9d38f-132">Pixel</span></span> | <span data-ttu-id="9d38f-133">Computação</span><span class="sxs-lookup"><span data-stu-id="9d38f-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9d38f-134">X</span><span class="sxs-lookup"><span data-stu-id="9d38f-134">X</span></span>      | <span data-ttu-id="9d38f-135">X</span><span class="sxs-lookup"><span data-stu-id="9d38f-135">X</span></span>    | <span data-ttu-id="9d38f-136">X</span><span class="sxs-lookup"><span data-stu-id="9d38f-136">X</span></span>      | <span data-ttu-id="9d38f-137">X</span><span class="sxs-lookup"><span data-stu-id="9d38f-137">X</span></span>        | <span data-ttu-id="9d38f-138">X</span><span class="sxs-lookup"><span data-stu-id="9d38f-138">X</span></span>     | <span data-ttu-id="9d38f-139">X</span><span class="sxs-lookup"><span data-stu-id="9d38f-139">X</span></span>       |



 

<span data-ttu-id="9d38f-140">Como UAVs estão disponíveis em todos os estágios de sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios de sombreador para UAVs para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9d38f-140">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for UAVs for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="9d38f-141">Vértice</span><span class="sxs-lookup"><span data-stu-id="9d38f-141">Vertex</span></span> | <span data-ttu-id="9d38f-142">Envoltória</span><span class="sxs-lookup"><span data-stu-id="9d38f-142">Hull</span></span> | <span data-ttu-id="9d38f-143">Domínio</span><span class="sxs-lookup"><span data-stu-id="9d38f-143">Domain</span></span> | <span data-ttu-id="9d38f-144">Geometria</span><span class="sxs-lookup"><span data-stu-id="9d38f-144">Geometry</span></span> | <span data-ttu-id="9d38f-145">16x16</span><span class="sxs-lookup"><span data-stu-id="9d38f-145">Pixel</span></span> | <span data-ttu-id="9d38f-146">Computação</span><span class="sxs-lookup"><span data-stu-id="9d38f-146">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9d38f-147">X</span><span class="sxs-lookup"><span data-stu-id="9d38f-147">X</span></span>      | <span data-ttu-id="9d38f-148">X</span><span class="sxs-lookup"><span data-stu-id="9d38f-148">X</span></span>    | <span data-ttu-id="9d38f-149">X</span><span class="sxs-lookup"><span data-stu-id="9d38f-149">X</span></span>      | <span data-ttu-id="9d38f-150">X</span><span class="sxs-lookup"><span data-stu-id="9d38f-150">X</span></span>        | <span data-ttu-id="9d38f-151">X</span><span class="sxs-lookup"><span data-stu-id="9d38f-151">X</span></span>     | <span data-ttu-id="9d38f-152">X</span><span class="sxs-lookup"><span data-stu-id="9d38f-152">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9d38f-153">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="9d38f-153">Minimum Shader Model</span></span>

<span data-ttu-id="9d38f-154">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="9d38f-154">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="9d38f-155">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="9d38f-155">Shader Model</span></span>                                              | <span data-ttu-id="9d38f-156">Com suporte</span><span class="sxs-lookup"><span data-stu-id="9d38f-156">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9d38f-157">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="9d38f-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9d38f-158">sim</span><span class="sxs-lookup"><span data-stu-id="9d38f-158">yes</span></span>       |
| [<span data-ttu-id="9d38f-159">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="9d38f-159">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9d38f-160">não</span><span class="sxs-lookup"><span data-stu-id="9d38f-160">no</span></span>        |
| [<span data-ttu-id="9d38f-161">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="9d38f-161">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9d38f-162">não</span><span class="sxs-lookup"><span data-stu-id="9d38f-162">no</span></span>        |
| [<span data-ttu-id="9d38f-163">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9d38f-163">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9d38f-164">não</span><span class="sxs-lookup"><span data-stu-id="9d38f-164">no</span></span>        |
| [<span data-ttu-id="9d38f-165">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9d38f-165">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9d38f-166">não</span><span class="sxs-lookup"><span data-stu-id="9d38f-166">no</span></span>        |
| [<span data-ttu-id="9d38f-167">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9d38f-167">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9d38f-168">não</span><span class="sxs-lookup"><span data-stu-id="9d38f-168">no</span></span>        |



 

<span data-ttu-id="9d38f-169">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 dão suporte a essa instrução para UAV, SRV e TGSM.</span><span class="sxs-lookup"><span data-stu-id="9d38f-169">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV and TGSM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d38f-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9d38f-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d38f-171">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9d38f-171">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





