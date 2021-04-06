---
description: Retorna o endereço local, a porta local, o endereço remoto, a porta remota, o tipo de soquete e o protocolo usados por um soquete.
ms.assetid: 2628f47e-3e73-4e02-91b8-ba4cb0800864
title: Opção de soquete SO_BSP_STATE (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10e391d70dd67190e1aec803036d019261c9000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661771"
---
# <a name="so_bsp_state-socket-option"></a>\_Opção de \_ soquete de estado BSP

A opção de soquete de **\_ \_ estado BSP de so** retorna o endereço local, a porta local, o endereço remoto, a porta remota, o tipo de soquete e o protocolo usado por um soquete.

Para executar essa operação, chame a função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) com os parâmetros a seguir.

## <a name="socket-option-value"></a>Valor da opção de soquete

A constante que representa essa opção de soquete é 0x1009.

## <a name="syntax"></a>Sintaxe


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_BSP_STATE, // optname
  (char *) optval,         // output buffer,
  (int) *optlen,       // size of output buffer
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

O nível no qual a opção é definida. Use **o \_ soquete sol** para esta operação.

</dd> <dt>

*OptName* \[ no\]
</dt> <dd>

A opção de soquete para a qual o valor deve ser recuperado. Use **o \_ \_ estado BSP** para esta operação.

</dd> <dt>

*optval* \[ fora\]
</dt> <dd>

Um ponteiro para o buffer no qual o valor da opção solicitada deve ser retornado. Esse parâmetro deve apontar para o buffer igual ou maior que o tamanho de uma estrutura de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .

</dd> <dt>

*optlen* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para o tamanho, em bytes, do buffer *optval* . Esse tamanho deve ser igual ou maior que o tamanho de uma estrutura [**de \_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com êxito, [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) retornará zero.

Se a operação falhar, um valor de erro de soquete \_ será retornado e um código de erro específico poderá ser recuperado chamando [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).



| Código do erro                                                                                                                                              | Significado                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Uma chamada [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) bem-sucedida deve ocorrer antes de usar essa função.<br/>                                                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Falha no subsistema de rede.<br/>                                                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Um dos parâmetros *optval* ou *optlen* aponta para a memória que não está em uma parte válida do espaço de endereço de usuário. Esse erro também será retornado se o valor apontado pelo parâmetro *optlen* for menor que o tamanho de uma estrutura [**de \_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | Uma chamada de bloqueio do Windows Sockets 1,1 está em andamento ou o provedor de serviços ainda está processando uma função de retorno de chamada.<br/>                                                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | O parâmetro de *nível* é desconhecido ou inválido.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | A opção é desconhecida ou não é suportada pela família de protocolos indicada.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | O descritor não é um soquete.<br/>                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Comentários

A função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chamada com a opção de soquete de **\_ \_ estado BSP de so** recupera o endereço local, a porta local, o endereço remoto, a porta remota, o tipo de soquete e o protocolo usados por um soquete. A opção de soquete de **\_ \_ estado BSP de so** funciona com soquetes IPv6 ou IPv4 (as famílias de endereços da **\_ inet** **\_ INET6** e AF).

Se a função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) for bem-sucedida, as informações serão retornadas em uma estrutura de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) no buffer apontado pelo parâmetro *optval* . O inteiro apontado por *optlen* deve conter originalmente o tamanho desse buffer; no retorno, ele será definido como o comprimento, em bytes, do valor retornado no parâmetro *optval* .

Os membros **iSocketType** e **iProtocol** na estrutura de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) retornada são preenchidos para o descritor de soquete no parâmetro *s* .

Se o soquete estiver em um estado conectado ou ligado, o membro **localaddr** da estrutura de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) retornada será definido como uma estrutura [SOCKADDR](sockaddr-2.md) que representa o endereço e a porta locais. Se o soquete estiver em um estado conectado, o membro **RemoteAddr** da estrutura de **\_ informações de CSADDR** retornada será definido como uma estrutura sockaddr que representa o endereço e a porta remotos.

Se o soquete não estiver em um estado conectado ou ligado, o membro **localaddr** da estrutura de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) retornada será retornado com um ponteiro **nulo** no membro **lpSockAddr** e o membro **iSockaddrLength** definido como zero. Se o soquete não estiver em um estado ligado, o membro **RemoteAddr** da estrutura de **\_ informações de CSADDR** retornada será retornado com um ponteiro **nulo** no membro **lpSockAddr** e o membro **iSockaddrLength** definido como zero.

Se a função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) falhar, os *parâmetros optval* e *optlen* permanecerão inalterados e o parâmetro *optval* não apontará para uma estrutura de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) retornada.

Observe que o arquivo de cabeçalho *Ws2def. h* é incluído automaticamente no *Winsock2. h* e nunca deve ser usado diretamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Ws2def. h (incluir Winsock2. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**informações de CSADDR \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[SOCKADDR](sockaddr-2.md)
</dt> </dl>

 

 
