---
title: Associar retornos de chamada de alerta
description: Quando o Gerenciador do grupo de multicast é notificado de que há novos receptores presentes para um grupo em uma interface, o Gerenciador do grupo de multicast invoca o retorno de chamada de \_ retorno do alerta de ingresso PMGM \_ \_ .
ms.assetid: b625f8ec-f59b-4151-aa38-48cf8f004966
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00dc70160b99c3cfc0e41078a3bd5882d930f31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005734"
---
# <a name="join-alert-callbacks"></a>Associar retornos de chamada de alerta

Quando o Gerenciador do grupo de multicast é notificado de que há novos receptores presentes para um grupo em uma interface, o Gerenciador do grupo de multicast invoca o retorno de chamada de [**\_ retorno do \_ alerta \_ de ingresso PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) . Esse retorno de chamada notifica os protocolos de roteamento que novos hosts ingressaram nos grupos especificados. Portanto, os protocolos de roteamento devem solicitar dados multicast para os grupos especificados pelo retorno de chamada.

O Gerenciador do grupo de multicast usa um conjunto predefinido de regras que são usadas para determinar quando esse retorno de chamada é invocado. Esse conjunto de regras se baseia no tipo de solicitação de junção enviado pelo cliente e na ordem em que as solicitações de junção foram recebidas.

## <a name="wildcard-join-requests"></a>Solicitações de junção curinga

Quando uma junção curinga para um grupo ( \* , g) é recebida do primeiro cliente, o Gerenciador do grupo de multicast invoca o retorno de chamada do [**\_ alerta de ingresso \_ \_ PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) para todos os outros clientes registrados. Quando uma junção curinga para um grupo é recebida do segundo cliente, o Gerenciador do grupo de multicast invoca esse retorno de chamada para o primeiro cliente para ingressar no grupo.

## <a name="source-specific-join-requests"></a>Source-Specific solicitações de junção

O Gerenciador do grupo de multicast não invoca esse retorno de chamada para todas as junções subsequentes para o grupo.

Quando uma junção específica de origem para um grupo (s, g) é recebida, o Gerenciador do grupo de multicast invoca o retorno de chamada do [**\_ alerta de ingresso \_ \_ PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) somente para o cliente que possui a interface de entrada em direção às s de origem.

 

 




