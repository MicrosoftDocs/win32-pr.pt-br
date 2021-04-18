---
description: Esse filtro desmultiplexa o transporte MPEG-2 e os fluxos de programa que são entregues no modo de push.
ms.assetid: 99bfc55d-6519-4e85-98ce-cad27bd71ffb
title: Demultiplexador MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ea71727dc273bd0dc5d65ac49b28385b4898067
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105759992"
---
# <a name="mpeg-2-demultiplexer"></a>Demultiplexador MPEG-2

Esse filtro desmultiplexa o transporte MPEG-2 e os fluxos de programa que são entregues no modo de push. A partir do Windows XP, esse filtro também dá suporte a fluxos de programa no modo de pull (reprodução de arquivo). Em plataformas anteriores, use o filtro [divisor MPEG-2](mpeg-2-splitter.md) para fluxos de programa no modo de pull. Esse filtro pode ser usado em qualquer tipo de grafo de filtro, incluindo um gráfico de filtro de TV digital BDA.

> [!Note]  
> O demultiplexador MPEG-2 não dá suporte à busca com precisão de quadro.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filtrar interfaces</td>
<td>Todos os modos:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li>
<li><strong>ISpecifyPropertyPages</strong></li>
</ul>
Somente modo de push:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de entrada</td>
<td>Tipo principal: MEDIATYPE_STREAM<br/> Subtipo<br/>
<ul>
<li>KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</li>
<li>MEDIASUBTYPE_MPEG2_PROGRAM</li>
<li>MEDIASUBTYPE_MPEG2_TRANSPORT</li>
<li>MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</li>
</ul>
Para obter mais informações, consulte <a href="mpeg-2-demultiplexer-media-types.md"><strong>tipos de mídia do demultiplexador MPEG-2</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia do pino de saída</td>
<td>Os fluxos elementares de áudio e vídeo devem ter um tipo principal de MEDIATYPE_Audio ou MEDIATYPE_Video.<br/> Para obter mais informações, consulte <a href="mpeg-2-demultiplexer-media-types.md"><strong>tipos de mídia do demultiplexador MPEG-2</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de saída</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>somente modo push: <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource</strong></a>, <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a><br/> Somente modo de pull: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a><br/></td>
</tr>
<tr class="even">
<td>CLSID do filtro</td>
<td>CLSID_MPEG2Demultiplexer</td>
</tr>
<tr class="odd">
<td>CLSID de página de propriedades</td>
<td>Disponível somente para teste. Usar a interface <strong>ISpecifyPropertyPages</strong> para acessar as páginas de propriedades</td>
</tr>
<tr class="even">
<td>Executável</td>
<td>mpg2splt.ax</td>
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

Para gerar fluxos de áudio e vídeo elementares, o Demux deve receber os fluxos de PCR e SCR. No lado da entrada, isso significa que um fluxo de transporte deve conter as tabelas PAT e PGTO que definem o PID para o fluxo de PCR; e fluxos de programa devem conter pelo menos um cabeçalho de pacote.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |
| Fim do suporte do servidor<br/>    | Windows Server 2003 R2<br/>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> <dt>

[Usando o demultiplexador MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




