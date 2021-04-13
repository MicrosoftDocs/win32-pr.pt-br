---
title: Referência de TraceLogging
description: Os tópicos a seguir fornecem informações sobre a API nativa do TraceLogging. O TraceLogging se baseia no ETW (rastreamento de eventos para Windows) e fornece uma maneira simplificada de instrumentar o código.
ms.assetid: 9E3F2140-DDB0-4C30-B7D0-A81F11823AA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71d81874e7aeb1a0618716b00d225d215c382ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366636"
---
# <a name="tracelogging-reference"></a>Referência de TraceLogging

Os tópicos a seguir fornecem informações sobre a API nativa do TraceLogging.

O TraceLogging se baseia no ETW (rastreamento de eventos para Windows) e fornece uma maneira simplificada de instrumentar o código. O TraceLogging permite incluir dados estruturados com eventos, correlacionar eventos e não requer um arquivo XML de manifesto de instrumentação separado.

<span class="underline">Para desenvolvedores do WinRT</span>

-   O [**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) foi estendido no Windows 10 para registrar eventos de ETW (rastreamento de eventos do Windows) autodescritivos sem a necessidade de um manifesto.
-   O [**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) foi estendido no Windows 10 para fornecer métodos de início e parada de atividade que fornecem controle sobre o formato e o conteúdo dos eventos de iniciar e parar. Além disso, as atividades podem ser aninhadas.

<span class="underline">Para desenvolvedores de código gerenciado (Microsoft .NET Framework)</span>

-   A classe [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) fornecida com versões anteriores do .NET Framework já oferece suporte à gravação de eventos ETW sem a necessidade de um manifesto. No entanto, os desenvolvedores eram obrigados a usar EventSource como uma classe base e adicionar atributos e métodos à classe derivada que foram transformados em um manifesto ETW automaticamente. Agora, os desenvolvedores não precisam derivar de EventSource e, em vez disso, podem usar a EventSource diretamente para registrar eventos autodescritivos que não exigem um manifesto.

<span class="underline">Para desenvolvedores de C/C++</span>

-   TraceLoggingProvider. h é a API recomendada para desenvolvedores de C/C++ no modo de usuário ou kernel. Essa API não é adequada para uso em cenários dinâmicos (com script), como JavaScript. Os links a seguir descrevem a API C/C++.

<!-- -->

-   [Classes](trace-logging-classes.md)
-   [Funções](trace-logging-functions.md)
-   [Macros](trace-logging-macros.md)

Observe que o valor de WINVER afetará a maneira como o TraceLoggingProvider. h se comporta.

-   Se WINVER não estiver definido antes de incluir <Windows. h>, <Windows. h> definirá WINVER como um valor padrão correspondente à versão do SDK.
-   Usando TraceLoggingProvider. h com WINVER definido como 0x0602 (Windows 8) ou superior, o programa não será executado no Windows Vista ou no Windows 7.
-   Usando TraceLoggingProvider. h com WINVER definido como 0x0600 (Windows Vista) ou 0x0601 (Windows 7), o programa será configurado para compatibilidade e funcionará nas versões especificadas do Windows.

 

 