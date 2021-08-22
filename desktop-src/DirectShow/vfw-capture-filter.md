---
description: Filtro de captura do VFW
ms.assetid: 663b6b3b-2a50-4586-9506-600a59869abe
title: Filtro de captura do VFW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 679f8e736564534948d05fe25ecb1bc18bbb787df370aca0f9a3752960f719ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071950"
---
# <a name="vfw-capture-filter"></a>Filtro de captura do VFW

Esse filtro funciona com um hardware de captura de vídeo mais antigo que usa o Video For Windows.

Esse filtro tem dois pinos de saída. Um é chamado de Captura e o outro é chamado de Visualização ou Sobreposição.



| Rótulo | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | **IPersistPropertyBag,** [**IAMVfwCaptureDialogs,**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) [**IAMFilterMiscFlags,**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) **ISpecifyPropertyPages,** [**IOverlayNotify**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Tipos de mídia de pino de entrada                    | Não aplicável.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Interfaces de pino de entrada                     | Não aplicável.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Tipos de mídia de pino de saída                   | Captura: VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL, FORMAT \_ VideoInfoOverlay: MEDIATYPE \_ Video, MEDIASUBTYPE \_ Overlay, FORMAT \_ VideoInfo<br/> Versão prévia: VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL, FORMAT \_ VideoInfo<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Interfaces de pino de saída                    | Pino de captura: [**IAMBufferNegotiation,**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation) [**IAMDroppedFrames,**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource), [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IKsPropertySet**](ikspropertyset.md), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)Overlay Pin: [**IAMStreamControl,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) [**IKsPropertySet,**](ikspropertyset.md) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> Pino de visualização: [**IAMPushSource,**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) [**IAMStreamControl,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) [**IKsPropertySet,**](ikspropertyset.md) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> |
| Filtrar CLSID                             | CLSID \_ VfwCapture                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| CLSID da página de propriedades                      | CLSID \_ CaptureProperties                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Executável                               | qcap.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Mérito](merit.md)                       | NÃO USE O NÃO \_ \_ USO \_ DE LIMITED                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [Categoria de filtro](filter-categories.md) | CLSID \_ VideoInputDeviceCategory                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Comentários

Embora o pino de captura exponha a interface [**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) somente os métodos **SetFormat** e **GetFormat** são implementados para essa interface.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 




