---
title: Retornos de chamada do Gerenciador de grupos multicast
description: O Gerenciador de grupos de multicast usa os seguintes retornos de chamada para notificar os clientes (normalmente, protocolos de roteamento) de eventos e alterações de estado
ms.assetid: ebabdfaf-8f5f-45be-9f01-f1dbc01a376c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ba18f874005e23aef6daca6071362362312e8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823876"
---
# <a name="multicast-group-manager-callbacks"></a>Retornos de chamada do Gerenciador de grupos multicast

O Gerenciador de grupos de multicast usa os seguintes retornos de chamada para notificar os clientes (normalmente, protocolos de roteamento) de eventos e alterações de Estado:

[**\_retorno de \_ chamada de alerta de criação de PMGM \_**](/windows/win32/api/mgm/nc-mgm-pmgm_creation_alert_callback)

[**\_retorno de \_ chamada de alerta do PMGM Join \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback)

[**retorno de chamada de alerta de remoção de PMGM \_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback)

[**\_retorno de \_ chamada de junção local PMGM \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback)

[**\_retorno de \_ chamada de saída local PMGM \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback)

[**retorno de chamada do PMGM \_ RPF \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback)

[**PMGM \_ errado \_ se o \_ retorno de chamada**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback)

O Gerenciador de grupos de multicast usa os seguintes retornos de chamada para notificar IGMP de eventos e alterações de Estado:

[**PMGM \_ desabilitar \_ \_ retorno de chamada IGMP**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback)

[**PMGM \_ habilitar \_ \_ retorno de chamada IGMP**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)

 

 