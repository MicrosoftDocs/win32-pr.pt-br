---
description: Especifica a taxa máxima de processamento de macrobloco para um fluxo de vídeo H. 264.
ms.assetid: 882F54D1-A963-4016-BEC7-F9C1AC5885FD
title: Atributo MF_MT_H264_MAX_MB_PER_SEC (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b53bdbabd9a633464ed388f2309627b69413c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796062"
---
# <a name="mf_mt_h264_max_mb_per_sec-attribute"></a>Atributo do MF \_ MT \_ H264 no \_ máximo \_ MB \_ por \_ segundo

Especifica a taxa máxima de processamento de macrobloco para um fluxo de vídeo H. 264.

## <a name="data-type"></a>Tipo de dados

**\[ UINT32 \]** armazenado como **UINT8 \[ \]**

## <a name="applies-to"></a>Aplica-se a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Comentários

Esse atributo se aplica aos tipos de mídia para os fluxos H. 264 transmitidos por USB. O valor do atributo é uma matriz de valores UINT32, que correspondem aos campos a seguir no descritor de formato de vídeo UVC 1,5 H. 264.

| Elemento de matriz | Campo de descritor                                           |
|---------------|------------------------------------------------------------|
| 0             | **dwMaxMBperSecOneResolutionNoScalability**                |
| 1             | **dwMaxMBperSecTwoResolutionsNoScalability**               |
| 2             | **dwMaxMBperSecThreeResolutionsNoScalability**             |
| 3             | **dwMaxMBperSecFourResolutionsNoScalability**              |
| 4             | **dwMaxMBperSecOneResolutionTemporalScalability**          |
| 5             | **dwMaxMBperSecTwoResolutionsTemporalScalablility**        |
| 6             | **dwMaxMBperSecThreeResolutionsTemporalScalability**       |
| 7             | **dwMaxMBperSecFourResolutionsTemporalScalability**        |
| 8             | **dwMaxMBperSecOneResolutionTemporalQualityScalability**   |
| 9             | **dwMaxMBperSecTwoResolutionsTemporalQualityScalability**  |
| 10            | **dwMaxMBperSecThreeResolutionsTemporalQualityScalablity** |
| 11            | **dwMaxMBperSecFourResolutionsTemporalQualityScalability** |
| 12            | **dwMaxMBperSecOneResolutionFullScalability**              |
| 13            | **dwMaxMBperSecTwoResolutionsFullScalability**             |
| 14            | **dwMaxMBperSecThreeResolutionsFullScalability**           |
| 15            | **dwMaxMBperSecFourResolutionsFullScalability**            |



 

Esse atributo também é usado com [codificadores de câmera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




