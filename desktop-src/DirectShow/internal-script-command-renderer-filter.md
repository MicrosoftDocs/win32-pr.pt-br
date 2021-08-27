---
description: Filtro de processador de comandos de script interno
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: Filtro de processador de comandos de script interno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b70fbcd7dc6347ec93a19558ef2306dffd5fb64
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982209"
---
# <a name="internal-script-command-renderer-filter"></a>Filtro de processador de comandos de script interno

Recebe comandos de script e os envia para o aplicativo.

Esse filtro aceita comandos de script em um dos dois formatos:

-   Texto de MEDIATYPE \_ : cada amostra de mídia contém uma cadeia de caracteres de texto ANSI.
-   MEDIATYPE \_ ScriptCommand: cada amostra de mídia contém duas cadeias de caracteres Unicode terminadas em nulo, concatenadas juntas. A primeira cadeia de caracteres descreve o tipo de comando e a segunda cadeia de caracteres é o comando de script.

    Quando o filtro recebe um exemplo, ele envia uma notificação de evento de [**\_ \_ evento OLE do EC**](ec-ole-event.md) . O primeiro parâmetro de evento é um **BSTR** com o tipo de comando, ou `Text` se o formato for texto de MediaType \_ . O segundo parâmetro de evento é um **BSTR** com o comando de script. O aplicativo pode recuperar o evento e responder ao comando de script.

Para obter um exemplo de como usar esse filtro, consulte [Sami (CC) Parser](sami--cc--parser-filter.md).




| Rótulo | Valor |
|--------|-------|
| Filtrar interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a> | 
| Tipos de mídia de pino de entrada | <ul><li>MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</li><li>MEDIATYPE_Text, MEDIASUBTYPE_NULL</li></ul> | 
| Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipos de mídia do pino de saída | Não Aplicável | 
| Interfaces de pino de saída | Não Aplicável | 
| CLSID do filtro | {48025243-2D39-11CE-875D-00608CB78066} | 
| CLSID de página de propriedades | Nenhuma página de propriedades | 
| Executável | Quartz.dll | 
| <a href="merit.md">Núcleo</a> | MERIT_PREFERRED + 1 | 
| <a href="filter-categories.md">Categoria do filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> </dl>

 

 



