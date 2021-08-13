---
title: Guia de programação para DDS
description: O Direct3D implementa o formato de arquivo DDS para armazenar texturas não compactadas ou compactadas (DXTn).
ms.assetid: 39f9847e-3b1c-4401-a253-74c183ffcc83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8fc1f8b9b84c2dc1f9236c79c320ae75848834ef2183db55b189f6b9d340d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796716"
---
# <a name="programming-guide-for-dds"></a>Guia de programação para DDS

O Direct3D implementa o formato de arquivo DDS para armazenar texturas não compactadas ou compactadas (DXTn). O formato de arquivo implementa vários tipos ligeiramente diferentes projetados para armazenar diferentes tipos de dados e dá suporte a texturas de camada única, texturas com mipmaps, mapas de cubo, mapas de volume e matrizes de textura (no Direct3D 10/11). Esta seção descreve o layout de um arquivo DDS.

Para obter ajuda para criar uma textura no Direct3D 11, consulte [como: criar uma textura](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create). Para obter ajuda no Direct3D 9, consulte [suporte a textura em D3DX (Direct3D 9)](/windows/desktop/direct3d9/texture-support-in-d3dx).

-   [Layout de arquivo DDS](#dds-file-layout)
-   [Variantes do DDS](#dds-variants)
-   [Usando matrizes de textura no Direct3D 10/11](#using-texture-arrays-in-direct3d-1011)
-   [Formatos de recursos de arquivo DDS comuns e conteúdo de cabeçalho associado](#common-dds-file-resource-formats-and-associated-header-content)
-   [Tópicos relacionados](#related-topics)

## <a name="dds-file-layout"></a>Layout de arquivo DDS

Um arquivo DDS é um arquivo binário que contém as seguintes informações:

-   Um DWORD (número mágico) contendo o valor de código com quatro caracteres 'DDS' (0x20534444).

-   Uma descrição dos dados no arquivo.

    Os dados são descritos com uma descrição de cabeçalho usando o [**\_ cabeçalho DDS**](dds-header.md); o formato de pixel é definido usando o [**DDS \_ PIXELFORMAT**](dds-pixelformat.md). Observe que as estruturas do **\_ cabeçalho DDS** e do **DDS \_ PIXELFORMAT** substituem as estruturas preteridas DDSURFACEDESC2, DDSCAPS2 e DDPIXELFORMAT DirectDraw 7. **DDS \_ HEADER** é o equivalente binário de DDSURFACEDESC2 e DDSCAPS2. **DDS \_ PIXELFORMAT** é o equivalente binário de DDPIXELFORMAT.

    ```
    DWORD               dwMagic;
    DDS_HEADER          header;
            
    ```

    

    Se o DDS \_ PIXELFORMAT dwFlags for definido como DDPF \_ FOURCC e dwFourCC estiver definido como "DX10", uma estrutura de [**\_ \_ DXT10 de cabeçalho DDS**](dds-header-dxt10.md) adicional estará presente para acomodar matrizes de textura ou formatos de dxgi que não podem ser expressos como um formato de pixel RGB, como formatos de ponto flutuante, formatos sRGB, etc. Quando a estrutura de **\_ \_ DXT10 de cabeçalho do DDS** estiver presente, a descrição completa dos dados será parecida com esta.

    ```
    DWORD               dwMagic;
    DDS_HEADER          header;
    DDS_HEADER_DXT10    header10;
    ```

    

-   Um ponteiro para uma matriz de bytes que contém os dados da superfície principal.
    ```
    BYTE bdata[]
    ```

    

-   Um ponteiro para uma matriz de bytes que contém as demais superfícies; por exemplo, níveis de minimapa, faces de um mapa de cubos, profundidades em uma textura de volume. Siga estes links para saber mais sobre o layout de arquivo DDS para: uma [textura](dds-file-layout-for-textures.md), um [mapa de cubos](dds-file-layout-for-cubic-environment-maps.md) ou uma [textura de volume](dds-file-layout-for-volume-textures.md).

    ```
    BYTE bdata2[]
    ```

    

Para obter amplo suporte a hardware, é recomendável que você use o [**\_ formato dxgi \_ R8G8B8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), o [**\_ formato dxgi \_ R8G8B8A8 \_ UNORM \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), o [**\_ formato dxgi \_ R8G8B8A8 \_ SNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), o [**\_ formato dxgi \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), o [**\_ formato dxgi \_ R16G16 \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)SNORM, o [**\_ formato dxgi \_ R8G8 \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)SNORM, o formato dxgi UNORM, o formato dxgi BC1 UNORM, o formato dxgi BC1 UNORM, ou o formato dxgi BC2 UNORM, formato [**\_ \_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**dxgi \_ \_ BC2 \_ UNORM \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format). [**\_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**\_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**\_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**\_ \_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**\_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Para obter mais informações sobre formatos de textura compactados, consulte [compactação de bloco de textura no Direct3D 11](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11) e [compactação de bloco (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression).

A biblioteca D3DX (por exemplo, D3DX11. lib) e outras bibliotecas semelhantes fornecem o valor de pitch no membro **dwPitchOrLinearSize** da estrutura do [**\_ cabeçalho DDS**](dds-header.md) . Portanto, ao ler e gravar em arquivos DDS, recomendamos que você calcule o timbre de uma das seguintes maneiras para os formatos Indicados:

-   Para formatos compactados em bloco, calcule a inclinação como:

    Max (1, ((largura + 3)/4)) \* tamanho do bloco

    O tamanho do bloco é de 8 bytes para os formatos DXT1, BC1 e BC4 e 16 bytes para outros formatos compactados por bloco.

-   Para \_ os formatos R8G8 B8G8, G8R8 \_ G8B8, Legacy UYVY e Legacy YUY2, computar a inclinação como:

    ((largura + 1)  >> 1) \* quatro

-   Para outros formatos, calcule a inclinação como:

    ( \* bits de largura por pixel + 7)/8

    Você divide por 8 para o alinhamento de bytes.

> [!Note]  
> O valor de pitch que você calcula nem sempre é igual ao que o tempo de execução fornece, que é alinhado por DWORD em algumas situações e alinhado por byte em outras situações. Portanto, recomendamos que você copie uma linha de verificação por vez, em vez de tentar copiar toda a imagem em uma cópia.

 

## <a name="dds-variants"></a>Variantes do DDS

Há muitas ferramentas que criam e consomem arquivos DDS, mas podem variar nos detalhes do que precisam no cabeçalho. Os gravadores devem preencher os cabeçalhos o mais totalmente possível e os leitores devem verificar os valores mínimos para obter a compatibilidade máxima. Para validar um arquivo DDS, um leitor deve garantir que o arquivo tenha pelo menos 128 bytes de comprimento para acomodar o valor mágico e o cabeçalho básico, o valor mágico é 0x20534444 ("DDS"), o \_ tamanho do cabeçalho DDS é 124 e o PIXELFORMAT do DDS \_ no tamanho do cabeçalho é 32. Se o DDS \_ PIXELFORMAT dwFlags for definido como DDPF \_ FOURCC e um dwFourCC for definido como "DX10", o tamanho total do arquivo precisará ter pelo menos 148 bytes.

Há algumas variantes comuns em uso em que o formato de pixel é definido como um \_ código FOURCC DDPF, em que dwFourCC é definido como um valor de enumeração de formato D3DFORMAT ou dxgi \_ . Não há como saber se um valor de enumeração é um formato D3DFORMAT ou DXGI \_ , portanto, é altamente recomendável que a extensão "DX10" e o \_ cabeçalho DXT10 de cabeçalho DDS \_ sejam usados para armazenar o dxgiFormat quando o PIXELFORMAT básico do DDS \_ não puder expressar o formato.

A PIXELFORMAT padrão DDS \_ deve ser preferida para compatibilidade máxima para armazenar dados não compactados em RGB e dados DXT1-5, pois nem todas as ferramentas DDS dão suporte à extensão DX10.

## <a name="using-texture-arrays-in-direct3d-1011"></a>Usando matrizes de textura no Direct3D 10/11

As novas estruturas DDS ([**\_ cabeçalho DDS**](dds-header.md) e [**\_ \_ DXT10 de cabeçalho DDS**](dds-header-dxt10.md)) no Direct3D 10/11 estendem o formato de arquivo DDS para dar suporte a uma matriz de texturas, que é um novo tipo de recurso no Direct3D 10/11. Aqui está um código de exemplo que mostra como acessar os diferentes níveis de mipmap em uma matriz de texturas, usando os novos cabeçalhos.


```
DWORD               dwMagic;
DDS_HEADER          header;
DDS_HEADER_DXT10    header10;
   
for (int iArrayElement = 0; iArrayElement < header10.arraySize; iArrayElement++)
{
   for (int iMipLevel = 0; iMipLevel < header.dwMipMapCount; iMipLevel++)
   {
     ...
   }
}       
```



## <a name="common-dds-file-resource-formats-and-associated-header-content"></a>Formatos de recursos de arquivo DDS comuns e conteúdo de cabeçalho associado



| Formato de recurso                                                                            | dwFlags        | dwRGBBitCount | dwRBitMask | dwGBitMask | dwBBitMask | dwABitMask |
|--------------------------------------------------------------------------------------------|----------------|---------------|------------|------------|------------|------------|
| \_Formato dxgi \_ R8G8B8A8 \_ UNORM<br/> D3DFMT \_ A8B8G8R8<br/>                       | o DDS \_ RGBA      | 32            | 0xFF       | 0xff00     | 0xff0000   | 0xff000000 |
| \_Formato dxgi \_ R16G16 \_ UNORM<br/> D3DFMT \_ G16R16<br/>                           | o DDS \_ RGBA      | 32            | 0xFFFF     | 0xffff0000 |            |            |
| \*\*<br/> \_Formato dxgi \_ R10G10B10A2 \_ UNORM<br/> D3DFMT \_ A2B10G10R10<br/> | o DDS \_ RGBA      | 32            | 0x3ff      | 0xffc00    | 0x3ff00000 |            |
| \_Formato dxgi \_ R16G16 \_ UNORM<br/> D3DFMT \_ G16R16<br/>                           | DDS \_ RGB       | 32            | 0xFFFF     | 0xffff0000 |            |            |
| \_Formato dxgi \_ B5G5R5A1 \_ UNORM<br/> D3DFMT \_ A1R5G5B5<br/>                       | o DDS \_ RGBA      | 16            | 0x7c00     | 0x3e0      | 0x1F       | 0x8000     |
| \_Formato dxgi \_ B5G6R5 \_ UNORM<br/> D3FMT \_ R5G6B5<br/>                            | DDS \_ RGB       | 16            | 0xf800     | 0x7e0      | 0x1F       |            |
| \_UNORM A8-dxgi \_<br/> D3DFMT \_ a8<br/>                                           | DDS \_ Alpha     | 8             |            |            |            | 0xFF       |
| D3DFMT \_ A8R8G8B8<br/>                                                                | o DDS \_ RGBA      | 32            | 0xff0000   | 0xff00     | 0xFF       | 0xff000000 |
| D3DFMT \_ X8R8G8B8<br/>                                                                | DDS \_ RGB       | 32            | 0xff0000   | 0xff00     | 0xFF       |            |
| D3DFMT \_ X8B8G8R8<br/>                                                                | DDS \_ RGB       | 32            | 0xFF       | 0xff00     | 0xff0000   |            |
| \*\*<br/> D3DFMT \_ A2R10G10B10<br/>                                             | o DDS \_ RGBA      | 32            | 0x3ff00000 | 0xffc00    | 0x3ff      | 0xc0000000 |
| D3DFMT \_ R8G8B8<br/>                                                                  | DDS \_ RGB       | 24            | 0xff0000   | 0xff00     | 0xFF       |            |
| D3DFMT \_ X1R5G5B5<br/>                                                                | DDS \_ RGB       | 16            | 0x7c00     | 0x3e0      | 0x1F       |            |
| D3DFMT \_ A4R4G4B4<br/>                                                                | o DDS \_ RGBA      | 16            | 0xf00      | 0xf0       | 0xf        | 0xf000     |
| D3DFMT \_ X4R4G4B4<br/>                                                                | DDS \_ RGB       | 16            | 0xf00      | 0xf0       | 0xf        |            |
| D3DFMT \_ A8R3G3B2<br/>                                                                | o DDS \_ RGBA      | 16            | 0xe0       | 0x1c       | 0x3        | 0xff00     |
| D3DFMT \_ A8L8<br/>                                                                    | luminância de DDS \_ | 16            | 0xFF       |            |            | 0xff00     |
| D3DFMT \_ L16<br/>                                                                     | luminância de DDS \_ | 16            | 0xFFFF     |            |            |            |
| \_L8 D3DFMT<br/>                                                                      | luminância de DDS \_ | 8             | 0xFF       |            |            |            |
| D3DFMT \_ A4L4<br/>                                                                    | luminância de DDS \_ | 8             | 0xf        |            |            | 0xf0       |



 



| Formato de recurso                                                                             | dwFlags     | dwFourCC |
|---------------------------------------------------------------------------------------------|-------------|----------|
| \_Formato dxgi \_ BC1 \_ UNORM<br/> D3DFMT \_ DXT1<br/>                                 | um DDS \_ FOURCC | "DXT1"   |
| \_Formato dxgi \_ BC2 \_ UNORM<br/> D3DFMT \_ DXT3<br/>                                 | um DDS \_ FOURCC | "DXT3"   |
| \_Formato dxgi \_ BC3 \_ UNORM<br/> D3DFMT \_ DXT5<br/>                                 | um DDS \_ FOURCC | "DXT5"   |
| \*<br/> \_Formato dxgi \_ BC4 \_ UNORM<br/>                                           | um DDS \_ FOURCC | "BC4U"   |
| \*<br/> \_Formato dxgi \_ BC4 \_ SNORM<br/>                                           | DDS \_ FOURCC | "BC4S"   |
| \*<br/> FORMATO DXGI \_ \_ BC5 \_ UNORM<br/>                                           | DDS \_ FOURCC | "ATI2"   |
| \*<br/> FORMATO DXGI \_ \_ BC5 \_ SNORM<br/>                                           | DDS \_ FOURCC | "BC5S"   |
| DXGI \_ FORMAT \_ R8G8 \_ B8G8 \_ UNORM<br/> D3DFMT \_ R8G8 \_ B8G8<br/>                    | DDS \_ FOURCC | "RGBG"   |
| DXGI \_ FORMAT \_ G8R8 \_ G8B8 \_ UNORM<br/> D3DFMT \_ G8R8 \_ G8B8<br/>                    | DDS \_ FOURCC | "GRGB"   |
| \*<br/> DXGI \_ FORMAT \_ R16G16B16A16 \_ UNORM<br/> D3DFMT \_ A16B16G16R16<br/>  | DDS \_ FOURCC | 36       |
| \*<br/> FORMATO DXGI \_ \_ R16G16B16A16 \_ SNORM<br/> D3DFMT \_ Q16W16V16U16<br/>  | DDS \_ FOURCC | 110      |
| \*<br/> DXGI \_ FORMAT \_ R16 \_ FLOAT<br/> D3DFMT \_ R16F<br/>                   | DDS \_ FOURCC | 111      |
| \*<br/> DXGI \_ FORMAT \_ R16G16 \_ FLOAT<br/> D3DFMT \_ G16R16F<br/>             | DDS \_ FOURCC | 112      |
| \*<br/> DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT<br/> D3DFMT \_ A16B16G16R16F<br/> | DDS \_ FOURCC | 113      |
| \*<br/> DXGI \_ FORMAT \_ R32 \_ FLOAT<br/> D3DFMT \_ R32F<br/>                   | DDS \_ FOURCC | 114      |
| \*<br/> DXGI \_ FORMAT \_ R32G32 \_ FLOAT<br/> D3DFMT \_ G32R32F<br/>             | DDS \_ FOURCC | 115      |
| \*<br/> DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT<br/> D3DFMT \_ A32B32G32R32F<br/> | DDS \_ FOURCC | 116      |
| D3DFMT \_ DXT2<br/>                                                                     | DDS \_ FOURCC | "DXT2"   |
| D3DFMT \_ DXT4<br/>                                                                     | DDS \_ FOURCC | "DXT4"   |
| D3DFMT \_ UYVY<br/>                                                                     | DDS \_ FOURCC | "UYVY"   |
| D3DFMT \_ YUY2<br/>                                                                     | DDS \_ FOURCC | "YUY2"   |
| D3DFMT \_ CxV8U8<br/>                                                                   | DDS \_ FOURCC | 117      |
| Qualquer formato DXGI                                                                             | DDS \_ FOURCC | "DX10"   |



 

\* = Um leitor de DDS robusto deve ser capaz de lidar com esses códigos de formato herdados. No entanto, esse leitor de DDS deve preferir usar a extensão de header "DX10" ao escrever esses códigos de formato para evitar ambiguidade.

\*\* = Devido a alguns problemas de longa duração em implementações comuns de leitores e autores DDS, a maneira mais robusta de gravar dados de tipo 10:10:10:2 é usar a extensão de header "DX10" com o código [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) "24" (ou seja, o valor DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM). Os dados D3DFMT \_ A2R10G10B10 devem ser convertidos em dados de tipo 10:10:10:2 antes de serem gravados como um arquivo DDS de formato \_ \_ DXGI FORMAT R10G10B10A2 \_ UNORM.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dds](dx-graphics-dds.md)
</dt> </dl>

 

