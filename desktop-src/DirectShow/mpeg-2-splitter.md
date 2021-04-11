---
description: Divisor MPEG-2
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: Divisor MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0f04062660df7711a573dd17deb82f90897454a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163836"
---
# <a name="mpeg-2-splitter"></a>Divisor MPEG-2

A partir do Microsoft® Windows® XP, o filtro de divisão MPEG-2 é preterido. Em vez disso, use o [demultiplexador MPEG-2](mpeg-2-demultiplexer.md) .

Em plataformas anteriores, use o divisor MPEG-2 para fluxos de programa MPEG-2 entregues no modo de pull que contém pelo menos um dos seguintes tipos de fluxo: vídeo MPEG-2; Áudio MPEG-2; Áudio AC3 codificado conforme definido para vídeo em DVD; ou áudio PCM codificado como definido para vídeo de DVD. Esse filtro analisa os fluxos, cria um pino de saída para cada fluxo e gera os pacotes de áudio ou vídeo MPEG compactados em um filtro de decodificador MPEG-2.

Para fluxos de programas e transporte entregues no modo Push, use o [demultiplexador MPEG-2](mpeg-2-demultiplexer.md)em todas as plataformas.

> [!Note]  
> O divisor MPEG-2 não dá suporte à busca com precisão de quadro.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filtrar interfaces</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de entrada</td>
<td><ul>
<li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</li>
<li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</li>
<li>MEDIATYPE_Stream, MEDIASUBTYPE_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia do pino de saída</td>
<td>Depende do tipo de fluxo. Consulte <a href="mpeg-2-splitter-media-types.md">tipos de mídia de divisor MPEG-2</a></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de saída</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></td>
</tr>
<tr class="even">
<td>CLSID do filtro</td>
<td>CLSID_MMSPLITTER</td>
</tr>
<tr class="odd">
<td>CLSID de página de propriedades</td>
<td>Não aplicável</td>
</tr>
<tr class="even">
<td>Executável</td>
<td>mpg2splt.ax</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Núcleo</a></td>
<td>MERIT_NORMAL + 1</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria do filtro</a></td>
<td>CLSID_AudioInputDeviceCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> <dt>

[Usando o divisor MPEG-2](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



