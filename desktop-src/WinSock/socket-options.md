---
description: Página de navegação para Windows soquetes (Winsock).
ms.assetid: e2831f76-4499-45b6-bc60-2908ec3a246c
title: Opções de soquete
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPPROTO_IP
- IPPROTO_IPV6
- IPPROTO_RM
- IPPROTO_TCP
- IPPROTO_UDP
- NSPROTO_IPX
- SOL_APPLETALK
- SOL_IRLMP
- SOL_SOCKET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 37da2ff25fe51b08c036fe75ac55b9b3fdb508d1d24dcc151ecd87e04e3b63b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119383876"
---
# <a name="socket-options"></a>Opções de soquete

Esta seção descreve as Opções de Soquete winsock para várias edições Windows sistemas operacionais. Use as [**funções getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obter e definir mais opções de soquete. Para enumerar protocolos e descobrir propriedades com suporte para cada protocolo instalado, use a [**função WSAEnumProtocols.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)

Algumas opções de soquete exigem mais explicação do que essas tabelas podem transmitir; essas opções contêm links para páginas adicionais.

<dl> <dt>

<span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**IPPROTO \_ IP**
</dt> <dd> <dl> <dt>



Opções de soquete aplicáveis no nível IPv4. Para obter mais informações, consulte as [**Opções de soquete \_ IP IPPROTO**](ipproto-ip-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**IPPROTO \_ IPV6**
</dt> <dd> <dl> <dt>



Opções de soquete aplicáveis no nível IPv6. Para obter mais informações, consulte Opções [**de soquete \_ IPV6 IPPROTO**](ipproto-ipv6-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**IPPROTO \_ RM**
</dt> <dd> <dl> <dt>



Opções de soquete aplicáveis no nível de multicast confiável. Para obter mais informações, consulte opções [**de soquete IPPROTO \_ RM**](ipproto-rm-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**IPPROTO \_ TCP**
</dt> <dd> <dl> <dt>



Opções de soquete aplicáveis no nível TCP. Para obter mais informações, consulte Opções [**de soquete \_ TCP IPPROTO**](ipproto-tcp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**IPPROTO \_ UDP**
</dt> <dd> <dl> <dt>



Opções de soquete aplicáveis no nível UDP. Para obter mais informações, consulte Opções [**de soquete \_ UDP IPPROTO**](ipproto-udp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**NSPROTO \_ IPX**
</dt> <dd> <dl> <dt>



Opções de soquete aplicáveis no nível de IPX. Para obter mais informações, consulte as Opções [**de soquete \_ IPX NSPROTO**](nsproto-ipx-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**SOL \_ APPLETALK**
</dt> <dd> <dl> <dt>



Opções de soquete aplicáveis no nível do AppleTalk. Para obter mais informações, consulte as Opções [**\_ de soquete SOL APPLETALK**](sol-appletalk-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**SOL \_ IRLMP**
</dt> <dd> <dl> <dt>



Opções de soquete aplicáveis no nível do Protocolo de Gerenciamento de Link InfraRed. Para obter mais informações, consulte as Opções [**de \_ soquete DOLMP do SOL.**](sol-irlmp-socket-options.md)


</dt> </dl> </dd> <dt>

<span id="SOL_SOCKET"></span><span id="sol_socket"></span>**SOQUETE SOL \_**
</dt> <dd> <dl> <dt>



Opções de soquete aplicáveis no nível do soquete. Para obter mais informações, consulte as Opções [**de \_ soquete sol socket**](sol-socket-socket-options.md).


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Todas as opções de soquete SO se aplicam igualmente a \_ \* IPv4 e IPv6 (exceto SO BROADCAST, pois \_ a difusão não é implementada no IPv6).

 

 



