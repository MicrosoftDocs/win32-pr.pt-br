---
title: Enumerando entidades registradas
description: Depois que um cliente é registrado, o cliente pode obter uma lista de todos os outros clientes que se registraram com o Gerenciador de tabela de roteamento. Alguns clientes devem executar determinadas operações se a presença de um determinado tipo de cliente for detectada.
ms.assetid: d94de573-7c1e-4179-a41f-5836d2c5d44a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1d67a810806c1bc29f8f18c4cdea9f3a36e5b5a95922e8f66a943a99923ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674156"
---
# <a name="enumerating-registered-entities"></a>Enumerando entidades registradas

Depois que um cliente é registrado, o cliente pode obter uma lista de todos os outros clientes que se registraram com o Gerenciador de tabela de roteamento. Alguns clientes devem executar determinadas operações se a presença de um determinado tipo de cliente for detectada.

O cliente pode chamar a função [**RtmGetRegisteredEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) . Um buffer de estruturas de [**\_ \_ informações de entidade RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) é retornado. Depois que o cliente tiver processado essas informações, o cliente deverá chamar [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) para liberar os identificadores nas estruturas de **\_ \_ informações da entidade RTM** .

Se o cliente do Gerenciador de tabela de roteamento forneceu uma função de retorno de chamada em chamar [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity), o cliente será notificado quando qualquer outro cliente registrar ou cancelar o registro.

Para obter um exemplo de código que mostra como usar essas funções, consulte [enumerar as entidades registradas](enumerate-the-registered-entities.md) e [usar o retorno de chamada de notificação de evento](use-the-event-notification-callback.md).

 

 




