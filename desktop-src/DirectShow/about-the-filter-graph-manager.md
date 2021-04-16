---
description: Sobre o Gerenciador do grafo de filtro
ms.assetid: a227539a-7f9a-4f8d-99fe-f9ab67df9ef4
title: Sobre o Gerenciador do grafo de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedf716b84ee62818e323bfaa082b6252e5faad0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500597"
---
# <a name="about-the-filter-graph-manager"></a><span data-ttu-id="05432-103">Sobre o Gerenciador do grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="05432-103">About the Filter Graph Manager</span></span>

<span data-ttu-id="05432-104">O [Gerenciador do grafo de filtro](filter-graph-manager.md) é um objeto com que controla os filtros em um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="05432-104">The [Filter Graph Manager](filter-graph-manager.md) is a COM object that controls the filters in a filter graph.</span></span> <span data-ttu-id="05432-105">Ele executa muitas funções, incluindo as seguintes:</span><span class="sxs-lookup"><span data-stu-id="05432-105">It performs many functions, including the following:</span></span>

-   <span data-ttu-id="05432-106">Coordenando alterações de estado entre os filtros.</span><span class="sxs-lookup"><span data-stu-id="05432-106">Coordinating state changes among the filters.</span></span>
-   <span data-ttu-id="05432-107">Estabelecendo um relógio de referência.</span><span class="sxs-lookup"><span data-stu-id="05432-107">Establishing a reference clock.</span></span>
-   <span data-ttu-id="05432-108">Comunicação de eventos de volta para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="05432-108">Communicating events back to the application.</span></span>
-   <span data-ttu-id="05432-109">Fornecer métodos para que os aplicativos criem o gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="05432-109">Providing methods for applications to build the filter graph.</span></span>

<span data-ttu-id="05432-110">Cada uma dessas funções é descrita brevemente aqui.</span><span class="sxs-lookup"><span data-stu-id="05432-110">Each of these functions is described briefly here.</span></span> <span data-ttu-id="05432-111">Os detalhes podem ser encontrados em outro lugar na documentação.</span><span class="sxs-lookup"><span data-stu-id="05432-111">Details can be found elsewhere in the documentation.</span></span>

<span data-ttu-id="05432-112">**Alterações de estado**.</span><span class="sxs-lookup"><span data-stu-id="05432-112">**State changes**.</span></span> <span data-ttu-id="05432-113">As alterações de estado dentro dos filtros devem ocorrer em uma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="05432-113">State changes within filters must occur in a particular order.</span></span> <span data-ttu-id="05432-114">Portanto, o aplicativo não emite comandos de alteração de estado diretamente para os filtros.</span><span class="sxs-lookup"><span data-stu-id="05432-114">Therefore, the application does not issue state-change commands directly to the filters.</span></span> <span data-ttu-id="05432-115">Em vez disso, ele fornece um único comando para o Gerenciador do grafo de filtro, que distribui o comando para cada um dos filtros.</span><span class="sxs-lookup"><span data-stu-id="05432-115">Instead, it gives a single command to the Filter Graph Manager, which distributes the command to each of the filters.</span></span> <span data-ttu-id="05432-116">Procurar funciona de maneira semelhante: o aplicativo fornece um comando de busca para o Gerenciador do grafo de filtro, que o distribui para os filtros.</span><span class="sxs-lookup"><span data-stu-id="05432-116">Seeking works in a similar fashion: The application gives a seek command to the Filter Graph Manager, which distributes it to the filters.</span></span>

<span data-ttu-id="05432-117">**Relógio de referência**.</span><span class="sxs-lookup"><span data-stu-id="05432-117">**Reference clock**.</span></span> <span data-ttu-id="05432-118">Todos os filtros no grafo usam o mesmo relógio, chamado de relógio de *referência*.</span><span class="sxs-lookup"><span data-stu-id="05432-118">All of the filters in the graph use the same clock, called a *reference clock*.</span></span> <span data-ttu-id="05432-119">O relógio de referência garante que todos os fluxos sejam sincronizados.</span><span class="sxs-lookup"><span data-stu-id="05432-119">The reference clock ensures that all the streams are synchronized.</span></span> <span data-ttu-id="05432-120">A hora em que um quadro de vídeo ou amostra de áudio deve ser renderizado é chamada de *tempo de apresentação*.</span><span class="sxs-lookup"><span data-stu-id="05432-120">The time at which a video frame or audio sample should be rendered is called the *presentation time*.</span></span> <span data-ttu-id="05432-121">O tempo de apresentação é medido em relação ao relógio de referência.</span><span class="sxs-lookup"><span data-stu-id="05432-121">The presentation time is measured relative to the reference clock.</span></span> <span data-ttu-id="05432-122">O Gerenciador de gráfico de filtro escolhe um relógio de referência, geralmente o relógio na placa de som ou o relógio do sistema.</span><span class="sxs-lookup"><span data-stu-id="05432-122">The Filter Graph Manager chooses a reference clock, usually either the clock on the sound card, or the system clock.</span></span>

<span data-ttu-id="05432-123">**Eventos de grafo**.</span><span class="sxs-lookup"><span data-stu-id="05432-123">**Graph events**.</span></span> <span data-ttu-id="05432-124">O Gerenciador de gráfico de filtro usa uma fila de eventos para informar a aplicação de eventos que ocorrem no grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="05432-124">The Filter Graph Manager uses an event queue to inform the application of events that occur in the filter graph.</span></span> <span data-ttu-id="05432-125">Esse mecanismo é semelhante a um loop de mensagem do Windows.</span><span class="sxs-lookup"><span data-stu-id="05432-125">This mechanism is similar to a Windows message loop.</span></span>

<span data-ttu-id="05432-126">**Métodos de criação de gráficos**.</span><span class="sxs-lookup"><span data-stu-id="05432-126">**Graph-building methods**.</span></span> <span data-ttu-id="05432-127">O Gerenciador de gráfico de filtro fornece métodos para que o aplicativo adicione filtros ao grafo, conecte filtros a outros filtros e desconecte filtros.</span><span class="sxs-lookup"><span data-stu-id="05432-127">The Filter Graph Manager provides methods for the application to add filters to the graph, connect filters to other filters, and disconnect filters.</span></span>

<span data-ttu-id="05432-128">Uma função que o Gerenciador de gráfico de filtro não trata é mover dados de um filtro para o próximo.</span><span class="sxs-lookup"><span data-stu-id="05432-128">One function the Filter Graph Manager does not handle is moving data from one filter to the next.</span></span> <span data-ttu-id="05432-129">Isso é feito pelos filtros em si, por meio de suas conexões de PIN.</span><span class="sxs-lookup"><span data-stu-id="05432-129">This is done by the filters themselves, through their pin connections.</span></span> <span data-ttu-id="05432-130">O processamento sempre acontece em um thread separado.</span><span class="sxs-lookup"><span data-stu-id="05432-130">Processing always happens on a separate thread.</span></span>

> [!Note]  
> <span data-ttu-id="05432-131">Os filtros são sempre de thread livre, residem no mesmo processo que o Gerenciador do grafo de filtro e são carregados de servidores em processo.</span><span class="sxs-lookup"><span data-stu-id="05432-131">Filters are always free-threaded, reside in the same process as the Filter Graph Manager, and are loaded from in-process servers.</span></span> <span data-ttu-id="05432-132">Portanto, as chamadas de método não são empacotadas entre filtros ou entre filtros e o Gerenciador de gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="05432-132">Therefore, method calls are not marshaled between filters, or between filters and the Filter Graph Manager.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="05432-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="05432-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05432-134">Fluxo de dados no grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="05432-134">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="05432-135">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="05432-135">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="05432-136">Configurando o relógio do grafo</span><span class="sxs-lookup"><span data-stu-id="05432-136">Setting the Graph Clock</span></span>](setting-the-graph-clock.md)
</dt> <dt>

[<span data-ttu-id="05432-137">Tempo e relógios no DirectShow</span><span class="sxs-lookup"><span data-stu-id="05432-137">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



