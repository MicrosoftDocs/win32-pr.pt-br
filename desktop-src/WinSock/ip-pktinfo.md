---
description: Permite que um aplicativo habilite ou desabilite o retorno de informações de pacote pela função WSARecvMsg em um soquete IPv4.
ms.assetid: C6246899-0220-4F88-B43B-CED1B1FF7DC3
title: Opção de soquete IP_PKTINFO (Ws2ipdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2134b31ead9efeb032b4ed72fcaedcd4cc9f67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296347"
---
# <a name="ip_pktinfo-socket-option"></a>\_Opção de soquete IP PKTINFO

A \_ opção IP PKTINFO Socket permite que um aplicativo habilite ou desabilite o retorno das informações de pacote pela função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) em um soquete IPv4.

Para consultar o status dessa opção de soquete, chame a função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) . Para definir essa opção, chame a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) com os parâmetros a seguir.

## <a name="socket-option-value"></a>Valor da opção de soquete

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

*nível* \[ do no\]
</dt> <dd>

O nível no qual a opção é definida. Use **o \_ IP IPPROTO** para esta operação.

</dd> <dt>

*OptName* \[ no\]
</dt> <dd>

A opção de soquete para obter ou definir o valor. Use \_ PKTINFO IP para esta operação.

</dd> <dt>

*optval* \[ fora\]
</dt> <dd>

Um ponteiro para o buffer que contém o valor da opção a ser definida. Esse parâmetro deve apontar para o buffer igual ou maior que o tamanho de um valor **DWORD** .

Esse valor é tratado como um valor booliano com 0 usado para indicar **falso** (desabilitado) e um valor diferente de zero para indicar **verdadeiro** (habilitado).

</dd> <dt>

*optlen* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para o tamanho, em bytes, do buffer *optval* . Esse tamanho deve ser igual ou maior que o tamanho de um valor **DWORD** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com êxito, a função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) ou [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) retornará zero.

Se a operação falhar, um valor de erro de soquete \_ será retornado e um código de erro específico poderá ser recuperado chamando [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).



| Código do erro                                                                                                                                              | Significado                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Uma chamada [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) bem-sucedida deve ocorrer antes de usar essa função.<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Falha no subsistema de rede.<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Um dos parâmetros *optval* ou *optlen* aponta para a memória que não está em uma parte válida do espaço de endereço de usuário. Esse erro também será retornado se o valor apontado pelo parâmetro *optlen* for menor que o tamanho de um valor **DWORD** .<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | Uma chamada de bloqueio do Windows Sockets 1,1 está em andamento ou o provedor de serviços ainda está processando uma função de retorno de chamada.<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Foi fornecido um argumento inválido. Esse erro será retornado se o parâmetro de *nível* for desconhecido ou inválido. No Windows Vista e posterior, esse erro também será retornado se o soquete estava em um estado de transição.<br/>                                     |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | A opção é desconhecida ou não é suportada pela família de protocolos indicada. Esse erro será retornado se o parâmetro de *tipo* para o descritor de soquete passado no parâmetro *s* não tiver sido **Sock \_ DGRAM** ou **Sock \_ RAW**. <br/>                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | O descritor não é um soquete.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Comentários

A função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chamada com a opção de soquete de PKTINFO de IP \_ permite que um aplicativo determine se as informações de pacote serão retornadas pela função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)para um soquete IPv4.

A função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) chamada com a \_ opção de soquete de PKTINFO de IP permite que um aplicativo habilite ou desabilite o retorno de informações de pacote pela função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) . A \_ opção de PKTINFO de IP para um soquete é desabilitada (definida como **false**) por padrão.

Quando essa opção de soquete é habilitada em um soquete IPv4 do tipo **Sock \_ DGRAM** ou **Sock \_ RAW**, a função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retorna informações de pacote na estrutura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) apontada pelo parâmetro *lpMsg* . Um dos objetos de dados de controle na estrutura **WSAMSG** retornada conterá uma estrutura [**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) usada para armazenar informações de endereço de pacote recebido.

Para datagrams recebidos pela função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) sobre IPv4, o membro **Control** da estrutura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) recebido conterá uma estrutura [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) que contém uma estrutura **WSACMSGHDR** . O membro de **\_ nível CMsg** dessa estrutura **WSACMSGHDR** conteria **o \_ IP IPPROTO**, o membro de **\_ tipo CMsg** dessa estrutura conteria o **IP \_ PKTINFO** e o membro de **\_ dados CMsg** conteria uma estrutura [**in \_ PKTINFO**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) usada para armazenar informações de endereço de pacote IPv4 recebido. O endereço IPv4 na estrutura **\_ pktinfo** é o endereço IPv4 do qual o pacote foi recebido.

Para um soquete de datagrama de pilha dupla, se um aplicativo exigir que a função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retorne informações de pacote em uma estrutura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) para datagramas recebidos por IPv4, \_ a opção IP PKTINFO Socket deverá ser definida como true no soquete. Se apenas a [opção \_ PKTINFO IPv6](ipv6-pktinfo.md) for definida como true no soquete, as informações de pacote serão fornecidas para datagramas recebidos via IPv6, mas podem não ser fornecidas para datagramas recebidos via IPv4.

Se um aplicativo tentar definir a opção de \_ soquete de IP PKTINFO em um soquete de datastack de pilha dupla e o IPv4 estiver desabilitado no sistema, a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) falhará e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará com um erro de [WSAEINVAL](windows-sockets-error-codes-2.md). Esse mesmo erro também é retornado pela função **setsockopt** como resultado de outros erros. Se um aplicativo tentar definir uma opção de \_ soquete de nível de IP IPPROTO em um soquete de pilha dupla e falhar com [WSAEINVAL](windows-sockets-error-codes-2.md), o aplicativo deverá determinar se o IPv4 está desabilitado no computador local. Um método que pode ser usado para detectar se o IPv4 está habilitado ou desabilitado é chamar a função de [**soquete**](/windows/desktop/api/Winsock2/nf-winsock2-socket) com o parâmetro *AF* definido como série AF para \_ tentar criar um soquete IPv4. Se a função **Socket** falhar e **WSAGetLastError** retornar um erro de [WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md), isso significará que o IPv4 não está habilitado. Nesse caso, uma falha de função **setsockopt** ao tentar definir a opção de soquete de PKTINFO de IP \_ pode ser ignorada pelo aplicativo. Caso contrário, uma falha ao tentar definir a \_ opção de soquete IP PKTINFO deve ser tratada como um erro inesperado.

Observe que o arquivo de cabeçalho *Ws2ipdef. h* é incluído automaticamente em *Ws2tcpip. h* e nunca deve ser usado diretamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Ws2ipdef. h (incluir Ws2tcpip. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Soquetes de pilha dupla](dual-stack-sockets.md)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**em \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[**\_Opções de soquete de IP IPPROTO**](ipproto-ip-socket-options.md)
</dt> <dt>

[\_PKTINFO IPv6](ipv6-pktinfo.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**SSA**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
