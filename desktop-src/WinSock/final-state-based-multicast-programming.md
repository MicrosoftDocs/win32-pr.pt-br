---
description: Esta seção descreve a programação multicast baseada em estado final usando IOCTLs em vez de opções de soquete. Para ter uma visão geral de como a programação multicast baseada em estado final difere da programação multicast baseada em alterações, consulte Programação multicast.
ms.assetid: 71c05393-3f8c-42c0-9060-e0df9b5e2578
title: Programação multicast baseada em estado final
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad31f0c840228e1fea729582f5e259ec92c4a04381752ed9ee50db2586b3b29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132509"
---
# <a name="final-state-based-multicast-programming"></a>Programação multicast baseada em estado final

Esta seção descreve a programação multicast baseada em estado final usando IOCTLs em vez de opções de soquete. Para ter uma visão geral de como a programação multicast baseada em estado final difere da programação multicast baseada em alterações, consulte [Programação multicast](multicast-programming.md).

A tabela a seguir descreve as IOCTLs Windows Sockets usadas para programação multicast em Windows. 

| Ioctl                       | Tipo de argumento                                   |
|-----------------------------|-------------------------------------------------|
| SIOCSMSFILTER               | [**GROUP \_ Estrutura FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) |
| SIOCGMSFILTER               | [**GROUP \_ Estrutura FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) |
| SIO \_ GET \_ MULTICAST \_ FILTER | [**Estrutura \_ ip msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)   |
| FILTRO \_ MULTICAST SIO SET \_ \_ | [**Estrutura \_ ip msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)   |



 

Observe que o IOCTLS **SIOCSMSFILTER** e **SIOCGMSFILTER** estão disponíveis no Windows Vista e posterior.

Usar essas IOCTLs para programação multicast tem benefícios de desempenho ao trabalhar com listas de origem grandes. Para obter mais informações sobre os parâmetros e configurações associados ao uso de SIO GET MULTICAST FILTER ou \_ \_ \_ SIO \_ SET \_ MULTICAST FILTER, \_ consulte [**\_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) a página de referência GROUP FILTER. Para obter mais informações sobre os parâmetros e configurações associados ao uso de SIO GET MULTICAST FILTER ou SIO SET MULTICAST FILTER, consulte a página de referência \_ \_ ip \_ \_ \_ \_ [**\_ msfilter.**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)

 

 



