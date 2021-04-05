---
title: Terminologia de ligação de RPC essencial
description: Para obter melhor ajuda em uma discussão sobre o processo de conexão do cliente/servidor, é útil conhecer os termos a seguir.
ms.assetid: 05aca325-87ee-4581-9152-a8a2ff7fb490
keywords:
- Chamada de procedimento remoto RPC, descrita, associação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b18b8d3872c830d90079ad740505fead14c1b3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007998"
---
# <a name="essential-rpc-binding-terminology"></a><span data-ttu-id="be71c-104">Terminologia de ligação de RPC essencial</span><span class="sxs-lookup"><span data-stu-id="be71c-104">Essential RPC Binding Terminology</span></span>

<span data-ttu-id="be71c-105">Para obter melhor ajuda em uma discussão sobre o processo de conexão do cliente/servidor, é útil conhecer os termos a seguir.</span><span class="sxs-lookup"><span data-stu-id="be71c-105">To better aid in a discussion of the client/server connection process, it is helpful to know the following terms.</span></span>

## <a name="parameters"></a><span data-ttu-id="be71c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be71c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be71c-107"><span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>Sequência de protocolos</span><span class="sxs-lookup"><span data-stu-id="be71c-107"><span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>Protocol Sequence</span></span>
</dt> <dd>

<span data-ttu-id="be71c-108">Quando os sistemas operacionais de rede se comunicam entre si, eles devem escutar e falar da mesma linguagem.</span><span class="sxs-lookup"><span data-stu-id="be71c-108">When network operating systems communicate with each other, they must listen and speak the same language.</span></span> <span data-ttu-id="be71c-109">Esses idiomas são chamados de *sequências de protocolo*.</span><span class="sxs-lookup"><span data-stu-id="be71c-109">These languages are called *protocol sequences*.</span></span> <span data-ttu-id="be71c-110">Os programas cliente e servidor devem usar sequências de protocolo às quais a rede que os conectam oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="be71c-110">Client and server programs must use protocol sequences that the network connecting them supports.</span></span> <span data-ttu-id="be71c-111">O Microsoft RPC dá suporte a uma variedade de sequências de protocolo.</span><span class="sxs-lookup"><span data-stu-id="be71c-111">Microsoft RPC supports a variety of protocol sequences.</span></span> <span data-ttu-id="be71c-112">Para obter detalhes, consulte [selecionando uma sequência de protocolo](selecting-a-protocol-sequence.md), [especificando sequências de protocolo](specifying-protocol-sequences.md)e ponto de [**extremidade**](/windows/desktop/Midl/endpoint).</span><span class="sxs-lookup"><span data-stu-id="be71c-112">For details, see [Selecting a Protocol Sequence](selecting-a-protocol-sequence.md), [Specifying Protocol Sequences](specifying-protocol-sequences.md), and [**endpoint**](/windows/desktop/Midl/endpoint).</span></span>

</dd> <dt>

<span data-ttu-id="be71c-113"><span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>Computador host do servidor ou sistema host do servidor</span><span class="sxs-lookup"><span data-stu-id="be71c-113"><span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>Server Host Computer or Server Host System</span></span>
</dt> <dd>

<span data-ttu-id="be71c-114">O programa do servidor é executado no computador host do servidor.</span><span class="sxs-lookup"><span data-stu-id="be71c-114">The server program runs on the server host computer.</span></span> <span data-ttu-id="be71c-115">No entanto, muitos literatura sobre a computação cliente/servidor refere-se ao programa do servidor e ao computador host do servidor como o "servidor".</span><span class="sxs-lookup"><span data-stu-id="be71c-115">However, much literature on client/server computing refers to both the server program and the server host computer as the "server."</span></span> <span data-ttu-id="be71c-116">O resultado é que nem sempre é claro que está sendo discutido.</span><span class="sxs-lookup"><span data-stu-id="be71c-116">The result is that it is not always clear which is being discussed.</span></span>

</dd> <dt>

<span data-ttu-id="be71c-117"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Extremidade</span><span class="sxs-lookup"><span data-stu-id="be71c-117"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span>
</dt> <dd>

<span data-ttu-id="be71c-118">Os programas de servidor escutam uma porta ou um grupo de portas no computador host do servidor para solicitações de cliente.</span><span class="sxs-lookup"><span data-stu-id="be71c-118">Server programs listen to a port or a group of ports on the server host computer for client requests.</span></span> <span data-ttu-id="be71c-119">Os sistemas de host de servidor mantêm um banco de dados dessas portas, que são chamadas de pontos de extremidade no RPC.</span><span class="sxs-lookup"><span data-stu-id="be71c-119">Server host systems maintain a database of these ports, which are called endpoints in RPC.</span></span> <span data-ttu-id="be71c-120">O banco de dados é chamado de mapa de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="be71c-120">The database is called the endpoint map.</span></span>

</dd> <dt>

<span data-ttu-id="be71c-121"><span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>Vinculação</span><span class="sxs-lookup"><span data-stu-id="be71c-121"><span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>Binding</span></span>
</dt> <dd>

<span data-ttu-id="be71c-122">Os programas cliente criam uma associação ao servidor para estabelecer uma sessão de comunicação.</span><span class="sxs-lookup"><span data-stu-id="be71c-122">Client programs create a binding to the server to establish a communication session.</span></span> <span data-ttu-id="be71c-123">Uma associação contém todas as informações de que os aplicativos cliente precisam para criar a sessão.</span><span class="sxs-lookup"><span data-stu-id="be71c-123">A binding contains all of the information the client applications needs to create the session.</span></span>

</dd> </dl>

 

 