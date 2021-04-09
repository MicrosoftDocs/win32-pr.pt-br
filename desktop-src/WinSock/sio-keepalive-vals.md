---
description: O código de controle habilita ou desabilita a configuração por conexão da opção TCP Keep-Alive que especifica o tempo limite e o intervalo de Keep-Alive TCP.
ms.assetid: c02e8ad5-bfad-489f-83bf-39b53fd68bde
title: SIO_KEEPALIVE_VALS código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ea8aabf452436ca2bbd6307366e7fc24f913dbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091306"
---
# <a name="sio_keepalive_vals-control-code"></a>SIO_KEEPALIVE_VALS código de controle

## <a name="description"></a>Description

O código de controle **sio \_ KeepAlive \_ Vals** habilita ou desabilita a configuração por conexão da opção TCP Keep-Alive que especifica o tempo limite e o intervalo de Keep-Alive TCP.

Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.

```cpp
int WSAIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
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
Use **sio \_ KeepAlive \_ Vals** para esta operação.

### <a name="lpvinbuffer"></a>lpvInBuffer

Um ponteiro para o buffer de entrada.
Esse parâmetro deve apontar para uma estrutura **TCP \_ KeepAlive** .

### <a name="cbinbuffer"></a>cbInBuffer

O tamanho, em bytes, do buffer de entrada.
Esse parâmetro deve ser igual ou maior que o tamanho da estrutura **TCP \_ KeepAlive** apontada pelo parâmetro *lpvInBuffer* .

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Um ponteiro para o buffer de saída.
Este parâmetro não é usado para esta operação.

### <a name="cboutbuffer"></a>cbOutBuffer

O tamanho, em bytes, do buffer de saída.
Esse parâmetro deve ser definido como zero.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.
Esse parâmetro retornado aponta para um valor **DWORD** de zero para esta operação, pois não há nenhuma saída.

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
|**\_e/s de WSA \_ pendente** | Uma operação sobreposta foi iniciada com êxito e a conclusão será indicada em um momento posterior. |
| **operação de WSA \_ \_ anulada** | Uma operação sobreposta foi cancelada devido ao fechamento do soquete ou à execução do comando **SIO_FLUSH IOCTL** . |
| **WSAEFAULT** | O parâmetro *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço do usuário. |
| **WSAEINPROGRESS** | A função é invocada quando um retorno de chamada está em andamento. |
| **WSAEINTR** | Uma operação de bloqueio foi interrompida. |
| **WSAEINVAL** | O parâmetro *dwIoControlCode* não é um comando válido ou um parâmetro de entrada especificado não é aceitável ou o comando não é aplicável ao tipo de soquete especificado. |
| **WSAENETDOWN** | Falha no subsistema de rede. |
| **WSAENOPROTOOPT** | Não há suporte para a opção de soquete no protocolo especificado. Esse erro é retornado para um soquete de datagrama. |
| **WSAENOTSOCK** | O descritor s não é um soquete. |
| **WSAEOPNOTSUPP** | Não há suporte para o comando IOCTL especificado. Esse erro será retornado se o **sio \_ KeepAlive \_ Vals** IOCTL não tiver suporte do provedor de transporte. |

## <a name="remarks"></a>Comentários

O **sio \_ KeepAlive \_ Vals** IOCTL tem suporte no Windows 2000 e versões posteriores do sistema operacional.

O código de controle do **sio \_ KeepAlive \_ Vals** habilita ou desabilita a configuração por conexão da opção TCP Keep-Alive que especifica o tempo limite e o intervalo de Keep-Alive TCP usados para pacotes Keep-Alive TCP.
Para obter mais informações sobre a opção keep-alive, consulte a seção 4.2.3.6 sobre os requisitos para hosts da Internet — camadas de comunicação especificadas no RFC 1122 disponíveis no [site da IETF](https://www.ietf.org/rfc/rfc1122.txt).
(Este recurso só pode estar disponível em inglês.)

O parâmetro *lpvInBuffer* deve apontar para uma estrutura **TCP \_ KeepAlive** definida no arquivo de cabeçalho *Mstcpip. h* .
Essa estrutura é definida da seguinte maneira:

```cpp
/* Argument structure for SIO_KEEPALIVE_VALS */
struct tcp_keepalive {
    u_long  onoff;
    u_long  keepalivetime;
    u_long  keepaliveinterval;
};
```

O valor especificado no membro **Onoff** determina se o TCP Keep-Alive está habilitado ou desabilitado.
Se o membro **Onoff** for definido como um valor diferente de zero, o TCP Keep-Alive será habilitado e os outros membros da estrutura serão usados.
O membro **KeepAliveTime** especifica o tempo limite, em milissegundos, sem atividade até que o primeiro pacote keep-alive seja enviado.
O membro **KeepAliveInterval** especifica o intervalo, em milissegundos, entre quando os pacotes Keep Alive sucessivos são enviados, caso nenhuma confirmação seja recebida.

A opção [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) , que é uma das [**opções de Soquete SOL_SOCKET**](/windows/desktop/winsock/sol-socket-socket-options), também pode ser usada para habilitar ou desabilitar o TCP Keep-Alive em uma conexão, bem como consultar o estado atual dessa opção.
Para consultar se o TCP Keep-Alive está habilitado em um soquete, a função getsockopt pode ser chamada com a opção [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) .
Para habilitar ou desabilitar o TCP Keep-Alive, a função **setsockopt** pode ser chamada com a opção [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) .
Se o TCP Keep-Alive estiver habilitado com [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive), as configurações de TCP padrão serão usadas para tempo limite de Keep-Alive e intervalo, a menos que esses valores tenham sido alterados usando **sio \_ KeepAlive \_ Vals**.

O valor padrão em todo o sistema do tempo limite de Keep-Alive é controlável por meio da configuração do registro [**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) que usa um valor em milissegundos. Se a chave não for definida, o tempo limite de Keep-Alive padrão será de 2 horas.
O valor padrão em todo o sistema do intervalo Keep-Alive é controlável por meio da configuração do registro [**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) , que usa um valor em milissegundos. Se a chave não for definida, o intervalo de Keep-Alive padrão será de 1 segundo.

No Windows Vista e posterior, o número de investigações de Keep-Alive (retransmissões de dados) é definido como 10 e não pode ser alterado.

No Windows Server 2003, Windows XP e Windows 2000, a configuração padrão para o número de investigações Keep-Alive é 5.
O número de investigações Keep Alive é controlável por meio das configurações de registro **TcpMaxDataRetransmissions** e [**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) .
O número de investigações Keep Alive é definido como o maior dos dois valores de chave do registro.
Se esse número for 0, as investigações Keep-Alive não serão enviadas.
Se esse número estiver acima de 255, ele será ajustado para 255.

## <a name="see-also"></a>Confira também

[**KeepAlivetime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))

[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))

[**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))

[SSA](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
