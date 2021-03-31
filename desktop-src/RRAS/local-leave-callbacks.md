---
title: Retornos de chamada de saída local
description: Depois que o Gerenciador do grupo de multicast é notificado pelo IGMP de que não há mais destinatários presentes para um grupo em uma interface, o Gerenciador do grupo de multicast invoca o retorno de chamada de PMGM \_ local \_ Leave de retorno de \_ chamada para o protocolo de roteamento nessa interface, se houver. Esse retorno de chamada notifica o protocolo de roteamento da alteração.
ms.assetid: 47696533-603c-459f-9aa7-3ce42fff3332
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a98d32e041b048e15497bc7fe35d17628b9331d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005732"
---
# <a name="local-leave-callbacks"></a>Retornos de chamada de saída local

Depois que o Gerenciador do grupo de multicast é notificado pelo IGMP de que não há mais destinatários presentes para um grupo em uma interface, o Gerenciador do grupo de multicast invoca o retorno de chamada de [**PMGM \_ local \_ Leave de retorno de \_ chamada**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) para o protocolo de roteamento nessa interface, se houver. Esse retorno de chamada notifica o protocolo de roteamento da alteração.

Esse retorno de chamada e o retorno de chamada da [**\_ \_ junção \_ local PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) são usados para sincronizar o encaminhamento entre os protocolos IGMP e de roteamento.

 

 




