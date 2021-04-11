---
title: Registrando com o Gerenciador de tabela de roteamento
description: Antes que um cliente possa acessar a tabela de roteamento, ele primeiro deve se registrar com o Gerenciador de tabela de roteamento usando a função RtmRegisterEntity.
ms.assetid: 9bdbe138-d31b-42bb-9c51-5f1c5e8a4ca7
keywords:
- Gerenciador de tabela de roteamento versão 2 RRAS, registrando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ce5a1b350ec5420b3fc32a4e5a68a213a61151
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159739"
---
# <a name="registering-with-the-routing-table-manager"></a>Registrando com o Gerenciador de tabela de roteamento

Antes que um cliente possa acessar a tabela de roteamento, ele primeiro deve se registrar com o Gerenciador de tabela de roteamento usando a função [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) .

Quando um cliente é registrado, ele passa para o Gerenciador de tabela de roteamento uma estrutura de [**\_ \_ informações de entidade RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) . Essa estrutura contém as informações que identificam exclusivamente um cliente, a família de endereços e a instância do Gerenciador de tabelas de roteamento com a qual o cliente está se registrando. Um cliente também pode estabelecer o retorno de chamada de [**\_ retorno de \_ chamada do evento RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) . O Gerenciador de tabela de roteamento usará esse retorno de chamada para notificar o cliente sobre eventos como notificações de alteração e registros de cliente.

O Gerenciador de tabela de roteamento conclui seu processamento de registro e retorna um identificador para o cliente. O cliente deve usar esse identificador para todas as chamadas subsequentes para as funções RTMv2.

A função [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) que é usada em RTMv2 é análoga à função [**RtmRegisterClient**](rtmregisterclient.md) que é usada em RTMv1. A função **RtmRegisterClient** é obsoleta, exceto para clientes que usam IPX.

Depois que um cliente termina de interagir com o Gerenciador de tabela de roteamento, ele deve chamar [**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity). O Gerenciador de tabela de roteamento destrói o identificador associado ao cliente. Para evitar vazamentos de memória, o cliente deve garantir que ele libera todos os identificadores e exclui todas as rotas e os próximos saltos que ele possui antes de chamar **RtmDeregisterEntity**.

Para obter um exemplo de código que mostra como usar essas funções, consulte [registrar com o Gerenciador de tabela de roteamento](register-with-the-routing-table-manager.md) e [usar o retorno de chamada de notificação de evento](use-the-event-notification-callback.md).

 

 




