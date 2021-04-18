---
description: Foi projetado para permitir que um aplicativo habilite pacotes Keep-Alive para uma conexão de soquete.
ms.assetid: d6da7761-7a09-4c91-9737-550590a773b3
title: Opção de soquete SO_KEEPALIVE (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d829f957e23c48a325444de7d992397fba26d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760615"
---
# <a name="so_keepalive-socket-option"></a>\_Opção de soquete KeepAlive

A opção de soquete **\_ KeepAlive** é projetada para permitir que um aplicativo habilite pacotes Keep-Alive para uma conexão de soquete.

Para consultar o status dessa opção de soquete, chame a função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) . Para definir essa opção, chame a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) com os parâmetros a seguir.

## <a name="socket-option-value"></a>Valor da opção de soquete

A constante que representa essa opção de soquete é 0x0008.

## <a name="syntax"></a>Sintaxe


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
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

O nível no qual a opção é definida. Use **o \_ soquete sol** para esta operação.

</dd> <dt>

*OptName* \[ no\]
</dt> <dd>

A opção de soquete para a qual o valor deve ser definido. Use **o \_ KeepAlive** para esta operação.

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

Se a operação for concluída com êxito, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) retornará zero.

Se a operação falhar, um valor de erro de soquete \_ será retornado e um código de erro específico poderá ser recuperado chamando [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).



| Código do erro                                                                                                                                              | Significado                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Uma chamada [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) bem-sucedida deve ocorrer antes de usar essa função.<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Falha no subsistema de rede.<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Um dos parâmetros *optval* ou *optlen* aponta para a memória que não está em uma parte válida do espaço de endereço de usuário. Esse erro também será retornado se o valor apontado pelo parâmetro *optlen* for menor que o tamanho de um valor **DWORD** .<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | Uma chamada de bloqueio do Windows Sockets 1,1 está em andamento ou o provedor de serviços ainda está processando uma função de retorno de chamada.<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | O parâmetro de *nível* é desconhecido ou inválido. No Windows Vista e posterior, esse erro também será retornado se o soquete estava em um estado de transição.<br/>                                                                                                 |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | A opção é desconhecida ou não é suportada pela família de protocolos indicada. Esse erro será retornado se o descritor de soquete passado no parâmetro *s* for para um soquete de datagrama.<br/>                                                                   |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | O descritor não é um soquete.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Comentários

A função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chamada com a opção de soquete **\_ Keep Alive** permite que um aplicativo recupere o estado atual da opção KeepAlive, embora esse recurso não seja usado normalmente. Se um aplicativo precisar habilitar pacotes KeepAlive em um soquete, ele apenas chamará a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para habilitar a opção.

A função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) chamada com a opção de soquete **\_ Keep Alive** permite que um aplicativo habilite pacotes Keep-Alive para uma conexão de soquete. A opção de **\_ KeepAlive** para um soquete é desabilitada (definida como **false**) por padrão.

Quando essa opção de soquete estiver habilitada, a pilha TCP enviará pacotes Keep-Alive quando nenhum pacote de dados ou de confirmação tiver sido recebido para a conexão em um intervalo. Para obter mais informações sobre a opção keep-alive, consulte a seção 4.2.3.6 sobre os *requisitos para hosts da Internet — camadas de comunicação* especificadas no RFC 1122 disponíveis no [site da IETF](https://www.ietf.org/rfc/rfc1122.txt). (Este recurso só pode estar disponível em inglês.)

A opção de soquete **\_ KeepAlive** é válida somente para protocolos que dão suporte à noção de Keep-Alive (protocolos orientados a conexões). Para TCP, o tempo limite de Keep-Alive padrão é 2 horas e o intervalo de Keep-Alive é de 1 segundo. O número padrão de investigações Keep-Alive varia de acordo com a versão do Windows.

O código de controle do [**sio \_ KeepAlive \_ Vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) pode ser usado para habilitar ou desabilitar Keep-Alive e ajustar o tempo limite e o intervalo para uma única conexão. Se Keep-Alive estiver habilitado com **o \_ KeepAlive**, as configurações de TCP padrão serão usadas para tempo limite de Keep-Alive e intervalo, a menos que esses valores tenham sido alterados usando **sio \_ KeepAlive \_ Vals**.

O valor padrão em todo o sistema do tempo limite de Keep-Alive é controlável por meio da configuração do registro [KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) que usa um valor em milissegundos. O valor padrão em todo o sistema do intervalo Keep-Alive é controlável por meio da configuração do registro [KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) , que usa um valor em milissegundos.

No Windows Vista e posterior, o número de investigações de Keep-Alive (retransmissões de dados) é definido como 10 e não pode ser alterado.

No Windows Server 2003, Windows XP e Windows 2000, a configuração padrão para o número de investigações Keep-Alive é 5. O número de investigações Keep Alive é controlável por meio das configurações de registro [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) e [PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) . O número de investigações Keep Alive é definido como o maior dos dois valores de chave do registro. Se esse número for 0, as investigações Keep-Alive não serão enviadas. Se esse número estiver acima de 255, ele será ajustado para 255.

No Windows Vista e posterior, a opção de soquete de **\_ KeepAlive** só pode ser definida usando a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) quando o soquete está em um estado bem conhecido, não em um estado de transição. Para TCP, a opção de soquete **\_ KeepAlive** deve ser definida antes da função Connect ([**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)ou [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)) ser chamada, ou após a solicitação de conexão ser realmente concluída. Se a função Connect tiver sido chamada de forma assíncrona, isso exigirá aguardar a conclusão da conexão antes de tentar definir a opção de soquete **\_ KeepAlive** . Se um aplicativo tentar definir a opção de soquete de **\_ KeepAlive** quando uma solicitação de conexão ainda estiver em andamento, a função **setsockopt** falhará e retornará [WSAEINVAL](windows-sockets-error-codes-2.md).

No Windows Server 2003, Windows XP e Windows 2000, a opção de soquete **\_ KeepAlive** pode ser definida usando a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) quando o soquete é um estado de transição (uma solicitação de conexão ainda está em andamento), bem como um estado bem conhecido.

Observe que o arquivo de cabeçalho *Ws2def. h* é incluído automaticamente no *Winsock2. h* e nunca deve ser usado diretamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Ws2def. h (incluir Winsock2. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[KeepAlivetime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))
</dt> <dt>

[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))
</dt> <dt>

[PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))
</dt> <dt>

[**SSA**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**SIO \_ KeepAlive \_ Vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))
</dt> <dt>

[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))
</dt> <dt>

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
