---
title: Formato BC6H
description: O formato BC6H é um formato de compactação de textura projetado para dar suporte a espaços de cores de intervalo altamente dinâmico (HDR) nos dados de origem.
ms.assetid: D6A1A729-5023-4A94-A8DB-5954D453E136
keywords:
- BC6H
- DXGI_FORMAT_BC6H
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ea15e0275bc478c0708ce08f531d8888a3c84d
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335220"
---
# <a name="bc6h-format"></a><span data-ttu-id="9c0d3-105">Formato BC6H</span><span class="sxs-lookup"><span data-stu-id="9c0d3-105">BC6H Format</span></span>

<span data-ttu-id="9c0d3-106">O formato BC6H é um formato de compactação de textura projetado para dar suporte a espaços de cores de intervalo altamente dinâmico (HDR) nos dados de origem.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-106">The BC6H format is a texture compression format designed to support high-dynamic range (HDR) color spaces in source data.</span></span>

-   [<span data-ttu-id="9c0d3-107">Sobre BC6H/DXGI \_ FORMAT \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="9c0d3-107">About BC6H/DXGI\_FORMAT\_BC6H</span></span>](/windows)
-   [<span data-ttu-id="9c0d3-108">Implementação de BC6H</span><span class="sxs-lookup"><span data-stu-id="9c0d3-108">BC6H Implementation</span></span>](#bc6h-implementation)
-   [<span data-ttu-id="9c0d3-109">Decodificação do formato BC6H</span><span class="sxs-lookup"><span data-stu-id="9c0d3-109">Decoding the BC6H Format</span></span>](#decoding-the-bc6h-format)
-   [<span data-ttu-id="9c0d3-110">Formato de ponto de extremidade compactado BC6H</span><span class="sxs-lookup"><span data-stu-id="9c0d3-110">BC6H Compressed Endpoint Format</span></span>](#bc6h-compressed-endpoint-format)
-   [<span data-ttu-id="9c0d3-111">Assinar extensão para valores de ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="9c0d3-111">Sign Extension for Endpoint Values</span></span>](#sign-extension-for-endpoint-values)
-   [<span data-ttu-id="9c0d3-112">Transformar inversão para valores de ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="9c0d3-112">Transform Inversion for Endpoint Values</span></span>](#transform-inversion-for-endpoint-values)
-   [<span data-ttu-id="9c0d3-113">Não resquantação de pontos de extremidade de cor</span><span class="sxs-lookup"><span data-stu-id="9c0d3-113">Unquantization of Color Endpoints</span></span>](#unquantization-of-color-endpoints)
-   [<span data-ttu-id="9c0d3-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9c0d3-114">Related topics</span></span>](#related-topics)

## <a name="about-bc6hdxgi_format_bc6h"></a><span data-ttu-id="9c0d3-115">Sobre BC6H/DXGI \_ FORMAT \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="9c0d3-115">About BC6H/DXGI\_FORMAT\_BC6H</span></span>

<span data-ttu-id="9c0d3-116">O formato BC6H fornece compactação de alta qualidade para imagens que usam canais de cor HDR, com um valor de 16 bits para cada canal de cor do valor (16: 16:16).</span><span class="sxs-lookup"><span data-stu-id="9c0d3-116">The BC6H format provides high-quality compression for images that use three HDR color channels, with a 16-bit value for each color channel of the value (16:16:16).</span></span> <span data-ttu-id="9c0d3-117">Não há nenhum suporte para um canal alfa.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-117">There is no support for an alpha channel.</span></span>

<span data-ttu-id="9c0d3-118">BC6H é especificado pelos seguintes valores de enumeração DXGI \_ FORMAT:</span><span class="sxs-lookup"><span data-stu-id="9c0d3-118">BC6H is specified by the following DXGI\_FORMAT enumeration values:</span></span>

-   <span data-ttu-id="9c0d3-119">**DXGI \_ FORMAT \_ BC6H \_ TYPELESS**.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-119">**DXGI\_FORMAT\_BC6H\_TYPELESS**.</span></span>
-   <span data-ttu-id="9c0d3-120">**DXGI \_ FORMAT \_ BC6H \_ UF16**.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-120">**DXGI\_FORMAT\_BC6H\_UF16**.</span></span> <span data-ttu-id="9c0d3-121">Esse formato BC6H não usa um bit de sinal nos valores de canal de cor da ponto flutuante de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-121">This BC6H format does not use a sign bit in the 16-bit floating point color channel values.</span></span>
-   <span data-ttu-id="9c0d3-122">**DXGI \_ FORMAT \_ BC6H \_ SF16**. Esse formato BC6H usa um bit de sinal nos valores de canal de cor de ponto flutuante de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-122">**DXGI\_FORMAT\_BC6H\_SF16**.This BC6H format uses a sign bit in the 16-bit floating point color channel values.</span></span>

> [!Note]  
> <span data-ttu-id="9c0d3-123">O formato de ponto flutuante de 16 bits para canais de cores geralmente é chamado de formato de ponto flutuante "metade".</span><span class="sxs-lookup"><span data-stu-id="9c0d3-123">The 16 bit floating point format for color channels is often referred to as a "half" floating point format.</span></span> <span data-ttu-id="9c0d3-124">Esse formato tem o seguinte layout de bit:</span><span class="sxs-lookup"><span data-stu-id="9c0d3-124">This format has the following bit layout:</span></span>
>
> |  <span data-ttu-id="9c0d3-125">Formatar</span><span class="sxs-lookup"><span data-stu-id="9c0d3-125">Format</span></span>                     | <span data-ttu-id="9c0d3-126">Layout de bit</span><span class="sxs-lookup"><span data-stu-id="9c0d3-126">Bit layout</span></span>                                                |
> |-----------------------|-------------------------------------------------|
> | <span data-ttu-id="9c0d3-127">UF16 (float não assinado)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-127">UF16 (unsigned float)</span></span> | <span data-ttu-id="9c0d3-128">5 bits de expoente + 11 bits de mantissa</span><span class="sxs-lookup"><span data-stu-id="9c0d3-128">5 exponent bits + 11 mantissa bits</span></span>              |
> | <span data-ttu-id="9c0d3-129">SF16 (float assinado)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-129">SF16 (signed float)</span></span>   | <span data-ttu-id="9c0d3-130">1 bit de sinal + 5 bits de expoente + 10 bits de mantissa</span><span class="sxs-lookup"><span data-stu-id="9c0d3-130">1 sign bit + 5 exponent bits + 10 mantissa bits</span></span> |
>
> 
>
>  

 

<span data-ttu-id="9c0d3-131">O formato BC6H pode ser usado para o recursos de textura [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (incluindo matrizes), Texture3D ou TextureCube (incluindo matrizes).</span><span class="sxs-lookup"><span data-stu-id="9c0d3-131">The BC6H format can be used for [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (including arrays), Texture3D, or TextureCube (including arrays) texture resources.</span></span> <span data-ttu-id="9c0d3-132">Da mesma forma, esse formato se aplica a qualquer superfície de MIP-map associada a esses recursos.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-132">Similarly, this format applies to any MIP-map surfaces associated with these resources.</span></span>

<span data-ttu-id="9c0d3-133">O BC6H usa um tamanho de bloco fixo de 16 bytes (128 bits) e um tamanho de bloco fixo de 4 x 4 texels.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-133">BC6H uses a fixed block size of 16 bytes (128 bits) and a fixed tile size of 4x4 texels.</span></span> <span data-ttu-id="9c0d3-134">Como com os formatos BC anteriores, as imagens de textura maiores que o tamanho de bloco com suporte (4 x 4) são compactadas usando vários blocos.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-134">As with previous BC formats, texture images larger than the supported tile size (4x4) are compressed by using multiple blocks.</span></span> <span data-ttu-id="9c0d3-135">Essa identidade de endereçamento também se aplica a imagens tridimensionais, mapas MIP, cubemaps e matrizes de textura.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-135">This addressing identity applies also to three-dimensional images, MIP-maps, cubemaps, and texture arrays.</span></span> <span data-ttu-id="9c0d3-136">Todos os blocos de imagem devem ser do mesmo formato.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-136">All image tiles must be of the same format.</span></span>

<span data-ttu-id="9c0d3-137">Algumas observações importantes sobre o formato BC6H:</span><span class="sxs-lookup"><span data-stu-id="9c0d3-137">Some important notes about the BC6H format:</span></span>

-   <span data-ttu-id="9c0d3-138">O BC6H suporta a denormalization de ponto flutuante, mas não suporta INF (infinito) e NaN (não numérico).</span><span class="sxs-lookup"><span data-stu-id="9c0d3-138">BC6H supports floating point denormalization, but does not support INF (infinity) and NaN (not a number).</span></span> <span data-ttu-id="9c0d3-139">A exceção é o modo assinado de BC6H (FORMATO DXGI \_ BC6H SF16), que dá suporte a \_ \_ -INF (infinito negativo).</span><span class="sxs-lookup"><span data-stu-id="9c0d3-139">The exception is the signed mode of BC6H (DXGI\_FORMAT\_BC6H\_SF16), which supports -INF (negative infinity).</span></span> <span data-ttu-id="9c0d3-140">Observe que esse suporte para-INF é meramente um artefato do próprio formato e não é especificamente suportado por codificadores para esse formato.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-140">Note that this support for -INF is merely an artifact of the format itself, and is not specifically supported by encoders for this format.</span></span> <span data-ttu-id="9c0d3-141">Em geral, quando os codificadores encontram dados de entrada INF (positivos ou negativos) ou NaN, eles devem \\ converter esses dados no valor máximo permitido de representação não-inf e mapear Nan para 0 antes da compactação.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-141">In general, when encoders encounter INF (positive or negative) or NaN input data, they should \\ convert that data to the maximum allowable non-INF representation value, and map NaN to 0 prior to compression.</span></span>
-   <span data-ttu-id="9c0d3-142">O BC6H não oferece suporte a um canal alfa.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-142">BC6H does not support an alpha channel.</span></span>
-   <span data-ttu-id="9c0d3-143">O decodificador BC6H executa descompactação antes de realizar a filtragem de textura.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-143">The BC6H decoder performs decompression before it performs texture filtering.</span></span>
-   <span data-ttu-id="9c0d3-144">A descompactação BC6H deve ser um pouco precisa. ou seja, o hardware deve retornar resultados idênticos ao decodificador descrito nesta documentação.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-144">BC6H decompression must be bit accurate; that is, the hardware must return results that are identical to the decoder described in this documentation.</span></span>

## <a name="bc6h-implementation"></a><span data-ttu-id="9c0d3-145">Implementação de BC6H</span><span class="sxs-lookup"><span data-stu-id="9c0d3-145">BC6H Implementation</span></span>

<span data-ttu-id="9c0d3-146">Um bloco de BC6H consiste em bits de modo, pontos de extremidade compactados, índices compactados e um índice de partição opcional.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-146">A BC6H block consists of mode bits, compressed endpoints, compressed indices, and an optional partition index.</span></span> <span data-ttu-id="9c0d3-147">Esse formato especifica 14 modos diferentes.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-147">This format specifies 14 different modes.</span></span>

<span data-ttu-id="9c0d3-148">Uma cor de ponto de extremidade é armazenada como um trio RGB.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-148">An endpoint color is stored as an RGB triplet.</span></span> <span data-ttu-id="9c0d3-149">O BC6H define uma paleta de cores em uma linha aproximada em um número de pontos de extremidade de cores definidos.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-149">BC6H defines a palette of colors on an approximate line across a number of defined color endpoints.</span></span> <span data-ttu-id="9c0d3-150">Além disso, dependendo do modo, um bloco pode ser dividido em duas regiões ou tratado como uma única região, onde um bloco de duas regiões tem um conjunto separado de pontos de extremidade de cor para cada região.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-150">Also, depending on the mode, a tile can be divided into two regions or treated as a single region, where a two-region tile has a separate set of color endpoints for each region.</span></span> <span data-ttu-id="9c0d3-151">O BC6H armazena um índice de paleta por texel.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-151">BC6H stores one palette index per texel.</span></span>

<span data-ttu-id="9c0d3-152">No caso de duas regiões, há 32 partições possíveis.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-152">In the two-region case, there are 32 possible partitions.</span></span>

## <a name="decoding-the-bc6h-format"></a><span data-ttu-id="9c0d3-153">Decodificando o formato BC6H</span><span class="sxs-lookup"><span data-stu-id="9c0d3-153">Decoding the BC6H Format</span></span>

<span data-ttu-id="9c0d3-154">O pseudocódigo a seguir mostra as etapas para descompactar o pixel em (x, y) que recebe o bloco de 16 bytes BC6H.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-154">The pseudocode below shows the steps to decompress the pixel at (x,y) given the 16 byte BC6H block.</span></span>

``` syntax
decompress_bc6h(x, y, block)
{
    mode = extract_mode(block);
    endpoints;
    index;
    
    if(mode.type == ONE)
    {
        endpoints = extract_compressed_endpoints(mode, block);
        index = extract_index_ONE(x, y, block);
    }
    else //mode.type == TWO
    {
        partition = extract_partition(block);
        region = get_region(partition, x, y);
        endpoints = extract_compressed_endpoints(mode, region, block);
        index = extract_index_TWO(x, y, partition, block);
    }
    
    unquantize(endpoints);
    color = interpolate(index, endpoints);
    finish_unquantize(color);
}
```

<span data-ttu-id="9c0d3-155">A tabela a seguir contém os valores e a contagem de bit de cada um dos 14 formatos possíveis para blocos de BC6H.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-155">The following table contains the bit count and values for each of the 14 possible formats for BC6H blocks.</span></span> 

| <span data-ttu-id="9c0d3-156">Modo</span><span class="sxs-lookup"><span data-stu-id="9c0d3-156">Mode</span></span> | <span data-ttu-id="9c0d3-157">Índices de partição</span><span class="sxs-lookup"><span data-stu-id="9c0d3-157">Partition Indices</span></span> | <span data-ttu-id="9c0d3-158">Partição</span><span class="sxs-lookup"><span data-stu-id="9c0d3-158">Partition</span></span> | <span data-ttu-id="9c0d3-159">Pontos de extremidade de cor</span><span class="sxs-lookup"><span data-stu-id="9c0d3-159">Color Endpoints</span></span>                  | <span data-ttu-id="9c0d3-160">Bits de modo</span><span class="sxs-lookup"><span data-stu-id="9c0d3-160">Mode Bits</span></span>      |
|------|-------------------|-----------|----------------------------------|----------------|
| <span data-ttu-id="9c0d3-161">1</span><span class="sxs-lookup"><span data-stu-id="9c0d3-161">1</span></span>    | <span data-ttu-id="9c0d3-162">46 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-162">46 bits</span></span>           | <span data-ttu-id="9c0d3-163">5 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-163">5 bits</span></span>    | <span data-ttu-id="9c0d3-164">75 bits (10.555, 10.555, 10.555)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-164">75 bits (10.555, 10.555, 10.555)</span></span> | <span data-ttu-id="9c0d3-165">2 bits (00)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-165">2 bits (00)</span></span>    |
| <span data-ttu-id="9c0d3-166">2</span><span class="sxs-lookup"><span data-stu-id="9c0d3-166">2</span></span>    | <span data-ttu-id="9c0d3-167">46 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-167">46 bits</span></span>           | <span data-ttu-id="9c0d3-168">5 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-168">5 bits</span></span>    | <span data-ttu-id="9c0d3-169">75 bits (7666, 7666, 7666)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-169">75 bits (7666, 7666, 7666)</span></span>       | <span data-ttu-id="9c0d3-170">2 bits (01)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-170">2 bits (01)</span></span>    |
| <span data-ttu-id="9c0d3-171">3</span><span class="sxs-lookup"><span data-stu-id="9c0d3-171">3</span></span>    | <span data-ttu-id="9c0d3-172">46 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-172">46 bits</span></span>           | <span data-ttu-id="9c0d3-173">5 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-173">5 bits</span></span>    | <span data-ttu-id="9c0d3-174">72 bits (11.555, 11.444, 11.444)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-174">72 bits (11.555, 11.444, 11.444)</span></span> | <span data-ttu-id="9c0d3-175">5 bits (00010)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-175">5 bits (00010)</span></span> |
| <span data-ttu-id="9c0d3-176">4</span><span class="sxs-lookup"><span data-stu-id="9c0d3-176">4</span></span>    | <span data-ttu-id="9c0d3-177">46 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-177">46 bits</span></span>           | <span data-ttu-id="9c0d3-178">5 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-178">5 bits</span></span>    | <span data-ttu-id="9c0d3-179">72 bits (11.444, 11.555, 11.444)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-179">72 bits (11.444, 11.555, 11.444)</span></span> | <span data-ttu-id="9c0d3-180">5 bits (00110)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-180">5 bits (00110)</span></span> |
| <span data-ttu-id="9c0d3-181">5</span><span class="sxs-lookup"><span data-stu-id="9c0d3-181">5</span></span>    | <span data-ttu-id="9c0d3-182">46 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-182">46 bits</span></span>           | <span data-ttu-id="9c0d3-183">5 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-183">5 bits</span></span>    | <span data-ttu-id="9c0d3-184">72 bits (11.444, 11.444, 11.555)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-184">72 bits (11.444, 11.444, 11.555)</span></span> | <span data-ttu-id="9c0d3-185">5 bits (01010)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-185">5 bits (01010)</span></span> |
| <span data-ttu-id="9c0d3-186">6</span><span class="sxs-lookup"><span data-stu-id="9c0d3-186">6</span></span>    | <span data-ttu-id="9c0d3-187">46 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-187">46 bits</span></span>           | <span data-ttu-id="9c0d3-188">5 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-188">5 bits</span></span>    | <span data-ttu-id="9c0d3-189">72 bits (9555, 9555, 9555)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-189">72 bits (9555, 9555, 9555)</span></span>       | <span data-ttu-id="9c0d3-190">5 bits (01110)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-190">5 bits (01110)</span></span> |
| <span data-ttu-id="9c0d3-191">7</span><span class="sxs-lookup"><span data-stu-id="9c0d3-191">7</span></span>    | <span data-ttu-id="9c0d3-192">46 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-192">46 bits</span></span>           | <span data-ttu-id="9c0d3-193">5 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-193">5 bits</span></span>    | <span data-ttu-id="9c0d3-194">72 bits (8666, 8555, 8555)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-194">72 bits (8666, 8555, 8555)</span></span>       | <span data-ttu-id="9c0d3-195">5 bits (10010)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-195">5 bits (10010)</span></span> |
| <span data-ttu-id="9c0d3-196">8</span><span class="sxs-lookup"><span data-stu-id="9c0d3-196">8</span></span>    | <span data-ttu-id="9c0d3-197">46 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-197">46 bits</span></span>           | <span data-ttu-id="9c0d3-198">5 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-198">5 bits</span></span>    | <span data-ttu-id="9c0d3-199">72 bits (8555, 8666, 8555)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-199">72 bits (8555, 8666, 8555)</span></span>       | <span data-ttu-id="9c0d3-200">5 bits (10110)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-200">5 bits (10110)</span></span> |
| <span data-ttu-id="9c0d3-201">9</span><span class="sxs-lookup"><span data-stu-id="9c0d3-201">9</span></span>    | <span data-ttu-id="9c0d3-202">46 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-202">46 bits</span></span>           | <span data-ttu-id="9c0d3-203">5 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-203">5 bits</span></span>    | <span data-ttu-id="9c0d3-204">72 bits (8555, 8555, 8666)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-204">72 bits (8555, 8555, 8666)</span></span>       | <span data-ttu-id="9c0d3-205">5 bits (11010)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-205">5 bits (11010)</span></span> |
| <span data-ttu-id="9c0d3-206">10</span><span class="sxs-lookup"><span data-stu-id="9c0d3-206">10</span></span>   | <span data-ttu-id="9c0d3-207">46 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-207">46 bits</span></span>           | <span data-ttu-id="9c0d3-208">5 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-208">5 bits</span></span>    | <span data-ttu-id="9c0d3-209">72 bits (6666, 6666, 6666)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-209">72 bits (6666, 6666, 6666)</span></span>       | <span data-ttu-id="9c0d3-210">5 bits (11110)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-210">5 bits (11110)</span></span> |
| <span data-ttu-id="9c0d3-211">11</span><span class="sxs-lookup"><span data-stu-id="9c0d3-211">11</span></span>   | <span data-ttu-id="9c0d3-212">63 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-212">63 bits</span></span>           | <span data-ttu-id="9c0d3-213">0 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-213">0 bits</span></span>    | <span data-ttu-id="9c0d3-214">60 bits (10.10, 10.10, 10.10)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-214">60 bits (10.10, 10.10, 10.10)</span></span>    | <span data-ttu-id="9c0d3-215">5 bits (00011)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-215">5 bits (00011)</span></span> |
| <span data-ttu-id="9c0d3-216">12</span><span class="sxs-lookup"><span data-stu-id="9c0d3-216">12</span></span>   | <span data-ttu-id="9c0d3-217">63 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-217">63 bits</span></span>           | <span data-ttu-id="9c0d3-218">0 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-218">0 bits</span></span>    | <span data-ttu-id="9c0d3-219">60 bits (11.9, 11.9, 11.9)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-219">60 bits (11.9, 11.9, 11.9)</span></span>       | <span data-ttu-id="9c0d3-220">5 bits (00111)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-220">5 bits (00111)</span></span> |
| <span data-ttu-id="9c0d3-221">13</span><span class="sxs-lookup"><span data-stu-id="9c0d3-221">13</span></span>   | <span data-ttu-id="9c0d3-222">63 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-222">63 bits</span></span>           | <span data-ttu-id="9c0d3-223">0 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-223">0 bits</span></span>    | <span data-ttu-id="9c0d3-224">60 bits (12.8, 12.8, 12.8)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-224">60 bits (12.8, 12.8, 12.8)</span></span>       | <span data-ttu-id="9c0d3-225">5 bits (01011)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-225">5 bits (01011)</span></span> |
| <span data-ttu-id="9c0d3-226">14</span><span class="sxs-lookup"><span data-stu-id="9c0d3-226">14</span></span>   | <span data-ttu-id="9c0d3-227">63 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-227">63 bits</span></span>           | <span data-ttu-id="9c0d3-228">0 bits</span><span class="sxs-lookup"><span data-stu-id="9c0d3-228">0 bits</span></span>    | <span data-ttu-id="9c0d3-229">60 bits (16.4, 16.4, 16.4)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-229">60 bits (16.4, 16.4, 16.4)</span></span>       | <span data-ttu-id="9c0d3-230">5 bits (01111)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-230">5 bits (01111)</span></span> |



 

<span data-ttu-id="9c0d3-231">Cada formato nesta tabela pode ser identificado exclusivamente pelos bits de modo.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-231">Each format in this table can be uniquely identified by the mode bits.</span></span> <span data-ttu-id="9c0d3-232">Os dez primeiros modos são usados para blocos de duas regiões e o campo de bit de modo pode ter dois ou cinco bits de comprimento.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-232">The first ten modes are used for two-region tiles, and the mode bit field can be either two or five bits long.</span></span> <span data-ttu-id="9c0d3-233">Esses blocos também têm campos para os pontos de extremidade de cor compactados (72 ou 75 bits), a partição (5 bits) e os índices de partição (46 bits).</span><span class="sxs-lookup"><span data-stu-id="9c0d3-233">These blocks also have fields for the compressed color endpoints (72 or 75 bits), the partition (5 bits), and the partition indices (46 bits).</span></span>

<span data-ttu-id="9c0d3-234">Para os pontos de extremidade de cor compactados, os valores na tabela anterior denotam a precisão dos pontos de extremidade armazenados RGB e o número de bits usados para cada valor de cor.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-234">For the compressed color endpoints, the values in the preceding table note the precision of the stored RGB endpoints, and the number of bits used for each color value.</span></span> <span data-ttu-id="9c0d3-235">Por exemplo, o modo 3 especifica um nível de precisão de ponto de extremidade de cor de valor 11, e o número de bits usados para armazenar os valores delta dos pontos de extremidade transformados para as cores vermelho, azul e verde (5, 4 e 4 respectivamente).</span><span class="sxs-lookup"><span data-stu-id="9c0d3-235">For example, mode 3 specifies a color endpoint precision level of 11, and the number of bits used to store the delta values of the transformed endpoints for the red, blue and green colors (5, 4, and 4 respectively).</span></span> <span data-ttu-id="9c0d3-236">O modo 10 não usa compactação delta e armazena em vez disso todos os pontos de extremidade de cor explicitamente.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-236">Mode 10 does not use delta compression, and instead stores all four color endpoints explicitly.</span></span>

<span data-ttu-id="9c0d3-237">Os últimos quatro modos de bloco são usados para blocos de uma região, onde o campo de modo é 5 bits.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-237">The last four block modes are used for one-region tiles, where the mode field is 5 bits.</span></span> <span data-ttu-id="9c0d3-238">Esses blocos têm campos para os pontos de extremidade (60 bits) e os índices compactados (63 bits).</span><span class="sxs-lookup"><span data-stu-id="9c0d3-238">These blocks have fields for the endpoints (60 bits) and the compressed indices (63 bits).</span></span> <span data-ttu-id="9c0d3-239">O modo 11 (assim como o modo 10) não usa compactação delta e armazena em vez disso ambos os pontos de extremidade de cor explicitamente.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-239">Mode 11 (like Mode 10) does not use delta compression, and instead stores both color endpoints explicitly.</span></span>

<span data-ttu-id="9c0d3-240">Os modos 10011, 10111, 11011 e 11111 (não mostrados) são reservados.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-240">Modes 10011, 10111, 11011, and 11111 (not shown) are reserved.</span></span> <span data-ttu-id="9c0d3-241">Não use-os em seu codificador.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-241">Do not use these in your encoder.</span></span> <span data-ttu-id="9c0d3-242">Se blocos forem passados ao hardware com um desses modos especificados, o bloco descompactado resultante deverá conter todos os zeros em todos os canais, exceto para o canal alfa.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-242">If the hardware is passed blocks with one of these modes specified, the resulting decompressed block must contain all zeroes in all channels except for the alpha channel.</span></span>

<span data-ttu-id="9c0d3-243">Para o BC6H, o canal alfa sempre deve retornar 1.0, independentemente do modo.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-243">For BC6H, the alpha channel must always return 1.0 regardless of the mode.</span></span>

### <a name="bc6h-partition-set"></a><span data-ttu-id="9c0d3-244">Conjunto de partições BC6H</span><span class="sxs-lookup"><span data-stu-id="9c0d3-244">BC6H Partition Set</span></span>

<span data-ttu-id="9c0d3-245">Há 32 conjuntos de partição possíveis para um bloco de duas regiões, e que estão definidos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-245">There are 32 possible partition sets for a two-region tile, and which are defined in the table below.</span></span> <span data-ttu-id="9c0d3-246">Cada bloco de 4 x 4 representa uma única forma.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-246">Each 4x4 block represents a single shape.</span></span>

![tabela dos conjuntos de partição bc6h](images/bc6h-partition-sets.png)

<span data-ttu-id="9c0d3-248">Nesta tabela de conjuntos de partição, a entrada em negrito e sublinhada é o local do índice correção para o subconjunto 1 (que é especificado com um bit a menos).</span><span class="sxs-lookup"><span data-stu-id="9c0d3-248">In this table of partition sets, the bolded and underlined entry is the location of the fix-up index for subset 1 (which is specified with one less bit).</span></span> <span data-ttu-id="9c0d3-249">O índice de correção de subconjunto 0 é sempre o índice 0, uma vez que o particionamento é sempre organizado de tal forma que o índice 0 esteja sempre o subconjunto 0.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-249">The fix-up index for subset 0 is always index 0, as the partitioning is always arranged such that index 0 is always in subset 0.</span></span> <span data-ttu-id="9c0d3-250">A ordem de partição vai do canto superior esquerdo para o canto inferior direito e, em seguida, move-se da esquerda para a direita e de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-250">Partition order goes from top-left to bottom-right, moving left to right and then top to bottom.</span></span>

## <a name="bc6h-compressed-endpoint-format"></a><span data-ttu-id="9c0d3-251">Formato de ponto de extremidade compactado BC6H</span><span class="sxs-lookup"><span data-stu-id="9c0d3-251">BC6H Compressed Endpoint Format</span></span>

![campos de bit para formatos de ponto de extremidade bc6h compactado](images/bc6h-headers-med.png)

<span data-ttu-id="9c0d3-253">Esta tabela mostra os campos de bit para os pontos de extremidade compactados como uma função de formato de ponto de extremidade, com cada coluna especificando uma codificação e cada linha especificando um campo de bit.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-253">This table shows the bit fields for the compressed endpoints as a function of the endpoint format, with each column specifying an encoding and each row specifying a bit field.</span></span> <span data-ttu-id="9c0d3-254">Essa abordagem ocupa 82 bits para blocos de duas regiões e 65 bits para blocos de uma região.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-254">This approach takes up 82 bits for two-region tiles and 65 bits for one-region tiles.</span></span> <span data-ttu-id="9c0d3-255">Por exemplo, os primeiros 5 bits para a codificação de uma região \[ 16 4 \] acima (especificamente a coluna mais à direita) são bits m \[ 4:0 \] , os próximos 10 bits são bits RW \[ 9:0 \] e assim por diante com os últimos 6 bits que contêm BW \[ 10:15 \] .</span><span class="sxs-lookup"><span data-stu-id="9c0d3-255">As an example, the first 5 bits for the one-region \[16 4\] encoding above (specifically the right-most column) are bits m\[4:0\], the next 10 bits are bits rw\[9:0\], and so on with the last 6 bits containing bw\[10:15\].</span></span>

<span data-ttu-id="9c0d3-256">Os nomes dos campos na tabela acima são definidos da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9c0d3-256">The field names in the table above are defined as follows:</span></span>

| <span data-ttu-id="9c0d3-257">Campo</span><span class="sxs-lookup"><span data-stu-id="9c0d3-257">Field</span></span> | <span data-ttu-id="9c0d3-258">Variável</span><span class="sxs-lookup"><span data-stu-id="9c0d3-258">Variable</span></span>          |
|-------|-------------------|
| <span data-ttu-id="9c0d3-259">m</span><span class="sxs-lookup"><span data-stu-id="9c0d3-259">m</span></span>     | <span data-ttu-id="9c0d3-260">mode</span><span class="sxs-lookup"><span data-stu-id="9c0d3-260">mode</span></span>              |
| <span data-ttu-id="9c0d3-261">d</span><span class="sxs-lookup"><span data-stu-id="9c0d3-261">d</span></span>     | <span data-ttu-id="9c0d3-262">índice de forma</span><span class="sxs-lookup"><span data-stu-id="9c0d3-262">shape index</span></span>       |
| <span data-ttu-id="9c0d3-263">rw</span><span class="sxs-lookup"><span data-stu-id="9c0d3-263">rw</span></span>    | <span data-ttu-id="9c0d3-264">Endpt \[ 0 \] . Um \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="9c0d3-264">endpt\[0\].A\[0\]</span></span> |
| <span data-ttu-id="9c0d3-265">rx</span><span class="sxs-lookup"><span data-stu-id="9c0d3-265">rx</span></span>    | <span data-ttu-id="9c0d3-266">Endpt \[ 0 \] . B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="9c0d3-266">endpt\[0\].B\[0\]</span></span> |
| <span data-ttu-id="9c0d3-267">ry</span><span class="sxs-lookup"><span data-stu-id="9c0d3-267">ry</span></span>    | <span data-ttu-id="9c0d3-268">Endpt \[ 1 \] . Um \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="9c0d3-268">endpt\[1\].A\[0\]</span></span> |
| <span data-ttu-id="9c0d3-269">rz</span><span class="sxs-lookup"><span data-stu-id="9c0d3-269">rz</span></span>    | <span data-ttu-id="9c0d3-270">Endpt \[ 1 \] . B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="9c0d3-270">endpt\[1\].B\[0\]</span></span> |
| <span data-ttu-id="9c0d3-271">gw</span><span class="sxs-lookup"><span data-stu-id="9c0d3-271">gw</span></span>    | <span data-ttu-id="9c0d3-272">Endpt \[ 0 \] . Um \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="9c0d3-272">endpt\[0\].A\[1\]</span></span> |
| <span data-ttu-id="9c0d3-273">gx</span><span class="sxs-lookup"><span data-stu-id="9c0d3-273">gx</span></span>    | <span data-ttu-id="9c0d3-274">Endpt \[ 0 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="9c0d3-274">endpt\[0\].B\[1\]</span></span> |
| <span data-ttu-id="9c0d3-275">gy</span><span class="sxs-lookup"><span data-stu-id="9c0d3-275">gy</span></span>    | <span data-ttu-id="9c0d3-276">Endpt \[ 1 \] . Um \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="9c0d3-276">endpt\[1\].A\[1\]</span></span> |
| <span data-ttu-id="9c0d3-277">gz</span><span class="sxs-lookup"><span data-stu-id="9c0d3-277">gz</span></span>    | <span data-ttu-id="9c0d3-278">Endpt \[ 1 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="9c0d3-278">endpt\[1\].B\[1\]</span></span> |
| <span data-ttu-id="9c0d3-279">bw</span><span class="sxs-lookup"><span data-stu-id="9c0d3-279">bw</span></span>    | <span data-ttu-id="9c0d3-280">Endpt \[ 0 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="9c0d3-280">endpt\[0\].A\[2\]</span></span> |
| <span data-ttu-id="9c0d3-281">bx</span><span class="sxs-lookup"><span data-stu-id="9c0d3-281">bx</span></span>    | <span data-ttu-id="9c0d3-282">Endpt \[ 0 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="9c0d3-282">endpt\[0\].B\[2\]</span></span> |
| <span data-ttu-id="9c0d3-283">by</span><span class="sxs-lookup"><span data-stu-id="9c0d3-283">by</span></span>    | <span data-ttu-id="9c0d3-284">Endpt \[ 1 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="9c0d3-284">endpt\[1\].A\[2\]</span></span> |
| <span data-ttu-id="9c0d3-285">bz</span><span class="sxs-lookup"><span data-stu-id="9c0d3-285">bz</span></span>    | <span data-ttu-id="9c0d3-286">Endpt \[ 1 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="9c0d3-286">endpt\[1\].B\[2\]</span></span> |



 

<span data-ttu-id="9c0d3-287">Endpt i , em que i é 0 ou 1, refere-se ao 0º ou 1º conjunto de pontos \[ \] de extremidade, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-287">Endpt\[i\], where i is either 0 or 1, refers to the 0th or 1st set of endpoints respectively.</span></span>

## <a name="sign-extension-for-endpoint-values"></a><span data-ttu-id="9c0d3-288">Assinar extensão para valores de ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="9c0d3-288">Sign Extension for Endpoint Values</span></span>

<span data-ttu-id="9c0d3-289">Para os blocos de duas regiões, há quatro valores de ponto de extremidade que pode ter seu sinal estendido.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-289">For two-region tiles, there are four endpoint values that can be sign extended.</span></span> <span data-ttu-id="9c0d3-290">Endpt \[ 0 \] . Um será assinado somente se o formato for um formato assinado; os outros pontos de extremidade serão assinados somente se o ponto de extremidade tiver sido transformado ou se o formato for um formato assinado.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-290">Endpt\[0\].A is signed only if the format is a signed format; the other endpoints are signed only if the endpoint was transformed, or if the format is a signed format.</span></span> <span data-ttu-id="9c0d3-291">O código a seguir demonstra o algoritmo para estender o sinal dos valores de ponto de extremidade de duas regiões.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-291">The code below demonstrates the algorithm for extending the sign of two-region endpoint values.</span></span>

``` syntax
static void sign_extend_two_region(Pattern &p, IntEndpts endpts[NREGIONS_TWO])
{
    for (int i=0; i<NCHANNELS; ++i)
    {
      if (BC6H::FORMAT == SIGNED_F16)
        endpts[0].A[i] = SIGN_EXTEND(endpts[0].A[i], p.chan[i].prec);
      if (p.transformed || BC6H::FORMAT == SIGNED_F16)
      {
        endpts[0].B[i] = SIGN_EXTEND(endpts[0].B[i], p.chan[i].delta[0]);
        endpts[1].A[i] = SIGN_EXTEND(endpts[1].A[i], p.chan[i].delta[1]);
        endpts[1].B[i] = SIGN_EXTEND(endpts[1].B[i], p.chan[i].delta[2]);
      }
    }
}
```

<span data-ttu-id="9c0d3-292">Para blocos de uma região, o comportamento é o mesmo, somente com endpt \[ 1 \] removido.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-292">For one-region tiles, the behavior is the same, only with endpt\[1\] removed.</span></span>

``` syntax
static void sign_extend_one_region(Pattern &p, IntEndpts endpts[NREGIONS_ONE])
{
    for (int i=0; i<NCHANNELS; ++i)
    {
    if (BC6H::FORMAT == SIGNED_F16)
        endpts[0].A[i] = SIGN_EXTEND(endpts[0].A[i], p.chan[i].prec);
    if (p.transformed || BC6H::FORMAT == SIGNED_F16) 
        endpts[0].B[i] = SIGN_EXTEND(endpts[0].B[i], p.chan[i].delta[0]);
    }
}
```

## <a name="transform-inversion-for-endpoint-values"></a><span data-ttu-id="9c0d3-293">Transformar inversão para valores de ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="9c0d3-293">Transform Inversion for Endpoint Values</span></span>

<span data-ttu-id="9c0d3-294">Para blocos de duas regiões, a transformação aplica o inverso da codificação de diferença, adicionando o valor base ao endpt \[ 0 \] . Um para as três outras entradas para um total de 9 operações de a adicionar.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-294">For two-region tiles, the transform applies the inverse of the difference encoding, adding the base value at endpt\[0\].A to the three other entries for a total of 9 add operations.</span></span> <span data-ttu-id="9c0d3-295">Na imagem abaixo, o valor base é representado como "A0" e tem a maior precisão de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-295">In the image below, the base value is represented as "A0" and has the highest floating point precision.</span></span> <span data-ttu-id="9c0d3-296">"A1", "B0" e "B1" são todos os deltas calculados a partir do valor de âncora, e esses valores delta são representados com precisão mais baixa.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-296">"A1," "B0," and "B1" are all deltas calculated from the anchor value, and these delta values are represented with lower precision.</span></span> <span data-ttu-id="9c0d3-297">(A0 corresponde ao endpt \[ \] 0. A, B0 corresponde ao endpt \[ \] 0. B, A1 corresponde ao endpt \[ \] 1. A e B1 correspondem ao endpt \[ 1 \] .B.)</span><span class="sxs-lookup"><span data-stu-id="9c0d3-297">(A0 corresponds to endpt\[0\].A, B0 corresponds to endpt\[0\].B, A1 corresponds to endpt\[1\].A, and B1 corresponds to endpt\[1\].B.)</span></span>

![cálculo dos valores de ponto de extremidade de inversão de transformação](images/bc6h-transform-inverse.png)

<span data-ttu-id="9c0d3-299">Para blocos de uma região, há apenas um deslocamento delta e, portanto, apenas 3 operações de adição.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-299">For one-region tiles there is only one delta offset, and therefore only 3 add operations.</span></span>

<span data-ttu-id="9c0d3-300">O descompactador deve garantir que os resultados da transformação inversa não estouram a precisão de \[ endpt 0 \] .a.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-300">The decompressor must ensure that that the results of the inverse transform will not overflow the precision of endpt\[0\].a.</span></span> <span data-ttu-id="9c0d3-301">No caso de um estouro, os valores resultantes da transformação inversa devem ser encapsulados dentro do mesmo número de bits.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-301">In the case of an overflow, the values resulting from the inverse transform must wrap within the same number of bits.</span></span> <span data-ttu-id="9c0d3-302">Se a precisão de A0 for "p" bits, o algoritmo de transformação é:</span><span class="sxs-lookup"><span data-stu-id="9c0d3-302">If the precision of A0 is "p" bits, then the transform algorithm is:</span></span>

`B0 = (B0 + A0) & ((1 << p) - 1)`

<span data-ttu-id="9c0d3-303">Para formatos assinados, os resultados do cálculo do delta também devem ter seu sinal estendido.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-303">For signed formats, the results of the delta calculation must be sign extended as well.</span></span> <span data-ttu-id="9c0d3-304">Se a operação de extensão do sinal considerar estender ambos os sinais, onde 0 é positivo e 1 é negativo, a extensão de sinal de 0 se encarregará da vinculação acima.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-304">If the sign extension operation considers extending both signs, where 0 is positive and 1 is negative, then the sign extension of 0 takes care of the clamp above.</span></span> <span data-ttu-id="9c0d3-305">De maneira equivalente, após a vinculação acima, apenas um valor de 1 (negativo) precisa ter o sinal estendido.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-305">Equivalently, after the clamp above, only a value of 1 (negative) needs to be sign extended.</span></span>

## <a name="unquantization-of-color-endpoints"></a><span data-ttu-id="9c0d3-306">Não resquantação de pontos de extremidade de cor</span><span class="sxs-lookup"><span data-stu-id="9c0d3-306">Unquantization of Color Endpoints</span></span>

<span data-ttu-id="9c0d3-307">Considerando os pontos de extremidade não compactados, a próxima etapa é executar uma desquantização inicial dos pontos de extremidade de cor.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-307">Given the uncompressed endpoints, the next step is to perform an initial unquantization of the color endpoints.</span></span> <span data-ttu-id="9c0d3-308">Isso envolve três etapas:</span><span class="sxs-lookup"><span data-stu-id="9c0d3-308">This involves three steps:</span></span>

-   <span data-ttu-id="9c0d3-309">Um desquantização de paletas de cores</span><span class="sxs-lookup"><span data-stu-id="9c0d3-309">An unquantization of the color palettes</span></span>
-   <span data-ttu-id="9c0d3-310">Interpolação de paletas</span><span class="sxs-lookup"><span data-stu-id="9c0d3-310">Interpolation of the palettes</span></span>
-   <span data-ttu-id="9c0d3-311">Finalização da desquantização</span><span class="sxs-lookup"><span data-stu-id="9c0d3-311">Unquantization finalization</span></span>

<span data-ttu-id="9c0d3-312">Dividir o processo de desquantização em duas partes (desquantização da paleta de cores antes da interpolação e desquantização final após a interpolação) reduz o número de operações de multiplicação necessárias quando comparado a um processo completo de desquantização antes da interpolação de paleta.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-312">Separating the unquantization process into two parts (color palette unquantization before interpolation and final unquantization after interpolation) reduces the number of multiplication operations required when compared to a full unquantization process before palette interpolation.</span></span>

<span data-ttu-id="9c0d3-313">O código a seguir ilustra o processo para recuperar estimativas dos valores de cor de 16 bits original e, em seguida, usando os valores de peso fornecidos para adicionar 6 valores de cor adicional à paleta.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-313">The code below illustrates the process for retrieving estimates of the original 16-bit color values, and then using the supplied weight values to add 6 additional color values to the palette.</span></span> <span data-ttu-id="9c0d3-314">A mesma operação é executada em cada canal.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-314">The same operation is performed on each channel.</span></span>

``` syntax
int aWeight3[] = {0, 9, 18, 27, 37, 46, 55, 64};
int aWeight4[] = {0, 4, 9, 13, 17, 21, 26, 30, 34, 38, 43, 47, 51, 55, 60, 64};

// c1, c2: endpoints of a component
void generate_palette_unquantized(UINT8 uNumIndices, int c1, int c2, int prec, UINT16 palette[NINDICES])
{
    int* aWeights;
    if(uNumIndices == 8)
        aWeights = aWeight3;
    else  // uNumIndices == 16
        aWeights = aWeight4;

    int a = unquantize(c1, prec); 
    int b = unquantize(c2, prec);

    // interpolate
    for(int i = 0; i < uNumIndices; ++i)
        palette[i] = finish_unquantize((a * (64 - aWeights[i]) + b * aWeights[i] + 32) >> 6);
}
```

<span data-ttu-id="9c0d3-315">O exemplo de código a seguir demonstra o processo de interpolação, com as seguintes observações:</span><span class="sxs-lookup"><span data-stu-id="9c0d3-315">The next code sample demonstrates the interpolation process, with the following observations:</span></span>

-   <span data-ttu-id="9c0d3-316">Como a gama completa de valores de cor para a função **unquantize** (abaixo) fica entre -32768 e 65535, o interpolador é implementado usando aritmética assinada de 17 bits.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-316">Since the full range of color values for the **unquantize** function (below) are from -32768 to 65535, the interpolator is implemented using 17-bit signed arithmetic.</span></span>
-   <span data-ttu-id="9c0d3-317">Após a interpolação, os valores são passados para a função **\_ final unquantize** (descrita no terceiro exemplo nesta seção), que aplica o dimensionamento final.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-317">After interpolation, the values are passed to the **finish\_unquantize** function (described in the third sample in this section), which applies the final scaling.</span></span>
-   <span data-ttu-id="9c0d3-318">Todos os descompactadores de hardware são obrigatórios para retornar resultados precisos de bit com essas funções.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-318">All hardware decompressors are required to return bit-accurate results with these functions.</span></span>

``` syntax
int unquantize(int comp, int uBitsPerComp)
{
    int unq, s = 0;
    switch(BC6H::FORMAT)
    {
    case UNSIGNED_F16:
        if(uBitsPerComp >= 15)
            unq = comp;
        else if(comp == 0)
            unq = 0;
        else if(comp == ((1 << uBitsPerComp) - 1))
            unq = 0xFFFF;
        else
            unq = ((comp << 16) + 0x8000) >> uBitsPerComp;
        break;

    case SIGNED_F16:
        if(uBitsPerComp >= 16)
            unq = comp;
        else
        {
            if(comp < 0)
            {
                s = 1;
                comp = -comp;
            }

            if(comp == 0)
                unq = 0;
            else if(comp >= ((1 << (uBitsPerComp - 1)) - 1))
                unq = 0x7FFF;
            else
                unq = ((comp << 15) + 0x4000) >> (uBitsPerComp-1);

            if(s)
                unq = -unq;
        }
        break;
    }
    return unq;
}
```

<span data-ttu-id="9c0d3-319">**finish \_ unquantize é** chamado após a interpolação de paleta.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-319">**finish\_unquantize** is called after palette interpolation.</span></span> <span data-ttu-id="9c0d3-320">A função **unquantize** adia o dimensionamento por 31/32 para assinado, 31/64 para não assinado.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-320">The **unquantize** function postpones the scaling by 31/32 for signed, 31/64 for unsigned.</span></span> <span data-ttu-id="9c0d3-321">Esse comportamento é necessário para obter o valor final no intervalo de metade válido (-0x7BFF ~ 0x7BFF) após a interpolação de paleta para reduzir o número de multiplicações necessárias.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-321">This behavior is required to get the final value into valid half range(-0x7BFF ~ 0x7BFF) after the palette interpolation is completed in order to reduce the number of necessary multiplications.</span></span> <span data-ttu-id="9c0d3-322">**concluir \_ desaquiantizar** aplica o dimensionamento final e retorna um **valor** curto sem assinatura que é reinterpretado na **metade**.</span><span class="sxs-lookup"><span data-stu-id="9c0d3-322">**finish\_unquantize** applies the final scaling and returns an **unsigned short** value that gets reinterpreted into **half**.</span></span>

``` syntax
unsigned short finish_unquantize(int comp)
{
    if(BC6H::FORMAT == UNSIGNED_F16)
    {
        comp = (comp * 31) >> 6;                                         // scale the magnitude by 31/64
        return (unsigned short) comp;
    }
    else // (BC6H::FORMAT == SIGNED_F16)
    {
        comp = (comp < 0) ? -(((-comp) * 31) >> 5) : (comp * 31) >> 5;   // scale the magnitude by 31/32
        int s = 0;
        if(comp < 0)
        {
            s = 0x8000;
            comp = -comp;
        }
        return (unsigned short) (s | comp);
    }
}
```

## <a name="related-topics"></a><span data-ttu-id="9c0d3-323">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9c0d3-323">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c0d3-324">Compactação de bloco de textura no Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="9c0d3-324">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 