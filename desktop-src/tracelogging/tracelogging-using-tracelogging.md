---
title: Usando TraceLogging
description: Os tópicos a seguir fornecem um início rápido do TraceLogging para código nativo e gerenciado, com exemplos.
ms.assetid: CEC57517-7A0E-45AA-85F7-F358AE51EF4A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e331f5ebec3d7eb8ce9c50d3e9d92f747bf76414
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366634"
---
# <a name="using-tracelogging"></a>Usando TraceLogging

Os tópicos a seguir fornecem um início rápido do TraceLogging para código nativo e gerenciado, com exemplos.

## <a name="prerequisites"></a>Pré-requisitos

-   O SDK (Software Development Kit) do Windows 10 é necessário para gravar um provedor de modo de usuário
-   O WDK (Kit de driver do Windows) é necessário para gravar um provedor de modo kernel

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TraceLogging C/C++ Início Rápido](tracelogging-native-quick-start.md)<br/>                             | A seção a seguir descreve as etapas básicas necessárias para adicionar o TraceLogging ao código nativo do modo de usuário. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Início Rápido gerenciados TraceLogging](tracelogging-managed-quick-start.md)<br/>                          | A seção a seguir descreve as etapas básicas necessárias para adicionar o TraceLogging ao código gerenciado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [Registrar e exibir eventos de TraceLogging](tracelogging-record-and-display-tracelogging-events.md)<br/> | Registre eventos do TraceLogging com o gravador de desempenho do Windows (WPR) e exiba-os com o Windows Performance Analyzer (WPA).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [Exemplos de Tracelogging C/C++](tracelogging-c-cpp-tracelogging-examples.md)<br/>                       | Este tópico contém exemplos de Tracelogging C/C++.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [Exemplos do .NET Tracelogging](tracelogging-net-examples.md)<br/>                                       | Este tópico contém um exemplo de código gerenciado Tracelogging que ilustra como registrar um evento somente quando o nível de detalhes da sessão é detalhado e como registrar em log dados de eventos estruturados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [Exemplo de log de Plataforma Universal do Windows](universal-windows-platform-logging-examples.md)<br/>     | Este exemplo mostra como usar as APIs de log no namespace Windows. Foundation. Diagnostics, incluindo LoggingChannel, LoggingActivity, LoggingSession e FileLoggingSession. Essas classes são projetadas para o log de diagnóstico em um aplicativo do Windows. Essas APIs foram adicionadas em Windows 8.1. <br/> As APIs LoggingChannel e LoggingActivity foram estendidas no Windows 10 para dar suporte à escrita de eventos complexos usando a codificação de eventos TraceLogging.<br/> O exemplo de log de Plataforma Universal do Windows pode ser baixado do [GitHub](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/Logging).<br/> |



 

Exemplos de TraceLogging.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[TraceLogging para drivers e componentes do modo kernel](/windows-hardware/drivers/devtest/tracelogging-for-kernel-mode-drivers-and-components)
</dt> </dl>

 

