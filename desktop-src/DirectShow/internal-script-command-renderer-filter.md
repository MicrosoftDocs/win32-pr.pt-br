---
description: Filtro de processador de comandos de script interno
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: Filtro de processador de comandos de script interno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b241643d991e9348015dc51ea5b2f1c4875f079d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500436"
---
# <a name="internal-script-command-renderer-filter"></a>Filtro de processador de comandos de script interno

Recebe comandos de script e os envia para o aplicativo.

Esse filtro aceita comandos de script em um dos dois formatos:

-   Texto de MEDIATYPE \_ : cada amostra de mídia contém uma cadeia de caracteres de texto ANSI.
-   MEDIATYPE \_ ScriptCommand: cada amostra de mídia contém duas cadeias de caracteres Unicode terminadas em nulo, concatenadas juntas. A primeira cadeia de caracteres descreve o tipo de comando e a segunda cadeia de caracteres é o comando de script.

    Quando o filtro recebe um exemplo, ele envia uma notificação de evento de [**\_ \_ evento OLE do EC**](ec-ole-event.md) . O primeiro parâmetro de evento é um **BSTR** com o tipo de comando, ou `Text` se o formato for texto de MediaType \_ . O segundo parâmetro de evento é um **BSTR** com o comando de script. O aplicativo pode recuperar o evento e responder ao comando de script.

Para obter um exemplo de como usar esse filtro, consulte [Sami (CC) Parser](sami--cc--parser-filter.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filtrar interfaces</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de entrada</td>
<td><ul>
<li>MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</li>
<li>MEDIATYPE_Text, MEDIASUBTYPE_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia do pino de saída</td>
<td>Não aplicável</td>
</tr>
<tr class="odd">
<td>Interfaces de pino de saída</td>
<td>Não aplicável</td>
</tr>
<tr class="even">
<td>CLSID do filtro</td>
<td>{48025243-2D39-11CE-875D-00608CB78066}</td>
</tr>
<tr class="odd">
<td>CLSID de página de propriedades</td>
<td>Nenhuma página de propriedades</td>
</tr>
<tr class="even">
<td>Executável</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Núcleo</a></td>
<td>MERIT_PREFERRED + 1</td>
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

 

 



