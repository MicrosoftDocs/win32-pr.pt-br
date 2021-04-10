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
# <a name="winsock-network-event-tracing-details"></a><span data-ttu-id="5ed06-103">Detalhes de rastreamento de eventos de rede do Winsock</span><span class="sxs-lookup"><span data-stu-id="5ed06-103">Winsock Network Event Tracing Details</span></span>

<span data-ttu-id="5ed06-104">Os detalhes a seguir cada um dos eventos de rede Winsock que podem ser rastreados e descreve quais parâmetros e informações são registrados.</span><span class="sxs-lookup"><span data-stu-id="5ed06-104">The following details each of the Winsock network events that can be traced and describes which parameters and information are logged.</span></span>

## <a name="socket-creation"></a><span data-ttu-id="5ed06-105">Criação de soquete</span><span class="sxs-lookup"><span data-stu-id="5ed06-105">Socket Creation</span></span>

<span data-ttu-id="5ed06-106">ID do evento = 1</span><span class="sxs-lookup"><span data-stu-id="5ed06-106">Event ID = 1</span></span>

<span data-ttu-id="5ed06-107">Nível = 4 (informações)</span><span class="sxs-lookup"><span data-stu-id="5ed06-107">Level = 4 (Information)</span></span>

<span data-ttu-id="5ed06-108">Os seguintes eventos do Winsock são rastreados para a criação de soquete:</span><span class="sxs-lookup"><span data-stu-id="5ed06-108">The following Winsock events are traced for socket creation:</span></span>

-   <span data-ttu-id="5ed06-109">Identificadores de soquete criados por chamadas para as funções [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) ou [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) .</span><span class="sxs-lookup"><span data-stu-id="5ed06-109">Socket handles created by calls to the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) or [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) functions.</span></span>
-   <span data-ttu-id="5ed06-110">Identificadores de soquete aceitos em soquetes de escuta.</span><span class="sxs-lookup"><span data-stu-id="5ed06-110">Accepted socket handles on listening sockets.</span></span>
-   <span data-ttu-id="5ed06-111">Identificadores de soquete criados por chamadas para a função [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) .</span><span class="sxs-lookup"><span data-stu-id="5ed06-111">Socket handles created by calls to the [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) function.</span></span>
-   <span data-ttu-id="5ed06-112">Identificadores de soquete reutilizados por chamadas para as funções [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) ou [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) .</span><span class="sxs-lookup"><span data-stu-id="5ed06-112">Socket handles re-used by calls to the [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) or [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) functions.</span></span>

<span data-ttu-id="5ed06-113">Os seguintes parâmetros são registrados em log para um evento de criação de soquete:</span><span class="sxs-lookup"><span data-stu-id="5ed06-113">The following parameters are logged for a socket creation event:</span></span>



| <span data-ttu-id="5ed06-114">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-114">Parameter</span></span>                                                                                                        | <span data-ttu-id="5ed06-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-115">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-116"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-116"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                 | <span data-ttu-id="5ed06-117">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-117">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-118"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-118"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>             | <span data-ttu-id="5ed06-119">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-119">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-120"><span id="SocketType"></span><span id="sockettype"></span><span id="SOCKETTYPE"></span>SocketType</span><span class="sxs-lookup"><span data-stu-id="5ed06-120"><span id="SocketType"></span><span id="sockettype"></span><span id="SOCKETTYPE"></span>SocketType</span></span><br/>     | <span data-ttu-id="5ed06-121">O tipo do soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-121">The type of the socket.</span></span><br/>                                                     |
| <span data-ttu-id="5ed06-122"><span id="Protocol"></span><span id="protocol"></span><span id="PROTOCOL"></span>Protocolo</span><span class="sxs-lookup"><span data-stu-id="5ed06-122"><span id="Protocol"></span><span id="protocol"></span><span id="PROTOCOL"></span>Protocol</span></span><br/>             | <span data-ttu-id="5ed06-123">O protocolo do soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-123">The protocol of the socket.</span></span><br/>                                                 |
| <span data-ttu-id="5ed06-124"><span id="UserModePid"></span><span id="usermodepid"></span><span id="USERMODEPID"></span>UserModePid</span><span class="sxs-lookup"><span data-stu-id="5ed06-124"><span id="UserModePid"></span><span id="usermodepid"></span><span id="USERMODEPID"></span>UserModePid</span></span><br/> | <span data-ttu-id="5ed06-125">A ID do processo do modo de usuário que criou o soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-125">The user-mode process ID that created the socket.</span></span><br/>                           |



 

## <a name="socket-bind"></a><span data-ttu-id="5ed06-126">Associação de soquete</span><span class="sxs-lookup"><span data-stu-id="5ed06-126">Socket Bind</span></span>

<span data-ttu-id="5ed06-127">ID do evento = 2 (IPv4), ID do evento = 3 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="5ed06-127">Event ID = 2 (IPv4), Event ID = 3 (IPv6)</span></span>

<span data-ttu-id="5ed06-128">Nível = 4 (informações)</span><span class="sxs-lookup"><span data-stu-id="5ed06-128">Level = 4 (Information)</span></span>

<span data-ttu-id="5ed06-129">Os seguintes eventos do Winsock são rastreados para uma operação de associação:</span><span class="sxs-lookup"><span data-stu-id="5ed06-129">The following Winsock events are traced for a bind operation:</span></span>

-   <span data-ttu-id="5ed06-130">Associação implícita ou explícita de um identificador de soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-130">Implicit or explicit binding of a socket handle.</span></span>

<span data-ttu-id="5ed06-131">Os seguintes parâmetros são registrados em log para um evento de ligação:</span><span class="sxs-lookup"><span data-stu-id="5ed06-131">The following parameters are logged for a bind event:</span></span>



| <span data-ttu-id="5ed06-132">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-132">Parameter</span></span>                                                                                            | <span data-ttu-id="5ed06-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-133">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-134"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-134"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ed06-135">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-135">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-136"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-136"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ed06-137">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-137">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-138"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Corrigir</span><span class="sxs-lookup"><span data-stu-id="5ed06-138"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="5ed06-139">O endereço IP local.</span><span class="sxs-lookup"><span data-stu-id="5ed06-139">The local IP address.</span></span><br/>                                                       |
| <span data-ttu-id="5ed06-140"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto</span><span class="sxs-lookup"><span data-stu-id="5ed06-140"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="5ed06-141">O número da porta IP local.</span><span class="sxs-lookup"><span data-stu-id="5ed06-141">The local IP port number.</span></span><br/>                                                   |
| <span data-ttu-id="5ed06-142"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Estado</span><span class="sxs-lookup"><span data-stu-id="5ed06-142"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Status</span></span><br/>         | <span data-ttu-id="5ed06-143">O status ou o código de erro retornado para a operação de associação.</span><span class="sxs-lookup"><span data-stu-id="5ed06-143">The status or error code returned for the bind operation.</span></span><br/>                   |



 

## <a name="failed-bind"></a><span data-ttu-id="5ed06-144">Falha na ligação</span><span class="sxs-lookup"><span data-stu-id="5ed06-144">Failed Bind</span></span>

<span data-ttu-id="5ed06-145">ID do evento = 40</span><span class="sxs-lookup"><span data-stu-id="5ed06-145">Event ID = 40</span></span>

<span data-ttu-id="5ed06-146">Nível = 4 (informações)</span><span class="sxs-lookup"><span data-stu-id="5ed06-146">Level = 4 (Information)</span></span>

<span data-ttu-id="5ed06-147">Os seguintes eventos do Winsock são rastreados para uma operação de ligação com falha:</span><span class="sxs-lookup"><span data-stu-id="5ed06-147">The following Winsock events are traced for a failed bind operation:</span></span>

-   <span data-ttu-id="5ed06-148">Associação implícita ou explícita de um identificador de soquete que falha.</span><span class="sxs-lookup"><span data-stu-id="5ed06-148">Implicit or explicit binding of a socket handle that fails.</span></span>

<span data-ttu-id="5ed06-149">Os seguintes parâmetros são registrados em log para um evento de ligação com falha:</span><span class="sxs-lookup"><span data-stu-id="5ed06-149">The following parameters are logged for a failed bind event:</span></span>



| <span data-ttu-id="5ed06-150">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-150">Parameter</span></span>                                                                                            | <span data-ttu-id="5ed06-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-151">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-152"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-152"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ed06-153">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-153">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-154"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-154"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ed06-155">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-155">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-156"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao</span><span class="sxs-lookup"><span data-stu-id="5ed06-156"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="5ed06-157">O código de erro retornado para a operação de ligação com falha.</span><span class="sxs-lookup"><span data-stu-id="5ed06-157">The error code returned for the failing bind operation.</span></span><br/>                     |



 

## <a name="socket-connect"></a><span data-ttu-id="5ed06-158">Conexão de soquete</span><span class="sxs-lookup"><span data-stu-id="5ed06-158">Socket Connect</span></span>

<span data-ttu-id="5ed06-159">ID do evento = 4 (IPv4), ID do evento = 5 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="5ed06-159">Event ID = 4 (IPv4), Event ID = 5 (IPv6)</span></span>

<span data-ttu-id="5ed06-160">Nível = 4 (informações)</span><span class="sxs-lookup"><span data-stu-id="5ed06-160">Level = 4 (Information)</span></span>

<span data-ttu-id="5ed06-161">Os seguintes eventos do Winsock são rastreados para uma solicitação de operação de conexão (uma chamada para a função [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)ou [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) ):</span><span class="sxs-lookup"><span data-stu-id="5ed06-161">The following Winsock events are traced for a connect operation request (a call to the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function):</span></span>

-   <span data-ttu-id="5ed06-162">Conectar um soquete a um destino para um soquete orientado a conexão ou sem conexão.</span><span class="sxs-lookup"><span data-stu-id="5ed06-162">Connecting a socket to a destination for either a connection-oriented or a connectionless socket.</span></span>

<span data-ttu-id="5ed06-163">Os seguintes parâmetros são registrados em log para um evento Connect:</span><span class="sxs-lookup"><span data-stu-id="5ed06-163">The following parameters are logged for a connect event:</span></span>



| <span data-ttu-id="5ed06-164">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-164">Parameter</span></span>                                                                                            | <span data-ttu-id="5ed06-165">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-165">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-166"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-166"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ed06-167">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-167">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-168"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-168"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ed06-169">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-169">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-170"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Corrigir</span><span class="sxs-lookup"><span data-stu-id="5ed06-170"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="5ed06-171">O endereço IP remoto.</span><span class="sxs-lookup"><span data-stu-id="5ed06-171">The remote IP address.</span></span><br/>                                                      |
| <span data-ttu-id="5ed06-172"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto</span><span class="sxs-lookup"><span data-stu-id="5ed06-172"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="5ed06-173">O número da porta IP remota.</span><span class="sxs-lookup"><span data-stu-id="5ed06-173">The remote IP port number.</span></span><br/>                                                  |



 

## <a name="connect-completed"></a><span data-ttu-id="5ed06-174">Conexão concluída</span><span class="sxs-lookup"><span data-stu-id="5ed06-174">Connect Completed</span></span>

<span data-ttu-id="5ed06-175">ID do evento = 6</span><span class="sxs-lookup"><span data-stu-id="5ed06-175">Event ID = 6</span></span>

<span data-ttu-id="5ed06-176">Nível = 4 (informações)</span><span class="sxs-lookup"><span data-stu-id="5ed06-176">Level = 4 (Information)</span></span>

<span data-ttu-id="5ed06-177">Os seguintes eventos do Winsock são rastreados para uma conexão concluída:</span><span class="sxs-lookup"><span data-stu-id="5ed06-177">The following Winsock events are traced for a connect completed:</span></span>

-   <span data-ttu-id="5ed06-178">A operação de conexão foi concluída.</span><span class="sxs-lookup"><span data-stu-id="5ed06-178">The connect operation is completed.</span></span>

<span data-ttu-id="5ed06-179">Os seguintes parâmetros são registrados em log para um evento Connect Completed:</span><span class="sxs-lookup"><span data-stu-id="5ed06-179">The following parameters are logged for a connect completed event:</span></span>



| <span data-ttu-id="5ed06-180">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-180">Parameter</span></span>                                                                                            | <span data-ttu-id="5ed06-181">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-181">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-182"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-182"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ed06-183">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-183">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-184"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-184"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ed06-185">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-185">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-186"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao</span><span class="sxs-lookup"><span data-stu-id="5ed06-186"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="5ed06-187">O código de erro retornado para a operação de conexão.</span><span class="sxs-lookup"><span data-stu-id="5ed06-187">The error code returned for the connect operation.</span></span><br/>                          |



 

## <a name="afd-initiated-abort"></a><span data-ttu-id="5ed06-188">Anular AFD-Initiated</span><span class="sxs-lookup"><span data-stu-id="5ed06-188">AFD-Initiated Abort</span></span>

<span data-ttu-id="5ed06-189">ID do evento = 7</span><span class="sxs-lookup"><span data-stu-id="5ed06-189">Event ID = 7</span></span>

<span data-ttu-id="5ed06-190">Nível = 4 (informações)</span><span class="sxs-lookup"><span data-stu-id="5ed06-190">Level = 4 (Information)</span></span>

<span data-ttu-id="5ed06-191">Os seguintes eventos do Winsock são rastreados para anulações iniciadas pelo Winsock ou operações de cancelamento:</span><span class="sxs-lookup"><span data-stu-id="5ed06-191">The following Winsock events are traced for Winsock-initiated aborts or cancel operations:</span></span>

-   <span data-ttu-id="5ed06-192">Uma anulação devido a dados de recebimento não lidos armazenados em buffer após o fechamento.</span><span class="sxs-lookup"><span data-stu-id="5ed06-192">An abort due to unread receive data buffered after close.</span></span>
-   <span data-ttu-id="5ed06-193">Uma anulação após uma chamada para a função de [**desligamento**](/windows/desktop/api/winsock/nf-winsock-shutdown) com o parâmetro de *como* definido como SD \_ Receive e uma chamada para a função [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) com dados de recebimento pendentes.</span><span class="sxs-lookup"><span data-stu-id="5ed06-193">An abort after a call to the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function with the *how* parameter set to SD\_RECEIVE and a call to the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function with receive data pending.</span></span>
-   <span data-ttu-id="5ed06-194">Uma anulação após uma tentativa com falha de liberar o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="5ed06-194">An abort after a failed attempt to flush the endpoint.</span></span>
-   <span data-ttu-id="5ed06-195">Uma anulação após um erro interno do Winsock ocorreu.</span><span class="sxs-lookup"><span data-stu-id="5ed06-195">An abort after an internal Winsock error occurred.</span></span>
-   <span data-ttu-id="5ed06-196">Uma anulação devido a uma conexão com erros e o aplicativo solicitou anteriormente que a conexão fosse anulada em determinadas circunstâncias.</span><span class="sxs-lookup"><span data-stu-id="5ed06-196">An abort due to a connection with errors and the application previously requested that the connection be aborted on certain circumstances.</span></span> <span data-ttu-id="5ed06-197">Um exemplo desse caso seria um aplicativo que foi definido como \_ remanescente com um tempo limite de zero e ainda há dados não confirmados na conexão.</span><span class="sxs-lookup"><span data-stu-id="5ed06-197">One example of this case would be an application that set SO\_LINGER with a timeout of zero and there is still unacknowledged data on the connection.</span></span>
-   <span data-ttu-id="5ed06-198">Uma anulação em uma conexão não está totalmente associada à aceitação do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="5ed06-198">An abort on a connection not fully associated with accepting endpoint.</span></span>
-   <span data-ttu-id="5ed06-199">Uma anulação em uma chamada com falha para a função [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) ou [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) .</span><span class="sxs-lookup"><span data-stu-id="5ed06-199">An abort on a failed call to the [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) or [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) function.</span></span>
-   <span data-ttu-id="5ed06-200">Uma anulação devido a uma falha na operação de recebimento.</span><span class="sxs-lookup"><span data-stu-id="5ed06-200">An abort due to a failed receive operation.</span></span>
-   <span data-ttu-id="5ed06-201">Uma anulação devido a um evento de Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="5ed06-201">An abort due to a Plug and Play event.</span></span>
-   <span data-ttu-id="5ed06-202">Uma anulação devido a uma solicitação de liberação com falha.</span><span class="sxs-lookup"><span data-stu-id="5ed06-202">An abort due to a failed flush request.</span></span>
-   <span data-ttu-id="5ed06-203">Uma anulação devido a uma solicitação de recebimento de dados emitida com falha.</span><span class="sxs-lookup"><span data-stu-id="5ed06-203">An abort due to a failed expedited data receive request.</span></span>
-   <span data-ttu-id="5ed06-204">Uma anulação devido a uma solicitação de envio com falha.</span><span class="sxs-lookup"><span data-stu-id="5ed06-204">An abort due to a failed send request.</span></span>
-   <span data-ttu-id="5ed06-205">Uma anulação devido à solicitação de envio cancelada.</span><span class="sxs-lookup"><span data-stu-id="5ed06-205">An abort due to canceled send request.</span></span>
-   <span data-ttu-id="5ed06-206">Uma anulação devido a um cancelamento chamado para a função [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) .</span><span class="sxs-lookup"><span data-stu-id="5ed06-206">An abort due to a canceled called to the [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) function.</span></span>

<span data-ttu-id="5ed06-207">Os parâmetros a seguir são registrados para uma operação de anulação ou cancelamento iniciada pelo Winsock:</span><span class="sxs-lookup"><span data-stu-id="5ed06-207">The following parameters are logged for a Winsock-initiated abort or cancel operation:</span></span>



| <span data-ttu-id="5ed06-208">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-208">Parameter</span></span>                                                                                            | <span data-ttu-id="5ed06-209">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-209">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-210"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-210"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ed06-211">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-211">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-212"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-212"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ed06-213">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-213">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-214"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Falha</span><span class="sxs-lookup"><span data-stu-id="5ed06-214"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>         | <span data-ttu-id="5ed06-215">O motivo para a operação anular ou cancelar.</span><span class="sxs-lookup"><span data-stu-id="5ed06-215">The reason for the abort or cancel operation.</span></span><br/>                               |



 

## <a name="transport-initiated-abort"></a><span data-ttu-id="5ed06-216">Anular Transport-Initiated</span><span class="sxs-lookup"><span data-stu-id="5ed06-216">Transport-Initiated Abort</span></span>

<span data-ttu-id="5ed06-217">ID do evento = 8</span><span class="sxs-lookup"><span data-stu-id="5ed06-217">Event ID = 8</span></span>

<span data-ttu-id="5ed06-218">Nível = 4 (informações)</span><span class="sxs-lookup"><span data-stu-id="5ed06-218">Level = 4 (Information)</span></span>

<span data-ttu-id="5ed06-219">Os seguintes eventos do Winsock são rastreados para operações de anular ou cancelar iniciadas pelo transporte:</span><span class="sxs-lookup"><span data-stu-id="5ed06-219">The following Winsock events are traced for transport-initiated abort or cancel operations:</span></span>

-   <span data-ttu-id="5ed06-220">Redefinição indicada pelo transporte.</span><span class="sxs-lookup"><span data-stu-id="5ed06-220">Reset indicated by the transport.</span></span>

<span data-ttu-id="5ed06-221">Os parâmetros a seguir são registrados para uma operação de anulação ou cancelamento iniciada pelo Winsock:</span><span class="sxs-lookup"><span data-stu-id="5ed06-221">The following parameters are logged for a Winsock-initiated abort or cancel operation:</span></span>



| <span data-ttu-id="5ed06-222">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-222">Parameter</span></span>                                                                                            | <span data-ttu-id="5ed06-223">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-223">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-224"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-224"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ed06-225">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-225">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-226"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-226"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ed06-227">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-227">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-228"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Falha</span><span class="sxs-lookup"><span data-stu-id="5ed06-228"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>         | <span data-ttu-id="5ed06-229">O motivo para a operação anular ou cancelar.</span><span class="sxs-lookup"><span data-stu-id="5ed06-229">The reason for the abort or cancel operation.</span></span><br/>                               |



 

## <a name="failed-send-request"></a><span data-ttu-id="5ed06-230">Solicitação de envio com falha</span><span class="sxs-lookup"><span data-stu-id="5ed06-230">Failed Send Request</span></span>

<span data-ttu-id="5ed06-231">ID do evento = 9</span><span class="sxs-lookup"><span data-stu-id="5ed06-231">Event ID = 9</span></span>

<span data-ttu-id="5ed06-232">Nível = 4 (informações)</span><span class="sxs-lookup"><span data-stu-id="5ed06-232">Level = 4 (Information)</span></span>

<span data-ttu-id="5ed06-233">Os seguintes eventos do Winsock são rastreados para erros em solicitações de [**envio**](/windows/desktop/api/Winsock2/nf-winsock2-send) ou [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) :</span><span class="sxs-lookup"><span data-stu-id="5ed06-233">The following Winsock events are traced for errors on [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) or [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) requests:</span></span>

-   <span data-ttu-id="5ed06-234">Erros retornados em solicitações de [**envio**](/windows/desktop/api/Winsock2/nf-winsock2-send) ou [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) com falha.</span><span class="sxs-lookup"><span data-stu-id="5ed06-234">Errors returned on failed [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) or [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) requests.</span></span>

<span data-ttu-id="5ed06-235">Os parâmetros a seguir são registrados em log para solicitações de envio que resultam em um erro:</span><span class="sxs-lookup"><span data-stu-id="5ed06-235">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="5ed06-236">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-236">Parameter</span></span>                                                                                            | <span data-ttu-id="5ed06-237">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-237">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-238"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-238"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ed06-239">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-239">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-240"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-240"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ed06-241">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-241">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-242"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao</span><span class="sxs-lookup"><span data-stu-id="5ed06-242"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="5ed06-243">O código de erro retornado para a operação.</span><span class="sxs-lookup"><span data-stu-id="5ed06-243">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-wsasendmsg-request"></a><span data-ttu-id="5ed06-244">Falha na solicitação de WsaSendMsg</span><span class="sxs-lookup"><span data-stu-id="5ed06-244">Failed WsaSendMsg Request</span></span>

<span data-ttu-id="5ed06-245">ID do evento = 10</span><span class="sxs-lookup"><span data-stu-id="5ed06-245">Event ID = 10</span></span>

<span data-ttu-id="5ed06-246">Nível = 4 (informações)</span><span class="sxs-lookup"><span data-stu-id="5ed06-246">Level = 4 (Information)</span></span>

<span data-ttu-id="5ed06-247">Os seguintes eventos do Winsock são rastreados para erros em solicitações [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) :</span><span class="sxs-lookup"><span data-stu-id="5ed06-247">The following Winsock events are traced for errors on [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) requests:</span></span>

-   <span data-ttu-id="5ed06-248">Erros retornados em solicitações [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) com falha.</span><span class="sxs-lookup"><span data-stu-id="5ed06-248">Errors returned on failed [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) requests.</span></span>

<span data-ttu-id="5ed06-249">Os parâmetros a seguir são registrados em log para solicitações de envio que resultam em um erro:</span><span class="sxs-lookup"><span data-stu-id="5ed06-249">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="5ed06-250">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-250">Parameter</span></span>                                                                                            | <span data-ttu-id="5ed06-251">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-251">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-252"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-252"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ed06-253">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-253">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-254"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-254"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ed06-255">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-255">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-256"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao</span><span class="sxs-lookup"><span data-stu-id="5ed06-256"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="5ed06-257">O código de erro retornado para a operação.</span><span class="sxs-lookup"><span data-stu-id="5ed06-257">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-recv-request"></a><span data-ttu-id="5ed06-258">Solicitação de recv com falha</span><span class="sxs-lookup"><span data-stu-id="5ed06-258">Failed Recv Request</span></span>

<span data-ttu-id="5ed06-259">ID do evento = 11</span><span class="sxs-lookup"><span data-stu-id="5ed06-259">Event ID = 11</span></span>

<span data-ttu-id="5ed06-260">Nível = 4 (informações)</span><span class="sxs-lookup"><span data-stu-id="5ed06-260">Level = 4 (Information)</span></span>

<span data-ttu-id="5ed06-261">Os seguintes eventos do Winsock são rastreados para erros em solicitações de [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)ou [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) :</span><span class="sxs-lookup"><span data-stu-id="5ed06-261">The following Winsock events are traced for errors on [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), or [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) requests:</span></span>

-   <span data-ttu-id="5ed06-262">Erros retornados em solicitações de recebimento com falha.</span><span class="sxs-lookup"><span data-stu-id="5ed06-262">Errors returned on failed receive requests.</span></span>

<span data-ttu-id="5ed06-263">Os parâmetros a seguir são registrados em log para solicitações de envio que resultam em um erro:</span><span class="sxs-lookup"><span data-stu-id="5ed06-263">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="5ed06-264">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-264">Parameter</span></span>                                                                                            | <span data-ttu-id="5ed06-265">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-265">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-266"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-266"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ed06-267">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-267">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-268"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-268"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ed06-269">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-269">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao</span><span class="sxs-lookup"><span data-stu-id="5ed06-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="5ed06-271">O código de erro retornado para a operação.</span><span class="sxs-lookup"><span data-stu-id="5ed06-271">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-recvfrom-request"></a><span data-ttu-id="5ed06-272">Falha na solicitação de recvfrom</span><span class="sxs-lookup"><span data-stu-id="5ed06-272">Failed Recvfrom Request</span></span>

<span data-ttu-id="5ed06-273">ID do evento = 12</span><span class="sxs-lookup"><span data-stu-id="5ed06-273">Event ID = 12</span></span>

<span data-ttu-id="5ed06-274">Nível = 4 (informações)</span><span class="sxs-lookup"><span data-stu-id="5ed06-274">Level = 4 (Information)</span></span>

<span data-ttu-id="5ed06-275">Os seguintes eventos do Winsock são rastreados para erros em solicitações [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) ou [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) :</span><span class="sxs-lookup"><span data-stu-id="5ed06-275">The following Winsock events are traced for errors on [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) requests:</span></span>

-   <span data-ttu-id="5ed06-276">Erros retornados em solicitações [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) ou [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) com falha.</span><span class="sxs-lookup"><span data-stu-id="5ed06-276">Errors returned on failed [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) requests.</span></span>

<span data-ttu-id="5ed06-277">Os parâmetros a seguir são registrados para uma solicitação [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) ou [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) que resulta em um erro:</span><span class="sxs-lookup"><span data-stu-id="5ed06-277">The following parameters are logged for a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) request that results in an error:</span></span>



| <span data-ttu-id="5ed06-278">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-278">Parameter</span></span>                                                                                            | <span data-ttu-id="5ed06-279">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-279">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-280"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-280"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ed06-281">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-281">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-282"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-282"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ed06-283">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-283">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-284"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao</span><span class="sxs-lookup"><span data-stu-id="5ed06-284"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="5ed06-285">O código de erro retornado para a operação.</span><span class="sxs-lookup"><span data-stu-id="5ed06-285">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="socket-close"></a><span data-ttu-id="5ed06-286">Fechamento de soquete</span><span class="sxs-lookup"><span data-stu-id="5ed06-286">Socket Close</span></span>

<span data-ttu-id="5ed06-287">ID do evento = 13</span><span class="sxs-lookup"><span data-stu-id="5ed06-287">Event ID = 13</span></span>

<span data-ttu-id="5ed06-288">Nível = 4 (informações)</span><span class="sxs-lookup"><span data-stu-id="5ed06-288">Level = 4 (Information)</span></span>

<span data-ttu-id="5ed06-289">Os seguintes eventos do Winsock são rastreados para operações de fechamento de soquete:</span><span class="sxs-lookup"><span data-stu-id="5ed06-289">The following Winsock events are traced for socket close operations:</span></span>

-   <span data-ttu-id="5ed06-290">Um identificador de soquete está fechado.</span><span class="sxs-lookup"><span data-stu-id="5ed06-290">A socket handle is closed.</span></span>

<span data-ttu-id="5ed06-291">Os seguintes parâmetros são registrados em log para um evento de fechamento de soquete:</span><span class="sxs-lookup"><span data-stu-id="5ed06-291">The following parameters are logged for a socket close event:</span></span>



| <span data-ttu-id="5ed06-292">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-292">Parameter</span></span>                                                                                            | <span data-ttu-id="5ed06-293">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-293">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-294"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-294"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ed06-295">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-295">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-296"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-296"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ed06-297">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-297">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao</span><span class="sxs-lookup"><span data-stu-id="5ed06-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="5ed06-299">O valor de retorno para a operação de fechamento de soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-299">The return value for the socket close operation.</span></span><br/>                            |



 

## <a name="socket-cleanup"></a><span data-ttu-id="5ed06-300">Limpeza de soquete</span><span class="sxs-lookup"><span data-stu-id="5ed06-300">Socket Cleanup</span></span>

<span data-ttu-id="5ed06-301">ID do evento = 14</span><span class="sxs-lookup"><span data-stu-id="5ed06-301">Event ID = 14</span></span>

<span data-ttu-id="5ed06-302">Nível = 4 (informações)</span><span class="sxs-lookup"><span data-stu-id="5ed06-302">Level = 4 (Information)</span></span>

<span data-ttu-id="5ed06-303">Os seguintes eventos do Winsock são rastreados para operações de limpeza de soquete (desligamento):</span><span class="sxs-lookup"><span data-stu-id="5ed06-303">The following Winsock events are traced for socket cleanup (shutdown) operations:</span></span>

-   <span data-ttu-id="5ed06-304">A função de [**desligamento**](/windows/desktop/api/winsock/nf-winsock-shutdown) é chamada em um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-304">The [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function is called on a socket.</span></span>
-   <span data-ttu-id="5ed06-305">O transporte indica uma desconexão normal com falha.</span><span class="sxs-lookup"><span data-stu-id="5ed06-305">The transport indicates a failed graceful disconnect.</span></span>

<span data-ttu-id="5ed06-306">Os seguintes parâmetros são registrados em log para um evento de limpeza de soquete (desligamento) ou de fechamento de soquete:</span><span class="sxs-lookup"><span data-stu-id="5ed06-306">The following parameters are logged for a socket cleanup (shutdown) or socket close event:</span></span>



| <span data-ttu-id="5ed06-307">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-307">Parameter</span></span>                                                                                            | <span data-ttu-id="5ed06-308">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-308">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-309"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-309"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ed06-310">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-310">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-311"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-311"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ed06-312">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-312">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-313"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao</span><span class="sxs-lookup"><span data-stu-id="5ed06-313"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="5ed06-314">O valor de retorno para a operação de limpeza de soquete (desligamento).</span><span class="sxs-lookup"><span data-stu-id="5ed06-314">The return value for the socket cleanup (shutdown) operation.</span></span><br/>               |



 

## <a name="socket-accept"></a><span data-ttu-id="5ed06-315">Aceitação de soquete</span><span class="sxs-lookup"><span data-stu-id="5ed06-315">Socket Accept</span></span>

<span data-ttu-id="5ed06-316">ID do evento = 15 (IPv4), ID do evento = 16 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="5ed06-316">Event ID = 15 (IPv4), Event ID = 16 (IPv6)</span></span>

<span data-ttu-id="5ed06-317">Nível = 4 (informações)</span><span class="sxs-lookup"><span data-stu-id="5ed06-317">Level = 4 (Information)</span></span>

<span data-ttu-id="5ed06-318">Os seguintes eventos do Winsock são rastreados para uma solicitação de função [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) :</span><span class="sxs-lookup"><span data-stu-id="5ed06-318">The following Winsock events are traced for an [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function request:</span></span>

-   <span data-ttu-id="5ed06-319">Uma solicitação de função [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) em um identificador de soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-319">An [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function request on a socket handle.</span></span>

<span data-ttu-id="5ed06-320">Os seguintes parâmetros são registrados em log para um evento de aceitação:</span><span class="sxs-lookup"><span data-stu-id="5ed06-320">The following parameters are logged for an accept event:</span></span>



| <span data-ttu-id="5ed06-321">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-321">Parameter</span></span>                                                                                            | <span data-ttu-id="5ed06-322">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-322">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-323"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-323"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ed06-324">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-324">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-325"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-325"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ed06-326">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-326">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-327"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Corrigir</span><span class="sxs-lookup"><span data-stu-id="5ed06-327"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="5ed06-328">O endereço IP remoto.</span><span class="sxs-lookup"><span data-stu-id="5ed06-328">The remote IP address.</span></span><br/>                                                      |
| <span data-ttu-id="5ed06-329"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto</span><span class="sxs-lookup"><span data-stu-id="5ed06-329"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="5ed06-330">O número da porta IP remota.</span><span class="sxs-lookup"><span data-stu-id="5ed06-330">The remote IP port number.</span></span><br/>                                                  |
| <span data-ttu-id="5ed06-331"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Estado</span><span class="sxs-lookup"><span data-stu-id="5ed06-331"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Status</span></span><br/>         | <span data-ttu-id="5ed06-332">O status ou o código de erro retornado para a operação de aceitação.</span><span class="sxs-lookup"><span data-stu-id="5ed06-332">The status or error code returned for the accept operation.</span></span><br/>                 |



 

## <a name="accept-failed"></a><span data-ttu-id="5ed06-333">Falha ao aceitar</span><span class="sxs-lookup"><span data-stu-id="5ed06-333">Accept Failed</span></span>

<span data-ttu-id="5ed06-334">ID do evento = 17</span><span class="sxs-lookup"><span data-stu-id="5ed06-334">Event ID = 17</span></span>

<span data-ttu-id="5ed06-335">Nível = 4 (informações)</span><span class="sxs-lookup"><span data-stu-id="5ed06-335">Level = 4 (Information)</span></span>

<span data-ttu-id="5ed06-336">Os seguintes eventos do Winsock são rastreados para uma operação de aceitação com falha:</span><span class="sxs-lookup"><span data-stu-id="5ed06-336">The following Winsock events are traced for a failed accept operation:</span></span>

-   <span data-ttu-id="5ed06-337">Uma solicitação [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) em um identificador de soquete que falha.</span><span class="sxs-lookup"><span data-stu-id="5ed06-337">An [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) request on a socket handle that fails.</span></span>

<span data-ttu-id="5ed06-338">Os seguintes parâmetros são registrados em log para um evento de aceitação com falha:</span><span class="sxs-lookup"><span data-stu-id="5ed06-338">The following parameters are logged for a failed accept event:</span></span>



| <span data-ttu-id="5ed06-339">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-339">Parameter</span></span>                                                                                            | <span data-ttu-id="5ed06-340">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-340">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-341"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-341"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ed06-342">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-342">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-343"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-343"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ed06-344">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-344">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-345"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao</span><span class="sxs-lookup"><span data-stu-id="5ed06-345"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="5ed06-346">O código de erro retornado para a operação de aceitação com falha.</span><span class="sxs-lookup"><span data-stu-id="5ed06-346">The error code returned for the failing accept operation.</span></span><br/>                   |



 

## <a name="send-posted"></a><span data-ttu-id="5ed06-347">Enviar Postado</span><span class="sxs-lookup"><span data-stu-id="5ed06-347">Send Posted</span></span>

<span data-ttu-id="5ed06-348">ID do evento = 18</span><span class="sxs-lookup"><span data-stu-id="5ed06-348">Event ID = 18</span></span>

<span data-ttu-id="5ed06-349">Nível = 5 (detalhado)</span><span class="sxs-lookup"><span data-stu-id="5ed06-349">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ed06-350">Para diagnosticar a corrupção do buffer do usuário (por exemplo, quando um aplicativo reutiliza o mesmo buffer em outra chamada de envio ou recebimento enquanto ele ainda está em uso), o buffer de dados é registrado quando é Postado no Winsock e após a conclusão do transporte subjacente.</span><span class="sxs-lookup"><span data-stu-id="5ed06-350">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="5ed06-351">Os seguintes eventos do Winsock são rastreados para operações de envio de soquete e recepção de buffer de recebimento:</span><span class="sxs-lookup"><span data-stu-id="5ed06-351">The following Winsock events are traced for socket send and receive buffer post operations:</span></span>

-   <span data-ttu-id="5ed06-352">Um aplicativo publica um envio.</span><span class="sxs-lookup"><span data-stu-id="5ed06-352">An application posts a send.</span></span>
-   <span data-ttu-id="5ed06-353">Uma operação de envio é concluída para o Winsock.</span><span class="sxs-lookup"><span data-stu-id="5ed06-353">A send operation completes to Winsock.</span></span>

<span data-ttu-id="5ed06-354">Os parâmetros a seguir são registrados para operações de envio de soquete:</span><span class="sxs-lookup"><span data-stu-id="5ed06-354">The following parameters are logged for socket send operations:</span></span>



| <span data-ttu-id="5ed06-355">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-355">Parameter</span></span>                                                                                                            | <span data-ttu-id="5ed06-356">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-356">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-357"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-357"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="5ed06-358">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-358">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="5ed06-359"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-359"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="5ed06-360">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-360">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="5ed06-361"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="5ed06-361"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="5ed06-362">Um valor booliano que indica se a e/s de caminho rápido foi usada.</span><span class="sxs-lookup"><span data-stu-id="5ed06-362">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="5ed06-363"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="5ed06-363"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="5ed06-364">A contagem de buffers.</span><span class="sxs-lookup"><span data-stu-id="5ed06-364">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="5ed06-365"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Completo</span><span class="sxs-lookup"><span data-stu-id="5ed06-365"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="5ed06-366">O endereço virtual do buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-366">The virtual address of the buffer.</span></span> <span data-ttu-id="5ed06-367">Para buffers encadeados, esse parâmetro é o endereço virtual do primeiro buffer na cadeia.</span><span class="sxs-lookup"><span data-stu-id="5ed06-367">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="5ed06-368"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="5ed06-368"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="5ed06-369">A duração do buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-369">The length of the buffer.</span></span> <span data-ttu-id="5ed06-370">Para buffers encadeados, esse parâmetro é o número total de bytes em todos os buffers na cadeia.</span><span class="sxs-lookup"><span data-stu-id="5ed06-370">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="5ed06-371">Quando FastPath é true, o endereço de UserMode do primeiro buffer na matriz de buffers é registrado no parâmetro buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-371">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="5ed06-372">Quando FastPath é false, o endereço de buffer do kernel do Winsock é registrado no parâmetro buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-372">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="receive-posted"></a><span data-ttu-id="5ed06-373">Receber Postado</span><span class="sxs-lookup"><span data-stu-id="5ed06-373">Receive Posted</span></span>

<span data-ttu-id="5ed06-374">ID do evento = 19</span><span class="sxs-lookup"><span data-stu-id="5ed06-374">Event ID = 19</span></span>

<span data-ttu-id="5ed06-375">Nível = 5 (detalhado)</span><span class="sxs-lookup"><span data-stu-id="5ed06-375">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ed06-376">Para diagnosticar a corrupção do buffer do usuário (por exemplo, quando um aplicativo reutiliza o mesmo buffer em outra chamada de envio ou recebimento enquanto ele ainda está em uso), o buffer de dados é registrado quando é Postado no Winsock e após a conclusão do transporte subjacente.</span><span class="sxs-lookup"><span data-stu-id="5ed06-376">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="5ed06-377">Os seguintes eventos do Winsock são rastreados para operações de postagem do buffer de recebimento de soquete:</span><span class="sxs-lookup"><span data-stu-id="5ed06-377">The following Winsock events are traced for socket receive buffer post operations:</span></span>

-   <span data-ttu-id="5ed06-378">Um aplicativo posta um Receive.</span><span class="sxs-lookup"><span data-stu-id="5ed06-378">An application posts a receive.</span></span>
-   <span data-ttu-id="5ed06-379">Uma operação de recebimento é concluída para o Winsock.</span><span class="sxs-lookup"><span data-stu-id="5ed06-379">A receive operation completes to Winsock.</span></span>

<span data-ttu-id="5ed06-380">Os parâmetros a seguir são registrados para operações de recebimento de soquete:</span><span class="sxs-lookup"><span data-stu-id="5ed06-380">The following parameters are logged for socket receive operations:</span></span>



| <span data-ttu-id="5ed06-381">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-381">Parameter</span></span>                                                                                                            | <span data-ttu-id="5ed06-382">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-382">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-383"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-383"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="5ed06-384">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-384">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="5ed06-385"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-385"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="5ed06-386">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-386">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="5ed06-387"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="5ed06-387"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="5ed06-388">Um valor booliano que indica se a e/s de caminho rápido foi usada.</span><span class="sxs-lookup"><span data-stu-id="5ed06-388">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="5ed06-389"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="5ed06-389"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="5ed06-390">A contagem de buffers.</span><span class="sxs-lookup"><span data-stu-id="5ed06-390">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="5ed06-391"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Completo</span><span class="sxs-lookup"><span data-stu-id="5ed06-391"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="5ed06-392">O endereço virtual do buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-392">The virtual address of the buffer.</span></span> <span data-ttu-id="5ed06-393">Para buffers encadeados, esse parâmetro é o endereço virtual do primeiro buffer na cadeia.</span><span class="sxs-lookup"><span data-stu-id="5ed06-393">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="5ed06-394"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="5ed06-394"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="5ed06-395">A duração do buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-395">The length of the buffer.</span></span> <span data-ttu-id="5ed06-396">Para buffers encadeados, esse parâmetro é o número total de bytes em todos os buffers na cadeia.</span><span class="sxs-lookup"><span data-stu-id="5ed06-396">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="5ed06-397">Quando FastPath é true, o endereço de UserMode do primeiro buffer na matriz de buffers é registrado no parâmetro buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-397">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="5ed06-398">Quando FastPath é false, o endereço de buffer do kernel do Winsock é registrado no parâmetro buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-398">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="recvfrom-posted"></a><span data-ttu-id="5ed06-399">RecvFrom Postado</span><span class="sxs-lookup"><span data-stu-id="5ed06-399">RecvFrom Posted</span></span>

<span data-ttu-id="5ed06-400">ID do evento = 20</span><span class="sxs-lookup"><span data-stu-id="5ed06-400">Event ID = 20</span></span>

<span data-ttu-id="5ed06-401">Nível = 5 (detalhado)</span><span class="sxs-lookup"><span data-stu-id="5ed06-401">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ed06-402">Para diagnosticar a corrupção do buffer do usuário (por exemplo, quando um aplicativo reutiliza o mesmo buffer em outra chamada de envio ou recebimento enquanto ele ainda está em uso), o buffer de dados é registrado quando é Postado no Winsock e após a conclusão do transporte subjacente.</span><span class="sxs-lookup"><span data-stu-id="5ed06-402">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="5ed06-403">Os seguintes eventos do Winsock são rastreados para uma operação post do buffer [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) em um soquete:</span><span class="sxs-lookup"><span data-stu-id="5ed06-403">The following Winsock events are traced for a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) buffer post operation on a socket:</span></span>

-   <span data-ttu-id="5ed06-404">Um aplicativo posta uma operação de recebimento de.</span><span class="sxs-lookup"><span data-stu-id="5ed06-404">An application posts a receive from operation.</span></span>

<span data-ttu-id="5ed06-405">Os parâmetros a seguir são registrados para a operação recvfrom:</span><span class="sxs-lookup"><span data-stu-id="5ed06-405">The following parameters are logged for the recvfrom operation:</span></span>



| <span data-ttu-id="5ed06-406">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-406">Parameter</span></span>                                                                                                            | <span data-ttu-id="5ed06-407">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-407">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-408"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-408"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="5ed06-409">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-409">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="5ed06-410"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-410"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="5ed06-411">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-411">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="5ed06-412"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="5ed06-412"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="5ed06-413">Um valor booliano que indica se a e/s de caminho rápido foi usada.</span><span class="sxs-lookup"><span data-stu-id="5ed06-413">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="5ed06-414"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="5ed06-414"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="5ed06-415">A contagem de buffers.</span><span class="sxs-lookup"><span data-stu-id="5ed06-415">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="5ed06-416"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Completo</span><span class="sxs-lookup"><span data-stu-id="5ed06-416"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="5ed06-417">O endereço virtual do buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-417">The virtual address of the buffer.</span></span> <span data-ttu-id="5ed06-418">Para buffers encadeados, esse parâmetro é o endereço virtual do primeiro buffer na cadeia.</span><span class="sxs-lookup"><span data-stu-id="5ed06-418">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="5ed06-419"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="5ed06-419"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="5ed06-420">A duração do buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-420">The length of the buffer.</span></span> <span data-ttu-id="5ed06-421">Para buffers encadeados, esse parâmetro é o número total de bytes em todos os buffers na cadeia.</span><span class="sxs-lookup"><span data-stu-id="5ed06-421">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="5ed06-422">Quando FastPath é true, o endereço de UserMode do primeiro buffer na matriz de buffers é registrado no parâmetro buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-422">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="5ed06-423">Quando FastPath é false, o endereço de buffer do kernel do Winsock é registrado no parâmetro buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-423">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="sendto-posted"></a><span data-ttu-id="5ed06-424">SendTo Postado</span><span class="sxs-lookup"><span data-stu-id="5ed06-424">SendTo Posted</span></span>

<span data-ttu-id="5ed06-425">ID do evento = 21 (IPv4), ID do evento = 22 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="5ed06-425">Event ID = 21 (IPv4), Event ID = 22 (IPv6)</span></span>

<span data-ttu-id="5ed06-426">Nível = 5 (detalhado)</span><span class="sxs-lookup"><span data-stu-id="5ed06-426">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ed06-427">Para diagnosticar a corrupção do buffer do usuário (por exemplo, quando um aplicativo reutiliza o mesmo buffer em outra chamada de envio ou recebimento enquanto ele ainda está em uso), o buffer de dados é registrado quando é Postado no Winsock e após a conclusão do transporte subjacente.</span><span class="sxs-lookup"><span data-stu-id="5ed06-427">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="5ed06-428">Os seguintes eventos do Winsock são rastreados para uma operação post do buffer [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) em um soquete:</span><span class="sxs-lookup"><span data-stu-id="5ed06-428">The following Winsock events are traced for a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) buffer post operation on a socket:</span></span>

-   <span data-ttu-id="5ed06-429">Um aplicativo publica um envio de.</span><span class="sxs-lookup"><span data-stu-id="5ed06-429">An application posts a send from.</span></span>

<span data-ttu-id="5ed06-430">Os parâmetros a seguir são registrados para a operação [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) :</span><span class="sxs-lookup"><span data-stu-id="5ed06-430">The following parameters are logged for the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) operation:</span></span>



| <span data-ttu-id="5ed06-431">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-431">Parameter</span></span>                                                                                                            | <span data-ttu-id="5ed06-432">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-432">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-433"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-433"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="5ed06-434">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-434">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="5ed06-435"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-435"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="5ed06-436">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-436">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="5ed06-437"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="5ed06-437"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="5ed06-438">Um valor booliano que indica se a e/s de caminho rápido foi usada.</span><span class="sxs-lookup"><span data-stu-id="5ed06-438">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="5ed06-439"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="5ed06-439"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="5ed06-440">A contagem de buffers.</span><span class="sxs-lookup"><span data-stu-id="5ed06-440">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="5ed06-441"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Completo</span><span class="sxs-lookup"><span data-stu-id="5ed06-441"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="5ed06-442">O endereço virtual do buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-442">The virtual address of the buffer.</span></span> <span data-ttu-id="5ed06-443">Para buffers encadeados, esse parâmetro é o endereço virtual do primeiro buffer na cadeia.</span><span class="sxs-lookup"><span data-stu-id="5ed06-443">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="5ed06-444"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="5ed06-444"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="5ed06-445">A duração do buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-445">The length of the buffer.</span></span> <span data-ttu-id="5ed06-446">Para buffers encadeados, esse parâmetro é o número total de bytes em todos os buffers na cadeia.</span><span class="sxs-lookup"><span data-stu-id="5ed06-446">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |
| <span data-ttu-id="5ed06-447"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Corrigir</span><span class="sxs-lookup"><span data-stu-id="5ed06-447"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="5ed06-448">O endereço IP remoto do soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-448">The remote IP address of the socket.</span></span><br/>                                                                                            |
| <span data-ttu-id="5ed06-449"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto</span><span class="sxs-lookup"><span data-stu-id="5ed06-449"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="5ed06-450">O número da porta IP remota do soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-450">The remote IP port number of the socket.</span></span><br/>                                                                                        |



 

<span data-ttu-id="5ed06-451">Quando FastPath é true, o endereço de UserMode do primeiro buffer na matriz de buffers é registrado no parâmetro buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-451">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="5ed06-452">Quando FastPath é false, o endereço de buffer do kernel do Winsock é registrado no parâmetro buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-452">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="recv-completed"></a><span data-ttu-id="5ed06-453">Recv concluído</span><span class="sxs-lookup"><span data-stu-id="5ed06-453">Recv Completed</span></span>

<span data-ttu-id="5ed06-454">ID do evento = 23</span><span class="sxs-lookup"><span data-stu-id="5ed06-454">Event ID = 23</span></span>

<span data-ttu-id="5ed06-455">Nível = 5 (detalhado)</span><span class="sxs-lookup"><span data-stu-id="5ed06-455">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ed06-456">Para diagnosticar a corrupção do buffer do usuário (por exemplo, quando um aplicativo reutiliza o mesmo buffer em outra chamada de envio ou recebimento enquanto ele ainda está em uso), o buffer de dados é registrado quando é Postado no Winsock e após a conclusão do transporte subjacente.</span><span class="sxs-lookup"><span data-stu-id="5ed06-456">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="5ed06-457">Os seguintes eventos do Winsock são rastreados para operações de recebimento de soquete concluídas:</span><span class="sxs-lookup"><span data-stu-id="5ed06-457">The following Winsock events are traced for socket receive completed operations:</span></span>

-   <span data-ttu-id="5ed06-458">Uma operação de envio é concluída para o transporte.</span><span class="sxs-lookup"><span data-stu-id="5ed06-458">A send operation completes to the transport.</span></span>
-   <span data-ttu-id="5ed06-459">Uma operação de recebimento é concluída para o transporte.</span><span class="sxs-lookup"><span data-stu-id="5ed06-459">A receive operation completes to the transport.</span></span>

<span data-ttu-id="5ed06-460">Os seguintes parâmetros são registrados em log para um envio concluído ou recebimento concluído:</span><span class="sxs-lookup"><span data-stu-id="5ed06-460">The following parameters are logged for a send completed or receive completed:</span></span>



| <span data-ttu-id="5ed06-461">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-461">Parameter</span></span>                                                                                                            | <span data-ttu-id="5ed06-462">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-462">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-463"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-463"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="5ed06-464">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-464">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                                   |
| <span data-ttu-id="5ed06-465"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-465"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="5ed06-466">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-466">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                              |
| <span data-ttu-id="5ed06-467"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Completo</span><span class="sxs-lookup"><span data-stu-id="5ed06-467"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="5ed06-468">O endereço virtual do buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-468">The virtual address of the buffer.</span></span> <span data-ttu-id="5ed06-469">Para buffers encadeados, esse parâmetro é o endereço virtual do primeiro buffer na cadeia.</span><span class="sxs-lookup"><span data-stu-id="5ed06-469">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>          |
| <span data-ttu-id="5ed06-470"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="5ed06-470"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="5ed06-471">O comprimento do buffer de bytes recebidos.</span><span class="sxs-lookup"><span data-stu-id="5ed06-471">The length of the buffer of bytes received.</span></span> <span data-ttu-id="5ed06-472">Para buffers encadeados, esse parâmetro é o total de bytes recebidos em todos os buffers na cadeia.</span><span class="sxs-lookup"><span data-stu-id="5ed06-472">For chained buffers, this parameter is the total bytes received in all buffers in the chain.</span></span><br/> |



 

## <a name="send-completed"></a><span data-ttu-id="5ed06-473">Envio concluído</span><span class="sxs-lookup"><span data-stu-id="5ed06-473">Send Completed</span></span>

<span data-ttu-id="5ed06-474">ID do evento = 24</span><span class="sxs-lookup"><span data-stu-id="5ed06-474">Event ID = 24</span></span>

<span data-ttu-id="5ed06-475">Nível = 5 (detalhado)</span><span class="sxs-lookup"><span data-stu-id="5ed06-475">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ed06-476">Para diagnosticar a corrupção do buffer do usuário (por exemplo, quando um aplicativo reutiliza o mesmo buffer em outra chamada de envio ou recebimento enquanto ele ainda está em uso), o buffer de dados é registrado quando é Postado no Winsock e após a conclusão do transporte subjacente.</span><span class="sxs-lookup"><span data-stu-id="5ed06-476">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="5ed06-477">Os seguintes eventos do Winsock são rastreados para operações de envio de soquete concluídas:</span><span class="sxs-lookup"><span data-stu-id="5ed06-477">The following Winsock events are traced for socket send completed operations:</span></span>

-   <span data-ttu-id="5ed06-478">Uma operação de envio é concluída para o transporte.</span><span class="sxs-lookup"><span data-stu-id="5ed06-478">A send operation completes to the transport.</span></span>

<span data-ttu-id="5ed06-479">Os seguintes parâmetros são registrados em log para um envio concluído:</span><span class="sxs-lookup"><span data-stu-id="5ed06-479">The following parameters are logged for a send completed:</span></span>



| <span data-ttu-id="5ed06-480">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-480">Parameter</span></span>                                                                                                            | <span data-ttu-id="5ed06-481">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-481">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-482"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-482"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="5ed06-483">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-483">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="5ed06-484"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-484"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="5ed06-485">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-485">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="5ed06-486"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Completo</span><span class="sxs-lookup"><span data-stu-id="5ed06-486"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="5ed06-487">O endereço virtual do buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-487">The virtual address of the buffer.</span></span> <span data-ttu-id="5ed06-488">Para buffers encadeados, esse parâmetro é o endereço virtual do primeiro buffer na cadeia.</span><span class="sxs-lookup"><span data-stu-id="5ed06-488">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="5ed06-489"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="5ed06-489"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="5ed06-490">O comprimento do buffer de bytes enviados.</span><span class="sxs-lookup"><span data-stu-id="5ed06-490">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="5ed06-491">Para buffers encadeados, esse parâmetro é o total de bytes enviados de todos os buffers na cadeia.</span><span class="sxs-lookup"><span data-stu-id="5ed06-491">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |



 

## <a name="sendmsg-completed"></a><span data-ttu-id="5ed06-492">SendMsg concluído</span><span class="sxs-lookup"><span data-stu-id="5ed06-492">SendMsg Completed</span></span>

<span data-ttu-id="5ed06-493">ID do evento = 25</span><span class="sxs-lookup"><span data-stu-id="5ed06-493">Event ID = 25</span></span>

<span data-ttu-id="5ed06-494">Nível = 5 (detalhado)</span><span class="sxs-lookup"><span data-stu-id="5ed06-494">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ed06-495">Para diagnosticar a corrupção do buffer do usuário (por exemplo, quando um aplicativo reutiliza o mesmo buffer em outra chamada de envio ou recebimento enquanto ele ainda está em uso), o buffer de dados é registrado quando é Postado no Winsock e após a conclusão do transporte subjacente.</span><span class="sxs-lookup"><span data-stu-id="5ed06-495">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="5ed06-496">Os seguintes eventos do Winsock são rastreados quando uma operação post do buffer [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) é concluída em um soquete:</span><span class="sxs-lookup"><span data-stu-id="5ed06-496">The following Winsock events are traced when a [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="5ed06-497">Um aplicativo conclui uma operação [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .</span><span class="sxs-lookup"><span data-stu-id="5ed06-497">An application completes a [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) operation.</span></span>

<span data-ttu-id="5ed06-498">Os parâmetros a seguir são registrados para a conclusão do [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) :</span><span class="sxs-lookup"><span data-stu-id="5ed06-498">The following parameters are logged for the [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) completion:</span></span>



| <span data-ttu-id="5ed06-499">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-499">Parameter</span></span>                                                                                                            | <span data-ttu-id="5ed06-500">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-500">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-501"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-501"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="5ed06-502">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-502">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="5ed06-503"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-503"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="5ed06-504">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-504">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="5ed06-505"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="5ed06-505"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="5ed06-506">A contagem de buffers.</span><span class="sxs-lookup"><span data-stu-id="5ed06-506">The buffer count.</span></span><br/>                                                                                                                  |
| <span data-ttu-id="5ed06-507"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Completo</span><span class="sxs-lookup"><span data-stu-id="5ed06-507"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="5ed06-508">O endereço virtual do buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-508">The virtual address of the buffer.</span></span> <span data-ttu-id="5ed06-509">Para buffers encadeados, esse parâmetro é o endereço virtual do primeiro buffer na cadeia.</span><span class="sxs-lookup"><span data-stu-id="5ed06-509">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="5ed06-510"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="5ed06-510"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="5ed06-511">O comprimento do buffer de bytes enviados.</span><span class="sxs-lookup"><span data-stu-id="5ed06-511">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="5ed06-512">Para buffers encadeados, esse parâmetro é o total de bytes enviados de todos os buffers na cadeia.</span><span class="sxs-lookup"><span data-stu-id="5ed06-512">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="5ed06-513"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Corrigir</span><span class="sxs-lookup"><span data-stu-id="5ed06-513"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="5ed06-514">O endereço IP remoto do soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-514">The remote IP address of the socket.</span></span><br/>                                                                                               |
| <span data-ttu-id="5ed06-515"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto</span><span class="sxs-lookup"><span data-stu-id="5ed06-515"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="5ed06-516">O número da porta IP remota do soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-516">The remote IP port number of the socket.</span></span><br/>                                                                                           |



 

## <a name="recvfrom-completed"></a><span data-ttu-id="5ed06-517">RecvFrom concluído</span><span class="sxs-lookup"><span data-stu-id="5ed06-517">RecvFrom Completed</span></span>

<span data-ttu-id="5ed06-518">ID do evento = 26 (IPv4), ID do evento = 27 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="5ed06-518">Event ID = 26 (IPv4), Event ID = 27 (IPv6)</span></span>

<span data-ttu-id="5ed06-519">Nível = 5 (detalhado)</span><span class="sxs-lookup"><span data-stu-id="5ed06-519">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ed06-520">Para diagnosticar a corrupção do buffer do usuário (por exemplo, quando um aplicativo reutiliza o mesmo buffer em outra chamada de envio ou recebimento enquanto ele ainda está em uso), o buffer de dados é registrado quando é Postado no Winsock e após a conclusão do transporte subjacente.</span><span class="sxs-lookup"><span data-stu-id="5ed06-520">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="5ed06-521">Os seguintes eventos do Winsock são rastreados quando uma operação post do buffer [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) é concluída em um soquete:</span><span class="sxs-lookup"><span data-stu-id="5ed06-521">The following Winsock events are traced when a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="5ed06-522">Um aplicativo conclui uma operação [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) .</span><span class="sxs-lookup"><span data-stu-id="5ed06-522">An application completes a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) operation.</span></span>

<span data-ttu-id="5ed06-523">Os parâmetros a seguir são registrados para a conclusão do [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) :</span><span class="sxs-lookup"><span data-stu-id="5ed06-523">The following parameters are logged for the [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) completion:</span></span>



| <span data-ttu-id="5ed06-524">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-524">Parameter</span></span>                                                                                                            | <span data-ttu-id="5ed06-525">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-525">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-526"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-526"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="5ed06-527">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-527">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                                   |
| <span data-ttu-id="5ed06-528"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-528"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="5ed06-529">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-529">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                              |
| <span data-ttu-id="5ed06-530"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="5ed06-530"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="5ed06-531">A contagem de buffers.</span><span class="sxs-lookup"><span data-stu-id="5ed06-531">The buffer count.</span></span><br/>                                                                                                                        |
| <span data-ttu-id="5ed06-532"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Completo</span><span class="sxs-lookup"><span data-stu-id="5ed06-532"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="5ed06-533">O endereço virtual do buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-533">The virtual address of the buffer.</span></span> <span data-ttu-id="5ed06-534">Para buffers encadeados, esse parâmetro é o endereço virtual do primeiro buffer na cadeia.</span><span class="sxs-lookup"><span data-stu-id="5ed06-534">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>          |
| <span data-ttu-id="5ed06-535"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="5ed06-535"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="5ed06-536">O comprimento do buffer de bytes recebidos.</span><span class="sxs-lookup"><span data-stu-id="5ed06-536">The length of the buffer of bytes received.</span></span> <span data-ttu-id="5ed06-537">Para buffers encadeados, esse parâmetro é o total de bytes recebidos em todos os buffers na cadeia.</span><span class="sxs-lookup"><span data-stu-id="5ed06-537">For chained buffers, this parameter is the total bytes received in all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="5ed06-538"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Corrigir</span><span class="sxs-lookup"><span data-stu-id="5ed06-538"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="5ed06-539">O endereço IP remoto do soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-539">The remote IP address of the socket.</span></span><br/>                                                                                                     |
| <span data-ttu-id="5ed06-540"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto</span><span class="sxs-lookup"><span data-stu-id="5ed06-540"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="5ed06-541">O número da porta IP remota do soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-541">The remote IP port number of the socket.</span></span><br/>                                                                                                 |



 

## <a name="sendto-completed"></a><span data-ttu-id="5ed06-542">SendTo concluído</span><span class="sxs-lookup"><span data-stu-id="5ed06-542">SendTo Completed</span></span>

<span data-ttu-id="5ed06-543">ID do evento = 28</span><span class="sxs-lookup"><span data-stu-id="5ed06-543">Event ID = 28</span></span>

<span data-ttu-id="5ed06-544">Nível = 5 (detalhado)</span><span class="sxs-lookup"><span data-stu-id="5ed06-544">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ed06-545">Para diagnosticar a corrupção do buffer do usuário (por exemplo, quando um aplicativo reutiliza o mesmo buffer em outra chamada de envio ou recebimento enquanto ele ainda está em uso), o buffer de dados é registrado quando é Postado no Winsock e após a conclusão do transporte subjacente.</span><span class="sxs-lookup"><span data-stu-id="5ed06-545">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="5ed06-546">Os seguintes eventos do Winsock são rastreados quando uma operação post do buffer [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) é concluída em um soquete:</span><span class="sxs-lookup"><span data-stu-id="5ed06-546">The following Winsock events are traced when a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="5ed06-547">Um aplicativo conclui uma operação [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) .</span><span class="sxs-lookup"><span data-stu-id="5ed06-547">An application completes a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) operation.</span></span>

<span data-ttu-id="5ed06-548">Os parâmetros a seguir são registrados para a conclusão do [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) :</span><span class="sxs-lookup"><span data-stu-id="5ed06-548">The following parameters are logged for the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) completion:</span></span>



| <span data-ttu-id="5ed06-549">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-549">Parameter</span></span>                                                                                                            | <span data-ttu-id="5ed06-550">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-550">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-551"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-551"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="5ed06-552">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-552">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="5ed06-553"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-553"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="5ed06-554">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-554">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="5ed06-555"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="5ed06-555"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="5ed06-556">A contagem de buffers.</span><span class="sxs-lookup"><span data-stu-id="5ed06-556">The buffer count.</span></span><br/>                                                                                                                  |
| <span data-ttu-id="5ed06-557"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Completo</span><span class="sxs-lookup"><span data-stu-id="5ed06-557"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="5ed06-558">O endereço virtual do buffer.</span><span class="sxs-lookup"><span data-stu-id="5ed06-558">The virtual address of the buffer.</span></span> <span data-ttu-id="5ed06-559">Para buffers encadeados, esse parâmetro é o endereço virtual do primeiro buffer na cadeia.</span><span class="sxs-lookup"><span data-stu-id="5ed06-559">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="5ed06-560"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="5ed06-560"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="5ed06-561">O comprimento do buffer de bytes enviados.</span><span class="sxs-lookup"><span data-stu-id="5ed06-561">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="5ed06-562">Para buffers encadeados, esse parâmetro é o total de bytes enviados de todos os buffers na cadeia.</span><span class="sxs-lookup"><span data-stu-id="5ed06-562">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="5ed06-563"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Corrigir</span><span class="sxs-lookup"><span data-stu-id="5ed06-563"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="5ed06-564">O endereço IP remoto do soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-564">The remote IP address of the socket.</span></span><br/>                                                                                               |
| <span data-ttu-id="5ed06-565"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto</span><span class="sxs-lookup"><span data-stu-id="5ed06-565"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="5ed06-566">O número da porta IP remota do soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-566">The remote IP port number of the socket.</span></span><br/>                                                                                           |



 

## <a name="socket-option-set"></a><span data-ttu-id="5ed06-567">Conjunto de opções de soquete</span><span class="sxs-lookup"><span data-stu-id="5ed06-567">Socket Option Set</span></span>

<span data-ttu-id="5ed06-568">ID do evento = 29</span><span class="sxs-lookup"><span data-stu-id="5ed06-568">Event ID = 29</span></span>

<span data-ttu-id="5ed06-569">Nível = 5 (detalhado)</span><span class="sxs-lookup"><span data-stu-id="5ed06-569">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ed06-570">Sempre que um aplicativo altera determinados valores de opção de soquete e IOCTLs, os novos valores serão registrados em log.</span><span class="sxs-lookup"><span data-stu-id="5ed06-570">Whenever an application changes certain socket option values and Ioctls, the new values will be logged.</span></span> <span data-ttu-id="5ed06-571">As opções registradas podem ser usadas para diagnosticar mau desempenho ou comportamento estranho em aplicativos.</span><span class="sxs-lookup"><span data-stu-id="5ed06-571">The options logged can be used to diagnose poor performance or strange behavior in applications.</span></span> <span data-ttu-id="5ed06-572">Os seguintes eventos do Winsock são rastreados para determinadas opções de soquete e IOCTLs:</span><span class="sxs-lookup"><span data-stu-id="5ed06-572">The following Winsock events are traced for certain socket options and Ioctls:</span></span>

-   <span data-ttu-id="5ed06-573">Portanto, o \_ SNDBUF muda.</span><span class="sxs-lookup"><span data-stu-id="5ed06-573">SO\_SNDBUF changes.</span></span>
-   <span data-ttu-id="5ed06-574">Portanto, o \_ RCVBUF muda.</span><span class="sxs-lookup"><span data-stu-id="5ed06-574">SO\_RCVBUF changes.</span></span>
-   <span data-ttu-id="5ed06-575">FIONBIO</span><span class="sxs-lookup"><span data-stu-id="5ed06-575">FIONBIO</span></span>
-   <span data-ttu-id="5ed06-576">SIO \_ habilitar \_ \_ enfileiramento circular</span><span class="sxs-lookup"><span data-stu-id="5ed06-576">SIO\_ENABLE\_CIRCULAR\_QUEUEING</span></span>
-   <span data-ttu-id="5ed06-577">SIO \_ UDP \_ CONNRESET</span><span class="sxs-lookup"><span data-stu-id="5ed06-577">SIO\_UDP\_CONNRESET</span></span>
-   <span data-ttu-id="5ed06-578">\_OOBINLINE</span><span class="sxs-lookup"><span data-stu-id="5ed06-578">SO\_OOBINLINE</span></span>

<span data-ttu-id="5ed06-579">Os parâmetros a seguir são registrados para chamadas de função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) e [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) que alteram qualquer um dos valores acima:</span><span class="sxs-lookup"><span data-stu-id="5ed06-579">The following parameters are logged for [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) and [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function calls that change any of the above values:</span></span>



| <span data-ttu-id="5ed06-580">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-580">Parameter</span></span>                                                                                            | <span data-ttu-id="5ed06-581">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-581">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-582"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-582"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ed06-583">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-583">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-584"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-584"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ed06-585">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-585">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-586"><span id="Option"></span><span id="option"></span><span id="OPTION"></span>Option</span><span class="sxs-lookup"><span data-stu-id="5ed06-586"><span id="Option"></span><span id="option"></span><span id="OPTION"></span>Option</span></span><br/>         | <span data-ttu-id="5ed06-587">A opção de soquete ou o IOCTL que é alterado.</span><span class="sxs-lookup"><span data-stu-id="5ed06-587">The socket option or Ioctl that is changed.</span></span> <br/>                                |
| <span data-ttu-id="5ed06-588"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="5ed06-588"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span><br/>             | <span data-ttu-id="5ed06-589">O novo valor para a opção de soquete ou o IOCTL.</span><span class="sxs-lookup"><span data-stu-id="5ed06-589">The new value for the socket option or Ioctl.</span></span> <br/>                              |



 

## <a name="selectpoll-posted"></a><span data-ttu-id="5ed06-590">Selecionar/sondagem postada</span><span class="sxs-lookup"><span data-stu-id="5ed06-590">Select/Poll Posted</span></span>

<span data-ttu-id="5ed06-591">ID do evento = 30</span><span class="sxs-lookup"><span data-stu-id="5ed06-591">Event ID = 30</span></span>

<span data-ttu-id="5ed06-592">Nível = 5 (detalhado)</span><span class="sxs-lookup"><span data-stu-id="5ed06-592">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ed06-593">Os seguintes eventos do Winsock são rastreados quando um aplicativo chama a função [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :</span><span class="sxs-lookup"><span data-stu-id="5ed06-593">The following Winsock events are traced when an application calls the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function:</span></span>

-   <span data-ttu-id="5ed06-594">O aplicativo posta uma solicitação [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="5ed06-594">Application posts a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) request.</span></span>

<span data-ttu-id="5ed06-595">Os parâmetros a seguir são registrados para eventos [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :</span><span class="sxs-lookup"><span data-stu-id="5ed06-595">The following parameters are logged for [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) events:</span></span>



| <span data-ttu-id="5ed06-596">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-596">Parameter</span></span>                                                                                                        | <span data-ttu-id="5ed06-597">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-597">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-598"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-598"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                 | <span data-ttu-id="5ed06-599">A ID do processo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="5ed06-599">The owning process ID.</span></span><br/>                                                                              |
| <span data-ttu-id="5ed06-600"><span id="HandleCount"></span><span id="handlecount"></span><span id="HANDLECOUNT"></span>HandleCount</span><span class="sxs-lookup"><span data-stu-id="5ed06-600"><span id="HandleCount"></span><span id="handlecount"></span><span id="HANDLECOUNT"></span>HandleCount</span></span><br/> | <span data-ttu-id="5ed06-601">O número de identificadores passados pelo aplicativo (válido somente no evento de inicialização).</span><span class="sxs-lookup"><span data-stu-id="5ed06-601">The number of handles passed in by the application (only valid on the initiating event).</span></span><br/>            |
| <span data-ttu-id="5ed06-602"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>Cedido</span><span class="sxs-lookup"><span data-stu-id="5ed06-602"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>Timeout</span></span><br/>                 | <span data-ttu-id="5ed06-603">O tempo máximo para a função [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) aguardar.</span><span class="sxs-lookup"><span data-stu-id="5ed06-603">The maximum time for the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function to wait.</span></span><br/> |



 

## <a name="selectpoll-completed"></a><span data-ttu-id="5ed06-604">Seleção/sondagem concluída</span><span class="sxs-lookup"><span data-stu-id="5ed06-604">Select/Poll Completed</span></span>

<span data-ttu-id="5ed06-605">ID do evento = 31</span><span class="sxs-lookup"><span data-stu-id="5ed06-605">Event ID = 31</span></span>

<span data-ttu-id="5ed06-606">Nível = 5 (detalhado)</span><span class="sxs-lookup"><span data-stu-id="5ed06-606">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ed06-607">Os seguintes eventos do Winsock são rastreados quando um aplicativo chama a função [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) :</span><span class="sxs-lookup"><span data-stu-id="5ed06-607">The following Winsock events are traced when an application calls the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function:</span></span>

-   <span data-ttu-id="5ed06-608">O Winsock conclui uma chamada [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="5ed06-608">Winsock completes a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) call.</span></span>

<span data-ttu-id="5ed06-609">Os parâmetros a seguir são registrados quando uma operação [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) é concluída:</span><span class="sxs-lookup"><span data-stu-id="5ed06-609">The following parameters are logged when a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) operation completes:</span></span>



| <span data-ttu-id="5ed06-610">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-610">Parameter</span></span>                                                                                            | <span data-ttu-id="5ed06-611">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-611">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-612"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-612"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ed06-613">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-613">The kernel EPROCESS structure address for the process.</span></span><br/>                                              |
| <span data-ttu-id="5ed06-614"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-614"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ed06-615">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-615">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                         |
| <span data-ttu-id="5ed06-616"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao</span><span class="sxs-lookup"><span data-stu-id="5ed06-616"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="5ed06-617">O código de erro retornado para a operação [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="5ed06-617">The error code returned for the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) operation.</span></span><br/> |



 

## <a name="wsaeventselect"></a><span data-ttu-id="5ed06-618">WSAEventSelect</span><span class="sxs-lookup"><span data-stu-id="5ed06-618">WSAEventSelect</span></span>

<span data-ttu-id="5ed06-619">ID do evento = 32</span><span class="sxs-lookup"><span data-stu-id="5ed06-619">Event ID = 32</span></span>

<span data-ttu-id="5ed06-620">Nível = 5 (detalhado)</span><span class="sxs-lookup"><span data-stu-id="5ed06-620">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ed06-621">Os seguintes eventos do Winsock são rastreados quando um aplicativo chama a função [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) :</span><span class="sxs-lookup"><span data-stu-id="5ed06-621">The following Winsock events are traced when an application calls the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function:</span></span>

-   <span data-ttu-id="5ed06-622">Registre a máscara de evento passada na função [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) .</span><span class="sxs-lookup"><span data-stu-id="5ed06-622">Log the event mask passed in the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function.</span></span>

<span data-ttu-id="5ed06-623">Os parâmetros a seguir são registrados para chamadas de função [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) :</span><span class="sxs-lookup"><span data-stu-id="5ed06-623">The following parameters are logged for [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function calls:</span></span>



| <span data-ttu-id="5ed06-624">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-624">Parameter</span></span>                                                                                                | <span data-ttu-id="5ed06-625">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-625">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-626"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-626"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>         | <span data-ttu-id="5ed06-627">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-627">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-628"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-628"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>     | <span data-ttu-id="5ed06-629">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-629">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-630"><span id="EventMask"></span><span id="eventmask"></span><span id="EVENTMASK"></span>EventMask</span><span class="sxs-lookup"><span data-stu-id="5ed06-630"><span id="EventMask"></span><span id="eventmask"></span><span id="EVENTMASK"></span>EventMask</span></span><br/> | <span data-ttu-id="5ed06-631">O valor da máscara de evento.</span><span class="sxs-lookup"><span data-stu-id="5ed06-631">The value for the event mask.</span></span> <br/>                                              |



 

## <a name="dropped-datagram"></a><span data-ttu-id="5ed06-632">Datagram removido</span><span class="sxs-lookup"><span data-stu-id="5ed06-632">Dropped Datagram</span></span>

<span data-ttu-id="5ed06-633">ID do evento = 33 (IPv4), ID do evento = 34 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="5ed06-633">Event ID = 33 (IPv4), Event ID = 34 (IPv6)</span></span>

<span data-ttu-id="5ed06-634">Nível = 5 (detalhado)</span><span class="sxs-lookup"><span data-stu-id="5ed06-634">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ed06-635">Para ajudar a diagnosticar problemas em relação a aplicativos de datagrama, os seguintes eventos de Winsock são rastreados:</span><span class="sxs-lookup"><span data-stu-id="5ed06-635">To help diagnose issues around datagram applications, the following Winsock events are traced:</span></span>

-   <span data-ttu-id="5ed06-636">Quando um datagrama chega e é removido do espaço de buffer insuficiente.</span><span class="sxs-lookup"><span data-stu-id="5ed06-636">When a datagram arrives and it is dropped do to insufficient buffer space.</span></span>
-   <span data-ttu-id="5ed06-637">Em um datagrama conectado, se os dados chegarem de uma fonte diferente de destino conectado.</span><span class="sxs-lookup"><span data-stu-id="5ed06-637">On a connected datagram, if data arrives from a source other than connected destination.</span></span>

<span data-ttu-id="5ed06-638">Os seguintes parâmetros são registrados em log para datagramas removidos:</span><span class="sxs-lookup"><span data-stu-id="5ed06-638">The following parameters are logged for dropped datagrams:</span></span>



| <span data-ttu-id="5ed06-639">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-639">Parameter</span></span>                                                                                                    | <span data-ttu-id="5ed06-640">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-640">Description</span></span>                                                                            |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-641"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-641"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>             | <span data-ttu-id="5ed06-642">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-642">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-643"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-643"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>         | <span data-ttu-id="5ed06-644">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-644">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-645"><span id="PacketSize"></span><span id="packetsize"></span><span id="PACKETSIZE"></span>Tamanho</span><span class="sxs-lookup"><span data-stu-id="5ed06-645"><span id="PacketSize"></span><span id="packetsize"></span><span id="PACKETSIZE"></span>PacketSize</span></span><br/> | <span data-ttu-id="5ed06-646">O tamanho do pacote que foi Descartado.</span><span class="sxs-lookup"><span data-stu-id="5ed06-646">The size of the packet that was dropped.</span></span> <br/>                                   |
| <span data-ttu-id="5ed06-647"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Corrigir</span><span class="sxs-lookup"><span data-stu-id="5ed06-647"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>             | <span data-ttu-id="5ed06-648">O endereço IP da origem do pacote.</span><span class="sxs-lookup"><span data-stu-id="5ed06-648">The IP address of the source of the packet.</span></span> <br/>                                |
| <span data-ttu-id="5ed06-649"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto</span><span class="sxs-lookup"><span data-stu-id="5ed06-649"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                         | <span data-ttu-id="5ed06-650">O número da porta IP da origem do pacote.</span><span class="sxs-lookup"><span data-stu-id="5ed06-650">The IP port number of the source of the packet.</span></span><br/>                             |
| <span data-ttu-id="5ed06-651"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Falha</span><span class="sxs-lookup"><span data-stu-id="5ed06-651"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>                 | <span data-ttu-id="5ed06-652">O código de erro ou o motivo pelo qual o pacote foi Descartado.</span><span class="sxs-lookup"><span data-stu-id="5ed06-652">The error code or reason the packet was dropped.</span></span><br/>                            |



 

## <a name="connection-indicated"></a><span data-ttu-id="5ed06-653">Conexão indicada</span><span class="sxs-lookup"><span data-stu-id="5ed06-653">Connection Indicated</span></span>

<span data-ttu-id="5ed06-654">ID do evento = 35 (IPv4), ID do evento = 36 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="5ed06-654">Event ID = 35 (IPv4), Event ID = 36 (IPv6)</span></span>

<span data-ttu-id="5ed06-655">Nível = 5 (detalhado)</span><span class="sxs-lookup"><span data-stu-id="5ed06-655">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ed06-656">Os seguintes eventos do Winsock são rastreados para operações indicadas de conexão:</span><span class="sxs-lookup"><span data-stu-id="5ed06-656">The following Winsock events are traced for connection indicated operations:</span></span>

-   <span data-ttu-id="5ed06-657">Um aplicativo recebe uma solicitação de conexão.</span><span class="sxs-lookup"><span data-stu-id="5ed06-657">An application receives a connection request.</span></span>

<span data-ttu-id="5ed06-658">Os seguintes parâmetros são registrados em log para conexões indicadas de eventos de transporte:</span><span class="sxs-lookup"><span data-stu-id="5ed06-658">The following parameters are logged for connections indicated from transport events:</span></span>



| <span data-ttu-id="5ed06-659">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-659">Parameter</span></span>                                                                                            | <span data-ttu-id="5ed06-660">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-660">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-661"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-661"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ed06-662">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-662">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-663"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-663"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ed06-664">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-664">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-665"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Corrigir</span><span class="sxs-lookup"><span data-stu-id="5ed06-665"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="5ed06-666">O endereço IP remoto.</span><span class="sxs-lookup"><span data-stu-id="5ed06-666">The remote IP address.</span></span> <br/>                                                     |
| <span data-ttu-id="5ed06-667"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto</span><span class="sxs-lookup"><span data-stu-id="5ed06-667"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="5ed06-668">O número da porta IP remota.</span><span class="sxs-lookup"><span data-stu-id="5ed06-668">The remote IP port number.</span></span><br/>                                                  |



 

## <a name="data-indicated"></a><span data-ttu-id="5ed06-669">Dados indicados</span><span class="sxs-lookup"><span data-stu-id="5ed06-669">Data Indicated</span></span>

<span data-ttu-id="5ed06-670">ID do evento = 37</span><span class="sxs-lookup"><span data-stu-id="5ed06-670">Event ID = 37</span></span>

<span data-ttu-id="5ed06-671">Nível = 5 (detalhado)</span><span class="sxs-lookup"><span data-stu-id="5ed06-671">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ed06-672">Os seguintes eventos do Winsock são rastreados para operações indicadas de dados:</span><span class="sxs-lookup"><span data-stu-id="5ed06-672">The following Winsock events are traced for data indicated operations:</span></span>

-   <span data-ttu-id="5ed06-673">Um aplicativo recebe dados em um Soquete conectado.</span><span class="sxs-lookup"><span data-stu-id="5ed06-673">An application receives data on a connected socket.</span></span>

<span data-ttu-id="5ed06-674">Os seguintes parâmetros são registrados em log para dados indicados de eventos de transporte:</span><span class="sxs-lookup"><span data-stu-id="5ed06-674">The following parameters are logged for data indicated from transport events:</span></span>



| <span data-ttu-id="5ed06-675">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-675">Parameter</span></span>                                                                                                                        | <span data-ttu-id="5ed06-676">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-676">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-677"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-677"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                                 | <span data-ttu-id="5ed06-678">A ID do processo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="5ed06-678">The owning process ID.</span></span><br/>                                                      |
| <span data-ttu-id="5ed06-679"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-679"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                             | <span data-ttu-id="5ed06-680">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-680">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-681"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes indicados</span><span class="sxs-lookup"><span data-stu-id="5ed06-681"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes Indicated</span></span><br/> | <span data-ttu-id="5ed06-682">O número de bytes recebidos no soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-682">The number of bytes received on the socket.</span></span><br/>                                 |



 

## <a name="data-indicated-from-transport"></a><span data-ttu-id="5ed06-683">Dados indicados do transporte</span><span class="sxs-lookup"><span data-stu-id="5ed06-683">Data Indicated from Transport</span></span>

<span data-ttu-id="5ed06-684">ID do evento = 38 (IPv4), ID do evento = 39 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="5ed06-684">Event ID = 38 (IPv4), Event ID = 39 (IPv6)</span></span>

<span data-ttu-id="5ed06-685">Nível = 5 (detalhado)</span><span class="sxs-lookup"><span data-stu-id="5ed06-685">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ed06-686">Os seguintes eventos do Winsock são rastreados para dados indicados de operações de transporte:</span><span class="sxs-lookup"><span data-stu-id="5ed06-686">The following Winsock events are traced for data indicated from transport operations:</span></span>

-   <span data-ttu-id="5ed06-687">Um aplicativo posta uma solicitação de recebimento e recebe dados.</span><span class="sxs-lookup"><span data-stu-id="5ed06-687">An application posts a receive request and receives data.</span></span>

<span data-ttu-id="5ed06-688">Os seguintes parâmetros são registrados em log para dados indicados de eventos de transporte:</span><span class="sxs-lookup"><span data-stu-id="5ed06-688">The following parameters are logged for data indicated from transport events:</span></span>



| <span data-ttu-id="5ed06-689">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-689">Parameter</span></span>                                                                                                                        | <span data-ttu-id="5ed06-690">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-690">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-691"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-691"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                                 | <span data-ttu-id="5ed06-692">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-692">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-693"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-693"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                             | <span data-ttu-id="5ed06-694">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-694">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ed06-695"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Corrigir</span><span class="sxs-lookup"><span data-stu-id="5ed06-695"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                                 | <span data-ttu-id="5ed06-696">O endereço IP remoto.</span><span class="sxs-lookup"><span data-stu-id="5ed06-696">The remote IP address.</span></span> <br/>                                                     |
| <span data-ttu-id="5ed06-697"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porto</span><span class="sxs-lookup"><span data-stu-id="5ed06-697"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                             | <span data-ttu-id="5ed06-698">O número da porta IP remota.</span><span class="sxs-lookup"><span data-stu-id="5ed06-698">The remote IP port number.</span></span><br/>                                                  |
| <span data-ttu-id="5ed06-699"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes indicados</span><span class="sxs-lookup"><span data-stu-id="5ed06-699"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes Indicated</span></span><br/> | <span data-ttu-id="5ed06-700">O número de bytes recebidos no soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-700">The number of bytes received on the socket.</span></span><br/>                                 |



 

## <a name="disconnect-indicated-from-transport"></a><span data-ttu-id="5ed06-701">Desconexão indicada pelo transporte</span><span class="sxs-lookup"><span data-stu-id="5ed06-701">Disconnect Indicated from Transport</span></span>

<span data-ttu-id="5ed06-702">ID do evento = 41</span><span class="sxs-lookup"><span data-stu-id="5ed06-702">Event ID = 41</span></span>

<span data-ttu-id="5ed06-703">Nível = 5 (detalhado)</span><span class="sxs-lookup"><span data-stu-id="5ed06-703">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ed06-704">Os seguintes eventos do Winsock são rastreados para operações indicadas de desconexão:</span><span class="sxs-lookup"><span data-stu-id="5ed06-704">The following Winsock events are traced for disconnect indicated operations:</span></span>

-   <span data-ttu-id="5ed06-705">Um aplicativo recebe uma indicação de desconexão.</span><span class="sxs-lookup"><span data-stu-id="5ed06-705">An application receives a disconnect indication.</span></span>

<span data-ttu-id="5ed06-706">Os seguintes parâmetros são registrados para desconexão indicada de eventos de transporte:</span><span class="sxs-lookup"><span data-stu-id="5ed06-706">The following parameters are logged for disconnect indicated from transport events:</span></span>



| <span data-ttu-id="5ed06-707">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed06-707">Parameter</span></span>                                                                                            | <span data-ttu-id="5ed06-708">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed06-708">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed06-709"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span><span class="sxs-lookup"><span data-stu-id="5ed06-709"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ed06-710">O endereço da estrutura EPROCESS do kernel para o processo.</span><span class="sxs-lookup"><span data-stu-id="5ed06-710">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ed06-711"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="5ed06-711"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ed06-712">O endereço de soquete do kernel Winsock usado como um identificador exclusivo para um soquete.</span><span class="sxs-lookup"><span data-stu-id="5ed06-712">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="5ed06-713">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ed06-713">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ed06-714">Controle do rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="5ed06-714">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="5ed06-715">Rastreamento de Winsock</span><span class="sxs-lookup"><span data-stu-id="5ed06-715">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="5ed06-716">Detalhes de rastreamento de alteração do catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="5ed06-716">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="5ed06-717">Níveis de rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="5ed06-717">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> </dl>

 

 
