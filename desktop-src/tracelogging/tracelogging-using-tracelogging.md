---
title: Usando TraceLogging
description: Os tópicos a seguir fornecem um início rápido do TraceLogging para código nativo e gerenciado, com exemplos.
ms.assetid: CEC57517-7A0E-45AA-85F7-F358AE51EF4A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be48ff03e1efe37b2ed18314557514c81715ea7e36dacfda309f473522dac39a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966485"
---
# <a name="using-tracelogging"></a>Usando TraceLogging

Os tópicos a seguir fornecem um início rápido do TraceLogging para código nativo e gerenciado, com exemplos.

## <a name="prerequisites"></a>Pré-requisitos

-   Windows 10 O SDK (Software Development Kit) é necessário para gravar um provedor de modo de usuário
-   Windows O kit de driver (WDK) é necessário para gravar um provedor de modo kernel

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TraceLogging C/C++ Início Rápido](tracelogging-native-quick-start.md)<br/>                             | A seção a seguir descreve as etapas básicas necessárias para adicionar o TraceLogging ao código nativo do modo de usuário. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Início Rápido gerenciados TraceLogging](tracelogging-managed-quick-start.md)<br/>                          | A seção a seguir descreve as etapas básicas necessárias para adicionar o TraceLogging ao código gerenciado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [Registrar e exibir eventos de TraceLogging](tracelogging-record-and-display-tracelogging-events.md)<br/> | registre eventos TraceLogging com o gravador de desempenho de Windows (WPR) e exiba-os com o analisador de desempenho de Windows (WPA).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [Exemplos de Tracelogging C/C++](tracelogging-c-cpp-tracelogging-examples.md)<br/>                       | Este tópico contém exemplos de Tracelogging C/C++.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [Exemplos do .NET Tracelogging](tracelogging-net-examples.md)<br/>                                       | Este tópico contém um exemplo de código gerenciado Tracelogging que ilustra como registrar um evento somente quando o nível de detalhes da sessão é detalhado e como registrar em log dados de eventos estruturados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [exemplo de log de Plataforma Universal do Windows](universal-windows-platform-logging-examples.md)<br/>     | Este exemplo mostra como usar as APIs de log no Windows. Namespace Foundation. Diagnostics, incluindo LoggingChannel, LoggingActivity, LoggingSession e FileLoggingSession. essas classes são projetadas para o log de diagnóstico em um aplicativo Windows. Essas APIs foram adicionadas em Windows 8.1. <br/> as APIs LoggingChannel e LoggingActivity foram estendidas em Windows 10 para dar suporte à escrita de eventos complexos usando a codificação de eventos TraceLogging.<br/> o exemplo de log de Plataforma Universal do Windows pode ser baixado de [GitHub](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/Logging).<br/> |



 

Exemplos de TraceLogging.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[TraceLogging para drivers e componentes do modo kernel](/windows-hardware/drivers/devtest/tracelogging-for-kernel-mode-drivers-and-components)
</dt> </dl>

 

