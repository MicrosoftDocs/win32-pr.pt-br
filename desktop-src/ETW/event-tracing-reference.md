---
description: Lista os elementos usados com o rastreamento de eventos.
ms.assetid: 8cb5907e-9006-45d1-9d48-13a43a631664
title: Referência de rastreamento de eventos
ms.topic: article
ms.date: 01/30/2020
ms.openlocfilehash: 7e0ee4576b9b9d64a5766c6ab096ea34abc2b176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968156"
---
# <a name="event-tracing-reference"></a>Referência de rastreamento de eventos

Você usa os seguintes elementos de programação para escrever aplicativos que incorporam o rastreamento de eventos:

-   [Enumerações de rastreamento de eventos](/windows/desktop/api/_etw/#enumerations)
-   [Funções de rastreamento de eventos](/windows/desktop/api/_etw/#functions)
-   [Interfaces de rastreamento de eventos](/windows/desktop/api/_etw/#interfaces)
-   [Estruturas de rastreamento de eventos](/windows/desktop/api/_etw/#structures)
-   [Constantes de rastreamento de eventos](event-tracing-constants.md)

Para obter detalhes sobre exemplos que usam esses elementos de programação, consulte [exemplos de rastreamento de eventos](event-tracing-samples.md).

Esta seção também contém informações sobre:

-   [Ferramentas](event-tracing-tools.md) fornecidas pelo ETW
-   [Definições de classe MOF](event-tracing-mof-classes.md) para eventos de kernel
-   [Qualificadores de classe MOF](event-tracing-mof-qualifiers.md) usados ao definir suas classes de evento

## <a name="process-etw-traces-in-net-code"></a>Processar rastreamentos ETW no código .NET

Você também pode usar a [API do .net TraceProcessing](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) para analisar rastreamentos ETW para seus aplicativos e outros componentes de software. Essa API é usada internamente na Microsoft para analisar dados de ETW produzidos pelo sistema de engenharia do Windows e também é usada para alimentar várias tabelas no [analisador de desempenho do Windows](/windows-hardware/test/wpt/windows-performance-analyzer). Essa API está disponível como um pacote NuGet.

Para obter mais informações, consulte [este artigo](/windows/apps/trace-processing/overview).
