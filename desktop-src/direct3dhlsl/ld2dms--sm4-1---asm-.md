---
title: ld2dms (SM 4.1-ASM)
description: Lê exemplos individuais fora de texturas com várias amostras bidimensionais.
ms.assetid: 8D92BFA8-4B22-46F3-876D-8D84BB3A96E7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9dd03b7c07f3fb25294dd0ad6aa382eb203560
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104084267"
---
# <a name="ld2dms-sm41---asm"></a><span data-ttu-id="a9837-103">ld2dms (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="a9837-103">ld2dms (sm4.1 - asm)</span></span>

<span data-ttu-id="a9837-104">Lê exemplos individuais fora de texturas com várias amostras bidimensionais.</span><span class="sxs-lookup"><span data-stu-id="a9837-104">Reads individual samples out of 2-dimensional multi-sample textures.</span></span>



| <span data-ttu-id="a9837-105">ld2dms \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , sampleIndex (operando escalar)</span><span class="sxs-lookup"><span data-stu-id="a9837-105">ld2dms\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], sampleIndex (scalar operand)</span></span> |
|------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="a9837-106">Item</span><span class="sxs-lookup"><span data-stu-id="a9837-106">Item</span></span>                                                                                                               | <span data-ttu-id="a9837-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9837-107">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9837-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a9837-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="a9837-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="a9837-109">\[in\] The address of result of the operation.</span></span> <br/>                                                                 |
| <span data-ttu-id="a9837-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="a9837-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="a9837-111">\[nas \] coordenadas de textura necessárias para executar o exemplo.</span><span class="sxs-lookup"><span data-stu-id="a9837-111">\[in\] The texture coordinates needed to perform the sample.</span></span><br/>                                                    |
| <span data-ttu-id="a9837-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="a9837-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="a9837-113">\[em \] um registro de textura (t \# ) que deve ter sido declarado identificando a textura ou o buffer a ser obtido</span><span class="sxs-lookup"><span data-stu-id="a9837-113">\[in\] A texture register (t\#) which must have been declared identifying which Texture or Buffer to fetch from</span></span><br/> |
| <span data-ttu-id="a9837-114"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span><span class="sxs-lookup"><span data-stu-id="a9837-114"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span></span><br/> | <span data-ttu-id="a9837-115">\[em \] Idendifies, os exemplos a serem lidos em *srcResource*.</span><span class="sxs-lookup"><span data-stu-id="a9837-115">\[in\] Idendifies the samples to read from *srcResource*.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="a9837-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9837-116">Remarks</span></span>

<span data-ttu-id="a9837-117">Essa instrução é uma alternativa simplificada para a instrução de [exemplo](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="a9837-117">This instruction is a simplified alternative to the [sample](sample--sm4---asm-.md) instruction.</span></span> <span data-ttu-id="a9837-118">Ele busca dados da textura especificada sem nenhuma filtragem (por exemplo, amostragem de ponto) usando o inteiro fornecido *srcAddress* e *sampleIndex*.</span><span class="sxs-lookup"><span data-stu-id="a9837-118">It fetches data from the specified Texture without any filtering (e.g. point sampling) using the provided integer *srcAddress* and *sampleIndex*.</span></span>

<span data-ttu-id="a9837-119">o *srcAddress* fornece o conjunto de coordenadas de textura necessárias para executar o exemplo na forma de inteiros sem sinal.</span><span class="sxs-lookup"><span data-stu-id="a9837-119">*srcAddress* provides the set of texture coordinates needed to perform the sample in the form of unsigned integers.</span></span> <span data-ttu-id="a9837-120">Se *srcAddress* estiver fora do intervalo \[ 0... ( \# texels na dimensão-1) \] , **ld2dms** sempre retorna 0 em todos os componentes presentes no formato do recurso, e os padrões (0, 0, 0, 1,0 f/0x00000001) para componentes ausentes.</span><span class="sxs-lookup"><span data-stu-id="a9837-120">If *srcAddress* is out of the range\[0...(\#texels in dimension -1)\], **ld2dms** always returns 0 in all components present in the format of the resource, and defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

<span data-ttu-id="a9837-121">*sampleIndex* não precisa ser um literal.</span><span class="sxs-lookup"><span data-stu-id="a9837-121">*sampleIndex* does not have to be a literal.</span></span> <span data-ttu-id="a9837-122">A contagem de várias amostras não precisa ser especificada no recurso de textura e funciona com exibições de profundidade ou de estêncil.</span><span class="sxs-lookup"><span data-stu-id="a9837-122">The multi-sample count does not have to be specified on the texture resource, and it works with depth or stencil views.</span></span>

<span data-ttu-id="a9837-123">Um aplicativo que deseja ter um controle mais flexível sobre o comportamento de endereço fora do intervalo deve usar a instrução de **exemplo** , pois ele honra o comportamento de encapsulamento/espelho/fixe/Border definido como um estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="a9837-123">An application wishing any more flexible control over out-of-range address behavior should use the **sample** instruction instead, as it honors address wrap/mirror/clamp/border behavior defined as sampler state.</span></span>

<span data-ttu-id="a9837-124">*srcAddress. b* (post-swizzle) é ignorado para Texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="a9837-124">*srcAddress.b* (post-swizzle) is ignored for Texture2Ds.</span></span> <span data-ttu-id="a9837-125">Se o valor estiver fora do intervalo de índices de matriz disponíveis \[ 0... ( tamanho da matriz-1) \] , em seguida, **ld2dms** sempre retorna 0 em todos os componentes presentes no formato do recurso, e os padrões (0, 0, 0, 1,0 f/0x00000001) para componentes ausentes.</span><span class="sxs-lookup"><span data-stu-id="a9837-125">If the value is out of the range of available array indices \[0...(array size-1)\], then **ld2dms** always returns 0 in all components present in the format of the resource, and defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

<span data-ttu-id="a9837-126">Para matrizes Texture2D, *srcAddress. b* (post-swizzle) fornece o índice de matriz.</span><span class="sxs-lookup"><span data-stu-id="a9837-126">For Texture2D Arrays, *srcAddress.b* (post-swizzle) provides the array index.</span></span> <span data-ttu-id="a9837-127">Oherwise ele tem o mesmo comportamento que Texture2D.</span><span class="sxs-lookup"><span data-stu-id="a9837-127">Oherwise it has the same behavior as Texture2D.</span></span>

<span data-ttu-id="a9837-128">*srcAddress. a* (post-swizzle) é sempre ignorada.</span><span class="sxs-lookup"><span data-stu-id="a9837-128">*srcAddress.a* (post-swizzle) is always ignored.</span></span> <span data-ttu-id="a9837-129">O compilador HLSL nunca produzirá nada lá.</span><span class="sxs-lookup"><span data-stu-id="a9837-129">The HLSL compiler will never output anything there.</span></span>

<span data-ttu-id="a9837-130">*srcResource* é um registro de textura (t \# ) que deve ter sido declarado (22.3.11), identificando a qual textura buscar.</span><span class="sxs-lookup"><span data-stu-id="a9837-130">*srcResource* is a texture register (t\#) which must have been declared(22.3.11), identifying which Texture to fetch from.</span></span>

<span data-ttu-id="a9837-131">A busca de t \# que não tem nada associado retorna 0 para todos os componentes.</span><span class="sxs-lookup"><span data-stu-id="a9837-131">Fetching from t\# that has nothing bound to it returns 0 for all components.</span></span>

### <a name="address-offset"></a><span data-ttu-id="a9837-132">Deslocamento de endereço</span><span class="sxs-lookup"><span data-stu-id="a9837-132">Address Offset</span></span>

<span data-ttu-id="a9837-133">O \[ \_ sufixo opcional aoffimmi (u, v, w) \] (deslocamento de endereço por inteiro imediato) indica que as coordenadas de textura para o **ld2dms** devem ser deslocadas por um conjunto de valores de constante de inteiro de espaço de Texel imediato fornecido.</span><span class="sxs-lookup"><span data-stu-id="a9837-133">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the **ld2dms** are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="a9837-134">Os valores literais são um conjunto de números de complemento de 4 bits 2, com intervalo de números inteiros \[ -8, 7 \] .</span><span class="sxs-lookup"><span data-stu-id="a9837-134">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span>

<span data-ttu-id="a9837-135">Os deslocamentos são adicionados às coordenadas de textura, no espaço Texel.</span><span class="sxs-lookup"><span data-stu-id="a9837-135">The offsets are added to the texture coordinates, in texel space.</span></span>

<span data-ttu-id="a9837-136">Deslocamentos de endereço não são aplicados ao longo do eixo de matriz de matrizes Texture1D/2D.</span><span class="sxs-lookup"><span data-stu-id="a9837-136">Address offsets are not applied along the array axis of Texture1D/2D Arrays.</span></span>

<span data-ttu-id="a9837-137">Os componentes *\_ aoffimmi v, w* são ignorados para Texture1Ds.</span><span class="sxs-lookup"><span data-stu-id="a9837-137">The *\_aoffimmi v,w* components are ignored for Texture1Ds.</span></span>

<span data-ttu-id="a9837-138">O componente *\_ aoffimmi w* é ignorado para Texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="a9837-138">The *\_aoffimmi w* component is ignored for Texture2Ds.</span></span>

<span data-ttu-id="a9837-139">Como as coordenadas de textura para **ld2dms** são inteiros não assinados, se o deslocamento fizer com que o endereço fique abaixo de zero, ele será encapsulado em um endereço grande e resultará em um acesso fora dos limites, que como **LD** retorna 0 em todos os componentes presentes no formato do recurso e os padrões (0, 0, 0, 1,0 f/0x00000001) para componentes ausentes.</span><span class="sxs-lookup"><span data-stu-id="a9837-139">Because the texture coordinates for **ld2dms** are unsigned integers, if the offset causes the address to go below zero, it will wrap to a large address, and result in an out of bounds access, which like **ld** returns 0 in all components present in the format of the resource, and the defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

### <a name="sample-number"></a><span data-ttu-id="a9837-140">Número de exemplo</span><span class="sxs-lookup"><span data-stu-id="a9837-140">Sample Number</span></span>

<span data-ttu-id="a9837-141">**ld2dms** está disponível para uso em qualquer recurso.</span><span class="sxs-lookup"><span data-stu-id="a9837-141">**ld2dms** is available for use on any resource.</span></span> <span data-ttu-id="a9837-142">o **ld2dms** Opera de forma idêntica a **LD** , exceto em recursos de multsample 2D, usando o operando de *sampleIndex* adicional (baseado em 0) para identificar qual exemplo ler do recurso.</span><span class="sxs-lookup"><span data-stu-id="a9837-142">**ld2dms** operates identically to **ld** except on 2D multsample resources, by using the additional (0-based) *sampleIndex* operand to identify which sample to read from the resource.</span></span>

<span data-ttu-id="a9837-143">O resultado da especificação de um *sampleIndex* que exceda o número de amostras no recurso é indefinido, mas não pode retornar dados fora do espaço de endereço do contexto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a9837-143">The result of specifying a *sampleIndex* that exceeds the number of samples in the resource is undefined, but cannot return data outside of the address space of the device context.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="a9837-144">Controle de tipo de retorno</span><span class="sxs-lookup"><span data-stu-id="a9837-144">Return Type Control</span></span>

<span data-ttu-id="a9837-145">O formato de dados retornado por **ld2dms** para o registro de destino é determinado da mesma maneira que descrito para a instrução de **exemplo** .</span><span class="sxs-lookup"><span data-stu-id="a9837-145">The data format returned by **ld2dms** to the destination register is determined in the same way as described for the **sample** instruction.</span></span> <span data-ttu-id="a9837-146">Ele se baseia no formato associado ao parâmetro *srcResource* (t \# ).</span><span class="sxs-lookup"><span data-stu-id="a9837-146">It is based on the format bound to the *srcResource* parameter (t\#).</span></span>

<span data-ttu-id="a9837-147">Assim como acontece com a instrução de **exemplo** , os valores retornados para **ld2dms** são 4 vetores com padrões específicos de formato para componentes que não estão presentes no formato.</span><span class="sxs-lookup"><span data-stu-id="a9837-147">As with the **sample** instruction, returned values for **ld2dms** are 4-vectors with format-specific defaults for components not present in the format.</span></span> <span data-ttu-id="a9837-148">O swizzle em *srcResource* determina como swizzle o resultado de 4 componentes de volta da carga de textura, após o qual. Mask no *dest* determina quais componentes no *dest* são atualizados.</span><span class="sxs-lookup"><span data-stu-id="a9837-148">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture load, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="a9837-149">Quando um valor float de 32 bits é lido por **ld2dms** em um registro de 32 bits, os bits são intocados; ou seja, os valores desnormals permanecem desnormalizados.</span><span class="sxs-lookup"><span data-stu-id="a9837-149">When a 32-bit float value is read by **ld2dms** into a 32-bit register, the bits are untouched; that is, denormal values remain denormal.</span></span> <span data-ttu-id="a9837-150">Isso é diferente da instrução de **exemplo** .</span><span class="sxs-lookup"><span data-stu-id="a9837-150">This is unlike the **sample** instruction.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="a9837-151">Detalhes diversos</span><span class="sxs-lookup"><span data-stu-id="a9837-151">Miscellaneous Details</span></span>

<span data-ttu-id="a9837-152">Como não há nenhuma filtragem associada a essa instrução, conceitos como LOD Bias não se aplicam.</span><span class="sxs-lookup"><span data-stu-id="a9837-152">As there is no filtering associated with this instruction, concepts like LOD bias do not apply.</span></span> <span data-ttu-id="a9837-153">Portanto, não há nenhum parâmetro de *s \# de amostra* .</span><span class="sxs-lookup"><span data-stu-id="a9837-153">Accordingly there is no *sampler s\#* parameter.</span></span>

### <a name="restrictions"></a><span data-ttu-id="a9837-154">Restrições</span><span class="sxs-lookup"><span data-stu-id="a9837-154">Restrictions</span></span>

-   <span data-ttu-id="a9837-155">*srcResource* deve ser um \# registro t e não um TextureCube, Texture1D ou Texture1DArray.</span><span class="sxs-lookup"><span data-stu-id="a9837-155">*srcResource* must be a t\# register, and not a TextureCube, Texture1D or Texture1DArray.</span></span> <span data-ttu-id="a9837-156">*srcResource* não pode ser um ConstantBuffer, que não pode ser associado a \# registros t.</span><span class="sxs-lookup"><span data-stu-id="a9837-156">*srcResource* cannot be a ConstantBuffer, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="a9837-157">O endereçamento relativo em *srcResource* não é permitido.</span><span class="sxs-lookup"><span data-stu-id="a9837-157">Relative addressing on *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="a9837-158">*srcAddress* e *sampleIndex* devem ser um registro temporário (r \# /x \# ), uma constante (CB \# ) ou de entrada (v \# ).</span><span class="sxs-lookup"><span data-stu-id="a9837-158">*srcAddress* and *sampleIndex* must be a temp (r\#/x\#), constant (cb\#) or input (v\#) register.</span></span>
-   <span data-ttu-id="a9837-159">*dest* deve ser um registro temporário (r \# /x \# ) ou saída (o \* \# ).</span><span class="sxs-lookup"><span data-stu-id="a9837-159">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>

<span data-ttu-id="a9837-160">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a9837-160">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a9837-161">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="a9837-161">Vertex Shader</span></span> | <span data-ttu-id="a9837-162">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="a9837-162">Geometry Shader</span></span> | <span data-ttu-id="a9837-163">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="a9837-163">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a9837-164">x</span><span class="sxs-lookup"><span data-stu-id="a9837-164">x</span></span>             | <span data-ttu-id="a9837-165">x</span><span class="sxs-lookup"><span data-stu-id="a9837-165">x</span></span>               | <span data-ttu-id="a9837-166">x</span><span class="sxs-lookup"><span data-stu-id="a9837-166">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a9837-167">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="a9837-167">Minimum Shader Model</span></span>

<span data-ttu-id="a9837-168">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a9837-168">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a9837-169">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="a9837-169">Shader Model</span></span>                                              | <span data-ttu-id="a9837-170">Com suporte</span><span class="sxs-lookup"><span data-stu-id="a9837-170">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a9837-171">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a9837-171">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a9837-172">sim</span><span class="sxs-lookup"><span data-stu-id="a9837-172">yes</span></span>       |
| [<span data-ttu-id="a9837-173">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="a9837-173">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a9837-174">sim</span><span class="sxs-lookup"><span data-stu-id="a9837-174">yes</span></span>       |
| [<span data-ttu-id="a9837-175">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a9837-175">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a9837-176">não</span><span class="sxs-lookup"><span data-stu-id="a9837-176">no</span></span>        |
| [<span data-ttu-id="a9837-177">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a9837-177">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a9837-178">não</span><span class="sxs-lookup"><span data-stu-id="a9837-178">no</span></span>        |
| [<span data-ttu-id="a9837-179">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a9837-179">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a9837-180">não</span><span class="sxs-lookup"><span data-stu-id="a9837-180">no</span></span>        |
| [<span data-ttu-id="a9837-181">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a9837-181">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a9837-182">não</span><span class="sxs-lookup"><span data-stu-id="a9837-182">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a9837-183">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a9837-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9837-184">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a9837-184">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





