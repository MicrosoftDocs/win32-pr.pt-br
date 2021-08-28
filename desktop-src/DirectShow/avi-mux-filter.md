---
description: Filtro AVI Mux
ms.assetid: 31d30c91-fc6a-45ec-a2e0-34e6a1e902a4
title: Filtro AVI Mux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3250746a65aaaf075c28700c3531bf97b1faf23
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986259"
---
# <a name="avi-mux-filter"></a>Filtro AVI Mux

O filtro AVI Mux aceita vários fluxos de entrada e os intercala no formato AVI. O filtro usa pinos de entrada separados para cada fluxo de entrada e um pino de saída para o fluxo AVI.

Os aplicativos de captura de vídeo ou de autor podem usar esse filtro para salvar arquivos em disco no formato AVI. O filtro normalmente é conectado ao filtro [Do](file-writer-filter.md) autor do arquivo, mas pode se conectar a qualquer filtro cujo pin de entrada dá suporte às interfaces IStream e [**IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)




| Rótulo | Valor |
|--------|-------|
| Interfaces de filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag,</strong></a>ISpecifyPropertyPages | 
| Tipos de mídia de pino de entrada | Qualquer tipo principal que corresponda a um FOURCC de estilo antigo ou MEDIATYPE_AUXLine21Data. (Para obter mais informações, consulte <a href="fourccmap.md"><strong>Classe FOURCCMap</strong></a>.)<ul><li>Se o tipo principal for MEDIATYPE_Audio, o formato deverá ser FORMAT_WaveFormatEx.</li><li>Se o tipo principal for MEDIATYPE_Video, o formato deverá ser FORMAT_VideoInfo ou FORMAT_DvInfo.</li><li>Se o tipo principal for MEDIATYPE_Interleaved, o formato deverá ser FORMAT_DvInfo.</li></ul> | 
| Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a>IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipos de mídia de pino de saída | MEDIATYPE_Stream, MEDIASUBTYPE_Avi | 
| Interfaces de pino de saída | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| Filtrar CLSID | CLSID_AviDest | 
| CLSID da página de propriedades | CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1 | 
| Executável | qcap.dll | 
| <a href="merit.md">Mérito</a> | MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">Categoria de filtro</a> | CLSID_LegacyAmFilterCategory | 




 

### <a name="remarks"></a>Comentários

Os comentários a seguir descrevem vários aspectos da funcionalidade do filtro AVI Mux.

Pins

Quando o filtro AVI Mux é criado, ele tem um pino de entrada. À medida que cada pino de entrada é conectado, o filtro cria um novo pino de entrada.

Propriedades do fluxo

Os pinos de entrada são suportados pela interface IPropertyBag para definir propriedades em fluxos individuais. Atualmente, a propriedade a seguir está definida:



| Propriedade | Descrição                                                           |
|----------|-----------------------------------------------------------------------|
| name     | O nome do fluxo. Essa propriedade é escrita como uma `'strn'` parte. |



 

Se o filtro estiver em execução ou em pausa, o método IPropertyBag::Write retornará VFW \_ E \_ WRONG \_ STATE.

Taxas de quadros

Se o filtro upstream não especificar uma taxa de quadros no membro **AvgTimePerFrame** da estrutura [**VIDEOINFOHEADER,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o AVI Mux usará os carimbos de data/hora no primeiro quadro de vídeo. O formato de arquivo AVI não dá suporte a taxas de quadros variáveis.

Quadros descartados

O filtro AVI Mux calcula quadros descartados com base nos tempos de mídia de cada amostra, se disponível, ou então os carimbos de data/hora da amostra. Ele grava uma entrada de índice de comprimento zero para cada quadro descartado.

Imediaseeking

O filtro AVI Mux implementa a interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) da seguinte forma:

-   O [**método GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) retorna o progresso atual da multiplexação. Se você estiver transcodificando um arquivo (mais lento do que em tempo real), esse valor será mais preciso do que o valor retornado pelo Gerenciador de Graph Filtro. Para obter mais informações, consulte a seção Comentários da página de referência GetCurrentPosition.
-   O [**método GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) consulta cada filtro upstream e retorna a duração do fluxo mais longo. Se qualquer um desses filtros falhar na chamada GetDuration (ou não der suporte a IMediaSeeking), o AVI Mux retornará um código de falha e preencherá o parâmetro *pDuration* com a duração mais longa encontrada. No entanto, o valor *de pDuration* nesse caso não é necessariamente o comprimento do fluxo de entrada mais longo.
-   O AVI Mux não implementa os métodos GetStopPosition, GetPositions, GetAvailable, GetRate ou GetPreroll; nem implementa métodos Set \* para busca.

Extensões de formato de arquivo AVI 2.0

DirectShow atualmente dá suporte às seguintes extensões de formato de arquivo AVI 2.0:

-   Maior tamanho do arquivo AVI (maior que 1 GB)
-   Indexação hierárquica

Para obter mais informações, consulte a versão 1.02 das "Extensões de formato de arquivo OPENDML AVI" publicadas pelo subcomitê de formato de arquivo OPENDML AVI M-JPEG.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



