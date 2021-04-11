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
ms.openlocfilehash: aa9b6c842ff7acd874e8e467d07c31e298a63564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170904"
---
# <a name="query-schema"></a>Esquema de consulta

O esquema de consulta define os seguintes elementos e tipos que você pode usar para escrever uma consulta XML estruturada para recuperar eventos de um canal ou arquivo de log:

-   [Elementos QuerySchema](queryschema-elements.md)
-   [Tipos complexos QuerySchema](queryschema-complex-types.md)

A seção elementos contém os nomes dos elementos que você usa em sua consulta; no entanto, para obter os detalhes de cada elemento, consulte o tipo complexo que contém o elemento.

Uma consulta pode conter uma ou mais expressões XPath que são usadas para incluir ou excluir o evento no conjunto de resultados da consulta. Você pode consultar eventos de vários canais ou arquivos de log, mas não pode misturar canais e arquivos de log. Você pode usar uma consulta em qualquer função que usa um XPath (por exemplo, as funções [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) ou [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) ). Cada XPath especificado é limitado a 32 expressões. Para obter um exemplo, consulte [consumindo eventos](consuming-events.md).

O SDK do Windows inclui o esquema no \\ arquivo include \\ Query. xsd.

Além do esquema de consulta, o log de eventos do Windows também define os seguintes esquemas:

-   [Esquema EventManifest](eventmanifestschema-schema.md)— define os elementos e tipos usados para escrever um manifesto de instrumentação.
-   [Esquema de evento](eventschema-schema.md)— define os elementos e tipos usados para renderizar um evento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Consumindo eventos](consuming-events.md)
</dt> </dl>

 

 




