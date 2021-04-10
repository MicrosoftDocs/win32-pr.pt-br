---
description: Filtro de renderizador DirectSound
ms.assetid: ec6cc790-8c1f-4de4-a7ca-a7073894380e
title: Filtro de renderizador DirectSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae932340ea22213e0f9d7234599742d74208f632
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087267"
---
# <a name="directsound-renderer-filter"></a>Filtro de renderizador DirectSound

Esse filtro processa áudio usando DirectSound. Esse filtro é atualmente o processador de áudio padrão para som de onda.

Além de seus recursos básicos de renderização de som, esse filtro pode processar chamadas da API DirectSound. Use os métodos [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) para definir e recuperar a janela que manipulará a reprodução do som. O renderizador de áudio do DirectSound é o filtro de renderização de áudio padrão para o DirectShow.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filtrar interfaces</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a>, <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>, <strong>IDirectSound3DBuffer</strong>, <strong>IDirectSound3dListener</strong>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de entrada</td>
<td>Tipo principal: MEDIATYPE_AudioSubtypes:<br/>
<ul>
<li>MEDIASUBTYPE_PCM</li>
<li>MEDIASUBTYPE_IEEE_FLOAT</li>
<li>MEDIASUBTYPE_DOLBY_AC3_SPDIF</li>
<li>MEDIASUBTYPE_RAW_SPORT</li>
<li>MEDIASUBTYPE_SPDIF_TAG_241h</li>
<li>MEDIASUBTYPE_DRM_Audio</li>
</ul>
Tipo de formato: FORMAT_WaveFormatEx<br/></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia do pino de saída</td>
<td>Não aplicável.</td>
</tr>
<tr class="odd">
<td>Interfaces de pino de saída</td>
<td>Não aplicável.</td>
</tr>
<tr class="even">
<td>CLSID do filtro</td>
<td>CLSID_DSoundRender</td>
</tr>
<tr class="odd">
<td>CLSID de página de propriedades</td>
<td>CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties</td>
</tr>
<tr class="even">
<td>Executável</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Núcleo</a></td>
<td>MERIT_PREFERRED</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria do filtro</a></td>
<td>CLSID_AudioRendererCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Esse filtro atua como um wrapper para um dispositivo de áudio. Para enumerar os dispositivos de áudio disponíveis no sistema do usuário, use a interface [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) com a categoria de processador de áudio (CLSID \_ AudioRendererCategory). Para cada dispositivo de áudio, a categoria de processador de áudio contém duas instâncias de filtro. Um deles corresponde ao renderizador do DirectSound e o outro corresponde ao filtro do [processador de áudio (WaveOut)](audio-renderer--waveout--filter.md) . A instância do DirectSound tem o nome amigável "DirectSound: *DeviceName*", em que *DeviceName* é o nome do dispositivo. A instância de WaveOut tem o nome amigável *DeviceName*.

A categoria de processador de áudio contém duas instâncias de filtro adicionais, chamadas "dispositivo DirectSound padrão" e "dispositivo wave out padrão". Eles correspondem ao dispositivo de som padrão, conforme escolhido pelo usuário por meio do painel de controle. Eles são, na verdade, mapeamentos para um dos pares descritos no parágrafo anterior. Por exemplo, se o sistema tiver dois dispositivos de áudio, o dispositivo A e o dispositivo B, a categoria de processador de áudio conterá o seguinte:

-   Dispositivo A
-   DirectSound: dispositivo A
-   Dispositivo B
-   DirectSound: dispositivo B
-   Dispositivo DirectSound padrão
-   Dispositivo wave out padrão

Se o usuário selecionou o dispositivo A como o dispositivo padrão, "dispositivo DirectSound padrão" é equivalente a "DirectSound: dispositivo A" e "dispositivo wave out padrão" é equivalente a "dispositivo A". Se o usuário selecionar o dispositivo B como o dispositivo padrão, esses mapeamentos serão alterados.

"Dispositivo DirectSound padrão" é atribuído a um mérito de um mérito \_ preferido. Os outros têm mérito de \_ mérito \_ não \_ usam. Portanto, o Intelligent Connect sempre escolherá o dispositivo DirectSound padrão.

O filtro do processador DirectSound dá suporte ao som 3D por meio das interfaces **IDirectSound3DBuffer** e **IDirectSound3dListener** do DirectSound. Você também pode consultar o filtro para as versões atuais dessas interfaces, **IDirectSound3DBuffer8** e **IDirectSound3dListener8**. Execute o grafo antes de chamar métodos nessas interfaces.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 




