---
description: Permite que um aplicativo habilite ou desabilite o retorno de informações de pacote pela função WSARecvMsg em um soquete IPv6.
ms.assetid: 7BF17538-BE92-44FE-BA3C-6B44F61D478A
title: Opção de soquete IPV6_PKTINFO (Ws2ipdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afd5b19cbaba7f6a66f5ba6fbd85d74eb2f2e3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813445"
---
# <a name="ipv6_pktinfo-socket-option"></a>\_Opção de soquete de PKTINFO IPv6

A \_ opção de soquete de PKTINFO IPv6 permite que um aplicativo habilite ou desabilite o retorno de informações de pacote pela função de [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) em um soquete IPv6.

Para consultar o status dessa opção de soquete, chame a função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) . Para definir essa opção, chame a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) com os parâmetros a seguir.

## <a name="socket-option-value"></a>Valor da opção de soquete

A constante que representa essa opção de soquete é 19.

## <a name="syntax"></a>Sintaxe


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
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

O nível no qual a opção é definida. Use **o \_ IPv6 IPPROTO** para esta operação.

</dd> <dt>

*OptName* \[ no\]
</dt> <dd>

A opção de soquete para obter ou definir o valor. Use \_ o PKTINFO IPv6 para esta operação.

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

A função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chamada com a \_ opção de soquete PKTINFO do IPv6 permite que um aplicativo determine se as informações do pacote serão retornadas pela função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)para um soquete IPv6.

A função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) chamada com a \_ opção de soquete PKTINFO do IPv6 permite que um aplicativo habilite ou desabilite o retorno das informações de pacote pela função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) . A \_ opção de PKTINFO IPv6 para um soquete é desabilitada (definida como **false**) por padrão.

Quando essa opção de soquete é habilitada em um soquete IPv6 do tipo **Sock \_ DGRAM** ou **Sock \_ RAW**, a função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retorna informações de pacote na estrutura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) apontada pelo parâmetro *lpMsg* . Um dos objetos de dados de controle na estrutura **WSAMSG** retornada conterá uma estrutura [**In6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) usada para armazenar informações de endereço de pacote recebido.

Para datagrams recebidos pela função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) sobre IPv6, o membro **Control** da estrutura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) recebido conterá uma estrutura [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) que contém uma estrutura **WSACMSGHDR** . O membro de **\_ nível CMsg** dessa estrutura **WSACMSGHDR** conteria **IPPROTO \_ IPv6**, o membro de **\_ tipo CMsg** dessa estrutura conteria o **IPv6 \_ PKTINFO** e o membro de **\_ dados CMsg** conteria [**uma \_ estrutura In6 PKTINFO usada**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) para armazenar informações de endereço de pacote IPv6 recebidas. O endereço IPv6 na estrutura **In6 \_ pktinfo** é o endereço IPv6 do qual o pacote foi recebido.

Para um soquete de datagrama de pilha dupla, se um aplicativo exigir que a função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retorne informações de pacote em uma estrutura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) para datagramas recebidos por IPv4, a opção [IP \_ PKTINFO](ip-pktinfo.md) Socket deverá ser definida como true no soquete. Se apenas a \_ opção PKTINFO IPv6 for definida como true no soquete, as informações de pacote serão fornecidas para datagramas recebidos via IPv6, mas podem não ser fornecidas para datagramas recebidos via IPv4.

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

[**In6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[\_PKTINFO IP](ip-pktinfo.md)
</dt> <dt>

[**Opções de soquete do IPPROTO \_ IPv6**](ipproto-ipv6-socket-options.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**SSA**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
