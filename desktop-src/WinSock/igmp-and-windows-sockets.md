---
description: O Windows Sockets permite a descoberta de ouvinte multicast (MLD) no IPv6 e o protocolo IGMP no IPv4 para aplicativos multicast por meio do uso de opções de soquete e de IOCTLs.
ms.assetid: a5de4273-e86e-4f13-b068-256cb38706d4
title: MLD e IGMP usando soquetes do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6cb9f9c345463e283adea0136037d7ccd03cebd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164470"
---
# <a name="mld-and-igmp-using-windows-sockets"></a>MLD e IGMP usando soquetes do Windows

O Windows Sockets permite a descoberta de ouvinte multicast (MLD) no IPv6 e o protocolo IGMP no IPv4 para aplicativos multicast por meio do uso de opções de soquete e de IOCTLs. Esta página descreve as opções de soquete que habilitam a programação de multicast e descreve como elas são usadas. Para obter definições de cada opção de soquete, consulte a página [Opções de soquete](socket-options.md) .

Para obter informações sobre como usar os IOCTLs para programação de multicast, consulte [programação de multicast com base no estado final](final-state-based-multicast-programming.md) mais adiante nesta seção.

No Windows Vista e posterior, um conjunto de opções de soquete está disponível para programação de multicast que dá suporte a endereços IPv6 e IPv4. Essas opções de soquete são independentes de IP e podem ser usadas no IPv6 e no IPv4. No IPv6, essas opções de soquete usam o MLDv2. No IPv4, essas opções de soquete usam IGMPv3. Essas opções independentes de IP são as opções de soquete preferenciais para programação multicast no Windows Vista e posterior. O Windows Sockets usa as seguintes opções de soquete: 

| Opção de soquete               | Tipo de argumento                                            |
|-----------------------------|----------------------------------------------------------|
| \_origem do bloco mcast \_        | [**Grupo \_ Estrutura de \_ req de origem**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| \_grupo de junção mcast \_          | [**Grupo \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_req) Estrutura de req.                |
| \_grupo de \_ origem de ingresso mcast \_  | [**Grupo \_ Estrutura de \_ req de origem**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| MCAST \_ sair do \_ grupo         | [**Grupo \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_req) Estrutura de req.                |
| MCAST \_ sair \_ do \_ grupo de origem | [**Grupo \_ Estrutura de \_ req de origem**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| \_origem de desbloqueio mcast \_      | [**Grupo \_ Estrutura de \_ req de origem**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |



 

Um conjunto de opções de soquete está disponível para a programação de multicast que dá suporte apenas a endereços IPv6. Essas opções de soquete usam MLDv1 ou MLDv2. A versão do MLD usada depende da versão do Windows. O MLDv2 tem suporte no Windows Vista e versões posteriores. O Windows Sockets usa as seguintes opções de soquete: 

| Opção de soquete          | Tipo de argumento                             |
|------------------------|-------------------------------------------|
| \_Adicionar \_ Associação de IPv6  | estrutura de [**\_ mreq IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) |
| \_Associação de remoção de IPv6 \_ | estrutura de [**\_ mreq IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) |



 

Um conjunto de opções de soquete está disponível para programação multicast que oferece suporte a endereços IPv4 somente. Essas opções de soquete usam IGMPv3 ou IGMPv2. A versão do IGMP usada depende da versão do Windows. O IGMPv3 tem suporte no Windows Vista e posterior. O Windows Sockets usa as seguintes opções de soquete:

| Opção de soquete                | Tipo de argumento                                        |
|------------------------------|------------------------------------------------------|
| \_Adicionar \_ Associação de IP          | estrutura de [**\_ mreq IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq)                |
| IP \_ Adicionar \_ Associação de origem \_  | estrutura de [**\_ \_ origem de mreq IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |
| \_origem do bloco de IP \_            | estrutura de [**\_ \_ origem de mreq IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |
| \_Associação IP drop \_         | estrutura de [**\_ mreq IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq)                |
| \_Associação de \_ origem IP drop \_ | estrutura de [**\_ \_ origem de mreq IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |
| \_origem de desbloqueio de IP \_          | estrutura de [**\_ \_ origem de mreq IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |



 

Quando o IGMPv3 está disponível, o IP \_ Adicionar \_ Associação de origem, origem do bloco de IP \_ \_ \_ , associação de \_ fonte IP drop \_ \_ e opções de origem de \_ desbloqueio de IP \_ são tratados com mais eficiência, pois o roteador pode manipular a filtragem. Quando apenas IGMPv2 está disponível, o host deve lidar com a filtragem.

Há duas categorias nas quais a maioria dos aplicativos provavelmente se enquadra: qualquer fonte e fonte controlada.

-   Todos os aplicativos **de origem** aceitam todas as fontes por padrão, permitindo que fontes individuais sejam desativadas conforme necessário. Um exemplo de aplicativo de qualquer fonte é uma chamada de conferência de vídeo que permite que todos os destinatários participem.
-   Os aplicativos **de origem controlada** limitam as fontes a uma determinada lista, como uma estação de rádio da Internet, ou a difusão de um evento notável. O processo de usar as opções de soquete é um pouco diferente para cada.

No Windows Vista e posterior, as seguintes etapas se aplicam a aplicativos de origem:

- Use **o \_ \_ grupo de junção mcast** para ingressar em um grupo.  
- Use **a \_ \_ origem do bloco mcast** para desativar uma determinada origem, se necessário.  
- Use **mcast \_ desbloquear \_ origem** para reabilitar uma fonte bloqueada, se necessário.  
- Use **mcast \_ Leave \_ Group** para sair do grupo.  

No Windows Vista e posterior, as seguintes etapas se aplicam a aplicativos de origem controlada:

- Use **o \_ \_ \_ grupo de origem mcast Join** para unir cada par de grupo/fonte.  
- Use **mcast \_ deixar \_ o \_ grupo de origem** para sair de cada grupo/origem ou use o **\_ \_ grupo de saída mcast** para deixar todas as fontes, se o mesmo endereço de grupo for usado por todas as fontes.  

As etapas a seguir se aplicam a aplicativos de origem:

- Usar **IP \_ Adicionar \_ Associação** para ingressar em um grupo (**IPv6 \_ Adicionar \_ Associação** para IPv6).  
- Use **a \_ \_ origem do bloco de IP** para desativar uma determinada origem, se necessário.  
- Use **a \_ \_ origem de desbloqueio de IP** para permitir novamente uma fonte bloqueada, se necessário.  
- Use **a \_ \_ Associação IP drop** para sair do grupo (**IPv6 \_ Remove \_ membership** para IPv6).  

As etapas a seguir se aplicam a aplicativos de origem controlada:

- Usar **IP \_ Adicionar \_ \_ Associação de origem** para ingressar em cada par de grupo/fonte.  
- Use **a \_ \_ \_ Associação de origem IP drop** para deixar cada grupo/origem ou use a **\_ \_ Associação IP drop** para deixar todas as fontes, se o mesmo endereço de grupo for usado por todas as fontes.  

A ordem na qual essas opções de soquete estão definidas tem regras associadas. Para obter informações e informações de solução de problemas em opções de soquete de multicast, consulte [comportamento da opção de soquete multicast](multicast-socket-option-behavior.md).
