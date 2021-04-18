---
title: Esquema EventManifest
ms.assetid: 89acbc43-739b-4e89-a96a-cc3438ec8ecc
description: 'Saiba mais sobre: esquema EventManifest'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 67e1c2e9b769cd26e81a71853037655220a27d1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788816"
---
# <a name="eventmanifest-schema"></a>Esquema EventManifest

O esquema EventManifest define os seguintes elementos e tipos que você usa para escrever um manifesto de instrumentação:

-   [Elementos EventManifestSchema](eventmanifestschema-elements.md)
-   [Tipos simples de EventManifestSchema](eventmanifestschema-simple-types.md)
-   [Tipos complexos EventManifestSchema](eventmanifestschema-complex-types.md)

A seção elementos contém os nomes dos elementos que você usa em seu manifesto; no entanto, para obter os detalhes de cada elemento, consulte o tipo complexo que contém o elemento.

Um manifesto de instrumentação é um arquivo XML que define um provedor de eventos, os canais nos quais os eventos são gravados, os próprios eventos, os critérios de filtragem de eventos, como níveis, tarefas e opcodes, e as cadeias de caracteres localizadas usadas ao renderizar os eventos. A Convenção é usar. Man como a extensão para arquivos de manifesto. Para obter detalhes sobre como escrever um manifesto, consulte [escrevendo um manifesto de instrumentação](writing-an-instrumentation-manifest.md).

O SDK do Windows inclui o esquema no \\ arquivo de \\ evento. xsd de inclusão. Você pode usar o XSD para validar seu manifesto.

Além do esquema EventManifest, o log de eventos do Windows também define os seguintes esquemas:

-   [Esquema de evento](eventschema-schema.md)— define os elementos e tipos usados para renderizar um evento.
-   [Esquema de consulta](queryschema-schema.md)— define os elementos e tipos usados para gravar uma consulta para recuperar eventos de um ou mais canais.

 

 




