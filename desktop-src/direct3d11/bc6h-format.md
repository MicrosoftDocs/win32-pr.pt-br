---
title: Formato BC6H
description: O formato BC6H é um formato de compactação de textura projetado para dar suporte a espaços de cores de intervalo altamente dinâmico (HDR) nos dados de origem.
ms.assetid: D6A1A729-5023-4A94-A8DB-5954D453E136
keywords:
- BC6H
- DXGI_FORMAT_BC6H
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed4b934df742a4d2c99e20b52b7172b64e598dc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007905"
---
# <a name="bc6h-format"></a><span data-ttu-id="12365-105">Formato BC6H</span><span class="sxs-lookup"><span data-stu-id="12365-105">BC6H Format</span></span>

<span data-ttu-id="12365-106">O formato BC6H é um formato de compactação de textura projetado para dar suporte a espaços de cores de intervalo altamente dinâmico (HDR) nos dados de origem.</span><span class="sxs-lookup"><span data-stu-id="12365-106">The BC6H format is a texture compression format designed to support high-dynamic range (HDR) color spaces in source data.</span></span>

-   [<span data-ttu-id="12365-107">Sobre o formato BC6H/DXGI \_ \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="12365-107">About BC6H/DXGI\_FORMAT\_BC6H</span></span>](/windows)
-   [<span data-ttu-id="12365-108">Implementação de BC6H</span><span class="sxs-lookup"><span data-stu-id="12365-108">BC6H Implementation</span></span>](#bc6h-implementation)
-   [<span data-ttu-id="12365-109">Decodificando o formato BC6H</span><span class="sxs-lookup"><span data-stu-id="12365-109">Decoding the BC6H Format</span></span>](#decoding-the-bc6h-format)
-   [<span data-ttu-id="12365-110">Formato de ponto de extremidade compactado BC6H</span><span class="sxs-lookup"><span data-stu-id="12365-110">BC6H Compressed Endpoint Format</span></span>](#bc6h-compressed-endpoint-format)
-   [<span data-ttu-id="12365-111">Extensão de assinatura para valores de ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="12365-111">Sign Extension for Endpoint Values</span></span>](#sign-extension-for-endpoint-values)
-   [<span data-ttu-id="12365-112">Transformar inversão para valores de ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="12365-112">Transform Inversion for Endpoint Values</span></span>](#transform-inversion-for-endpoint-values)
-   [<span data-ttu-id="12365-113">Desquantificação de pontos de extremidade de cor</span><span class="sxs-lookup"><span data-stu-id="12365-113">Unquantization of Color Endpoints</span></span>](#unquantization-of-color-endpoints)
-   [<span data-ttu-id="12365-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12365-114">Related topics</span></span>](#related-topics)

## <a name="about-bc6hdxgi_format_bc6h"></a><span data-ttu-id="12365-115">Sobre o formato BC6H/DXGI \_ \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="12365-115">About BC6H/DXGI\_FORMAT\_BC6H</span></span>

<span data-ttu-id="12365-116">O formato BC6H fornece compactação de alta qualidade para imagens que usam canais de cor HDR, com um valor de 16 bits para cada canal de cor do valor (16: 16:16).</span><span class="sxs-lookup"><span data-stu-id="12365-116">The BC6H format provides high-quality compression for images that use three HDR color channels, with a 16-bit value for each color channel of the value (16:16:16).</span></span> <span data-ttu-id="12365-117">Não há nenhum suporte para um canal alfa.</span><span class="sxs-lookup"><span data-stu-id="12365-117">There is no support for an alpha channel.</span></span>

<span data-ttu-id="12365-118">BC6H é especificado pelos seguintes valores de \_ enumeração de formato DXGI:</span><span class="sxs-lookup"><span data-stu-id="12365-118">BC6H is specified by the following DXGI\_FORMAT enumeration values:</span></span>

-   <span data-ttu-id="12365-119">**Dxgi \_ BC6H de formato não \_ \_ Type**.</span><span class="sxs-lookup"><span data-stu-id="12365-119">**DXGI\_FORMAT\_BC6H\_TYPELESS**.</span></span>
-   <span data-ttu-id="12365-120">**Dxgi \_ FORMAT \_ BC6H \_ UF16**.</span><span class="sxs-lookup"><span data-stu-id="12365-120">**DXGI\_FORMAT\_BC6H\_UF16**.</span></span> <span data-ttu-id="12365-121">Esse formato BC6H não usa um bit de sinal nos valores de canal de cor da ponto flutuante de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="12365-121">This BC6H format does not use a sign bit in the 16-bit floating point color channel values.</span></span>
-   <span data-ttu-id="12365-122">**Dxgi \_ FORMAT \_ BC6H \_ SF16**. Esse formato BC6H usa um bit de sinal nos valores de canal de cor de ponto flutuante de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="12365-122">**DXGI\_FORMAT\_BC6H\_SF16**.This BC6H format uses a sign bit in the 16-bit floating point color channel values.</span></span>

> [!Note]  
> <span data-ttu-id="12365-123">O formato de ponto flutuante de 16 bits para canais de cor é geralmente chamado de formato de ponto flutuante "metade".</span><span class="sxs-lookup"><span data-stu-id="12365-123">The 16 bit floating point format for color channels is often referred to as a "half" floating point format.</span></span> <span data-ttu-id="12365-124">Esse formato tem o seguinte layout de bit:</span><span class="sxs-lookup"><span data-stu-id="12365-124">This format has the following bit layout:</span></span>
>
> |                       |                                                 |
> |-----------------------|-------------------------------------------------|
> | <span data-ttu-id="12365-125">UF16 (float não assinado)</span><span class="sxs-lookup"><span data-stu-id="12365-125">UF16 (unsigned float)</span></span> | <span data-ttu-id="12365-126">5 bits de expoente + 11 bits de mantissa</span><span class="sxs-lookup"><span data-stu-id="12365-126">5 exponent bits + 11 mantissa bits</span></span>              |
> | <span data-ttu-id="12365-127">SF16 (float assinado)</span><span class="sxs-lookup"><span data-stu-id="12365-127">SF16 (signed float)</span></span>   | <span data-ttu-id="12365-128">1 bit de sinal + 5 bits de expoente + 10 bits de mantissa</span><span class="sxs-lookup"><span data-stu-id="12365-128">1 sign bit + 5 exponent bits + 10 mantissa bits</span></span> |
>
> 
>
>  

 

<span data-ttu-id="12365-129">O formato BC6H pode ser usado para o recursos de textura [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (incluindo matrizes), Texture3D ou TextureCube (incluindo matrizes).</span><span class="sxs-lookup"><span data-stu-id="12365-129">The BC6H format can be used for [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (including arrays), Texture3D, or TextureCube (including arrays) texture resources.</span></span> <span data-ttu-id="12365-130">Da mesma forma, esse formato se aplica a qualquer superfície de MIP-map associada a esses recursos.</span><span class="sxs-lookup"><span data-stu-id="12365-130">Similarly, this format applies to any MIP-map surfaces associated with these resources.</span></span>

<span data-ttu-id="12365-131">O BC6H usa um tamanho de bloco fixo de 16 bytes (128 bits) e um tamanho de bloco fixo de 4 x 4 texels.</span><span class="sxs-lookup"><span data-stu-id="12365-131">BC6H uses a fixed block size of 16 bytes (128 bits) and a fixed tile size of 4x4 texels.</span></span> <span data-ttu-id="12365-132">Como com os formatos BC anteriores, as imagens de textura maiores que o tamanho de bloco com suporte (4 x 4) são compactadas usando vários blocos.</span><span class="sxs-lookup"><span data-stu-id="12365-132">As with previous BC formats, texture images larger than the supported tile size (4x4) are compressed by using multiple blocks.</span></span> <span data-ttu-id="12365-133">Essa identidade de endereçamento também se aplica a imagens tridimensionais, mapas MIP, cubemaps e matrizes de textura.</span><span class="sxs-lookup"><span data-stu-id="12365-133">This addressing identity applies also to three-dimensional images, MIP-maps, cubemaps, and texture arrays.</span></span> <span data-ttu-id="12365-134">Todos os blocos de imagem devem ser do mesmo formato.</span><span class="sxs-lookup"><span data-stu-id="12365-134">All image tiles must be of the same format.</span></span>

<span data-ttu-id="12365-135">Algumas observações importantes sobre o formato BC6H:</span><span class="sxs-lookup"><span data-stu-id="12365-135">Some important notes about the BC6H format:</span></span>

-   <span data-ttu-id="12365-136">O BC6H suporta a denormalization de ponto flutuante, mas não suporta INF (infinito) e NaN (não numérico).</span><span class="sxs-lookup"><span data-stu-id="12365-136">BC6H supports floating point denormalization, but does not support INF (infinity) and NaN (not a number).</span></span> <span data-ttu-id="12365-137">A exceção é o modo assinado de BC6H ( \_ formato dxgi \_ BC6H \_ SF16), que dá suporte a-inf (infinito negativo).</span><span class="sxs-lookup"><span data-stu-id="12365-137">The exception is the signed mode of BC6H (DXGI\_FORMAT\_BC6H\_SF16), which supports -INF (negative infinity).</span></span> <span data-ttu-id="12365-138">Observe que esse suporte para-INF é meramente um artefato do próprio formato e não é especificamente suportado por codificadores para esse formato.</span><span class="sxs-lookup"><span data-stu-id="12365-138">Note that this support for -INF is merely an artifact of the format itself, and is not specifically supported by encoders for this format.</span></span> <span data-ttu-id="12365-139">Em geral, quando os codificadores encontram dados de entrada INF (positivos ou negativos) ou NaN, eles devem \\ converter esses dados no valor máximo permitido de representação não-inf e mapear Nan para 0 antes da compactação.</span><span class="sxs-lookup"><span data-stu-id="12365-139">In general, when encoders encounter INF (positive or negative) or NaN input data, they should \\ convert that data to the maximum allowable non-INF representation value, and map NaN to 0 prior to compression.</span></span>
-   <span data-ttu-id="12365-140">O BC6H não oferece suporte a um canal alfa.</span><span class="sxs-lookup"><span data-stu-id="12365-140">BC6H does not support an alpha channel.</span></span>
-   <span data-ttu-id="12365-141">O decodificador BC6H executa descompactação antes de realizar a filtragem de textura.</span><span class="sxs-lookup"><span data-stu-id="12365-141">The BC6H decoder performs decompression before it performs texture filtering.</span></span>
-   <span data-ttu-id="12365-142">A descompactação BC6H deve ser um pouco precisa. ou seja, o hardware deve retornar resultados idênticos ao decodificador descrito nesta documentação.</span><span class="sxs-lookup"><span data-stu-id="12365-142">BC6H decompression must be bit accurate; that is, the hardware must return results that are identical to the decoder described in this documentation.</span></span>

## <a name="bc6h-implementation"></a><span data-ttu-id="12365-143">Implementação de BC6H</span><span class="sxs-lookup"><span data-stu-id="12365-143">BC6H Implementation</span></span>

<span data-ttu-id="12365-144">Um bloco de BC6H consiste em bits de modo, pontos de extremidade compactados, índices compactados e um índice de partição opcional.</span><span class="sxs-lookup"><span data-stu-id="12365-144">A BC6H block consists of mode bits, compressed endpoints, compressed indices, and an optional partition index.</span></span> <span data-ttu-id="12365-145">Esse formato especifica 14 modos diferentes.</span><span class="sxs-lookup"><span data-stu-id="12365-145">This format specifies 14 different modes.</span></span>

<span data-ttu-id="12365-146">Uma cor de ponto de extremidade é armazenada como um trio RGB.</span><span class="sxs-lookup"><span data-stu-id="12365-146">An endpoint color is stored as an RGB triplet.</span></span> <span data-ttu-id="12365-147">O BC6H define uma paleta de cores em uma linha aproximada em um número de pontos de extremidade de cores definidos.</span><span class="sxs-lookup"><span data-stu-id="12365-147">BC6H defines a palette of colors on an approximate line across a number of defined color endpoints.</span></span> <span data-ttu-id="12365-148">Além disso, dependendo do modo, um bloco pode ser dividido em duas regiões ou tratado como uma única região, onde um bloco de duas regiões tem um conjunto separado de pontos de extremidade de cor para cada região.</span><span class="sxs-lookup"><span data-stu-id="12365-148">Also, depending on the mode, a tile can be divided into two regions or treated as a single region, where a two-region tile has a separate set of color endpoints for each region.</span></span> <span data-ttu-id="12365-149">O BC6H armazena um índice de paleta por texel.</span><span class="sxs-lookup"><span data-stu-id="12365-149">BC6H stores one palette index per texel.</span></span>

<span data-ttu-id="12365-150">No caso de duas regiões, há 32 partições possíveis.</span><span class="sxs-lookup"><span data-stu-id="12365-150">In the two-region case, there are 32 possible partitions.</span></span>

## <a name="decoding-the-bc6h-format"></a><span data-ttu-id="12365-151">Decodificando o formato BC6H</span><span class="sxs-lookup"><span data-stu-id="12365-151">Decoding the BC6H Format</span></span>

<span data-ttu-id="12365-152">O pseudocódigo a seguir mostra as etapas para descompactar o pixel em (x, y) que recebe o bloco de 16 bytes BC6H.</span><span class="sxs-lookup"><span data-stu-id="12365-152">The pseudocode below shows the steps to decompress the pixel at (x,y) given the 16 byte BC6H block.</span></span>

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

<span data-ttu-id="12365-153">A tabela a seguir contém os valores e a contagem de bit de cada um dos 14 formatos possíveis para blocos de BC6H.</span><span class="sxs-lookup"><span data-stu-id="12365-153">The following table contains the bit count and values for each of the 14 possible formats for BC6H blocks.</span></span> 

| <span data-ttu-id="12365-154">Mode</span><span class="sxs-lookup"><span data-stu-id="12365-154">Mode</span></span> | <span data-ttu-id="12365-155">Índices de partição</span><span class="sxs-lookup"><span data-stu-id="12365-155">Partition Indices</span></span> | <span data-ttu-id="12365-156">Partition</span><span class="sxs-lookup"><span data-stu-id="12365-156">Partition</span></span> | <span data-ttu-id="12365-157">Pontos de extremidade de cor</span><span class="sxs-lookup"><span data-stu-id="12365-157">Color Endpoints</span></span>                  | <span data-ttu-id="12365-158">Bits de modo</span><span class="sxs-lookup"><span data-stu-id="12365-158">Mode Bits</span></span>      |
|------|-------------------|-----------|----------------------------------|----------------|
| <span data-ttu-id="12365-159">1</span><span class="sxs-lookup"><span data-stu-id="12365-159">1</span></span>    | <span data-ttu-id="12365-160">46 bits</span><span class="sxs-lookup"><span data-stu-id="12365-160">46 bits</span></span>           | <span data-ttu-id="12365-161">5 bits</span><span class="sxs-lookup"><span data-stu-id="12365-161">5 bits</span></span>    | <span data-ttu-id="12365-162">75 bits (10.555, 10.555, 10.555)</span><span class="sxs-lookup"><span data-stu-id="12365-162">75 bits (10.555, 10.555, 10.555)</span></span> | <span data-ttu-id="12365-163">2 bits (00)</span><span class="sxs-lookup"><span data-stu-id="12365-163">2 bits (00)</span></span>    |
| <span data-ttu-id="12365-164">2</span><span class="sxs-lookup"><span data-stu-id="12365-164">2</span></span>    | <span data-ttu-id="12365-165">46 bits</span><span class="sxs-lookup"><span data-stu-id="12365-165">46 bits</span></span>           | <span data-ttu-id="12365-166">5 bits</span><span class="sxs-lookup"><span data-stu-id="12365-166">5 bits</span></span>    | <span data-ttu-id="12365-167">75 bits (7666, 7666, 7666)</span><span class="sxs-lookup"><span data-stu-id="12365-167">75 bits (7666, 7666, 7666)</span></span>       | <span data-ttu-id="12365-168">2 bits (01)</span><span class="sxs-lookup"><span data-stu-id="12365-168">2 bits (01)</span></span>    |
| <span data-ttu-id="12365-169">3</span><span class="sxs-lookup"><span data-stu-id="12365-169">3</span></span>    | <span data-ttu-id="12365-170">46 bits</span><span class="sxs-lookup"><span data-stu-id="12365-170">46 bits</span></span>           | <span data-ttu-id="12365-171">5 bits</span><span class="sxs-lookup"><span data-stu-id="12365-171">5 bits</span></span>    | <span data-ttu-id="12365-172">72 bits (11.555, 11.444, 11.444)</span><span class="sxs-lookup"><span data-stu-id="12365-172">72 bits (11.555, 11.444, 11.444)</span></span> | <span data-ttu-id="12365-173">5 bits (00010)</span><span class="sxs-lookup"><span data-stu-id="12365-173">5 bits (00010)</span></span> |
| <span data-ttu-id="12365-174">4</span><span class="sxs-lookup"><span data-stu-id="12365-174">4</span></span>    | <span data-ttu-id="12365-175">46 bits</span><span class="sxs-lookup"><span data-stu-id="12365-175">46 bits</span></span>           | <span data-ttu-id="12365-176">5 bits</span><span class="sxs-lookup"><span data-stu-id="12365-176">5 bits</span></span>    | <span data-ttu-id="12365-177">72 bits (11.444, 11.555, 11.444)</span><span class="sxs-lookup"><span data-stu-id="12365-177">72 bits (11.444, 11.555, 11.444)</span></span> | <span data-ttu-id="12365-178">5 bits (00110)</span><span class="sxs-lookup"><span data-stu-id="12365-178">5 bits (00110)</span></span> |
| <span data-ttu-id="12365-179">5</span><span class="sxs-lookup"><span data-stu-id="12365-179">5</span></span>    | <span data-ttu-id="12365-180">46 bits</span><span class="sxs-lookup"><span data-stu-id="12365-180">46 bits</span></span>           | <span data-ttu-id="12365-181">5 bits</span><span class="sxs-lookup"><span data-stu-id="12365-181">5 bits</span></span>    | <span data-ttu-id="12365-182">72 bits (11.444, 11.444, 11.555)</span><span class="sxs-lookup"><span data-stu-id="12365-182">72 bits (11.444, 11.444, 11.555)</span></span> | <span data-ttu-id="12365-183">5 bits (01010)</span><span class="sxs-lookup"><span data-stu-id="12365-183">5 bits (01010)</span></span> |
| <span data-ttu-id="12365-184">6</span><span class="sxs-lookup"><span data-stu-id="12365-184">6</span></span>    | <span data-ttu-id="12365-185">46 bits</span><span class="sxs-lookup"><span data-stu-id="12365-185">46 bits</span></span>           | <span data-ttu-id="12365-186">5 bits</span><span class="sxs-lookup"><span data-stu-id="12365-186">5 bits</span></span>    | <span data-ttu-id="12365-187">72 bits (9555, 9555, 9555)</span><span class="sxs-lookup"><span data-stu-id="12365-187">72 bits (9555, 9555, 9555)</span></span>       | <span data-ttu-id="12365-188">5 bits (01110)</span><span class="sxs-lookup"><span data-stu-id="12365-188">5 bits (01110)</span></span> |
| <span data-ttu-id="12365-189">7</span><span class="sxs-lookup"><span data-stu-id="12365-189">7</span></span>    | <span data-ttu-id="12365-190">46 bits</span><span class="sxs-lookup"><span data-stu-id="12365-190">46 bits</span></span>           | <span data-ttu-id="12365-191">5 bits</span><span class="sxs-lookup"><span data-stu-id="12365-191">5 bits</span></span>    | <span data-ttu-id="12365-192">72 bits (8666, 8555, 8555)</span><span class="sxs-lookup"><span data-stu-id="12365-192">72 bits (8666, 8555, 8555)</span></span>       | <span data-ttu-id="12365-193">5 bits (10010)</span><span class="sxs-lookup"><span data-stu-id="12365-193">5 bits (10010)</span></span> |
| <span data-ttu-id="12365-194">8</span><span class="sxs-lookup"><span data-stu-id="12365-194">8</span></span>    | <span data-ttu-id="12365-195">46 bits</span><span class="sxs-lookup"><span data-stu-id="12365-195">46 bits</span></span>           | <span data-ttu-id="12365-196">5 bits</span><span class="sxs-lookup"><span data-stu-id="12365-196">5 bits</span></span>    | <span data-ttu-id="12365-197">72 bits (8555, 8666, 8555)</span><span class="sxs-lookup"><span data-stu-id="12365-197">72 bits (8555, 8666, 8555)</span></span>       | <span data-ttu-id="12365-198">5 bits (10110)</span><span class="sxs-lookup"><span data-stu-id="12365-198">5 bits (10110)</span></span> |
| <span data-ttu-id="12365-199">9</span><span class="sxs-lookup"><span data-stu-id="12365-199">9</span></span>    | <span data-ttu-id="12365-200">46 bits</span><span class="sxs-lookup"><span data-stu-id="12365-200">46 bits</span></span>           | <span data-ttu-id="12365-201">5 bits</span><span class="sxs-lookup"><span data-stu-id="12365-201">5 bits</span></span>    | <span data-ttu-id="12365-202">72 bits (8555, 8555, 8666)</span><span class="sxs-lookup"><span data-stu-id="12365-202">72 bits (8555, 8555, 8666)</span></span>       | <span data-ttu-id="12365-203">5 bits (11010)</span><span class="sxs-lookup"><span data-stu-id="12365-203">5 bits (11010)</span></span> |
| <span data-ttu-id="12365-204">10</span><span class="sxs-lookup"><span data-stu-id="12365-204">10</span></span>   | <span data-ttu-id="12365-205">46 bits</span><span class="sxs-lookup"><span data-stu-id="12365-205">46 bits</span></span>           | <span data-ttu-id="12365-206">5 bits</span><span class="sxs-lookup"><span data-stu-id="12365-206">5 bits</span></span>    | <span data-ttu-id="12365-207">72 bits (6666, 6666, 6666)</span><span class="sxs-lookup"><span data-stu-id="12365-207">72 bits (6666, 6666, 6666)</span></span>       | <span data-ttu-id="12365-208">5 bits (11110)</span><span class="sxs-lookup"><span data-stu-id="12365-208">5 bits (11110)</span></span> |
| <span data-ttu-id="12365-209">11</span><span class="sxs-lookup"><span data-stu-id="12365-209">11</span></span>   | <span data-ttu-id="12365-210">63 bits</span><span class="sxs-lookup"><span data-stu-id="12365-210">63 bits</span></span>           | <span data-ttu-id="12365-211">0 bits</span><span class="sxs-lookup"><span data-stu-id="12365-211">0 bits</span></span>    | <span data-ttu-id="12365-212">60 bits (10.10, 10.10, 10.10)</span><span class="sxs-lookup"><span data-stu-id="12365-212">60 bits (10.10, 10.10, 10.10)</span></span>    | <span data-ttu-id="12365-213">5 bits (00011)</span><span class="sxs-lookup"><span data-stu-id="12365-213">5 bits (00011)</span></span> |
| <span data-ttu-id="12365-214">12</span><span class="sxs-lookup"><span data-stu-id="12365-214">12</span></span>   | <span data-ttu-id="12365-215">63 bits</span><span class="sxs-lookup"><span data-stu-id="12365-215">63 bits</span></span>           | <span data-ttu-id="12365-216">0 bits</span><span class="sxs-lookup"><span data-stu-id="12365-216">0 bits</span></span>    | <span data-ttu-id="12365-217">60 bits (11.9, 11.9, 11.9)</span><span class="sxs-lookup"><span data-stu-id="12365-217">60 bits (11.9, 11.9, 11.9)</span></span>       | <span data-ttu-id="12365-218">5 bits (00111)</span><span class="sxs-lookup"><span data-stu-id="12365-218">5 bits (00111)</span></span> |
| <span data-ttu-id="12365-219">13</span><span class="sxs-lookup"><span data-stu-id="12365-219">13</span></span>   | <span data-ttu-id="12365-220">63 bits</span><span class="sxs-lookup"><span data-stu-id="12365-220">63 bits</span></span>           | <span data-ttu-id="12365-221">0 bits</span><span class="sxs-lookup"><span data-stu-id="12365-221">0 bits</span></span>    | <span data-ttu-id="12365-222">60 bits (12.8, 12.8, 12.8)</span><span class="sxs-lookup"><span data-stu-id="12365-222">60 bits (12.8, 12.8, 12.8)</span></span>       | <span data-ttu-id="12365-223">5 bits (01011)</span><span class="sxs-lookup"><span data-stu-id="12365-223">5 bits (01011)</span></span> |
| <span data-ttu-id="12365-224">14</span><span class="sxs-lookup"><span data-stu-id="12365-224">14</span></span>   | <span data-ttu-id="12365-225">63 bits</span><span class="sxs-lookup"><span data-stu-id="12365-225">63 bits</span></span>           | <span data-ttu-id="12365-226">0 bits</span><span class="sxs-lookup"><span data-stu-id="12365-226">0 bits</span></span>    | <span data-ttu-id="12365-227">60 bits (16.4, 16.4, 16.4)</span><span class="sxs-lookup"><span data-stu-id="12365-227">60 bits (16.4, 16.4, 16.4)</span></span>       | <span data-ttu-id="12365-228">5 bits (01111)</span><span class="sxs-lookup"><span data-stu-id="12365-228">5 bits (01111)</span></span> |



 

<span data-ttu-id="12365-229">Cada formato nesta tabela pode ser identificado exclusivamente pelos bits de modo.</span><span class="sxs-lookup"><span data-stu-id="12365-229">Each format in this table can be uniquely identified by the mode bits.</span></span> <span data-ttu-id="12365-230">Os dez primeiros modos são usados para blocos de duas regiões e o campo de bit de modo pode ter dois ou cinco bits de comprimento.</span><span class="sxs-lookup"><span data-stu-id="12365-230">The first ten modes are used for two-region tiles, and the mode bit field can be either two or five bits long.</span></span> <span data-ttu-id="12365-231">Esses blocos também têm campos para os pontos de extremidade de cor compactados (72 ou 75 bits), a partição (5 bits) e os índices de partição (46 bits).</span><span class="sxs-lookup"><span data-stu-id="12365-231">These blocks also have fields for the compressed color endpoints (72 or 75 bits), the partition (5 bits), and the partition indices (46 bits).</span></span>

<span data-ttu-id="12365-232">Para os pontos de extremidade de cor compactados, os valores na tabela anterior denotam a precisão dos pontos de extremidade armazenados RGB e o número de bits usados para cada valor de cor.</span><span class="sxs-lookup"><span data-stu-id="12365-232">For the compressed color endpoints, the values in the preceding table note the precision of the stored RGB endpoints, and the number of bits used for each color value.</span></span> <span data-ttu-id="12365-233">Por exemplo, o modo 3 especifica um nível de precisão de ponto de extremidade de cor de valor 11, e o número de bits usados para armazenar os valores delta dos pontos de extremidade transformados para as cores vermelho, azul e verde (5, 4 e 4 respectivamente).</span><span class="sxs-lookup"><span data-stu-id="12365-233">For example, mode 3 specifies a color endpoint precision level of 11, and the number of bits used to store the delta values of the transformed endpoints for the red, blue and green colors (5, 4, and 4 respectively).</span></span> <span data-ttu-id="12365-234">O modo 10 não usa compactação delta e armazena em vez disso todos os pontos de extremidade de cor explicitamente.</span><span class="sxs-lookup"><span data-stu-id="12365-234">Mode 10 does not use delta compression, and instead stores all four color endpoints explicitly.</span></span>

<span data-ttu-id="12365-235">Os últimos quatro modos de bloco são usados para blocos de uma região, onde o campo de modo é 5 bits.</span><span class="sxs-lookup"><span data-stu-id="12365-235">The last four block modes are used for one-region tiles, where the mode field is 5 bits.</span></span> <span data-ttu-id="12365-236">Esses blocos têm campos para os pontos de extremidade (60 bits) e os índices compactados (63 bits).</span><span class="sxs-lookup"><span data-stu-id="12365-236">These blocks have fields for the endpoints (60 bits) and the compressed indices (63 bits).</span></span> <span data-ttu-id="12365-237">O modo 11 (assim como o modo 10) não usa compactação delta e armazena em vez disso ambos os pontos de extremidade de cor explicitamente.</span><span class="sxs-lookup"><span data-stu-id="12365-237">Mode 11 (like Mode 10) does not use delta compression, and instead stores both color endpoints explicitly.</span></span>

<span data-ttu-id="12365-238">Os modos 10011, 10111, 11011 e 11111 (não mostrados) são reservados.</span><span class="sxs-lookup"><span data-stu-id="12365-238">Modes 10011, 10111, 11011, and 11111 (not shown) are reserved.</span></span> <span data-ttu-id="12365-239">Não use-os em seu codificador.</span><span class="sxs-lookup"><span data-stu-id="12365-239">Do not use these in your encoder.</span></span> <span data-ttu-id="12365-240">Se blocos forem passados ao hardware com um desses modos especificados, o bloco descompactado resultante deverá conter todos os zeros em todos os canais, exceto para o canal alfa.</span><span class="sxs-lookup"><span data-stu-id="12365-240">If the hardware is passed blocks with one of these modes specified, the resulting decompressed block must contain all zeroes in all channels except for the alpha channel.</span></span>

<span data-ttu-id="12365-241">Para o BC6H, o canal alfa sempre deve retornar 1.0, independentemente do modo.</span><span class="sxs-lookup"><span data-stu-id="12365-241">For BC6H, the alpha channel must always return 1.0 regardless of the mode.</span></span>

### <a name="bc6h-partition-set"></a><span data-ttu-id="12365-242">Conjunto de partições BC6H</span><span class="sxs-lookup"><span data-stu-id="12365-242">BC6H Partition Set</span></span>

<span data-ttu-id="12365-243">Há 32 conjuntos de partição possíveis para um bloco de duas regiões, e que estão definidos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="12365-243">There are 32 possible partition sets for a two-region tile, and which are defined in the table below.</span></span> <span data-ttu-id="12365-244">Cada bloco de 4 x 4 representa uma única forma.</span><span class="sxs-lookup"><span data-stu-id="12365-244">Each 4x4 block represents a single shape.</span></span>

![tabela dos conjuntos de partição bc6h](images/bc6h-partition-sets.png)

<span data-ttu-id="12365-246">Nesta tabela de conjuntos de partição, a entrada em negrito e sublinhada é o local do índice correção para o subconjunto 1 (que é especificado com um bit a menos).</span><span class="sxs-lookup"><span data-stu-id="12365-246">In this table of partition sets, the bolded and underlined entry is the location of the fix-up index for subset 1 (which is specified with one less bit).</span></span> <span data-ttu-id="12365-247">O índice de correção de subconjunto 0 é sempre o índice 0, uma vez que o particionamento é sempre organizado de tal forma que o índice 0 esteja sempre o subconjunto 0.</span><span class="sxs-lookup"><span data-stu-id="12365-247">The fix-up index for subset 0 is always index 0, as the partitioning is always arranged such that index 0 is always in subset 0.</span></span> <span data-ttu-id="12365-248">A ordem de partição vai do canto superior esquerdo para o canto inferior direito e, em seguida, move-se da esquerda para a direita e de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="12365-248">Partition order goes from top-left to bottom-right, moving left to right and then top to bottom.</span></span>

## <a name="bc6h-compressed-endpoint-format"></a><span data-ttu-id="12365-249">Formato de ponto de extremidade compactado BC6H</span><span class="sxs-lookup"><span data-stu-id="12365-249">BC6H Compressed Endpoint Format</span></span>

![campos de bit para formatos de ponto de extremidade bc6h compactado](images/bc6h-headers-med.png)

<span data-ttu-id="12365-251">Esta tabela mostra os campos de bit para os pontos de extremidade compactados como uma função de formato de ponto de extremidade, com cada coluna especificando uma codificação e cada linha especificando um campo de bit.</span><span class="sxs-lookup"><span data-stu-id="12365-251">This table shows the bit fields for the compressed endpoints as a function of the endpoint format, with each column specifying an encoding and each row specifying a bit field.</span></span> <span data-ttu-id="12365-252">Essa abordagem ocupa 82 bits para blocos de duas regiões e 65 bits para blocos de uma região.</span><span class="sxs-lookup"><span data-stu-id="12365-252">This approach takes up 82 bits for two-region tiles and 65 bits for one-region tiles.</span></span> <span data-ttu-id="12365-253">Por exemplo, os primeiros 5 bits para a codificação de uma região \[ 16 4 \] acima (especificamente a coluna mais à direita) são bits m \[ 4:0 \] , os próximos 10 bits são bits RW \[ 9:0 \] e assim por diante com os últimos 6 bits que contêm BW \[ 10:15 \] .</span><span class="sxs-lookup"><span data-stu-id="12365-253">As an example, the first 5 bits for the one-region \[16 4\] encoding above (specifically the right-most column) are bits m\[4:0\], the next 10 bits are bits rw\[9:0\], and so on with the last 6 bits containing bw\[10:15\].</span></span>

<span data-ttu-id="12365-254">Os nomes dos campos na tabela acima são definidos da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="12365-254">The field names in the table above are defined as follows:</span></span>

| <span data-ttu-id="12365-255">Campo</span><span class="sxs-lookup"><span data-stu-id="12365-255">Field</span></span> | <span data-ttu-id="12365-256">Variável</span><span class="sxs-lookup"><span data-stu-id="12365-256">Variable</span></span>          |
|-------|-------------------|
| <span data-ttu-id="12365-257">m</span><span class="sxs-lookup"><span data-stu-id="12365-257">m</span></span>     | <span data-ttu-id="12365-258">mode</span><span class="sxs-lookup"><span data-stu-id="12365-258">mode</span></span>              |
| <span data-ttu-id="12365-259">d</span><span class="sxs-lookup"><span data-stu-id="12365-259">d</span></span>     | <span data-ttu-id="12365-260">índice de forma</span><span class="sxs-lookup"><span data-stu-id="12365-260">shape index</span></span>       |
| <span data-ttu-id="12365-261">rw</span><span class="sxs-lookup"><span data-stu-id="12365-261">rw</span></span>    | <span data-ttu-id="12365-262">Endpt \[ 0 \] . Um \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="12365-262">endpt\[0\].A\[0\]</span></span> |
| <span data-ttu-id="12365-263">rx</span><span class="sxs-lookup"><span data-stu-id="12365-263">rx</span></span>    | <span data-ttu-id="12365-264">Endpt \[ 0 \] . B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="12365-264">endpt\[0\].B\[0\]</span></span> |
| <span data-ttu-id="12365-265">ry</span><span class="sxs-lookup"><span data-stu-id="12365-265">ry</span></span>    | <span data-ttu-id="12365-266">Endpt \[ 1 \] . Um \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="12365-266">endpt\[1\].A\[0\]</span></span> |
| <span data-ttu-id="12365-267">rz</span><span class="sxs-lookup"><span data-stu-id="12365-267">rz</span></span>    | <span data-ttu-id="12365-268">Endpt \[ 1 \] . B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="12365-268">endpt\[1\].B\[0\]</span></span> |
| <span data-ttu-id="12365-269">gw</span><span class="sxs-lookup"><span data-stu-id="12365-269">gw</span></span>    | <span data-ttu-id="12365-270">Endpt \[ 0 \] . Um \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="12365-270">endpt\[0\].A\[1\]</span></span> |
| <span data-ttu-id="12365-271">gx</span><span class="sxs-lookup"><span data-stu-id="12365-271">gx</span></span>    | <span data-ttu-id="12365-272">Endpt \[ 0 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="12365-272">endpt\[0\].B\[1\]</span></span> |
| <span data-ttu-id="12365-273">gy</span><span class="sxs-lookup"><span data-stu-id="12365-273">gy</span></span>    | <span data-ttu-id="12365-274">Endpt \[ 1 \] . Um \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="12365-274">endpt\[1\].A\[1\]</span></span> |
| <span data-ttu-id="12365-275">gz</span><span class="sxs-lookup"><span data-stu-id="12365-275">gz</span></span>    | <span data-ttu-id="12365-276">Endpt \[ 1 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="12365-276">endpt\[1\].B\[1\]</span></span> |
| <span data-ttu-id="12365-277">bw</span><span class="sxs-lookup"><span data-stu-id="12365-277">bw</span></span>    | <span data-ttu-id="12365-278">Endpt \[ 0 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="12365-278">endpt\[0\].A\[2\]</span></span> |
| <span data-ttu-id="12365-279">bx</span><span class="sxs-lookup"><span data-stu-id="12365-279">bx</span></span>    | <span data-ttu-id="12365-280">Endpt \[ 0 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="12365-280">endpt\[0\].B\[2\]</span></span> |
| <span data-ttu-id="12365-281">by</span><span class="sxs-lookup"><span data-stu-id="12365-281">by</span></span>    | <span data-ttu-id="12365-282">Endpt \[ 1 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="12365-282">endpt\[1\].A\[2\]</span></span> |
| <span data-ttu-id="12365-283">bz</span><span class="sxs-lookup"><span data-stu-id="12365-283">bz</span></span>    | <span data-ttu-id="12365-284">Endpt \[ 1 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="12365-284">endpt\[1\].B\[2\]</span></span> |



 

<span data-ttu-id="12365-285">Endpt \[ i \] , onde eu é 0 ou 1, refere-se ao 0º ou ao primeiro conjunto de pontos de extremidade, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="12365-285">Endpt\[i\], where i is either 0 or 1, refers to the 0th or 1st set of endpoints respectively.</span></span>

## <a name="sign-extension-for-endpoint-values"></a><span data-ttu-id="12365-286">Extensão de assinatura para valores de ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="12365-286">Sign Extension for Endpoint Values</span></span>

<span data-ttu-id="12365-287">Para os blocos de duas regiões, há quatro valores de ponto de extremidade que pode ter seu sinal estendido.</span><span class="sxs-lookup"><span data-stu-id="12365-287">For two-region tiles, there are four endpoint values that can be sign extended.</span></span> <span data-ttu-id="12365-288">Endpt \[ 0 \] . Um será assinado somente se o formato for um formato assinado; os outros pontos de extremidade serão assinados somente se o ponto de extremidades tiver sido transformado ou se o formato for um formato assinado.</span><span class="sxs-lookup"><span data-stu-id="12365-288">Endpt\[0\].A is signed only if the format is a signed format; the other endpoints are signed only if the endpoint was transformed, or if the format is a signed format.</span></span> <span data-ttu-id="12365-289">O código a seguir demonstra o algoritmo para estender o sinal dos valores de ponto de extremidade de duas regiões.</span><span class="sxs-lookup"><span data-stu-id="12365-289">The code below demonstrates the algorithm for extending the sign of two-region endpoint values.</span></span>

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

<span data-ttu-id="12365-290">Para blocos de uma região, o comportamento é o mesmo, somente com Endpt \[ 1 \] removido.</span><span class="sxs-lookup"><span data-stu-id="12365-290">For one-region tiles, the behavior is the same, only with endpt\[1\] removed.</span></span>

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

## <a name="transform-inversion-for-endpoint-values"></a><span data-ttu-id="12365-291">Transformar inversão para valores de ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="12365-291">Transform Inversion for Endpoint Values</span></span>

<span data-ttu-id="12365-292">Para blocos de duas regiões, a transformação aplica o inverso da codificação de diferença, adicionando o valor base em Endpt \[ 0 \] . Um para as três outras entradas para um total de 9 adicionar operações.</span><span class="sxs-lookup"><span data-stu-id="12365-292">For two-region tiles, the transform applies the inverse of the difference encoding, adding the base value at endpt\[0\].A to the three other entries for a total of 9 add operations.</span></span> <span data-ttu-id="12365-293">Na imagem abaixo, o valor base é representado como "A0" e tem a maior precisão de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="12365-293">In the image below, the base value is represented as "A0" and has the highest floating point precision.</span></span> <span data-ttu-id="12365-294">"A1", "B0" e "B1" são todos os deltas calculados a partir do valor de âncora, e esses valores delta são representados com precisão mais baixa.</span><span class="sxs-lookup"><span data-stu-id="12365-294">"A1," "B0," and "B1" are all deltas calculated from the anchor value, and these delta values are represented with lower precision.</span></span> <span data-ttu-id="12365-295">(A0 corresponde a Endpt \[ 0 \] . A, B0 corresponde a Endpt \[ 0 \] . B, a1 corresponde a Endpt \[ 1 \] . A e B1 corresponde a Endpt \[ 1 \] . B.)</span><span class="sxs-lookup"><span data-stu-id="12365-295">(A0 corresponds to endpt\[0\].A, B0 corresponds to endpt\[0\].B, A1 corresponds to endpt\[1\].A, and B1 corresponds to endpt\[1\].B.)</span></span>

![cálculo dos valores de ponto de extremidade de inversão de transformação](images/bc6h-transform-inverse.png)

<span data-ttu-id="12365-297">Para blocos de uma região, há apenas um deslocamento delta e, portanto, apenas 3 operações de adição.</span><span class="sxs-lookup"><span data-stu-id="12365-297">For one-region tiles there is only one delta offset, and therefore only 3 add operations.</span></span>

<span data-ttu-id="12365-298">O descompactador deve garantir que os resultados da transformação inversa não irão exceder a precisão de Endpt \[ 0 \] . a.</span><span class="sxs-lookup"><span data-stu-id="12365-298">The decompressor must ensure that that the results of the inverse transform will not overflow the precision of endpt\[0\].a.</span></span> <span data-ttu-id="12365-299">No caso de um estouro, os valores resultantes da transformação inversa devem ser encapsulados dentro do mesmo número de bits.</span><span class="sxs-lookup"><span data-stu-id="12365-299">In the case of an overflow, the values resulting from the inverse transform must wrap within the same number of bits.</span></span> <span data-ttu-id="12365-300">Se a precisão de A0 for "p" bits, o algoritmo de transformação é:</span><span class="sxs-lookup"><span data-stu-id="12365-300">If the precision of A0 is "p" bits, then the transform algorithm is:</span></span>

`B0 = (B0 + A0) & ((1 << p) - 1)`

<span data-ttu-id="12365-301">Para formatos assinados, os resultados do cálculo do delta também devem ter seu sinal estendido.</span><span class="sxs-lookup"><span data-stu-id="12365-301">For signed formats, the results of the delta calculation must be sign extended as well.</span></span> <span data-ttu-id="12365-302">Se a operação de extensão do sinal considerar estender ambos os sinais, onde 0 é positivo e 1 é negativo, a extensão de sinal de 0 se encarregará da vinculação acima.</span><span class="sxs-lookup"><span data-stu-id="12365-302">If the sign extension operation considers extending both signs, where 0 is positive and 1 is negative, then the sign extension of 0 takes care of the clamp above.</span></span> <span data-ttu-id="12365-303">De maneira equivalente, após a vinculação acima, apenas um valor de 1 (negativo) precisa ter o sinal estendido.</span><span class="sxs-lookup"><span data-stu-id="12365-303">Equivalently, after the clamp above, only a value of 1 (negative) needs to be sign extended.</span></span>

## <a name="unquantization-of-color-endpoints"></a><span data-ttu-id="12365-304">Desquantificação de pontos de extremidade de cor</span><span class="sxs-lookup"><span data-stu-id="12365-304">Unquantization of Color Endpoints</span></span>

<span data-ttu-id="12365-305">Considerando os pontos de extremidade não compactados, a próxima etapa é executar uma desquantização inicial dos pontos de extremidade de cor.</span><span class="sxs-lookup"><span data-stu-id="12365-305">Given the uncompressed endpoints, the next step is to perform an initial unquantization of the color endpoints.</span></span> <span data-ttu-id="12365-306">Isso envolve três etapas:</span><span class="sxs-lookup"><span data-stu-id="12365-306">This involves three steps:</span></span>

-   <span data-ttu-id="12365-307">Um desquantização de paletas de cores</span><span class="sxs-lookup"><span data-stu-id="12365-307">An unquantization of the color palettes</span></span>
-   <span data-ttu-id="12365-308">Interpolação de paletas</span><span class="sxs-lookup"><span data-stu-id="12365-308">Interpolation of the palettes</span></span>
-   <span data-ttu-id="12365-309">Finalização da desquantização</span><span class="sxs-lookup"><span data-stu-id="12365-309">Unquantization finalization</span></span>

<span data-ttu-id="12365-310">Dividir o processo de desquantização em duas partes (desquantização da paleta de cores antes da interpolação e desquantização final após a interpolação) reduz o número de operações de multiplicação necessárias quando comparado a um processo completo de desquantização antes da interpolação de paleta.</span><span class="sxs-lookup"><span data-stu-id="12365-310">Separating the unquantization process into two parts (color palette unquantization before interpolation and final unquantization after interpolation) reduces the number of multiplication operations required when compared to a full unquantization process before palette interpolation.</span></span>

<span data-ttu-id="12365-311">O código a seguir ilustra o processo para recuperar estimativas dos valores de cor de 16 bits original e, em seguida, usando os valores de peso fornecidos para adicionar 6 valores de cor adicional à paleta.</span><span class="sxs-lookup"><span data-stu-id="12365-311">The code below illustrates the process for retrieving estimates of the original 16-bit color values, and then using the supplied weight values to add 6 additional color values to the palette.</span></span> <span data-ttu-id="12365-312">A mesma operação é executada em cada canal.</span><span class="sxs-lookup"><span data-stu-id="12365-312">The same operation is performed on each channel.</span></span>

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

<span data-ttu-id="12365-313">O exemplo de código a seguir demonstra o processo de interpolação, com as seguintes observações:</span><span class="sxs-lookup"><span data-stu-id="12365-313">The next code sample demonstrates the interpolation process, with the following observations:</span></span>

-   <span data-ttu-id="12365-314">Como a gama completa de valores de cor para a função **unquantize** (abaixo) fica entre -32768 e 65535, o interpolador é implementado usando aritmética assinada de 17 bits.</span><span class="sxs-lookup"><span data-stu-id="12365-314">Since the full range of color values for the **unquantize** function (below) are from -32768 to 65535, the interpolator is implemented using 17-bit signed arithmetic.</span></span>
-   <span data-ttu-id="12365-315">Após a interpolação, os valores são passados para a função de **\_ desquantificação de término** (descrita no terceiro exemplo nesta seção), que aplica o dimensionamento final.</span><span class="sxs-lookup"><span data-stu-id="12365-315">After interpolation, the values are passed to the **finish\_unquantize** function (described in the third sample in this section), which applies the final scaling.</span></span>
-   <span data-ttu-id="12365-316">Todos os descompactadores de hardware são obrigatórios para retornar resultados precisos de bit com essas funções.</span><span class="sxs-lookup"><span data-stu-id="12365-316">All hardware decompressors are required to return bit-accurate results with these functions.</span></span>

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

<span data-ttu-id="12365-317">**concluir \_ unquantificate** é chamado após a interpolação da paleta.</span><span class="sxs-lookup"><span data-stu-id="12365-317">**finish\_unquantize** is called after palette interpolation.</span></span> <span data-ttu-id="12365-318">A função **unquantize** adia o dimensionamento por 31/32 para assinado, 31/64 para não assinado.</span><span class="sxs-lookup"><span data-stu-id="12365-318">The **unquantize** function postpones the scaling by 31/32 for signed, 31/64 for unsigned.</span></span> <span data-ttu-id="12365-319">Esse comportamento é necessário para obter o valor final no intervalo de metade válido (-0x7BFF ~ 0x7BFF) após a interpolação de paleta para reduzir o número de multiplicações necessárias.</span><span class="sxs-lookup"><span data-stu-id="12365-319">This behavior is required to get the final value into valid half range(-0x7BFF ~ 0x7BFF) after the palette interpolation is completed in order to reduce the number of necessary multiplications.</span></span> <span data-ttu-id="12365-320">**terminar \_ desquantificar** aplica o dimensionamento final e retorna um valor **curto sem sinal** que é reinterpretado na **metade**.</span><span class="sxs-lookup"><span data-stu-id="12365-320">**finish\_unquantize** applies the final scaling and returns an **unsigned short** value that gets reinterpreted into **half**.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="12365-321">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12365-321">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12365-322">Compactação de bloco de textura no Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="12365-322">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 