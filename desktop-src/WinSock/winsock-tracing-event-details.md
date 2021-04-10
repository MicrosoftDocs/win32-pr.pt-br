---
description: Detalhes de rastreamento de eventos de rede do Winsock
ms.assetid: f0386bd3-15d0-45f3-82c9-365d1c9f59c5
title: Detalhes de rastreamento de eventos de rede do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588363420aee9c3b04f4f8060bbd9c77b9cc3232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170773"
---
# <a name="winsock-network-event-tracing-details"></a>Detalhes de rastreamento de eventos de rede do Winsock

Os detalhes a seguir cada um dos eventos de rede Winsock que podem ser rastreados e descreve quais parâmetros e informações são registrados.

## <a name="socket-creation"></a>Criação de soquete

ID do evento = 1

Nível = 4 (informações)

Os seguintes eventos do Winsock são rastreados para a criação de soquete:

-   Identificadores de soquete criados por chamadas para as funções [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) ou [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) .
-   Identificadores de soquete aceitos em soquetes de escuta.
-   Identificadores de soquete criados por chamadas para a função [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) .
-   Identificadores de soquete reutilizados por chamadas para as funções [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) ou [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) .

Os seguintes parâmetros são registrados em log para um evento de criação de soquete:



| Parâmetro                                                                                                        | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>                 | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/>             | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="SocketType"></span><span id="sockettype"></span><span id="SOCKETTYPE"></span>SocketType<br/>     | O tipo do soquete.<br/>                                                     |
| <span id="Protocol"></span><span id="protocol"></span><span id="PROTOCOL"></span>Protocolo<br/>             | O protocolo do soquete.<br/>                                                 |
| <span id="UserModePid"></span><span id="usermodepid"></span><span id="USERMODEPID"></span>UserModePid<br/> | A ID do processo do modo de usuário que criou o soquete.<br/>                           |



 

## <a name="socket-bind"></a>Associação de soquete

ID do evento = 2 (IPv4), ID do evento = 3 (IPv6)

Nível = 4 (informações)

Os seguintes eventos do Winsock são rastreados para uma operação de associação:

-   Associação implícita ou explícita de um identificador de soquete.

Os seguintes parâmetros são registrados em log para um evento de ligação:



| Parâmetro                                                                                            | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/> | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Corrigir<br/>     | O endereço IP local.<br/>                                                       |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto<br/>                 | O número da porta IP local.<br/>                                                   |
| <span id="Status"></span><span id="status"></span><span id="STATUS"></span>Estado<br/>         | O status ou o código de erro retornado para a operação de associação.<br/>                   |



 

## <a name="failed-bind"></a>Falha na ligação

ID do evento = 40

Nível = 4 (informações)

Os seguintes eventos do Winsock são rastreados para uma operação de ligação com falha:

-   Associação implícita ou explícita de um identificador de soquete que falha.

Os seguintes parâmetros são registrados em log para um evento de ligação com falha:



| Parâmetro                                                                                            | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/> | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao<br/>             | O código de erro retornado para a operação de ligação com falha.<br/>                     |



 

## <a name="socket-connect"></a>Conexão de soquete

ID do evento = 4 (IPv4), ID do evento = 5 (IPv6)

Nível = 4 (informações)

Os seguintes eventos do Winsock são rastreados para uma solicitação de operação de conexão (uma chamada para a função [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)ou [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) ):

-   Conectar um soquete a um destino para um soquete orientado a conexão ou sem conexão.

Os seguintes parâmetros são registrados em log para um evento Connect:



| Parâmetro                                                                                            | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/> | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Corrigir<br/>     | O endereço IP remoto.<br/>                                                      |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto<br/>                 | O número da porta IP remota.<br/>                                                  |



 

## <a name="connect-completed"></a>Conexão concluída

ID do evento = 6

Nível = 4 (informações)

Os seguintes eventos do Winsock são rastreados para uma conexão concluída:

-   A operação de conexão foi concluída.

Os seguintes parâmetros são registrados em log para um evento Connect Completed:



| Parâmetro                                                                                            | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/> | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao<br/>             | O código de erro retornado para a operação de conexão.<br/>                          |



 

## <a name="afd-initiated-abort"></a>Anular AFD-Initiated

ID do evento = 7

Nível = 4 (informações)

Os seguintes eventos do Winsock são rastreados para anulações iniciadas pelo Winsock ou operações de cancelamento:

-   Uma anulação devido a dados de recebimento não lidos armazenados em buffer após o fechamento.
-   Uma anulação após uma chamada para a função de [**desligamento**](/windows/desktop/api/winsock/nf-winsock-shutdown) com o parâmetro de *como* definido como SD \_ Receive e uma chamada para a função [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) com dados de recebimento pendentes.
-   Uma anulação após uma tentativa com falha de liberar o ponto de extremidade.
-   Uma anulação após um erro interno do Winsock ocorreu.
-   Uma anulação devido a uma conexão com erros e o aplicativo solicitou anteriormente que a conexão fosse anulada em determinadas circunstâncias. Um exemplo desse caso seria um aplicativo que foi definido como \_ remanescente com um tempo limite de zero e ainda há dados não confirmados na conexão.
-   Uma anulação em uma conexão não está totalmente associada à aceitação do ponto de extremidade.
-   Uma anulação em uma chamada com falha para a função [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) ou [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) .
-   Uma anulação devido a uma falha na operação de recebimento.
-   Uma anulação devido a um evento de Plug and Play.
-   Uma anulação devido a uma solicitação de liberação com falha.
-   Uma anulação devido a uma solicitação de recebimento de dados emitida com falha.
-   Uma anulação devido a uma solicitação de envio com falha.
-   Uma anulação devido à solicitação de envio cancelada.
-   Uma anulação devido a um cancelamento chamado para a função [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) .

Os parâmetros a seguir são registrados para uma operação de anulação ou cancelamento iniciada pelo Winsock:



| Parâmetro                                                                                            | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/> | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Falha<br/>         | O motivo para a operação anular ou cancelar.<br/>                               |



 

## <a name="transport-initiated-abort"></a>Anular Transport-Initiated

ID do evento = 8

Nível = 4 (informações)

Os seguintes eventos do Winsock são rastreados para operações de anular ou cancelar iniciadas pelo transporte:

-   Redefinição indicada pelo transporte.

Os parâmetros a seguir são registrados para uma operação de anulação ou cancelamento iniciada pelo Winsock:



| Parâmetro                                                                                            | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/> | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Falha<br/>         | O motivo para a operação anular ou cancelar.<br/>                               |



 

## <a name="failed-send-request"></a>Solicitação de envio com falha

ID do evento = 9

Nível = 4 (informações)

Os seguintes eventos do Winsock são rastreados para erros em solicitações de [**envio**](/windows/desktop/api/Winsock2/nf-winsock2-send) ou [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) :

-   Erros retornados em solicitações de [**envio**](/windows/desktop/api/Winsock2/nf-winsock2-send) ou [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) com falha.

Os parâmetros a seguir são registrados em log para solicitações de envio que resultam em um erro:



| Parâmetro                                                                                            | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/> | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao<br/>             | O código de erro retornado para a operação.<br/>                                  |



 

## <a name="failed-wsasendmsg-request"></a>Falha na solicitação de WsaSendMsg

ID do evento = 10

Nível = 4 (informações)

Os seguintes eventos do Winsock são rastreados para erros em solicitações [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) :

-   Erros retornados em solicitações [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) com falha.

Os parâmetros a seguir são registrados em log para solicitações de envio que resultam em um erro:



| Parâmetro                                                                                            | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/> | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao<br/>             | O código de erro retornado para a operação.<br/>                                  |



 

## <a name="failed-recv-request"></a>Solicitação de recv com falha

ID do evento = 11

Nível = 4 (informações)

Os seguintes eventos do Winsock são rastreados para erros em solicitações de [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)ou [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) :

-   Erros retornados em solicitações de recebimento com falha.

Os parâmetros a seguir são registrados em log para solicitações de envio que resultam em um erro:



| Parâmetro                                                                                            | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/> | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao<br/>             | O código de erro retornado para a operação.<br/>                                  |



 

## <a name="failed-recvfrom-request"></a>Falha na solicitação de recvfrom

ID do evento = 12

Nível = 4 (informações)

Os seguintes eventos do Winsock são rastreados para erros em solicitações [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) ou [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) :

-   Erros retornados em solicitações [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) ou [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) com falha.

Os parâmetros a seguir são registrados para uma solicitação [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) ou [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) que resulta em um erro:



| Parâmetro                                                                                            | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/> | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao<br/>             | O código de erro retornado para a operação.<br/>                                  |



 

## <a name="socket-close"></a>Fechamento de soquete

ID do evento = 13

Nível = 4 (informações)

Os seguintes eventos do Winsock são rastreados para operações de fechamento de soquete:

-   Um identificador de soquete está fechado.

Os seguintes parâmetros são registrados em log para um evento de fechamento de soquete:



| Parâmetro                                                                                            | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/> | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao<br/>             | O valor de retorno para a operação de fechamento de soquete.<br/>                            |



 

## <a name="socket-cleanup"></a>Limpeza de soquete

ID do evento = 14

Nível = 4 (informações)

Os seguintes eventos do Winsock são rastreados para operações de limpeza de soquete (desligamento):

-   A função de [**desligamento**](/windows/desktop/api/winsock/nf-winsock-shutdown) é chamada em um soquete.
-   O transporte indica uma desconexão normal com falha.

Os seguintes parâmetros são registrados em log para um evento de limpeza de soquete (desligamento) ou de fechamento de soquete:



| Parâmetro                                                                                            | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/> | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao<br/>             | O valor de retorno para a operação de limpeza de soquete (desligamento).<br/>               |



 

## <a name="socket-accept"></a>Aceitação de soquete

ID do evento = 15 (IPv4), ID do evento = 16 (IPv6)

Nível = 4 (informações)

Os seguintes eventos do Winsock são rastreados para uma solicitação de função [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) :

-   Uma solicitação de função [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) em um identificador de soquete.

Os seguintes parâmetros são registrados em log para um evento de aceitação:



| Parâmetro                                                                                            | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/> | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Corrigir<br/>     | O endereço IP remoto.<br/>                                                      |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto<br/>                 | O número da porta IP remota.<br/>                                                  |
| <span id="Status"></span><span id="status"></span><span id="STATUS"></span>Estado<br/>         | O status ou o código de erro retornado para a operação de aceitação.<br/>                 |



 

## <a name="accept-failed"></a>Falha ao aceitar

ID do evento = 17

Nível = 4 (informações)

Os seguintes eventos do Winsock são rastreados para uma operação de aceitação com falha:

-   Uma solicitação [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) em um identificador de soquete que falha.

Os seguintes parâmetros são registrados em log para um evento de aceitação com falha:



| Parâmetro                                                                                            | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/> | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao<br/>             | O código de erro retornado para a operação de aceitação com falha.<br/>                   |



 

## <a name="send-posted"></a>Enviar Postado

ID do evento = 18

Nível = 5 (detalhado)

Para diagnosticar a corrupção do buffer do usuário (por exemplo, quando um aplicativo reutiliza o mesmo buffer em outra chamada de envio ou recebimento enquanto ele ainda está em uso), o buffer de dados é registrado quando é Postado no Winsock e após a conclusão do transporte subjacente. Os seguintes eventos do Winsock são rastreados para operações de envio de soquete e recepção de buffer de recebimento:

-   Um aplicativo publica um envio.
-   Uma operação de envio é concluída para o Winsock.

Os parâmetros a seguir são registrados para operações de envio de soquete:



| Parâmetro                                                                                                            | Descrição                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>                     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/>                 | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | Um valor booliano que indica se a e/s de caminho rápido foi usada.<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | A contagem de buffers.<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Completo<br/>                         | O endereço virtual do buffer. Para buffers encadeados, esse parâmetro é o endereço virtual do primeiro buffer na cadeia.<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | A duração do buffer. Para buffers encadeados, esse parâmetro é o número total de bytes em todos os buffers na cadeia.<br/>  |



 

Quando FastPath é true, o endereço de UserMode do primeiro buffer na matriz de buffers é registrado no parâmetro buffer. Quando FastPath é false, o endereço de buffer do kernel do Winsock é registrado no parâmetro buffer.

## <a name="receive-posted"></a>Receber Postado

ID do evento = 19

Nível = 5 (detalhado)

Para diagnosticar a corrupção do buffer do usuário (por exemplo, quando um aplicativo reutiliza o mesmo buffer em outra chamada de envio ou recebimento enquanto ele ainda está em uso), o buffer de dados é registrado quando é Postado no Winsock e após a conclusão do transporte subjacente. Os seguintes eventos do Winsock são rastreados para operações de postagem do buffer de recebimento de soquete:

-   Um aplicativo posta um Receive.
-   Uma operação de recebimento é concluída para o Winsock.

Os parâmetros a seguir são registrados para operações de recebimento de soquete:



| Parâmetro                                                                                                            | Descrição                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>                     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/>                 | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | Um valor booliano que indica se a e/s de caminho rápido foi usada.<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | A contagem de buffers.<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Completo<br/>                         | O endereço virtual do buffer. Para buffers encadeados, esse parâmetro é o endereço virtual do primeiro buffer na cadeia.<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | A duração do buffer. Para buffers encadeados, esse parâmetro é o número total de bytes em todos os buffers na cadeia.<br/>  |



 

Quando FastPath é true, o endereço de UserMode do primeiro buffer na matriz de buffers é registrado no parâmetro buffer. Quando FastPath é false, o endereço de buffer do kernel do Winsock é registrado no parâmetro buffer.

## <a name="recvfrom-posted"></a>RecvFrom Postado

ID do evento = 20

Nível = 5 (detalhado)

Para diagnosticar a corrupção do buffer do usuário (por exemplo, quando um aplicativo reutiliza o mesmo buffer em outra chamada de envio ou recebimento enquanto ele ainda está em uso), o buffer de dados é registrado quando é Postado no Winsock e após a conclusão do transporte subjacente. Os seguintes eventos do Winsock são rastreados para uma operação post do buffer [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) em um soquete:

-   Um aplicativo posta uma operação de recebimento de.

Os parâmetros a seguir são registrados para a operação recvfrom:



| Parâmetro                                                                                                            | Descrição                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>                     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/>                 | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | Um valor booliano que indica se a e/s de caminho rápido foi usada.<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | A contagem de buffers.<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Completo<br/>                         | O endereço virtual do buffer. Para buffers encadeados, esse parâmetro é o endereço virtual do primeiro buffer na cadeia.<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | A duração do buffer. Para buffers encadeados, esse parâmetro é o número total de bytes em todos os buffers na cadeia.<br/>  |



 

Quando FastPath é true, o endereço de UserMode do primeiro buffer na matriz de buffers é registrado no parâmetro buffer. Quando FastPath é false, o endereço de buffer do kernel do Winsock é registrado no parâmetro buffer.

## <a name="sendto-posted"></a>SendTo Postado

ID do evento = 21 (IPv4), ID do evento = 22 (IPv6)

Nível = 5 (detalhado)

Para diagnosticar a corrupção do buffer do usuário (por exemplo, quando um aplicativo reutiliza o mesmo buffer em outra chamada de envio ou recebimento enquanto ele ainda está em uso), o buffer de dados é registrado quando é Postado no Winsock e após a conclusão do transporte subjacente. Os seguintes eventos do Winsock são rastreados para uma operação post do buffer [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) em um soquete:

-   Um aplicativo publica um envio de.

Os parâmetros a seguir são registrados para a operação [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) :



| Parâmetro                                                                                                            | Descrição                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>                     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/>                 | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | Um valor booliano que indica se a e/s de caminho rápido foi usada.<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | A contagem de buffers.<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Completo<br/>                         | O endereço virtual do buffer. Para buffers encadeados, esse parâmetro é o endereço virtual do primeiro buffer na cadeia.<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | A duração do buffer. Para buffers encadeados, esse parâmetro é o número total de bytes em todos os buffers na cadeia.<br/>  |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Corrigir<br/>                     | O endereço IP remoto do soquete.<br/>                                                                                            |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto<br/>                                 | O número da porta IP remota do soquete.<br/>                                                                                        |



 

Quando FastPath é true, o endereço de UserMode do primeiro buffer na matriz de buffers é registrado no parâmetro buffer. Quando FastPath é false, o endereço de buffer do kernel do Winsock é registrado no parâmetro buffer.

## <a name="recv-completed"></a>Recv concluído

ID do evento = 23

Nível = 5 (detalhado)

Para diagnosticar a corrupção do buffer do usuário (por exemplo, quando um aplicativo reutiliza o mesmo buffer em outra chamada de envio ou recebimento enquanto ele ainda está em uso), o buffer de dados é registrado quando é Postado no Winsock e após a conclusão do transporte subjacente. Os seguintes eventos do Winsock são rastreados para operações de recebimento de soquete concluídas:

-   Uma operação de envio é concluída para o transporte.
-   Uma operação de recebimento é concluída para o transporte.

Os seguintes parâmetros são registrados em log para um envio concluído ou recebimento concluído:



| Parâmetro                                                                                                            | Descrição                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>                     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                                                                                   |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/>                 | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/>                                                              |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Completo<br/>                         | O endereço virtual do buffer. Para buffers encadeados, esse parâmetro é o endereço virtual do primeiro buffer na cadeia.<br/>          |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | O comprimento do buffer de bytes recebidos. Para buffers encadeados, esse parâmetro é o total de bytes recebidos em todos os buffers na cadeia.<br/> |



 

## <a name="send-completed"></a>Envio concluído

ID do evento = 24

Nível = 5 (detalhado)

Para diagnosticar a corrupção do buffer do usuário (por exemplo, quando um aplicativo reutiliza o mesmo buffer em outra chamada de envio ou recebimento enquanto ele ainda está em uso), o buffer de dados é registrado quando é Postado no Winsock e após a conclusão do transporte subjacente. Os seguintes eventos do Winsock são rastreados para operações de envio de soquete concluídas:

-   Uma operação de envio é concluída para o transporte.

Os seguintes parâmetros são registrados em log para um envio concluído:



| Parâmetro                                                                                                            | Descrição                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>                     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                                                                             |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/>                 | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/>                                                        |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Completo<br/>                         | O endereço virtual do buffer. Para buffers encadeados, esse parâmetro é o endereço virtual do primeiro buffer na cadeia.<br/>    |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | O comprimento do buffer de bytes enviados. Para buffers encadeados, esse parâmetro é o total de bytes enviados de todos os buffers na cadeia.<br/> |



 

## <a name="sendmsg-completed"></a>SendMsg concluído

ID do evento = 25

Nível = 5 (detalhado)

Para diagnosticar a corrupção do buffer do usuário (por exemplo, quando um aplicativo reutiliza o mesmo buffer em outra chamada de envio ou recebimento enquanto ele ainda está em uso), o buffer de dados é registrado quando é Postado no Winsock e após a conclusão do transporte subjacente. Os seguintes eventos do Winsock são rastreados quando uma operação post do buffer [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) é concluída em um soquete:

-   Um aplicativo conclui uma operação [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .

Os parâmetros a seguir são registrados para a conclusão do [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) :



| Parâmetro                                                                                                            | Descrição                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>                     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                                                                             |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/>                 | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/>                                                        |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | A contagem de buffers.<br/>                                                                                                                  |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Completo<br/>                         | O endereço virtual do buffer. Para buffers encadeados, esse parâmetro é o endereço virtual do primeiro buffer na cadeia.<br/>    |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | O comprimento do buffer de bytes enviados. Para buffers encadeados, esse parâmetro é o total de bytes enviados de todos os buffers na cadeia.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Corrigir<br/>                     | O endereço IP remoto do soquete.<br/>                                                                                               |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto<br/>                                 | O número da porta IP remota do soquete.<br/>                                                                                           |



 

## <a name="recvfrom-completed"></a>RecvFrom concluído

ID do evento = 26 (IPv4), ID do evento = 27 (IPv6)

Nível = 5 (detalhado)

Para diagnosticar a corrupção do buffer do usuário (por exemplo, quando um aplicativo reutiliza o mesmo buffer em outra chamada de envio ou recebimento enquanto ele ainda está em uso), o buffer de dados é registrado quando é Postado no Winsock e após a conclusão do transporte subjacente. Os seguintes eventos do Winsock são rastreados quando uma operação post do buffer [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) é concluída em um soquete:

-   Um aplicativo conclui uma operação [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) .

Os parâmetros a seguir são registrados para a conclusão do [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) :



| Parâmetro                                                                                                            | Descrição                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>                     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                                                                                   |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/>                 | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/>                                                              |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | A contagem de buffers.<br/>                                                                                                                        |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Completo<br/>                         | O endereço virtual do buffer. Para buffers encadeados, esse parâmetro é o endereço virtual do primeiro buffer na cadeia.<br/>          |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | O comprimento do buffer de bytes recebidos. Para buffers encadeados, esse parâmetro é o total de bytes recebidos em todos os buffers na cadeia.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Corrigir<br/>                     | O endereço IP remoto do soquete.<br/>                                                                                                     |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto<br/>                                 | O número da porta IP remota do soquete.<br/>                                                                                                 |



 

## <a name="sendto-completed"></a>SendTo concluído

ID do evento = 28

Nível = 5 (detalhado)

Para diagnosticar a corrupção do buffer do usuário (por exemplo, quando um aplicativo reutiliza o mesmo buffer em outra chamada de envio ou recebimento enquanto ele ainda está em uso), o buffer de dados é registrado quando é Postado no Winsock e após a conclusão do transporte subjacente. Os seguintes eventos do Winsock são rastreados quando uma operação post do buffer [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) é concluída em um soquete:

-   Um aplicativo conclui uma operação [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) .

Os parâmetros a seguir são registrados para a conclusão do [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) :



| Parâmetro                                                                                                            | Descrição                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>                     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                                                                             |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/>                 | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/>                                                        |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | A contagem de buffers.<br/>                                                                                                                  |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Completo<br/>                         | O endereço virtual do buffer. Para buffers encadeados, esse parâmetro é o endereço virtual do primeiro buffer na cadeia.<br/>    |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | O comprimento do buffer de bytes enviados. Para buffers encadeados, esse parâmetro é o total de bytes enviados de todos os buffers na cadeia.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Corrigir<br/>                     | O endereço IP remoto do soquete.<br/>                                                                                               |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto<br/>                                 | O número da porta IP remota do soquete.<br/>                                                                                           |



 

## <a name="socket-option-set"></a>Conjunto de opções de soquete

ID do evento = 29

Nível = 5 (detalhado)

Sempre que um aplicativo altera determinados valores de opção de soquete e IOCTLs, os novos valores serão registrados em log. As opções registradas podem ser usadas para diagnosticar mau desempenho ou comportamento estranho em aplicativos. Os seguintes eventos do Winsock são rastreados para determinadas opções de soquete e IOCTLs:

-   Portanto, o \_ SNDBUF muda.
-   Portanto, o \_ RCVBUF muda.
-   FIONBIO
-   SIO \_ habilitar \_ \_ enfileiramento circular
-   SIO \_ UDP \_ CONNRESET
-   \_OOBINLINE

Os parâmetros a seguir são registrados para chamadas de função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) e [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) que alteram qualquer um dos valores acima:



| Parâmetro                                                                                            | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/> | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="Option"></span><span id="option"></span><span id="OPTION"></span>Option<br/>         | A opção de soquete ou o IOCTL que é alterado. <br/>                                |
| <span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor<br/>             | O novo valor para a opção de soquete ou o IOCTL. <br/>                              |



 

## <a name="selectpoll-posted"></a>Selecionar/sondagem postada

ID do evento = 30

Nível = 5 (detalhado)

Os seguintes eventos do Winsock são rastreados quando um aplicativo chama a função [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :

-   O aplicativo posta uma solicitação [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .

Os parâmetros a seguir são registrados para eventos [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :



| Parâmetro                                                                                                        | Descrição                                                                                                    |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>                 | A ID do processo de propriedade.<br/>                                                                              |
| <span id="HandleCount"></span><span id="handlecount"></span><span id="HANDLECOUNT"></span>HandleCount<br/> | O número de identificadores passados pelo aplicativo (válido somente no evento de inicialização).<br/>            |
| <span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>Cedido<br/>                 | O tempo máximo para a função [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) aguardar.<br/> |



 

## <a name="selectpoll-completed"></a>Seleção/sondagem concluída

ID do evento = 31

Nível = 5 (detalhado)

Os seguintes eventos do Winsock são rastreados quando um aplicativo chama a função [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :

-   O Winsock conclui uma chamada [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .

Os parâmetros a seguir são registrados quando uma operação [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) é concluída:



| Parâmetro                                                                                            | Descrição                                                                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                                              |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/> | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/>                         |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao<br/>             | O código de erro retornado para a operação [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .<br/> |



 

## <a name="wsaeventselect"></a>WSAEventSelect

ID do evento = 32

Nível = 5 (detalhado)

Os seguintes eventos do Winsock são rastreados quando um aplicativo chama a função [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) :

-   Registre a máscara de evento passada na função [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) .

Os parâmetros a seguir são registrados para chamadas de função [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) :



| Parâmetro                                                                                                | Descrição                                                                            |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>         | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/>     | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="EventMask"></span><span id="eventmask"></span><span id="EVENTMASK"></span>EventMask<br/> | O valor da máscara de evento. <br/>                                              |



 

## <a name="dropped-datagram"></a>Datagram removido

ID do evento = 33 (IPv4), ID do evento = 34 (IPv6)

Nível = 5 (detalhado)

Para ajudar a diagnosticar problemas em relação a aplicativos de datagrama, os seguintes eventos de Winsock são rastreados:

-   Quando um datagrama chega e é removido do espaço de buffer insuficiente.
-   Em um datagrama conectado, se os dados chegarem de uma fonte diferente de destino conectado.

Os seguintes parâmetros são registrados em log para datagramas removidos:



| Parâmetro                                                                                                    | Descrição                                                                            |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>             | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/>         | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="PacketSize"></span><span id="packetsize"></span><span id="PACKETSIZE"></span>Tamanho<br/> | O tamanho do pacote que foi Descartado. <br/>                                   |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Corrigir<br/>             | O endereço IP da origem do pacote. <br/>                                |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto<br/>                         | O número da porta IP da origem do pacote.<br/>                             |
| <span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Falha<br/>                 | O código de erro ou o motivo pelo qual o pacote foi Descartado.<br/>                            |



 

## <a name="connection-indicated"></a>Conexão indicada

ID do evento = 35 (IPv4), ID do evento = 36 (IPv6)

Nível = 5 (detalhado)

Os seguintes eventos do Winsock são rastreados para operações indicadas de conexão:

-   Um aplicativo recebe uma solicitação de conexão.

Os seguintes parâmetros são registrados em log para conexões indicadas de eventos de transporte:



| Parâmetro                                                                                            | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/> | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Corrigir<br/>     | O endereço IP remoto. <br/>                                                     |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto<br/>                 | O número da porta IP remota.<br/>                                                  |



 

## <a name="data-indicated"></a>Dados indicados

ID do evento = 37

Nível = 5 (detalhado)

Os seguintes eventos do Winsock são rastreados para operações indicadas de dados:

-   Um aplicativo recebe dados em um Soquete conectado.

Os seguintes parâmetros são registrados em log para dados indicados de eventos de transporte:



| Parâmetro                                                                                                                        | Descrição                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>                                 | A ID do processo de propriedade.<br/>                                                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/>                             | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes indicados<br/> | O número de bytes recebidos no soquete.<br/>                                 |



 

## <a name="data-indicated-from-transport"></a>Dados indicados do transporte

ID do evento = 38 (IPv4), ID do evento = 39 (IPv6)

Nível = 5 (detalhado)

Os seguintes eventos do Winsock são rastreados para dados indicados de operações de transporte:

-   Um aplicativo posta uma solicitação de recebimento e recebe dados.

Os seguintes parâmetros são registrados em log para dados indicados de eventos de transporte:



| Parâmetro                                                                                                                        | Descrição                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>                                 | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/>                             | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Corrigir<br/>                                 | O endereço IP remoto. <br/>                                                     |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto<br/>                                             | O número da porta IP remota.<br/>                                                  |
| <span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes indicados<br/> | O número de bytes recebidos no soquete.<br/>                                 |



 

## <a name="disconnect-indicated-from-transport"></a>Desconexão indicada pelo transporte

ID do evento = 41

Nível = 5 (detalhado)

Os seguintes eventos do Winsock são rastreados para operações indicadas de desconexão:

-   Um aplicativo recebe uma indicação de desconexão.

Os seguintes parâmetros são registrados para desconexão indicada de eventos de transporte:



| Parâmetro                                                                                            | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process<br/>     | O endereço da estrutura EPROCESS do kernel para o processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade<br/> | O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controle do rastreamento do Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Rastreamento de Winsock](winsock-tracing.md)
</dt> <dt>

[Detalhes de rastreamento de alteração do catálogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Níveis de rastreamento do Winsock](winsock-tracing-levels.md)
</dt> </dl>

 

 
