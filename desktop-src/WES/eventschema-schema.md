---
title: Esquema do evento
ms.assetid: 36037697-b777-4e5c-99af-77964200a3e4
description: 'Saiba mais sobre: esquema de evento'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bfb26f6c71d544e0c0a6a4d833b40a5d15ae5485
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828319"
---
# <a name="event-schema"></a>Esquema do evento

O esquema de evento define os seguintes elementos e tipos que identificam os elementos e atributos de um evento registrado:

-   [Elementos EventSchema](eventschema-elements.md)
-   [Tipos simples de EventSchema](eventschema-simple-types.md)
-   [Tipos complexos EventSchema](eventschema-complex-types.md)

A seção Elements contém os nomes dos elementos que você encontraria em eventos registrados; no entanto, para obter os detalhes de cada elemento, consulte o tipo complexo que contém o elemento.

O SDK do Windows inclui o esquema no \\ arquivo include \\ Event. xsd.

Você pode usar esse esquema para identificar os elementos e atributos ao chamar a função [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) para renderizar seções ou propriedades específicas do evento. Para obter um exemplo que mostra como usar esse esquema ao renderizar eventos, consulte [renderizando eventos](rendering-events.md).

Além do esquema de evento, o log de eventos do Windows também define os seguintes esquemas:

-   [Esquema EventManifest](eventmanifestschema-schema.md)— define os elementos e tipos usados para escrever um manifesto de instrumentação.
-   [Esquema de consulta](queryschema-schema.md)— define os elementos e tipos usados para gravar uma consulta para recuperar eventos de um ou mais canais.

 

 




