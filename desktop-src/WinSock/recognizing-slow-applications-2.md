---
description: Este guia identifica um aplicativo lento como um aplicativo do Microsoft Windows com desempenho prejudicado.
ms.assetid: cacf55d8-ab64-47a4-a55b-59a3c4e3877b
title: Reconhecendo aplicativos lentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07be9484a3b08951b8b64989757459531ff72906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814143"
---
# <a name="recognizing-slow-applications"></a><span data-ttu-id="be0c8-103">Reconhecendo aplicativos lentos</span><span class="sxs-lookup"><span data-stu-id="be0c8-103">Recognizing Slow Applications</span></span>

<span data-ttu-id="be0c8-104">Este guia identifica um aplicativo *lento* como um aplicativo do Microsoft Windows com desempenho prejudicado.</span><span class="sxs-lookup"><span data-stu-id="be0c8-104">This guide identifies a *slow* application as a Microsoft Windows application with impaired performance.</span></span> <span data-ttu-id="be0c8-105">Um aplicativo lento exibe um ou mais dos seguintes sintomas:</span><span class="sxs-lookup"><span data-stu-id="be0c8-105">A slow application exhibits one or more of the following symptoms:</span></span>

-   <span data-ttu-id="be0c8-106">A utilização da CPU e da rede é baixa.</span><span class="sxs-lookup"><span data-stu-id="be0c8-106">CPU and network utilization are low.</span></span>

    <span data-ttu-id="be0c8-107">O computador parece estar aguardando algo.</span><span class="sxs-lookup"><span data-stu-id="be0c8-107">The computer appears to be waiting on something.</span></span> <span data-ttu-id="be0c8-108">Geralmente, o aplicativo está aguardando a rede.</span><span class="sxs-lookup"><span data-stu-id="be0c8-108">Often, the application is waiting on the network.</span></span>

-   <span data-ttu-id="be0c8-109">A desativação do algoritmo Nagle por meio da \_ opção de soquete TCP NoDelay aumenta o desempenho.</span><span class="sxs-lookup"><span data-stu-id="be0c8-109">Turning off the Nagle Algorithm through the TCP\_NODELAY socket option increases performance.</span></span>

    <span data-ttu-id="be0c8-110">Isso indica outros problemas e não deve ser considerado uma solução.</span><span class="sxs-lookup"><span data-stu-id="be0c8-110">This indicates other problems, and should not be considered a solution.</span></span> <span data-ttu-id="be0c8-111">A desativação do algoritmo Nagle aumenta a sobrecarga do protocolo.</span><span class="sxs-lookup"><span data-stu-id="be0c8-111">Turning off the Nagle algorithm increases the protocol overhead.</span></span> <span data-ttu-id="be0c8-112">Não use esse método como uma correção para os aplicativos desfeitos – apenas como uma indicação de que o aplicativo precisa de outro trabalho para corrigir problemas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="be0c8-112">Do not use this method as a fix for the broken applications—only as an indication the application needs other work to fix performance issues.</span></span>

-   <span data-ttu-id="be0c8-113">O aplicativo exibe uma sobrecarga alta.</span><span class="sxs-lookup"><span data-stu-id="be0c8-113">The application exhibits high overhead.</span></span>

    <span data-ttu-id="be0c8-114">Para calcular a sobrecarga dos aplicativos, determine a quantidade de dados que você pretende transferir em cada direção.</span><span class="sxs-lookup"><span data-stu-id="be0c8-114">To calculate your applications overhead, determine how much data you intended to transfer in each direction.</span></span> <span data-ttu-id="be0c8-115">Em seguida, use netstat e Add (para Ethernet) 60 bytes para cada pacote e 500 bytes para cada conexão.</span><span class="sxs-lookup"><span data-stu-id="be0c8-115">Then use Netstat and add (for Ethernet) 60 bytes for each packet and 500 bytes for each connection.</span></span> <span data-ttu-id="be0c8-116">A melhor sobrecarga que pode ser esperada para streaming pela Ethernet é de aproximadamente 6%.</span><span class="sxs-lookup"><span data-stu-id="be0c8-116">The best overhead that can be expected for streaming over Ethernet is approximately 6%.</span></span> <span data-ttu-id="be0c8-117">Para uma conexão de modem, a melhor sobrecarga é de aproximadamente 2%, devido ao fato de que um link PPP usa a compactação de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="be0c8-117">For a modem connection, the best overhead is approximately 2%, due to the fact that a PPP link uses header compression.</span></span> <span data-ttu-id="be0c8-118">Consulte [calculando a sobrecarga com o netstat](calculating-overhead-with-netstat-2.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="be0c8-118">See [Calculating Overhead with Netstat](calculating-overhead-with-netstat-2.md) for more information.</span></span>

-   <span data-ttu-id="be0c8-119">A resposta do aplicativo fica mais lenta quando a conexão tem um RTT grande.</span><span class="sxs-lookup"><span data-stu-id="be0c8-119">Application response slows when the connection has a large RTT.</span></span>

    <span data-ttu-id="be0c8-120">Supondo que o aplicativo não esteja se aproximando da largura de banda do link, um RTT grande deve ter pouco ou nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="be0c8-120">Assuming the application is not approaching the link's bandwidth, a large RTT should have little or no effect.</span></span> <span data-ttu-id="be0c8-121">Uma lentidão drástica com um grande RTT é um sinal claro de processamento serializado e muitas transações pequenas.</span><span class="sxs-lookup"><span data-stu-id="be0c8-121">A dramatic slowdown with a large RTT is a clear sign of serialized processing and many small transactions.</span></span>

<span data-ttu-id="be0c8-122">Cada aplicativo deve ser testado em um ambiente com um grande RTT.</span><span class="sxs-lookup"><span data-stu-id="be0c8-122">Every application should be tested in an environment with a large RTT.</span></span> <span data-ttu-id="be0c8-123">Isso revela a maioria dos aplicativos que sofrem com opções de desenvolvimento deficientes.</span><span class="sxs-lookup"><span data-stu-id="be0c8-123">Doing so reveals most applications that suffer from poor development choices.</span></span> <span data-ttu-id="be0c8-124">Esse teste pode ser executado em vários ambientes, incluindo uma rede LAN sem fio, um simulador de atraso de link ou uma rede de satélite.</span><span class="sxs-lookup"><span data-stu-id="be0c8-124">This testing can be performed in several environments, including a wireless LAN network, a link-delay simulator, or a satellite network.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be0c8-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="be0c8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be0c8-126">Comportamento do aplicativo</span><span class="sxs-lookup"><span data-stu-id="be0c8-126">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="be0c8-127">Aplicativos de alto desempenho do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="be0c8-127">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="be0c8-128">Algoritmo Nagle</span><span class="sxs-lookup"><span data-stu-id="be0c8-128">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



