---
description: Filtro de processador de áudio (WaveOut)
ms.assetid: a3f2776b-974b-4886-82a3-38e00b607a07
title: Filtro de processador de áudio (WaveOut)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d66d92357b41b6fa23018acf6d44b966eb77fab
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987649"
---
# <a name="audio-renderer-waveout-filter"></a>Filtro de processador de áudio (WaveOut)

Esse filtro usa a API de WaveOut \* para renderizar áudio de onda. No entanto, o [filtro de processamento do DirectSound](directsound-renderer-filter.md) fornece a mesma funcionalidade usando o DirectSound. por padrão, o filtro Graph Manager usa o renderizador DirectSound em vez desse filtro. A mixagem de áudio está desabilitada no processador de áudio de onda e, portanto, se você precisar misturar vários fluxos de áudio durante a reprodução, use o renderizador DirectSound.

Esse filtro não verifica o subtipo do fluxo de áudio. A estrutura [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) ou [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) passada no formato contém as informações necessárias para a conexão.

Esse filtro oferece suporte a um intervalo de taxas de exemplo que depende do driver de áudio.




| Rótulo | Valor |
|--------|-------|
| Filtrar interfaces | <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li><li>IPersistPropertyBag</li><li>IPersistStream</li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></li></ul> | 
| Tipos de mídia de pino de entrada | <strong>MEDIATYPE_Audio</strong> | 
| Interfaces de pino de entrada | <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li></ul> | 
| Tipos de mídia do pino de saída | Não aplicável. | 
| Interfaces de pino de saída | Não aplicável. | 
| CLSID do filtro | <strong>CLSID_AudioRender</strong> | 
| CLSID de página de propriedades | <strong>CLSID_AudioProperties</strong>, <strong>CLSID_AudioRendererAdvancedProperties</strong> | 
| Executável | quartz.dll | 
| <a href="merit.md">Núcleo</a> | <strong>MERIT_DO_NOT_USE</strong> | 
| <a href="filter-categories.md">Categoria do filtro</a> | <strong>CLSID_AudioRendererCategory</strong> | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> </dl>

 

 
