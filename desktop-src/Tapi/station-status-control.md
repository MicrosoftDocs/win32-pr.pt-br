---
description: Há três funções de status de estação principais que precisam de controle de luzes de espera, encaminhamento e não perturbe.
ms.assetid: 4a6dc47f-caff-4f2b-8858-0e9bec32b137
title: Controle de status de estação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f6ddd1b1ce6df1ad2f3dc61e891ed6952a7f05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779444"
---
# <a name="station-status-control"></a>Controle de status de estação

Há três funções de status de estação principais que precisam de controle: luzes de espera de mensagem, encaminhamento e não incomodar. O encaminhamento e não incomodar são controláveis por meio da função [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) existente (que é específica de endereço) e consultados usando [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus). O LINEDEVSTATUSFLAGS \_ MSGWAIT bit no membro **DwDevStatusFlags** de [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) indica o status da luz de espera da mensagem no dispositivo e uma mensagem LINEDEVSTATE MSGWAITON \_ ou LINEDEVSTATE \_ MSGWAITOFF é enviada para indicar quando o estado é alterado. A função [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) permite que a luz de espera da mensagem seja controlada sem a necessidade de implementar um dispositivo de telefone TAPI apenas para essa finalidade. O LINEFEATURE \_ SETDEVSTATUS bit (no membro **DwLineFeatures** de [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) e **LINEDEVSTATUS**) indica quando ele pode ser chamado, e o membro **dwSettableDevStatus** de **LINEDEVCAPS** permite que o aplicativo detecte quais configurações de status do dispositivo podem ser controladas a partir do aplicativo. Além de permitir que o recurso de espera de mensagem seja controlado, ele também permite que o status conectado, inmanutenção e bloqueado do dispositivo seja definido, na medida em que eles têm suporte no comutador ou outro hardware. As chamadas para essa função resultam na [**linha apropriada \_ LINEDEVSTATE**](line-linedevstate.md) mensagens enviadas para refletir o novo status.

 

 



