---
title: Esquema de consulta
ms.assetid: 5710231b-5195-413e-8953-e47a411897a6
description: 'Saiba mais sobre: esquema de consulta'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 14beeaf8c4d739e490de972107fedf279e16e75b5401f63a709d43b03c338c79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005166"
---
# <a name="query-schema"></a>Esquema de consulta

O esquema de consulta define os seguintes elementos e tipos que você pode usar para escrever uma consulta XML estruturada para recuperar eventos de um canal ou arquivo de log:

-   [Elementos QuerySchema](queryschema-elements.md)
-   [Tipos complexos QuerySchema](queryschema-complex-types.md)

A seção elementos contém os nomes dos elementos que você usa em sua consulta; no entanto, para obter os detalhes de cada elemento, consulte o tipo complexo que contém o elemento.

Uma consulta pode conter uma ou mais expressões XPath que são usadas para incluir ou excluir o evento no conjunto de resultados da consulta. Você pode consultar eventos de vários canais ou arquivos de log, mas não pode misturar canais e arquivos de log. Você pode usar uma consulta em qualquer função que usa um XPath (por exemplo, as funções [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) ou [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) ). Cada XPath especificado é limitado a 32 expressões. Para obter um exemplo, consulte [consumindo eventos](consuming-events.md).

o SDK do Windows inclui o esquema no \\ arquivo Include \\ Query. xsd.

além do esquema de consulta, Windows Log de eventos também define os seguintes esquemas:

-   [Esquema EventManifest](eventmanifestschema-schema.md)— define os elementos e tipos usados para escrever um manifesto de instrumentação.
-   [Esquema de evento](eventschema-schema.md)— define os elementos e tipos usados para renderizar um evento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Consumindo eventos](consuming-events.md)
</dt> </dl>

 

 




