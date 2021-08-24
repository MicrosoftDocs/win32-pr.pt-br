---
description: O encaminhamento é a deflexão de uma sessão de entrada para um endereço de destino diferente.
ms.assetid: c70bf596-b2a4-46ec-9b1a-c9d948768b51
title: Encaminhar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddddd21a945c3ca63a5c9040b8eabe0d1056b74b2f819f3fb62dbd8b760aaca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660846"
---
# <a name="forward"></a>Encaminhar

O encaminhamento é a deflexão de uma sessão de entrada para um endereço de destino diferente. A TAPI permite que um aplicativo especifique uma lista de condições de encaminhamento para um endereço. As condições de encaminhamento podem ser tão refinadas como um destino e [**modo de encaminhamento**](./lineforwardmode--constants.md) diferentes para cada endereço de chamador.

A operação de encaminhamento também pode ser usada para implementar um recurso do-não-perturbe seletivo, encaminhando alguns chamadores para o correio de voz e permitindo que outros tentem a conclusão.

A operação de encaminhamento também pode cancelar qualquer encaminhamento atualmente em vigor.

Alguns provedores de serviços exigem que um aplicativo crie uma chamada de consulta antes de uma operação de encaminhamento. Em seguida, a operação de encaminhamento passa um ponteiro para a chamada de consulta.

Nem todos os provedores de serviço dão suporte ao uso desta operação.

**TAPI 2. x:** Para definir [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward) para obter [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), altere a mensagem de notificação [**\_ addressstate de linha**](./line-addressstate.md) com o LINEADDRESSSTATE \_ forward.

**TAPI 3. x:** Consulte [**ITAddress:: encaminhar**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**ITAddress:: get \_ CurrentForwardInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), notificação de alteração: [**ITADDRESSEVENT:: get \_ evento**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) com AE \_ forward.

> [!Note]  
> Pode ser impossível que um provedor de serviços saiba sempre que o encaminhamento está em vigor para um endereço. O encaminhamento pode ser cancelado ou alterado de maneiras que não resultam em notificação para o provedor de serviços.

 

 

 
