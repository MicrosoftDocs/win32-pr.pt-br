---
description: O decodificador de vídeo da parte 2 do MPEG4 decodifica fluxos de vídeo que foram codificados de acordo com o padrão da parte 2 do MPEG4.
ms.assetid: 56e32d3c-9bd0-41fe-bb22-e4ff37b7cc5c
title: Decodificador de vídeo MPEG-4 parte 2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847e5be8c506e534c42962ecf6b0037a2ecb2f184c9c47fa92981fa32fd55422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973015"
---
# <a name="mpeg-4-part-2-video-decoder"></a>Decodificador de vídeo MPEG-4 parte 2

O decodificador de vídeo da parte 2 do MPEG4 decodifica fluxos de vídeo que foram codificados de acordo com o padrão da parte 2 do MPEG4.

Você pode criar uma instância do decodificador de vídeo da parte 2 do MPEG4 chamando **CoCreateInstance**. para criar uma instância do decodificador que se comporta como um objeto de mídia do DirectX (DMO), use o **CLSID \_** do identificador de classe CMpeg4sDecMediaObject. Para criar um Istance do decodificador que se comporta como uma Media Foundation transformação (MFT), use o CLSID do identificador de classe **\_ CMpeg4sDecMFT**.

## <a name="input-types"></a>Tipos de entrada

O decodificador de vídeo da parte 2 do MPEG4 dá suporte aos seguintes tipos de mídia de entrada.

-   MEDIASUBTYPE \_ M4S2
-   MEDIASUBTYPE \_ m4s2
-   MEDIASUBTYPE \_ MP4V
-   MEDIASUBTYPE \_ MP4V
-   MEDIASUBTYPE \_ MP4S (preterido)
-   MEDIASUBTYPE \_ MP4s (preterido)

## <a name="output-types"></a>Tipos de saída

O decodificador de vídeo da parte 2 do MPEG4 dá suporte aos seguintes subtipos de mídia de saída quando está agindo como um DMO.

-   MEDIASUBTYPE \_ YV12
-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ YVYU
-   MEDIASUBTYPE \_ NV11
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

O decodificador de vídeo da parte 2 do MPEG4 dá suporte aos seguintes subtipos de mídia de saída quando ele está atuando como um MFT.

-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YV12

## <a name="formats"></a>Formatos

O decodificador de vídeo da parte 2 do MPEG4 aceita os seguintes formatos.

-   [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)
-   [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)
-   [**MFVideoInfo**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoinfo)
-   [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (somente a parte VIH2 do cabeçalho é usada.)

## <a name="interfaces-for-the-dmo"></a>Interfaces para o DMO

se você criar uma instância do decodificador de vídeo do MPEG4 parte 2 como um DMO, o decodificador expõe as interfaces a seguir.

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)

Você pode obter uma interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) chamando **CoCreateInstance** e pode obter uma interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) chamando **QueryInterface**.

## <a name="interfaces-for-the-mft"></a>Interfaces para o MFT

Se você criar uma instância do decodificador de vídeo MPEG2 parte 2 como um MFT, o decodificador exporá as interfaces a seguir.

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)

Você pode obter um ponteiro para a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) chamando **CoCreateInstance**, e você pode obter um ponteiro para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) chamando [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes). Você pode obter um ponteiro para a interface [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) ou [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) chamando **QueryInterface** no MFT. Você pode obter um ponteiro para a interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) ou [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) chamando [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) e passando o serviço de **controle de \_ taxa \_ \_ de MF** do identificador de serviço.

## <a name="profiles-and-levels"></a>Perfis e níveis

A especificação MPEG4 define vários perfis, cada um deles especifica as ferramentas que um codificador pode usar para gerar um fluxo codificado. O decodificador de vídeo MPEG4 parte 2 dá suporte a dois desses perfis: perfil visual simples e perfil simples avançado. Em outras palavras, o decodificador de vídeo da parte 2 do MPEG4 pode decodificar fluxos que foram codificados de acordo com o perfil visual simples ou com o perfil simples avançado.

O perfil visual simples dá suporte à transmissão básica de vídeo de taxa de bits baixa no modo progressivo. Ele dá suporte apenas a imagens de intra e de previsão. Ele também dá suporte ao modo de cabeçalho curto, que é compatível com versões anteriores com o perfil de linha de base H. 263. a partir do Windows 10, o decodificador de vídeo da parte 2 MPEG-4 também dá suporte a h. 263v2 (h. 263 +) que oferece suporte a tamanhos de imagem personalizados.

O perfil simples avançado dá suporte a todas as ferramentas do perfil visual simples e, além disso, dá suporte a vídeo entrelaçado, quadros B, compensação de movimento trimestre-PEL, tabelas de quantificação adicionais e compensação de movimento global.

A especificação MPEG4 também define vários níveis, cada um deles especifica restrições no fluxo de saída gerado por um codificador.

A tabela a seguir mostra os perfis e os níveis, juntamente com as resoluções típicas, suportadas pelo decodificador de vídeo da parte 2 do MPEG4.



| Perfil         | Nível | Resolução típica |
|-----------------|-------|--------------------|
| Visual simples   | 0     | 176 x 144          |
| Visual simples   | 1     | 176 x 144          |
| Visual simples   | 2     | 352 x 288          |
| Visual simples   | 3     | 352 x 288          |
| SimpleVisual    | 4a    | 640 x 480          |
| Visual simples   | 5     | 720 x 576          |
| Avançado simples | 0     | 176 x 144          |
| Avançado simples | 1     | 176 x 144          |
| Avançado simples | 2     | 352 x 288          |
| Avançado simples | 3     | 352 x 288          |
| Avançado simples | 3b    | 352 x 288          |
| Advanced Simple | 4     | 352 x 756          |
| Advanced Simple | 5     | 720 x 576          |



 

Para obter mais informações sobre perfis e níveis, consulte a especificação MPEG4 Parte 2 (ISO/IEC 14496-2): Tecnologia da informação – Codificação de objetos audiovisual – Parte 2: Visual.

## <a name="decoder-properties"></a>Propriedades do decodificador

Para definir propriedades no decodificador de vídeo MPEG4 Parte 2, use a interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) ou a interface [**IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

O decodificador de vídeo MPEG4 Parte 2 dá suporte às propriedades a seguir.



<table>
<thead>
<tr class="header">
<th>Propriedade</th>
<th>Descrição</th>
<th>Valor padrão</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></td>
<td>Especifica o nível de energia.<br/> <dl> Windows 7.<br />
Somente gravação.<br />
</dl></td>
<td>100</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></td>
<td>Especifica o modo de geração de miniaturas.<br/> <dl> Windows 7.<br />
Somente gravação.<br />
</dl></td>
<td><strong>VARIANT_FALSE</strong></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Os GUIDs (identificadores globalmente exclusivos) para subtipos de mídia RGB diferem dependendo se um decodificador está atuando como um DMO ou um MFT. Os GUIDs para subtipos de mídia não RGB são os mesmos, independentemente de um decodificador estar atuando como um DMO ou um MFT. Para obter informações sobre os GUIDs que representam subtipos de mídia, consulte [Tipos de mídia](media-types.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MP4SDecd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos codec](codecobjects.md)
</dt> </dl>

 

 
