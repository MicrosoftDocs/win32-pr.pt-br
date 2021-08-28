---
description: Esse filtro demultiplexes de fluxos de transporte e programa MPEG-2 que são entregues no modo push.
ms.assetid: 99bfc55d-6519-4e85-98ce-cad27bd71ffb
title: MPEG-2 Demultiplexer
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21898cb4fa3c16b07508dc3370c519d3edfbced
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983949"
---
# <a name="mpeg-2-demultiplexer"></a>MPEG-2 Demultiplexer

Esse filtro demultiplexes de fluxos de transporte e programa MPEG-2 que são entregues no modo push. Começando no Windows XP, esse filtro também dá suporte a fluxos de programas no modo de pull (reprodução de arquivo). Em plataformas anteriores, use o filtro [divisor MPEG-2](mpeg-2-splitter.md) para fluxos de programas no modo de pull. Esse filtro pode ser usado em qualquer tipo de grafo de filtro, incluindo um grafo de filtro de TV digital BDA.

> [!Note]  
> O Demultiplexer MPEG-2 não dá suporte à busca com precisão de quadro.

 




| Rótulo | Valor |
|--------|-------|
| Interfaces de filtro | Todos os modos:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a></li><li><strong>Ispecifypropertypages</strong></li></ul>Somente no modo de push:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>Ireferenceclock</strong></a></li></ul> | 
| Tipos de mídia de pino de entrada | Tipo principal: MEDIATYPE_STREAM<br /> Subtipo:<br /><ul><li>KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</li><li>MEDIASUBTYPE_MPEG2_PROGRAM</li><li>MEDIASUBTYPE_MPEG2_TRANSPORT</li><li>MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</li></ul>Para obter mais informações, <a href="mpeg-2-demultiplexer-media-types.md"><strong>consulte MpEG-2 Demultiplexer Media Types</strong></a>.<br /> | 
| Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipos de mídia de pino de saída | Os fluxos elementares de áudio e vídeo devem ter um tipo principal de MEDIATYPE_Audio ou MEDIATYPE_Video.<br /> Para obter mais informações, <a href="mpeg-2-demultiplexer-media-types.md"><strong>consulte MpEG-2 Demultiplexer Media Types</strong></a>.<br /> | 
| Interfaces de pino de saída | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Somente no</strong></a>modo push <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IPin, IQualityControl:</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource</strong></a>, <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a><br /> Somente modo de pull: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a><br /> | 
| Filtrar CLSID | CLSID_MPEG2Demultiplexer | 
| CLSID da página de propriedades | Disponível somente para teste. Use a interface <strong>ISpecifyPropertyPages</strong> para acessar as páginas de propriedades | 
| Executável | mpg2splt.ax | 
| <a href="merit.md">Mérito</a> | MERIT_NORMAL | 
| <a href="filter-categories.md">Categoria de filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Comentários

Para saída de fluxos elementares de áudio e vídeo, o demux deve receber os fluxos PCR e SCR. No lado de entrada, isso significa que um fluxo de transporte deve conter as tabelas PAT e PMT que definem o PID para o fluxo PCR; Os fluxos de programa e devem conter pelo menos um header de pacote.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |
| Fim do suporte ao servidor<br/>    | Windows Server 2003 R2<br/>                          |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Usando o Demultiplexer MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




