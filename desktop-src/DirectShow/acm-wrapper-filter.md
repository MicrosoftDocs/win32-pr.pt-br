---
description: Filtro de invólucro do ACM
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: Filtro de invólucro do ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da0c1283ac6d4980f51d40001b38c719f5e31c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105792570"
---
# <a name="acm-wrapper-filter"></a>Filtro de invólucro do ACM

O filtro de invólucro do ACM permite que os codecs do ACM (Gerenciador de compactação de áudio) ingressem em um grafo de filtro. Ele pode atuar como um filtro de descompactação ou como um filtro de compactação.

Como um filtro de descompactação, o invólucro do ACM aparece na categoria "filtros do DirectShow" (CLSID \_ LegacyAmFilterCategory) e tem um mérito de mérito \_ normal. O tipo de mídia de conexão no PIN de entrada determina qual codec o filtro usa. Normalmente, o aplicativo não precisa adicionar o filtro ao grafo de filtro; Ele é retirado automaticamente pelo Gerenciador de gráficos de filtro quando necessário. A descompactação é apenas para áudio PCM.

Como um filtro de compactação, o invólucro do ACM aparece na categoria "compactadores de áudio" (CLSID \_ AudioCompressorCategory) e tem um mérito de mérito \_ \_ não \_ usar. Cada codec aparece como uma instância separada. Para compactação, você não pode criar o filtro diretamente com CoCreateInstance. Em vez disso, você deve usar o enumerador de dispositivo do sistema. Para obter mais informações, consulte [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filtrar interfaces</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, IPersist, IPersistPropertyBag</td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de entrada</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia do pino de saída</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_PCM FORMAT_WaveFormatEx. qualquer combinação dos seguintes é possível:<br/>
<ul>
<li>Exemplos por segundo (kHz): 44,1, 22, 5, 11, 25 ou 8,0.</li>
<li>Canais: estéreo ou mono.</li>
<li>Bits por amostra: 8 ou 16.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de saída</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID do filtro</td>
<td>CLSID_ACMWrapper</td>
</tr>
<tr class="odd">
<td>CLSID de página de propriedades</td>
<td>Nenhuma página de propriedades.</td>
</tr>
<tr class="even">
<td>Executável</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Núcleo</a></td>
<td>MERIT_NORMAL ou MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria do filtro</a></td>
<td>CLSID_LegacyAmFilterCategory ou CLSID_AudioCompressorCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 




