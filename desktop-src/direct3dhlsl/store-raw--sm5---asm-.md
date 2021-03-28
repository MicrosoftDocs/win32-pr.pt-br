---
title: store_raw (SM5-ASM)
description: Gravação de acesso aleatório de 1-4 de componentes de 32 bits em memória de tipo insuficiente.
ms.assetid: D166116A-CF4E-4020-9F6A-F9CEEFCDAB21
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44b4d22a576853fb8b7d2c43fcb6a2d7fc9a448
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365275"
---
# <a name="store_raw-sm5---asm"></a><span data-ttu-id="830ac-103">armazenamento \_ bruto (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="830ac-103">store\_raw (sm5 - asm)</span></span>

<span data-ttu-id="830ac-104">Gravação de acesso aleatório de 1-4 de componentes de 32 bits em memória de tipo insuficiente.</span><span class="sxs-lookup"><span data-stu-id="830ac-104">Random-access write of 1-4 32bit components into typeless memory.</span></span>



| <span data-ttu-id="830ac-105">armazenar a \_ \[ máscara dst0. Write, o \_ \] componente dstByteOffset \[ . Select \_ , o \] src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="830ac-105">store\_raw dst0\[.write\_mask\], dstByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------|



 



| <span data-ttu-id="830ac-106">Item</span><span class="sxs-lookup"><span data-stu-id="830ac-106">Item</span></span>                                                                                                                       | <span data-ttu-id="830ac-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="830ac-107">Description</span></span>                                |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="830ac-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="830ac-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="830ac-109">\[no \] endereço de memória.</span><span class="sxs-lookup"><span data-stu-id="830ac-109">\[in\] The memory address.</span></span><br/>      |
| <span data-ttu-id="830ac-110"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span><span class="sxs-lookup"><span data-stu-id="830ac-110"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span></span><br/> | <span data-ttu-id="830ac-111">\[no \] deslocamento.</span><span class="sxs-lookup"><span data-stu-id="830ac-111">\[in\] The offset.</span></span><br/>              |
| <span data-ttu-id="830ac-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="830ac-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="830ac-113">\[nos \] componentes a serem gravados.</span><span class="sxs-lookup"><span data-stu-id="830ac-113">\[in\] The components to write.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="830ac-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="830ac-114">Remarks</span></span>

<span data-ttu-id="830ac-115">Esta instrução executa \* componentes de 32 bits de componente 1-4 gravados de *src0* para *Dst0* no deslocamento em *dstByteOffset*.</span><span class="sxs-lookup"><span data-stu-id="830ac-115">This instruction performs 1-4 component \*32-bit components written from *src0* to *dst0* at the offset in *dstByteOffset*.</span></span> <span data-ttu-id="830ac-116">Não há conversão de formato.</span><span class="sxs-lookup"><span data-stu-id="830ac-116">There is no format conversion.</span></span>

<span data-ttu-id="830ac-117">*dst0* deve ser um UAV (u \# ) ou, no sombreador de computação, ele também pode ser a memória compartilhada do grupo de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="830ac-117">*dst0* must be a UAV (u\#), or in the compute shader it can also be thread group shared memory (g\#).</span></span>

<span data-ttu-id="830ac-118">*dstByteOffset* especifica o valor de base de 32 bits na memória para uma janela de 4 valores sequenciais de 32 bits nos quais os dados podem ser gravados, dependendo do swizzle e da máscara em outros parâmetros.</span><span class="sxs-lookup"><span data-stu-id="830ac-118">*dstByteOffset* specifies the base 32-bit value in memory for a window of 4 sequential 32-bit values in which data may be written, depending on the swizzle and mask on other parameters.</span></span>

<span data-ttu-id="830ac-119">O local dos dados gravados é equivalente ao pseudocódigo a seguir, que mostra o endereço, o ponteiro para o conteúdo do buffer e os dados armazenados linearmente.</span><span class="sxs-lookup"><span data-stu-id="830ac-119">The location of the data written is equivalent to the following pseudocode which show the address, pointer to the buffer contents, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;          // from src0
                    UINT dstByteOffset;            // source register
                    BYTE *WriteLocation;           // value to calculate

                    // calculate writing location
                    WriteLocation = BufferContents 
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
                             WriteComponents * sizeof(UINT32));
```

<span data-ttu-id="830ac-120">Esse pseudocódigo mostra como a operação funciona, mas os dados reais não precisam ser armazenados linearmente.</span><span class="sxs-lookup"><span data-stu-id="830ac-120">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="830ac-121">*dst0* só pode ter uma máscara de gravação que seja uma das seguintes:. x,. XY,. xyz,. xyzw.</span><span class="sxs-lookup"><span data-stu-id="830ac-121">*dst0* can only have a write mask that is one of the following: .x, .xy, .xyz, .xyzw.</span></span> <span data-ttu-id="830ac-122">A máscara de gravação determina o número de componentes de 32 bits a serem gravados sem intervalos.</span><span class="sxs-lookup"><span data-stu-id="830ac-122">The write mask determines the number of 32bit components to write without gaps.</span></span>

<span data-ttu-id="830ac-123">O endereçamento fora dos limites em u \# significa que nada é gravado na memória fora dos limites; qualquer parte que esteja em limites é gravada corretamente.</span><span class="sxs-lookup"><span data-stu-id="830ac-123">Out of bounds addressing on u\# means nothing is written to the out of bounds memory; any part that is in bounds is written correctly.</span></span>

<span data-ttu-id="830ac-124">O endereçamento fora dos limites em g \# (os limites desse g específico \# , em oposição a toda a memória compartilhada) para qualquer componente de 32 bits determinado faz com que todo o conteúdo de toda a memória compartilhada se torne indefinido.</span><span class="sxs-lookup"><span data-stu-id="830ac-124">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="830ac-125">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 dão suporte a essa instrução para UAV.</span><span class="sxs-lookup"><span data-stu-id="830ac-125">cs\_4\_0 and cs\_4\_1 support this instruction for UAV.</span></span>

<span data-ttu-id="830ac-126">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="830ac-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="830ac-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="830ac-127">Vertex</span></span> | <span data-ttu-id="830ac-128">Envoltória</span><span class="sxs-lookup"><span data-stu-id="830ac-128">Hull</span></span> | <span data-ttu-id="830ac-129">Domínio</span><span class="sxs-lookup"><span data-stu-id="830ac-129">Domain</span></span> | <span data-ttu-id="830ac-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="830ac-130">Geometry</span></span> | <span data-ttu-id="830ac-131">16x16</span><span class="sxs-lookup"><span data-stu-id="830ac-131">Pixel</span></span> | <span data-ttu-id="830ac-132">Computação</span><span class="sxs-lookup"><span data-stu-id="830ac-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="830ac-133">X</span><span class="sxs-lookup"><span data-stu-id="830ac-133">X</span></span>     | <span data-ttu-id="830ac-134">X</span><span class="sxs-lookup"><span data-stu-id="830ac-134">X</span></span>       |



 

<span data-ttu-id="830ac-135">Como UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios do sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="830ac-135">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="830ac-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="830ac-136">Vertex</span></span> | <span data-ttu-id="830ac-137">Envoltória</span><span class="sxs-lookup"><span data-stu-id="830ac-137">Hull</span></span> | <span data-ttu-id="830ac-138">Domínio</span><span class="sxs-lookup"><span data-stu-id="830ac-138">Domain</span></span> | <span data-ttu-id="830ac-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="830ac-139">Geometry</span></span> | <span data-ttu-id="830ac-140">16x16</span><span class="sxs-lookup"><span data-stu-id="830ac-140">Pixel</span></span> | <span data-ttu-id="830ac-141">Computação</span><span class="sxs-lookup"><span data-stu-id="830ac-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="830ac-142">X</span><span class="sxs-lookup"><span data-stu-id="830ac-142">X</span></span>      | <span data-ttu-id="830ac-143">X</span><span class="sxs-lookup"><span data-stu-id="830ac-143">X</span></span>    | <span data-ttu-id="830ac-144">X</span><span class="sxs-lookup"><span data-stu-id="830ac-144">X</span></span>      | <span data-ttu-id="830ac-145">X</span><span class="sxs-lookup"><span data-stu-id="830ac-145">X</span></span>        | <span data-ttu-id="830ac-146">X</span><span class="sxs-lookup"><span data-stu-id="830ac-146">X</span></span>     | <span data-ttu-id="830ac-147">X</span><span class="sxs-lookup"><span data-stu-id="830ac-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="830ac-148">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="830ac-148">Minimum Shader Model</span></span>

<span data-ttu-id="830ac-149">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="830ac-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="830ac-150">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="830ac-150">Shader Model</span></span>                                              | <span data-ttu-id="830ac-151">Com suporte</span><span class="sxs-lookup"><span data-stu-id="830ac-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="830ac-152">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="830ac-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="830ac-153">sim</span><span class="sxs-lookup"><span data-stu-id="830ac-153">yes</span></span>       |
| [<span data-ttu-id="830ac-154">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="830ac-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="830ac-155">não</span><span class="sxs-lookup"><span data-stu-id="830ac-155">no</span></span>        |
| [<span data-ttu-id="830ac-156">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="830ac-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="830ac-157">não</span><span class="sxs-lookup"><span data-stu-id="830ac-157">no</span></span>        |
| [<span data-ttu-id="830ac-158">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="830ac-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="830ac-159">não</span><span class="sxs-lookup"><span data-stu-id="830ac-159">no</span></span>        |
| [<span data-ttu-id="830ac-160">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="830ac-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="830ac-161">não</span><span class="sxs-lookup"><span data-stu-id="830ac-161">no</span></span>        |
| [<span data-ttu-id="830ac-162">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="830ac-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="830ac-163">não</span><span class="sxs-lookup"><span data-stu-id="830ac-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="830ac-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="830ac-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="830ac-165">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="830ac-165">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





