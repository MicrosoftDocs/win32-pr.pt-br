---
description: O auxiliar de protocolo de Internet (auxiliar de IP) auxilia a administração de rede do computador local, permitindo que os aplicativos recuperem informações sobre a configuração de rede do computador local e modifiquem essa configuração.
ms.assetid: 9eb8af78-612f-406c-ab92-4623b10a510e
title: Sobre o auxiliar de IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77445eb999b08bda038fbffc4de5d440b7a3e79c3fa921d50f6da4ccc1f42237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014184"
---
# <a name="about-ip-helper"></a>Sobre o auxiliar de IP

O auxiliar de protocolo de Internet (auxiliar de IP) auxilia a administração de rede do computador local, permitindo que os aplicativos recuperem informações sobre a configuração de rede do computador local e modifiquem essa configuração. O IP Helper também fornece mecanismos de notificação para garantir que um aplicativo seja notificado quando determinados aspectos da configuração de rede do computador local forem alterados.

Muitas das funções auxiliares de IP passam por parâmetros de estrutura que representam tipos de dados associados à tecnologia [base de informações de gerenciamento](/previous-versions/windows/desktop/mib/about-management-information-base) . As funções auxiliares de IP usam essas estruturas para representar várias informações de rede, como entradas de cache ARP. Como essas estruturas também são usadas pela API MIB, elas são descritas na [referência base de informações de gerenciamento](/previous-versions/windows/desktop/mib/management-information-base-reference). Embora a API auxiliar de IP use essas estruturas, o IP Helper é diferente da MIB (base de informações de gerenciamento) e do SNMP (Simple Network Management Protocol).

A documentação do IP Helper usa os termos "adaptador" e "interface" extensivamente. Um "adaptador" é um termo herdado que é uma forma abreviada de adaptador de rede que originalmente fazia referência a alguma forma de hardware de rede. Um adaptador é uma abstração no nível de vínculo de datalink.

Uma "interface" é um termo mais recente usado nos documentos RFC da IETF. As RFCs definem uma interface como um conceito abstrato que representa o anexo de um nó a um link. Uma interface é uma abstração em nível de IP.

Os termos do adaptador e da interface são usados de maneira ligeiramente intercambiável na documentação do auxiliar de IP. Na documentação do auxiliar de IP, uma lista de adaptadores pode incluir uma interface WAN de software, bem como a interface de loopback (nenhuma delas se refere a um dispositivo de hardware). Nas APIs auxiliares de IP, há um mapeamento um-para-um de adaptadores para interfaces.

O IP Helper fornece recursos nas seguintes áreas:

-   [Recuperando informações sobre a configuração de rede](retrieving-information-about-network-configuration.md)
-   [Gerenciando adaptadores de rede](managing-network-adapters.md)
-   [Gerenciando interfaces](managing-interfaces.md)
-   [Gerenciando endereços IP](managing-ip-addresses.md)
-   [Usando o protocolo de resolução de endereço](using-the-address-resolution-protocol.md)
-   [Recuperando informações sobre o protocolo de Internet e o protocolo de mensagem de controle da Internet](retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol.md)
-   [Gerenciando o roteamento](managing-routing.md)
-   [Recebendo notificação de eventos de rede](receiving-notification-of-network-events.md)
-   [Recuperando informações sobre o protocolo de controle de transmissão e o protocolo de datagrama do usuário](retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol.md)

 

 
