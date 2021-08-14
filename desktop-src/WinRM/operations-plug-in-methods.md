---
title: Métodos de plug-in de operações
description: Métodos de plug-in de operações
ms.assetid: 81fe751f-51fd-4da6-b44a-0af9007eea9a
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8bcfc2263a9ecd35c050499f0547b5bc5190e5896b430edabe6be8490239b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323888"
---
# <a name="operations-plug-in-methods"></a>Métodos de plug-in de operações

Todos os pontos de entrada de plug-in de operações têm um mecanismo de retorno de chamada para relatar o êxito ou a falha da chamada. Alguns mecanismos de retorno de chamada são chamados várias vezes, até que todos os resultados sejam relatados.

A tabela a seguir fornece uma visão geral dos métodos de retorno de chamada de operações.



| Método                                                                         | Descrição                                                                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSManPluginFreeRequestDetails**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginfreerequestdetails)         | Libera a memória alocada para a estrutura DE SOLICITAÇÃO DE [**\_ PLUG-IN \_ do WSMAN.**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request)                                          |
| [**WSManPluginGetOperationParameters**](/windows/desktop/api/Wsman/nf-wsman-wsmanplugingetoperationparameters) | Obtém informações operacionais, como tempos-limites e restrições de dados associadas a uma operação.                                         |
| [**WSManPluginOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginoperationcomplete)           | Registra a conclusão de uma operação.                                                                                                              |
| [**WSManPluginReceiveResult**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreceiveresult)                   | Relata os resultados Windows plug-ins do WinRM (Gerenciamento Remoto).                                                                                       |
| [**WSManPluginReportContext**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreportcontext)                   | Relata o contexto de shell e comando de volta para a infraestrutura do WinRM para que outras operações possam ser executadas no shell e/ou comando. |



 

 

 




