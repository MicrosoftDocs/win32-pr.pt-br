---
description: para dar suporte a IPv4 e IPv6 no Windows XP com Service Pack 1 (SP1) e no Windows Server 2003, um aplicativo precisa criar dois soquetes, um soquete para uso com IPv4 e um soquete para uso com IPv6.
ms.assetid: 7ae49081-ffb5-4eee-b488-2541398e7acc
title: Soquetes de Dual-Stack para aplicativos Winsock IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424580569fb3bed5e81c6232cb99dc2d53a30af1ab2c23c9b4afa6945c0a6eb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132659"
---
# <a name="dual-stack-sockets-for-ipv6-winsock-applications"></a>Soquetes de Dual-Stack para aplicativos Winsock IPv6

para dar suporte a IPv4 e IPv6 no Windows XP com Service Pack 1 (SP1) e no Windows Server 2003, um aplicativo precisa criar dois soquetes, um soquete para uso com IPv4 e um soquete para uso com IPv6. Esses dois soquetes devem ser tratados separadamente pelo aplicativo.

Windows O Vista e versões posteriores oferecem a capacidade de criar um único soquete IPv6 que pode lidar com tráfego IPv6 e IPv4. Por exemplo, um soquete de escuta TCP para IPv6 é criado, colocado em modo de pilha dupla e vinculado à porta 5001. Esse soquete de pilha dupla pode aceitar conexões de clientes IPv6 TCP conectando-se à porta 5001 e de clientes TCP IPv4 conectando-se à porta 5001. Esse recurso permite um design de aplicativo bastante simplificado e reduz a sobrecarga de recursos necessária ao lançamento de operações em dois soquetes separados.

## <a name="creating-a-dual-stack-socket"></a>Criando um soquete de Dual-Stack

por padrão, um soquete ipv6 criado no Windows Vista e posterior opera apenas sobre o protocolo ipv6. Para tornar um soquete IPv6 em um soquete de pilha dupla, a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) deve ser chamada com a opção de **soquete \_ V6ONLY do IPv6** para definir esse valor como zero antes que o soquete seja associado a um endereço IP. Quando a opção de soquete de **\_ V6ONLY IPv6** é definida como zero, um soquete criado para a família de endereços **\_ INET6 de AF** pode ser usado para enviar e receber pacotes de e para um endereço IPv6 ou um endereço de IPv4 mapeado.

## <a name="ip-addresses-with-a-dual-stack-socket"></a>Endereços IP com um soquete de Dual-Stack

Os soquetes de pilha dupla sempre exigem endereços IPv6. A capacidade de interagir com um endereço IPv4 requer o uso do formato de endereço IPv6 mapeado para IPv4. Todos os endereços IPv4 devem ser representados no formato de endereço IPv6 mapeado para IPv4, o que permite que um aplicativo somente IPv6 se comunique com um nó IPv4. O formato de endereço IPv6 mapeado para IPv4 permite que o endereço IPv4 de um nó IPv4 seja representado como um endereço IPv6. O endereço IPv4 é codificado em 32 bits de ordem inferior do endereço IPv6 e os bits 96 de ordem superior contêm o prefixo fixo 0:0: 0:0: 0: FFFF. O formato de endereço IPv6 mapeado para IPv4 é especificado no RFC 4291. Para obter mais informações, consulte [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291). A \_ macro IN6ADDR SETV4MAPPED em *Mstcpip. h* pode ser usada para converter um endereço IPv4 para o formato de endereço IPv6 mapeado para IPv4 necessário.

Se o protocolo subjacente for realmente IPv4, o endereço IPv4 será mapeado em um formato de endereço IPv6 mapeado para IPv4. Ou seja, o campo família na estrutura [SOCKADDR](sockaddr-2.md) indica AF \_ INET6, mas um endereço IPv6 mapeado para IPv4 é codificado na estrutura de endereços IPv6. Para um soquete de pilha dupla no modo de escuta, isso significa que todas as conexões IPv4 aceitas retornarão um endereço IPv6 mapeado para IPv4. Para um soquete de pilha dupla que está se conectando a um destino IPv4, a estrutura SOCKADDR passada para Connect deve ser um endereço IPv6 mapeado para IPv4. Os aplicativos devem cuidar para tratar esses endereços IPv6 mapeados para IPv4 adequadamente e usá-los apenas com soquetes de pilha dupla. Se um endereço IP for passado para um soquete IPv4 regular, o endereço deverá ser um endereço IPv4 regular, não um endereço IPv6 mapeado pelo IPv4.

## <a name="potential-issues-using-a-dual-stack-socket"></a>Problemas em potencial usando um soquete de Dual-Stack

Uma possível armadilha para os aplicativos é obter um endereço IPv6 mapeado para IPv4 em um soquete de pilha dupla e, em seguida, tentar usar o endereço IP retornado em um soquete somente IPv6 diferente. Por exemplo, as funções [**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname) ou [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) podem retornar um endereço IPv6 mapeado para IPv4 quando usado em um soquete de pilha dupla. Se o endereço IPv6 mapeado para IPv4 retornado for usado posteriormente em um soquete diferente que não foi definido como pilha dupla (um soquete somente IPv6, que é o comportamento padrão quando um soquete é criado), qualquer uso desse soquete somente IPv6 com um endereço IPv6 mapeado para IPv4 falhará. O formato de endereço IPv6 mapeado para IPv4 só pode ser usado em um soquete de pilha dupla.

Em um soquete de datagrama de pilha dupla, se um aplicativo exigir que a função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retorne informações de pacote em uma estrutura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) para datagramas recebidos por IPv4, a opção [IP \_ PKTINFO](ip-pktinfo.md) Socket deverá ser definida como true no soquete. Se apenas a [opção \_ PKTINFO IPv6](ipv6-pktinfo.md) for definida como true no soquete, as informações de pacote serão fornecidas para datagramas recebidos via IPv6, mas podem não ser fornecidas para datagramas recebidos via IPv4.

Se um aplicativo tentar definir a opção de soquete de [IP \_ PKTINFO](ip-pktinfo.md) em um soquete de datastack de pilha dupla e o IPv4 estiver desabilitado no sistema, a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) falhará e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará com um erro de [WSAEINVAL](windows-sockets-error-codes-2.md). Esse mesmo erro também é retornado pela função **setsockopt** como resultado de outros erros. Se um aplicativo tentar definir uma opção de \_ soquete de nível de IP IPPROTO em um soquete de pilha dupla e falhar com [WSAEINVAL](windows-sockets-error-codes-2.md), o aplicativo deverá determinar se o IPv4 está desabilitado no computador local. Um método que pode ser usado para detectar se o IPv4 está habilitado ou desabilitado é chamar a função de [**soquete**](/windows/desktop/api/Winsock2/nf-winsock2-socket) com o parâmetro *AF* definido como série AF para \_ tentar criar um soquete IPv4. Se a função **Socket** falhar e **WSAGetLastError** retornar um erro de [WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md), isso significará que o IPv4 não está habilitado. Nesse caso, uma falha de função **setsockopt** ao tentar definir a opção de soquete de PKTINFO de IP \_ pode ser ignorada pelo aplicativo. Caso contrário, uma falha ao tentar definir a \_ opção de soquete IP PKTINFO deve ser tratada como um erro inesperado.

Para um soquete de pilha dupla ao enviar datagramas com a função [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) e um aplicativo desejar especificar um endereço de origem IP local específico a ser usado, o método para lidar com isso dependerá do endereço IP de destino. Ao enviar para um endereço de destino IPv4 ou um endereço de destino IPv6 mapeado para IPv4, um dos objetos de dados de controle passados na estrutura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) apontados pelo parâmetro *lpMsg* deve conter uma estrutura [**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) que contém o endereço de origem IPv4 local a ser usado para envio. Ao enviar para um endereço de destino IPv6 que não é um endereço IPv6 mapeado para IPv4, um dos objetos de dados de controle passados na estrutura **WSAMSG** apontada pelo parâmetro *lpMsg* deve conter uma estrutura [**In6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) contendo o endereço de origem IPv6 local a ser usado para envio.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[guia de IPv6 para aplicativos de Windows sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Alterando estruturas de dados para aplicativos Winsock do IPv6](changing-data-structures-2.md)
</dt> <dt>

[Chamadas de função para aplicativos Winsock IPv6](function-calls-2.md)
</dt> <dt>

[Uso de endereços IPv4 codificados](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Problemas de interface do usuário para aplicativos Winsock do IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocolos subjacentes para aplicativos Winsock IPv6](underlying-protocols-2.md)
</dt> <dt>

[**getemparelhaname**](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname)
</dt> <dt>

[**em \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[**In6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[\_PKTINFO IP](ip-pktinfo.md)
</dt> <dt>

[\_PKTINFO IPv6](ipv6-pktinfo.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> <dt>

[**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)
</dt> </dl>

 

 
