---
title: store_structured (SM5-ASM)
description: Gravação aleatória-acesso de componentes de 1-4 32 bits em um UAV (modo de exibição de acesso não ordenado) de buffer estruturado.
ms.assetid: 8080B2CA-5BDA-4F01-8B2B-B85BDD58C5AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5890d30fac57923365f0bdea89fcce55f7922c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006882"
---
# <a name="store_structured-sm5---asm"></a><span data-ttu-id="70cbb-103">armazenamento \_ estruturado (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="70cbb-103">store\_structured (sm5 - asm)</span></span>

<span data-ttu-id="70cbb-104">Gravação aleatória-acesso de componentes de 1-4 32 bits em um UAV (modo de exibição de acesso não ordenado) de buffer estruturado.</span><span class="sxs-lookup"><span data-stu-id="70cbb-104">Random-access write of 1-4 32-bit components into a structured buffer unordered access view (UAV).</span></span>



| <span data-ttu-id="70cbb-105">armazene a \_ \[ máscara dst0. Write \_ \] , dstAddress \[ . Select, o \_ componente \] dstByteOffset \[ . Select \_ \] , src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="70cbb-105">store\_structured dst0\[.write\_mask\], dstAddress\[.select\_component\], dstByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="70cbb-106">Item</span><span class="sxs-lookup"><span data-stu-id="70cbb-106">Item</span></span>                                                                                                                       | <span data-ttu-id="70cbb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="70cbb-107">Description</span></span>                                                    |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="70cbb-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="70cbb-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="70cbb-109">\[no \] endereço dos resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="70cbb-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="70cbb-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="70cbb-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/>             | <span data-ttu-id="70cbb-111">\[no \] endereço no qual gravar.</span><span class="sxs-lookup"><span data-stu-id="70cbb-111">\[in\] The address at which to write.</span></span><br/>               |
| <span data-ttu-id="70cbb-112"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span><span class="sxs-lookup"><span data-stu-id="70cbb-112"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span></span><br/> | <span data-ttu-id="70cbb-113">\[no \] índice da estrutura a ser gravada.</span><span class="sxs-lookup"><span data-stu-id="70cbb-113">\[in\] The index of the structure to write.</span></span><br/>         |
| <span data-ttu-id="70cbb-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="70cbb-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="70cbb-115">\[nos \] componentes a serem gravados.</span><span class="sxs-lookup"><span data-stu-id="70cbb-115">\[in\] The components to write.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="70cbb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="70cbb-116">Remarks</span></span>

<span data-ttu-id="70cbb-117">Esta instrução executa \* componentes de 32 bits do componente de 1-4 gravados de *src0* para *Dst0* no endereço em *dstAddress* e *dstByteOffset*.</span><span class="sxs-lookup"><span data-stu-id="70cbb-117">This instruction performs 1-4 component \*32bit components written from *src0* to *dst0* at the address in *dstAddress* and *dstByteOffset*.</span></span> <span data-ttu-id="70cbb-118">Nenhuma conversão de formato.</span><span class="sxs-lookup"><span data-stu-id="70cbb-118">No format conversion.</span></span>

<span data-ttu-id="70cbb-119">*dst0* deve ser um UAV (u \# ).</span><span class="sxs-lookup"><span data-stu-id="70cbb-119">*dst0* must be a UAV (u\#).</span></span> <span data-ttu-id="70cbb-120">No sombreador de computação, ele também pode ser a memória compartilhada do grupo de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="70cbb-120">In the compute shader it can also be thread group shared memory (g\#).</span></span>

<span data-ttu-id="70cbb-121">*dstAddress* especifica o índice da estrutura a ser gravada.</span><span class="sxs-lookup"><span data-stu-id="70cbb-121">*dstAddress* specifies the index of the structure to write.</span></span>

<span data-ttu-id="70cbb-122">O local dos dados gravados é equivalente ao pseudocódigo a seguir, que mostra o deslocamento, o endereço, o ponteiro para o conteúdo do buffer, o stride da fonte e os dados armazenados linearmente.</span><span class="sxs-lookup"><span data-stu-id="70cbb-122">The location of the data written is equivalent to the following pseudocode which shows the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;             // from dst0
                    UINT BufferStride;                // from dst0
                    UINT dstAddress, dstByteOffset;   // source registers
                    BYTE *WriteLocation;              // value to calculate

                    // calculate writing location
                     WriteLocation = BufferContents 
                                + BufferStride * dstAddress 
                                + dstByteOffset;

                    // calculate the number of components to write
                    switch (dstWriteMask)
                    {
                        x:    WriteComponents = 1; break;
                        xy:   WriteComponents = 2; break;
                        xyz:  WriteComponents = 3; break;
                        xyzw: WriteComponents = 4; break;
                        default:  // only these masks are valid                              
                    }

                    // copy the data from the source register with
                    //    the swizzle applied
                    memcpy(WriteLocation, swizzle(src0, src0.swizzle), 
                             WriteComponents * sizeof(INT32));
```

<span data-ttu-id="70cbb-123">Esse pseudocódigo mostra como a operação funciona, mas os dados reais não precisam ser armazenados linearmente.</span><span class="sxs-lookup"><span data-stu-id="70cbb-123">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="70cbb-124">Se os dados não forem armazenados linearmente, a operação real da instrução precisará corresponder ao comportamento da operação acima.</span><span class="sxs-lookup"><span data-stu-id="70cbb-124">If the data is not stored linearly, the actual operation of the instruction needs to match the behavior of the above operation.</span></span>

<span data-ttu-id="70cbb-125">*dst0* só pode ter uma máscara de gravação que seja uma das seguintes:. x,. XY,. xyz,. xyzw.</span><span class="sxs-lookup"><span data-stu-id="70cbb-125">*dst0* can only have a write mask that is one of the following: .x, .xy, .xyz, .xyzw.</span></span> <span data-ttu-id="70cbb-126">A máscara de gravação determina o número de componentes de 32 bits a serem gravados sem intervalos.</span><span class="sxs-lookup"><span data-stu-id="70cbb-126">The write mask determines the number of 32-bit components to write without gaps.</span></span>

<span data-ttu-id="70cbb-127">O endereçamento fora dos limites em u \# casued by *dstAddress* significa que nada é gravado na memória fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="70cbb-127">Out of bounds addressing on u\# casued by *dstAddress* means nothing is written to the out of bounds memory.</span></span>

<span data-ttu-id="70cbb-128">Se o *dstByteOffset*, incluindo *dstWriteMask*, for o que faz com que os limites tenham acesso a você \# , todo o conteúdo do UAV se tornará indefinido.</span><span class="sxs-lookup"><span data-stu-id="70cbb-128">If the *dstByteOffset*, including *dstWriteMask*, is what causes out of bounds access to u\#, the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="70cbb-129">O endereçamento fora dos limites em g \# (os limites desse g específico \# , em oposição a toda a memória compartilhada) para qualquer componente de 32 bits determinado faz com que todo o conteúdo de toda a memória compartilhada se torne indefinido.</span><span class="sxs-lookup"><span data-stu-id="70cbb-129">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="70cbb-130">*dstByteOffset* é um argumento separado de *dstAddress* porque é normalmente um literal.</span><span class="sxs-lookup"><span data-stu-id="70cbb-130">*dstByteOffset* is a separate argument from *dstAddress* because it is commonly a literal.</span></span> <span data-ttu-id="70cbb-131">Essa separação de parâmetro não foi feita para Atomics na memória estruturada.</span><span class="sxs-lookup"><span data-stu-id="70cbb-131">This parameter separation has not been done for atomics on structured memory.</span></span>

<span data-ttu-id="70cbb-132">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 dão suporte a essa instrução para UAV e TGSM.</span><span class="sxs-lookup"><span data-stu-id="70cbb-132">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and TGSM.</span></span>

<span data-ttu-id="70cbb-133">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="70cbb-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="70cbb-134">Vértice</span><span class="sxs-lookup"><span data-stu-id="70cbb-134">Vertex</span></span> | <span data-ttu-id="70cbb-135">Envoltória</span><span class="sxs-lookup"><span data-stu-id="70cbb-135">Hull</span></span> | <span data-ttu-id="70cbb-136">Domínio</span><span class="sxs-lookup"><span data-stu-id="70cbb-136">Domain</span></span> | <span data-ttu-id="70cbb-137">Geometria</span><span class="sxs-lookup"><span data-stu-id="70cbb-137">Geometry</span></span> | <span data-ttu-id="70cbb-138">16x16</span><span class="sxs-lookup"><span data-stu-id="70cbb-138">Pixel</span></span> | <span data-ttu-id="70cbb-139">Computação</span><span class="sxs-lookup"><span data-stu-id="70cbb-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="70cbb-140">X</span><span class="sxs-lookup"><span data-stu-id="70cbb-140">X</span></span>     | <span data-ttu-id="70cbb-141">X</span><span class="sxs-lookup"><span data-stu-id="70cbb-141">X</span></span>       |



 

<span data-ttu-id="70cbb-142">Como UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios do sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="70cbb-142">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="70cbb-143">Vértice</span><span class="sxs-lookup"><span data-stu-id="70cbb-143">Vertex</span></span> | <span data-ttu-id="70cbb-144">Envoltória</span><span class="sxs-lookup"><span data-stu-id="70cbb-144">Hull</span></span> | <span data-ttu-id="70cbb-145">Domínio</span><span class="sxs-lookup"><span data-stu-id="70cbb-145">Domain</span></span> | <span data-ttu-id="70cbb-146">Geometria</span><span class="sxs-lookup"><span data-stu-id="70cbb-146">Geometry</span></span> | <span data-ttu-id="70cbb-147">16x16</span><span class="sxs-lookup"><span data-stu-id="70cbb-147">Pixel</span></span> | <span data-ttu-id="70cbb-148">Computação</span><span class="sxs-lookup"><span data-stu-id="70cbb-148">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="70cbb-149">X</span><span class="sxs-lookup"><span data-stu-id="70cbb-149">X</span></span>      | <span data-ttu-id="70cbb-150">X</span><span class="sxs-lookup"><span data-stu-id="70cbb-150">X</span></span>    | <span data-ttu-id="70cbb-151">X</span><span class="sxs-lookup"><span data-stu-id="70cbb-151">X</span></span>      | <span data-ttu-id="70cbb-152">X</span><span class="sxs-lookup"><span data-stu-id="70cbb-152">X</span></span>        | <span data-ttu-id="70cbb-153">X</span><span class="sxs-lookup"><span data-stu-id="70cbb-153">X</span></span>     | <span data-ttu-id="70cbb-154">X</span><span class="sxs-lookup"><span data-stu-id="70cbb-154">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="70cbb-155">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="70cbb-155">Minimum Shader Model</span></span>

<span data-ttu-id="70cbb-156">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="70cbb-156">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="70cbb-157">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="70cbb-157">Shader Model</span></span>                                              | <span data-ttu-id="70cbb-158">Com suporte</span><span class="sxs-lookup"><span data-stu-id="70cbb-158">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="70cbb-159">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="70cbb-159">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="70cbb-160">sim</span><span class="sxs-lookup"><span data-stu-id="70cbb-160">yes</span></span>       |
| [<span data-ttu-id="70cbb-161">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="70cbb-161">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="70cbb-162">não</span><span class="sxs-lookup"><span data-stu-id="70cbb-162">no</span></span>        |
| [<span data-ttu-id="70cbb-163">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="70cbb-163">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="70cbb-164">não</span><span class="sxs-lookup"><span data-stu-id="70cbb-164">no</span></span>        |
| [<span data-ttu-id="70cbb-165">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="70cbb-165">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="70cbb-166">não</span><span class="sxs-lookup"><span data-stu-id="70cbb-166">no</span></span>        |
| [<span data-ttu-id="70cbb-167">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="70cbb-167">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="70cbb-168">não</span><span class="sxs-lookup"><span data-stu-id="70cbb-168">no</span></span>        |
| [<span data-ttu-id="70cbb-169">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="70cbb-169">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="70cbb-170">não</span><span class="sxs-lookup"><span data-stu-id="70cbb-170">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="70cbb-171">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70cbb-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70cbb-172">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="70cbb-172">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





