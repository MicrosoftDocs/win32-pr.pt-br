---
description: Windows Os soquetes habilitam a MLD (Descoberta de Ouvinte Multicast) em IPv6 e o protocolo IGMP no IPv4 para aplicativos multicast por meio do uso de opções de soquete e IOCTLs.
ms.assetid: a5de4273-e86e-4f13-b068-256cb38706d4
title: MLD e IGMP usando Windows soquetes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2c550cf2c1463f5b646efc286c05010274d3cb44e13b9559302452bccb81c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051644"
---
# <a name="mld-and-igmp-using-windows-sockets"></a>MLD e IGMP usando Windows soquetes

Windows Os soquetes habilitam a MLD (Descoberta de Ouvinte Multicast) em IPv6 e o protocolo IGMP no IPv4 para aplicativos multicast por meio do uso de opções de soquete e IOCTLs. Esta página descreve as opções de soquete que habilitam a programação multicast e descreve como elas são usadas. Para definições de cada opção de soquete, consulte a página [Opções de Soquete.](socket-options.md)

Para obter informações sobre como usar IOCTLs para programação multicast, consulte [Programação multicast](final-state-based-multicast-programming.md) baseada em estado final mais adiante nesta seção.

No Windows Vista e posterior, um conjunto de opções de soquete está disponível para programação multicast que suporta endereços IPv6 e IPv4. Essas opções de soquete são agnósticas de IP e podem ser usadas em IPv6 e IPv4. No IPv6, essas opções de soquete usam MLDv2. No IPv4, essas opções de soquete usam IGMPv3. Essas opções de agnóstica de IP são as opções de soquete preferenciais para programação multicast no Windows Vista e posterior. Windows Os soquetes usam as seguintes opções de soquete: 

| Opção de soquete               | Tipo de argumento                                            |
|-----------------------------|----------------------------------------------------------|
| ORIGEM DO BLOCO MCAST \_ \_        | [**GROUP \_ Estrutura \_ SOURCE REQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| GRUPO DE \_ JUNÇÃO MCAST \_          | [**GROUP \_ Estrutura REQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_req)                |
| GRUPO DE \_ ORIGEM DE \_ JUNÇÃO MCAST \_  | [**GROUP \_ Estrutura \_ SOURCE REQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| MCAST \_ LEAVE \_ GROUP         | [**GROUP \_ Estrutura REQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_req)                |
| MCAST \_ SAIR DO GRUPO DE \_ \_ ORIGEM | [**GROUP \_ Estrutura \_ SOURCE REQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| MCAST \_ UNBLOCK \_ SOURCE      | [**GROUP \_ Estrutura \_ SOURCE REQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |



 

Um conjunto de opções de soquete está disponível para programação multicast que suporta apenas endereços IPv6. Essas opções de soquete usam MLDv1 ou MLDv2. A versão do MLD usada depende da versão do Windows. O MLDv2 tem suporte no Windows Vista e posterior. Windows Os soquetes usam as seguintes opções de soquete: 

| Opção de soquete          | Tipo de argumento                             |
|------------------------|-------------------------------------------|
| IPV6 \_ ADD \_ MEMBERSHIP  | [**Estrutura \_ mreq ipv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) |
| IPV6 \_ DROP \_ MEMBERSHIP | [**Estrutura \_ mreq ipv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) |



 

Um conjunto de opções de soquete está disponível para programação multicast que suporta apenas endereços IPv4. Essas opções de soquete usam IGMPv3 ou IGMPv2. A versão do IGMP usada depende da versão do Windows. Há suporte para IGMPv3 no Windows Vista e posterior. Windows Os soquetes usam as seguintes opções de soquete:

| Opção de soquete                | Tipo de argumento                                        |
|------------------------------|------------------------------------------------------|
| IP \_ ADD \_ MEMBERSHIP          | [**Estrutura \_ ip mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq)                |
| ASSOCIAÇÃO DE \_ ORIGEM DO IP ADD \_ \_  | [**Estrutura \_ de \_ origem ip mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |
| IP \_ BLOCK \_ SOURCE            | [**Estrutura \_ de \_ origem ip mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |
| ASSOCIAÇÃO \_ AO IP DROP \_         | [**Estrutura \_ ip mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq)                |
| ASSOCIAÇÃO \_ DE \_ ORIGEM DO IP DROP \_ | [**Estrutura \_ de \_ origem ip mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |
| IP \_ UNBLOCK \_ SOURCE          | [**Estrutura \_ de \_ origem ip mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |



 

Quando O IGMPv3 está disponível, as opções \_ IP ADD \_ SOURCE MEMBERSHIP, IP BLOCK SOURCE, IP DROP SOURCE MEMBERSHIP e IP UNBLOCK SOURCE são tratadas com mais eficiência, pois o roteador pode lidar com a \_ \_ \_ \_ \_ \_ \_ \_ filtragem. Quando apenas IGMPv2 estiver disponível, o host deverá lidar com a filtragem.

Há duas categorias nas quais a maioria dos aplicativos provavelmente se enquadra: qualquer fonte e origem controlada.

-   **Aplicativos de qualquer** fonte aceitam todas as fontes por padrão, permitindo que fontes individuais sejam desligadas conforme necessário. Um exemplo de um aplicativo de qualquer fonte é uma chamada de videoconferência que permite que todos os destinatários participem.
-   **Os aplicativos de origem** controlada limitam as fontes a uma determinada lista, como uma estação de rádio da Internet ou a difusão de um evento notável. O processo de usar opções de soquete é ligeiramente diferente para cada uma.

No Windows Vista e posterior, as seguintes etapas se aplicam a aplicativos de qualquer fonte:

- Use **MCAST \_ JOIN \_ GROUP** para ingressar em um grupo.  
- Use **MCAST \_ BLOCK \_ SOURCE** para desligar uma determinada origem, se necessário.  
- Use **MCAST \_ UNBLOCK \_ SOURCE** para permitir uma origem bloqueada, se necessário.  
- Use **MCAST \_ LEAVE \_ GROUP** para sair do grupo.  

No Windows Vista e posterior, as seguintes etapas se aplicam a aplicativos de origem controlada:

- Use **MCAST \_ JOIN SOURCE \_ GROUP \_ para** unir cada par grupo/origem.  
- Use **MCAST \_ LEAVE SOURCE \_ \_ GROUP** para sair de cada grupo/origem ou use **MCAST LEAVE \_ \_ GROUP** para deixar todas as fontes, se o mesmo endereço de grupo for usado por todas as fontes.  

As etapas a seguir se aplicam a aplicativos de qualquer fonte:

- Use **IP \_ ADD \_ MEMBERSHIP** para ingressar em um grupo (**IPV6 \_ ADD \_ MEMBERSHIP** para IPv6).  
- Use **IP \_ BLOCK \_ SOURCE** para desligar uma determinada origem, se necessário.  
- Use **IP \_ UNBLOCK \_ SOURCE** para permitir uma origem bloqueada, se necessário.  
- Use **IP \_ DROP \_ MEMBERSHIP** para sair do grupo (**IPV6 \_ DROP \_ MEMBERSHIP** para IPv6).  

As etapas a seguir se aplicam a aplicativos de origem controlada:

- Use **IP ADD SOURCE MEMBERSHIP \_ \_ \_ para** unir cada par grupo/origem.  
- Use **IP DROP SOURCE \_ \_ \_ MEMBERSHIP** para sair de cada grupo/origem ou use **IP DROP \_ \_ MEMBERSHIP** para deixar todas as fontes, se o mesmo endereço de grupo for usado por todas as fontes.  

A ordem na qual essas opções de soquete são definidas tem regras associadas. Para obter informações e informações de solução de problemas sobre opções de soquete multicast, consulte [Comportamento da opção de soquete multicast](multicast-socket-option-behavior.md).
