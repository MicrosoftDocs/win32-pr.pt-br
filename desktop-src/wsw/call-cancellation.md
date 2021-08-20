---
title: Cancelamento de chamada
description: A notificação de cancelamento de chamada cancela a operação de operações de serviço no servidor e retornos de chamada de modelo de serviço.
ms.assetid: dc371921-869f-4775-98d3-80a1006358ba
keywords:
- Chamar o cancelamento de serviços Web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dda4ec4227403bed5239b68cfa05d2064976517a7473fa7926c8de5f56227645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026694"
---
# <a name="call-cancellation"></a>Cancelamento de chamada

A notificação de cancelamento de chamada cancela a operação de [operações de serviço no servidor](server-side-service-operations.md) e retornos de chamada de modelo de serviço. Esse cancelamento pode ser por uma destas duas razões:

-   O host de serviço parou as operações devido a uma chamada para a função [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) .
-   O canal subjacente gerou uma falha.


Para receber uma notificação de cancelamento, a operação de serviço ou o retorno de chamada de modelo de serviço deve registrar um retorno de chamada de [**\_ \_ cancelamento de \_ retorno de operação do WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) chamando a função [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) .

Opcionalmente, como parte do registro para notificação de cancelamento, a operação de serviço ou o retorno de chamada de modelo de serviço também pode registrar dados de estado específicos do aplicativo e o retorno de chamada do [**\_ \_ \_ \_ estado livre do WS Operation**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) .

Os dados de estado são disponibilizados para o retorno de chamada de [**\_ \_ cancelamento \_ da operação WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) . Na conclusão da chamada, o retorno de chamada do [**\_ \_ \_ \_ estado livre do WS Operation**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) é chamado para dar ao aplicativo uma oportunidade de liberar os dados de estado.

Para obter um exemplo de código, consulte [BlockingServiceExample](blockingserviceexample.md).

O retorno de chamada de cancelamento é chamado apenas uma vez durante o tempo de vida da função de operações ou de retorno de chamada do [serviço do servidor](server-side-service-operations.md) .

O cancelamento de chamada está disponível em para todos os retornos de chamada do host de serviço que usam o [ \_ \_ contexto de operação do WS](ws-operation-context.md) como um parâmetro.

Os elementos da API a seguir estão relacionados ao cancelamento da chamada.

| Callback                                                                         | Descrição                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_retorno de \_ chamada Cancelar operação \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)          | Chamado pelo modelo de serviço para notificar um cancelamento de uma operação de serviço assíncrono como resultado de um desligamento anulado do host de serviço. |
| [**\_retorno de \_ \_ chamada de estado livre de operação WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) | Chamado pelo modelo de serviço para permitir que um aplicativo Limpe os dados de estado que foram registrados com o retorno de chamada de cancelamento.                |



 



| Função                                                             | Descrição                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) | Permite que uma operação de serviço ou um retorno de chamada de modelo de serviço seja registrado para uma notificação de cancelamento. |



 

 

 




