---
title: Compactação de bloco de textura no Direct3D 11
description: O suporte para texturas de compactação de bloco (BC) foi estendido no Direct3D 11 para incluir os algoritmos de BC6H e BC7.
ms.assetid: E0735D4E-9C0F-45DC-854A-C27EB8367D86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52c2c764c0f9dca4021dcb14187db67e697cd7155701294a9c6214b4543d00b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027796"
---
# <a name="texture-block-compression-in-direct3d-11"></a>Compactação de bloco de textura no Direct3D 11

O suporte para texturas de compactação de bloco (BC) foi estendido no Direct3D 11 para incluir os algoritmos de BC6H e BC7. O BC6H dá suporte a dados de origem de cor de intervalo altamente dinâmico e o BC7 fornece compactação de qualidade melhor que a média com menos artefatos para dados de origem RGB padrão.

Para obter informações mais específicas sobre o suporte do algoritmo de compactação de bloco antes do Direct3D 11, incluindo o suporte para os formatos BC1 a BC5, consulte [Compactação de bloco (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression).

**Observação sobre formatos de arquivo:** Os formatos de compactação de textura BC6H e BC7 usam o formato de arquivo DDS para armazenar os dados de textura compactados. Para obter mais informações, consulte o [Guia de programação para DDS](/windows/desktop/direct3ddds/dx-graphics-dds-pguide) para obter detalhes.

## <a name="block-compression-formats-supported-in-direct3d-11"></a>Formatos de compactação de bloco com suporte no Direct3D 11



| Dados de origem                                  | Resolução de compactação de dados mínima necessária                              | Formato recomendado | Nível mínimo de recursos com suporte |
|----------------------------------------------|---------------------------------------------------------------------------|--------------------|---------------------------------|
| Cor de três canais com canal alfa       | Três canais de cores (5 bits:6 bits:5 bits), com 0 ou 1 bit de alfa  | BC1                | Direct3D 9.1                    |
| Cor de três canais com canal alfa       | Três canais de cores (5 bits:6 bits:5 bits), com 4 bits de alfa         | BC2                | Direct3D 9.1                    |
| Cor de três canais com canal alfa       | Três canais de cores (5 bits:6 bits:5 bits) com 8 bits de alfa          | BC3                | Direct3D 9.1                    |
| Cor de um canal                            | Um canal de cor (8 bits)                                                | BC4                | Direct3D 10                     |
| Cor de dois canais                            | Dois canais de cores (8 bits:8 bits)                                        | BC5                | Direct3D 10                     |
| Cor de alto alcance dinâmico (HDR) de três canais | Três canais de cores (16 bits:16 bits:16 bits) no ponto flutuante "metade"\* | BC6H               | Direct3D 11                     |
| Cor de três canais, canal alfa opcional  | Três canais de cores (4 a 7 bits por canal) com 0 a 8 bits de alfa  | BC7                | Direct3D 11                     |



 

\*O ponto flutuante "Half" é um valor de 16 bits que consiste em um bit de sinal opcional, um expoente com desvio de 5 bits e uma mantissa de 10 ou 11 bits.

## <a name="bc1-bc2-and-b3-formats"></a>Formatos BC1, BC2 e B3

Os formatos BC1, BC2 e BC3 são equivalentes aos formatos de compactação de textura 9 DXTn do Direct3D e são iguais aos formatos BC1, BC2 e BC3 correspondentes do Direct3D 10. O suporte para esses três formatos é necessário para todos os níveis de recurso (D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1, D3D \_ FEATURE LEVEL \_ \_ 9 \_ 2, \_ D3D FEATURE LEVEL \_ \_ \_ 9 3, D3D \_ FEATURE LEVEL \_ \_ 10 \_ 0, D3D \_ FEATURE LEVEL \_ \_ 10 1 e \_ D3D \_ FEATURE LEVEL \_ \_ 11 \_ 0).



| Formato de compactação de bloco | Formato DXGI                                                                           | Formato equivalente do Direct3D 9                               | Bytes por bloco de pixels 4x4 |
|--------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------|---------------------------|
| BC1                      | FORMATO DXGI \_ \_ BC1 \_ UNORM, FORMATO DXGI \_ \_ BC1 \_ UNORM \_ SRGB, FORMATO DXGI \_ \_ BC1 \_ SEM TIPO | D3DFMT \_ DXT1, FourCC="DXT1"                                | 8                         |
| BC2                      | FORMATO DXGI \_ \_ BC2 \_ UNORM, FORMATO DXGI \_ \_ BC2 \_ UNORM \_ SRGB, FORMATO DXGI \_ \_ BC2 \_ SEM TIPO | D3DFMT \_ DXT2 \* , FourCC="DXT2", D3DFMT \_ DXT3, FourCC="DXT3" | 16                        |
| BC3                      | FORMATO DXGI \_ \_ BC3 \_ UNORM, FORMATO DXGI \_ \_ BC3 \_ UNORM \_ SRGB, FORMATO DXGI \_ \_ BC3 \_ SEM TIPO | D3DFMT \_ DXT4 \* , FourCC="DXT4", D3DFMT \_ DXT5, FourCC="DXT5" | 16                        |



 

\*Esses esquemas de compactação (DXT2 e DXT4) não fazem distinção entre os formatos alfa pré-multiplicados do Direct3D 9 e os formatos alfa padrão. Essa distinção deve ser processada pelos sombreadores programáveis no momento da renderização.

## <a name="bc4-and-bc5-formats"></a>Formatos BC4 e BC5



| Formato de compactação de bloco | Formato DXGI                                                                     | Formato equivalente do Direct3D 9 | Bytes por bloco de pixels 4x4 |
|--------------------------|---------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC4                      | FORMATO DXGI \_ \_ BC4 \_ UNORM, FORMATO DXGI \_ \_ BC4 \_ SNORM, FORMATO DXGI \_ \_ BC4 \_ SEM TIPO | FourCC="ATI1"                | 8                         |
| BC5                      | FORMATO DXGI \_ \_ BC5 \_ UNORM, FORMATO DXGI \_ \_ BC5 \_ SNORM, FORMATO DXGI \_ \_ BC5 \_ SEM TIPO | FourCC="ATI2"                | 16                        |



 

## <a name="bc6h-format"></a>Formato BC6H

Para obter mais informações sobre esse formato, consulte a documentação do [formato BC6H](bc6h-format.md).



| Formato de compactação de bloco | Formato DXGI                                                                      | Formato equivalente do Direct3D 9 | Bytes por bloco de pixels 4x4 |
|--------------------------|----------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC6H                     | FORMATO DXGI \_ \_ BC6H \_ UF16, FORMATO DXGI \_ \_ BC6H \_ SF16, FORMATO DXGI \_ \_ BC6H \_ SEM TIPO | N/D                          | 16                        |



 

O formato BC6H pode selecionar diferentes modos de codificação para cada bloco de pixels 4x4. Um total de 14 modos de codificação diferentes estão disponíveis, cada um com compensações ligeiramente diferentes na qualidade visual resultante da textura exibida. A escolha dos modos permite a decodificação rápida pelo hardware com o nível de qualidade selecionado ou adaptado de acordo com o conteúdo de origem, mas também aumenta a complexidade do espaço de pesquisa.

## <a name="bc7-format"></a>Formato BC7

Para obter mais informações sobre esse formato, consulte a documentação do [formato BC7](bc7-format.md).



| Formato de compactação de bloco | Formato DXGI                                                                           | Formato equivalente do Direct3D 9 | Bytes por bloco de pixels 4x4 |
|--------------------------|---------------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC7                      | FORMATO DXGI \_ \_ BC7 \_ UNORM, FORMATO DXGI \_ \_ BC7 \_ UNORM \_ SRGB, FORMATO DXGI \_ \_ BC7 \_ SEM TIPO | N/D                          | 16                        |



 

O formato BC7 pode selecionar diferentes modos de codificação para cada bloco de pixels 4x4. Um total de 8 modos de codificação diferentes estão disponíveis, cada um com compensações ligeiramente diferentes na qualidade visual resultante da textura exibida. A escolha dos modos permite a decodificação rápida pelo hardware com o nível de qualidade selecionado ou adaptado de acordo com o conteúdo de origem, mas também aumenta a complexidade do espaço de pesquisa.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                 | Descrição                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Formato BC6H](bc6h-format.md)<br/>                             | O formato BC6H é um formato de compactação de textura projetado para dar suporte a espaços de cores de intervalo altamente dinâmico (HDR) nos dados de origem.<br/> |
| [Formato BC7](bc7-format.md)<br/>                               | O formato BC7 é um formato de compactação de textura usado para compactação de alta qualidade de dados de RGB e RGBA.<br/>                    |
| [Referência do modo de formato BC7](bc7-format-mode-reference.md)<br/> | Esta documentação contém uma lista de 8 modos de bloqueio e alocações de bits para blocos de formato de compactação de textura BC7.<br/>    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Compactação de bloco (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)
</dt> <dt>

[Texturas](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

