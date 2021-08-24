---
title: Formato BC7
description: O formato BC7 é um formato de compactação de textura usado para compactação de alta qualidade de dados de RGB e RGBA.
ms.assetid: DF333106-293E-4B3E-A1EB-B0BF0ADBAC72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bd48826cc0c02be6d15a837c272442c0931e9660f507a90cb491acf4d5820ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858216"
---
# <a name="bc7-format"></a>Formato BC7

O formato BC7 é um formato de compactação de textura usado para compactação de alta qualidade de dados de RGB e RGBA.

-   [Sobre BC7/DXGI \_ FORMAT \_ BC7](/windows)
-   [Implementação bc7](#bc7-implementation)
-   [Decodificação do formato BC7](#decoding-the-bc7-format)
-   [Tópicos relacionados](#related-topics)

Para obter informações sobre os modos de bloco do formato BC7, consulte [Referência do Modo de Formato BC7](bc7-format-mode-reference.md).

## <a name="about-bc7dxgi_format_bc7"></a>Sobre BC7/DXGI \_ FORMAT \_ BC7

BC7 é especificado pelos seguintes valores de enumeração DXGI \_ FORMAT:

-   **DXGI \_ FORMAT \_ BC7 \_ TYPELESS**.
-   **DXGI \_ FORMATAR \_ BC7 \_ UNORM**.
-   **DXGI \_ FORMAT \_ BC7 \_ UNORM \_ SRGB**.

O formato BC7 pode ser usado para o recursos de textura [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (incluindo matrizes), Texture3D ou TextureCube (incluindo matrizes). Da mesma forma, esse formato se aplica a qualquer superfície de MIP-map associada a esses recursos.

O BC7 usa um tamanho de bloco fixo de 16 bytes (128 bits) e um tamanho de bloco fixo de 4 x 4 texels. Como com os formatos BC anteriores, as imagens de textura maiores que o tamanho de bloco com suporte (4 x 4) são compactadas usando vários blocos. Essa identidade endereçamento se aplica também a imagens tridimensionais, mapas MIP, mapas de cubo e matrizes de textura. Todos os blocos de imagem devem ser do mesmo formato.

O BC7 compacta imagens de dados de ponto fixo de três canais (RGB) e quatro canais (RGBA). Normalmente, os dados de origem tem 8 bits por componente de cor (canal), embora o formato seja capaz de codificar dados de origem com maior quantidade de bits por componente de cor. Todos os blocos de imagem devem ser do mesmo formato.

O decodificador BC7 executa descompactação antes da filtragem de textura ser aplicada.

O hardware de descompactação BC7 deve ter precisão de bit, ou seja, o hardware deve retornar resultados que são idênticos aos resultados retornados pelo decodificador descrito neste documento.

## <a name="bc7-implementation"></a>Implementação do BC7

Uma implementação de BC7 pode especificar um dos 8 modos, com o modo especificado no bit menos significativo do bloco de 16 bytes (128 bits). O modo é codificado por zero ou mais bits com um valor de 0 seguido por um 1.

Um bloco BC7 pode conter vários pares de ponto de extremidade. Para os fins desta documentação, o conjunto de índices que correspondem a um par de pontos de extremidade pode ser chamado de "subconjunto". Além disso, em alguns modos de bloco, a representação de ponto de extremidade é codificada em uma forma que, novamente, para os fins desta documentação, deve ser conhecida como "RBGP", em que o bit "P" representa um bit menos significativo compartilhado para os componentes de cor do ponto de extremidade. Por exemplo, se a representação de ponto de extremidade para o formato for "RGB 5.5.5.1", então o ponto de extremidade é interpretado como um valor RGB 6.6.6, onde o estado do bit P define o bit menos significativo de cada componente. Da mesma forma, para dados de origem com um canal alfa, se a representação para o formato for "RGBAP 5.5.5.5.1", o ponto de extremidade será intercalado como RGBA 6.6.6.6. Dependendo do modo de bloco, você pode especificar o bit menos significativo compartilhado para um ambos os pontos de extremidade de um subconjunto individualmente (2 bits P por subconjunto), ou compartilhados entre os pontos de extremidade de um subconjunto (1 bit P por subconjunto).

Para os blocos de BC7 que não codificam explicitamente o componente alfa, um bloco BC7 consiste em bits de modo, bits de partição, pontos de extremidade compactados, índices compactados e um bit P opcional. Nesses blocos, os pontos de extremidade têm uma representação somente RGB e o componente alfa é decodificado como 1.0 para todos os texels nos dados de origem.

Para os blocos de BC7 que tem componentes de cor e alfa combinados, um bloco consiste em bits de modo, pontos de extremidade compactados, índices compactados, bits de partição opcionais e um bit P. Nesses blocos, as cores de ponto de extremidade são expressas em formato RGBA e os valores de componente alfa são interpolados junto com os valores de componente de cor.

Para os blocos BC7 que têm componentes de cor e alfa separados, um bloco consiste em bits de modo, bits de rotação, pontos de extremidade compactados, índices compactados, e um bit seletor de índice opcional. Esses blocos têm um vetor RGB efetivo R, G, B e um canal \[ alfa escalar A codificado \] \[ \] separadamente.

A tabela a seguir lista os componentes de cada tipo de bloco.



| O bloco BC7 contém...     | bits de modo | bits de rotação | bits de seletor de índice | bits de partição | pontos de extremidade compactados | bit P    | índices compactados |
|---------------------------|-----------|---------------|--------------------|----------------|----------------------|----------|--------------------|
| somente os componentes de cor     | exigido  | N/D           | N/D                | exigido       | exigido             | opcionais | exigido           |
| cor + alfa combinado    | exigido  | N/D           | N/D                | opcionais       | exigido             | opcionais | exigido           |
| cor e alfa separados | exigido  | exigido      | opcionais           | N/D            | exigido             | N/D      | exigido           |



 

O BC7 define uma paleta de cores em uma linha aproximada entre dois pontos de extremidade. O valor de modo determina o número de pares de ponto de extremidade de interpolação por bloco. O BC7 armazena um índice de paleta por texel.

Para cada subconjunto de índices que corresponde a um par de pontos de extremidade, o codificador corrige o estado de um bit dos dados de índice compactado para esse subconjunto. Ele faz isso, escolhendo uma ordem de ponto de extremidade que permite que o índice do índice de "correção" designado defina o bit mais significativo como 0, e que pode então ser descartada, salvando um bit por subconjunto. Para os modos de bloco com apenas um subconjunto único, o índice de correção será sempre o índice 0.

## <a name="decoding-the-bc7-format"></a>Decodificar o formato BC7

O pseudocódigo a seguir mostra as etapas para descompactar o pixel em (x, y) que recebe o bloco de 16 bytes BC7

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

O pseudocódigo a seguir descreve as etapas para decodificar totalmente os componentes de cor e alfa do ponto de extremidade para cada subconjunto dado um bloco de BC7 16 bytes.

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

Para gerar cada componente interpolado para cada subconjunto, use o seguinte algoritmo: deixe "c" ser o componente a ser gerado; deixe "e0" ser o componente de ponto de extremidade 0 do subconjunto; e deixe "e1" ser o componente de ponto de extremidade 1 do subconjunto.

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

O seguinte pseudocódigo ilustra como extrair índices e contagens de bit de componentes de cor e alfa. Os blocos com cor e alfa separados também têm dois conjuntos de dados de índice: um para o canal de vetor e outro para o canal escalar. Para o modo de 4, esses índices são de larguras diferentes (2 ou 3 bits), e há um seletor de um bit que especifica se o vetor ou dados escalares usam os índices de 3 bits. (A extração da contagem de bits alfa é semelhante à extração de contagem de bits de cor, mas com comportamento inverso com base no bit **idxMode**.)

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

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Compactação de bloco de textura no Direct3D 11](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 