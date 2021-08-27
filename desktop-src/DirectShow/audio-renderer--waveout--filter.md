---
description: Filtro de Renderização de Áudio (WaveOut)
ms.assetid: a3f2776b-974b-4886-82a3-38e00b607a07
title: Filtro de Renderização de Áudio (WaveOut)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef79acb21221c1a0b91efc2da67773534fe54ca
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470153"
---
# <a name="audio-renderer-waveout-filter"></a>Filtro de Renderização de Áudio (WaveOut)

Esse filtro usa a API waveOut \* para renderizar o áudio de forma de onda. No entanto, [o Filtro do Renderador DirectSound](directsound-renderer-filter.md) fornece a mesma funcionalidade usando o DirectSound. Por padrão, o Gerenciador Graph Filtro usa o Renderador DirectSound em vez desse filtro. A combinação de áudio está desabilitada no renderador de áudio waveOut, portanto, se você precisar misturar vários fluxos de áudio durante a reprodução, use o renderador DirectSound.

Esse filtro não verifica o subtipo do fluxo de áudio. A [**estrutura WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) [**ou WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) passada no formato contém as informações necessárias para a conexão.

Esse filtro dá suporte a uma variedade de taxas de exemplo que dependem do driver de áudio.




| | | Interfaces de filtro | <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClock Ltda</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>Ibasicaudio</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Imediaposition</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>Imediaseeking</strong></a></li><li>Ipersistpropertybag</li><li>Ipersiststream</li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>Iqualitycontrol</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>Ireferenceclock</strong></a></li></ul> | | Tipos de mídia de pino de entrada | <strong>MEDIATYPE_Audio</strong> | | Interfaces de pino de entrada | <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Imeminputpin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>Iqualitycontrol</strong></a></li></ul> | | Tipos de mídia de pino de | Não aplicável. | | Interfaces de pino de | Não aplicável. | | Filtrar CLSID | <strong>CLSID_AudioRender</strong> | | ClSID da página de propriedades | <strong>CLSID_AudioProperties</strong>, <strong>CLSID_AudioRendererAdvancedProperties</strong> | | Arquivo executável | quartz.dll | | <a href="merit.md">Berem</a>  |  <strong>MERIT_DO_NOT_USE</strong> | | <a href="filter-categories.md">Categoria de filtro</a>  |  <strong>CLSID_AudioRendererCategory</strong> | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 
