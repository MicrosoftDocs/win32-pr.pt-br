---
description: O código de controle recupera o valor de pendência de envio ideal para a conexão subjacente.
ms.assetid: 03fe964b-26f7-4af7-83bf-62cc877d01a8
title: SIO_IDEAL_SEND_BACKLOG_QUERY código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 440e42477a8939a62eeb84b800c0fd8feead5aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105816041"
---
# <a name="sio_ideal_send_backlog_query-control-code"></a>SIO_IDEAL_SEND_BACKLOG_QUERY código de controle

## <a name="description"></a>Descrição

O código de controle de **consulta da pendência de envio do sio \_ ideal \_ \_ \_** recupera o valor de registro posterior de envio (ISB) ideal para a conexão subjacente.

Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
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
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
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
Use **a \_ \_ consulta de \_ pendência \_ de envio sio ideal** para esta operação.

### <a name="lpvinbuffer"></a>lpvInBuffer

Um ponteiro para o buffer de entrada.
Este parâmetro não é usado para esta operação.

### <a name="cbinbuffer"></a>cbInBuffer

O tamanho, em bytes, do buffer de entrada.
Este parâmetro não é usado para esta operação.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Um ponteiro para o buffer de saída.
Esse parâmetro deve apontar para um tipo de dados **ULONG** se os parâmetros *lpOverlapped* e *lpCompletionRoutine* forem **nulos**.

### <a name="cboutbuffer"></a>cbOutBuffer

O tamanho, em bytes, do buffer de saída.
Esse parâmetro deve ter pelo menos o tamanho de um tipo de dados **ULONG** .

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
| **\_e/s de WSA \_ pendente** | Uma operação sobreposta foi iniciada com êxito e a conclusão será indicada em um momento posterior. |
| **operação de WSA \_ \_ anulada** | Uma operação sobreposta foi cancelada devido ao fechamento do soquete ou à execução do comando **sio \_ flush** IOCTL. |
| **WSAEFAULT** | O parâmetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço de usuário. |
| **WSAEINPROGRESS** | A função é invocada quando um retorno de chamada está em andamento. |
| **WSAEINTR** | Uma operação de bloqueio foi interrompida. |
| **WSAEINVAL** | O parâmetro *dwIoControlCode* não é um comando válido ou um parâmetro de entrada especificado não é aceitável ou o comando não é aplicável ao tipo de soquete especificado. Esse erro será retornado se o parâmetro *cbOutBuffer* for menor que o tamanho de um tipo de dados **ULONG** .
| **WSAENETDOWN** | Falha no subsistema de rede. |
| **WSAENOPROTOOPT** | Não há suporte para a opção de soquete no protocolo especificado. |
| **WSAENOTCONN** | O Soquete s não está conectado. |
| **WSAENOTSOCK** | O descritor *s* não é um soquete. |
| **WSAEOPNOTSUPP** | Não há suporte para o comando IOCTL especificado. Esse erro será retornado se a **\_ consulta de \_ \_ pendência \_ de envio sio ideal** não tiver suporte do provedor de transporte. Esse erro também é retornado quando uma tentativa de usar a **\_ consulta de \_ \_ pendência \_ de envio sio ideal** é feita em um soquete de datagrama. |

## <a name="remarks"></a>Comentários

O IOCTL de **\_ consulta de pendência de \_ envio \_ \_ sio ideal** tem suporte no Windows Server 2008, no Windows Vista com Service Pack 1 (SP1) e em versões posteriores do sistema operacional.

Ao enviar dados por uma conexão TCP usando o Windows Sockets, é importante manter uma quantidade suficiente de dados pendentes (enviados mas não confirmados ainda) no TCP para alcançar a taxa de transferência mais alta.
O valor ideal para a quantidade de dados pendentes para atingir a melhor taxa de transferência para a conexão TCP é chamado de tamanho ideal de envio de pendências (ISB).
O valor ISB é uma função do produto de atraso de largura de banda da conexão TCP e da janela de recebimento anunciada do receptor (e parcialmente a quantidade de congestionamento na rede).

O valor do ISB por conexão está disponível na implementação do protocolo TCP no Windows Server 2008, no Windows Vista com SP1 e em versões posteriores do sistema operacional.
O IOCTL de **\_ consulta de pendência de \_ envio \_ \_ sio ideal** pode ser usado por um aplicativo para receber uma notificação quando o valor do ISB é alterado dinamicamente para uma conexão.

No Windows Server 2008, no Windows Vista com SP1 e em versões posteriores do sistema operacional, a [**sio ideal de enviar lista de \_ \_ \_ pendências de envio \_**](sio-ideal-send-backlog-change.md) e sio ideais de envio de consulta da lista de **\_ \_ \_ pendências \_** têm suporte em soquetes orientados a fluxo que estão em um estado conectado.

Teoricamente, o intervalo para o valor do ISB para uma conexão TCP pode variar de 0 a um máximo de 16 megabytes.

O uso típico do [**sio \_ ideal de \_ Enviar \_ pendências \_ de envio**](sio-ideal-send-backlog-change.md) e de **sio ideais de \_ \_ \_ \_ consulta de pendências de envio** é baseado no método Send usado pelos aplicativos.
Dois casos comuns são discutidos.

Os aplicativos que executam um bloqueio ou solicitação de envio sem bloqueio por vez normalmente dependem do buffer de envio interno pelo Winsock para obter uma taxa de transferência razoável.
O limite do buffer de envio para uma determinada conexão é controlado pela opção de soquete **\_ SNDBUF** .
Para o método Send de bloqueio e sem bloqueio, o limite do buffer de envio determina a quantidade de dados mantida pendente no TCP.
Se o valor do ISB para a conexão for maior que o limite do buffer de envio, a taxa de transferência obtida na conexão não será ideal.
Para obter uma melhor taxa de transferência, os aplicativos podem definir o limite do buffer de envio com base no resultado da consulta do ISB conforme as notificações de alteração do ISB ocorrem na conexão.

Para aplicativos que usam o método de envio sobreposto com várias solicitações Send pendentes, a quantidade de dados mantidas pendentes no TCP é determinada pelo limite do buffer de envio no Winsock e pela quantidade total de dados contidos nas solicitações de envio sobrepostas pendentes.
Nesse caso, os aplicativos devem usar o valor ISB para determinar quantas solicitações de envio pendentes devem ser mantidas e qual deve ser o tamanho dos dados de cada solicitação de envio.
O ideal é que o aplicativo tente manter a equação a seguir satisfeita:

`ISB value == send buffer limit + (number of simultaneous overlapped send requests * data length per send request)`

Observe que usar os IOCTLs do ISB sobre Soquetes TCP na maneira acima pode levar a um aumento no uso de memória no Exchange para maior taxa de transferência em conexões com um produto de atraso de largura de banda alta.
A implementação TCP no Windows limitará os valores do ISB conforme necessário com base no uso geral da memória do sistema.

O IOCTL de **\_ consulta de pendência de \_ envio \_ \_ sio ideal** é permitido somente em um soquete de fluxo que está no estado conectado.
Caso contrário, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** falhará com **WSAENOTCONN**.

Qualquer IOCTL pode bloquear indefinidamente, dependendo da implementação do provedor de serviço.
Se o aplicativo não puder tolerar o bloqueio em uma chamada de função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** , a e/s sobreposta seria ACONSELHAda para os IOCTLs que são especialmente prováveis de bloquear.

A **\_ consulta de \_ \_ pendência de \_ envio sio ideal** não é provavelmente bloqueada, portanto, ela normalmente é chamada de forma síncrona com os parâmetros *lpOverlapped* e *lpCompletionRoutine* definidos como **NULL**.

O IOCTL de **consulta de pendência de \_ \_ envio \_ \_ sio ideal** pode falhar com a operação **WSAEINTR** ou **WSA \_ \_ anulada** nos seguintes casos:

A conexão TCP é desconectada normalmente na direção de envio.
Isso pode ocorrer como resultado de uma chamada para a função de desligamento com o parâmetro de como definido como **SD \_ Send**, uma chamada para a função **DisconnectEx** ou uma chamada para a função **TransmitFile** ou **TransmitPackets** com o parâmetro *dwFlags* definido como **TF \_ Disconnect** ou **TF \_ reutilization**.
A conexão TCP foi redefinida ou anulada.
A solicitação é cancelada pelo Gerenciador de e/s.

Duas funções de wrapper embutidas para esses IOCTLs são definidas no arquivo de cabeçalho *Ws2tcpip. h* .
É recomendável que essas funções embutidas sejam usadas em vez de usar a consulta de [**\_ pendência de envio sio ideal \_ \_ \_**](sio-ideal-send-backlog-change.md) e o **sio \_ ideal \_ Enviar \_ \_ consultas de pendências** para os IOCTLs diretamente.

A função de wrapper embutido para o [**sio \_ ideal \_ Enviar \_ registro da pendência de \_ alteração**](sio-ideal-send-backlog-change.md) do IOCTL é a função **idealsendbacklognotify** .

A função de wrapper embutida para a **consulta de pendência de \_ \_ envio sio \_ \_ ideal** é a função **idealsendbacklogquery** .

O buffer de envio dinâmico para TCP foi adicionado no Windows 7 e no Windows Server 2008 R2.
Por padrão, o buffer de envio dinâmico para TCP é habilitado, a menos que um aplicativo defina a opção de soquete **\_ SNDBUF** no soquete de fluxo.

Usar o netsh é o método recomendado para consultar ou definir o buffer de envio dinâmico para TCP.

O valor atual para o buffer de envio dinâmico para TCP pode ser recuperado usando o seguinte comando:

`netsh winsock show autotuning`

O buffer de envio dinâmico para TCP pode ser desabilitado usando o seguinte comando:

`netsh winsock set autotuning off`

O buffer de envio dinâmico para TCP pode ser habilitado usando o seguinte comando:

`netsh winsock set autotuning on`

Embora não seja recomendado, o buffer de envio dinâmico pode ser desabilitado em um aplicativo definindo o seguinte valor de registro como zero:

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\AFD\Parameters\DynamicSendBufferDisable`

Ao alterar o valor de buffer de envio dinâmico usando NetSh.exe ou alterar o valor do registro, o computador deve ser reiniciado para que a alteração entre em vigor.

Com o buffer de envio dinâmico no Windows 7 e no Windows Server 2008 R2, o uso da consulta de [**\_ pendência de envio sio ideal \_ \_ \_**](sio-ideal-send-backlog-change.md) e os IOCTLs de **\_ \_ \_ \_ consultas pendentes de envio da lista de pendências sio ideais** são necessários apenas em circunstâncias especiais.

## <a name="see-also"></a>Confira também

[**SIO_IDEAL_SEND_BACKLOG_CHANGE**](sio-ideal-send-backlog-change.md)

[**SSA**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
