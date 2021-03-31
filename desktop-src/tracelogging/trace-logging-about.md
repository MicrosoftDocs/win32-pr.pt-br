---
title: Sobre o TraceLogging
description: TraceLogging é o novo rastreamento de eventos do Windows 10 para aplicativos de modo de usuário e drivers de modo kernel.
ms.assetid: 8C6A9E91-98F9-4D6B-A937-A22BA7CEB1E4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c2b1ca72385a51df1e0cd82f3e91c198f15b5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823827"
---
# <a name="about-tracelogging"></a>Sobre o TraceLogging

TraceLogging é o novo rastreamento de eventos do Windows 10 para aplicativos de modo de usuário e drivers de modo kernel. TraceLogging é um formato para o ETW (rastreamento de eventos autodescritivo para Windows). O TraceLogging se baseia no ETW (rastreamento de eventos para Windows) e fornece uma maneira simplificada de instrumentar o código.

O TraceLogging oferece a simplicidade do WPP (pré-processador de rastreamento de software) do Windows com o benefício adicional de ser capaz de incluir dados estruturados com eventos, a capacidade de correlacionar eventos e todos sem a necessidade de um arquivo XML de manifesto de instrumentação separado. Os eventos são autodescritivos, o que significa que um binário contendo o manifesto de instrumentação não precisa ser registrado no sistema para usar as APIs do auxiliar de dados de rastreamento (TDH) para decodificar e mostrar eventos.

O ETW (rastreamento de eventos para Windows) foi introduzido com o Windows 2000 e atualizado no Windows Vista. O Tracelogging se baseia nas APIs do ETW do Windows Vista. Os provedores podem usar a tecnologia TraceLogging e ainda funcionar no Windows Vista. Os controladores existentes (usando o Windows VistaAPIs) podem ser usados para controlar provedores de TraceLogging.

O TraceLogging também é compatível com as ferramentas existentes. Ainda há suporte para provedores que usam o ETW baseado em manifesto. Você não precisa converter provedores ETW baseados em manifesto para provedores TraceLogging, a menos que queira aproveitar a simplicidade que o TraceLogging fornece. O rastreamento de WPP ainda tem suporte.

O TraceLogging baseia-se no ETW, mas apresenta várias melhorias importantes:

-   O rastreamento de um evento é tão simples quanto uma chamada à API.
-   Os eventos são autodescritivos e não exigem binários adicionais que contenham o manifesto de evento compilado para interpretar o evento. Todos os metadados sobre o evento são registrados no evento.
-   As atividades dentro de um único processo podem ser facilmente expressas por meio de eventos de iniciar e parar.
-   TraceLogging é compatível com o suporte de instrumentação existente. As novas APIs de ETW continuam a dar suporte aos provedores antigos. Você pode investir nas novas APIs de ETW para cenários estratégicos, deixando os pontos de instrumentação antigos como estão.
-   O TraceLogging oferece a mesma API de rastreamento de eventos para Windows 10, Xbox One e Windows 10 Mobile.
-   As APIs TraceLogging podem ser acessadas em C, C++, .NET e Windows Runtime.

## <a name="api-high-level-overview"></a>Visão geral de alto nível da API

Há três APIs TraceLogging separadas que visam públicos diferentes do desenvolvedor. Cada API foi projetada para atender a diferentes conjuntos de requisitos, conforme apropriado para o público-alvo dessa API.

Para desenvolvedores do WinRT:

-   O [**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) foi estendido no Windows 10 para registrar eventos de ETW (rastreamento de eventos do Windows) autodescritivos sem a necessidade de um manifesto.
-   O [**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) foi estendido no Windows 10 para fornecer métodos de início e parada de atividade que fornecem controle sobre o formato e o conteúdo dos eventos de iniciar e parar. Além disso, as atividades podem ser aninhadas.

Para desenvolvedores de C/C++:

-   O TraceLoggingProvider. h contém a API mais eficiente, no entanto, essa API não é adequada para uso em cenários dinâmicos (com script), como JavaScript. Essa API pode ser usada no modo de usuário e no código de modo kernel.

Para desenvolvedores de código gerenciado (Microsoft .NET Framework):

-   A classe [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) fornecida com versões anteriores do .NET Framework já tem suporte para gravar eventos ETW, gerando automaticamente o manifesto e inserindo o manifesto no fluxo de eventos. No entanto, o desenvolvedor ainda tinha de controlar o manifesto para decodificar os eventos (a menos que funcione em um cenário em que o manifesto incorporado tenha sido suportado). TraceLogging permite que o manifesto seja completamente eliminado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o rastreamento de eventos](/windows/desktop/ETW/about-event-tracing)
</dt> </dl>

 

 