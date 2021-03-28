---
title: exemplo (sm4-ASM)
description: Amostras de dados do elemento/textura especificado usando o endereço especificado e o modo de filtragem identificados pelo determinado exemplo. | exemplo (sm4-ASM)
ms.assetid: 9055D3EE-FD4A-418C-A743-D12E8BDF69FF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397aba4a165f13721e73f87da82cff3e8918e33b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930433"
---
# <a name="sample-sm4---asm"></a><span data-ttu-id="0c02f-104">exemplo (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="0c02f-104">sample (sm4 - asm)</span></span>

<span data-ttu-id="0c02f-105">Amostras de dados do elemento/textura especificado usando o endereço especificado e o modo de filtragem identificados pelo determinado exemplo.</span><span class="sxs-lookup"><span data-stu-id="0c02f-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="0c02f-106">aoffimmi de exemplo \[ \_ (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler</span><span class="sxs-lookup"><span data-stu-id="0c02f-106">sample\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler</span></span> |
|--------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="0c02f-107">Item</span><span class="sxs-lookup"><span data-stu-id="0c02f-107">Item</span></span>                                                                                                               | <span data-ttu-id="0c02f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c02f-108">Description</span></span>                                                                                        |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c02f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="0c02f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="0c02f-110">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="0c02f-110">\[in\] The address of the result of the operation.</span></span><br/>                                      |
| <span data-ttu-id="0c02f-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="0c02f-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="0c02f-112">\[em \] um conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="0c02f-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="0c02f-113">Para obter mais informações, consulte a seção **comentários** .</span><span class="sxs-lookup"><span data-stu-id="0c02f-113">For more information, see the **Remarks** section.</span></span><br/> |
| <span data-ttu-id="0c02f-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="0c02f-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="0c02f-115">\[em \] um registro de textura.</span><span class="sxs-lookup"><span data-stu-id="0c02f-115">\[in\] A texture register.</span></span> <span data-ttu-id="0c02f-116">Para obter mais informações, consulte a seção **comentários** .</span><span class="sxs-lookup"><span data-stu-id="0c02f-116">For more information, see the **Remarks** section.</span></span><br/>           |
| <span data-ttu-id="0c02f-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="0c02f-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="0c02f-118">\[em \] um registro de amostra.</span><span class="sxs-lookup"><span data-stu-id="0c02f-118">\[in\] A sampler register.</span></span> <span data-ttu-id="0c02f-119">Para obter mais informações, consulte a seção **comentários** .</span><span class="sxs-lookup"><span data-stu-id="0c02f-119">For more information, see the **Remarks** section.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="0c02f-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c02f-120">Remarks</span></span>

<span data-ttu-id="0c02f-121">Os dados de origem podem vir de qualquer tipo de recurso, além de buffers.</span><span class="sxs-lookup"><span data-stu-id="0c02f-121">The source data may come from any Resource Type, other than Buffers.</span></span>

<span data-ttu-id="0c02f-122">o *srcAddress* fornece o conjunto de coordenadas de textura necessárias para executar o exemplo, como valores de ponto flutuante referenciando o espaço normalizado na textura.</span><span class="sxs-lookup"><span data-stu-id="0c02f-122">*srcAddress* provides the set of texture coordinates needed to perform the sample, as floating point values referencing normalized space in the texture.</span></span> <span data-ttu-id="0c02f-123">Os modos de disposição de endereço (Wrap/espelho/fixe/Border etc.) são aplicados para coordenadas de textura fora de \[ 0... 1 \] intervalo, extraído dos Estados de amostra \# e aplicados depois que qualquer deslocamento de endereço é aplicado às coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="0c02f-123">Address wrapping modes (wrap/mirror/clamp/border etc.) are applied for texture coordinates outside \[0...1\] range, taken from the sampler state (s\#), and applied after any address offset is applied to texture coordinates.</span></span>

<span data-ttu-id="0c02f-124">*srcResource* é um registro de textura (t \# ).</span><span class="sxs-lookup"><span data-stu-id="0c02f-124">*srcResource* is a texture register (t\#).</span></span> <span data-ttu-id="0c02f-125">Isso é simplesmente um espaço reservado para uma textura, incluindo o tipo de dados de retorno do recurso que está sendo amostrado.</span><span class="sxs-lookup"><span data-stu-id="0c02f-125">This is simply a placeholder for a texture, including the return data type of the resource being sampled.</span></span> <span data-ttu-id="0c02f-126">Todas essas informações são declaradas no preâmbulo do sombreador.</span><span class="sxs-lookup"><span data-stu-id="0c02f-126">All of this information is declared in the Shader preamble.</span></span> <span data-ttu-id="0c02f-127">O recurso real a ser amostrado é associado ao sombreador externamente no slot \# (para t \# ).</span><span class="sxs-lookup"><span data-stu-id="0c02f-127">The actual resource to be sampled is bound to the Shader externally at slot \# (for t\#).</span></span>

<span data-ttu-id="0c02f-128">*srcSampler* é um ou mais registros de amostra.</span><span class="sxs-lookup"><span data-stu-id="0c02f-128">*srcSampler* is a sampler register (s).</span></span> <span data-ttu-id="0c02f-129">Trata-se simplesmente de um espaço reservado para uma coleção de controles de filtragem como controles Point vs. linear, mipmapping e address entorno.</span><span class="sxs-lookup"><span data-stu-id="0c02f-129">This is simply a placeholder for a collection of filtering controls such as point vs. linear, mipmapping and address wrapping controls.</span></span>

<span data-ttu-id="0c02f-130">O conjunto de informações necessárias para que o hardware execute a amostragem é dividido em duas partes ortogonal.</span><span class="sxs-lookup"><span data-stu-id="0c02f-130">The set of information required for the hardware to perform sampling is split into two orthogonal pieces.</span></span> <span data-ttu-id="0c02f-131">Primeiro, o registro de textura fornece informações de tipo de dados de origem, incluindo, por exemplo, informações sobre se a textura contém dados SRGB.</span><span class="sxs-lookup"><span data-stu-id="0c02f-131">First, the texture register provides source data type information including, for example, information about whether the texture contains SRGB data.</span></span> <span data-ttu-id="0c02f-132">Ele também faz referência à memória real que está sendo amostrada.</span><span class="sxs-lookup"><span data-stu-id="0c02f-132">It also references the actual memory being sampled.</span></span> <span data-ttu-id="0c02f-133">Em segundo lugar, o registro de amostra define o modo de filtragem a ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="0c02f-133">Second, the sampler register defines the filtering mode to apply.</span></span>

### <a name="array-resources"></a><span data-ttu-id="0c02f-134">Recursos de matriz</span><span class="sxs-lookup"><span data-stu-id="0c02f-134">Array Resources</span></span>

<span data-ttu-id="0c02f-135">Para matrizes Texture1D, o componente g do *srcAddress* (pos-swizzle) seleciona a fatia da matriz da qual buscar.</span><span class="sxs-lookup"><span data-stu-id="0c02f-135">For Texture1D Arrays, the *srcAddress* g component (POS-swizzle) selects which Array Slice to fetch from.</span></span> <span data-ttu-id="0c02f-136">Isso é sempre tratado como um valor float dimensionado, em vez do espaço normalizado para coordenadas de textura padrão, e um ponto de arredondamento para mais próximo é aplicado ao valor, seguido por um fixe para o intervalo BufferArray disponível.</span><span class="sxs-lookup"><span data-stu-id="0c02f-136">This is always treated as a scaled float value, rather than the normalized space for standard texture coordinates, and a round-to-nearest even is applied on the value, followed by a clamp to the available BufferArray range.</span></span>

<span data-ttu-id="0c02f-137">Para matrizes Texture2D, o componente *srcAddress* b (pos-swizzle) seleciona a fatia da matriz da qual buscar, caso contrário, usando a mesma semântica descrita para matrizes Texture1D.</span><span class="sxs-lookup"><span data-stu-id="0c02f-137">For Texture2D Arrays, the *srcAddress* b component (POS-swizzle) selects which Array Slice to fetch from, otherwise using the same semantics described for Texture1D Arrays .</span></span>

### <a name="address-offset"></a><span data-ttu-id="0c02f-138">Deslocamento de endereço</span><span class="sxs-lookup"><span data-stu-id="0c02f-138">Address Offset</span></span>

<span data-ttu-id="0c02f-139">O \[ \_ sufixo opcional aoffimmi (u, v, w) \] (deslocamento de endereço por inteiro imediato) indica que as coordenadas de textura do exemplo devem ser deslocadas por um conjunto de valores de constante de inteiro de espaço de Texel imediato fornecido.</span><span class="sxs-lookup"><span data-stu-id="0c02f-139">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the sample are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="0c02f-140">Os valores literais são um conjunto de números de complemento de 4 bits 2, com intervalo de números inteiros \[ -8, 7 \] .</span><span class="sxs-lookup"><span data-stu-id="0c02f-140">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span> <span data-ttu-id="0c02f-141">Esse modificador é definido para todos os recursos, incluindo matrizes Texture1D/2D e Texture3D, mas não é definido para TextureCube.</span><span class="sxs-lookup"><span data-stu-id="0c02f-141">This modifier is defined for all Resources, including Texture1D/2D Arrays and Texture3D, but it is undefined for TextureCube.</span></span>

<span data-ttu-id="0c02f-142">O hardware pode aproveitar o conhecimento imediato de que uma passagem em uma superfície de texels sobre um local comum está sendo executada por um conjunto de instruções de exemplo.</span><span class="sxs-lookup"><span data-stu-id="0c02f-142">Hardware can take advantage of immediate knowledge that a traversal over some footprint of texels about a common location is being performed by a set of sample instructions.</span></span> <span data-ttu-id="0c02f-143">Isso pode ser transmitido usando \_ aoffimmi (u, v, w).</span><span class="sxs-lookup"><span data-stu-id="0c02f-143">This can be conveyed using \_aoffimmi(u,v,w).</span></span>

<span data-ttu-id="0c02f-144">Os deslocamentos são adicionados às coordenadas de textura, no espaço Texel, em relação a cada MipLevel que está sendo acessado.</span><span class="sxs-lookup"><span data-stu-id="0c02f-144">The offsets are added to the texture coordinates, in texel space, relative to each miplevel being accessed.</span></span> <span data-ttu-id="0c02f-145">Portanto, embora as coordenadas de textura sejam fornecidas como valores float normalizados, o deslocamento aplica um deslocamento de inteiro de Texel de espaço.</span><span class="sxs-lookup"><span data-stu-id="0c02f-145">So even though texture coordinates are provided as normalized float values, the offset applies a texel-space integer offset.</span></span>

<span data-ttu-id="0c02f-146">Deslocamentos de endereço não são aplicados ao longo do eixo de matriz de matrizes Texture1D/2D.</span><span class="sxs-lookup"><span data-stu-id="0c02f-146">Address offsets are not applied along the array axis of Texture1D/2D Arrays.</span></span>

<span data-ttu-id="0c02f-147">\_os componentes aoffimmi v, w são ignorados para Texture1Ds.</span><span class="sxs-lookup"><span data-stu-id="0c02f-147">\_aoffimmi v,w components are ignored for Texture1Ds.</span></span>

<span data-ttu-id="0c02f-148">\_o componente aoffimmi w é ignorado para Texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="0c02f-148">\_aoffimmi w component is ignored for Texture2Ds.</span></span>

<span data-ttu-id="0c02f-149">Os modos de quebra de endereço (quebra/espelho/fixe/borda etc.) dos Estados de amostra \# são aplicados depois que qualquer deslocamento de endereço é aplicado às coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="0c02f-149">Address wrapping modes (wrap/mirror/clamp/border etc.) from the sampler state (s\#) are applied after any address offset is applied to texture coordinates.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="0c02f-150">Controle de tipo de retorno</span><span class="sxs-lookup"><span data-stu-id="0c02f-150">Return Type Control</span></span>

<span data-ttu-id="0c02f-151">O formato de dados retornado pelo exemplo para o registro de destino é determinado pelo formato de recurso ( \_ formato dxgi \* ) associado ao parâmetro *srcResource* (t \# ).</span><span class="sxs-lookup"><span data-stu-id="0c02f-151">The data format returned by the sample to the destination register is determined by the resource format (DXGI\_FORMAT\*) bound to the *srcResource* parameter (t\#).</span></span> <span data-ttu-id="0c02f-152">Por exemplo, se o t especificado \# tiver sido associado a um recurso com formato de formato dxgi \_ \_ A8B8G8R8 \_ UNORM \_ sRGB, a operação de amostragem converterá texels de amostra de gama 2,0 para 1,0, aplicará a filtragem e o resultado será gravado no registro de destino como valores de ponto flutuante no intervalo \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="0c02f-152">For example, if the specified t\# was bound with a resource with format DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB, then the sampling operation will convert sampled texels from gamma 2.0 to 1.0, apply filtering, and the result will written to the destination register as floating point values in the range \[0..1\].</span></span>

<span data-ttu-id="0c02f-153">Os valores retornados são de 4 vetores (com padrões específicos de formato para componentes que não estão presentes no formato).</span><span class="sxs-lookup"><span data-stu-id="0c02f-153">Returned values are 4-vectors (with format-specific defaults for components not present in the format).</span></span> <span data-ttu-id="0c02f-154">O swizzle em *srcResource* determina como swizzle o resultado de 4 componentes de volta do exemplo de textura/filtro, após o qual. Mask no *dest* determina quais componentes no *dest* são atualizados.</span><span class="sxs-lookup"><span data-stu-id="0c02f-154">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture sample/filter, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="0c02f-155">Quando o **exemplo** lê um valor float de 32 bits em um registro de 32 bits, com amostragem de ponto (sem filtragem), ele pode ou não liberar valores desnormals, mas os números não são modificados.</span><span class="sxs-lookup"><span data-stu-id="0c02f-155">When **sample** reads a 32-bit float value into a 32-bit register, with point sampling (no filtering), it may or may not flush denormal values, but otherwise numbers are unmodified.</span></span> <span data-ttu-id="0c02f-156">Se a incerteza com valores desnormals de amostragem de ponto for um problema para um aplicativo, use a instrução [LD](ld--sm4---asm-.md) , que garante que os valores float de 32 bits sejam lidos sem modificações.</span><span class="sxs-lookup"><span data-stu-id="0c02f-156">If the uncertainty with point sampling denormal values is an issue for an application,use the [ld](ld--sm4---asm-.md) instruction, which guarantees that 32-bit float values are read unmodified.</span></span>

### <a name="lod-calculation"></a><span data-ttu-id="0c02f-157">Cálculo de LOD</span><span class="sxs-lookup"><span data-stu-id="0c02f-157">LOD Calculation</span></span>

<span data-ttu-id="0c02f-158">Para obter detalhes sobre como os derivativos são calculados no processo de determinação de LOD para filtragem, consulte [derivar \_ RTX](deriv-rtx--sm4---asm-.md) e [derivar \_ rty](deriv-rty--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="0c02f-158">For details on how derivatives are calculated in the process of determining LOD for filtering, see [deriv\_rtx](deriv-rtx--sm4---asm-.md) and [deriv\_rty](deriv-rty--sm4---asm-.md).</span></span> <span data-ttu-id="0c02f-159">A instrução de **exemplo** computa implicitamente as derivações nas coordenadas de textura usando a mesma definição que as instruções **derivadas** do sombreador usam.</span><span class="sxs-lookup"><span data-stu-id="0c02f-159">The **sample** instruction implicitly computes derivatives on the texture coordinates using the same definition that the **deriv** Shader instructions use.</span></span> <span data-ttu-id="0c02f-160">Isso não se aplica às [instruções \_ l](sample-l--sm4---asm-.md) ou [ \_ d](sample-d--sm4---asm-.md) de exemplo.</span><span class="sxs-lookup"><span data-stu-id="0c02f-160">This does not apply to [sample\_l](sample-l--sm4---asm-.md) or [sample\_d](sample-d--sm4---asm-.md) instructions.</span></span> <span data-ttu-id="0c02f-161">Para essas instruções, LOD ou derivativos são fornecidos diretamente pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0c02f-161">For those instructions, LOD or derivatives are provided directly by the application.</span></span>

<span data-ttu-id="0c02f-162">Para a instrução de **exemplo** , as implementações podem optar por compartilhar o mesmo cálculo de LOD em todos os quatro pixels em um carimbo 2x2 (mas sem área maior) ou executar cálculos de LOD por pixel.</span><span class="sxs-lookup"><span data-stu-id="0c02f-162">For the **sample** instruction, implementations can choose to share the same LOD calculation across all 4 pixels in a 2x2 stamp (but no larger area), or perform per-pixel LOD calculations.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="0c02f-163">Detalhes diversos</span><span class="sxs-lookup"><span data-stu-id="0c02f-163">Miscellaneous Details</span></span>

<span data-ttu-id="0c02f-164">Para o buffer & Texture1D, os componentes *srcAddress* . GBA (pos-swizzle) são ignorados.</span><span class="sxs-lookup"><span data-stu-id="0c02f-164">For Buffer & Texture1D, *srcAddress* .gba components (POS-swizzle) are ignored.</span></span> <span data-ttu-id="0c02f-165">Para matrizes Texture1D, os componentes *srcAddress* . BA (pos-swizzle) são ignorados.</span><span class="sxs-lookup"><span data-stu-id="0c02f-165">For Texture1D Arrays, *srcAddress* .ba components (POS-swizzle) are ignored.</span></span> <span data-ttu-id="0c02f-166">Para Texture2Ds, *srcAddress* . a Component (pos-swizzle) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="0c02f-166">For Texture2Ds, *srcAddress* .a component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="0c02f-167">A busca de um slot de entrada que não tem nada associado a ele retorna 0 para todos os componentes.</span><span class="sxs-lookup"><span data-stu-id="0c02f-167">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

### <a name="restrictions"></a><span data-ttu-id="0c02f-168">Restrições</span><span class="sxs-lookup"><span data-stu-id="0c02f-168">Restrictions</span></span>

-   <span data-ttu-id="0c02f-169">*srcResource* deve ser um \# registro t.</span><span class="sxs-lookup"><span data-stu-id="0c02f-169">*srcResource* must be a t\# register.</span></span> <span data-ttu-id="0c02f-170">*srcResource* não pode ser um ConstantBuffer, que não pode ser associado a \# registros t.</span><span class="sxs-lookup"><span data-stu-id="0c02f-170">*srcResource* cannot be a ConstantBuffer, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="0c02f-171">*srcSampler* deve ser um registro de s \# .</span><span class="sxs-lookup"><span data-stu-id="0c02f-171">*srcSampler* must be an s\# register.</span></span>
-   <span data-ttu-id="0c02f-172">O endereçamento relativo em *srcResource* ou *srcSampler* não é permitido.</span><span class="sxs-lookup"><span data-stu-id="0c02f-172">Relative addressing on *srcResource* or *srcSampler* is not permitted.</span></span>
-   <span data-ttu-id="0c02f-173">*srcAddress* deve ser temp (r \# /X \# ), constantBuffer (CB \# ), registro de entrada (v \# ) ou valor (es) imediato (s).</span><span class="sxs-lookup"><span data-stu-id="0c02f-173">*srcAddress* must be a temp (r\#/x\#), constantBuffer (cb\#), input (v\#) register or immediate value(s).</span></span>
-   <span data-ttu-id="0c02f-174">*dest* deve ser um registro temporário (r \# /x \# ) ou saída (o \* \# ).</span><span class="sxs-lookup"><span data-stu-id="0c02f-174">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>
-   <span data-ttu-id="0c02f-175">\_aoffimmi (u, v, w) não é permitido para TextureCubes.</span><span class="sxs-lookup"><span data-stu-id="0c02f-175">\_aoffimmi(u,v,w) is not permitted for TextureCubes.</span></span>

<span data-ttu-id="0c02f-176">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="0c02f-176">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0c02f-177">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="0c02f-177">Vertex Shader</span></span> | <span data-ttu-id="0c02f-178">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="0c02f-178">Geometry Shader</span></span> | <span data-ttu-id="0c02f-179">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="0c02f-179">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="0c02f-180">x</span><span class="sxs-lookup"><span data-stu-id="0c02f-180">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0c02f-181">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="0c02f-181">Minimum Shader Model</span></span>

<span data-ttu-id="0c02f-182">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0c02f-182">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0c02f-183">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="0c02f-183">Shader Model</span></span>                                              | <span data-ttu-id="0c02f-184">Com suporte</span><span class="sxs-lookup"><span data-stu-id="0c02f-184">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0c02f-185">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="0c02f-185">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0c02f-186">sim</span><span class="sxs-lookup"><span data-stu-id="0c02f-186">yes</span></span>       |
| [<span data-ttu-id="0c02f-187">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="0c02f-187">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0c02f-188">sim</span><span class="sxs-lookup"><span data-stu-id="0c02f-188">yes</span></span>       |
| [<span data-ttu-id="0c02f-189">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="0c02f-189">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0c02f-190">sim</span><span class="sxs-lookup"><span data-stu-id="0c02f-190">yes</span></span>       |
| [<span data-ttu-id="0c02f-191">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0c02f-191">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0c02f-192">não</span><span class="sxs-lookup"><span data-stu-id="0c02f-192">no</span></span>        |
| [<span data-ttu-id="0c02f-193">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0c02f-193">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0c02f-194">não</span><span class="sxs-lookup"><span data-stu-id="0c02f-194">no</span></span>        |
| [<span data-ttu-id="0c02f-195">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0c02f-195">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0c02f-196">não</span><span class="sxs-lookup"><span data-stu-id="0c02f-196">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0c02f-197">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0c02f-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c02f-198">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0c02f-198">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





