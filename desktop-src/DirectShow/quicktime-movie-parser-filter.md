---
description: Filtro do analisador de filmes QuickTime
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: Filtro do analisador de filmes QuickTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a046e143487a1455aeeb125910bbf4452b4f947
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104296039"
---
# <a name="quicktime-movie-parser-filter"></a>Filtro do analisador de filmes QuickTime

Este componente foi removido do Windows Vista e de sistemas operacionais posteriores. Ele está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.

O filtro QuickTime Movie Parser divide os dados do Apple® QuickTime® em fluxos de áudio e vídeo. Ele dá suporte ao QuickTime 2,0 e anterior. O PIN de entrada se conecta a um filtro de origem, como o filtro de [origem de arquivo assíncrono](file-source--async--filter.md) ou o filtro de [origem de arquivo de URL](file-source--url--filter.md) . O analisador usa o filtro [AVI descompactador](avi-decompressor-filter.md) ou [Qt descompactador](qt-decompressor-filter.md) para descompactar arquivos QuickTime. O filtro cria um pino de saída para o fluxo de vídeo e um PIN de saída para o fluxo de áudio.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filtrar interfaces</td>
<td><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de entrada</td>
<td>MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie;</td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia do pino de saída</td>
<td><ul>
<li>MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</li>
<li>MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de saída</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID do filtro</td>
<td>CLSID_QuickTimeParser</td>
</tr>
<tr class="odd">
<td>CLSID de página de propriedades</td>
<td>Nenhuma página de propriedades.</td>
</tr>
<tr class="even">
<td>Executável</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Núcleo</a></td>
<td>MERIT_NORMAL</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria do filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 



