---
title: Início da demanda nas filas de solicitações da versão 2,0
description: Início da demanda nas filas de solicitações da versão 2,0
ms.assetid: 84a744b7-1b0e-4fa7-8015-4840251aa856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ec5f0d2d973cfb7d4d0a3f23a5d1f6b6c6055dd9aff19521ed9ff100879c43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050786"
---
# <a name="demand-start-on-version-20-request-queues"></a>Início da demanda nas filas de solicitações da versão 2,0

O recurso de início de demanda das filas de solicitação da API do servidor HTTP versão 2,0 permite que o aplicativo do controlador adie a instanciação do processo de trabalho até que a primeira solicitação chegue à fila de solicitações. Portanto, os aplicativos podem evitar o consumo de recursos até que sejam necessários. Para obter mais informações sobre o aplicativo do controlador, consulte o tópico [fila de solicitações nomeadas](named-request-queue.md) .

## <a name="asynchronous-demand-start"></a>Início de demanda assíncrona

O aplicativo do controlador chama [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) com o identificador da fila de solicitação para iniciar uma notificação de início de demanda. Para a conclusão assíncrona, o aplicativo fornece a estrutura sobreposta no parâmetro *pOverlapped* . Quando **HttpWaitForDemandStart** é chamado de forma assíncrona, o aplicativo do controlador é notificado quando a primeira solicitação chega na fila de solicitações. Depois que a notificação de início de demanda for concluída, o aplicativo do controlador poderá se registrar para outra notificação de início de demanda na fila de solicitações.

A API do servidor HTTP não permite mais de uma notificação de início de demanda simultânea para uma fila de solicitações. No entanto, quando a notificação de início de demanda pendente é concluída, o aplicativo chama [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) novamente para iniciar vários processos de trabalho na fila de solicitações. O HTTP não impõe limitações no número de notificações de início de demanda ou no número de processos de trabalho operando na fila de solicitações. No entanto, os aplicativos do controlador podem impor o número de processos de trabalho permitidos em uma fila de solicitações.

A API do servidor HTTP dá suporte à cancelamento de chamadas [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) assíncronas. Os aplicativos podem usar [**CancelIoEx**](/windows/desktop/FileIO/cancelioex-func) com a estrutura sobreposta fornecida em *pOverlapped* para cancelar uma chamada **HttpWaitForDemandStart** pendente.

## <a name="synchronous-demand-start"></a>Início de demanda síncrona

O início de demanda síncrona não é recomendado porque o aplicativo é bloqueado até que uma solicitação chegue à fila de solicitações.

 

 
