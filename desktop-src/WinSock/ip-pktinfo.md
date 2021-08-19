---
description: Permite que um aplicativo habilita ou desabilite o retorno de informações de pacote pela função WSARecvMsg em um soquete IPv4.
ms.assetid: C6246899-0220-4F88-B43B-CED1B1FF7DC3
title: IP_PKTINFO de soquete (Ws2ipdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ba653b4ece11086706493b920e1ed650b66eecdd6e788a5edfe259cf9eb9f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097786"
---
# <a name="ip_pktinfo-socket-option"></a>Opção \_ de soquete IP PKTINFO

A opção de soquete IP PKTINFO permite que um aplicativo habilita ou desabilite o retorno de informações de pacote pela \_ [**função LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) em um soquete IPv4..

Para consultar o status dessa opção de soquete, chame a [**função getsockopt.**](/windows/desktop/api/winsock/nf-winsock-getsockopt) Para definir essa opção, chame a [**função setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) com os parâmetros a seguir.

## <a name="socket-option-value"></a>Valor da opção socket

A constante que representa essa opção de soquete é 19.

## <a name="syntax"></a>Sintaxe


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IP,   // level
  (int) IP_PKTINFO, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IP,   // level
  (int) IP_PKTINFO, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*s* \[ em\]
</dt> <dd>

Um descritor que identifica o soquete.

</dd> <dt>

*nível* \[ Em\]
</dt> <dd>

O nível no qual a opção é definida. Use **IP IPPROTO \_** para esta operação.

</dd> <dt>

*optname* \[ Em\]
</dt> <dd>

A opção de soquete para a qual obter ou definir o valor. Use IP \_ PKTINFO para esta operação.

</dd> <dt>

*optval* \[ out\]
</dt> <dd>

Um ponteiro para o buffer que contém o valor da opção a ser definida. Esse parâmetro deve apontar para buffer igual ou maior que o tamanho de um **valor DWORD.**

Esse valor é tratado como um valor booliana com 0 usado para indicar **FALSE** (desabilitado) e um valor não zero para indicar **TRUE** (habilitado).

</dd> <dt>

*optlen* \[ in, out\]
</dt> <dd>

Um ponteiro para o tamanho, em bytes, do buffer *de aceitação.* Esse tamanho deve ser igual ou maior que o tamanho de um **valor DWORD.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a operação for concluída com êxito, a [**função getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) ou [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) retornará zero.

Se a operação falhar, um valor de SOCKET ERROR será retornado e um código de erro específico poderá ser recuperado chamando \_ [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).



| Código do erro                                                                                                                                              | Significado                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Uma chamada [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) bem-sucedida deve ocorrer antes de usar essa função.<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | O subsistema de rede falhou.<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Um dos *parâmetros optval* ou *optlen* aponta para a memória que não está em uma parte válida do espaço de endereço do usuário. Esse erro também será retornado se o valor apontado pelo parâmetro *optlen* for menor que o tamanho de um **valor DWORD.**<br/> |
| <dl> <dt>**[Wsaeinprogress](windows-sockets-error-codes-2.md)**</dt> </dl>       | Uma chamada Windows Sockets 1.1 está em andamento ou o provedor de serviços ainda está processando uma função de retorno de chamada.<br/>                                                                                                                            |
| <dl> <dt>**[Wsaeinval](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Foi fornecido um argumento inválido. Esse erro será retornado se o *parâmetro de nível* for desconhecido ou inválido. No Windows Vista e posterior, esse erro também será retornado se o soquete estiver em um estado de transição.<br/>                                     |
| <dl> <dt>**[Wsaenoprotoopt](windows-sockets-error-codes-2.md)**</dt> </dl>       | A opção é desconhecida ou não é compatível com a família de protocolos indicada. Esse erro será retornado se o *parâmetro de* tipo para o descritor de soquete passado no parâmetro *s* não for **SOCK \_ DGRAM** ou **SOCK \_ RAW.** <br/>                          |
| <dl> <dt>**[Wsaenotsock](windows-sockets-error-codes-2.md)**</dt> </dl>             | O descritor não é um soquete.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Comentários

A [**função getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chamada com a opção de soquete IP PKTINFO permite que um aplicativo determine se as informações de pacote devem ser retornadas pela função \_ LPFN_WSARECVMSG [**(WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)para um soquete IPv4.

A [**função setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) chamada com a opção de soquete IP PKTINFO permite que um aplicativo habilita ou desabilite o retorno de informações de pacote pela função \_ LPFN_WSARECVMSG [**(WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) A opção \_ IP PKTINFO para um soquete está desabilitada (definida como **FALSE**) por padrão.

Quando essa opção de soquete está habilitada em um soquete IPv4 do tipo **SOCK \_ DGRAM** ou **SOCK \_ RAW**, a função [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retorna informações de pacote na estrutura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) apontada pelo *parâmetro lpMsg.* Um dos objetos de dados de controle na estrutura **WSAMSG** retornada conterá um na estrutura [**\_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) usada para armazenar informações de endereço de pacote recebidas.

Para datagramas recebidos pela função [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) sobre IPv4, o membro **Control** da estrutura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) recebida conterá uma estrutura [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) que contém uma estrutura **WSACMSGHDR.** O membro de nível **cmsg \_** dessa estrutura **WSACMSGHDR** conteria **\_ IP IPPROTO,** o membro do tipo **cmsg \_** dessa estrutura conteria **IP \_ PKTINFO** e o membro de dados **cmsg \_** conteria um na estrutura [**\_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) usada para armazenar informações de endereço de pacote IPv4 recebidas. O endereço IPv4 na estrutura **\_ em pktinfo** é o endereço IPv4 do qual o pacote foi recebido.

Para um soquete de datagrama de pilha dupla, se um aplicativo exigir a função [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) para retornar informações de pacote em uma estrutura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) para datagramas recebidos por IPv4, a opção de soquete IP PKTINFO deverá ser definida como true no \_ soquete. Se apenas a [opção \_ PKTINFO IPV6](ipv6-pktinfo.md) estiver definida como true no soquete, as informações de pacote serão fornecidas para datagramas recebidos por IPv6, mas não poderão ser fornecidas para datagramas recebidos por IPv4.

Se um aplicativo tentar definir a opção de soquete IP PKTINFO em um soquete de datagrama de pilha dupla e IPv4 estiver desabilitado no sistema, a função \_ [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) falhará e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará com um erro [de WSAEINVAL](windows-sockets-error-codes-2.md). Esse mesmo erro também é retornado pela **função setsockopt** como resultado de outros erros. Se um aplicativo tentar definir uma opção de soquete de nível IP IPPROTO em um soquete de pilha dupla e falhar com \_ [WSAEINVAL,](windows-sockets-error-codes-2.md)o aplicativo deverá determinar se o IPv4 está desabilitado no computador local. Um método que pode ser usado para detectar se o IPv4 está habilitado ou desabilitado é chamar a função [**de**](/windows/desktop/api/Winsock2/nf-winsock2-socket) soquete com o parâmetro *af* definido como AF INET para tentar criar um soquete \_ IPv4. Se a **função de soquete** falhar **e WSAGetLastError** retornar um erro [de WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md), isso significa que IPv4 não está habilitado. Nesse caso, uma falha de função **setsockopt** ao tentar definir a opção de \_ soquete IP PKTINFO pode ser ignorada pelo aplicativo. Caso contrário, uma falha ao tentar definir a opção de \_ soquete IP PKTINFO deve ser tratada como um erro inesperado.

Observe que o *arquivo de título Ws2ipdef.h* é incluído automaticamente em *Ws2tcpip.h* e nunca deve ser usado diretamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                       |
| Cabeçalho<br/>                   | <dl> <dt>Ws2ipdef.h (inclua Ws2tcpip.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Soquetes de pilha dupla](dual-stack-sockets.md)
</dt> <dt>

[**Getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**em \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[**Opções de soquete \_ IP IPPROTO**](ipproto-ip-socket-options.md)
</dt> <dt>

[IPV6 \_ PKTINFO](ipv6-pktinfo.md)
</dt> <dt>

[**Setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**Soquete**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
