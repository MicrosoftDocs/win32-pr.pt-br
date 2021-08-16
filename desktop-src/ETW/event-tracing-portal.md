---
description: Esta documentação é para aplicativos de modo de usuário que querem usar o ETW. Para obter informações sobre como instrumentar drivers de dispositivo executados no modo kernel, consulte WPP Software Tracing and Adding Event Tracing to Kernel-Mode Drivers in the Windows Driver Kit (WDK).
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

O ETW (Rastreamento de Eventos para Windows) fornece aos programadores de aplicativos a capacidade de iniciar e parar sessões de rastreamento de eventos, instrumentar um aplicativo para fornecer eventos de rastreamento e consumir eventos de rastreamento. Os eventos de rastreamento contêm um header de evento e dados definidos pelo provedor que descrevem o estado atual de um aplicativo ou operação. Você pode usar os eventos para depurar um aplicativo e executar a análise de capacidade e desempenho.

Esta documentação é para aplicativos de modo de usuário que querem usar o ETW. Para obter informações sobre como instrumentar drivers de dispositivo executados no modo kernel, consulte [WPP Software Tracing](/windows-hardware/drivers/devtest/wpp-software-tracing) and [Adding Event Tracing to Kernel-Mode Drivers](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) in the Windows Driver Kit (WDK).

## <a name="where-applicable"></a>Quando aplicável

Use ETW quando quiser instrumentar seu aplicativo, registrar eventos de usuário ou kernel em um arquivo de log e consumir eventos de um arquivo de log ou em tempo real.

## <a name="developer-audience"></a>Público de desenvolvedores

O ETW foi projetado para desenvolvedores C e C++ que escrevem aplicativos no modo de usuário.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O ETW está incluído no Microsoft Windows 2000 e posterior. Para obter informações sobre quais sistemas operacionais são necessários para usar uma função específica, consulte a seção Requisitos da documentação da função.

## <a name="process-etw-traces-in-net-code"></a>Processar rastreamentos ETW no código .NET

Você pode usar a [API de TraceProcessing](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) do .NET para analisar rastreamentos ETW para seus aplicativos e outros componentes de software. Essa API é usada internamente na Microsoft para analisar dados ETW produzidos pelo sistema de engenharia Windows e também é usado para a energia de várias tabelas [no Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer). Essa API está disponível como um NuGet pacote.

Para obter mais informações, consulte [este artigo](/windows/apps/trace-processing/overview).

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                     | Descrição                                                                        |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Novidades no rastreamento de eventos](what-s-new-in-event-tracing.md)<br/> | Novos recursos que foram adicionados ao Rastreamento de Eventos em cada versão.<br/>          |
| [Sobre o rastreamento de eventos](about-event-tracing.md)<br/>                 | Informações gerais sobre o Rastreamento de Eventos.<br/>                                |
| [Usando o rastreamento de eventos](using-event-tracing.md)<br/>                 | Tópicos relacionados a tarefas que descrevem como usar a API etw.<br/>               |
| [Referência de rastreamento de eventos](event-tracing-reference.md)<br/>         | Descrições detalhadas de funções ETW e outros elementos de programação. <br/> |



 

 

 
