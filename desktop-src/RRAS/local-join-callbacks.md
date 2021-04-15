---
title: Retornos de chamada de junção local
description: Depois que o Gerenciador do grupo de multicast é notificado pelo IGMP que novos receptores estão presentes para um grupo em uma interface, o Gerenciador do grupo de multicast invoca o retorno de chamada de \_ retorno de chamadas de junção local PMGM \_ \_ para o protocolo de roteamento que possui a interface, se houver.
ms.assetid: 136f86e0-380d-4158-a9dd-c6de1c7f6689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c97f0e16e08bc3781b946a51f69d2b0d65b3272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453673"
---
# <a name="local-join-callbacks"></a>Retornos de chamada de junção local

Depois que o Gerenciador do grupo de multicast é notificado pelo IGMP que novos receptores estão presentes para um grupo em uma interface, o Gerenciador do grupo de multicast invoca o retorno de chamada de [**\_ retorno de \_ \_ chamadas de junção local PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) para o protocolo de roteamento que possui a interface, se houver. Esse retorno de chamada notifica o protocolo de roteamento da alteração.

Esse retorno de chamada e o retorno de chamada de [**PMGM \_ local \_ deixam \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) são usados para sincronizar o encaminhamento entre os protocolos IGMP e de roteamento.

 

 




