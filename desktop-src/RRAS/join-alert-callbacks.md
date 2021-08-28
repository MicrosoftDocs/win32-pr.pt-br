---
title: Unir retornos de chamada de alerta
description: Quando o gerenciador de grupos multicast é notificado de que há novos receptores presentes para um grupo em uma interface, o gerenciador de grupos multicast invoca o retorno de chamada DE ALERTA DE JUNÇÃO \_ \_ PMGM. \_
ms.assetid: b625f8ec-f59b-4151-aa38-48cf8f004966
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0da66e405441804cbca4452cedd7a6599067138bee95a33eaee7a2f10c34c9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074116"
---
# <a name="join-alert-callbacks"></a>Unir retornos de chamada de alerta

Quando o gerenciador de grupos multicast é notificado de que há novos receptores presentes para um grupo em uma interface, o gerenciador de grupos multicast invoca o retorno de chamada DE ALERTA DE JUNÇÃO [**PMGM. \_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) Esse retorno de chamada notifica os protocolos de roteamento de que novos hosts ingressaram nos grupos especificados. Portanto, os protocolos de roteamento devem solicitar dados multicast para os grupos especificados pelo retorno de chamada.

O gerenciador de grupos multicast usa um conjunto predefinido de regras que são usadas para determinar quando esse retorno de chamada é invocado. Esse conjunto de regras baseia-se no tipo de solicitação de junção enviada pelo cliente e na ordem em que as solicitações de junção foram recebidas.

## <a name="wildcard-join-requests"></a>Solicitações de junção curinga

Quando uma junção curinga para um grupo ( , g) é recebida do primeiro cliente, o gerenciador de grupos multicast invoca o retorno de chamada de RETORNO DE CHAMADA DE ALERTA DE JUNÇÃO DO \* [**PMGM \_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) para todos os outros clientes registrados. Quando uma junção curinga para um grupo é recebida do segundo cliente, o gerenciador de grupos multicast invoca esse retorno de chamada para o primeiro cliente a ingressar no grupo.

## <a name="source-specific-join-requests"></a>Source-Specific solicitações de junção

O gerenciador de grupos multicast não invoca esse retorno de chamada para quaisquer junções subsequentes ao grupo.

Quando uma junção específica da origem para um grupo (s, g) é recebida, o gerenciador de grupos multicast invoca o retorno de chamada DE ALERTA DE JUNÇÃO [**PMGM \_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) somente para o cliente que possui a interface de entrada para os s de origem.

 

 




