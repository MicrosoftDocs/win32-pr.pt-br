---
description: Threads de streaming e o Gerenciador de gráfico de filtro
ms.assetid: b490b72a-ab34-46e6-8dc6-a7bb07cfc7b1
title: Threads de streaming e o Gerenciador de gráfico de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a8c5b8fa972a8118563ae8f9e73d480ac15e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759111"
---
# <a name="streaming-threads-and-the-filter-graph-manager"></a><span data-ttu-id="84be0-103">Threads de streaming e o Gerenciador de gráfico de filtro</span><span class="sxs-lookup"><span data-stu-id="84be0-103">Streaming Threads and the Filter Graph Manager</span></span>

<span data-ttu-id="84be0-104">Quando o Gerenciador de gráfico de filtro para o grafo, ele aguarda que todos os threads de streaming sejam desligados.</span><span class="sxs-lookup"><span data-stu-id="84be0-104">When the Filter Graph Manager stops the graph, it waits for all streaming threads to shut down.</span></span> <span data-ttu-id="84be0-105">Isso tem as seguintes implicações para filtros:</span><span class="sxs-lookup"><span data-stu-id="84be0-105">This has the following implications for filters:</span></span>

-   <span data-ttu-id="84be0-106">Um filtro nunca deve chamar métodos no Gerenciador do grafo de filtro de um thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="84be0-106">A filter must never call methods on the Filter Graph Manager from a streaming thread.</span></span>

    <span data-ttu-id="84be0-107">O Gerenciador de gráfico de filtro usa uma seção crítica para sincronizar suas próprias operações.</span><span class="sxs-lookup"><span data-stu-id="84be0-107">The Filter Graph Manager uses a critical section to synchronize its own operations.</span></span> <span data-ttu-id="84be0-108">Se um thread de streaming tentar manter essa seção crítica, isso poderá causar um deadlock.</span><span class="sxs-lookup"><span data-stu-id="84be0-108">If a streaming thread tries to hold this critical section, it can cause a deadlock.</span></span> <span data-ttu-id="84be0-109">Por exemplo: Suponha que outro thread interrompa o grafo.</span><span class="sxs-lookup"><span data-stu-id="84be0-109">For example: Suppose that another thread stops the graph.</span></span> <span data-ttu-id="84be0-110">Esse thread pega o bloqueio do grafo de filtro e aguarda o filtro parar de entregar os dados.</span><span class="sxs-lookup"><span data-stu-id="84be0-110">That thread takes the filter graph lock and waits for your filter to stop delivering data.</span></span> <span data-ttu-id="84be0-111">Se o filtro estiver aguardando o bloqueio, ele nunca será interrompido, causando um deadlock.</span><span class="sxs-lookup"><span data-stu-id="84be0-111">If your filter is waiting for the lock, it will never stop, causing a deadlock.</span></span>

-   <span data-ttu-id="84be0-112">Um filtro nunca deve ser **AddRef** ou **QueryInterface** no Gerenciador do grafo de filtro de um thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="84be0-112">A filter must never **AddRef** or **QueryInterface** the Filter Graph Manager from a streaming thread.</span></span>

    <span data-ttu-id="84be0-113">Se o filtro mantiver uma contagem de referência no Gerenciador de gráfico de filtro (por meio de **AddRef** ou **QueryInterface**), ele poderá se tornar o último objeto para manter uma contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="84be0-113">If the filter holds a reference count on the Filter Graph Manager (through **AddRef** or **QueryInterface**), it might become the last object to hold a reference count.</span></span> <span data-ttu-id="84be0-114">Quando o filtro chama **Release**, o Gerenciador do grafo de filtro se destrói.</span><span class="sxs-lookup"><span data-stu-id="84be0-114">When the filter calls **Release**, the Filter Graph Manager destroys itself.</span></span> <span data-ttu-id="84be0-115">Dentro de sua rotina de limpeza, o Gerenciador do grafo de filtro tenta parar o grafo, fazendo com que ele aguarde até que o thread de streaming saia.</span><span class="sxs-lookup"><span data-stu-id="84be0-115">Inside its cleanup routine, the Filter Graph Manager attempts to stop the graph, causing it to wait for the streaming thread to exit.</span></span> <span data-ttu-id="84be0-116">No entanto, ele está aguardando dentro do thread de streaming, portanto, o thread de streaming não pode sair.</span><span class="sxs-lookup"><span data-stu-id="84be0-116">However, it is waiting inside the streaming thread, so the streaming thread cannot exit.</span></span> <span data-ttu-id="84be0-117">O resultado é um deadlock.</span><span class="sxs-lookup"><span data-stu-id="84be0-117">The result is a deadlock.</span></span>

 

 



