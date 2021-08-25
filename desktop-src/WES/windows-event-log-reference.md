---
title: Windows Referência do Log de Eventos
description: A seguir estão os elementos de programação que você usa para criar um manifesto de instrumentação, criar recursos do manifesto que seu provedor usa, obter metadados de instrumentação em tempo de executar e consultar eventos de canais e arquivos de log
ms.assetid: 7af07a43-62f6-412f-9f67-46ad08922daf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6ce52f3756b8f33ac710e189677de053dc538339d0a0cdeb335410dd76a171
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957786"
---
# <a name="windows-event-log-reference"></a>Windows Referência do Log de Eventos

A seguir estão os elementos de programação que você usa para criar um manifesto de instrumentação, criar recursos do manifesto que seu provedor usa, obter metadados de instrumentação em tempo de executar e consultar eventos de canais e arquivos de log:

-   [Esquema EventManifest](eventmanifestschema-schema.md)
-   [Esquema de evento](eventschema-schema.md)
-   [Esquema de consulta](queryschema-schema.md)
-   [Windows Constantes do log de eventos](windows-event-log-constants.md)
-   [Windows Tipos de dados do log de eventos](windows-event-log-data-types.md)
-   [Windows Enumerações do Log de Eventos](windows-event-log-enumerations.md)
-   [Windows Funções de log de eventos](windows-event-log-functions.md)
-   [Windows Estruturas de log de eventos](windows-event-log-structures.md)
-   [Windows Ferramentas de Log de Eventos](windows-event-log-tools.md)

Para aplicativos escritos usando uma linguagem .NET, como C# ou Visual Basic, consulte os seguintes namespaces:

-   Para gravar eventos, use as classes e métodos definidos no namespace [System.Diagnostics.Eventing.](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8)
-   Para consumir eventos de um canal ou log Windows Log de Eventos, use as classes e métodos definidos no namespace [System.Diagnostics.Eventing.Reader.](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true)

Como alternativa ao uso do namespace [System.Diagnostics.Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) para gravar eventos, você pode usar o argumento **-cs** ou **-css** para fazer com que o compilador de mensagem gere o código para gravar os eventos. Para obter detalhes, consulte [**Compilador de mensagens**](message-compiler--mc-exe-.md).
