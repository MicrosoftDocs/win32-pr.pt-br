---
description: Esta seção descreve as práticas recomendadas para portar um aplicativo de difusão IPv6 para os recursos de multicast disponíveis com o Windows Sockets.
ms.assetid: 12e491fd-650f-43b4-afa1-9f37b1c30240
title: Portando aplicativos de difusão para IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f7dce09db6822a6f9b0a61873ca6bbff5a256b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461109"
---
# <a name="porting-broadcast-applications-to-ipv6"></a>Portando aplicativos de difusão para IPv6

Esta seção descreve as práticas recomendadas para portar um aplicativo de difusão IPv6 para os recursos de multicast disponíveis com o Windows Sockets.

## <a name="comparing-ipv4-to-ipv6"></a>Comparando IPv4 com IPv6

A consideração mais notável ao se preparar para portar um aplicativo de difusão IPv4 para IPv6 é: o IPv6 não tem nenhum conceito de difusão implementado. Em vez disso, o IPv6 usa multicast.

O multicast para IPv6 pode emular os recursos de difusão tradicionais encontrados no IPv4. A definição da opção [IPv6 adicionar soquete de \_ \_ Associação](ipproto-ipv6-socket-options.md) com o endereço IPv6 definido como o escopo de vínculo local todos os nós endereço (FF02:: 1) é equivalente à difusão de endereços de difusão IPv4 usando a opção de soquete de [ \_ difusão](socket-options.md) . Esse endereço às vezes é chamado de *grupo de multicast de todos os nós*. Para aplicativos que simplesmente desejam emulação de difusão para IPv6, essa abordagem é operacionalmente equivalente. No entanto, uma diferença notável com o IPv6 é que as difusões seletivas no endereço do grupo multicast de todos os nós não são recebidas por padrão (as transmissões IPv4 são recebidas por padrão). Os programadores de aplicativos devem usar \_ a \_ opção IPv6 adicionar soquete de associação para habilitar a recepção multicast de qualquer fonte, incluindo o endereço de grupo multicast de todos os nós.

> [!Note]  
> No IPv6, a seleção de interface é especificada na estrutura de argumento passada para a opção de soquete multicast ou para o IOCTL.

 

Mas, para transmissões mais avançadas, mais robustas e mais gerenciáveis para vários hosts, os desenvolvedores de aplicativos devem considerar a mudança para um modelo de multicast.

## <a name="moving-to-multicast"></a>Migrando para multicast

Com o multicast, os programadores de aplicativos podem escolher seletivamente um par de origem/grupo específico, habilitando um modelo de recepção seletiva. A descoberta de ouvinte multicast (MLD) no IPv6 e na versão 3 do protocolo IGMPv3 (Internet Group Management Protocol) no IPv4 dão suporte à programação de multidifusão. Além disso, o multicast permite que os aplicativos bloqueiem (ou desbloqueiem) os remetentes em um grupo, protegendo ainda mais os aplicativos contra difusores não autorizados. Esse recurso está disponível para IPv4 (requer IGMPv3), bem como IPv6 (requer MLDv2).

Há dois cenários principais para programadores de aplicativos usando multicast: a portabilidade de aplicativos de difusão IPv4 (ou multicast) para IPv6 e os que criam novos aplicativos de multicast IPv6.

Para portar aplicativos existentes, há duas opções para mover para o multicast IPv6: usando opções de soquete e usando IOCTLs.

-   O uso de opções de soquete é uma abordagem baseada em alteração, que permite aos desenvolvedores alterar as propriedades do soquete conforme necessário (como bloquear ou desbloquear um remetente, adicionar uma nova fonte e assim por diante). Essa abordagem é mais intuitiva e a abordagem recomendada. Para obter mais informações sobre a abordagem baseada em alteração para programação de multicast, consulte [MLD e IGMP usando soquetes do Windows](igmp-and-windows-sockets.md).
-   O uso de IOCTLs é uma abordagem baseada em estado final, pois permite que os desenvolvedores forneçam um estado de soquete totalmente configurado, incluindo listas de inclusão e exclusão, com uma chamada. Para obter mais informações sobre a abordagem baseada em estado final, consulte [programação de multicast com base no estado final](final-state-based-multicast-programming.md).

Para aqueles que criam novos aplicativos de multicast IPv6, a prática recomendada é usar as opções de soquete, em vez de usar os IOCTLs.

Há uma outra abordagem para criar aplicativos multicast com IPv6, e isso envolve o uso da função [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) . Embora o uso da função **WSAJoinLeaf** não seja a prática recomendada, há situações que podem ditar seu uso. Por exemplo, uma desvantagem de usar as opções de soquete no Windows Server 2003 e versões anteriores é que elas são específicas de versão de IP. Nessas versões anteriores do Windows, diferentes opções de soquetes devem ser para IPv6 e IPv4. No Windows Vista e posterior, há suporte para novas opções de soquete que podem ser usadas com IPv4 e IPv6. A função **WSAJoinLeaf** , por outro lado, é independente do protocolo e da versão do IP e, portanto, pode ser uma abordagem útil para criar um aplicativo que deve funcionar com várias versões de IP no Windows Server 2003 e versões anteriores. Usar a função **WSAJoinLeaf** pode ser mais apropriado em determinadas situações em que o protocolo e o indiferente de versão IP são necessários.

 

 



