---
description: O código de controle recupera o registro de redirecionamento para a conexão TCP/IP aceita para uso por um serviço de redirecionamento da plataforma de filtragem do Windows.
ms.assetid: E0D7CC1A-8F93-45A0-9543-3F2ACAF352F5
title: SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 2389914d29bd403a33e23065c29f549a01adbb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790426"
---
# <a name="sio_query_wfp_connection_redirect_records-control-code"></a>SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS código de controle

## <a name="description"></a>Descrição

O código de controle de **\_ \_ \_ \_ redirecionamento \_ de conexão WFP consulta sio** recupera o registro de redirecionamento para a conexão TCP/IP aceita para uso por um serviço de redirecionamento WFP (Windows Filtering Platform).

Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
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
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a>Parâmetros

### <a name="s"></a>s

Um descritor que identifica um soquete.

### <a name="dwiocontrolcode"></a>dwIoControlCode

O código de controle para a operação.
Use **sio \_ consultar \_ os \_ \_ \_ registros de redirecionamento de conexão WFP** para esta operação.

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
| **WSA_IO_PENDING** | Uma operação sobreposta foi iniciada com êxito e a conclusão será indicada em um momento posterior. |
| **WSA_OPERATION_ABORTED** | Uma operação sobreposta foi cancelada devido ao fechamento do soquete ou à execução do comando **SIO_FLUSH** IOCTL. |
| **WSAEFAULT** | O parâmetro *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço de usuário. |
| **WSAEINPROGRESS** | A função é invocada quando um retorno de chamada está em andamento. |
| **WSAEINTR** | Uma operação de bloqueio foi interrompida. |
| **WSAEINVAL** | O parâmetro *dwIoControlCode* não é um comando válido ou um parâmetro de entrada especificado não é aceitável ou o comando não é aplicável ao tipo de soquete especificado. Esse erro será retornado se o parâmetro *cbOutBuffer* for menor que o tamanho de um tipo de dados **ULONG** . |
| **WSAENETDOWN** | Falha no subsistema de rede. |
| **WSAENOPROTOOPT** | Não há suporte para a opção de soquete no protocolo especificado. |
| **WSAENOTCONN** | O soquete *s* não está conectado. |
| **WSAENOTSOCK** | O descritor *s* não é um soquete. |
| **WSAEOPNOTSUPP** | Não há suporte para o comando IOCTL especificado. Esse erro será retornado se a **\_ consulta sio \_ consultar \_ \_ \_ registros de redirecionamento de conexão WFP** não for suportada pelo provedor de transporte. |

## <a name="remarks"></a>Comentários

Os **\_ registros de \_ \_ \_ redirecionamento \_ de conexão WFP de consulta sio** são suportados no Windows 8, no Windows Server 2012 e em versões posteriores do sistema operacional.

A WFP permite o acesso ao caminho de processamento de pacotes TCP/IP, onde os pacotes de saída e de entrada podem ser examinados ou alterados antes de permitir que sejam processados ainda mais.
Ao tocar no caminho de processamento TCP/IP, os ISVs (fornecedores independentes de software) podem criar com mais facilidade firewalls, software antivírus, software de diagnóstico e outros tipos de aplicativos e serviços.
A WFP fornece componentes de modo de usuário e de modo kernel para que ISVs de terceiros possam participar das decisões de filtragem que ocorrem em várias camadas na pilha do protocolo TCP/IP e em todo o sistema operacional.
O recurso de redirecionamento de conexão WFP permite que um driver de kernel de texto explicativo WFP redirecione uma conexão localmente para um processo de modo de usuário, execute a inspeção de conteúdo no modo de usuário e encaminhe o conteúdo inspecionado usando uma conexão diferente com o destino original.

O **sio \_ consulta \_ WFP \_ \_ redirecionar \_ registros** IOCTL e vários outros IOCTLs relacionados são componentes do modo de usuário usados para permitir que vários aplicativos de proxy de conexão baseados em WFP inspecionem o mesmo fluxo de tráfego de maneira cooperativa.
Cada agente de inspeção pode Reinspecionar com segurança o tráfego de rede que já foi inspecionado por outro agente de inspeção.
Com a presença de vários proxies (desenvolvidos por diferentes ISVs, por exemplo), a conexão usada por um proxy para se comunicar com o destino final pode, por sua vez, ser redirecionada por um segundo proxy e essa nova conexão pode ser redirecionada novamente pelo proxy original.
Sem o controle de conexão, a conexão original pode nunca alcançar seu destino final, pois fica presa em um loop de proxy infinito.

O **IOCTL \_ consulta \_ de \_ \_ \_ registros de redirecionamento de conexão WFP sio** é usado para fornecer rastreamento de conexão com proxy em conexões de soquete redirecionadas.
Esse recurso de WFP facilita o rastreamento de registros de redirecionamento do redirecionamento inicial de uma conexão com a conexão final com o destino.

O **sio \_ consulta \_ WFP \_ \_ redirecionar \_ registros** do IOCTL é usado por um serviço de redirecionamento baseado em WFP para recuperar o registro de redirecionamento da conexão de pacote TCP/IP aceita (o Soquete conectado para um soquete TCP ou um soquete UDP, por exemplo) Redirecionado para ele por seu texto explicativo complementar no modo kernel registrado em **ALE_CONNECT_REDIRECT** camadas em um driver de modo kernel.
O **\_ contexto de \_ \_ \_ redirecionamento \_ de conexão WFP de consulta sio** é usado por um serviço de redirecionamento baseado em WFP para recuperar o contexto de redirecionamento de um registro de redirecionamento da conexão de pacote TCP/IP aceita (o Soquete conectado para um soquete TCP ou um soquete UDP, por exemplo) Redirecionado para ele por seu balão complementar registrado nas camadas de **\_ \_ redirecionamento** do
O contexto de redirecionamento é um contexto opcional alocado para driver usado se o estado de redirecionamento atual de uma conexão é que a conexão foi redirecionada pelo serviço de redirecionamento de chamada ou a conexão foi redirecionada anteriormente pelo serviço de redirecionamento de chamada, mas posterior redirecionada por um serviço de redirecionamento diferente.
Para uma conexão de proxy TCP, o serviço de redirecionamento transfere o registro de redirecionamento recuperado para o soquete TCP que ele usa para fazer o proxy do conteúdo original usando o **sio \_ set \_ WFP \_ Connection \_ Redirect de \_ registros** IOCTL.

Quando o serviço de redirecionamento está redirecionando um soquete não TCP (UDP, por exemplo), os registros de redirecionamento retornados pelo **sio \_ consulta \_ WFP \_ \_ \_ registros de redirecionamento de conexão** do o IOCTL indicam isso ao serviço de redirecionamento usando a estrutura [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) usada com a função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .
O membro Control da estrutura [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) teria um cmsg_type na estrutura **WSACMSGHDR** definida como **\_ \_ \_ registro de redirecionamento de conexão IP**.
O parâmetro [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) deve ser fornecido pelo serviço de redirecionamento ao aceitar redirecionamentos não TCP.

Para o tráfego não TCP, o registro de redirecionamento é encaminhado usando a estrutura [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) com a função [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .

Observe que, para o tráfego não TCP, somente o pacote de criação de fluxo carregará o **\_ \_ \_ registro de redirecionamento de conexão IP**.
Como resultado, somente o primeiro pacote com proxy precisa incluir essas informações usando a função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .

Como o registro de redirecionamento de WFP é um blob de dados de comprimento variável, o chamador pode fornecer um buffer de saída grande (um buffer de 1.024 bytes apontado pelo parâmetro *lpvOutBuffer* , por exemplo) ou pode passar um tamanho de buffer de saída no parâmetro *cbOutBuffer* de 0 para consultar o tamanho do buffer necessário para manter o blob retornado.
Se o tamanho do buffer de saída não for suficiente para manter os dados, as funções [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornarão um **erro de \_ \_ buffer insuficiente** e o tamanho de buffer necessário será retornado no valor apontado pelo parâmetro *lpcbBytesReturned* .

O aplicativo que chama o [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) não precisa entender o blob que contém o contexto de redirecionamento recuperado.
Este é um blob opaco de dados que o aplicativo precisa recuperar e passar de volta para o novo soquete.

## <a name="see-also"></a>Confira também

[**Opções de soquete IPPROTO_IP**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md)

[**SSA**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)

[**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
