---
title: Referência da API do auxiliar de roteamento de conexão sob demanda
description: Os tópicos a seguir fornecem detalhes para o auxiliar de roteamento de conexão sob demanda.
ms.assetid: 39AFFD16-488E-4CA3-9161-9424F0D15948
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e9e046c1add8703e6603d925d2c80b03aab8d7eae3a352825e56ec907f3adb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685576"
---
# <a name="on-demand-connection-routing-helper-api-reference"></a>Referência da API do auxiliar de roteamento de conexão sob demanda

Os tópicos a seguir fornecem detalhes para o auxiliar de roteamento de conexão sob demanda.



| Referência                                                                          | Descrição                                                                                                                                                                 |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnDemandGetRoutingHint**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandgetroutinghint)                           | Pesquisar um destino no cache de solicitação de rota e, se uma correspondência for encontrada, retorna a ID de interface correspondente.<br/>                                               |
| [**OnDemandRegisterNotification**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandregisternotification)               | Registre-se para ser notificado quando o cache de solicitações de rota for modificado.<br/>                                                                                               |
| [**OnDemandUnregisterNotification**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandunregisternotification)           | Cancelar o registro para notificações e limpar recursos.<br/>                                                                                                             |
| [**\_contexto de interface de rede \_**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context)                           | O contexto de interface que faz parte da estrutura da [**tabela de contexto da interface de rede \_ \_ \_**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table) .<br/>                                       |
| [**\_tabela de \_ contexto de interface de rede \_**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table)              | A tabela de estruturas de [**\_ \_ contexto de interface de rede**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context) .<br/>                                                                                |
| [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) | Essa função recupera uma tabela de contexto de interface para o nome de host e o filtro de perfil de conexão fornecidos.<br/>                                                         |
| [**FreeInterfaceContextTable**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-freeinterfacecontexttable)                     | Essa função libera a tabela de contexto da interface recuperada usando a função [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) .<br/> |



 

 

 





