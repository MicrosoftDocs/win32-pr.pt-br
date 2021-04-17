---
description: Determinadas técnicas de programação são executadas em problemas de desempenho que estão vinculados à implementação do TCP/IP.
ms.assetid: 2a63e85e-06fd-4b6f-8351-9866099b9d54
title: Problemas específicos de TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9a7334471d3e419830eb054399ff1dcb721cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798514"
---
# <a name="tcpip-specific-issues"></a><span data-ttu-id="b36c7-103">Problemas específicos de TCP/IP</span><span class="sxs-lookup"><span data-stu-id="b36c7-103">TCP/IP-specific Issues</span></span>

<span data-ttu-id="b36c7-104">Determinadas técnicas de programação são executadas em problemas de desempenho que estão vinculados à implementação do TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="b36c7-104">Certain programming techniques run into performance issues that are linked to the implementation of TCP/IP.</span></span> <span data-ttu-id="b36c7-105">Esses problemas de desempenho não sugerem que o TCP/IP é ineficiente ou um afunilamento de desempenho; em vez disso, esses problemas são vistos quando as operações de TCP/IP não são compreendidas.</span><span class="sxs-lookup"><span data-stu-id="b36c7-105">Such performance issues do not suggest that TCP/IP is inefficient or a performance bottleneck; rather, these issues are seen when TCP/IP operations are not understood.</span></span>

<span data-ttu-id="b36c7-106">Os problemas a seguir identificam cenários comuns nos quais a combinação de operação TCP/IP e opções de desenvolvimento de aplicativos de rede resultam em baixo desempenho.</span><span class="sxs-lookup"><span data-stu-id="b36c7-106">The following issues identify common scenarios in which the combination of TCP/IP operation and network application development choices result in poor performance.</span></span>

-   <span data-ttu-id="b36c7-107">Aplicativos com conexão pesada.</span><span class="sxs-lookup"><span data-stu-id="b36c7-107">Connect-heavy Applications.</span></span>

    <span data-ttu-id="b36c7-108">Alguns aplicativos instanciam uma nova conexão TCP para cada transação.</span><span class="sxs-lookup"><span data-stu-id="b36c7-108">Some applications instantiate a new TCP connection for each transaction.</span></span> <span data-ttu-id="b36c7-109">O estabelecimento da conexão TCP leva tempo, contribui para RTTs extras e está sujeito a um início lento.</span><span class="sxs-lookup"><span data-stu-id="b36c7-109">TCP connection establishment takes time, contributes extra RTTs, and is subject to slow-start.</span></span> <span data-ttu-id="b36c7-110">Além disso, as conexões fechadas estão sujeitas à espera de tempo, o que consome recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="b36c7-110">In addition, the closed connections are subject to TIME-WAIT, which consumes system resources.</span></span>

    <span data-ttu-id="b36c7-111">Aplicativos com conexão pesada são comuns em grande parte porque são fáceis de criar; o teste e o tratamento de erros são muito simples.</span><span class="sxs-lookup"><span data-stu-id="b36c7-111">Connect-heavy applications are common largely because they are easy to create; testing and error handling is very simple.</span></span> <span data-ttu-id="b36c7-112">Detectar falhas em uma conexão persistente pode levar a um código e esforço consideráveis e, portanto, às vezes não é concluído.</span><span class="sxs-lookup"><span data-stu-id="b36c7-112">Detecting faults on a persistent connection can take considerable code and effort, and therefore is sometimes not completed.</span></span>

    <span data-ttu-id="b36c7-113">Remediar essa situação reutilizando a conexão TCP.</span><span class="sxs-lookup"><span data-stu-id="b36c7-113">Remedy this situation by reusing the TCP connection.</span></span> <span data-ttu-id="b36c7-114">Isso pode causar a serialização sobre a conexão TCP, a menos que as transações sejam multiplexada em várias conexões.</span><span class="sxs-lookup"><span data-stu-id="b36c7-114">This may cause serialization over the TCP connection unless the transactions are multiplexed over multiple connections.</span></span> <span data-ttu-id="b36c7-115">Se essa abordagem for adotada, o número de conexões deverá ser limitado a dois, e o enquadramento de camada de aplicativo e o tratamento de erros avançado serão necessários.</span><span class="sxs-lookup"><span data-stu-id="b36c7-115">If this approach is taken, the number of connections should be limited to two, and application-layer framing and advanced error handling are required.</span></span>

-   <span data-ttu-id="b36c7-116">Buffers de envio de comprimento zero e envios de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="b36c7-116">Zero-length Send Buffers and Blocking Sends.</span></span>

    <span data-ttu-id="b36c7-117">Desativar o armazenamento em buffer usando a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para definir o buffer de envio (portanto, \_ SNDBUF) como zero é semelhante a desativar o cache de disco.</span><span class="sxs-lookup"><span data-stu-id="b36c7-117">Turning off buffering by using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to set the send buffer (SO\_SNDBUF) to zero is similar to turning off disk caching.</span></span> <span data-ttu-id="b36c7-118">Ao definir o buffer de envio como zero e emitir o bloqueio envia, um aplicativo tem uma chance de 50% de atingir uma confirmação de atraso de 200 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="b36c7-118">When setting the send buffer to zero and issuing blocking sends, an application has a fifty percent chance of hitting a 200-millisecond delayed acknowledgment.</span></span>

    <span data-ttu-id="b36c7-119">Não desative o buffer de envio, a menos que você tenha considerado o impacto em todos os ambientes de rede.</span><span class="sxs-lookup"><span data-stu-id="b36c7-119">Do not turn off send buffering unless you have considered the impact in all network environments.</span></span> <span data-ttu-id="b36c7-120">Uma exceção: streaming de dados usando e/s sobreposta deve definir o buffer de envio como zero.</span><span class="sxs-lookup"><span data-stu-id="b36c7-120">One exception: streaming data using overlapped I/O should set the send buffer to zero.</span></span>

-   <span data-ttu-id="b36c7-121">Modelo de programação enviar-enviar-receber.</span><span class="sxs-lookup"><span data-stu-id="b36c7-121">Send-Send-Receive programming model.</span></span>

    <span data-ttu-id="b36c7-122">Estruturar um aplicativo para executar Send-Send-receives aumenta suas chances de encontrar o algoritmo Nagle, o que causa um atraso de RTT + 200 ms.</span><span class="sxs-lookup"><span data-stu-id="b36c7-122">Structuring an application to perform send-send-receives increases your chances of encountering the Nagle Algorithm, which causes a delay of RTT+200 ms.</span></span> <span data-ttu-id="b36c7-123">O algoritmo Nagle poderá ser encontrado se o último envio for menor que o tamanho máximo de segmento TCP (MSS, o máximo de dados em um único datagrama).</span><span class="sxs-lookup"><span data-stu-id="b36c7-123">The Nagle Algorithm may be encountered if the last send is less than the TCP Maximum Segment Size (MSS, the maximum data in a single datagram).</span></span> <span data-ttu-id="b36c7-124">O MSS pode ser um valor muito grande (64K em IPv4 e ainda maior no IPv6), portanto, não conte em um MSS pequeno, normalmente.</span><span class="sxs-lookup"><span data-stu-id="b36c7-124">MSS can be a very large value (64K in IPv4, and even larger in IPv6), so do not count on a typically small MSS.</span></span> <span data-ttu-id="b36c7-125">Uma opção melhor é combinar os dois envios em um único envio usando a função [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) ou **memcpy** .</span><span class="sxs-lookup"><span data-stu-id="b36c7-125">A better option is to combine the two sends into a single send using the [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) or **memcpy** function.</span></span>

-   <span data-ttu-id="b36c7-126">Grande número de conexões simultâneas.</span><span class="sxs-lookup"><span data-stu-id="b36c7-126">Large Number of Simultaneous Connections.</span></span>

    <span data-ttu-id="b36c7-127">As conexões simultâneas não devem exceder duas, exceto em aplicativos de finalidade especial.</span><span class="sxs-lookup"><span data-stu-id="b36c7-127">Concurrent connections should not exceed two, except in special purpose applications.</span></span> <span data-ttu-id="b36c7-128">Exceder duas conexões simultâneas resulta em recursos desperdiçados.</span><span class="sxs-lookup"><span data-stu-id="b36c7-128">Exceeding two concurrent connections results in wasted resources.</span></span> <span data-ttu-id="b36c7-129">Uma boa regra é ter até quatro conexões de curta duração ou duas conexões persistentes por destino.</span><span class="sxs-lookup"><span data-stu-id="b36c7-129">A good rule is to have up to four short lived connections, or two persistent connections per destination.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b36c7-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b36c7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b36c7-131">Comportamento do aplicativo</span><span class="sxs-lookup"><span data-stu-id="b36c7-131">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="b36c7-132">Aplicativos de alto desempenho do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="b36c7-132">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="b36c7-133">Algoritmo Nagle</span><span class="sxs-lookup"><span data-stu-id="b36c7-133">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



