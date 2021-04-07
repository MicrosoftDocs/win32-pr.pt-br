---
description: O código de controle consulta as configurações de transporte em um soquete.
ms.assetid: 3845BE07-A414-4118-96E8-8BEF1DEDB1D3
title: SIO_QUERY_TRANSPORT_SETTING código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 592301f0fcdbbb0d3d5babba446583d2e48db086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827732"
---
# <a name="sio_query_transport_setting-control-code"></a>SIO_QUERY_TRANSPORT_SETTING código de controle

## <a name="description"></a>Descrição

O código de controle de **\_ configuração de \_ transporte \_ de consulta sio** consultas as configurações de transporte em um soquete.

Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
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
Use **a \_ \_ \_ configuração de transporte de consulta sio** para esta operação.

### <a name="lpvinbuffer"></a>lpvInBuffer

Um ponteiro para o buffer de entrada.
Esse parâmetro contém um ponteiro para uma estrutura em que o primeiro membro da estrutura é uma estrutura [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) que determina qual configuração de transporte está sendo consultada.

### <a name="cbinbuffer"></a>cbInBuffer

O tamanho, em bytes, do buffer de entrada.
Esse parâmetro depende da configuração de transporte que está sendo consultada.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Um ponteiro para o buffer de saída.
Esse parâmetro depende da configuração de transporte que está sendo consultada se os parâmetros *lpOverlapped* e *lpCompletionRoutine* forem **nulos**.

### <a name="cboutbuffer"></a>cbOutBuffer

O tamanho, em bytes, do buffer de saída.

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
| **ERRO \_ de \_ buffer insuficiente** | A área de dados passada para uma chamada do sistema é muito pequena. Esse erro será retornado se o buffer apontado pelo parâmetro *lpvOutBuffer* com um tamanho de buffer passado no parâmetro *cbOutBuffer* for muito pequeno. O tamanho do buffer necessário será retornado no parâmetro *lpcbBytesReturned* . |
| **\_e/s de WSA \_ pendente** | Uma operação sobreposta foi iniciada com êxito e a conclusão será indicada em um momento posterior. |
| **operação de WSA \_ \_ anulada** | Uma operação sobreposta foi cancelada devido ao fechamento do soquete ou à execução do comando **sio \_ flush** IOCTL. |
| **WSAEFAULT** | O parâmetro *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço de usuário. |
| **WSAEINPROGRESS** | A função é invocada quando um retorno de chamada está em andamento. |
| **WSAEINTR** | Uma operação de bloqueio foi interrompida. |
| **WSAEINVAL** | O parâmetro *dwIoControlCode* não é um comando válido ou um parâmetro de entrada especificado não é aceitável ou o comando não é aplicável ao tipo de soquete especificado. |
| **WSAENETDOWN** | Falha no subsistema de rede. |
| **WSAENOPROTOOPT** | Não há suporte para a opção de soquete no protocolo especificado. |
| **WSAENOTCONN** | O Soquete s não está conectado. |
| **WSAENOTSOCK** | O descritor s não é um soquete. |
| **WSAEOPNOTSUPP** | Não há suporte para o comando IOCTL especificado. Esse erro será retornado se a **\_ configuração de \_ transporte \_ de consulta sio** do IOCTL não for suportada pelo provedor de transporte. |

## <a name="remarks"></a>Comentários

A **\_ configuração de \_ transporte \_ de consulta sio** do IOCTL tem suporte no Windows 8, no Windows Server 2012 e em versões posteriores do sistema operacional.

A **\_ configuração de \_ transporte \_ de consulta sio** do IOCTL é um IOCTL genérico usado para consultar as configurações de transporte em um soquete.
A configuração de transporte sendo consultada se baseia no [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passado no parâmetro *lpvInBuffer* .

A única configuração de transporte definida atualmente é para o recurso de **\_ capacidade de \_ notificação \_ em tempo real** em um soquete TCP.

Se o [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passado no parâmetro *lpvInBuffer* tiver o membro GUID definido como **recurso de \_ \_ notificação em \_ tempo real**, essa será uma solicitação para consultar as configurações de notificação em tempo real para o soquete TCP usado com o [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) para receber notificações de rede em segundo plano em um aplicativo da Windows Store.
O parâmetro *lpvInBuffer* deve apontar para uma estrutura de [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) .
O parâmetro *lpvOutBuffer* deve apontar para uma estrutura de saída de **configuração de \_ \_ notificação em \_ \_ tempo real** .
Essa configuração de transporte aplica-se somente a soquetes TCP.
Essa configuração de transporte fornece uma maneira para que o WinInet ou serviços de rede semelhantes consultem um determinado soquete TCP para determinar o status do [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) .
Um aplicativo da Windows Store não chamará esse IOCTL diretamente.
Se a chamada [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** for bem-sucedida, esse IOCTL retornará uma estrutura de saída de **configuração de \_ \_ notificação em \_ \_ tempo real** com o status atual.

A **\_ configuração de \_ transporte \_ de consulta sio** do IOCTL fornece uma maneira para que o WinInet ou serviços de rede semelhantes consultem o status de configuração de transporte de um determinado soquete TCP para determinar se o [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) está habilitado no soquete.
Um aplicativo da Windows Store não chamará esse IOCTL diretamente.

Este IOCTL aplica-se somente a soquetes TCP.

## <a name="see-also"></a>Confira também

[**CONTROL_CHANNEL_TRIGGER_STATUS**](/windows/desktop/api/mstcpip/ne-mstcpip-control_channel_trigger_status)

[**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[**REAL_TIME_NOTIFICATION_SETTING_OUTPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-real_time_notification_setting_output)

[**SIO_APPLY_TRANSPORT_SETTING**](sio-apply-transport-setting.md)

[SSA](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
