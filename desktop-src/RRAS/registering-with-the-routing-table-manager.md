---
title: Registrando com o Gerenciador de Tabelas de Roteamento
description: Antes que um cliente possa acessar a tabela de roteamento, ele deve primeiro se registrar no gerenciador de tabelas de roteamento usando a função RtmRegisterEntity.
ms.assetid: 9bdbe138-d31b-42bb-9c51-5f1c5e8a4ca7
keywords:
- RRAS do Gerenciador de Tabelas de Roteamento versão 2, registrando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 088072fac8679d9b2f87729b67a826ac850e77109f18b28fef3c2dc33c433f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028286"
---
# <a name="registering-with-the-routing-table-manager"></a>Registrando com o Gerenciador de Tabelas de Roteamento

Antes que um cliente possa acessar a tabela de roteamento, ele deve primeiro se registrar no gerenciador de tabelas de roteamento usando a [**função RtmRegisterEntity.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity)

Quando um cliente se registra, ele passa para o gerenciador de tabela de roteamento uma [**estrutura DE INFORMAÇÕES DE \_ ENTIDADE \_ RTM.**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) Essa estrutura contém as informações que identificam exclusivamente um cliente, a família de endereços e a instância do gerenciador de tabela de roteamento com o qual o cliente está se registrando. Um cliente também pode estabelecer o retorno de chamada DE RETORNO DE CHAMADA DE [**EVENTO RTM. \_ \_**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) O gerenciador de tabela de roteamento usará esse retorno de chamada para notificar o cliente de eventos, como notificações de alteração e registros de cliente.

O gerenciador de tabela de roteamento conclui seu processamento de registro e retorna um handle para o cliente. O cliente deve usar esse handle para todas as chamadas subsequentes para funções RTMv2.

A [**função RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) usada no RTMv2 é análoga à [**função RtmRegisterClient**](rtmregisterclient.md) usada no RTMv1. A **função RtmRegisterClient** está obsoleta, exceto para clientes que usam IPX.

Depois que um cliente terminar de interagir com o gerenciador de tabela de roteamento, ele deverá chamar [**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity). O gerenciador de tabela de roteamento destrói o alça associado ao cliente. Para evitar vazamentos de memória, o cliente deve garantir que ele libere todos os handles e exclua todas as rotas e os próximos saltos que possui antes de chamar **RtmDeregisterEntity.**

Para o código de exemplo que mostra como usar essas funções, consulte [Registrar](register-with-the-routing-table-manager.md) com o Gerenciador de Tabela de Roteamento e Usar o Retorno de Chamada [de Notificação de Eventos](use-the-event-notification-callback.md).

 

 




