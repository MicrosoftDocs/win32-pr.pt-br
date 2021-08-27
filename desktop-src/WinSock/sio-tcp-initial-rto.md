---
description: Um código de controle que configura os parâmetros de RTO (tempo limite de retransmissão inicial) em um soquete.
ms.assetid: F5ABAE57-E0F0-4AEB-825C-B53AEE8210E7
title: SIO_TCP_INITIAL_RTO código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 63ebbfd0d8d56c03d62c7bba417d69e3ac1a576abfc8c72ac489117a7d8b74c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097476"
---
# <a name="sio_tcp_initial_rto-control-code"></a>SIO_TCP_INITIAL_RTO código de controle

## <a name="description"></a>Descrição

O código de controle de **SIO_TCP_INITIAL_RTO** configura os parâmetros de RTO (tempo limite de retransmissão inicial) em um soquete.

Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
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
Use **SIO_TCP_INITIAL_RTO** para esta operação.

### <a name="lpvinbuffer"></a>lpvInBuffer

Um ponteiro para o buffer de entrada.
Esse parâmetro contém um ponteiro para o [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) associado ao soquete.

### <a name="cbinbuffer"></a>cbInBuffer

O tamanho, em bytes, do buffer de entrada.

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

## <a name="return-value"></a>Valor retornado

Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.

Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.
Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Código do erro | Significado |
|------------|---------|
| **\_e/s de WSA \_ pendente** | A operação de e/s sobreposta está em andamento. Esse valor será retornado se uma operação sobreposta tiver sido iniciada com êxito e a conclusão será indicada mais tarde. |
| **operação de WSA \_ \_ anulada** | A operação de e/s foi anulada devido a uma saída de thread ou uma solicitação de aplicativo. Esse erro será retornado se uma operação sobreposta tiver sido cancelada devido ao fechamento do soquete ou à execução do comando **sio \_ flush** IOCTL. |
| **WSAEACCES** | Foi feita uma tentativa de acessar um soquete de uma maneira proibida por suas permissões de acesso. Esse erro é retornado sob várias condições que incluem o seguinte: o usuário não tem os privilégios administrativos necessários no computador local ou o aplicativo não está sendo executado em um shell avançado como administrador interno ( `RunAs administrator` ). |
| **WSAEFAULT** | O sistema detectou um endereço de ponteiro inválido ao tentar usar um argumento de ponteiro em uma chamada. Esse erro é retornado do parâmetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço de usuário. |
| **WSAEINPROGRESS** | Uma operação de bloqueio está atualmente em execução. Esse erro será retornado se a função for invocada quando um retorno de chamada estiver em andamento. |
| **WSAEINTR** | Uma operação de bloqueio foi interrompida por uma chamada para *WSACancelBlockingCall*. Esse erro será retornado se uma operação de bloqueio tiver sido interrompida. |
| **WSAEINVAL** | Foi fornecido um argumento inválido. Esse erro será retornado se o parâmetro *dwIoControlCode* não for um comando válido ou se um parâmetro de entrada especificado não for aceitável ou se o comando não for aplicável ao tipo de soquete especificado. |
| **WSAENETDOWN** | Uma operação de soquete encontrou uma rede inoperante. Esse erro será retornado se o subsistema de rede tiver falhado. |
| **WSAENOTSOCK** | Uma operação foi tentada em algo que não é um soquete. Esse erro será retornado se o descritor s não for um soquete. |
| **WSAEOPNOTSUPP** | Não há suporte para a operação tentada para o tipo de objeto referenciado. Esse erro será retornado se o comando IOCTL especificado não tiver suporte. Esse erro também será retornado se o **SIO_TCP_INITIAL_RTO** IOCTL não tiver suporte do provedor de transporte. |

## <a name="remarks"></a>Comentários

Um aplicativo pode usar o **SIO_TCP_INITIAL_RTO** IOCTL para controlar as características de retransmissão iniciais (SYN/SYN + ACK) de um soquete TCP, se necessário.
Um aplicativo, se estiver usando essa opção, deve fornecer valores adequados antes de iniciar uma tentativa de conexão TCP no soquete.

O [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) IOCTL permite que um aplicativo configure o RTO (tempo limite de retransmissão) inicial usado pelo soquete.

Um ponteiro para uma estrutura de [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) passada no parâmetro *lpvInBuffer* permite que um aplicativo configure o tempo de ida e volta (RTT) inicial usado para calcular o tempo limite de retransmissão.
O aplicativo também pode configurar o número de retransmissões que serão tentadas antes da tentativa de conexão falhar.

## <a name="see-also"></a>Confira também

[SSA](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
