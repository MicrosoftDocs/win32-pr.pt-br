---
title: Desenvolvendo um servidor RPC de alto desempenho
description: As informações nesta seção aplicam-se às sequências de protocolo remoto ncacn \_ IP \_ TCP, ncacn \_ http, ncacn \_ np e ao Windows 2000 e Windows XP.
ms.assetid: 7b4239af-951b-4d1b-8ac3-224279f6929e
keywords:
- RPC de chamada de procedimento remoto, práticas recomendadas, desenvolvimento de um servidor de alto desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a18319c1f4ade80ae026b68c8f5540030b992b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454283"
---
# <a name="developing-a-high-performance-rpc-server"></a><span data-ttu-id="bbe86-104">Desenvolvendo um servidor RPC de alto desempenho</span><span class="sxs-lookup"><span data-stu-id="bbe86-104">Developing a High Performance RPC Server</span></span>

<span data-ttu-id="bbe86-105">As informações contidas nesta seção aplicam-se a sequências de protocolo remoto: [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn \_ http**](/windows/desktop/Midl/ncacn-http), [**NCACN \_ NP**](/windows/desktop/Midl/ncacn-np)e para Windows 2000 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bbe86-105">The information in this section applies to remote protocol sequences: [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn\_http**](/windows/desktop/Midl/ncacn-http), [**ncacn\_np**](/windows/desktop/Midl/ncacn-np), and to Windows 2000 and Windows XP.</span></span>

<span data-ttu-id="bbe86-106">Esta seção aborda três aspectos principais do desempenho do servidor RPC:</span><span class="sxs-lookup"><span data-stu-id="bbe86-106">This section addresses three primary aspects of RPC server performance:</span></span>

-   [<span data-ttu-id="bbe86-107">Latência de rede e taxa de transferência</span><span class="sxs-lookup"><span data-stu-id="bbe86-107">Network Latency and Throughput</span></span>](network-latency-and-throughput.md)
-   [<span data-ttu-id="bbe86-108">Escalabilidade</span><span class="sxs-lookup"><span data-stu-id="bbe86-108">Scalability</span></span>](scalability.md)
-   [<span data-ttu-id="bbe86-109">Dicas de desempenho de RPC diversas</span><span class="sxs-lookup"><span data-stu-id="bbe86-109">Miscellaneous RPC Performance Tips</span></span>](miscellaneous-rpc-performance-tips.md)

<span data-ttu-id="bbe86-110">O comprimento do caminho de código é outra consideração de desempenho principal para RPC.</span><span class="sxs-lookup"><span data-stu-id="bbe86-110">Code path length is another primary performance consideration for RPC.</span></span> <span data-ttu-id="bbe86-111">O tamanho do caminho de código geralmente é bem compreendido e, como a literatura e as ferramentas estão amplamente disponíveis nesse tópico, este artigo não o resolve.</span><span class="sxs-lookup"><span data-stu-id="bbe86-111">Code path length is generally well understood, and since literature and tools are widely available on that topic, this article does not address it.</span></span>

<span data-ttu-id="bbe86-112">Uma regra de desempenho geral importante e estabelecida a ser lembrada ao considerar o desempenho de RPC é esta: Encontre o afunilamento no sistema e trabalhe para resolver isso.</span><span class="sxs-lookup"><span data-stu-id="bbe86-112">An important and established general performance rule to remember while considering RPC performance is this: find the bottleneck in the system, and work to resolve that.</span></span> <span data-ttu-id="bbe86-113">O afunilamento de retenção pode não ser a programação RPC e, se esse for o caso, o ajuste de desempenho no RPC não resultará em desempenho aprimorado até que o afunilamento seja resolvido.</span><span class="sxs-lookup"><span data-stu-id="bbe86-113">The gating bottleneck may not be the RPC programming, and if that is the case, performance tuning in RPC will not result in enhanced performance until that bottleneck is addressed.</span></span> <span data-ttu-id="bbe86-114">Por exemplo, um sistema afetado pela contenção de recursos não precisa fazer uso mais eficiente da rede.</span><span class="sxs-lookup"><span data-stu-id="bbe86-114">For example, a system plagued by resource contention does not need to make more efficient use of the network.</span></span>

<span data-ttu-id="bbe86-115">Se o seu sistema estiver implantado em vários ambientes, é uma boa ideia garantir que todos os aspectos dele sejam bem ajustados, pois diferentes ambientes podem produzir gargalos de desempenho variados.</span><span class="sxs-lookup"><span data-stu-id="bbe86-115">If your system is deployed in various environments, it is a good idea to make sure all aspects of it are well tuned, as different environments can produce varied performance bottlenecks.</span></span>

 

 