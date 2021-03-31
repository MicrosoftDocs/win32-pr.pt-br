---
description: O código de controle consulta a associação entre um soquete e um núcleo de processador RSS e um nó NUMA.
ms.assetid: DAF18C92-B479-474F-B438-0746CBA20653
title: SIO_QUERY_RSS_PROCESSOR_INFO código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: a2d251fa4fee996adaec51599e7b1d140a296b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920902"
---
# <a name="sio_query_rss_processor_info-control-code"></a>SIO_QUERY_RSS_PROCESSOR_INFO código de controle

## <a name="description"></a>Descrição

O código de controle de **\_ \_ \_ \_ informações do processador RSS do sio Query** consulta a associação entre um soquete e um núcleo de processador RSS e um nó numa.

Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
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
Use **as \_ \_ informações do \_ processador \_ RSS da consulta sio** para esta operação.

### <a name="lpvinbuffer"></a>lpvInBuffer

Um ponteiro para o buffer de entrada.
Este parâmetro não é usado para esta operação.

### <a name="cbinbuffer"></a>cbInBuffer

O tamanho, em bytes, do buffer de entrada.
Este parâmetro não é usado para esta operação.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Um ponteiro para o buffer de saída.
Esse parâmetro deve apontar para uma estrutura de [**\_ \_ afinidade de processador de soquete**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) se os parâmetros *lpOverlapped* e *lpCompletionRoutine* forem **nulos**.

### <a name="cboutbuffer"></a>cbOutBuffer

O tamanho, em bytes, do buffer de saída.
Esse parâmetro deve ter pelo menos o tamanho de uma estrutura de [**\_ \_ afinidade de processador de soquete**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.

Se o buffer de saída for muito pequeno, a chamada falhará, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [**WSAEINVAL**](windows-sockets-error-codes-2.md)e o parâmetro *lpcbBytesReturned* apontará para um valor *DWORD* igual a zero.

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

Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).
O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.

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
| **ERRO \_ de \_ buffer insuficiente** | A área de dados passada para uma chamada do sistema é muito pequena. Esse erro será retornado se o buffer apontado pelo parâmetro *lpvOutBuffer* com um tamanho de buffer passado no parâmetro *cbOutBuffer* for muito pequeno. O tamanho do buffer necessário será retornado no parâmetro *lpcbBytesReturned* . Esse erro será retornado se o parâmetro *cbOutBuffer* for menor que o tamanho de uma estrutura de [**\_ \_ afinidade de processador de soquete**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) . |
| **\_e/s de WSA \_ pendente** | Uma operação sobreposta foi iniciada com êxito e a conclusão será indicada em um momento posterior. |
| **operação de WSA \_ \_ anulada** | Uma operação sobreposta foi cancelada devido ao fechamento do soquete ou à execução do comando **sio \_ flush** IOCTL. |
| **WSAEFAULT** | O parâmetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço de usuário. |
| **WSAEINPROGRESS** | A função é invocada quando um retorno de chamada está em andamento. |
| **WSAEINTR** | Uma operação de bloqueio foi interrompida. |
| **WSAEINVAL** | O parâmetro *dwIoControlCode* não é um comando válido ou um parâmetro de entrada especificado não é aceitável ou o comando não é aplicável ao tipo de soquete especificado. Esse erro será retornado se o parâmetro *cbOutBuffer* for menor que o tamanho de uma estrutura de [**\_ \_ afinidade de processador de soquete**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .
| **WSAENETDOWN** | Falha no subsistema de rede. |
| **WSAENOPROTOOPT** | Não há suporte para a opção de soquete no protocolo especificado. |
| **WSAENOTCONN** | O soquete *s* não está conectado. |
| **WSAENOTSOCK** | O descritor *s* não é um soquete. |
| **WSAEOPNOTSUPP** | Não há suporte para o comando IOCTL especificado. Esse erro será retornado se o provedor de transporte não oferecer suporte ao IOCTL de **\_ \_ \_ \_ informações do processador RSS de consulta sio** . |

## <a name="remarks"></a>Comentários

O **sio \_ de \_ \_ \_ informações do processador RSS da consulta** do Microsoft Azure tem suporte no windows 8, no Windows Server 2012 e em versões posteriores do sistema operacional.

O IOCTL de **\_ \_ \_ \_ informações do processador RSS de consulta sio** é usado para determinar a associação entre um soquete e um núcleo de processador RSS e um nó numa.
Esse IOCTL retorna uma estrutura de [**\_ \_ afinidade de processador de soquete**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) que contém o [**\_ número do processador**](/windows/desktop/api/winnt/ns-winnt-processor_number) e a ID do nó numa.
A estrutura [**de \_ número de processador**](/windows/desktop/api/winnt/ns-winnt-processor_number) retornada contém um número de grupo e um número de processador relativo no grupo.

Se o soquete for um soquete UDP, o soquete deverá estar conectado para que **as \_ \_ informações do \_ processador \_ RSS de consulta sio** do IOCTL funcionem corretamente.

## <a name="see-also"></a>Confira também

[**PROCESSOR_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number)

[**SSA**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SOCKET_PROCESSOR_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
