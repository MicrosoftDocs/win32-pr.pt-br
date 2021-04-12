---
description: O código de controle associa um soquete a uma reserva persistente ou de tempo de execução para um bloco de TCP ou UDP identificado pelo token de reserva de porta.
ms.assetid: 4CBFB5F8-1FA1-44BA-9932-6F0329A465CB
title: SIO_ASSOCIATE_PORT_RESERVATION código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 69af4f396fabd32f948d7e43cbf348aa34fb1a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170775"
---
# <a name="sio_associate_port_reservation-control-code"></a>SIO_ASSOCIATE_PORT_RESERVATION código de controle

## <a name="description"></a>Descrição

O código de controle de **\_ \_ \_ reserva de porta sio** associa um soquete com uma reserva persistente ou de tempo de execução para um bloco de TCP ou UDP identificado pelo token de reserva de porta.
Esse IOCTL deve ser emitido antes do soquete ser associado.
Se e quando o soquete estiver associado, a porta atribuída a ele será selecionada na reserva de porta identificada pelo token fornecido.
Se nenhuma porta estiver disponível na reserva especificada, a chamada de função de [**Associação**](/windows/desktop/api/winsock/nf-winsock-bind) falhará.

Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a>Parâmetros

### <a name="s"></a>s

Um descritor que identifica um soquete.

### <a name="dwiocontrolcode"></a>dwIoControlCode

O código de controle para a operação.
Use **a \_ \_ \_ reserva de porta associada do sio** para esta operação.

### <a name="lpvinbuffer"></a>lpvInBuffer

Um ponteiro para o buffer de entrada.
Esse parâmetro contém um ponteiro para uma estrutura de [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) com o token para a reserva de porta TCP ou UDP a ser associada ao soquete.

### <a name="cbinbuffer"></a>cbInBuffer

O tamanho, em bytes, do buffer de entrada.
Esse parâmetro deve ter pelo menos o tamanho da estrutura de [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) .

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Um ponteiro para o buffer de saída.
Este parâmetro não é usado para esta operação.

### <a name="cboutbuffer"></a>cbOutBuffer

O tamanho, em bytes, do buffer de saída.
Esse parâmetro deve ser definido como zero.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.

Se o buffer de saída for muito pequeno, a chamada falhará, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [**WSAEINVAL**](windows-sockets-error-codes-2.md)e o parâmetro *lpcbBytesReturned* apontará para um valor **DWORD** igual a zero.

Se *lpOverlapped* for **NULL**, o valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* retornado em uma chamada bem-sucedida não poderá ser zero.

Se o parâmetro *lpOverlapped* não for **nulo** para os soquetes sobrepostos, as operações que não puderem ser concluídas imediatamente serão iniciadas e a conclusão será indicada mais tarde.
O valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* que é retornado pode ser zero, já que o tamanho dos dados armazenados não pode ser determinado até que a operação sobreposta seja concluída.
O status final de conclusão pode ser recuperado quando o método de conclusão apropriado é sinalizado quando a operação é concluída.

### <a name="lpvoverlapped"></a>lpvOverlapped

Um ponteiro para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .

Se o soquete *s* foi criado sem o atributo sobreposto, o parâmetro *lpOverlapped* será ignorado.

Se *s* foi aberto com o atributo Overlapped e o parâmetro *LpOverlapped* não for **nulo**, a operação será executada como uma operação sobreposta (assíncrona).
Nesse caso, o parâmetro *lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.

Para operações sobrepostas, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente, e o método de conclusão apropriado é sinalizado quando a operação é concluída.
Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.

### <a name="lpcompletionroutine"></a>lpCompletionRoutine

Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobrepostos).

### <a name="lpthreadid"></a>lpThreadId

Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).
O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.

**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .

### <a name="lperrno"></a>lpErrno

Um ponteiro para o código de erro.

**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.

Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.
Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Código do erro | Significado |
|------------|---------|
|**\_e/s de WSA \_ pendente** | A operação de e/s sobreposta está em andamento. Esse valor será retornado se uma operação sobreposta tiver sido iniciada com êxito e a conclusão será indicada mais tarde. |
| **operação de WSA \_ \_ anulada** | A operação de e/s foi anulada devido a uma saída de thread ou uma solicitação de aplicativo. Esse erro será retornado se uma operação sobreposta tiver sido cancelada devido ao fechamento do soquete ou à execução do comando **sio \_ flush IOCTL** . |
| **WSAEACCES** | Foi feita uma tentativa de acessar um soquete de uma maneira proibida por suas permissões de acesso. Esse erro é retornado sob várias condições para reservas de porta persistentes que incluem o seguinte: o usuário não tem os privilégios administrativos necessários no computador local ou o aplicativo não está sendo executado em um shell avançado como o administrador interno ( `RunAs administrator` ). |
| **WSAEFAULT** | O sistema detectou um endereço de ponteiro inválido ao tentar usar um argumento de ponteiro em uma chamada. Esse erro é retornado do parâmetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço de usuário. |
| **WSAEINPROGRESS** | Uma operação de bloqueio está atualmente em execução. Esse erro será retornado se a função for invocada quando um retorno de chamada estiver em andamento. |
| **WSAEINTR** | Uma operação de bloqueio foi interrompida por uma chamada para [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall). Esse erro será retornado se uma operação de bloqueio tiver sido interrompida. |
| **WSAEINVAL** | Foi fornecido um argumento inválido. Esse erro será retornado se o parâmetro *dwIoControlCode* não for um comando válido ou se um parâmetro de entrada especificado não for aceitável ou se o comando não for aplicável ao tipo de soquete especificado. |
| **WSAENETDOWN** | Uma operação de soquete encontrou uma rede inoperante. Esse erro será retornado se o subsistema de rede tiver falhado. |
| **WSAENOTSOCK** | Uma operação foi tentada em algo que não é um soquete. Esse erro será retornado se o descritor *s* não for um soquete. |
| **WSAEOPNOTSUPP** | Não há suporte para a operação tentada para o tipo de objeto referenciado. Esse erro será retornado se o comando IOCTL especificado não tiver suporte. Esse erro também será retornado se o **sio \_ associar \_ a \_ reserva de porta** IOCTL não for suportado pelo provedor de transporte. Esse erro também é retornado quando uma tentativa de usar o **IOCTL \_ \_ \_ reserva de porta de associação sio** é feita em um soquete diferente de UDP ou TCP. |

## <a name="remarks"></a>Comentários

O **sio \_ associar \_ a \_ reserva de porta** IOCTL tem suporte no Windows Vista e em versões posteriores do sistema operacional.

Os aplicativos e serviços que precisam reservar portas se enquadram em duas categorias.
A primeira categoria inclui componentes que precisam de uma porta específica como parte de sua operação.
Esses componentes geralmente preferem especificar a porta necessária no momento da instalação (em um manifesto do aplicativo, por exemplo).
A segunda categoria inclui componentes que precisam de qualquer porta disponível ou bloco de portas em tempo de execução.
Essas duas categorias correspondem a solicitações específicas e de reserva de porta curinga.
As solicitações de reserva específicas podem ser persistentes ou tempo de execução, enquanto as solicitações de reserva de porta curinga só têm suporte em tempo de execução.

O IOCTL de reserva de porta de associação de sio é usado para associar uma reserva de porta TCP ou UDP a uma reserva persistente ou de tempo de execução. **\_ \_ \_**

A função [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) ou [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) fornece a capacidade de um aplicativo ou serviço reservar um bloco persistente de portas TCP ou UDP.
As reservas de porta persistentes são registradas em um repositório persistente para o módulo TCP ou UDP no Windows.
Observe que o token de uma determinada reserva de porta persistente pode ser alterado cada vez que o sistema é reiniciado.

Depois que uma reserva de porta TCP ou UDP persistente tiver sido obtida, um aplicativo poderá solicitar atribuições de porta da reserva de porta abrindo um soquete TCP ou UDP e, em seguida, chamando a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) especificando o IOCTL de **reserva de \_ porta de associação \_ \_ sio** e passando o token de reserva antes de emitir uma chamada para a função de [**Associação**](/windows/desktop/api/winsock/nf-winsock-bind) no soquete.

O [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL pode ser usado para solicitar uma reserva de tempo de execução para um bloco de portas TCP ou UDP.
Para reservas de porta de tempo de execução, o pool de portas requer que as reservas sejam consumidas do processo em cujo soquete a reserva foi concedida.
As reservas de porta de tempo de execução duram apenas desde o tempo de vida do soquete no qual o [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL foi chamado.
Por outro lado, as reservas de porta persistentes criadas usando a função [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) ou [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) podem ser consumidas por qualquer processo com a capacidade de obter reservas persistentes.

Depois que uma reserva de porta TCP ou UDP de tempo de execução for obtida, um aplicativo poderá solicitar atribuições de porta da reserva de porta abrindo um soquete TCP ou UDP e, em seguida, chamando a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) especificando o IOCTL de **reserva de \_ porta de associação \_ \_ sio** e passando o token de reserva antes de emitir uma chamada para a função de [**Associação**](/windows/desktop/api/winsock/nf-winsock-bind) no soquete.

Se os parâmetros *lpOverlapped* e *lpCompletionRoutine* forem nulos, o soquete nessa função será tratado como um soquete não sobreposto.
Para um soquete não sobreposto, os parâmetros *lpOverlapped* e *lpCompletionRoutine* são ignorados, exceto que a função pode bloquear se o soquete *s* estiver no modo de bloqueio.
Se o soquete *s* estiver no modo sem bloqueio, essa função ainda será bloqueada, pois esse IOCTL específico não oferece suporte ao modo sem bloqueio.

Para os soquetes sobrepostos, as operações que não podem ser concluídas imediatamente serão iniciadas e a conclusão será indicada mais tarde.

Qualquer IOCTL pode bloquear indefinidamente, dependendo da implementação do provedor de serviço.
Se o aplicativo não puder tolerar o bloqueio em uma chamada de função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** , a e/s sobreposta seria ACONSELHAda para os IOCTLs que são especialmente prováveis de bloquear.

O **sio \_ associar \_ a \_ reserva de porta** do IOCTL pode falhar com **WSAEINTR** ou **WSA_OPERATION_ABORTED** nos seguintes casos:

* A solicitação é cancelada pelo Gerenciador de e/s.
* O soquete está fechado.

O IOCTL de reserva de porta de associação de sio passado para a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** para uma reserva de porta persistente só pode ser usado em um aplicativo quando o usuário está conectado como um membro do grupo Administradores. **\_ \_ \_**
Se **sio \_ associar \_ \_ reserva de porta** IOCTL for usado em um aplicativo quando o usuário não for um membro do grupo Administradores, a chamada de função falhará e **WSAEACCES** será retornado.
O uso do IOCTL **de \_ \_ \_ reserva de porta de associação de sio** também pode falhar devido ao UAC (controle de conta de usuário) no Windows Vista e posterior.
Se um aplicativo que usa esse IOCTL com uma reserva de porta persistente for executado por um usuário conectado como um membro do grupo de administradores que não seja o administrador interno, essa chamada falhará, a menos que o aplicativo tenha sido marcado no arquivo de manifesto com um **requestedExecutionLevel** definido como *requireAdministrator*.
Se o aplicativo não tiver esse arquivo de manifesto, um usuário conectado como membro do grupo Administradores que não seja o administrador interno deverá, então, executar o aplicativo em um shell avançado como o administrador interno ( `RunAs administrator` ) para que essa função tenha sucesso.

## <a name="see-also"></a>Confira também

[**associa**](/windows/desktop/api/winsock/nf-winsock-bind)

[**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[**DeletePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[**DeletePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[**LookupPersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[**LookupPersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md)

[**SIO_RELEASE_PORT_RESERVATION**](sio-release-port-reservation.md)

[SSA](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
