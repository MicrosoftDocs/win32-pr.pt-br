---
description: Esta seção descreve a programação de multicast com base no estado final usando IOCTLs, em vez de opções de soquete. Para obter uma visão geral de como a programação de multicast baseada em estado final difere da programação de multicast baseada em alteração, consulte programação de multicast.
ms.assetid: 71c05393-3f8c-42c0-9060-e0df9b5e2578
title: Programação de multicast com base no estado final
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6abfebfc7efe27f1c5a6d63312c376bd659dce57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789343"
---
# <a name="final-state-based-multicast-programming"></a>Programação de multicast com base no estado final

Esta seção descreve a programação de multicast com base no estado final usando IOCTLs, em vez de opções de soquete. Para obter uma visão geral de como a programação de multicast baseada em estado final difere da programação de multicast baseada em alteração, consulte [programação de multicast](multicast-programming.md).

A tabela a seguir descreve os IOCTLs do Windows Sockets usados para programação de multicast no Windows. 

| IOCTL                       | Tipo de argumento                                   |
|-----------------------------|-------------------------------------------------|
| SIOCSMSFILTER               | [**Grupo \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) Estrutura do filtro |
| SIOCGMSFILTER               | [**Grupo \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) Estrutura do filtro |
| SIO \_ obter \_ \_ filtro multicast | estrutura de [**\_ MsFilter IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)   |
| SIO \_ definir \_ filtro de multicast \_ | estrutura de [**\_ MsFilter IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)   |



 

Observe que os IOCTLs **SIOCSMSFILTER** e **SIOCGMSFILTER** estão disponíveis no Windows Vista e versões posteriores.

O uso desses IOCTLs para a programação de multicast tem benefícios de desempenho ao trabalhar com listas de origem grandes. Para obter mais informações sobre os parâmetros e configurações associados ao uso do SIO \_ obter \_ \_ filtro de multicast ou \_ \_ o filtro de multicast definido por Sio \_ , consulte a página de referência de [**\_ filtro de grupo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) . Para obter mais informações sobre os parâmetros e as configurações associadas ao uso do SIO \_ obter \_ \_ filtro multicast ou \_ o sio definir \_ \_ filtro de multicast, consulte a página de referência de [**\_ MsFilter de IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) .

 

 



