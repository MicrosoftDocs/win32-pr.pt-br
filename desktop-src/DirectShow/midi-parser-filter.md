---
description: Filtro de analisador de MIDI
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: Filtro de analisador de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5907c36e668a39494b46ec6bbc67e4d8cb4870357df9c1f0303c882bc86f0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119256506"
---
# <a name="midi-parser-filter"></a>Filtro de analisador de MIDI

O filtro analisador de MIDI lê dados MIDI encontrados no. MID e. Arquivos RMI. O filtro aceita um fluxo da [origem do arquivo assíncrono](file-source--async--filter.md) ou dos filtros de [origem do arquivo de URL](file-source--url--filter.md) e gera amostras de MIDI para o [**renderizador de Midi**](midi-renderer-filter.md) para reprodução.



| Rótulo | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| Tipos de mídia de pino de entrada                    | \_Fluxo de MediaType, \_ MIDI MEDIASUBTYPE                                                                    |
| Interfaces de pino de entrada                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| Tipos de mídia do pino de saída                   | \_MEDIASUBTYPE de mídia MIDI, \_ nulo                                                                      |
| Interfaces de pino de saída                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| CLSID do filtro                             | \_MIDIPARSER CLSID                                                                                        |
| CLSID de página de propriedades                      | Nenhuma página de propriedades                                                                                         |
| Executável                               | quartz.dll                                                                                               |
| [Núcleo](merit.md)                       | MÉRITO \_ improvável                                                                                          |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                            |



 

## <a name="remarks"></a>Comentários

Para obter mais informações, consulte [**processador de Midi**](midi-renderer-filter.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> </dl>

 

 



