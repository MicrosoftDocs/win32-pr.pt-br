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
# <a name="pgm-senders-and-receivers"></a><span data-ttu-id="e18fb-103">Remetentes e receptores de PGM</span><span class="sxs-lookup"><span data-stu-id="e18fb-103">PGM Senders and Receivers</span></span>

<span data-ttu-id="e18fb-104">O estabelecimento de uma sessão PGM é semelhante à rotina de estabelecimento da conexão associada a uma sessão TCP.</span><span class="sxs-lookup"><span data-stu-id="e18fb-104">Establishing a PGM session is similar to the connection establishment routine associated with a TCP session.</span></span> <span data-ttu-id="e18fb-105">No entanto, o desvio significativo de uma sessão TCP é que a semântica do cliente e do servidor são revertidas; o servidor (o remetente do PGM) se conecta a um grupo de multicast, enquanto o cliente (o receptor de PGM) aguarda para aceitar uma conexão.</span><span class="sxs-lookup"><span data-stu-id="e18fb-105">The significant departure from a TCP session, however, is that the client and server semantics are reversed; the server (the PGM sender) connects to a multicast group, while the client (the PGM receiver) waits to accept a connection.</span></span> <span data-ttu-id="e18fb-106">Os parágrafos a seguir detalham as etapas programáticas necessárias para criar um emissor PGM e um receptor PGM.</span><span class="sxs-lookup"><span data-stu-id="e18fb-106">The following paragraphs detail programmatic steps necessary for creating a PGM sender and a PGM receiver.</span></span> <span data-ttu-id="e18fb-107">Esta página também descreve os modos de dados disponíveis para sessões PGM.</span><span class="sxs-lookup"><span data-stu-id="e18fb-107">This page also describes the available data modes for PGM sessions.</span></span>

## <a name="pgm-sender"></a><span data-ttu-id="e18fb-108">Remetente PGM</span><span class="sxs-lookup"><span data-stu-id="e18fb-108">PGM Sender</span></span>

<span data-ttu-id="e18fb-109">**Para criar um remetente PGM, execute as seguintes etapas**</span><span class="sxs-lookup"><span data-stu-id="e18fb-109">**To create a PGM sender, perform the following steps**</span></span>

1.  <span data-ttu-id="e18fb-110">Crie um soquete PGM.</span><span class="sxs-lookup"><span data-stu-id="e18fb-110">Create a PGM socket.</span></span>
2.  <span data-ttu-id="e18fb-111">[**associe**](/windows/desktop/api/winsock/nf-winsock-bind) o soquete a qualquer inaddr \_ .</span><span class="sxs-lookup"><span data-stu-id="e18fb-111">[**bind**](/windows/desktop/api/winsock/nf-winsock-bind) the socket to INADDR\_ANY.</span></span>
3.  <span data-ttu-id="e18fb-112">[**Conecte-se**](/windows/desktop/api/Winsock2/nf-winsock2-connect) ao endereço de transmissão do grupo multicast.</span><span class="sxs-lookup"><span data-stu-id="e18fb-112">[**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) to the multicast group transmission address.</span></span>

<span data-ttu-id="e18fb-113">Nenhum handshake de sessão formal é executado com clientes.</span><span class="sxs-lookup"><span data-stu-id="e18fb-113">No formal session handshaking is performed with any clients.</span></span> <span data-ttu-id="e18fb-114">O processo de conexão é semelhante a um UDP [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), pois ele associa um endereço de ponto de extremidade (o grupo de multicast) ao soquete.</span><span class="sxs-lookup"><span data-stu-id="e18fb-114">The connection process is similar to a UDP [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), in that it associates an endpoint address (the multicast group) with the socket.</span></span> <span data-ttu-id="e18fb-115">Depois de concluído, os dados podem ser enviados no soquete.</span><span class="sxs-lookup"><span data-stu-id="e18fb-115">Once completed, data may be sent on the socket.</span></span>

<span data-ttu-id="e18fb-116">Quando um remetente cria um soquete PGM e o conecta a um endereço de multicast, uma sessão do PGM é criada.</span><span class="sxs-lookup"><span data-stu-id="e18fb-116">When a sender creates a PGM socket and connects it to a multicast address, a PGM session is created.</span></span> <span data-ttu-id="e18fb-117">Uma sessão de multicast confiável é definida por uma combinação do GUID (identificador global exclusivo) e da porta de origem.</span><span class="sxs-lookup"><span data-stu-id="e18fb-117">A reliable multicast session is defined by a combination of the globally unique identifier (GUID) and the source port.</span></span> <span data-ttu-id="e18fb-118">O GUID é gerado pelo transporte.</span><span class="sxs-lookup"><span data-stu-id="e18fb-118">The GUID is generated by the transport.</span></span> <span data-ttu-id="e18fb-119">A porta sSource é especificada pelo transporte e nenhum controle é fornecido sobre qual porta de origem é usada.</span><span class="sxs-lookup"><span data-stu-id="e18fb-119">The sSource port is specified by the transport, and no control is provided over which source port is used.</span></span>

> [!Note]  
> <span data-ttu-id="e18fb-120">O recebimento de dados em um soquete de remetente não é permitido e resulta em um erro.</span><span class="sxs-lookup"><span data-stu-id="e18fb-120">Receiving data on a sender socket is not allowed, and results in an error.</span></span>

 

<span data-ttu-id="e18fb-121">O trecho de código a seguir ilustra a configuração de um remetente PGM:</span><span class="sxs-lookup"><span data-stu-id="e18fb-121">The following code snippet illustrates setting up a PGM sender:</span></span>


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



## <a name="pgm-receiver"></a><span data-ttu-id="e18fb-122">Receptor de PGM</span><span class="sxs-lookup"><span data-stu-id="e18fb-122">PGM Receiver</span></span>

<span data-ttu-id="e18fb-123">**Para criar um receptor PGM, execute as seguintes etapas**</span><span class="sxs-lookup"><span data-stu-id="e18fb-123">**To create a PGM receiver, perform the following steps**</span></span>

1.  <span data-ttu-id="e18fb-124">Crie um soquete PGM.</span><span class="sxs-lookup"><span data-stu-id="e18fb-124">Create a PGM socket.</span></span>
2.  <span data-ttu-id="e18fb-125">[**associe**](/windows/desktop/api/winsock/nf-winsock-bind) o soquete ao endereço do grupo de multicast no qual o remetente está transmitindo.</span><span class="sxs-lookup"><span data-stu-id="e18fb-125">[**bind**](/windows/desktop/api/winsock/nf-winsock-bind) the socket to the multicast group address on which the sender is transmitting.</span></span>
3.  <span data-ttu-id="e18fb-126">Chame a função [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) no soquete para colocar o soquete no modo de escuta.</span><span class="sxs-lookup"><span data-stu-id="e18fb-126">Call the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function on the socket to put the socket in listening mode.</span></span> <span data-ttu-id="e18fb-127">A função Listen retorna quando uma sessão PGM é detectada no endereço e na porta do grupo de multicast especificado.</span><span class="sxs-lookup"><span data-stu-id="e18fb-127">The listen function returns when a PGM session is detected on the specified multicast group address and port.</span></span>
4.  <span data-ttu-id="e18fb-128">Chame a função [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) para obter um novo identificador de soquete correspondente à sessão.</span><span class="sxs-lookup"><span data-stu-id="e18fb-128">Call the [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) function to obtain a new socket handle corresponding to the session.</span></span>

<span data-ttu-id="e18fb-129">Somente os dados PGM originais (ODATA) disparam a aceitação de uma nova sessão.</span><span class="sxs-lookup"><span data-stu-id="e18fb-129">Only original PGM data (ODATA) triggers the acceptance of a new session.</span></span> <span data-ttu-id="e18fb-130">Assim, outro tráfego de PGM (como os pacotes SPM ou RDATA) pode ser recebido pelo transporte, mas não resulta na função [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) retornando.</span><span class="sxs-lookup"><span data-stu-id="e18fb-130">As such, other PGM traffic (such as SPM or RDATA packets) may be received by the transport, but do not result in the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function returning.</span></span>

<span data-ttu-id="e18fb-131">Depois que uma sessão é aceita, o identificador de soquete retornado é usado para receber dados.</span><span class="sxs-lookup"><span data-stu-id="e18fb-131">Once a session is accepted, the returned socket handle is used for receiving data.</span></span>

> [!Note]  
> <span data-ttu-id="e18fb-132">O envio de dados em um soquete de recebimento não é permitido e resulta em um erro.</span><span class="sxs-lookup"><span data-stu-id="e18fb-132">Sending data on a receive socket is not allowed, and results in an error.</span></span>

 

<span data-ttu-id="e18fb-133">O trecho de código a seguir ilustra a configuração de um receptor PGM:</span><span class="sxs-lookup"><span data-stu-id="e18fb-133">The following code snippet illustrates setting up a PGM receiver:</span></span>


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



## <a name="data-modes"></a><span data-ttu-id="e18fb-134">Modos de dados</span><span class="sxs-lookup"><span data-stu-id="e18fb-134">Data Modes</span></span>

<span data-ttu-id="e18fb-135">As sessões PGM têm duas opções para modos de dados: modo de mensagem e modo de fluxo.</span><span class="sxs-lookup"><span data-stu-id="e18fb-135">PGM sessions have two options for data modes: message mode and stream mode.</span></span>

<span data-ttu-id="e18fb-136">O modo de mensagem é apropriado para aplicativos que precisam enviar mensagens discretas e é especificado por um tipo de soquete de SOCK \_ RDM.</span><span class="sxs-lookup"><span data-stu-id="e18fb-136">Message mode is appropriate for applications that need to send discrete messages, and is specified by a socket type of SOCK\_RDM.</span></span> <span data-ttu-id="e18fb-137">O modo de fluxo é apropriado para aplicativos que precisam enviar dados de streaming para receptores, como aplicativos de voz ou vídeo, e é especificado por um tipo de soquete de \_ fluxo Sock.</span><span class="sxs-lookup"><span data-stu-id="e18fb-137">Stream mode is appropriate for applications that need to send streaming data to receivers, such as video or voice applications, and is specified by a socket type of SOCK\_STREAM.</span></span> <span data-ttu-id="e18fb-138">A escolha do modo afeta a forma como o Winsock processa os dados.</span><span class="sxs-lookup"><span data-stu-id="e18fb-138">The choice of mode effects how Winsock processes data.</span></span>

<span data-ttu-id="e18fb-139">Considere o seguinte exemplo: um remetente PGM de modo de mensagem faz três chamadas para a função [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) , cada uma com um buffer de 100 bytes.</span><span class="sxs-lookup"><span data-stu-id="e18fb-139">Consider the following example: A message mode PGM sender makes three calls to the [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) function, each with a 100-byte buffer.</span></span> <span data-ttu-id="e18fb-140">Essa operação aparece na conexão como três pacotes PGM discretos.</span><span class="sxs-lookup"><span data-stu-id="e18fb-140">This operation appears on the wire as three discrete PGM packets.</span></span> <span data-ttu-id="e18fb-141">No lado do destinatário, cada chamada para a função [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) retorna apenas 100 bytes, mesmo se um buffer de recebimento maior for fornecido.</span><span class="sxs-lookup"><span data-stu-id="e18fb-141">On the receiver side, each call to the [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) function returns only 100 bytes, even if a larger receive buffer is provided.</span></span> <span data-ttu-id="e18fb-142">Por outro lado, com um retransmissor de modo de fluxo de PGM, essas transmissões de 3 100 bytes podem ser Unidas em menos de três pacotes físicos na conexão (ou Unidos em um blob de dados no lado do destinatário).</span><span class="sxs-lookup"><span data-stu-id="e18fb-142">In contrast, with a stream mode PGM sender those three 100 byte transmissions could be coalesced into less than three physical packets on the wire (or coalesced into one blob of data on the receiver side).</span></span> <span data-ttu-id="e18fb-143">Assim, quando o receptor chama uma das funções Receive do Windows Sockets, qualquer quantidade de dados recebidos pelo transporte de PGM pode ser retornada ao aplicativo sem considerar como os dados foram transmitidos fisicamente ou recebidos.</span><span class="sxs-lookup"><span data-stu-id="e18fb-143">As such, when the receiver calls one of the Windows Sockets receive functions, any amount of data that has been received by the PGM transport may be returned to the application without regard to how the data was physically transmitted or received.</span></span>

 

 



