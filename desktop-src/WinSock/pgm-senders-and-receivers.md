---
description: O estabelecimento de uma sessão PGM é semelhante à rotina de estabelecimento da conexão associada a uma sessão TCP.
ms.assetid: 777e0106-0314-4ec8-b064-88ceb694614b
title: Remetentes e receptores de PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e300a0c9de199e1f836e71407caf6487812cf7b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501678"
---
# <a name="pgm-senders-and-receivers"></a>Remetentes e receptores de PGM

O estabelecimento de uma sessão PGM é semelhante à rotina de estabelecimento da conexão associada a uma sessão TCP. No entanto, o desvio significativo de uma sessão TCP é que a semântica do cliente e do servidor são revertidas; o servidor (o remetente do PGM) se conecta a um grupo de multicast, enquanto o cliente (o receptor de PGM) aguarda para aceitar uma conexão. Os parágrafos a seguir detalham as etapas programáticas necessárias para criar um emissor PGM e um receptor PGM. Esta página também descreve os modos de dados disponíveis para sessões PGM.

## <a name="pgm-sender"></a>Remetente PGM

**Para criar um remetente PGM, execute as seguintes etapas**

1.  Crie um soquete PGM.
2.  [**associe**](/windows/desktop/api/winsock/nf-winsock-bind) o soquete a qualquer inaddr \_ .
3.  [**Conecte-se**](/windows/desktop/api/Winsock2/nf-winsock2-connect) ao endereço de transmissão do grupo multicast.

Nenhum handshake de sessão formal é executado com clientes. O processo de conexão é semelhante a um UDP [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), pois ele associa um endereço de ponto de extremidade (o grupo de multicast) ao soquete. Depois de concluído, os dados podem ser enviados no soquete.

Quando um remetente cria um soquete PGM e o conecta a um endereço de multicast, uma sessão do PGM é criada. Uma sessão de multicast confiável é definida por uma combinação do GUID (identificador global exclusivo) e da porta de origem. O GUID é gerado pelo transporte. A porta sSource é especificada pelo transporte e nenhum controle é fornecido sobre qual porta de origem é usada.

> [!Note]  
> O recebimento de dados em um soquete de remetente não é permitido e resulta em um erro.

 

O trecho de código a seguir ilustra a configuração de um remetente PGM:


```C++

SOCKET        s;
SOCKADDR_IN   salocal, sasession;
int           dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

salocal.sin_family = AF_INET;
salocal.sin_port   = htons (0);    // Port is ignored here
salocal.sin_addr.s_addr = htonl (INADDR_ANY);

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant sender socket options here
//

//
// Now, connect <entity type="hellip"/>
// Setting the connection port (dwSessionPort) has relevance, and
// can be used to multiplex multiple sessions to the same
// multicast group address over different ports
//
dwSessionPort = 0;
sasession.sin_family = AF_INET;
sasession.sin_port   = htons (dwSessionPort);
sasession.sin_addr.s_addr = inet_addr ("234.5.6.7");

connect (s, (SOCKADDR *)&sasession, sizeof(sasession));

//
// We're now ready to send data!
//



```



## <a name="pgm-receiver"></a>Receptor de PGM

**Para criar um receptor PGM, execute as seguintes etapas**

1.  Crie um soquete PGM.
2.  [**associe**](/windows/desktop/api/winsock/nf-winsock-bind) o soquete ao endereço do grupo de multicast no qual o remetente está transmitindo.
3.  Chame a função [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) no soquete para colocar o soquete no modo de escuta. A função Listen retorna quando uma sessão PGM é detectada no endereço e na porta do grupo de multicast especificado.
4.  Chame a função [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) para obter um novo identificador de soquete correspondente à sessão.

Somente os dados PGM originais (ODATA) disparam a aceitação de uma nova sessão. Assim, outro tráfego de PGM (como os pacotes SPM ou RDATA) pode ser recebido pelo transporte, mas não resulta na função [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) retornando.

Depois que uma sessão é aceita, o identificador de soquete retornado é usado para receber dados.

> [!Note]  
> O envio de dados em um soquete de recebimento não é permitido e resulta em um erro.

 

O trecho de código a seguir ilustra a configuração de um receptor PGM:


```C++

SOCKET        s,
              sclient;
SOCKADDR_IN   salocal,
              sasession;
int           sasessionsz, dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

//
// The bind port (dwSessionPort) specified should match that
// which the sender specified in the connect call
//
dwSessionPort = 0;
salocal.sin_family = AF_INET;
salocal.sin_port   = htons (dwSessionPort);    
salocal.sin_addr.s_addr = inet_addr ("234.5.6.7");

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant receiver socket options here
//

listen (s, 10);

sasessionsz = sizeof(sasession);
sclient = accept (s, (SOCKADDR *)&sasession, &sasessionsz);

//
// accept will return the client socket and we are now ready
// to receive data on the new socket!
//



```



## <a name="data-modes"></a>Modos de dados

As sessões PGM têm duas opções para modos de dados: modo de mensagem e modo de fluxo.

O modo de mensagem é apropriado para aplicativos que precisam enviar mensagens discretas e é especificado por um tipo de soquete de SOCK \_ RDM. O modo de fluxo é apropriado para aplicativos que precisam enviar dados de streaming para receptores, como aplicativos de voz ou vídeo, e é especificado por um tipo de soquete de \_ fluxo Sock. A escolha do modo afeta a forma como o Winsock processa os dados.

Considere o seguinte exemplo: um remetente PGM de modo de mensagem faz três chamadas para a função [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) , cada uma com um buffer de 100 bytes. Essa operação aparece na conexão como três pacotes PGM discretos. No lado do destinatário, cada chamada para a função [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) retorna apenas 100 bytes, mesmo se um buffer de recebimento maior for fornecido. Por outro lado, com um retransmissor de modo de fluxo de PGM, essas transmissões de 3 100 bytes podem ser Unidas em menos de três pacotes físicos na conexão (ou Unidos em um blob de dados no lado do destinatário). Assim, quando o receptor chama uma das funções Receive do Windows Sockets, qualquer quantidade de dados recebidos pelo transporte de PGM pode ser retornada ao aplicativo sem considerar como os dados foram transmitidos fisicamente ou recebidos.

 

 



