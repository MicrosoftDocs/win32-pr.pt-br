---
title: TraceLogging
description: TraceLogging
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d20f14980646680e0f6a0418470416801240ca17
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473112"
---
# <a name="tracelogging"></a>TraceLogging

## <a name="purpose"></a>Finalidade

TraceLogging é a nova Windows 10 de rastreamento de eventos para aplicativos de modo de usuário e drivers de modo kernel. TraceLogging se baseia no ETW (Rastreamento de Windows) e fornece uma maneira simplificada de instrumentar o código.

## <a name="in-this-section"></a>Nesta seção




| Tópico | Descrição | 
|-------|-------------|
| <a href="trace-logging-about.md">Sobre TraceLogging</a><br /> | TraceLogging é a nova Windows 10 de eventos para aplicativos de modo de usuário e drivers de modo kernel. TraceLogging é um formato para descrição de rastreamento de eventos para Windows (ETW). TraceLogging se baseia no ETW (Rastreamento de Windows) e fornece uma maneira simplificada de instrumentar o código.<br /> | 
| <a href="tracelogging-using-tracelogging.md">Usando TraceLogging</a><br /> | Os tópicos a seguir fornecem um início rápido traceLogging para código nativo e gerenciado, com exemplos.<br /> | 
| <a href="trace-logging-reference.md">Referência de TraceLogging</a><br /> | Os tópicos a seguir fornecem informações sobre a API de TraceLogging nativa.<br /> TraceLogging se baseia no ETW (Rastreamento de Windows) e fornece uma maneira simplificada de instrumentar o código. TraceLogging permite incluir dados estruturados com eventos, correlacionar eventos e não requer um arquivo XML de manifesto de instrumentação separado.<br /><span class="underline">Para desenvolvedores do WinRT</span><br /><ul><li><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> foi estendido em Windows 10 para registrar eventos ETW (Rastreamento de Eventos para Windows) sem a necessidade de um manifesto.</li><li><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> foi estendida em Windows 10 para fornecer métodos de início e parada de atividade que fornecem controle sobre o formato e o conteúdo dos eventos Iniciar e Parar. Além disso, as atividades podem ser aninhadas.</li></ul><span class="underline">Para desenvolvedores de código gerenciado (Microsoft .NET Framework)</span><br /><ul><li>A <a href="/dotnet/api/system.diagnostics.tracing.eventsource">classe EventSource</a> que acompanha as versões anteriores do .NET Framework já dá suporte à escrita de eventos ETW sem a necessidade de um manifesto. No entanto, os desenvolvedores precisaram usar EventSource como uma classe base e adicionar atributos e métodos à classe derivada que foram transformados em um manifesto ETW automaticamente. Agora, os desenvolvedores não precisam derivar de EventSource e, em vez disso, podem usar EventSource diretamente para registrar eventos autodescretos que não exigem um manifesto.</li></ul><span class="underline">Para desenvolvedores C/C++</span><br /><ul><li>TraceLoggingProvider.h é a API recomendada para desenvolvedores C/C++ no modo de usuário ou kernel. Essa API não é adequada para uso em cenários dinâmicos (com script), como Javascript. Os links a seguir descrevem a API do C/C++.</li></ul> | 




 

## <a name="developer-audience"></a>Público de desenvolvedores

TraceLogging foi projetado para uso por desenvolvedores de aplicativos no modo de usuário e desenvolvedores de driver no modo kernel que querem adicionar rastreamento ao código.

