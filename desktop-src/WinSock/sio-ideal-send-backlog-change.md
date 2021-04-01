---
description: O código de controle notifica um aplicativo quando o valor da pendência de envio ideal é alterado para a conexão.
ms.assetid: 337883a5-7ceb-40d3-b318-b86dd488b94a
title: SIO_IDEAL_SEND_BACKLOG_CHANGE código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 4eb07efecd39774c60d47cbcf7245c5831760e06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661774"
---
# <a name="sio_ideal_send_backlog_change-control-code"></a>SIO_IDEAL_SEND_BACKLOG_CHANGE código de controle

## <a name="description"></a>Descrição

O código de controle de **alteração da pendência de envio do sio \_ ideal \_ \_ \_** notifica um aplicativo quando o valor da pendência de envio ideal (ISB) é alterado para a conexão.

Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
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
Use **a \_ \_ alteração da \_ pendência \_ de envio sio ideal** para esta operação.

### <a name="lpvinbuffer"></a>lpvInBuffer

Um ponteiro para o buffer de entrada.
Este parâmetro não é usado para esta operação.

### <a name="cbinbuffer"></a>cbInBuffer

O tamanho, em bytes, do buffer de entrada. Este parâmetro não é usado para esta operação.

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
| **WSAEFAULT** | O parâmetro *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço do usuário. |
| **WSAEINPROGRESS** | A função é invocada quando um retorno de chamada está em andamento. |
| **WSAEINTR** | Uma operação de bloqueio foi interrompida. |
| **WSAEINVAL** | O parâmetro *dwIoControlCode* não é um comando válido ou um parâmetro de entrada especificado não é aceitável ou o comando não é aplicável ao tipo de soquete especificado. Esse erro será retornado se o parâmetro *cbOutBuffer* não for zero. |
| **WSAENETDOWN** | Falha no subsistema de rede. |
| **WSAENOPROTOOPT** | Não há suporte para a opção de soquete no protocolo especificado. |
| **WSAENOTCONN** | O soquete *s* não está conectado. |
| **WSAENOTSOCK** | O descritor *s* não é um soquete. |
| **WSAEOPNOTSUPP** | Não há suporte para o comando IOCTL especificado. Esse erro será retornado se o provedor de transporte não oferecer suporte ao **sio \_ ideal para \_ Enviar \_ pendências de \_ alteração** . Esse erro também é retornado quando uma tentativa de usar o **sio \_ ideal \_ de \_ \_ alteração de pendência de envio** do IOCTL é feita em um soquete de datagrama. |

## <a name="remarks"></a>Comentários

O **sio \_ ideal para \_ Enviar \_ pendências de \_ alteração do registro posterior** tem suporte no Windows Server 2008, no Windows Vista com Service Pack 1 (SP1) e em versões posteriores do sistema operacional.

Ao enviar dados por uma conexão TCP usando o Windows Sockets, é importante manter uma quantidade suficiente de dados pendentes (enviados mas não confirmados ainda) no TCP para alcançar a taxa de transferência mais alta.
O valor ideal para a quantidade de dados pendentes para atingir a melhor taxa de transferência para a conexão TCP é chamado de tamanho ideal de envio de pendências (ISB).
O valor ISB é uma função do produto de atraso de largura de banda da conexão TCP e da janela de recebimento anunciada do receptor (e parcialmente a quantidade de congestionamento na rede).

O valor do ISB por conexão está disponível na implementação do protocolo TCP no Windows Server 2008, no Windows Vista com SP1 e em versões posteriores do sistema operacional.
O IOCTL de **alteração da pendência de envio do sio \_ ideal \_ \_ \_** pode ser usado por um aplicativo para receber uma notificação quando o valor do ISB é alterado dinamicamente para uma conexão.

No Windows Server 2008, no Windows Vista com SP1 e em versões posteriores do sistema operacional, a **sio ideal de enviar lista de \_ \_ \_ pendências de envio \_** e sio ideais de envio de consulta da lista de [**\_ \_ \_ pendências \_**](sio-ideal-send-backlog-query.md) têm suporte em soquetes orientados a fluxo que estão em um estado conectado.

Teoricamente, o intervalo para o valor do ISB para uma conexão TCP pode variar de 0 a um máximo de 16 megabytes.

Consulte a página de referência do IOCTL [**sio \_ ideal \_ Enviar \_ \_ consulta de pendência**](sio-ideal-send-backlog-query.md) para uso típico do mecanismo do ISB para obter uma melhor taxa de transferência em conexões de produto com atraso de largura de banda alta.

O IOCTL de **\_ alteração da pendência de \_ envio \_ \_ sio ideal** só é permitido em um soquete de fluxo que esteja no estado conectado.
Caso contrário, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** falhará com **WSAENOTCONN**.

O IOCTL de **\_ alteração da pendência de \_ envio \_ \_ sio ideal** não usa buffers de entrada ou saída e pends ou blocos até que uma alteração do ISB ocorra na conexão subjacente.
Quando esse IOCTL é concluído, um aplicativo Winsock pode usar a [**\_ consulta de \_ \_ pendência \_ de envio sio ideal**](sio-ideal-send-backlog-query.md) para recuperar o novo valor do ISB na conexão.

O IOCTL de **\_ alteração da pendência de \_ envio \_ \_ sio ideal** não dá suporte ao modo sem bloqueio.
Um aplicativo pode emitir esse IOCTL em um soquete sem bloqueio, mas o IOCTL simplesmente bloqueará ou ficará pendente até que o valor do ISB seja alterado.

Se os parâmetros *lpOverlapped* e *lpCompletionRoutine* forem nulos, o soquete nessa função será tratado como um soquete não sobreposto.
Para um soquete não sobreposto, os parâmetros *lpOverlapped* e *lpCompletionRoutine* são ignorados, exceto que a função pode bloquear se o soquete *s* estiver no modo de bloqueio.
Se o soquete *s* estiver no modo sem bloqueio, essa função ainda será bloqueada, pois esse IOCTL específico não oferece suporte ao modo sem bloqueio.

Para os soquetes sobrepostos, as operações que não podem ser concluídas imediatamente serão iniciadas e a conclusão será indicada mais tarde.

Qualquer IOCTL pode bloquear indefinidamente, dependendo da implementação do provedor de serviço.
Se o aplicativo não puder tolerar o bloqueio em uma chamada de função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** , a e/s sobreposta seria ACONSELHAda para os IOCTLs que são especialmente prováveis de bloquear.

O IOCTL de alteração da lista de **\_ \_ \_ pendências \_ de envio sio ideal** fornece uma notificação e é esperado para bloquear ou ficar pendente até que o valor do ISB seja alterado.
Em geral, ele seria chamado de forma assíncrona com o parâmetro *lpOverlapped* definido como uma estrutura WSAOVERLAPPED válida.

O IOCTL de **alteração da pendência de envio do sio \_ ideal \_ \_ \_** pode falhar com a operação **WSAEINTR** ou **WSA \_ \_ anulada** nos seguintes casos:

* A conexão TCP é desconectada normalmente na direção de envio. Isso pode ocorrer como resultado de uma chamada para a função de desligamento com o parâmetro de como definido como **SD \_ Send**, uma chamada para a função **DisconnectEx** ou uma chamada para a função **TransmitFile** ou **TransmitPackets** com o parâmetro *dwFlags* definido como **TF \_ Disconnect** ou **TF \_ reutilization**.
* A conexão TCP foi redefinida ou anulada.
* O aplicativo emite um **sio \_ ideal \_ Enviar \_ pendências de alteração do registro de \_ alterações** quando já existe uma solicitação de notificação pendente. Somente 1 1 sio pendentes a solicitação de **\_ alteração de pendência de envio do \_ \_ registro posterior \_** é permitida por vez.
* A solicitação é cancelada pelo Gerenciador de e/s.
* O soquete está fechado.

Duas funções de wrapper embutidas para esses IOCTLs são definidas no arquivo de cabeçalho *Ws2tcpip. h* .
É recomendável que essas funções embutidas sejam usadas em vez de usar a consulta de **\_ pendência de envio sio ideal \_ \_ \_** e o [**sio \_ ideal \_ Enviar \_ \_ consultas de pendências**](sio-ideal-send-backlog-query.md) para os IOCTLs diretamente.

A função de wrapper embutido para o **sio \_ ideal \_ Enviar \_ registro da pendência de \_ alteração** do IOCTL é a função **idealsendbacklognotify** .

A função de wrapper embutida para a [**consulta de pendência de \_ \_ envio sio \_ \_ ideal**](sio-ideal-send-backlog-query.md) é a função **idealsendbacklogquery** .

## <a name="see-also"></a>Confira também

[**SIO_IDEAL_SEND_BACKLOG_QUERY**](sio-ideal-send-backlog-query.md)

[**SSA**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
