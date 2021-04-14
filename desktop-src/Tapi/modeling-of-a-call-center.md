---
description: Os provedores de serviço podem expor cada recurso no PBX como um dispositivo de linha e possivelmente um dispositivo de telefone associado.
ms.assetid: 25394b19-bf75-4adc-b07d-41bc781931b6
title: Modelagem de um Call Center
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2763a1baafa41cf2d9b3b9b3c9d13be675a02d83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370560"
---
# <a name="modeling-of-a-call-center"></a>Modelagem de um Call Center

Os provedores de serviço podem expor cada recurso no PBX como um dispositivo de linha e possivelmente um dispositivo de telefone associado. Os terminais que dão suporte a várias aparências de chamada fariam isso por meio de vários endereços, assim como no controle de chamada de primeira parte. Na verdade, a exibição de terceiros de um dispositivo é idêntica à exibição de primeira empresa; os aplicativos no servidor podem ver e controlar todos os dispositivos primários, enquanto um PC cliente individual conectado ao servidor só pode ver os dispositivos que se tornaram visíveis por meio de controles de acesso administrados pelo TAPISRV no servidor. Recursos diferentes de terminais também podem ser modelados como dispositivos de linha. Por exemplo, uma fila ad ou um ponto de rota seria modelado como um dispositivo de linha que poderia ter muitas chamadas ativas; um servidor IVR, um servidor de correio de voz ou um conjunto de portas de discagem preditiva também podem ser modelados como um dispositivo de linha que dá suporte a várias chamadas.

Nesse modelo, o status do dispositivo endereçado e as chamadas associadas a ele podem ser monitorados por meio de mensagens TAPI existentes, como [**line \_ LINEDEVSTATE**](line-linedevstate.md), [**line \_ addressstate**](line-addressstate.md), [**line \_ callstate**](line-callstate.md)e [**line \_ CALLINFO**](line-callinfo.md), e detalhes obtidos por meio de funções como [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus), [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus), [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)e [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo). Sempre que um objeto TAPI é operado por meio de um aplicativo de terceiros em execução no servidor, o resultado é idêntico ao que teria ocorrido se o mesmo objeto tivesse sido operado da mesma forma por um aplicativo primário em execução em um computador cliente associado a esse dispositivo. As indicações de status enviadas pelo provedor de serviço do servidor que controlam a malha de comutação (ou switch) são entregues tanto para aplicativos em execução no servidor quanto para aqueles em execução em clientes autorizados e associados.

 

 



