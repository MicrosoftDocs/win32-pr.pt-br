---
description: A operação de suspensão permite que um único endereço manipule várias sessões de comunicação.
ms.assetid: 65e22e4e-e346-41c2-929a-ba0d1f7f1732
title: Bloquear
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afacd6d9664e9a095a1e8b0c725dc0171da709fdecffb88b428231a5b5359a4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003634"
---
# <a name="hold"></a>Bloquear

A operação de suspensão permite que um único endereço manipule várias sessões de comunicação. Colocar uma sessão em um disco rígido libera a linha/endereço do usuário para fazer outras chamadas. Uma chamada em retenção rígida normalmente não pode ser transferida ou incluída em uma chamada de conferência, mas uma chamada de consulta pode. As chamadas de consulta são iniciadas usando as operações de [conferência](conference-ovr.md) ou de [transferência](transfer-ovr.md) .

Depois que uma chamada é colocada em espera com êxito, o estado de chamada normalmente faz a transição para o estado onHold. Enquanto uma chamada está em espera, o aplicativo pode receber mensagens sobre alterações de estado da chamada mantida. Por exemplo, se a parte mantida for desligada, o estado da chamada poderá passar para desconectado.

Em uma situação de ponte, a operação de espera pode não fazer a chamada em espera. O status de outras estações na chamada pode controlar (por exemplo, tentar "manter" uma chamada quando não é possível participar de outras estações); em vez disso, a chamada pode simplesmente ser alterada para o estado inativo enquanto ela permanece conectada em outras estações.

Nem todos os provedores de serviço dão suporte ao uso desta operação.

**TAPI 2. x:** Consulte [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold), [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold).

**TAPI 3. x:** Consulte [**ITBasicCallControl:: Hold**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold).

 

 
