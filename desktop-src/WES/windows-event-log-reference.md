---
title: Referência do log de eventos do Windows
description: A seguir estão os elementos de programação que você usa para criar um manifesto de instrumentação, criar recursos do manifesto que seu provedor usa, obter metadados de instrumentação em tempo de execução e consultar eventos de canais e arquivos de log
ms.assetid: 7af07a43-62f6-412f-9f67-46ad08922daf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fef1af82cdab1ab92b4ea4768479541053fe65d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010125"
---
# <a name="windows-event-log-reference"></a>Referência do log de eventos do Windows

A seguir estão os elementos de programação que você usa para criar um manifesto de instrumentação, criar recursos do manifesto que seu provedor usa, obter metadados de instrumentação em tempo de execução e consultar eventos de canais e arquivos de log:

-   [Esquema EventManifest](eventmanifestschema-schema.md)
-   [Esquema de evento](eventschema-schema.md)
-   [Esquema de consulta](queryschema-schema.md)
-   [Constantes do log de eventos do Windows](windows-event-log-constants.md)
-   [Tipos de dados de log de eventos do Windows](windows-event-log-data-types.md)
-   [Enumerações de log de eventos do Windows](windows-event-log-enumerations.md)
-   [Funções de log de eventos do Windows](windows-event-log-functions.md)
-   [Estruturas de log de eventos do Windows](windows-event-log-structures.md)
-   [Ferramentas de log de eventos do Windows](windows-event-log-tools.md)

Para aplicativos escritos usando uma linguagem .NET, como C# ou Visual Basic, consulte os seguintes namespaces:

-   Para gravar eventos, use as classes e os métodos definidos no namespace [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) .
-   Para consumir eventos de um canal ou log de log de eventos do Windows, use as classes e os métodos definidos no namespace [System. Diagnostics. Eventing. Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) .

Como alternativa ao uso do namespace [System. Diagnostics.](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) informativo para gravar eventos, você pode usar o argumento **-cs** ou **-CSS** para que o compilador de mensagens gere o código para gravar os eventos. Para obter detalhes, consulte [**compilador de mensagem**](message-compiler--mc-exe-.md).
