---
description: Esta seção descreve as práticas recomendadas para portar um aplicativo de difusão IPv6 para os recursos de multicast disponíveis com Windows Sockets.
ms.assetid: 12e491fd-650f-43b4-afa1-9f37b1c30240
title: Portando aplicativos de difusão para IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb54fec87be2aa6174de603d2c3e4d0e640156902002b1e87fab149a70e3d1ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641696"
---
# <a name="porting-broadcast-applications-to-ipv6"></a>Portando aplicativos de difusão para IPv6

Esta seção descreve as práticas recomendadas para portar um aplicativo de difusão IPv6 para os recursos de multicast disponíveis com Windows Sockets.

## <a name="comparing-ipv4-to-ipv6"></a>Comparando IPv4 com IPv6

A consideração mais importante ao se preparar para por portabilidade de um aplicativo de difusão IPv4 para IPv6 é esta: O IPv6 não tem nenhum conceito implementado de difusão. Em vez disso, o IPv6 usa multicast.

Multicast para IPv6 pode emular funcionalidades tradicionais de difusão encontradas em IPv4. Definir a opção de [soquete IPV6 \_ ADD \_ MEMBERSHIP](ipproto-ipv6-socket-options.md) com o endereço IPv6 definido como o escopo local do link, todos os nós de endereço (FF02::1) equivalem à difusão em endereços de difusão IPv4 usando a opção [ \_ soquete SO BROADCAST.](socket-options.md) Às vezes, esse endereço é chamado de *grupo multicast de todos os nós.* Para aplicativos que simplesmente querem emulação de difusão para IPv6, essa abordagem é operacionalmente equivalente. No entanto, uma diferença notável com iPv6 é que os multicasts no endereço do grupo multicast de todos os nós não são recebidos por padrão (as difusões IPv4 são recebidas por padrão). Os programadores de aplicativos devem usar a opção de soquete IPV6 ADD MEMBERSHIP para habilitar a recepção multicast de qualquer origem, incluindo o endereço do grupo multicast de todos os \_ \_ nós.

> [!Note]  
> No IPv6, a seleção de interface é especificada na estrutura de argumentos passada para a opção de soquete multicast ou IOCTL.

 

Porém, para transmissões mais robustas, mais seletivas e mais gerenciáveis para vários hosts, os desenvolvedores de aplicativos devem considerar a mudança para um modelo multicast.

## <a name="moving-to-multicast"></a>Mover para Multicast

Com o multicast, os programadores de aplicativos podem escolher seletivamente um par de origem/grupo específico, habilitando um modelo de recepção seletivo. O MLD (Multicast Listener Discovery) em IPv6 e a versão 3 do protocolo IGMPv3 no IPv4 são de suporte à programação multicast. Além disso, o multicast permite que os aplicativos bloqueiem especificamente (ou desbloqueiem) os senders em um grupo, protegendo ainda mais os aplicativos contra difusões não capacitadas. Essa funcionalidade está disponível para IPv4 (requer IGMPv3), bem como IPv6 (requer MLDv2).

Há dois cenários principais para programadores de aplicativos que usam multicast: aqueles portando de aplicativos de difusão IPv4 (ou multicast) para IPv6 e aqueles que criam novos aplicativos multicast IPv6.

Para portar aplicativos existentes, há duas opções para migrar para o multicast IPv6: usando opções de soquete e usando IOCTLs.

-   O uso de opções de soquete é uma abordagem baseada em alterações, que permite aos desenvolvedores alterar as propriedades do soquete conforme necessário (como bloquear ou desbloquear um remetente, adicionar uma nova fonte e assim por diante). Essa abordagem é mais intuitiva e a abordagem recomendada. Para obter mais informações sobre a abordagem baseada em alterações para programação multicast, consulte MLD e [IGMP usando Windows soquetes](igmp-and-windows-sockets.md).
-   O uso de IOCTLs é uma abordagem baseada em estado final, pois permite que os desenvolvedores forneçam um estado de soquete totalmente configurado, incluindo listas de inclusão e exclusão, com uma chamada. Para obter mais informações sobre a abordagem baseada em estado final, consulte Programação multicast baseada em [estado final.](final-state-based-multicast-programming.md)

Para aqueles que criam novos aplicativos multicast IPv6, a prática recomendada é usar opções de soquete, em vez de usar IOCTLs.

Há outra abordagem para criar aplicativos multicast com IPv6 e que envolve o uso da [**função WSAJoinLeaf.**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) Ao usar a **função WSAJoinLeaf** não é a prática recomendada, há situações que podem determinar seu uso. Por exemplo, uma desvantagem ao usar opções de soquete no Windows Server 2003 e anteriores é que elas são específicas da versão de IP. Nessas versões mais antigas do Windows, diferentes opções de soquetes devem ser para IPv6 e IPv4. No Windows Vista e posterior, há suporte para novas opções de soquete que podem ser usadas com IPv4 e IPv6. A **função WSAJoinLeaf,** por outro lado, é agnostic de protocolo e versão de IP e, portanto, pode ser uma abordagem útil para a criação de um aplicativo que deve funcionar com várias versões de IP no Windows Server 2003 e anteriores. O uso **da função WSAJoinLeaf** pode ser mais apropriado em determinadas situações em que o agnosticismo de protocolo e versão de IP é necessário.

 

 



