---
description: Página de navegação para opções de soquete do Windows Sockets (Winsock).
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
ms.openlocfilehash: 805f779965afc808e32952b58815c7b6bc528fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762181"
---
# <a name="socket-options"></a>Opções de soquete

Esta seção descreve as opções de soquete do Winsock para várias edições de sistemas operacionais Windows. Use as funções [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obter e definir opções de soquete. Para enumerar protocolos e descobrir Propriedades com suporte para cada protocolo instalado, use a função [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) .

Algumas opções de soquete exigem mais explicações do que essas tabelas podem ser transmitidas; essas opções contêm links para páginas adicionais.

<dl> <dt>

<span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**\_IP IPPROTO**
</dt> <dd> <dl> <dt>



Opções de soquete aplicáveis no nível de IPv4. Para obter mais informações, consulte [**as \_ Opções de soquete de IP do IPPROTO**](ipproto-ip-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**IPPROTO \_ IPv6**
</dt> <dd> <dl> <dt>



Opções de soquete aplicáveis no nível de IPv6. Para obter mais informações, consulte [**as \_ Opções de soquete do IPPROTO IPv6**](ipproto-ipv6-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**IPPROTO \_ RM**
</dt> <dd> <dl> <dt>



Opções de soquete aplicáveis no nível de multicast confiável. Para obter mais informações, consulte [**as \_ Opções de soquete do IPPROTO RM**](ipproto-rm-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**\_TCP IPPROTO**
</dt> <dd> <dl> <dt>



Opções de soquete aplicáveis no nível de TCP. Para obter mais informações, consulte [**as \_ Opções de soquete TCP IPPROTO**](ipproto-tcp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**IPPROTO \_ UDP**
</dt> <dd> <dl> <dt>



Opções de soquete aplicáveis no nível de UDP. Para obter mais informações, consulte [**as \_ Opções de soquete do IPPROTO UDP**](ipproto-udp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**NSPROTO \_ IPX**
</dt> <dd> <dl> <dt>



Opções de soquete aplicáveis no nível de IPX. Para obter mais informações, consulte [**as \_ Opções de soquete IPX NSPROTO**](nsproto-ipx-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**SOL para o \_ APPLETALK**
</dt> <dd> <dl> <dt>



Opções de soquete aplicáveis no nível de AppleTalk. Para obter mais informações, consulte [**as \_ Opções de soquete do sol**](sol-appletalk-socket-options.md)


</dt> </dl> </dd> <dt>

<span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**SOL \_ IRLMP**
</dt> <dd> <dl> <dt>



Opções de soquete aplicáveis ao nível do protocolo de gerenciamento de link de infravermelho. Para obter mais informações, consulte [**as \_ Opções de soquete sol IRLMP**](sol-irlmp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="SOL_SOCKET"></span><span id="sol_socket"></span>**soquete de SOL \_**
</dt> <dd> <dl> <dt>



Opções de soquete aplicáveis no nível do soquete. Para obter mais informações, consulte [**as \_ Opções de soquete de soquete de sol**](sol-socket-socket-options.md).


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Todas as \_ \* Opções de soquete se aplicam igualmente ao IPv4 e ao IPv6 (exceto por \_ difusão, já que a difusão não é implementada no IPv6).

 

 



