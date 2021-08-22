---
description: Esta documentação é para aplicativos de modo de usuário que desejam usar o ETW. para obter informações sobre como instrumentar drivers de dispositivo executados no modo kernel, consulte rastreamento de Software do WPP e adicionando o rastreamento de eventos a drivers de Kernel-Mode no WDK (Windows Driver Kit).
ms.assetid: 3de69436-671b-46a2-8d92-4eb3af2a4233
title: Rastreamento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 908e935d48749d80e5b2cfe237efeed5413c839157e53b489f4857c0349b4a1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070216"
---
# <a name="event-tracing"></a>Rastreamento de eventos

## <a name="purpose"></a>Finalidade

o rastreamento de eventos para Windows (ETW) fornece aos programadores de aplicativos a capacidade de iniciar e parar sessões de rastreamento de eventos, instrumentar um aplicativo para fornecer eventos de rastreamento e consumir eventos de rastreamento. Os eventos de rastreamento contêm um cabeçalho de evento e dados definidos pelo provedor que descrevem o estado atual de um aplicativo ou operação. Você pode usar os eventos para depurar um aplicativo e executar a análise de capacidade e desempenho.

Esta documentação é para aplicativos de modo de usuário que desejam usar o ETW. para obter informações sobre como instrumentar drivers de dispositivo executados no modo kernel, consulte [rastreamento de Software do WPP](/windows-hardware/drivers/devtest/wpp-software-tracing) e adicionando o [rastreamento de eventos a drivers de Kernel-Mode](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) no WDK (Windows Driver Kit).

## <a name="where-applicable"></a>Quando aplicável

Use o ETW quando desejar instrumentar seu aplicativo, registrar eventos de usuário ou kernel em um arquivo de log e consumir eventos de um arquivo de log ou em tempo real.

## <a name="developer-audience"></a>Público de desenvolvedores

O ETW foi projetado para desenvolvedores de C e C++ que escrevem aplicativos de modo de usuário.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

o ETW está incluído no Microsoft Windows 2000 e posterior. Para obter informações sobre quais sistemas operacionais são necessários para usar uma função específica, consulte a seção requisitos da documentação da função.

## <a name="process-etw-traces-in-net-code"></a>Processar rastreamentos ETW no código .NET

Você pode usar a [API do .net TraceProcessing](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) para analisar rastreamentos ETW para seus aplicativos e outros componentes de software. essa API é usada internamente na Microsoft para analisar dados de ETW produzidos pelo sistema de engenharia de Windows e também é usada para alimentar várias tabelas no [analisador de desempenho Windows](/windows-hardware/test/wpt/windows-performance-analyzer). essa API está disponível como um pacote NuGet.

Para obter mais informações, consulte [este artigo](/windows/apps/trace-processing/overview).

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                     | Descrição                                                                        |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [O que há de novo no rastreamento de eventos](what-s-new-in-event-tracing.md)<br/> | Novos recursos que foram adicionados ao rastreamento de eventos em cada versão.<br/>          |
| [Sobre o rastreamento de eventos](about-event-tracing.md)<br/>                 | Informações gerais sobre o rastreamento de eventos.<br/>                                |
| [Usando o rastreamento de eventos](using-event-tracing.md)<br/>                 | Tópicos relacionados a tarefas que descrevem como usar a API do ETW.<br/>               |
| [Referência de rastreamento de eventos](event-tracing-reference.md)<br/>         | Descrições detalhadas de funções de ETW e outros elementos de programação. <br/> |



 

 

 
