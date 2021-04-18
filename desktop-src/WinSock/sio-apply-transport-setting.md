---
description: O código de controle aplica uma ou mais configurações de transporte a um soquete.
ms.assetid: FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715
title: SIO_APPLY_TRANSPORT_SETTING código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: e167a87e70dc3c6c44a263308beb333176a3d525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105816040"
---
# <a name="sio_apply_transport_setting-control-code"></a>SIO_APPLY_TRANSPORT_SETTING código de controle

## <a name="description"></a>Descrição

O código de controle de **\_ configuração de \_ transporte \_ sio Apply** aplica uma ou mais configurações de transporte a um soquete.

Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
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
Use **a \_ \_ \_ configuração aplicar transporte do sio** para esta operação.

### <a name="lpvinbuffer"></a>lpvInBuffer

Um ponteiro para o buffer de entrada.
Esse parâmetro contém um ponteiro para uma estrutura em que o primeiro membro da estrutura é uma estrutura [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) que determina qual configuração de transporte está sendo aplicada.

### <a name="cbinbuffer"></a>cbInBuffer

O tamanho, em bytes, do buffer de entrada.
Esse parâmetro depende da configuração de transporte que está sendo aplicada.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Um ponteiro para o buffer de saída.
Esse parâmetro depende da configuração de transporte que está sendo aplicada.

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
|**\_e/s de WSA \_ pendente** | A operação de e/s sobreposta está em andamento. Esse valor será retornado se uma operação sobreposta tiver sido iniciada com êxito e a conclusão será indicada mais tarde. |
| **operação de WSA \_ \_ anulada** | A operação de e/s foi anulada devido a uma saída de thread ou uma solicitação de aplicativo. Esse erro será retornado se uma operação sobreposta tiver sido cancelada devido ao fechamento do soquete ou à execução do comando **sio \_ flush** IOCTL. |
| **WSAEFAULT** | O sistema detectou um endereço de ponteiro inválido ao tentar usar um argumento de ponteiro em uma chamada. Esse erro é retornado do parâmetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço de usuário. |
| **WSAEINPROGRESS** | Uma operação de bloqueio está atualmente em execução. Esse erro será retornado se a função for invocada quando um retorno de chamada estiver em andamento. |
| **WSAEINTR** | Uma operação de bloqueio foi interrompida por uma chamada para [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall). Esse erro será retornado se uma operação de bloqueio tiver sido interrompida. |
| **WSAEINVAL** | Foi fornecido um argumento inválido. Esse erro será retornado se o parâmetro *dwIoControlCode* não for um comando válido ou se um parâmetro de entrada especificado não for aceitável ou se o comando não for aplicável ao tipo de soquete especificado. |
| **WSAENETDOWN** | Uma operação de soquete encontrou uma rede inoperante. Esse erro será retornado se o subsistema de rede tiver falhado. |
| **WSAENOTSOCK** | Uma operação foi tentada em algo que não é um soquete. Esse erro será retornado se o descritor *s* não for um soquete. |
| **WSAEOPNOTSUPP** | Não há suporte para a operação tentada para o tipo de objeto referenciado. Esse erro será retornado se o comando IOCTL especificado não tiver suporte. Esse erro também será retornado se a **\_ configuração de \_ transporte \_ sio aplicar** o IOCTL não tiver suporte do provedor de transporte. Esse erro também é retornado quando uma tentativa de usar a **\_ configuração de \_ transporte \_ sio Apply** do IOCTL é feita em um soquete diferente de UDP ou TCP. |

## <a name="remarks"></a>Comentários

O IOCTL de **\_ configuração de \_ transporte \_ sio Apply** tem suporte no Windows 8, no Windows Server 2012 e em versões posteriores do sistema operacional.

A **\_ configuração de \_ transporte \_ sio de aplicação** do IOCTL é um IOCTL genérico usado para aplicar a configuração de transporte ao soquete.
A configuração de transporte sendo aplicada é baseada no [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passado no parâmetro *lpvInBuffer* .

A partir do Windows 8 e do Windows Server 2012, o sistema define o recurso de **REAL_TIME_NOTIFICATION_CAPABILITY** em um soquete TCP.
A partir do Windows 10 e do Windows Server 2016, o **\_ \_ contexto NAMERES associado** também é definido.
Para obter mais informações, consulte [**addrinfoex4**](/windows/desktop/api/ws2def/ns-ws2def-addrinfoex4) e [**ASSOCIATE_NAMERES_CONTEXT_INPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-associate_nameres_context_input).

Se o [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passado no parâmetro lpvInBuffer tiver o membro GUID definido como **recurso de \_ \_ notificação em \_ tempo real**, essa será uma solicitação para aplicar configurações de notificação em tempo real para o soquete TCP usado com o [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) para receber notificações de rede em segundo plano em um aplicativo da Windows Store.
O parâmetro *lpvInBuffer* deve apontar para uma estrutura de **REAL_TIME_NOTIFICATION_SETTING_INPUT** .
O parâmetro *lpvOutBuffer* não é usado para esta operação.
Essa configuração de transporte aplica-se somente a soquetes TCP.
Essa configuração de transporte fornece uma maneira para que o WinInet ou serviços de rede semelhantes marquem um determinado soquete TCP como [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) habilitado.
O Windows marcará o soquete TCP correspondente e definirá as configurações de hardware e software apropriadas quando essa opção for chamada.
Um aplicativo da Windows Store não chamará esse IOCTL diretamente.

## <a name="see-also"></a>Confira também

[**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[SSA](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SIO_QUERY_TRANSPORT_SETTING**](sio-query-transport-setting.md)

[**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
