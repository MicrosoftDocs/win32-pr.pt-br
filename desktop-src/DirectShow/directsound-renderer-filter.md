---
description: Filtro do renderador DirectSound
ms.assetid: ec6cc790-8c1f-4de4-a7ca-a7073894380e
title: Filtro do renderador DirectSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc1dbd6fc39e7e102cbcd5d25075be6bf86bcc8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983839"
---
# <a name="directsound-renderer-filter"></a>Filtro do renderador DirectSound

Esse filtro renderiza áudio usando DirectSound. Atualmente, esse filtro é o renderador de áudio padrão para som de forma de onda.

Além de seus recursos básicos de renderização de som, esse filtro pode processar chamadas à API DirectSound. Use os [**métodos IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) para definir e recuperar a janela que manipulará a reprodução de som. O Renderador de Áudio DirectSound é o filtro de renderização de áudio padrão para DirectShow.




| Rótulo | Valor |
|--------|-------|
| Interfaces de filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockKinge,</strong></a> <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio,</strong></a> <strong>IDirectSound3DBuffer,</strong> <strong>IDirectSound3dListener,</strong> <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a> | 
| Tipos de mídia de pino de entrada | Tipo principal: MEDIATYPE_AudioSubtypes:<br /><ul><li>MEDIASUBTYPE_PCM</li><li>MEDIASUBTYPE_IEEE_FLOAT</li><li>MEDIASUBTYPE_DOLBY_AC3_SPDIF</li><li>MEDIASUBTYPE_RAW_SPORT</li><li>MEDIASUBTYPE_SPDIF_TAG_241h</li><li>MEDIASUBTYPE_DRM_Audio</li></ul>Tipo de formato: FORMAT_WaveFormatEx<br /> | 
| Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipos de mídia de pino de saída | Não aplicável. | 
| Interfaces de pino de saída | Não aplicável. | 
| Filtrar CLSID | CLSID_DSoundRender | 
| CLSID da página de propriedades | CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties | 
| Executável | quartz.dll | 
| <a href="merit.md">Mérito</a> | MERIT_PREFERRED | 
| <a href="filter-categories.md">Categoria de filtro</a> | CLSID_AudioRendererCategory | 




 

## <a name="remarks"></a>Comentários

Esse filtro atua como um wrapper para um dispositivo de áudio. Para enumerar os dispositivos de áudio disponíveis no sistema do usuário, use a interface [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) com a categoria do renderador de áudio (CLSID \_ AudioRendererCategory). Para cada dispositivo de áudio, a categoria do renderador de áudio contém duas instâncias de filtro. Um deles corresponde ao Renderador DirectSound e o outro corresponde ao filtro Renderador de Áudio [(WaveOut).](audio-renderer--waveout--filter.md) A instância directSound tem o nome amigável "DirectSound: *DeviceName*," em *que DeviceName* é o nome do dispositivo. A instância waveOut tem o nome amigável *DeviceName*.

A categoria do renderador de áudio contém duas instâncias de filtro adicionais, chamadas "Dispositivo DirectSound Padrão" e "Dispositivo WaveOut Padrão". Elas correspondem ao dispositivo de som padrão, conforme escolhido pelo usuário por meio do Painel de Controle. Na verdade, eles são mapeamentos para um dos pares descritos no parágrafo anterior. Por exemplo, se o sistema tiver dois dispositivos de áudio, o Dispositivo A e o Dispositivo B, a categoria do renderador de áudio conterá o seguinte:

-   Dispositivo A
-   DirectSound: Dispositivo A
-   Dispositivo B
-   DirectSound: Dispositivo B
-   Dispositivo DirectSound padrão
-   Dispositivo WaveOut padrão

Se o usuário selecionou Dispositivo A como o dispositivo padrão, "Dispositivo DirectSound Padrão" será equivalente a "DirectSound: Dispositivo A" e "Dispositivo WaveOut Padrão" será equivalente a "Dispositivo A". Se o usuário selecionar o Dispositivo B como o dispositivo padrão, esses mapeamentos serão alteração.

"Dispositivo DirectSound Padrão" recebe um crédito de \_ PREFERENCIAL. Os outros têm o valor DE TAMBÉM \_ NÃO \_ \_ USAR. Portanto, o Conexão inteligente sempre escolherá o dispositivo DirectSound padrão.

O filtro do Renderador DirectSound dá suporte ao som 3D por meio das interfaces DirectSound **IDirectSound3DBuffer** e **IDirectSound3dListener.** Você também pode consultar o filtro para as versões atuais dessas interfaces, **IDirectSound3DBuffer8** e **IDirectSound3dListener8**. Execute o grafo antes de chamar métodos nessas interfaces.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




