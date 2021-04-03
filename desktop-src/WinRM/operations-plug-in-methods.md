---
title: Métodos de plug-in de operações
description: Métodos de plug-in de operações
ms.assetid: 81fe751f-51fd-4da6-b44a-0af9007eea9a
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff64a53c4c63b9e552efe90ac057b8a31d603b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915848"
---
# <a name="operations-plug-in-methods"></a>Métodos de plug-in de operações

Todos os pontos de entrada de plug-in de operações têm um mecanismo de retorno de chamada para relatar o êxito ou a falha da chamada. Alguns mecanismos de retorno de chamada são chamados várias vezes, até que todos os resultados sejam relatados.

A tabela a seguir fornece uma visão geral dos métodos de retorno de chamada de operações.



| Método                                                                         | Descrição                                                                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSManPluginFreeRequestDetails**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginfreerequestdetails)         | Libera a memória alocada para a estrutura de [**\_ \_ solicitação de plug-in do WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) .                                          |
| [**WSManPluginGetOperationParameters**](/windows/desktop/api/Wsman/nf-wsman-wsmanplugingetoperationparameters) | Obtém informações operacionais, tais como tempos limite e restrições de dados associadas a uma operação.                                         |
| [**WSManPluginOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginoperationcomplete)           | Registra a conclusão de uma operação.                                                                                                              |
| [**WSManPluginReceiveResult**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreceiveresult)                   | Relata resultados para Gerenciamento Remoto do Windows (WinRM) plug-ins.                                                                                       |
| [**WSManPluginReportContext**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreportcontext)                   | Relata o Shell e o contexto de comando de volta para a infraestrutura do WinRM para que outras operações possam ser executadas em relação ao shell e/ou ao comando. |



 

 

 




