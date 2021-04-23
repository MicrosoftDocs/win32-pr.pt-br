---
description: Filtro de captura de áudio
ms.assetid: f76d5c82-33b2-4579-9420-8f97eca53ede
title: Filtro de captura de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a630452565fafad3c4a4420154efd8fe6b282f
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910204"
---
# <a name="audio-capture-filter"></a>Filtro de captura de áudio

O filtro de captura de áudio representa um dispositivo de captura de áudio. Ele tem um pino de saída de captura e vários Pins de entrada (um para cada tipo de entrada no cartão, como linha em, MIC, CD e MIDI).

Esse filtro pode funcionar com mais de um dispositivo de hardware, portanto, chamar CoCreateInstance para criar o filtro não funciona. Em vez disso, use o [enumerador de dispositivo do sistema](system-device-enumerator.md). O enumerador de dispositivo do sistema retorna um moniker exclusivo para cada dispositivo. O nome amigável do moniker corresponde ao nome do dispositivo. (Esse é o nome que aparece em GraphEdit.) Para obter mais informações, consulte [enumerando dispositivos e filtros](enumerating-devices-and-filters.md).



| Label | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer), [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages                                                               |
| Tipos de mídia de pino de entrada                    | MEDIATYPE \_ AnalogAudio, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                                                                         |
| Interfaces de pino de entrada                     | [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                           |
| Tipos de mídia do pino de saída                   | \_Áudio de MediaType, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                                                                               |
| Interfaces de pino de saída                    | [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation), [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource), [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IKsPropertySet**](ikspropertyset.md), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID do filtro                             | Não aplicável                                                                                                                                                                                                                                                                                     |
| CLSID de página de propriedades                      | \_AUDIOINPUTMIXERPROPERTIES CLSID                                                                                                                                                                                                                                                                   |
| Executável                               | qcap.dll                                                                                                                                                                                                                                                                                           |
| [Núcleo](merit.md)                       | MÉRITO \_ \_ não \_ use                                                                                                                                                                                                                                                                                |
| [Categoria do filtro](filter-categories.md) | \_AUDIOINPUTDEVICECATEGORY CLSID                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Comentários

Os Pins de entrada representam conexões de hardware físico e nunca estão conectados a outros filtros no DirectShow.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> <dt>

[Captura de áudio](audio-capture.md)
</dt> </dl>

 

 



