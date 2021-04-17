---
description: Outro aspecto do desenvolvimento de aplicativos a ser considerado é a diferença no comportamento entre operações locais ou intracomputer e o comportamento quando as operações ocorrem entre dois computadores em rede.
ms.assetid: e6f48446-948c-458c-8ecf-04ffb249c8a4
title: Comportamento do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a9b871a2c0535d9ef4220824651657332a224a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501709"
---
# <a name="application-behavior"></a><span data-ttu-id="80106-103">Comportamento do aplicativo</span><span class="sxs-lookup"><span data-stu-id="80106-103">Application Behavior</span></span>

<span data-ttu-id="80106-104">Outro aspecto do desenvolvimento de aplicativos a ser considerado é a diferença no comportamento entre operações locais ou intracomputer e o comportamento quando as operações ocorrem entre dois computadores em rede.</span><span class="sxs-lookup"><span data-stu-id="80106-104">Another aspect of application development to consider is the difference in behavior between local, or intracomputer operations, and behavior when operations take place between two networked computers.</span></span> <span data-ttu-id="80106-105">Há comportamentos de aplicativo que podem funcionar de forma aceitável em um computador local, mas quando executados em uma rede, causam degradação significativa de desempenho e consumo de recursos.</span><span class="sxs-lookup"><span data-stu-id="80106-105">There are application behaviors that may work acceptably well on a local computer, but when run across a network, cause significant performance degradation and resource consumption.</span></span> <span data-ttu-id="80106-106">Os comportamentos de aplicativo a seguir devem ser evitados durante o desenvolvimento de aplicativos do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="80106-106">The following application behaviors should be avoided when developing Windows Sockets applications.</span></span>

## <a name="behaviors-to-avoid"></a><span data-ttu-id="80106-107">Comportamentos a serem evitados</span><span class="sxs-lookup"><span data-stu-id="80106-107">Behaviors to Avoid</span></span>

-   <span data-ttu-id="80106-108">Aplicativos informais.</span><span class="sxs-lookup"><span data-stu-id="80106-108">Chatty Applications.</span></span>

    <span data-ttu-id="80106-109">Alguns aplicativos executam muitas transações pequenas.</span><span class="sxs-lookup"><span data-stu-id="80106-109">Some applications perform many small transactions.</span></span> <span data-ttu-id="80106-110">Quando combinado com a sobrecarga de rede associada a cada uma dessas transações, o efeito é multiplicado.</span><span class="sxs-lookup"><span data-stu-id="80106-110">When combined with the network overhead associated with each such transaction, the effect is multiplied.</span></span> <span data-ttu-id="80106-111">Em rede, as transações pequenas podem consumir tantos recursos quanto grandes transações.</span><span class="sxs-lookup"><span data-stu-id="80106-111">In networking, small transactions can consume as many resources and as much time as large transactions.</span></span> <span data-ttu-id="80106-112">Uma abordagem melhor é combinar muitas transações pequenas em uma única transação grande.</span><span class="sxs-lookup"><span data-stu-id="80106-112">A better approach is to combine many small transactions into a single large transaction.</span></span>

-   <span data-ttu-id="80106-113">Transações serializadas.</span><span class="sxs-lookup"><span data-stu-id="80106-113">Serialized Transactions.</span></span>

    <span data-ttu-id="80106-114">A serialização desnecessária de transações pode resultar em baixo desempenho e afetar a escalabilidade.</span><span class="sxs-lookup"><span data-stu-id="80106-114">Unnecessary serialization of transactions can result in poor performance, and affect scalability.</span></span> <span data-ttu-id="80106-115">Por exemplo, 1000 transações serializadas levam pelo menos 1000 \* RTT para serem concluídas.</span><span class="sxs-lookup"><span data-stu-id="80106-115">For example, 1000 serialized transactions take at least 1000 \* RTT to complete.</span></span> <span data-ttu-id="80106-116">Uma abordagem melhor é executar transações não relacionadas em paralelo.</span><span class="sxs-lookup"><span data-stu-id="80106-116">A better approach is to run unrelated transactions in parallel.</span></span> <span data-ttu-id="80106-117">Quando aplicativos serializados são combinados com aplicativos informais, a capacidade de resposta pode ser seriamente dificultada.</span><span class="sxs-lookup"><span data-stu-id="80106-117">When serialized applications are combined with chatty applications, responsiveness can be seriously hampered.</span></span>

    > [!Note]  
    > <span data-ttu-id="80106-118">A desserialização correta de um aplicativo pode ser difícil.</span><span class="sxs-lookup"><span data-stu-id="80106-118">Properly deserializing an application can be difficult.</span></span> <span data-ttu-id="80106-119">Se a alteração de uma prova de serializado para paralelo for muito difícil, considere combinar várias transações em menos transações grandes.</span><span class="sxs-lookup"><span data-stu-id="80106-119">If changing from serialized to parallel proves too difficult, consider combining multiple transactions into fewer large transactions.</span></span>

     

-   <span data-ttu-id="80106-120">Transações de Fat.</span><span class="sxs-lookup"><span data-stu-id="80106-120">Fat Transactions.</span></span>

    <span data-ttu-id="80106-121">Os aplicativos que enviam bytes desnecessários na rede são considerados aplicativos Fat.</span><span class="sxs-lookup"><span data-stu-id="80106-121">Applications that send unnecessary bytes on the network are considered fat applications.</span></span> <span data-ttu-id="80106-122">Os aplicativos que enviam bytes desnecessários na rede aumentam a sobrecarga de rede e o desempenho é dificultado.</span><span class="sxs-lookup"><span data-stu-id="80106-122">Applications that send unnecessary bytes on the network increase network overhead, and performance is hampered.</span></span> <span data-ttu-id="80106-123">Essa situação geralmente vem de estruturas de dados ineficientes ou streaming de dados ineficiente.</span><span class="sxs-lookup"><span data-stu-id="80106-123">This situation often comes from inefficient data structures or inefficient data streaming.</span></span> <span data-ttu-id="80106-124">Para corrigir isso, Otimize as estruturas de dados ou considere o uso da compactação.</span><span class="sxs-lookup"><span data-stu-id="80106-124">To remedy this, optimize data structures, or consider using compression.</span></span>

<span data-ttu-id="80106-125">As seções a seguir abordam aspectos do desenvolvimento de aplicativos a serem considerados.</span><span class="sxs-lookup"><span data-stu-id="80106-125">The following sections address aspects of application development to consider.</span></span>

-   [<span data-ttu-id="80106-126">Problemas específicos de TCP/IP</span><span class="sxs-lookup"><span data-stu-id="80106-126">TCP/IP-specific Issues</span></span>](tcp-ip-specific-issues-2.md)
-   [<span data-ttu-id="80106-127">Reconhecendo aplicativos lentos</span><span class="sxs-lookup"><span data-stu-id="80106-127">Recognizing Slow Applications</span></span>](recognizing-slow-applications-2.md)
-   [<span data-ttu-id="80106-128">Calculando a sobrecarga com netstat</span><span class="sxs-lookup"><span data-stu-id="80106-128">Calculating Overhead with Netstat</span></span>](calculating-overhead-with-netstat-2.md)

## <a name="related-topics"></a><span data-ttu-id="80106-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="80106-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80106-130">Aplicativos de alto desempenho do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="80106-130">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



