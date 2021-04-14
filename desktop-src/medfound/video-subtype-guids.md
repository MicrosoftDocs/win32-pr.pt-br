---
description: Os GUIDs de subtipo de vídeo a seguir são definidos no arquivo de cabeçalho mfapi. h. Para especificar o subtipo, defina o \_ atributo de \_ subtipo MF MT no tipo de mídia.
ms.assetid: 7dfd85e6-936e-4b78-a2cb-a5d59153e1c4
title: GUIDs de subtipo de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38829480aed7372496fc196cc6c55d781b672a2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505695"
---
# <a name="video-subtype-guids"></a>GUIDs de subtipo de vídeo

Os GUIDs de subtipo de vídeo a seguir são definidos no arquivo de cabeçalho mfapi. h. Para especificar o subtipo, defina o atributo de [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md) no tipo de mídia.

Quando esses subtipos forem usados, defina o atributo de [ \_ \_ \_ tipo principal MF MT](mf-mt-major-type-attribute.md) como **\_ vídeo MFMediaType**.

-   [Formatos RGB não compactados](#uncompressed-rgb-formats)
-   [Formatos YUV: 8 bits e palettized](#yuv-formats-8-bit-and-palettized)
-   [Formatos YUV: de 10 bits e de 16 bits](#yuv-formats-10-bit-and-16-bit)
-   [Formatos de luminância e profundidade](#luminance-and-depth-formats)
-   [Tipos de vídeo codificados](#encoded-video-types)
-   [Criando GUIDs de subtipo de valores FOURCC e D3DFORMAT](#creating-subtype-guids-from-fourccs-and-d3dformat-values)
-   [Tópicos relacionados](#related-topics)

## <a name="uncompressed-rgb-formats"></a>Formatos RGB não compactados



| GUID                             | Descrição                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------|
| **MFVideoFormat \_ RGB8**          | RGB, 8 bits por pixel (BPP). (Mesmo layout de memória do **D3DFMT \_ P8**.)                            |
| **MFVideoFormat \_ RGB555**        | RGB 555, 16 BPP. (Mesmo layout de memória que **D3DFMT \_ X1R5G5B5**.)                                  |
| **MFVideoFormat \_ RGB565**        | RGB 565, 16 BPP. (Mesmo layout de memória que **D3DFMT \_ R5G6B5**.)                                    |
| **MFVideoFormat \_ RGB24**         | RGB, 24 bpp.                                                                                    |
| **MFVideoFormat \_ RGB32**         | RGB, 32 bpp.                                                                                    |
| **MFVideoFormat \_ ARGB32**        | RGB, 32 bpp com canal alfa.                                                                 |
| **MFVideoFormat \_ A2R10G10B10**   | RGB, 10 bpp para cada cor e 2 bpp para alfa. (Mesmo layout de memória que **D3DFMT \_ A2B10G10R10**) |
| **MFVideoFormat \_ A16B16G16R16F** | RGB, 16 bpp com canal alfa. (Mesmo layout de memória que **D3DFMT \_ A16B16G16R16F**)               |



 

> [!Note]  
> Esses subtipos não correspondem aos GUIDs de subtipo RGB usados em SDKs anteriores, como o DirectShow.

 

## <a name="yuv-formats-8-bit-and-palettized"></a>Formatos YUV: 8 bits e palettized



| GUID                    | Formatar | amostragem | Embalado ou planar | Bits por canal |
|-------------------------|--------|----------|------------------|------------------|
| **MFVideoFormat \_ AI44** | AI44   | 4:4:4    | Colocado           | Palettized       |
| **MFVideoFormat \_ AYUV** | AYUV   | 4:4:4    | Colocado           | 8                |
| **MFVideoFormat \_ I420** | I420   | 4:2:0    | Planar           | 8                |
| **MFVideoFormat \_ IYUV** | IYUV   | 4:2:0    | Planar           | 8                |
| **MFVideoFormat \_ NV11** | NV11   | 4:1:1    | Planar           | 8                |
| **MFVideoFormat \_ NV12** | NV12   | 4:2:0    | Planar           | 8                |
| **MFVideoFormat \_ UYVY** | UYVY   | 4:2:2    | Colocado           | 8                |
| **MFVideoFormat \_ Y41P** | Y41P   | 4:1:1    | Colocado           | 8                |
| **MFVideoFormat \_ Y41T** | Y41T   | 4:1:1    | Colocado           | 8                |
| **MFVideoFormat \_ Y42T** | Y42T   | 4:2:2    | Colocado           | 8                |
| **MFVideoFormat \_ YUY2** | YUY2   | 4:2:2    | Colocado           | 8                |
| **MFVideoFormat \_ YVU9** | YVU9   | 8:4:4    | Planar           | 9                |
| **MFVideoFormat \_ YV12** | YV12   | 4:2:0    | Planar           | 8                |
| **MFVideoFormat \_ YVYU** | YVYU   | 4:2:2    | Colocado           | 8                |



 

Os formatos YUV recomendados são descritos em detalhes no tópico [formatos de YUV de 8 bits recomendados para renderização de vídeo](recommended-8-bit-yuv-formats-for-video-rendering.md).

> [!Note]  
> I420 e IYUV têm o mesmo layout na memória, mas são atribuídos GUIDs de subtipo distintos. Os GUIDs de subtipo correspondem aos códigos FOURCC ' I420 ' e ' IYUV '; consulte [FOURCC de vídeo](video-fourccs.md) para obter mais informações.

 

## <a name="yuv-formats-10-bit-and-16-bit"></a>Formatos YUV: de 10 bits e de 16 bits



| GUID                    | Formatar | amostragem | Embalado ou planar | Bits por canal |
|-------------------------|--------|----------|------------------|------------------|
| **MFVideoFormat \_ P010** | P010   | 4:2:0    | Planar           | 10               |
| **MFVideoFormat \_ P016** | P016   | 4:2:0    | Planar           | 16               |
| **MFVideoFormat \_ P210** | P210   | 4:2:2    | Planar           | 10               |
| **MFVideoFormat \_ P216** | P216   | 4:2:2    | Planar           | 16               |
| **MFVideoFormat \_ v210** | v210   | 4:2:2    | Colocado           | 10               |
| **MFVideoFormat \_ v216** | v216   | 4:2:2    | Colocado           | 16               |
| **MFVideoFormat \_ v410** | v40    | 4:4:4    | Colocado           | 10               |
| **MFVideoFormat \_ Y210** | Y210   | 4:2:2    | Colocado           | 10               |
| **MFVideoFormat \_ Y216** | Y216   | 4:2:2    | Colocado           | 16               |
| **MFVideoFormat \_ Y410** | Y40    | 4:4:4    | Colocado           | 10               |
| **MFVideoFormat \_ Y416** | Y416   | 4:4:4    | Colocado           | 16               |



 

Para obter mais informações sobre esses formatos, consulte [formatos de vídeo YUV de 10 e 16 bits](10-bit-and-16-bit-yuv-video-formats.md).

## <a name="luminance-and-depth-formats"></a>Formatos de luminância e profundidade



| GUID                   | Descrição                                                          |
|------------------------|----------------------------------------------------------------------|
| **\_L8 MFVideoFormat**  | apenas luminância de 8 bits. (BPP). (Mesmo layout de memória que **D3DFMT \_ L8**.) |
| **MFVideoFormat \_ L16** | apenas luminância de 16 bits. (Mesmo layout de memória que **D3DFMT \_ L16**.)      |
| **MFVideoFormat \_ D16** | profundidade de buffer z de 16 bits. (Mesmo layout de memória que **D3DFMT \_ D16**.)      |



 

## <a name="encoded-video-types"></a>Tipos de vídeo codificados



| GUID                        | FOURCC         | Descrição                                                                                                                                                                                                                                                                                                 |
|-----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFVideoFormat \_ DV25**     | 'dv25'         | DVCPRO 25 (525-60 ou 625-50).                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ DV50**     | 'dv50'         | DVCPRO 50 (525-60 ou 625-50).                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ DVC**      | DVC         | Vídeo DVC/DV.                                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ DVH1**     | 'dvh1'         | DVCPRO 100 (1080/60i, 1080/50i ou 720/60P).                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ DVHD**     | 'dvhd'         | HD-DVCR (1125-60 ou 1250-50).                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ DVSD**     | 'dvsd'         | SDL-DVCR (525-60 ou 625-50).                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ DVSL**     | 'dvsl'         | SD-DVCR (525-60 ou 625-50).                                                                                                                                                                                                                                                                                 |
| **MFVideoFormat \_ H263**     | 'H263'         | Vídeo H. 263.                                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ H264**     | Taxas         | Vídeo H. 264.<br/> Os exemplos de mídia contêm dados H. 264 fragmentado com códigos de início e têm SPS/PPS intercalados. Cada exemplo contém uma imagem completa, um campo ou um quadro.<br/>                                                                                                       |
| **MFVideoFormat \_ H265**     | 'H265'         | Vídeo H. 265.                                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ H264 \_ es** | Não aplicável | Fluxo Element H. 264.<br/> Esse tipo de mídia é o mesmo que **MFVideoFormat \_ H264**, exceto que amostras de mídia contêm um fragmentado de H. 264 com fragmentação. Cada exemplo pode conter uma imagem parcial; várias imagens completas; ou uma ou mais imagens completas, além de uma imagem parcial.<br/>           |
| **MFVideoFormat \_ HEVC**     | HEVC         | O perfil principal do HEVC e o perfil de imagem ainda principal.<br/> Cada exemplo contém uma imagem completa.<br/> Com suporte no Windows 8.1 e posterior. O perfil principal do HEVC e o fluxo elementar do perfil de imagem ainda principal. <br/>                                                              |
| **MFVideoFormat \_ HEVC \_ es** | 'HEVS'         | Esse tipo de mídia é o mesmo que **MFVideoFormat \_ HEVC**, exceto que os exemplos de mídia contêm um fragmentado de HEVC fragmentado. Cada exemplo pode conter uma imagem parcial; várias imagens completas; ou uma ou mais imagens completas, além de uma imagem parcial.<br/> Com suporte no Windows 8.1 e posterior.<br/> |
| **MFVideoFormat \_ M4S2**     | ' 4S2 '         | Vídeo MPEG-4 parte 2.                                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ MJPG**     | 'MJPG'         | Movimento JPEG.                                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ MP43**     | 'MP43'         | Microsoft MPEG 4 codec versão 3. Não há mais suporte para esse codec.                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ MP4S**     | MP4S         | Codec ISO MPEG 4 versão 1.                                                                                                                                                                                                                                                                                 |
| **MFVideoFormat \_ MP4V**     | 'MP4V'         | Vídeo MPEG-4 parte 2.                                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ MPEG2**    | Não aplicável | Vídeo MPEG-2. (Equivalente ao **\_ \_ vídeo MEDIASUBTYPE MPEG2** no DirectShow.)                                                                                                                                                                                                                                 |
| **MFVideoFormat \_ VP80**     | 'MPG1'         | Vídeo do VP8.                                                                                                                                                                                                                                                                                                  |
| **MFVideoFormat \_ VP90**     | 'MPG1'         | Vídeo do VP9.                                                                                                                                                                                                                                                                                                  |
| **MFVideoFormat \_ MPG1**     | 'MPG1'         | Vídeo MPEG-1.                                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ MSS1**     | 'MSS1'         | Codec de tela do Windows Media versão 1.                                                                                                                                                                                                                                                                       |
| **MFVideoFormat \_ MSS2**     | 'MSS2'         | Codec de tela do Windows Media Video 9.                                                                                                                                                                                                                                                                         |
| **MFVideoFormat \_ WMV1**     | 'WMV1'         | Windows Media Video Codec versão 7.                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ WMV2**     | 'WMV2'         | Codec do Windows Media Video 8.                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ WMV3**     | 'WMV3'         | Codec do Windows Media Video 9.                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ WVC1**     | 'WVC1'         | SMPTE 421M ("VC-1").                                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ 420O**     | '420O'         | vídeo de 8 bits por canal de planar YUV 4:2:0.                                                                                                                                                                                                                                                                   |
| **MFVideoFormat \_ AV1**     | 'AV01'         | Vídeo do AV1.                                                                                                                                                                                                                                                                                                |



 

## <a name="creating-subtype-guids-from-fourccs-and-d3dformat-values"></a>Criando GUIDs de subtipo de valores FOURCC e D3DFORMAT

Os formatos de vídeo são geralmente representados por valores FOURCC ou **D3DFORMAT** . Um intervalo de GUIDs é reservado para representar esses valores como subtipos. Essas GUIDs têm o formato `XXXXXXXX-0000-0010-8000-00AA00389B71` , em que `XXXXXXXX` é o código FOURCC de 4 bytes ou o valor **D3DFORMAT** .

Se um formato de vídeo tiver um valor **D3DFORMAT** ou FOURCC associado, você poderá criar o GUID de subtipo correspondente da seguinte maneira: comece com a constante **MFVideoFormat \_ base** e substitua a primeira **DWORD** do GUID pelo valor de video FOURCC ou **D3DFORMAT** . Você pode usar a [**macro \_ definir \_ GUID de MediaType**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) para essa finalidade.

> [!Note]  
> O DirectShow também usa esse sistema para a maioria dos subtipos de vídeo, mas não para formatos RGB não compactados. Portanto, os subtipos RGB no DirectShow não correspondem aos subtipos RGB no Media Foundation.

 

A enumeração **D3DFORMAT** é definida no arquivo de cabeçalho d3d9types. h. A tabela a seguir mostra os formatos RGB não compactados mais comuns e o valor **D3DFORMAT** correspondente.



| Formato RGB                                                              | Valor de **D3DFORMAT**     |
|-------------------------------------------------------------------------|-------------------------|
| RGB de 32 bits                                                              | **D3DFMT \_ X8R8G8B8**    |
| RGB de 32 bits com canal alfa                                           | **D3DFMT \_ A8R8G8B8**    |
| RGB de 24 bits                                                              | **D3DFMT \_ R8G8B8**      |
| RGB 555 (RGB de 16 bits)                                                    | **D3DFMT \_ X1R5G5B5**    |
| RGB 555 com canal alfa                                              | **D3DFMT \_ A4R4G4B4**    |
| RGB 565 (RGB de 16 bits)                                                    | **D3DFMT \_ R5G6B5**      |
| palettized RGB de 8 bits                                                    | **D3DFMT \_ P8**          |
| A2 R10 G10 B10 (32 bits RGB com canal alfa; 10 bits por canal RGB) | **D3DFMT \_ A2R10G10B10** |
| A2 B10 G10 R10 (32 bits RGB com canal alfa; 10 bits por canal RGB) | **D3DFMT \_ A2B10G10R10** |
| apenas luminância de 8 bits.                                                   | **\_L8 D3DFMT**          |
| apenas luminância de 16 bits.                                                  | **D3DFMT \_ L16**         |
| profundidade de buffer z de 16 bits                                                   | **D3DFMT \_ D16**         |



 

Para obter mais informações sobre FOURCC, consulte [vídeo FOURCCs](video-fourccs.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[GUIDs de tipo de mídia](media-type-guids.md)
</dt> <dt>

[**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)
</dt> <dt>

[Tipos de mídia](media-types.md)
</dt> <dt>

[Tipos de mídia de vídeo](video-media-types.md)
</dt> </dl>

 

 




