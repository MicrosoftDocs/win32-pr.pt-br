---
title: Retornos de chamada do Gerenciador de Grupos multicast
description: O gerenciador de grupos multicast usa os retornos de chamada a seguir para notificar os clientes (normalmente, protocolos de roteamento) de eventos e alterações de estado
ms.assetid: ebabdfaf-8f5f-45be-9f01-f1dbc01a376c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037281a2cb636b337c5133c2c3a261e2c435a136a30d0ccfdcf0407a9b62509b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036646"
---
# <a name="multicast-group-manager-callbacks"></a>Retornos de chamada do Gerenciador de Grupos multicast

O gerenciador de grupos multicast usa os seguintes retornos de chamada para notificar os clientes (normalmente, protocolos de roteamento) de eventos e alterações de estado:

[**RETORNO DE CHAMADA DE \_ ALERTA DE CRIAÇÃO \_ \_ DO PMGM**](/windows/win32/api/mgm/nc-mgm-pmgm_creation_alert_callback)

[**RETORNO DE CHAMADA DE ALERTA \_ DE \_ \_ JUNÇÃO DO PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback)

[**RETORNO DE CHAMADA DE ALERTA \_ DE REMOÇÃO \_ \_ DE PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback)

[**RETORNO DE CHAMADA DE \_ JUNÇÃO LOCAL \_ \_ DO PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback)

[**RETORNO DE CHAMADA DE \_ SAÍDA LOCAL \_ \_ DO PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback)

[**RETORNO DE CHAMADA RPF DO PMGM \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback)

[**PMGM \_ ERRADO SE RETORNO DE \_ \_ CHAMADA**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback)

O gerenciador de grupos multicast usa os seguintes retornos de chamada para notificar o IGMP de eventos e alterações de estado:

[**PMGM \_ DISABLE \_ IGMP \_ CALLBACK**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback)

[**PMGM \_ ENABLE \_ IGMP \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)

 

 