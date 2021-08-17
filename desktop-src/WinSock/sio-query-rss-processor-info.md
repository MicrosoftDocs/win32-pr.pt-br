---
description: O código de controle consulta a associação entre um soquete e um núcleo do processador RSS e um nó NUMA.
ms.assetid: DAF18C92-B479-474F-B438-0746CBA20653
title: SIO_QUERY_RSS_PROCESSOR_INFO de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 6c0f690555beb19f7d5d79a81e2cc900194f731c3acacb075ae12dc304debffd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740378"
---
# <a name="sio_query_rss_processor_info-control-code"></a>SIO_QUERY_RSS_PROCESSOR_INFO de controle

## <a name="description"></a>Descrição

O **código de controle SIO \_ QUERY \_ RSS \_ PROCESSOR \_ INFO** consulta a associação entre um soquete e um núcleo do processador RSS e o nó NUMA.

Para executar essa operação, chame a [**função WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) **ou WSPIoctl** com os parâmetros a seguir.

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

### <a name="dwiocontrolcode"></a>Dwiocontrolcode

O código de controle para a operação.
Use **INFORMAÇÕES DO PROCESSADOR \_ \_ RSS de CONSULTA SIO \_ \_** para esta operação.

### <a name="lpvinbuffer"></a>Lpvinbuffer

Um ponteiro para o buffer de entrada.
Esse parâmetro não éusado para esta operação.

### <a name="cbinbuffer"></a>Cbinbuffer

O tamanho, em bytes, do buffer de entrada.
Esse parâmetro não éusado para esta operação.

### <a name="lpvoutbuffer"></a>Lpvoutbuffer

Um ponteiro para o buffer de saída.
Esse parâmetro deve apontar para uma estrutura [**SOCKET \_ PROCESSOR \_ AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) se os parâmetros *lpOverlapped* e *lpCompletionRoutine* são **NULL.**

### <a name="cboutbuffer"></a>cbOutBuffer

O tamanho, em bytes, do buffer de saída.
Esse parâmetro deve ter pelo menos o tamanho de uma estrutura [**SOCKET \_ PROCESSOR \_ AFFINITY.**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)

### <a name="lpcbbytesreturned"></a>Lpcbbytesreturned

Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.

Se o buffer de saída for muito pequeno, a chamada falhará, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [**WSAEINVAL**](windows-sockets-error-codes-2.md)e o parâmetro *lpcbBytesReturned* aponta para um *valor DWORD* de zero.

Se *lpOverlapped* for **NULL,** o valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* retornado em uma chamada bem-sucedida não poderá ser zero.

Se o *parâmetro lpOverlapped* não for **NULL** para soquetes sobrepondo, as operações que não puderem ser concluídas imediatamente serão iniciadas e a conclusão será indicada posteriormente.
O **valor DWORD** apontado pelo parâmetro *lpcbBytesReturned* retornado pode ser zero, pois o tamanho dos dados armazenados não pode ser determinado até que a operação sobrecarregada seja concluída.
O status de conclusão final pode ser recuperado quando o método de conclusão apropriado é sinalizado quando a operação é concluída.

### <a name="lpvoverlapped"></a>lpvOverlapped

Um ponteiro para uma [**estrutura WSAOVERLAPPED.**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

Se o *soquete s* tiver sido criado sem o atributo sobrecodado, *o parâmetro lpOverlapped* será ignorado.

Se *s* foi aberto com o atributo sobre mapeado e o parâmetro *lpOverlapped* não é **NULL,** a operação é executada como uma operação sobressalo (assíncrona).
Nesse caso, *o parâmetro lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.

Para operações sobreporadas, a [**função WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente e o método de conclusão apropriado é sinalizado quando a operação é concluída.
Caso contrário, a função não retornará até que a operação seja concluída ou ocorra um erro.

### <a name="lpcompletionroutine"></a>Lpcompletionroutine

Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobre mapeados).

### <a name="lpthreadid"></a>lpThreadId

Um ponteiro para uma [**estrutura WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usada pelo provedor em uma chamada subsequente para [**WPUQueueApc.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)
O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até depois que a [**função WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) retornar.

**Observação**  Esse parâmetro se aplica somente à **função WSPIoctl.**

### <a name="lperrno"></a>Lperrno

Um ponteiro para o código de erro.

**Observação**  Esse parâmetro se aplica somente à **função WSPIoctl.**

## <a name="return-value"></a>Valor retornado

Se a operação for concluída com êxito, a [**função WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) **ou WSPIoctl** retornará zero.

Se a operação falhar ou estiver pendente, a [**função WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **SOCKET \_ ERROR**.
Para obter informações de erro estendidas, [**chame WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Código do erro | Significado |
|------------|---------|
| **ERRO \_ BUFFER \_ INSUFICIENTE** | A área de dados passada para uma chamada do sistema é muito pequena. Esse erro será retornado se o buffer apontado pelo parâmetro *lpvOutBuffer* com um tamanho de buffer passado no *parâmetro cbOutBuffer* for muito pequeno. O tamanho do buffer necessário será retornado no *parâmetro lpcbBytesReturned.* Esse erro será retornado se o *parâmetro cbOutBuffer* for menor que o tamanho de uma estrutura [**SOCKET PROCESSOR \_ \_ AFFINITY.**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) |
| **\_E/S WSA \_ PENDENTE** | Uma operação sobrecarada foi iniciada com êxito e a conclusão será indicada posteriormente. |
| **OPERAÇÃO WSA \_ \_ ANULADA** | Uma operação sobrecarada foi cancelada devido ao fechamento do soquete ou à execução do comando **IOCTL SIO \_ FLUSH.** |
| **WSAEFAULT** | O *parâmetro lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço do usuário. |
| **Wsaeinprogress** | A função é invocada quando um retorno de chamada está em andamento. |
| **Wsaeintr** | Uma operação de bloqueio foi interrompida. |
| **Wsaeinval** | O *parâmetro dwIoControlCode* não é um comando válido ou um parâmetro de entrada especificado não é aceitável ou o comando não é aplicável ao tipo de soquete especificado. Esse erro será retornado se o *parâmetro cbOutBuffer* for menor que o tamanho de uma estrutura [**SOCKET PROCESSOR \_ \_ AFFINITY.**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)
| **WSAENETDOWN** | O subsistema de rede falhou. |
| **Wsaenoprotoopt** | Não há suporte para a opção de soquete no protocolo especificado. |
| **WSAENOTCONN** | O *soquete s* não está conectado. |
| **Wsaenotsock** | O descritor *s não* é um soquete. |
| **Wsaeopnotsupp** | Não há suporte para o comando IOCTL especificado. Esse erro será retornado se o IOCTL de INFORMAÇÕES DO PROCESSADOR **\_ \_ RSS \_ \_** da CONSULTA SIO não tiver suporte do provedor de transporte. |

## <a name="remarks"></a>Comentários

O IOCTL de INFORMAÇÕES DO PROCESSADOR **\_ \_ RSS \_ \_** de CONSULTA SIO tem suporte Windows 8 e Windows Server 2012 e versões posteriores do sistema operacional.

O IOCTL de INFORMAÇÕES DO PROCESSADOR **\_ \_ RSS \_ \_** DA CONSULTA SIO é usado para determinar a associação entre um soquete e um núcleo do processador RSS e o nó NUMA.
Esse IOCTL retorna uma estrutura [**SOCKET \_ PROCESSOR \_ AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) que contém o [**NÚMERO DO PROCESSADOR \_**](/windows/desktop/api/winnt/ns-winnt-processor_number) e a ID do nó NUMA.
A estrutura [**PROCESSOR \_ NUMBER retornada**](/windows/desktop/api/winnt/ns-winnt-processor_number) contém um número de grupo e um número de processador relativo dentro do grupo.

Se o soquete for um soquete UDP, o soquete deverá ser conectado para que o IOCTL de INFORMAÇÕES DO PROCESSADOR **\_ \_ RSS \_ \_** da CONSULTA SIO funcione corretamente.

## <a name="see-also"></a>Confira também

[**PROCESSOR_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number)

[**Soquete**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SOCKET_PROCESSOR_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)

[**Wsagetlasterror**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**Wsagetoverlappedresult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**Wsaioctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**Wsaoverlapped**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
