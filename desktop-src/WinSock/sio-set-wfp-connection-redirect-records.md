---
description: O código de controle define o registro de redirecionamento para o novo soquete TCP usado para conectar o serviço de redirecionamento.
ms.assetid: 0AC78ED4-A6EC-4D62-919C-1EF7CDE8EE80
title: Código de controle SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 11ce07c94104ecd986dc117b00dba2a49a7b5dc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105794011"
---
# <a name="sio_set_wfp_connection_redirect_records-control-code"></a>Código de controle SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS

## <a name="description"></a>Descrição

O código de controle **sio \_ set \_ WFP \_ Connection \_ Redirect \_** define o registro de redirecionamento para o novo soquete TCP usado para se conectar ao destino final para uso por um serviço de redirecionamento WFP (Windows Filtering Platform).

Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.

```cpp
int WSAIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine, // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,              // a WSATHREADID structure
  (LPINT) lpErrno                          // a pointer to the error code.
);
```

## <a name="parameters"></a>Parâmetros

### <a name="s"></a>s

Um descritor que identifica um soquete.

### <a name="dwiocontrolcode"></a>dwIoControlCode

O código de controle para a operação.
Use **sio \_ definir \_ \_ \_ \_ registros de redirecionamento de conexão WFP** para esta operação.

### <a name="lpvinbuffer"></a>lpvInBuffer

Um ponteiro para o buffer de entrada.
Esse parâmetro contém um ponteiro para o registro de redirecionamento de WFP associado ao soquete.

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

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.

Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.
Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Código do erro | Significado |
|------------|---------|
| **\_e/s de WSA \_ pendente** | A operação de e/s sobreposta está em andamento. Esse valor será retornado se uma operação sobreposta tiver sido iniciada com êxito e a conclusão será indicada mais tarde. |
| **operação de WSA \_ \_ anulada** | A operação de e/s foi anulada devido a uma saída de thread ou uma solicitação de aplicativo. Esse erro será retornado se uma operação sobreposta tiver sido cancelada devido ao fechamento do soquete ou à execução do comando **SIO_FLUSH** IOCTL. |
| **WSAEACCES** | Foi feita uma tentativa de acessar um soquete de uma maneira proibida por suas permissões de acesso. Esse erro é retornado sob várias condições que incluem o seguinte: o usuário não tem os privilégios administrativos necessários no computador local ou o aplicativo não está sendo executado em um shell avançado como administrador interno ( `RunAs administrator` ). |
| **WSAEFAULT** | O sistema detectou um endereço de ponteiro inválido ao tentar usar um argumento de ponteiro em uma chamada. Esse erro é retornado do parâmetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço de usuário. |
| **WSAEINPROGRESS** | Uma operação de bloqueio está atualmente em execução. Esse erro será retornado se a função for invocada quando um retorno de chamada estiver em andamento. |
| **WSAEINTR** | Uma operação de bloqueio foi interrompida por uma chamada para **WSACancelBlockingCall**. Esse erro será retornado se uma operação de bloqueio tiver sido interrompida. |
| **WSAEINVAL** | Foi fornecido um argumento inválido. Esse erro será retornado se o parâmetro *dwIoControlCode* não for um comando válido ou se um parâmetro de entrada especificado não for aceitável ou se o comando não for aplicável ao tipo de soquete especificado. |
| **WSAENETDOWN** | Uma operação de soquete encontrou uma rede inoperante. Esse erro será retornado se o subsistema de rede tiver falhado. |
| **WSAENOTSOCK** | Uma operação foi tentada em algo que não é um soquete. Esse erro será retornado se o descritor *s* não for um soquete. |
| **WSAEOPNOTSUPP** | Não há suporte para a operação tentada para o tipo de objeto referenciado. Esse erro será retornado se o comando IOCTL especificado não tiver suporte. Esse erro também será retornado se o **sio \_ definir \_ os \_ \_ \_ registros de redirecionamento de conexão WFP** não for suportado pelo provedor de transporte. |

## <a name="remarks"></a>Comentários

O **sio \_ conjunto \_ de \_ \_ \_ registros de redirecionamento de conexão WFP** não tem suporte no Windows 8, no Windows Server 2012 e em versões posteriores do sistema operacional.

A WFP permite o acesso ao caminho de processamento de pacotes TCP/IP, onde os pacotes de saída e de entrada podem ser examinados ou alterados antes de permitir que sejam processados ainda mais.
Ao tocar no caminho de processamento TCP/IP, os ISVs (fornecedores independentes de software) podem criar com mais facilidade firewalls, software antivírus, software de diagnóstico e outros tipos de aplicativos e serviços.
A WFP fornece componentes de modo de usuário e de modo kernel para que ISVs de terceiros possam participar das decisões de filtragem que ocorrem em várias camadas na pilha do protocolo TCP/IP e em todo o sistema operacional.
O recurso de redirecionamento de conexão WFP permite que um driver de kernel de texto explicativo WFP redirecione uma conexão localmente para um processo de modo de usuário, execute a inspeção de conteúdo no modo de usuário e encaminhe o conteúdo inspecionado usando uma conexão diferente com o destino original.

O **sio \_ set \_ WFP \_ \_ reredirect \_ RECORDs** IOCTL e vários outros IOCTLs relacionados são componentes do modo de usuário usados para permitir que vários aplicativos de proxy de conexão baseados em WFP inspecionem o mesmo fluxo de tráfego de maneira cooperativa.
Cada agente de inspeção pode Reinspecionar com segurança o tráfego de rede que já foi inspecionado por outro agente de inspeção.
Com a presença de vários proxies (desenvolvidos por diferentes ISVs, por exemplo), a conexão usada por um proxy para se comunicar com o destino final pode, por sua vez, ser redirecionada por um segundo proxy e essa nova conexão pode ser redirecionada novamente pelo proxy original.
Sem o controle de conexão, a conexão original pode nunca alcançar seu destino final, pois fica presa em um loop de proxy infinito.

O **sio \_ set \_ WFP \_ Connection \_ Redirect \_ Records** IOCTL é usado para fornecer rastreamento de conexão com proxy em conexões de soquete redirecionadas.
Esse recurso de WFP facilita o rastreamento de registros de redirecionamento do redirecionamento inicial de uma conexão com a conexão final com o destino.

O [**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md) IOCTL é usado por um serviço de redirecionamento baseado em WFP para recuperar o registro de redirecionamento da conexão de pacote TCP/IP aceita (o Soquete conectado para um soquete TCP ou um soquete UDP, por exemplo) Redirecionado para ele por seu texto explicativo do modo kernel complementar registrado em camadas de  **\_ \_ redirecionamento da conexão Ale** em um driver de modo kernel.
O [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) IOCTL recupera o contexto de redirecionamento para um registro de redirecionamento, que é usado.
O contexto de redirecionamento é opcional e é usado se o estado de redirecionamento atual de uma conexão é que a conexão foi redirecionada pelo serviço de redirecionamento de chamada ou a conexão foi redirecionada anteriormente pelo serviço de redirecionamento de chamada, mas mais tarde redirecionada novamente por um serviço de redirecionamento diferente. O serviço de redirecionamento transfere o registro de redirecionamento recuperado para o soquete TCP que ele usa para fazer proxy do conteúdo original usando o **sio \_ set \_ WFP \_ Connection \_ Redirect de \_ registros** IOCTL.

O aplicativo que chama o **sio \_ set \_ WFP \_ Connection Redirect de \_ \_ registros** IOCTL não precisa entender o blob que contém o registro de redirecionamento que está sendo definido.
Este é um blob opaco de dados que o aplicativo precisa passar para o novo soquete.

## <a name="see-also"></a>Confira também

[**Opções de soquete IPPROTO_IP**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md)

[**SSA**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
