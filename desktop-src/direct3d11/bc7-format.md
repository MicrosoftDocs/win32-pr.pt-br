---
title: Formato BC7
description: O formato BC7 é um formato de compactação de textura usado para compactação de alta qualidade de dados de RGB e RGBA.
ms.assetid: DF333106-293E-4B3E-A1EB-B0BF0ADBAC72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9b64c3d4a8b5e960077a9f33de82ff08cd4bbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366511"
---
# <a name="bc7-format"></a><span data-ttu-id="b376d-103">Formato BC7</span><span class="sxs-lookup"><span data-stu-id="b376d-103">BC7 Format</span></span>

<span data-ttu-id="b376d-104">O formato BC7 é um formato de compactação de textura usado para compactação de alta qualidade de dados de RGB e RGBA.</span><span class="sxs-lookup"><span data-stu-id="b376d-104">The BC7 format is a texture compression format used for high-quality compression of RGB and RGBA data.</span></span>

-   [<span data-ttu-id="b376d-105">Sobre o formato BC7/DXGI \_ \_ BC7</span><span class="sxs-lookup"><span data-stu-id="b376d-105">About BC7/DXGI\_FORMAT\_BC7</span></span>](/windows)
-   [<span data-ttu-id="b376d-106">Implementação de BC7</span><span class="sxs-lookup"><span data-stu-id="b376d-106">BC7 Implementation</span></span>](#bc7-implementation)
-   [<span data-ttu-id="b376d-107">Decodificando o formato BC7</span><span class="sxs-lookup"><span data-stu-id="b376d-107">Decoding the BC7 Format</span></span>](#decoding-the-bc7-format)
-   [<span data-ttu-id="b376d-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b376d-108">Related topics</span></span>](#related-topics)

<span data-ttu-id="b376d-109">Para obter informações sobre os modos de bloco do formato BC7, consulte [Referência do Modo de Formato BC7](bc7-format-mode-reference.md).</span><span class="sxs-lookup"><span data-stu-id="b376d-109">For info about the block modes of the BC7 format, see [BC7 Format Mode Reference](bc7-format-mode-reference.md).</span></span>

## <a name="about-bc7dxgi_format_bc7"></a><span data-ttu-id="b376d-110">Sobre o formato BC7/DXGI \_ \_ BC7</span><span class="sxs-lookup"><span data-stu-id="b376d-110">About BC7/DXGI\_FORMAT\_BC7</span></span>

<span data-ttu-id="b376d-111">BC7 é especificado pelos seguintes valores de \_ enumeração de formato DXGI:</span><span class="sxs-lookup"><span data-stu-id="b376d-111">BC7 is specified by the following DXGI\_FORMAT enumeration values:</span></span>

-   <span data-ttu-id="b376d-112">**Dxgi \_ BC7 de formato não \_ \_ Type**.</span><span class="sxs-lookup"><span data-stu-id="b376d-112">**DXGI\_FORMAT\_BC7\_TYPELESS**.</span></span>
-   <span data-ttu-id="b376d-113">**Dxgi \_ FORMAT \_ BC7 \_ UNORM**.</span><span class="sxs-lookup"><span data-stu-id="b376d-113">**DXGI\_FORMAT\_BC7\_UNORM**.</span></span>
-   <span data-ttu-id="b376d-114">**Dxgi \_ FORMATO \_ BC7 \_ UNORM \_ sRGB**.</span><span class="sxs-lookup"><span data-stu-id="b376d-114">**DXGI\_FORMAT\_BC7\_UNORM\_SRGB**.</span></span>

<span data-ttu-id="b376d-115">O formato BC7 pode ser usado para o recursos de textura [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (incluindo matrizes), Texture3D ou TextureCube (incluindo matrizes).</span><span class="sxs-lookup"><span data-stu-id="b376d-115">The BC7 format can be used for [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (including arrays), Texture3D, or TextureCube (including arrays) texture resources.</span></span> <span data-ttu-id="b376d-116">Da mesma forma, esse formato se aplica a qualquer superfície de MIP-map associada a esses recursos.</span><span class="sxs-lookup"><span data-stu-id="b376d-116">Similarly, this format applies to any MIP-map surfaces associated with these resources.</span></span>

<span data-ttu-id="b376d-117">O BC7 usa um tamanho de bloco fixo de 16 bytes (128 bits) e um tamanho de bloco fixo de 4 x 4 texels.</span><span class="sxs-lookup"><span data-stu-id="b376d-117">BC7 uses a fixed block size of 16 bytes (128 bits) and a fixed tile size of 4x4 texels.</span></span> <span data-ttu-id="b376d-118">Como com os formatos BC anteriores, as imagens de textura maiores que o tamanho de bloco com suporte (4 x 4) são compactadas usando vários blocos.</span><span class="sxs-lookup"><span data-stu-id="b376d-118">As with previous BC formats, texture images larger than the supported tile size (4x4) are compressed by using multiple blocks.</span></span> <span data-ttu-id="b376d-119">Essa identidade endereçamento se aplica também a imagens tridimensionais, mapas MIP, mapas de cubo e matrizes de textura.</span><span class="sxs-lookup"><span data-stu-id="b376d-119">This addressing identity also applies to three-dimensional images and MIP-maps, cubemaps, and texture arrays.</span></span> <span data-ttu-id="b376d-120">Todos os blocos de imagem devem ser do mesmo formato.</span><span class="sxs-lookup"><span data-stu-id="b376d-120">All image tiles must be of the same format.</span></span>

<span data-ttu-id="b376d-121">O BC7 compacta imagens de dados de ponto fixo de três canais (RGB) e quatro canais (RGBA).</span><span class="sxs-lookup"><span data-stu-id="b376d-121">BC7 compresses both three-channel (RGB) and four-channel (RGBA) fixed-point data images.</span></span> <span data-ttu-id="b376d-122">Normalmente, os dados de origem tem 8 bits por componente de cor (canal), embora o formato seja capaz de codificar dados de origem com maior quantidade de bits por componente de cor.</span><span class="sxs-lookup"><span data-stu-id="b376d-122">Typically, source data is 8 bits per color component (channel), although the format is capable of encoding source data with higher bits per color component.</span></span> <span data-ttu-id="b376d-123">Todos os blocos de imagem devem ser do mesmo formato.</span><span class="sxs-lookup"><span data-stu-id="b376d-123">All image tiles must be of the same format.</span></span>

<span data-ttu-id="b376d-124">O decodificador BC7 executa descompactação antes da filtragem de textura ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="b376d-124">The BC7 decoder performs decompression before texture filtering is applied.</span></span>

<span data-ttu-id="b376d-125">O hardware de descompactação BC7 deve ter precisão de bit, ou seja, o hardware deve retornar resultados que são idênticos aos resultados retornados pelo decodificador descrito neste documento.</span><span class="sxs-lookup"><span data-stu-id="b376d-125">BC7 decompression hardware must be bit accurate; that is, the hardware must return results that are identical to the results returned by the decoder described in this document.</span></span>

## <a name="bc7-implementation"></a><span data-ttu-id="b376d-126">Implementação do BC7</span><span class="sxs-lookup"><span data-stu-id="b376d-126">BC7 Implementation</span></span>

<span data-ttu-id="b376d-127">Uma implementação de BC7 pode especificar um dos 8 modos, com o modo especificado no bit menos significativo do bloco de 16 bytes (128 bits).</span><span class="sxs-lookup"><span data-stu-id="b376d-127">A BC7 implementation can specify one of 8 modes, with the mode specified in the least significant bit of the 16 byte (128 bit) block.</span></span> <span data-ttu-id="b376d-128">O modo é codificado por zero ou mais bits com um valor de 0 seguido por um 1.</span><span class="sxs-lookup"><span data-stu-id="b376d-128">The mode is encoded by zero or more bits with a value of 0 followed by a 1.</span></span>

<span data-ttu-id="b376d-129">Um bloco BC7 pode conter vários pares de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="b376d-129">A BC7 block can contain multiple endpoint pairs.</span></span> <span data-ttu-id="b376d-130">Para os fins desta documentação, o conjunto de índices que correspondem a um par de pontos de extremidade pode ser chamado de "subconjunto".</span><span class="sxs-lookup"><span data-stu-id="b376d-130">For the purposes of this documentation, the set of indices that correspond to an endpoint pair may be referred to as a "subset."</span></span> <span data-ttu-id="b376d-131">Além disso, em alguns modos de bloco, a representação do ponto de extremidade é codificada em um formulário que, novamente, para os fins desta documentação, deve ser chamada de "RBGP", onde o bit "P" representa um bit menos significativo compartilhado para os componentes de cor do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="b376d-131">Also, in some block modes, the endpoint representation is encoded in a form that -- again, for the purposes of this documentation -- shall be referred to as "RBGP," where the "P" bit represents a shared least significant bit for the color components of the endpoint.</span></span> <span data-ttu-id="b376d-132">Por exemplo, se a representação de ponto de extremidade para o formato for "RGB 5.5.5.1", então o ponto de extremidade é interpretado como um valor RGB 6.6.6, onde o estado do bit P define o bit menos significativo de cada componente.</span><span class="sxs-lookup"><span data-stu-id="b376d-132">For example, if the endpoint representation for the format is "RGB 5.5.5.1," then the endpoint is interpreted as an RGB 6.6.6 value, where the state of the P-bit defines the least significant bit of each component.</span></span> <span data-ttu-id="b376d-133">Da mesma forma, para dados de origem com um canal alfa, se a representação para o formato for "RGBAP 5.5.5.5.1", o ponto de extremidade será interepreted como RGBA 6.6.6.6.</span><span class="sxs-lookup"><span data-stu-id="b376d-133">Similarly, for source data with an alpha channel, if the representation for the format is "RGBAP 5.5.5.5.1," then the endpoint is interepreted as RGBA 6.6.6.6.</span></span> <span data-ttu-id="b376d-134">Dependendo do modo de bloco, você pode especificar o bit menos significativo compartilhado para um ambos os pontos de extremidade de um subconjunto individualmente (2 bits P por subconjunto), ou compartilhados entre os pontos de extremidade de um subconjunto (1 bit P por subconjunto).</span><span class="sxs-lookup"><span data-stu-id="b376d-134">Depending on the block mode, you can specify the shared least significant bit for either both endpoints of a subset individually (2 P-bits per subset), or shared between endpoints of a subset (1 P-bit per subset).</span></span>

<span data-ttu-id="b376d-135">Para os blocos de BC7 que não codificam explicitamente o componente alfa, um bloco BC7 consiste em bits de modo, bits de partição, pontos de extremidade compactados, índices compactados e um bit P opcional.</span><span class="sxs-lookup"><span data-stu-id="b376d-135">For BC7 blocks that don't explicitly encode the alpha component, a BC7 block consists of mode bits, partition bits, compressed endpoints, compressed indices, and an optional P-bit.</span></span> <span data-ttu-id="b376d-136">Nesses blocos, os pontos de extremidade têm uma representação somente RGB e o componente alfa é decodificado como 1.0 para todos os texels nos dados de origem.</span><span class="sxs-lookup"><span data-stu-id="b376d-136">In these blocks the endpoints have an RGB-only representation and the alpha component is decoded as 1.0 for all texels in the source data.</span></span>

<span data-ttu-id="b376d-137">Para os blocos de BC7 que tem componentes de cor e alfa combinados, um bloco consiste em bits de modo, pontos de extremidade compactados, índices compactados, bits de partição opcionais e um bit P.</span><span class="sxs-lookup"><span data-stu-id="b376d-137">For BC7 blocks that have combined color and alpha components, a block consists of mode bits, compressed endpoints, compressed indices, and optional partition bits and a P-bit.</span></span> <span data-ttu-id="b376d-138">Nesses blocos, as cores de ponto de extremidade são expressas em formato RGBA e os valores de componente alfa são interpolados junto com os valores de componente de cor.</span><span class="sxs-lookup"><span data-stu-id="b376d-138">In these blocks, the endpoint colors are expressed in RGBA format, and alpha component values are interpolated alongside the color component values.</span></span>

<span data-ttu-id="b376d-139">Para os blocos BC7 que têm componentes de cor e alfa separados, um bloco consiste em bits de modo, bits de rotação, pontos de extremidade compactados, índices compactados, e um bit seletor de índice opcional.</span><span class="sxs-lookup"><span data-stu-id="b376d-139">For BC7 blocks that have separate color and alpha components, a block consists of mode bits, rotation bits, compressed endpoints, compressed indices, and an optional index selector bit.</span></span> <span data-ttu-id="b376d-140">Esses blocos têm um R de vetor RGB efetivo \[ , G, B \] e um canal alfa escalar \[ um \] codificado separadamente.</span><span class="sxs-lookup"><span data-stu-id="b376d-140">These blocks have an effective RGB vector \[R, G, B\] and a scalar alpha channel \[A\] separately encoded.</span></span>

<span data-ttu-id="b376d-141">A tabela a seguir lista os componentes de cada tipo de bloco.</span><span class="sxs-lookup"><span data-stu-id="b376d-141">The following table lists the components of each block type.</span></span>



| <span data-ttu-id="b376d-142">O bloco BC7 contém...</span><span class="sxs-lookup"><span data-stu-id="b376d-142">BC7 block contains...</span></span>     | <span data-ttu-id="b376d-143">bits de modo</span><span class="sxs-lookup"><span data-stu-id="b376d-143">mode bits</span></span> | <span data-ttu-id="b376d-144">bits de rotação</span><span class="sxs-lookup"><span data-stu-id="b376d-144">rotation bits</span></span> | <span data-ttu-id="b376d-145">bits de seletor de índice</span><span class="sxs-lookup"><span data-stu-id="b376d-145">index selector bit</span></span> | <span data-ttu-id="b376d-146">bits de partição</span><span class="sxs-lookup"><span data-stu-id="b376d-146">partition bits</span></span> | <span data-ttu-id="b376d-147">pontos de extremidade compactados</span><span class="sxs-lookup"><span data-stu-id="b376d-147">compressed endpoints</span></span> | <span data-ttu-id="b376d-148">bit P</span><span class="sxs-lookup"><span data-stu-id="b376d-148">P-bit</span></span>    | <span data-ttu-id="b376d-149">índices compactados</span><span class="sxs-lookup"><span data-stu-id="b376d-149">compressed indices</span></span> |
|---------------------------|-----------|---------------|--------------------|----------------|----------------------|----------|--------------------|
| <span data-ttu-id="b376d-150">somente os componentes de cor</span><span class="sxs-lookup"><span data-stu-id="b376d-150">color components only</span></span>     | <span data-ttu-id="b376d-151">exigido</span><span class="sxs-lookup"><span data-stu-id="b376d-151">required</span></span>  | <span data-ttu-id="b376d-152">N/D</span><span class="sxs-lookup"><span data-stu-id="b376d-152">N/A</span></span>           | <span data-ttu-id="b376d-153">N/D</span><span class="sxs-lookup"><span data-stu-id="b376d-153">N/A</span></span>                | <span data-ttu-id="b376d-154">exigido</span><span class="sxs-lookup"><span data-stu-id="b376d-154">required</span></span>       | <span data-ttu-id="b376d-155">exigido</span><span class="sxs-lookup"><span data-stu-id="b376d-155">required</span></span>             | <span data-ttu-id="b376d-156">opcionais</span><span class="sxs-lookup"><span data-stu-id="b376d-156">optional</span></span> | <span data-ttu-id="b376d-157">exigido</span><span class="sxs-lookup"><span data-stu-id="b376d-157">required</span></span>           |
| <span data-ttu-id="b376d-158">cor + alfa combinado</span><span class="sxs-lookup"><span data-stu-id="b376d-158">color + alpha combined</span></span>    | <span data-ttu-id="b376d-159">exigido</span><span class="sxs-lookup"><span data-stu-id="b376d-159">required</span></span>  | <span data-ttu-id="b376d-160">N/D</span><span class="sxs-lookup"><span data-stu-id="b376d-160">N/A</span></span>           | <span data-ttu-id="b376d-161">N/D</span><span class="sxs-lookup"><span data-stu-id="b376d-161">N/A</span></span>                | <span data-ttu-id="b376d-162">opcionais</span><span class="sxs-lookup"><span data-stu-id="b376d-162">optional</span></span>       | <span data-ttu-id="b376d-163">exigido</span><span class="sxs-lookup"><span data-stu-id="b376d-163">required</span></span>             | <span data-ttu-id="b376d-164">opcionais</span><span class="sxs-lookup"><span data-stu-id="b376d-164">optional</span></span> | <span data-ttu-id="b376d-165">exigido</span><span class="sxs-lookup"><span data-stu-id="b376d-165">required</span></span>           |
| <span data-ttu-id="b376d-166">cor e alfa separados</span><span class="sxs-lookup"><span data-stu-id="b376d-166">color and alpha separated</span></span> | <span data-ttu-id="b376d-167">exigido</span><span class="sxs-lookup"><span data-stu-id="b376d-167">required</span></span>  | <span data-ttu-id="b376d-168">exigido</span><span class="sxs-lookup"><span data-stu-id="b376d-168">required</span></span>      | <span data-ttu-id="b376d-169">opcionais</span><span class="sxs-lookup"><span data-stu-id="b376d-169">optional</span></span>           | <span data-ttu-id="b376d-170">N/D</span><span class="sxs-lookup"><span data-stu-id="b376d-170">N/A</span></span>            | <span data-ttu-id="b376d-171">exigido</span><span class="sxs-lookup"><span data-stu-id="b376d-171">required</span></span>             | <span data-ttu-id="b376d-172">N/D</span><span class="sxs-lookup"><span data-stu-id="b376d-172">N/A</span></span>      | <span data-ttu-id="b376d-173">exigido</span><span class="sxs-lookup"><span data-stu-id="b376d-173">required</span></span>           |



 

<span data-ttu-id="b376d-174">O BC7 define uma paleta de cores em uma linha aproximada entre dois pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="b376d-174">BC7 defines a palette of colors on an approximate line between two endpoints.</span></span> <span data-ttu-id="b376d-175">O valor de modo determina o número de pares de ponto de extremidade de interpolação por bloco.</span><span class="sxs-lookup"><span data-stu-id="b376d-175">The mode value determines the number of interpolating endpoint pairs per block.</span></span> <span data-ttu-id="b376d-176">O BC7 armazena um índice de paleta por texel.</span><span class="sxs-lookup"><span data-stu-id="b376d-176">BC7 stores one palette index per texel.</span></span>

<span data-ttu-id="b376d-177">Para cada subconjunto de índices que corresponde a um par de pontos de extremidade, o codificador corrige o estado de um bit dos dados de índice compactado para esse subconjunto.</span><span class="sxs-lookup"><span data-stu-id="b376d-177">For each subset of indices that corresponds to a pair of endpoints, the encoder fixes the state of one bit of the compressed index data for that subset.</span></span> <span data-ttu-id="b376d-178">Ele faz isso, escolhendo uma ordem de ponto de extremidade que permite que o índice do índice de "correção" designado defina o bit mais significativo como 0, e que pode então ser descartada, salvando um bit por subconjunto.</span><span class="sxs-lookup"><span data-stu-id="b376d-178">It does so by choosing an endpoint order that allows the index for the designated "fix-up" index to set its most significant bit to 0, and which can then be discarded, saving one bit per subset.</span></span> <span data-ttu-id="b376d-179">Para os modos de bloco com apenas um subconjunto único, o índice de correção será sempre o índice 0.</span><span class="sxs-lookup"><span data-stu-id="b376d-179">For block modes with only a single subset, the fix-up index is always index 0.</span></span>

## <a name="decoding-the-bc7-format"></a><span data-ttu-id="b376d-180">Decodificar o formato BC7</span><span class="sxs-lookup"><span data-stu-id="b376d-180">Decoding the BC7 Format</span></span>

<span data-ttu-id="b376d-181">O pseudocódigo a seguir mostra as etapas para descompactar o pixel em (x, y) que recebe o bloco de 16 bytes BC7</span><span class="sxs-lookup"><span data-stu-id="b376d-181">The following pseudocode outlines the steps to decompress the pixel at (x,y) given the 16 byte BC7 block.</span></span>

``` syntax
decompress_bc7(x, y, block)
{
    mode = extract_mode(block);
    
    //decode partition data from explicit partition bits
    subset_index = 0;
    num_subsets = 1;
    
    if (mode.type == 0 OR == 1 OR == 2 OR == 3 OR == 7)
    {
        num_subsets = get_num_subsets(mode.type);
        partition_set_id = extract_partition_set_id(mode, block);
        subset_index = get_partition_index(num_subsets, partition_set_id, x, y);
    }
    
    //extract raw, compressed endpoint bits
    UINT8 endpoint_array[num_subsets][4] = extract_endpoints(mode, block);
    
    //decode endpoint color and alpha for each subset
    fully_decode_endpoints(endpoint_array, mode, block);
    
    //endpoints are now complete.
    UINT8 endpoint_start[4] = endpoint_array[2 * subset_index];
    UINT8 endpoint_end[4]   = endpoint_array[2 * subset_index + 1];
        
    //Determine the palette index for this pixel
    alpha_index     = get_alpha_index(block, mode, x, y);
    alpha_bitcount  = get_alpha_bitcount(block, mode);
    color_index     = get_color_index(block, mode, x, y);
    color_bitcount  = get_color_bitcount(block, mode);

    //determine output
    UINT8 output[4];
    output.rgb = interpolate(endpoint_start.rgb, endpoint_end.rgb, color_index, color_bitcount);
    output.a   = interpolate(endpoint_start.a,   endpoint_end.a,   alpha_index, alpha_bitcount);
    
    if (mode.type == 4 OR == 5)
    {
        //Decode the 2 color rotation bits as follows:
        // 00 – Block format is Scalar(A) Vector(RGB) - no swapping
        // 01 – Block format is Scalar(R) Vector(AGB) - swap A and R
        // 10 – Block format is Scalar(G) Vector(RAB) - swap A and G
        // 11 - Block format is Scalar(B) Vector(RGA) - swap A and B
        rotation = extract_rot_bits(mode, block);
        output = swap_channels(output, rotation);
    }
    
}
```

<span data-ttu-id="b376d-182">O pseudocódigo a seguir descreve as etapas para decodificar totalmente os componentes de cor e alfa do ponto de extremidade para cada subconjunto dado um bloco de BC7 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="b376d-182">The followoing pseudocode outlines the steps to fully decode endpoint color and alpha components for each subset given a 16-byte BC7 block.</span></span>

``` syntax
fully_decode_endpoints(endpoint_array, mode, block)
{
    //first handle modes that have P-bits
    if (mode.type == 0 OR == 1 OR == 3 OR == 6 OR == 7)
    {
        for each endpoint i
        {
            //component-wise left-shift
            endpoint_array[i].rgba = endpoint_array[i].rgba << 1;
        }
        
        //if P-bit is shared
        if (mode.type == 1) 
        {
            pbit_zero = extract_pbit_zero(mode, block);
            pbit_one = extract_pbit_one(mode, block);
            
            //rgb component-wise insert pbits
            endpoint_array[0].rgb |= pbit_zero;
            endpoint_array[1].rgb |= pbit_zero;
            endpoint_array[2].rgb |= pbit_one;
            endpoint_array[3].rgb |= pbit_one;  
        }
        else //unique P-bit per endpoint
        {  
            pbit_array = extract_pbit_array(mode, block);
            for each endpoint i
            {
                endpoint_array[i].rgba |= pbit_array[i];
            }
        }
    }

    for each endpoint i
    {
        // Color_component_precision & alpha_component_precision includes pbit
        // left shift endpoint components so that their MSB lies in bit 7
        endpoint_array[i].rgb = endpoint_array[i].rgb << (8 - color_component_precision(mode));
        endpoint_array[i].a = endpoint_array[i].a << (8 - alpha_component_precision(mode));

        // Replicate each component's MSB into the LSBs revealed by the left-shift operation above
        endpoint_array[i].rgb = endpoint_array[i].rgb | (endpoint_array[i].rgb >> color_component_precision(mode));
        endpoint_array[i].a = endpoint_array[i].a | (endpoint_array[i].a >> alpha_component_precision(mode));
    }
        
    //If this mode does not explicitly define the alpha component
    //set alpha equal to 1.0
    if (mode.type == 0 OR == 1 OR == 2 OR == 3)
    {
        for each endpoint i
        {
            endpoint_array[i].a = 255; //i.e. alpha = 1.0f
        }
    }
}
```

<span data-ttu-id="b376d-183">Para gerar cada componente interpolado para cada subconjunto, use o seguinte algoritmo: deixe "c" ser o componente a ser gerado; deixe "e0" ser o componente de ponto de extremidade 0 do subconjunto; e deixe "e1" ser o componente de ponto de extremidade 1 do subconjunto.</span><span class="sxs-lookup"><span data-stu-id="b376d-183">To generate each interpolated component for each subset, use the following algorithm: let "c" be the component to generate; let "e0" be that component of endpoint 0 of the subset; and let "e1" be that component of endpoint 1 of the subset.</span></span>

``` syntax
UINT16 aWeight2[] = {0, 21, 43, 64};
UINT16 aWeight3[] = {0, 9, 18, 27, 37, 46, 55, 64};
UINT16 aWeight4[] = {0, 4, 9, 13, 17, 21, 26, 30, 34, 38, 43, 47, 51, 55, 60, 64};

UINT8 interpolate(UINT8 e0, UINT8 e1, UINT8 index, UINT8 indexprecision)
{
    if(indexprecision == 2)
        return (UINT8) (((64 - aWeights2[index])*UINT16(e0) + aWeights2[index]*UINT16(e1) + 32) >> 6);
    else if(indexprecision == 3)
        return (UINT8) (((64 - aWeights3[index])*UINT16(e0) + aWeights3[index]*UINT16(e1) + 32) >> 6);
    else // indexprecision == 4
        return (UINT8) (((64 - aWeights4[index])*UINT16(e0) + aWeights4[index]*UINT16(e1) + 32) >> 6);
}
```

<span data-ttu-id="b376d-184">O seguinte pseudocódigo ilustra como extrair índices e contagens de bit de componentes de cor e alfa.</span><span class="sxs-lookup"><span data-stu-id="b376d-184">The following pseudocode illustrates how to extract indices and bit counts for color and alpha components.</span></span> <span data-ttu-id="b376d-185">Os blocos com cor e alfa separados também têm dois conjuntos de dados de índice: um para o canal de vetor e outro para o canal escalar.</span><span class="sxs-lookup"><span data-stu-id="b376d-185">Blocks with separate color and alpha also have two sets of index data: one for the vector channel, and one for the scalar channel.</span></span> <span data-ttu-id="b376d-186">Para o modo de 4, esses índices são de larguras diferentes (2 ou 3 bits), e há um seletor de um bit que especifica se o vetor ou dados escalares usam os índices de 3 bits.</span><span class="sxs-lookup"><span data-stu-id="b376d-186">For Mode 4, these indices are of differing widths (2 or 3 bits), and there is a one-bit selector which specifies whether the vector or scalar data uses the 3-bit indices.</span></span> <span data-ttu-id="b376d-187">(A extração da contagem de bits alfa é semelhante à extração de contagem de bits de cor, mas com comportamento inverso com base no bit **idxMode**.)</span><span class="sxs-lookup"><span data-stu-id="b376d-187">(Extracting the alpha bit count is similar to extracting color bit count but with inverse behavior based on the **idxMode** bit.)</span></span>

``` syntax
bitcount get_color_bitcount(block, mode)
{
    if (mode.type == 0 OR == 1)
        return 3;
    
    if (mode.type == 2 OR == 3 OR == 5 OR == 7)
        return 2;
    
    if (mode.type == 6)
        return 4;
        
    //The only remaining case is Mode 4 with 1-bit index selector
    idxMode = extract_idxMode(block);
    if (idxMode == 0)
        return 2;
    else
        return 3;
}
```

## <a name="related-topics"></a><span data-ttu-id="b376d-188">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b376d-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b376d-189">Compactação de bloco de textura no Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="b376d-189">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 