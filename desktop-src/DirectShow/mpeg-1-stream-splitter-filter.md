---
description: Filtro de divisor de fluxo MPEG-1
ms.assetid: abadf37f-2876-496d-90e7-77c3475a0064
title: Filtro de divisor de fluxo MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec47e5ad8df16446c588beec2c5d1c2606b9b1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087839"
---
# <a name="mpeg-1-stream-splitter-filter"></a>Filtro de divisor de fluxo MPEG-1

Esse filtro divide um fluxo do sistema MPEG-1 em seus fluxos de áudio e vídeo do componente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filtrar interfaces</td>
<td><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de entrada</td>
<td>Tipo principal: MEDIATYPE_Stream<br/> Subtipos<br/>
<ul>
<li>MEDIASUBTYPE_MPEG1System</li>
<li>MEDIASUBTYPE_MPEG1VideoCD</li>
<li>MEDIASUBTYPE_Audio</li>
<li>MEDIASUBTYPE_Video</li>
</ul>
Consulte <a href="mpeg-1-media-types.md"> <strong>tipos de mídia MPEG-1</strong></a><br/></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia do pino de saída</td>
<td>Tipo principal: MEDIATYPE_Audio ou MEDIATYPE_Video<br/> Subtipo: MEDIASUBTYPE_MPEG1Payload ou MEDIASUBTYPE_MPEG1Packet<br/> Consulte <a href="mpeg-1-media-types.md"> <strong>tipos de mídia MPEG-1</strong></a><br/></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de saída</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></td>
</tr>
<tr class="even">
<td>CLSID do filtro</td>
<td>CLSID_MPEG1Splitter</td>
</tr>
<tr class="odd">
<td>CLSID de página de propriedades</td>
<td>Nenhuma página de propriedades</td>
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



 

## <a name="remarks"></a>Comentários

Este arquivo dá suporte ao modo de pull somente por meio de [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ; Ele não dá suporte ao modo de push.

Como o conteúdo MPEG-1 não é indexado, a busca pode ser muito aproximada. Geralmente é bom para um fluxo de sistema de taxa de bits MPEG-1 fixo (que geralmente é gerado pelo hardware para o CD de vídeo).

O filtro dá suporte à interface [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) para recuperar metadados ID3.

Nem todas as amostras MPEG têm carimbos de data/hora. A falta de um carimbo de data/hora em um exemplo de MPEG não é um erro. Para os desenvolvedores de filtro, isso significa que você não deve retornar um código de erro do método **Receive** do PIN de entrada se [**IMediaSample:: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) falhar. Se **Receive** retornar qualquer valor diferente de S \_ OK, isso fará com que o divisor pare de enviar amostras.

Se o arquivo contiver um fluxo de vídeo, o divisor de fluxo MPEG-1 dará suporte à busca por número de quadro. Para habilitar a busca baseada em quadros, chame [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) no [Gerenciador de gráficos de filtro](filter-graph-manager.md) com o **\_ \_ quadro formato de tempo** de valor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 




