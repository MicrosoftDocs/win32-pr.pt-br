---
title: Enumerando entidades registradas
description: Depois que um cliente é registrado, o cliente pode obter uma lista de todos os outros clientes que se registraram com o Gerenciador de tabela de roteamento. Alguns clientes devem executar determinadas operações se a presença de um determinado tipo de cliente for detectada.
ms.assetid: d94de573-7c1e-4179-a41f-5836d2c5d44a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac92ccf89336d3fbca378209b9e79877d9b426a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005569"
---
# <a name="enumerating-registered-entities"></a>Enumerando entidades registradas

Depois que um cliente é registrado, o cliente pode obter uma lista de todos os outros clientes que se registraram com o Gerenciador de tabela de roteamento. Alguns clientes devem executar determinadas operações se a presença de um determinado tipo de cliente for detectada.

O cliente pode chamar a função [**RtmGetRegisteredEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) . Um buffer de estruturas de [**\_ \_ informações de entidade RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) é retornado. Depois que o cliente tiver processado essas informações, o cliente deverá chamar [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) para liberar os identificadores nas estruturas de **\_ \_ informações da entidade RTM** .

Se o cliente do Gerenciador de tabela de roteamento forneceu uma função de retorno de chamada em chamar [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity), o cliente será notificado quando qualquer outro cliente registrar ou cancelar o registro.

Para obter um exemplo de código que mostra como usar essas funções, consulte [enumerar as entidades registradas](enumerate-the-registered-entities.md) e [usar o retorno de chamada de notificação de evento](use-the-event-notification-callback.md).

 

 




