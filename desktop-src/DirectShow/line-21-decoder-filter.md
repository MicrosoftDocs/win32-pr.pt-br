---
description: Filtro de decodificador de linha 21
ms.assetid: 48fa5484-1f8c-4133-b2e1-888cb1834402
title: Filtro de decodificador de linha 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839a6ff8e77f4815b74f5de65b8f0e2a565cdc2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105775556"
---
# <a name="line-21-decoder-filter"></a>Filtro de decodificador de linha 21

Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

Este filtro de decodificador de linha 21 decodifica os dados da linha 21 e desenha o texto da legenda em bitmaps.

O pino de entrada conecta-se a qualquer linha de 21 provedor de dados, normalmente um decodificador de vídeo DVD ou o filtro de [decodificador de CC](cc-decoder-filter.md) . O decodificador de CC fornece dados de linha 21 do VBI de um sinal de televisão analógica. O pino de saída se conecta a um pin secundário no [mixer de sobreposição](overlay-mixer-filter.md) ou a outro processador de vídeo, como o VMR.

Esse filtro aceita dados de linha 21 no formato de par de bytes padrão ou, para DVD, como um pacote para todo o grupo de imagens (GOP). Para cada GOP no fluxo de vídeo do DVD, pode haver um pacote de dados do usuário que tenha as informações de cabeçalho de GOP específicas e os dados da linha 21. O formato dos pares de bytes é definido no padrão EIA/CEA-608-B; Veja esse padrão para obter mais informações.

Duas versões deste filtro estão disponíveis:



| Filtrar            | CLSID                 |
|-------------------|-----------------------|
| Decodificador de linha 21   | \_LINE21DECODER CLSID  |
| Linha 21 Decoder 2 | \_LINE21DECODER2 CLSID |



 

O filtro da versão 1 é usado nas plataformas Microsoft® Windows® 95/98/me e Windows 2000. O filtro versão 2 está disponível no Microsoft Windows XP e versões posteriores e é usado sempre que o processador de mixagem de vídeo estiver no grafo.

As informações na tabela a seguir se aplicam a ambas as versões do filtro:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filtrar interfaces</td>
<td><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de entrada</td>
<td>Tipo principal: MEDIATYPE_AUXLine21DataSubtype:<br/>
<ul>
<li>MEDIASUBTYPE_Line21_BytePair (linha padrão 21)</li>
<li>MEDIASUBTYPE_Line21_GOPPacket (linha de DVD 21)</li>
</ul>
Tipo de formato: FORMAT_VideoInfo ou GUID_NULL<br/></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia do pino de saída</td>
<td>Tipo principal: MEDIATYPE_VideoSubtype:<br/>
<ul>
<li>MEDIASUBTYPE_RGB8</li>
<li>MEDIASUBTYPE_RGB555</li>
<li>MEDIASUBTYPE_RGB565</li>
<li>MEDIASUBTYPE_RGB24</li>
<li>MEDIASUBTYPE_RGB32</li>
</ul>
Tipo de formato: FORMAT_VideoInfo<br/></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de saída</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID do filtro</td>
<td>Consulte a tabela anterior</td>
</tr>
<tr class="odd">
<td>CLSID de página de propriedades</td>
<td>Nenhum</td>
</tr>
<tr class="even">
<td>Executável</td>
<td>qdvd.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Núcleo</a></td>
<td>Decodificador de linha 21: MERIT_NORMALLine 21 Decoder 2: MERIT_NORMAL + 2<br/></td>
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
</dt> <dt>

[Legendas e teletextos codificados](closed-captions-and-teletext.md)
</dt> <dt>

[Configuração de grafo de filtro de DVD](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




