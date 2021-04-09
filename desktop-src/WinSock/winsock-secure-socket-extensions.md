---
description: As extensões de soquete seguro para Winsock permitem que um aplicativo de soquete controle a segurança de seu tráfego em uma rede.
ms.assetid: 023a9f96-814f-40c3-a186-ae0a0c9baef2
title: Extensões do Winsock Secure Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b62ee593b3abbb3bb0f8dbf27b79d6868f04fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010480"
---
# <a name="winsock-secure-socket-extensions"></a>Extensões do Winsock Secure Socket

As extensões de soquete seguro para Winsock permitem que um aplicativo de soquete controle a segurança de seu tráfego em uma rede. Essas extensões permitem que um aplicativo forneça a política de segurança e os requisitos para seu tráfego de rede e consulte as configurações de segurança aplicadas. Por exemplo, um aplicativo pode usar essas extensões para consultar o token de segurança de mesmo nível que pode ser usado para executar verificações de acesso no nível do aplicativo.

As extensões de soquete seguro destinam-se a integrar os serviços fornecidos pelo IPsec e outros protocolos de segurança com a estrutura do Winsock. Antes do Windows Vista, no Windows Server 2003 e no Windows XP, o IPsec foi configurado por um administrador por meio de políticas locais e de domínio. No Windows Vista, as extensões de soquete seguro permitem que os aplicativos configurem total ou parcialmente e controlem a segurança de seu tráfego de rede no nível do soquete.

Os aplicativos já podem proteger o tráfego de rede usando APIs públicas, como gerenciamento de IPsec, plataforma de filtragem do Windows e SSPI (interface do provedor de suporte de segurança). No entanto, o uso dessas APIs pode tornar o aplicativo mais difícil de desenvolver e pode dificultar a configuração e a implantação. As extensões do Winsock Secure Socket foram projetadas para simplificar o desenvolvimento de aplicativos de rede que exigem o tráfego de rede seguro, permitindo que o Winsock lide com a maior parte da complexidade.

Essas extensões de soquete seguro estão disponíveis no Windows Vista e versões posteriores.

## <a name="secure-socket-functions"></a>Funções de soquete seguro

As funções de extensão de soquete seguro são as seguintes:

-   [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname)
-   [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer)
-   [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity)
-   [**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation)
-   [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)
-   [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity)

> [!Note]  
> Atualmente, as funções de soquete seguro dão suporte apenas ao protocolo IPsec e estão disponíveis no Windows Vista e versões posteriores.

 

As estruturas e enumerações usadas pelas funções de soquete seguro são as seguintes:

-   [**\_nome de \_ destino de par de soquete \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_peer_target_name)
-   [**\_protocolo de segurança de soquete \_**](/windows/desktop/api/Mstcpip/ne-mstcpip-socket_security_protocol)
-   [**\_informações de \_ consulta de segurança de soquete \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_info)
-   [**\_modelo de \_ consulta de segurança de soquete \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_template)
-   [**\_configurações de segurança de soquete \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings)
-   [**configurações de segurança de soquete \_ \_ \_ IPSec**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings_ipsec)

As funções de soquete seguro são simples de usar para aplicativos normais e são flexíveis o suficiente para aplicativos que precisam de um alto grau de controle sobre sua segurança. Essas funções possibilitam manter o mecanismo de segurança subjacente oculto do aplicativo. Um aplicativo pode especificar requisitos de segurança genéricos e permitir que o administrador controle o protocolo de segurança que é usado para dar suporte aos requisitos. Embora seja possível estender essas funções para adicionar outros protocolos de segurança, no momento, apenas o IPsec se integra com as funções de soquete seguro.

A função [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) permite que um aplicativo habilite a segurança e aplique configurações de segurança antes que uma conexão seja estabelecida.

A função [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) permite que um aplicativo especifique o nome de destino correspondente a uma entidade par. O protocolo de segurança selecionado usará essas informações ao autenticar o par. Esse recurso aborda as preocupações com ataques intermediários confiáveis.

A função [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) é usada para excluir um nome de par especificado anteriormente para um soquete.

Depois que uma conexão é estabelecida, a função [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) permite que um aplicativo consulte as propriedades de segurança da conexão, que pode incluir o acesso de pares ou o token de acesso do computador.

Depois que uma conexão é estabelecida, a função [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) permite que um aplicativo represente a entidade de segurança correspondente a um par de soquetes para executar a autorização em nível de aplicativo.

O [**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) permite que um aplicativo encerre a representação de um par de soquetes.

## <a name="secure-socket-architecture"></a>Arquitetura de soquete seguro

![arquitetura básica das extensões de soquete de segurança do Winsock](images/ss-arch.png)

-   Um aplicativo chama as funções de soquete seguro para definir ou consultar as configurações de segurança de um soquete.
-   As funções de soquete seguro são um conjunto de funções de extensão de tipo seguro que encapsulam chamadas para a função [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) usando valores definidos recentemente para o parâmetro *DwIoControlCode* disponível no Windows Vista e posterior. Esses IOCTLs são tratados pela pilha de rede.
-   A pilha de rede direcionará a chamada para a [camada de aplicação (ALE)](../fwp/application-layer-enforcement--ale-.md) junto com a alça do ponto de extremidade. Para as funções [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname), [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)e [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) , a EPA definirá as configurações do aplicativo no ponto de extremidade local. Para a função [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) , a Ale lerá as informações solicitadas dos pontos de extremidade locais e remotos aplicáveis.
-   Com base em eventos de soquete, a ALE (aplicação de camada de aplicativo) impõe políticas para a arquitetura de soquete seguro usando a plataforma de filtragem do Windows. Para obter mais informações, consulte [sobre a plataforma de filtragem do Windows](../fwp/about-windows-filtering-platform.md) e a [camada de aplicação (ALE)](../fwp/application-layer-enforcement--ale-.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a plataforma de filtragem do Windows](../fwp/about-windows-filtering-platform.md)
</dt> <dt>

[Exemplos de Winsock avançados usando extensões de soquete seguro](advanced-winsock-samples-using-secure-socket-extensions.md)
</dt> <dt>

[Aplicação da camada de aplicativo (EPA)](../fwp/application-layer-enforcement--ale-.md)
</dt> <dt>

[Configuração de IPsec](../fwp/ipsec-configuration.md)
</dt> <dt>

[Funções IPsec](../fwp/fwp-ipsec-functions.md)
</dt> <dt>

[Programação de Winsock seguro](secure-winsock-programming.md)
</dt> <dt>

[SSPI (interface do provedor de suporte de segurança)](../rpc/security-support-provider-interface-sspi-.md)
</dt> <dt>

[Usando extensões de soquete seguro](using-secure-socket-extensions.md)
</dt> <dt>

[Plataforma de filtragem do Windows](../fwp/windows-filtering-platform-start-page.md)
</dt> <dt>

[Funções da API da Windows Filtering Platform](../fwp/fwp-functions.md)
</dt> </dl>

 

 
