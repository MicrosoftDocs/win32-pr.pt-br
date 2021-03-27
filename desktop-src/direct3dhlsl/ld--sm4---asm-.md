---
title: LD (sm4-ASM)
description: Busca dados do buffer ou da textura especificada sem nenhuma filtragem (por exemplo, amostragem de ponto) usando o endereço inteiro fornecido. Os dados de origem podem vir de qualquer tipo de recurso, diferente de TextureCube.
ms.assetid: DEE9A55F-EDFE-478E-8169-5BF9C43E98AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaacc3d76d49cc2b3043d39036f0ff652d7b8794
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293574"
---
# <a name="ld-sm4---asm"></a><span data-ttu-id="3eb2b-104">LD (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3eb2b-104">ld (sm4 - asm)</span></span>

<span data-ttu-id="3eb2b-105">Busca dados do buffer ou da textura especificada sem nenhuma filtragem (por exemplo, amostragem de ponto) usando o endereço inteiro fornecido.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-105">Fetches data from the specified buffer or texture without any filtering (e.g. point sampling) using the provided integer address.</span></span> <span data-ttu-id="3eb2b-106">Os dados de origem podem vir de qualquer tipo de recurso, diferente de TextureCube.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-106">The source data may come from any resource type, other than TextureCube.</span></span>



| <span data-ttu-id="3eb2b-107">LD \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="3eb2b-107">ld\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------|



 



| <span data-ttu-id="3eb2b-108">Item</span><span class="sxs-lookup"><span data-stu-id="3eb2b-108">Item</span></span>                                                                                                               | <span data-ttu-id="3eb2b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3eb2b-109">Description</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3eb2b-110"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="3eb2b-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="3eb2b-111">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-111">\[in\] The address of the result of the operation.</span></span><br/>                                                               |
| <span data-ttu-id="3eb2b-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="3eb2b-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="3eb2b-113">\[nas \] coordenadas de textura necessárias para executar o exemplo.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-113">\[in\] The texture coordinates needed to perform the sample.</span></span><br/>                                                     |
| <span data-ttu-id="3eb2b-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="3eb2b-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="3eb2b-115">\[em \] um registro de textura (t \# ) que deve ter sido declarado identificando de qual textura ou buffer deve ser obtido.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-115">\[in\] A texture register (t\#) which must have been declared identifying which Texture or Buffer to fetch from.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3eb2b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3eb2b-116">Remarks</span></span>

<span data-ttu-id="3eb2b-117">Essa instrução é uma alternativa simplificada para a instrução de [exemplo](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="3eb2b-117">This instruction is a simplified alternative to the [sample](sample--sm4---asm-.md) instruction.</span></span> <span data-ttu-id="3eb2b-118">Ao contrário de **Sample**, **LD** também é capaz de buscar dados de buffers.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-118">Unlike **sample**, **ld** is also capable of fetching data from buffers.</span></span> <span data-ttu-id="3eb2b-119">**LD** também pode buscar de recursos de várias amostras (somente no sombreador de pixel).</span><span class="sxs-lookup"><span data-stu-id="3eb2b-119">**ld** is can also fetch from multi-sample resources (on pixel shader only).</span></span>

<span data-ttu-id="3eb2b-120">o *srcAddress* fornece o conjunto de coordenadas de textura necessárias para executar o exemplo na forma de inteiros sem sinal.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-120">*srcAddress* provides the set of texture coordinates needed to perform the sample in the form of unsigned integers.</span></span> <span data-ttu-id="3eb2b-121">Se *srcAddress* estiver fora do intervalo \[ 0... ( \# texels na dimensão-1) \] , o comportamento fora dos limites é invocado, em que **LD** retorna 0 em todos os componentes não ausentes do formato do *srcResource* e o padrão para componentes ausentes.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-121">If *srcAddress* is out of the range\[0...(\#texels in dimension -1)\], then out-of-bounds behavior is invoked, where **ld** returns 0 in all non-missing components of the format of the *srcResource*, and the default for missing components.</span></span> <span data-ttu-id="3eb2b-122">Um aplicativo que deseja ter um controle mais flexível sobre o comportamento de endereço fora do intervalo deve usar a instrução de **exemplo** , pois ele honra o comportamento de encapsulamento/espelho/fixe/Border definido como um estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-122">An application wishing any more flexible control over out-of-range address behavior should use the **sample** instruction instead, as it honors address wrap/mirror/clamp/border behavior defined as sampler state.</span></span>

<span data-ttu-id="3eb2b-123">*srcAddress. a* (pos-swizzle) sempre fornece um nível de mipmap inteiro sem sinal.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-123">*srcAddress.a* (POS-swizzle) always provides an unsigned integer mipmap level.</span></span> <span data-ttu-id="3eb2b-124">Se o valor estiver fora do intervalo \[ 0... ( num miplevels no Resource-1) \] ), o comportamento fora dos limites é invocado.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-124">If the value is out of the range \[0...(num miplevels in resource-1)\]), then out-of-bounds behavior is invoked.</span></span> <span data-ttu-id="3eb2b-125">Se o recurso for um buffer, que não pode ter nenhum mipmaps, então *srcAddress. a* será ignorada</span><span class="sxs-lookup"><span data-stu-id="3eb2b-125">If the resource is a buffer, which can not have any mipmaps, then *srcAddress.a* is ignored</span></span>

<span data-ttu-id="3eb2b-126">*srcAddress. GB* (pos-swizzle) é ignorado para buffers e texture1D (não matriz).</span><span class="sxs-lookup"><span data-stu-id="3eb2b-126">*srcAddress.gb* (POS-swizzle) is ignored for buffers and texture1D (non-Array).</span></span> <span data-ttu-id="3eb2b-127">*srcAddress. b* (pos-swizzle) é ignorado para matrizes Texture1D e texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-127">*srcAddress.b* (POS-swizzle) is ignored for texture1D arrays and texture2Ds.</span></span>

<span data-ttu-id="3eb2b-128">Para matrizes texture1D, *srcAddress. g* (pos-swizzle) fornece o índice de matriz como um inteiro sem sinal.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-128">For texture1D arrays, *srcAddress.g* (POS-swizzle) provides the array index as an unsigned integer.</span></span> <span data-ttu-id="3eb2b-129">Se o valor estiver fora do intervalo de índices de matriz disponíveis \[ 0... ( tamanho da matriz-1) \] , então o comportamento fora dos limites é invocado.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-129">If the value is out of the range of available array indices \[0...(array size-1)\], then out-of-bounds behavior is invoked.</span></span>

<span data-ttu-id="3eb2b-130">Para matrizes texture2D, *srcAddress. b* (pos-swizzle) fornece o índice de matriz, caso contrário, com a mesma semântica que para texture1D.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-130">For texture2D arrays, *srcAddress.b* (POS-swizzle) provides the array index, otherwise with same semantics as for texture1D.</span></span>

<span data-ttu-id="3eb2b-131">A busca de *t \#* que não tem nada associado retorna 0 para todos os componentes.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-131">Fetching from *t\#* that has nothing bound to it returns 0 for all components.</span></span>

### <a name="address-offset"></a><span data-ttu-id="3eb2b-132">Deslocamento de endereço</span><span class="sxs-lookup"><span data-stu-id="3eb2b-132">Address Offset</span></span>

<span data-ttu-id="3eb2b-133">O \[ \_ sufixo opcional aoffimmi (u, v, w) \] (deslocamento de endereço por inteiro imediato) indica que as coordenadas de textura para o **LD** devem ser deslocadas por um conjunto de valores de constante de inteiro de espaço de Texel imediato fornecido.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-133">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the **ld** are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="3eb2b-134">Os valores literais são um conjunto de números de complemento de 4 bits 2, com intervalo de números inteiros \[ -8, 7 \] .</span><span class="sxs-lookup"><span data-stu-id="3eb2b-134">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span> <span data-ttu-id="3eb2b-135">Esse modificador é definido somente para texture1D/2D/3D, incluindo matrizes, e não para buffers.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-135">This modifier is defined only for texture1D/2D/3D, including arrays, and not for buffers.</span></span>

<span data-ttu-id="3eb2b-136">Os deslocamentos são adicionados às coordenadas de textura, no espaço Texel, em relação ao MipLevel que está sendo acessado pela **LD**.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-136">The offsets are added to the texture coordinates, in texel space, relative to the miplevel being accessed by the **ld**.</span></span>

<span data-ttu-id="3eb2b-137">Deslocamentos de endereço não são aplicados ao longo do eixo de matriz de matrizes texture1D/2D.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-137">Address offsets are not applied along the array axis of texture1D/2D arrays.</span></span>

<span data-ttu-id="3eb2b-138">Os componentes *\_ aoffimmi v, w* são ignorados para texture1Ds.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-138">The *\_aoffimmi v,w* components are ignored for texture1Ds.</span></span>

<span data-ttu-id="3eb2b-139">O componente *\_ aoffimmi w* é ignorado para texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-139">The *\_aoffimmi w* component is ignored for texture2Ds.</span></span>

<span data-ttu-id="3eb2b-140">Como as coordenadas de textura para **LD** são inteiros não assinados, se o deslocamento fizer com que o endereço fique abaixo de zero, ele será encapsulado em um endereço grande e resultará em um acesso fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-140">Because the texture coordinates for **ld** are unsigned integers, if the offset causes the address to go below zero, it will wrap to a large address, and result in an out of bounds access.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="3eb2b-141">Controle de tipo de retorno</span><span class="sxs-lookup"><span data-stu-id="3eb2b-141">Return Type Control</span></span>

<span data-ttu-id="3eb2b-142">O formato de dados retornado por **LD** para o registro de destino é determinado da mesma maneira que descrito para a instrução de **exemplo** ; Ele se baseia no formato associado ao parâmetro *srcResource* (*t \#*).</span><span class="sxs-lookup"><span data-stu-id="3eb2b-142">The data format returned by **ld** to the destination register is determined in the same way as described for the **sample** instruction; it is based on the format bound to the *srcResource* parameter (*t\#*).</span></span>

<span data-ttu-id="3eb2b-143">Assim como acontece com a instrução de **exemplo** , os valores retornados para **LD** são 4 vetores com padrões específicos de formato para componentes que não estão presentes no formato.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-143">As with the **sample** instruction, returned values for **ld** are 4-vectors with format-specific defaults for components not present in the format.</span></span> <span data-ttu-id="3eb2b-144">O swizzle em *srcResource* determina como swizzle o resultado de 4 componentes de volta da carga de textura, após o qual. Mask no *dest* determina quais componentes no *dest* são atualizados.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-144">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture load, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="3eb2b-145">Quando um valor float de 32 bits é lido por *LD* em um registro de 32 bits, os bits são intocados; ou seja, os valores desnormals permanecem desnormalizados.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-145">When a 32-bit float value is read by *ld* into a 32-bit register, the bits are untouched; that is, denormal values remain denormal.</span></span> <span data-ttu-id="3eb2b-146">Isso é diferente da instrução de **exemplo** .</span><span class="sxs-lookup"><span data-stu-id="3eb2b-146">This is unlike the **sample** instruction.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="3eb2b-147">Detalhes diversos</span><span class="sxs-lookup"><span data-stu-id="3eb2b-147">Miscellaneous Details</span></span>

<span data-ttu-id="3eb2b-148">Como não há nenhuma filtragem associada à instrução **LD** , conceitos como LOD Bias não se aplicam a **LD**.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-148">As there is no filtering associated with the **ld** instruction, concepts like LOD bias do not apply to **ld**.</span></span> <span data-ttu-id="3eb2b-149">Portanto, não há nenhum parâmetro de *s \#* de amostra.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-149">Accordingly there is no sampler *s\#* parameter.</span></span>

### <a name="restrictions"></a><span data-ttu-id="3eb2b-150">Restrições</span><span class="sxs-lookup"><span data-stu-id="3eb2b-150">Restrictions</span></span>

-   <span data-ttu-id="3eb2b-151">*srcResource* deve ser um \# registro t e não um TextureCube.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-151">*srcResource* must be a t\# register, and not a TextureCube.</span></span> <span data-ttu-id="3eb2b-152">*srcResource* não pode ser um constantbuffer, que não pode ser associado a \# registros t.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-152">*srcResource* cannot be a constantbuffer either, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="3eb2b-153">O endereçamento relativo em *srcResource* não é permitido.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-153">Relative addressing on *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="3eb2b-154">*srcAddress* deve ser um registro temporário (r \# /x \# ), uma constante (CB \# ) ou de entrada (v \# ).</span><span class="sxs-lookup"><span data-stu-id="3eb2b-154">*srcAddress* must be a temp (r\#/x\#), constant (cb\#) or input (v\#) register.</span></span>
-   <span data-ttu-id="3eb2b-155">*dest* deve ser um registro temporário (r \# /x \# ) ou saída (o \* \# ).</span><span class="sxs-lookup"><span data-stu-id="3eb2b-155">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>

<span data-ttu-id="3eb2b-156">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="3eb2b-156">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3eb2b-157">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="3eb2b-157">Vertex Shader</span></span> | <span data-ttu-id="3eb2b-158">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="3eb2b-158">Geometry Shader</span></span> | <span data-ttu-id="3eb2b-159">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="3eb2b-159">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="3eb2b-160">x</span><span class="sxs-lookup"><span data-stu-id="3eb2b-160">x</span></span>             | <span data-ttu-id="3eb2b-161">x</span><span class="sxs-lookup"><span data-stu-id="3eb2b-161">x</span></span>               | <span data-ttu-id="3eb2b-162">x</span><span class="sxs-lookup"><span data-stu-id="3eb2b-162">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3eb2b-163">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="3eb2b-163">Minimum Shader Model</span></span>

<span data-ttu-id="3eb2b-164">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3eb2b-164">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3eb2b-165">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="3eb2b-165">Shader Model</span></span>                                              | <span data-ttu-id="3eb2b-166">Com suporte</span><span class="sxs-lookup"><span data-stu-id="3eb2b-166">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3eb2b-167">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="3eb2b-167">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3eb2b-168">sim</span><span class="sxs-lookup"><span data-stu-id="3eb2b-168">yes</span></span>       |
| [<span data-ttu-id="3eb2b-169">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="3eb2b-169">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3eb2b-170">sim</span><span class="sxs-lookup"><span data-stu-id="3eb2b-170">yes</span></span>       |
| [<span data-ttu-id="3eb2b-171">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="3eb2b-171">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3eb2b-172">sim</span><span class="sxs-lookup"><span data-stu-id="3eb2b-172">yes</span></span>       |
| [<span data-ttu-id="3eb2b-173">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3eb2b-173">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3eb2b-174">não</span><span class="sxs-lookup"><span data-stu-id="3eb2b-174">no</span></span>        |
| [<span data-ttu-id="3eb2b-175">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3eb2b-175">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3eb2b-176">não</span><span class="sxs-lookup"><span data-stu-id="3eb2b-176">no</span></span>        |
| [<span data-ttu-id="3eb2b-177">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3eb2b-177">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3eb2b-178">não</span><span class="sxs-lookup"><span data-stu-id="3eb2b-178">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3eb2b-179">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3eb2b-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3eb2b-180">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3eb2b-180">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





