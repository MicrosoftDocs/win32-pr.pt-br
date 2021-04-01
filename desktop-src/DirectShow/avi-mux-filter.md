---
description: Filtro AVI Mux
ms.assetid: 31d30c91-fc6a-45ec-a2e0-34e6a1e902a4
title: Filtro AVI Mux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3755a4d5f63e824ae08eb736a5999dcac3d7ab32
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825990"
---
# <a name="avi-mux-filter"></a>Filtro AVI Mux

O filtro AVI Mux aceita vários fluxos de entrada e os intercala no formato AVI. O filtro usa Pins de entrada separados para cada fluxo de entrada e um PIN de saída para o fluxo AVI.

Aplicativos de criação ou captura de vídeo podem usar esse filtro para salvar arquivos em disco no formato AVI. O filtro é normalmente conectado ao filtro do [gravador de arquivo](file-writer-filter.md) , mas pode se conectar a qualquer filtro cujo PIN de entrada dê suporte às interfaces IStream e [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filtrar interfaces</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a>, ISpecifyPropertyPages</td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de entrada</td>
<td>Qualquer tipo principal que corresponda a um FOURCC de estilo antigo ou MEDIATYPE_AUXLine21Data. (Para obter mais informações, consulte <a href="fourccmap.md"><strong>classe FOURCCMap</strong></a>.)
<ul>
<li>Se o tipo principal for MEDIATYPE_Audio, o formato deverá ser FORMAT_WaveFormatEx.</li>
<li>Se o tipo principal for MEDIATYPE_Video, o formato deverá ser FORMAT_VideoInfo ou FORMAT_DvInfo.</li>
<li>Se o tipo principal for MEDIATYPE_Interleaved, o formato deverá ser FORMAT_DvInfo.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia do pino de saída</td>
<td>MEDIATYPE_Stream, MEDIASUBTYPE_Avi</td>
</tr>
<tr class="odd">
<td>Interfaces de pino de saída</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID do filtro</td>
<td>CLSID_AviDest</td>
</tr>
<tr class="odd">
<td>CLSID de página de propriedades</td>
<td>CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1</td>
</tr>
<tr class="even">
<td>Executável</td>
<td>qcap.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Núcleo</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria do filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

### <a name="remarks"></a>Comentários

Os comentários a seguir descrevem vários aspectos da funcionalidade do filtro AVI Mux.

Pins

Quando o filtro AVI Mux é criado, ele tem um PIN de entrada. Como cada pino de entrada é conectado, o filtro cria um novo PIN de entrada.

Propriedades do fluxo

Os Pins de entrada dão suporte à interface IPropertyBag para definir propriedades em fluxos individuais. Atualmente, a seguinte propriedade é definida:



| Propriedade | Descrição                                                           |
|----------|-----------------------------------------------------------------------|
| name     | O nome do fluxo. Essa propriedade é gravada como uma `'strn'` parte. |



 

Se o filtro estiver em execução ou em pausa, o método IPropertyBag:: Write retornará \_ VFW \_ E \_ estado incorreto.

Taxas de quadros

Se o filtro upstream não especificar uma taxa de quadros no membro **AvgTimePerFrame** da estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , o AVI Mux usará os carimbos de data/hora no primeiro quadro de vídeo. O formato de arquivo AVI não oferece suporte a taxas de quadros variáveis.

Quadros descartados

O filtro AVI Mux calcula os quadros descartados com base nos tempos de mídia de cada amostra, se disponíveis ou os carimbos de data/hora do exemplo. Ele grava uma entrada de índice de comprimento zero para cada quadro Descartado.

IMediaSeeking

O filtro AVI Mux implementa a interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) da seguinte maneira:

-   O método [**getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) retorna o progresso atual da multiplexação. Se você estiver transcodificando um arquivo (mais lento do que o tempo real), esse valor será mais preciso do que o valor retornado pelo Gerenciador do gráfico de filtro. Para obter mais informações, consulte a seção comentários da página de referência do GetCurrentPosition.
-   O método [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) consulta cada filtro upstream e retorna a duração do fluxo mais longo. Se qualquer um desses filtros falhar na chamada getDuration (ou não oferecer suporte a IMediaSeeking), o AVI Mux retornará um código de falha e preencherá o parâmetro *pDuration* com a duração mais longa encontrada. No entanto, o valor de *pDuration* nesse caso não é necessariamente o comprimento do fluxo de entrada mais longo.
-   O AVI Mux não implementa os métodos GetStopPosition, GetPositions, GetAvailable, GetRate ou GetPreroll; Nem implementa nenhum \* método definido para busca.

Extensões de formato de arquivo AVI 2,0

Atualmente, o DirectShow dá suporte às seguintes extensões de formato de arquivo AVI 2,0:

-   Maior tamanho de arquivo AVI (maior que 1 GB)
-   Indexação hierárquica

Para obter mais informações, consulte a versão 1, 2 do "OpenDML AVI File Format Extensions" publicado pelo Subcomitê OpenDML AVI M-JPEG File Format.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 



