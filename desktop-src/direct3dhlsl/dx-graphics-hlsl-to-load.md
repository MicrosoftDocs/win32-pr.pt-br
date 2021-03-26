---
title: Carregar (objeto de textura DirectX HLSL)
description: Lê dados do Texel sem nenhuma filtragem ou amostragem.
ms.assetid: a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 08d3964788a238492ff7d5189544603b35808465
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "104087205"
---
# <a name="load-directx-hlsl-texture-object"></a><span data-ttu-id="0db9a-103">Carregar (objeto de textura DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0db9a-103">Load (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="0db9a-104">Lê dados do Texel sem nenhuma filtragem ou amostragem.</span><span class="sxs-lookup"><span data-stu-id="0db9a-104">Reads texel data without any filtering or sampling.</span></span>



<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0db9a-105">Objeto Ret. Load (</span><span class="sxs-lookup"><span data-stu-id="0db9a-105">ret Object.Load(</span></span><dl> <span data-ttu-id="0db9a-106">Local typeX,</span><span class="sxs-lookup"><span data-stu-id="0db9a-106">typeX Location,</span></span><br />
<span data-ttu-id="0db9a-107">[typeX SampleIndex,]</span><span class="sxs-lookup"><span data-stu-id="0db9a-107">[typeX SampleIndex, ]</span></span><br />
<span data-ttu-id="0db9a-108">[deslocamento de typeX]</span><span class="sxs-lookup"><span data-stu-id="0db9a-108">[typeX Offset ]</span></span><br />
</dl><span data-ttu-id="0db9a-109">);</span><span class="sxs-lookup"><span data-stu-id="0db9a-109">);</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0db9a-110">typeX denota que há quatro tipos possíveis: **int**, **Int2**, **Int3** ou **INT4**.</span><span class="sxs-lookup"><span data-stu-id="0db9a-110">typeX denotes that there are four possible types: **int**, **int2**, **int3** or **int4**.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="0db9a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0db9a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0db9a-112"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*</span><span class="sxs-lookup"><span data-stu-id="0db9a-112"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span>
</dt> <dd>

<span data-ttu-id="0db9a-113">Um tipo de [objeto de textura](dx-graphics-hlsl-to-type.md) (exceto TextureCube ou TextureCubeArray).</span><span class="sxs-lookup"><span data-stu-id="0db9a-113">A [texture-object](dx-graphics-hlsl-to-type.md) type (except TextureCube or TextureCubeArray).</span></span>

</dd> <dt>

<span data-ttu-id="0db9a-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Local*</span><span class="sxs-lookup"><span data-stu-id="0db9a-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Location*</span></span>
</dt> <dd>

<span data-ttu-id="0db9a-115">\[nas \] coordenadas de textura, o último componente especifica o nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="0db9a-115">\[in\] The texture coordinates; the last component specifies the mipmap level.</span></span> <span data-ttu-id="0db9a-116">Esse método usa um sistema de coordenadas baseado em 0 e não um sistema UV de 0,0-1,0.</span><span class="sxs-lookup"><span data-stu-id="0db9a-116">This method uses a 0-based coordinate system and not a 0.0-1.0 UV system.</span></span> <span data-ttu-id="0db9a-117">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="0db9a-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="0db9a-118">Tipo de objeto</span><span class="sxs-lookup"><span data-stu-id="0db9a-118">Object Type</span></span>                                  | <span data-ttu-id="0db9a-119">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="0db9a-119">Parameter Type</span></span> |
|----------------------------------------------|----------------|
| <span data-ttu-id="0db9a-120">Buffer</span><span class="sxs-lookup"><span data-stu-id="0db9a-120">Buffer</span></span>                                       | <span data-ttu-id="0db9a-121">INT</span><span class="sxs-lookup"><span data-stu-id="0db9a-121">int</span></span>            |
| <span data-ttu-id="0db9a-122">Texture1D, Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="0db9a-122">Texture1D, Texture2DMS</span></span>                       | <span data-ttu-id="0db9a-123">int2</span><span class="sxs-lookup"><span data-stu-id="0db9a-123">int2</span></span>           |
| <span data-ttu-id="0db9a-124">Texture1DArray, 2D de textura, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="0db9a-124">Texture1DArray, Texture 2D, Texture2DMSArray</span></span> | <span data-ttu-id="0db9a-125">Int3</span><span class="sxs-lookup"><span data-stu-id="0db9a-125">int3</span></span>           |
| <span data-ttu-id="0db9a-126">Texture2DArray, Texture3D</span><span class="sxs-lookup"><span data-stu-id="0db9a-126">Texture2DArray, Texture3D</span></span>                    | <span data-ttu-id="0db9a-127">int4</span><span class="sxs-lookup"><span data-stu-id="0db9a-127">int4</span></span>           |



 

<span data-ttu-id="0db9a-128">Por exemplo, para acessar uma textura 2D, forneça coordenadas UV para os dois primeiros componentes e um nível de mipmap para o terceiro componente.</span><span class="sxs-lookup"><span data-stu-id="0db9a-128">For example, to access a 2D texture, supply UV coordinates for the first two components and a mipmap level for the third component.</span></span>

> [!Note]  
> <span data-ttu-id="0db9a-129">Quando uma ou mais das coordenadas no *local* excedem as dimensões de nível u, v ou w mipmap da textura, **Load** retorna zero em todos os componentes.</span><span class="sxs-lookup"><span data-stu-id="0db9a-129">When one or more of the coordinates in *Location* exceed the u, v, or w mipmap level dimensions of the texture, **Load** returns zero in all components.</span></span> <span data-ttu-id="0db9a-130">O Direct3D garante para retornar zero para qualquer recurso que seja acessado fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="0db9a-130">Direct3D guarantees to return zero for any resource that is accessed out of bounds.</span></span>

 

</dd> <dt>

<span data-ttu-id="0db9a-131"><span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*</span><span class="sxs-lookup"><span data-stu-id="0db9a-131"><span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*</span></span>
</dt> <dd>

<span data-ttu-id="0db9a-132">\[em \] um índice de amostragem opcional.</span><span class="sxs-lookup"><span data-stu-id="0db9a-132">\[in\] An optional sampling index.</span></span>



| <span data-ttu-id="0db9a-133">Tipo de textura</span><span class="sxs-lookup"><span data-stu-id="0db9a-133">Texture Type</span></span>                                                                                                   | <span data-ttu-id="0db9a-134">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="0db9a-134">Parameter Type</span></span> |
|----------------------------------------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="0db9a-135">Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="0db9a-135">Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="0db9a-136">sem suporte</span><span class="sxs-lookup"><span data-stu-id="0db9a-136">not supported</span></span>  |
| <span data-ttu-id="0db9a-137">Texture2DMS, Texture2DMSArray ¹</span><span class="sxs-lookup"><span data-stu-id="0db9a-137">Texture2DMS, Texture2DMSArray¹</span></span>                                                                                 | <span data-ttu-id="0db9a-138">INT</span><span class="sxs-lookup"><span data-stu-id="0db9a-138">int</span></span>            |



 

> [!Note]  
> <span data-ttu-id="0db9a-139">*SampleIndex* só está disponível para texturas com várias amostras.</span><span class="sxs-lookup"><span data-stu-id="0db9a-139">*SampleIndex* is only available for multi-sample textures.</span></span>

 

</dd> <dt>

<span data-ttu-id="0db9a-140"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Desvio*</span><span class="sxs-lookup"><span data-stu-id="0db9a-140"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Offset*</span></span>
</dt> <dd>

<span data-ttu-id="0db9a-141">\[em \] um deslocamento opcional aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="0db9a-141">\[in\] An optional offset applied to the texture coordinates before sampling.</span></span> <span data-ttu-id="0db9a-142">O tipo de deslocamento depende do tipo de objeto de textura e deve ser estático.</span><span class="sxs-lookup"><span data-stu-id="0db9a-142">The offset type is dependent on the texture-object type, and needs to be static.</span></span>



| <span data-ttu-id="0db9a-143">Tipo de textura</span><span class="sxs-lookup"><span data-stu-id="0db9a-143">Texture Type</span></span>                                             | <span data-ttu-id="0db9a-144">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="0db9a-144">Parameter Type</span></span> |
|----------------------------------------------------------|----------------|
| <span data-ttu-id="0db9a-145">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="0db9a-145">Texture1D, Texture1DArray</span></span>                                | <span data-ttu-id="0db9a-146">INT</span><span class="sxs-lookup"><span data-stu-id="0db9a-146">int</span></span>            |
| <span data-ttu-id="0db9a-147">Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="0db9a-147">Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray</span></span> | <span data-ttu-id="0db9a-148">int2</span><span class="sxs-lookup"><span data-stu-id="0db9a-148">int2</span></span>           |
| <span data-ttu-id="0db9a-149">Texture3D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="0db9a-149">Texture3D, Texture2DArray</span></span>                                | <span data-ttu-id="0db9a-150">Int3</span><span class="sxs-lookup"><span data-stu-id="0db9a-150">int3</span></span>           |



 

> [!Note]  
> <span data-ttu-id="0db9a-151">Se você usar o *deslocamento* com texturas com várias amostras, também deverá especificar *SampleIndex*.</span><span class="sxs-lookup"><span data-stu-id="0db9a-151">If you use *Offset* with multi-sample textures, you must also specify *SampleIndex*.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0db9a-152">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0db9a-152">Return Value</span></span>

<span data-ttu-id="0db9a-153">O tipo de retorno corresponde ao tipo na declaração de *objeto* .</span><span class="sxs-lookup"><span data-stu-id="0db9a-153">The return type matches the type in the *Object* declaration.</span></span> <span data-ttu-id="0db9a-154">Por exemplo, um objeto Texture2D que foi declarado como "Texture2d <uint4> MyTexture;" tem um valor de retorno do tipo **uint4**.</span><span class="sxs-lookup"><span data-stu-id="0db9a-154">For example, a Texture2D object that was declared as "Texture2d<uint4> myTexture;" has a return value of type **uint4**.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="0db9a-155">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="0db9a-155">Minimum Shader Model</span></span>

<span data-ttu-id="0db9a-156">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0db9a-156">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0db9a-157">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0db9a-157">vs\_4\_0</span></span> | <span data-ttu-id="0db9a-158">vs \_ 4 \_ 1 ¹</span><span class="sxs-lookup"><span data-stu-id="0db9a-158">vs\_4\_1¹</span></span> | <span data-ttu-id="0db9a-159">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0db9a-159">ps\_4\_0</span></span> | <span data-ttu-id="0db9a-160">PS \_ 4 \_ 1 ¹</span><span class="sxs-lookup"><span data-stu-id="0db9a-160">ps\_4\_1¹</span></span> | <span data-ttu-id="0db9a-161">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0db9a-161">gs\_4\_0</span></span> | <span data-ttu-id="0db9a-162">GS \_ 4 \_ 1 ¹</span><span class="sxs-lookup"><span data-stu-id="0db9a-162">gs\_4\_1¹</span></span> |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="0db9a-163">x</span><span class="sxs-lookup"><span data-stu-id="0db9a-163">x</span></span>        | <span data-ttu-id="0db9a-164">x</span><span class="sxs-lookup"><span data-stu-id="0db9a-164">x</span></span>         | <span data-ttu-id="0db9a-165">x</span><span class="sxs-lookup"><span data-stu-id="0db9a-165">x</span></span>        | <span data-ttu-id="0db9a-166">x</span><span class="sxs-lookup"><span data-stu-id="0db9a-166">x</span></span>         | <span data-ttu-id="0db9a-167">x</span><span class="sxs-lookup"><span data-stu-id="0db9a-167">x</span></span>        | <span data-ttu-id="0db9a-168">x</span><span class="sxs-lookup"><span data-stu-id="0db9a-168">x</span></span>         |



 

-   <span data-ttu-id="0db9a-169">O modelo do sombreador 4,1 está disponível no Direct3D 10,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="0db9a-169">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="0db9a-170">Exemplo</span><span class="sxs-lookup"><span data-stu-id="0db9a-170">Example</span></span>

<span data-ttu-id="0db9a-171">Este exemplo de código parcial é do arquivo Paint. FX no [exemplo AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="0db9a-171">This partial code example is from the Paint.fx file in the [AdvancedParticles Sample](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx).</span></span>


```
// Object Declarations
Buffer<float4> g_ParticleBuffer;

// Shader body calling the intrinsic function
float4 PSPaint(PSQuadIn input) : SV_Target
{       
    ... 
    for( int i=g_ParticleStart; i<g_NumParticles; i+=g_ParticleStep )
    {
        ... 
        // load the particle
        float4 particlePos = g_ParticleBuffer.Load( i*4 );
        float4 particleColor = g_ParticleBuffer.Load( (i*4) + 2 );
        ...     
    }
    ...
}   
```



## <a name="related-topics"></a><span data-ttu-id="0db9a-172">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0db9a-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0db9a-173">Textura-objeto</span><span class="sxs-lookup"><span data-stu-id="0db9a-173">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 




