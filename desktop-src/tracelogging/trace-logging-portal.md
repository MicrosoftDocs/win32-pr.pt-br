---
title: TraceLogging
description: .
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975c2f70cc645cc04d6b1461e32bb3b899097d1c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103642686"
---
# <a name="tracelogging"></a>TraceLogging

## <a name="purpose"></a>Finalidade

TraceLogging é a nova estrutura de rastreamento de eventos do Windows 10 para aplicativos de modo de usuário e drivers de modo kernel. O TraceLogging se baseia no ETW (rastreamento de eventos para Windows) e fornece uma maneira simplificada de instrumentar o código.

## <a name="in-this-section"></a>Nesta seção



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="trace-logging-about.md">Sobre o TraceLogging</a><br/></td>
<td>TraceLogging é o novo rastreamento de eventos do Windows 10 para aplicativos de modo de usuário e drivers de modo kernel. TraceLogging é um formato para o ETW (rastreamento de eventos autodescritivo para Windows). O TraceLogging se baseia no ETW (rastreamento de eventos para Windows) e fornece uma maneira simplificada de instrumentar o código.<br/></td>
</tr>
<tr class="even">
<td><a href="tracelogging-using-tracelogging.md">Usando TraceLogging</a><br/></td>
<td>Os tópicos a seguir fornecem um início rápido do TraceLogging para código nativo e gerenciado, com exemplos.<br/></td>
</tr>
<tr class="odd">
<td><a href="trace-logging-reference.md">Referência de TraceLogging</a><br/></td>
<td>Os tópicos a seguir fornecem informações sobre a API nativa do TraceLogging.<br/> O TraceLogging se baseia no ETW (rastreamento de eventos para Windows) e fornece uma maneira simplificada de instrumentar o código. O TraceLogging permite incluir dados estruturados com eventos, correlacionar eventos e não requer um arquivo XML de manifesto de instrumentação separado.<br/> <span class="underline">Para desenvolvedores do WinRT</span><br/>
<ul>
<li>O <a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> foi estendido no Windows 10 para registrar eventos de ETW (rastreamento de eventos do Windows) autodescritivos sem a necessidade de um manifesto.</li>
<li>O <a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> foi estendido no Windows 10 para fornecer métodos de início e parada de atividade que fornecem controle sobre o formato e o conteúdo dos eventos de iniciar e parar. Além disso, as atividades podem ser aninhadas.</li>
</ul>
<span class="underline">Para desenvolvedores de código gerenciado (Microsoft .NET Framework)</span><br/>
<ul>
<li>A classe <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource</a> fornecida com versões anteriores do .NET Framework já oferece suporte à gravação de eventos ETW sem a necessidade de um manifesto. No entanto, os desenvolvedores eram obrigados a usar EventSource como uma classe base e adicionar atributos e métodos à classe derivada que foram transformados em um manifesto ETW automaticamente. Agora, os desenvolvedores não precisam derivar de EventSource e, em vez disso, podem usar a EventSource diretamente para registrar eventos autodescritivos que não exigem um manifesto.</li>
</ul>
<span class="underline">Para desenvolvedores de C/C++</span><br/>
<ul>
<li>TraceLoggingProvider. h é a API recomendada para desenvolvedores de C/C++ no modo de usuário ou kernel. Essa API não é adequada para uso em cenários dinâmicos (com script), como JavaScript. Os links a seguir descrevem a API C/C++.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="developer-audience"></a>Público de desenvolvedores

O TraceLogging foi projetado para ser usado por desenvolvedores de aplicativos no modo de usuário e por desenvolvedores de driver de modo kernel que desejam adicionar rastreamento ao seu código.

