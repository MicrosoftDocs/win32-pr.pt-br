---
title: Sobre TraceLogging
description: TraceLogging é a nova Windows 10 de eventos para aplicativos de modo de usuário e drivers de modo kernel.
ms.assetid: 8C6A9E91-98F9-4D6B-A937-A22BA7CEB1E4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cc38210bf4c3ed1ed0b1ebf56ca22a0597b9288fc30ae4c0231d5317465644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218385"
---
# <a name="about-tracelogging"></a>Sobre TraceLogging

TraceLogging é a nova Windows 10 de eventos para aplicativos de modo de usuário e drivers de modo kernel. TraceLogging é um formato para descrição de rastreamento de eventos para Windows (ETW). TraceLogging se baseia no ETW (Rastreamento de Windows) e fornece uma maneira simplificada de instrumentar o código.

TraceLogging oferece a simplicidade do WPP (pré-processador de rastreamento de software) do Windows com o benefício adicional de poder incluir dados estruturados com eventos, a capacidade de correlacionar eventos e tudo isso sem exigir um arquivo XML de manifesto de instrumentação separado. Os eventos são autodescrevendo, o que significa que um binário que contém o manifesto de instrumentação não precisa ser registrado no sistema para usar as APIs de TDH (Auxiliar de Dados de Rastreamento) para decodificar e mostrar eventos.

O ETW (Rastreamento de Windows) foi introduzido com o Windows 2000 e atualizado no Windows Vista. O rastreamento é construído sobre as APIs Windows ETW do Vista. Os provedores podem usar a tecnologia TraceLogging e ainda trabalhar no Windows Vista. Controladores existentes (usando Windows VistaAPIs) podem ser usados para controlar provedores TraceLogging.

TraceLogging também é compatível com ferramentas existentes. Provedores que usam ETW baseado em manifesto ainda têm suporte. Você não precisa converter provedores ETW baseados em manifesto em provedores TraceLogging, a menos que deseje aproveitar a simplicidade que TraceLogging fornece. O rastreamento WPP também ainda é suportado.

TraceLogging se baseia no ETW, mas apresenta várias melhorias importantes:

-   O rastreamento de um evento é tão simples quanto uma chamada à API.
-   Os eventos são autodescrevendo e não exigem binários adicionais que contenham o manifesto de evento compilado para interpretar o evento. Todos os metadados sobre o evento são registrados no evento.
-   As atividades dentro de um único processo podem ser expressas facilmente por meio de eventos de início e parada.
-   TraceLogging é compatível com o suporte de instrumentação existente. As novas APIs ETW continuam a dar suporte aos provedores antigos. Você pode investir nas novas APIs etw para cenários estratégicos, deixando seus pontos de instrumentação antigos como estão.
-   TraceLogging oferece a mesma API de rastreamento de eventos para Windows 10, Xbox One e Windows 10 Mobile.
-   As APIs TraceLogging podem ser acessadas em C, C++, .NET e Windows Runtime.

## <a name="api-high-level-overview"></a>Visão geral da API de alto nível

Há três APIs traceLogging separadas que se direcionam a diferentes públicos de desenvolvedores. Cada API foi projetada para atender a diferentes conjuntos de requisitos conforme apropriado para o público-alvo dessa API.

Para desenvolvedores do WinRT:

-   [**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) foi estendido em Windows 10 para registrar eventos ETW (Rastreamento de Eventos de autodescrevão) Windows sem a necessidade de um manifesto.
-   [**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) foi estendida em Windows 10 para fornecer métodos de início e parada de atividade que fornecem controle sobre o formato e o conteúdo dos eventos Iniciar e Parar. Além disso, as atividades podem ser aninhadas.

Para desenvolvedores C/C++:

-   TraceLoggingProvider.h contém a API mais eficiente, no entanto, essa API não é adequada para uso em cenários dinâmicos (com script), como Javascript. Essa API pode ser usada no modo de usuário e no código de modo kernel.

Para desenvolvedores de código gerenciado (Microsoft .NET Framework) :

-   A [classe EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) que foi enviada com versões anteriores do .NET Framework já suportava a escrita de eventos ETW , gerando automaticamente o manifesto e incorporação do manifesto no fluxo de eventos. No entanto, o desenvolvedor ainda precisava manter o controle do manifesto para decodificar os eventos (a menos que estivesse trabalhando em um cenário em que o manifesto inserido tivesse suporte). TraceLogging permite que o manifesto seja completamente eliminado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o rastreamento de eventos](/windows/desktop/ETW/about-event-tracing)
</dt> </dl>

 

 