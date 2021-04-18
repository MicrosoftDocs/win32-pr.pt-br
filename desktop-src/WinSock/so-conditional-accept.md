---
description: Foi projetado para permitir que um aplicativo decida se deseja ou não aceitar uma conexão de entrada em um soquete de escuta.
ms.assetid: 964683eb-5dfc-4441-abb7-315be8b89a19
title: Opção de soquete SO_CONDITIONAL_ACCEPT (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badfdd1f8aac49ae05fa6b77dadb2561ba5ea02f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814056"
---
# <a name="so_conditional_accept-socket-option"></a>\_Opção de \_ soquete de aceitação condicional

A opção de soquete de **\_ \_ aceitação condicional** foi projetada para permitir que um aplicativo decida se deseja ou não aceitar uma conexão de entrada em um soquete de escuta.

## <a name="socket-option-value"></a>Valor da opção de soquete

A constante que representa essa opção de soquete é 0x3002.

## <a name="syntax"></a>Sintaxe


```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_CONDITIONAL_ACCEPT, // optname
  (char *) optval,         // input buffer,
  (int) optlen,       // size of input buffer
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

A opção de soquete para a qual o valor deve ser definido. Use **a \_ \_ aceitação condicional** para esta operação.

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
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | O parâmetro de *nível* é desconhecido ou inválido. Esse erro também será retornado se o soquete já estava em um estado de escuta.<br/>                                                                                                                        |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | A opção é desconhecida ou não é suportada pela família de protocolos indicada.<br/>                                                                                                                                                                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | O descritor não é um soquete.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Comentários

A função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) chamada com a opção de soquete de **\_ \_ aceitação condicional** permite que um aplicativo decida se deseja ou não aceitar uma conexão de entrada em um soquete de escuta. A opção Accept condicional para um soquete é desabilitada (definida como **false**) por padrão.

Quando essa opção de soquete está habilitada, a pilha TCP não aceita conexões automaticamente. Ele aguarda que o aplicativo indique que ele aceita a conexão por meio do retorno de chamada de aceitação condicional registrado com a função [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) . Depois que uma solicitação de conexão é recebida, o Winsock invoca o retorno de chamada de aceitação condicional registrado pelo aplicativo. Somente quando o retorno de chamada de aceitação condicional retorna **CF \_ Accept** , o Winsock notificará o transporte para aceitar totalmente a conexão.

Quando a opção de soquete de **\_ \_ aceitação condicional** estiver definida como habilitado (definido como **true**), isso terá vários efeitos colaterais no soquete:

-   Isso desabilita as defesas de proteção contra ataques SYN internas da pilha TCP, já que o aplicativo agora está assumindo a propriedade de aceitar conexões.
-   Isso efetivamente desabilita a pendência de escuta, pois as conexões não são aceitas em nome de um soquete de escuta. Uma conexão nunca é totalmente aceita até que o aplicativo aceite totalmente usando o mecanismo de **\_ aceitação do CF** .
-   Isso também significa que o aplicativo deve cuidar sempre estar em um estado para lidar prontamente com os retornos de chamada Accept para aceitar a conexão. Se o aplicativo estiver ocupado fazendo outro processamento, o lado do cliente poderá atingir o tempo limite antes que o aplicativo realmente aceite a conexão. Isso leva a uma experiência de cliente ruim.

Em geral, o principal motivo pelo qual os aplicativos usam a aceitação condicional é inspecionar o endereço IP de origem ou a porta usada pelo cliente que está se conectando e, em seguida, decidir aceitar ou rejeitar a conexão. No entanto, os aplicativos provavelmente executarão melhor se \_ a \_ opção de aceitação condicional não estiver habilitada e o aplicativo permitir que a pilha TCP e a lista de pendências de escuta funcionem conforme o esperado. Em seguida, quando o aplicativo lida com a conexão aceita, se for de uma porta ou endereço de origem de IP impróprio, o aplicativo poderá simplesmente fechar o soquete. A desvantagem da segurança desse comportamento é que agora o cliente tem uma confirmação de que o aplicativo está escutando em um endereço IP e uma porta, uma vez que ele fechou de modo forçado a conexão aceita anteriormente. No entanto, as desvantagens de habilitar a **\_ \_ aceitação condicional** geralmente superam essa limitação.

A função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chamada com a opção de soquete de **\_ \_ aceitação condicional** permite que um aplicativo recupere o estado atual da opção de aceitação condicional, embora esse recurso não seja usado normalmente. Se um aplicativo precisar habilitar a aceitação condicional em um soquete, ele apenas chamará a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para habilitar a opção.

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

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)
</dt> </dl>

 

 




