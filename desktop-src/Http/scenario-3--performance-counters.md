---
title: Cenário 3 contadores de desempenho
description: Os contadores de desempenho medem quantidades de informações ou dados, de acordo com o número, o tamanho, a duração e a taxa de dados que estão sendo solicitados ou recebidos.
ms.assetid: 1b264144-7600-402e-86f8-674a2d02f9f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de90607cbda0542ee385b83f44bec878927d509f
ms.sourcegitcommit: fc3f2a28a55e590ac38846048f10b64ba527a98d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "105780544"
---
# <a name="scenario-3-performance-counters"></a><span data-ttu-id="5eeb9-103">Cenário 3: contadores de desempenho</span><span class="sxs-lookup"><span data-stu-id="5eeb9-103">Scenario 3: Performance Counters</span></span>

<span data-ttu-id="5eeb9-104">Os contadores de desempenho medem quantidades de informações ou dados, de acordo com o número, o tamanho, a duração e a taxa de dados que estão sendo solicitados ou recebidos.</span><span class="sxs-lookup"><span data-stu-id="5eeb9-104">Performance counters measure quantities of information or data, according to the number, size, duration, and rate of data being requested or received.</span></span> <span data-ttu-id="5eeb9-105">Você não deve esperar obter uma lista de detalhes de um contador, como uma lista de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="5eeb9-105">You should not expect to get a list of details from a counter, such as a list of error messages.</span></span> <span data-ttu-id="5eeb9-106">Em vez disso, use contadores de desempenho para obter quantidades, como o número de mensagens de erro desde a inicialização ou a taxa na qual as mensagens de erro estão sendo geradas.</span><span class="sxs-lookup"><span data-stu-id="5eeb9-106">Instead, use performance counters to get quantities, such as the number of error message since startup or the rate at which error messages are being generated.</span></span>

## <a name="performance-counters-for-httpsys"></a><span data-ttu-id="5eeb9-107">Contadores de desempenho para HTTP.sys</span><span class="sxs-lookup"><span data-stu-id="5eeb9-107">Performance Counters for HTTP.sys</span></span>

<span data-ttu-id="5eeb9-108">A partir do Windows Vista e do Windows Server 2008, HTTP.sys tem os seguintes contadores de métrica de desempenho para ajudá-lo com monitoramento, diagnóstico e planejamento de capacidade para servidores Web: o componente de API do servidor HTTP tem os seguintes contadores de desempenho para ajudá-lo com monitoramento, diagnóstico e planejamento de capacidade para servidores Web:</span><span class="sxs-lookup"><span data-stu-id="5eeb9-108">Starting with Windows Vista and Windows Server 2008, HTTP.sys has the following performance metric counters to help you with monitoring, diagnosing, and capacity planning for Web servers: The HTTP Server API component has the following performance counters to help you with monitoring, diagnosing, and capacity planning for Web servers:</span></span>

- <span data-ttu-id="5eeb9-109">Contadores de serviço HTTP:</span><span class="sxs-lookup"><span data-stu-id="5eeb9-109">HTTP Service Counters:</span></span>
  - <span data-ttu-id="5eeb9-110">Número de URIs no cache, adicionadas desde a inicialização, excluídas desde a inicialização e o número de liberações de cache</span><span class="sxs-lookup"><span data-stu-id="5eeb9-110">Number of URIs in the cache, added since startup, deleted since startup, and number of cache flushes</span></span>
  - <span data-ttu-id="5eeb9-111">Acertos de cache/segundo e erros de cache/segundo</span><span class="sxs-lookup"><span data-stu-id="5eeb9-111">Cache hits/second and Cache misses/second</span></span>
- <span data-ttu-id="5eeb9-112">Grupos de URLs de serviço HTTP:</span><span class="sxs-lookup"><span data-stu-id="5eeb9-112">HTTP Service URL Groups:</span></span>
  - <span data-ttu-id="5eeb9-113">Taxa de envio de dados, taxa de recebimento de dados, bytes transferidos (enviados e recebidos)</span><span class="sxs-lookup"><span data-stu-id="5eeb9-113">Data send rate, data receive rate, bytes transferred (sent and received)</span></span>
  - <span data-ttu-id="5eeb9-114">Número máximo de conexões, taxa de tentativas de conexão, taxa para solicitações GET e HEAD e número total de solicitações</span><span class="sxs-lookup"><span data-stu-id="5eeb9-114">Maximum number of connections, connection attempts rate, rate for GET and HEAD requests, and total number of requests</span></span>
- <span data-ttu-id="5eeb9-115">Filas de solicitação de serviço HTTP:</span><span class="sxs-lookup"><span data-stu-id="5eeb9-115">HTTP Service Request Queues:</span></span>
  - <span data-ttu-id="5eeb9-116">Número de solicitações na fila, idade das solicitações mais antigas na fila (idade da última solicitação na fila)</span><span class="sxs-lookup"><span data-stu-id="5eeb9-116">Number of requests in queue, age of oldest requests in queue (age of the last request in the queue)</span></span>
  - <span data-ttu-id="5eeb9-117">Taxa de entradas de solicitação na fila, taxa de rejeição, número total de solicitações rejeitadas, taxa de acertos de cache</span><span class="sxs-lookup"><span data-stu-id="5eeb9-117">Rate of request arrivals into the queue, rate of rejection, total number of rejected requests, rate of cache hits</span></span>

<span data-ttu-id="5eeb9-118">**Acessando contadores de desempenho**</span><span class="sxs-lookup"><span data-stu-id="5eeb9-118">**Accessing Performance Counters**</span></span>

1.  <span data-ttu-id="5eeb9-119">Digite **Perfmon** no prompt de comando para iniciar o console de diagnóstico de desempenho.</span><span class="sxs-lookup"><span data-stu-id="5eeb9-119">Type **perfmon** at the command prompt to start the Performance Diagnostic Console.</span></span>
2.  <span data-ttu-id="5eeb9-120">Selecione **Monitor de desempenho** no controle de árvore e, em seguida, abra **Adicionar contadores** clicando em **+** .</span><span class="sxs-lookup"><span data-stu-id="5eeb9-120">Select **Performance Monitor** in the tree control and then open the **Add Counters** by clicking **+**.</span></span>
3.  <span data-ttu-id="5eeb9-121">Em **Adicionar contadores** , selecione entre os três conjuntos de contadores de desempenho: **serviço http**, **filas de solicitação de serviço http** ou **grupos de URL de serviço http**.</span><span class="sxs-lookup"><span data-stu-id="5eeb9-121">From **Add Counters** select from the three Performance Counters sets: **HTTP Service**, **HTTP Service Request Queues** , or **HTTP Service Url Groups**.</span></span>
4.  <span data-ttu-id="5eeb9-122">Para exibir os contadores dos conjuntos de contadores **filas de solicitação de serviço http** e **grupos de URLs de serviço http** , selecione **instâncias** e clique em **Adicionar** e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="5eeb9-122">To view counters from the **HTTP Service Request Queues** and **HTTP Service Url Groups** counter sets, select **instance(s)** and click **Add**, and then click **OK**.</span></span> <span data-ttu-id="5eeb9-123">Para exibir os contadores de serviço HTTP, selecione o conjunto de contadores no painel esquerdo e clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="5eeb9-123">To view the HTTP Service counters, select the counter set in the left pane and click **Add**.</span></span>

> [!Note]  
> <span data-ttu-id="5eeb9-124">Há apenas uma instância dos contadores da API do servidor HTTP por computador, pois esses contadores representam o estado de todo o componente.</span><span class="sxs-lookup"><span data-stu-id="5eeb9-124">Only one instance of the HTTP Server API counters exists per machine, as these counters represent the component-wide state.</span></span> <span data-ttu-id="5eeb9-125">Com instâncias de contadores de desempenho do grupo de URLs, a ID da instância (para o contador de desempenho) corresponderá à ID do grupo de URLs.</span><span class="sxs-lookup"><span data-stu-id="5eeb9-125">With instances of Url Group performance counters, the instance ID (for the performance counter) will match the Url Group ID.</span></span> <span data-ttu-id="5eeb9-126">A ID do grupo de URLs pode ser exibida executando **netsh http show ServiceState**.</span><span class="sxs-lookup"><span data-stu-id="5eeb9-126">The Url Group ID can be viewed by running **netsh http show servicestate**.</span></span> <span data-ttu-id="5eeb9-127">Com instâncias de contadores de desempenho de filas de solicitações, o nome da instância corresponde ao nome da fila de solicitações.</span><span class="sxs-lookup"><span data-stu-id="5eeb9-127">With instances of Request Queues performance counters, the instance name corresponds to Request Queue Name.</span></span> <span data-ttu-id="5eeb9-128">O nome da fila de solicitação (se houver) pode ser mostrado pelo mesmo **netsh http show ServiceState**.</span><span class="sxs-lookup"><span data-stu-id="5eeb9-128">The Request Queue Name (if one exists) can be shown by the same **netsh http show servicestate**.</span></span> <span data-ttu-id="5eeb9-129">No entanto, alguns aplicativos de servidor podem ter filas de solicitação sem nome que não podem corresponder a uma ID de instância de contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="5eeb9-129">However, some server applications may have unnamed Request Queues that cannot be matched to a performance counter instance ID.</span></span>

 

 

 




