---
description: Introdução ao desenvolvimento de filtro do DirectShow
ms.assetid: d5162ea4-ef37-4993-a82c-782f03b08c64
title: Introdução ao desenvolvimento de filtro do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a42c5d2437b32f521b0efc39775f186267d3c99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105788081"
---
# <a name="introduction-to-directshow-filter-development"></a><span data-ttu-id="f88a2-103">Introdução ao desenvolvimento de filtro do DirectShow</span><span class="sxs-lookup"><span data-stu-id="f88a2-103">Introduction to DirectShow Filter Development</span></span>

<span data-ttu-id="f88a2-104">Esta seção fornece uma breve descrição das tarefas envolvidas no desenvolvimento de um filtro do DirectShow personalizado.</span><span class="sxs-lookup"><span data-stu-id="f88a2-104">This section gives a brief outline of the tasks involved in developing a custom DirectShow filter.</span></span> <span data-ttu-id="f88a2-105">Ele também fornece links para tópicos que discutem essas tarefas com mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="f88a2-105">It also provides links to topics that discuss these tasks in greater detail.</span></span> <span data-ttu-id="f88a2-106">Antes de ler esta seção, leia os tópicos em [sobre o DirectShow](about-directshow.md), que descrevem a arquitetura geral do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f88a2-106">Before reading this section, read the topics in [About DirectShow](about-directshow.md), which describe the overall DirectShow architecture.</span></span>

<span data-ttu-id="f88a2-107">**Biblioteca de classes base do DirectShow**</span><span class="sxs-lookup"><span data-stu-id="f88a2-107">**DirectShow Base Class Library**</span></span>

<span data-ttu-id="f88a2-108">O SDK do DirectShow inclui um conjunto de classes C++ para a gravação de filtros.</span><span class="sxs-lookup"><span data-stu-id="f88a2-108">The DirectShow SDK includes a set of C++ classes for writing filters.</span></span> <span data-ttu-id="f88a2-109">Embora não sejam necessárias, essas classes são a maneira recomendada para escrever um novo filtro.</span><span class="sxs-lookup"><span data-stu-id="f88a2-109">Although they are not required, these classes are the recommended way to write a new filter.</span></span> <span data-ttu-id="f88a2-110">Para usar as classes base, compile-as em uma biblioteca estática e vincule o arquivo. lib ao seu projeto, conforme descrito em [Criando filtros do DirectShow](building-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="f88a2-110">To use the base classes, compile them into a static library and link the .lib file to your project, as described in [Building DirectShow Filters](building-directshow-filters.md).</span></span>

<span data-ttu-id="f88a2-111">A biblioteca de classes base define uma classe raiz para filtros, a classe [**CBaseFilter**](cbasefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="f88a2-111">The base class library defines a root class for filters, the [**CBaseFilter**](cbasefilter.md) class.</span></span> <span data-ttu-id="f88a2-112">Várias outras classes derivam de **CBaseFilter** e são especializadas para determinados tipos de filtros.</span><span class="sxs-lookup"><span data-stu-id="f88a2-112">Several other classes derive from **CBaseFilter**, and are specialized for particular kinds of filters.</span></span> <span data-ttu-id="f88a2-113">Por exemplo, a classe [**CTransformFilter**](ctransformfilter.md) foi projetada para filtros de transformação.</span><span class="sxs-lookup"><span data-stu-id="f88a2-113">For example, the [**CTransformFilter**](ctransformfilter.md) class is designed for transform filters.</span></span> <span data-ttu-id="f88a2-114">Para criar um novo filtro, implemente uma classe que herde de uma das classes de filtro.</span><span class="sxs-lookup"><span data-stu-id="f88a2-114">To create a new filter, implement a class that inherits from one of the filter classes.</span></span> <span data-ttu-id="f88a2-115">Por exemplo, sua declaração de classe pode ser da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f88a2-115">For example, your class declaration might be as follows:</span></span>


```C++
class CMyFilter : public CTransformFilter
{
private:
    /* Declare variables and methods that are specific to your filter.
public:
    /* Override various methods in CTransformFilter */
};
```



<span data-ttu-id="f88a2-116">Para obter mais informações sobre as classes base do DirectShow, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="f88a2-116">For more information about the DirectShow base classes, see the following topics:</span></span>

-   [<span data-ttu-id="f88a2-117">Classes base do DirectShow</span><span class="sxs-lookup"><span data-stu-id="f88a2-117">DirectShow Base Classes</span></span>](directshow-base-classes.md)
-   [<span data-ttu-id="f88a2-118">Criando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="f88a2-118">Building DirectShow Filters</span></span>](building-directshow-filters.md)

<span data-ttu-id="f88a2-119">**Criando Pins**</span><span class="sxs-lookup"><span data-stu-id="f88a2-119">**Creating Pins**</span></span>

<span data-ttu-id="f88a2-120">Um filtro deve criar um ou mais Pins.</span><span class="sxs-lookup"><span data-stu-id="f88a2-120">A filter must create one or more pins.</span></span> <span data-ttu-id="f88a2-121">O número de Pins pode ser corrigido no tempo de design ou o filtro pode criar novos PINs, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="f88a2-121">The number of pins can be fixed at design time, or the filter can create new pins as needed.</span></span> <span data-ttu-id="f88a2-122">Os Pins geralmente derivam da classe [**CBasePin**](cbasepin.md) ou de uma classe que herda **CBasePin**, como [**CBaseInputPin**](cbaseinputpin.md).</span><span class="sxs-lookup"><span data-stu-id="f88a2-122">Pins generally derive from the [**CBasePin**](cbasepin.md) class, or from a class that inherits **CBasePin**, such as [**CBaseInputPin**](cbaseinputpin.md).</span></span> <span data-ttu-id="f88a2-123">Os Pins do filtro devem ser declarados como variáveis de membro na classe de filtro.</span><span class="sxs-lookup"><span data-stu-id="f88a2-123">The filter's pins should be declared as member variables in the filter class.</span></span> <span data-ttu-id="f88a2-124">Algumas das classes de filtro já definem os Pins, mas se o filtro herdar diretamente do **CBaseFilter**, você deverá declarar os Pins em sua classe derivada.</span><span class="sxs-lookup"><span data-stu-id="f88a2-124">Some of the filter classes already define the pins, but if your filter inherits directly from **CBaseFilter**, you must declare the pins in your derived class.</span></span>

<span data-ttu-id="f88a2-125">**Negociando conexões de PIN**</span><span class="sxs-lookup"><span data-stu-id="f88a2-125">**Negotiating Pin Connections**</span></span>

<span data-ttu-id="f88a2-126">Quando o Gerenciador de gráficos de filtro tenta conectar dois filtros, os Pins devem concordar com várias coisas.</span><span class="sxs-lookup"><span data-stu-id="f88a2-126">When the Filter Graph Manager tries to connect two filters, the pins must agree on various things.</span></span> <span data-ttu-id="f88a2-127">Se não puderem, a tentativa de conexão falhará.</span><span class="sxs-lookup"><span data-stu-id="f88a2-127">If they cannot, the connection attempt fails.</span></span> <span data-ttu-id="f88a2-128">Em geral, os Pins negociam o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f88a2-128">Generally, pins negotiate the following:</span></span>

-   <span data-ttu-id="f88a2-129">Transport:</span><span class="sxs-lookup"><span data-stu-id="f88a2-129">Transport.</span></span> <span data-ttu-id="f88a2-130">O transporte é o mecanismo que os filtros usarão para mover amostras de mídia do pino de saída para o pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="f88a2-130">The transport is the mechanism that the filters will use to move media samples from the output pin to the input pin.</span></span> <span data-ttu-id="f88a2-131">Por exemplo, eles podem usar a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ("modelo de push") ou a interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ("modelo de pull").</span><span class="sxs-lookup"><span data-stu-id="f88a2-131">For example, they can use the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface ("push model") or the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface ("pull model").</span></span>
-   <span data-ttu-id="f88a2-132">Tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="f88a2-132">Media type.</span></span> <span data-ttu-id="f88a2-133">Quase todos os Pins usam tipos de mídia para descrever o formato dos dados que eles fornecerão.</span><span class="sxs-lookup"><span data-stu-id="f88a2-133">Almost all pins use media types to describe the format of the data they will deliver.</span></span>
-   <span data-ttu-id="f88a2-134">Alocador.</span><span class="sxs-lookup"><span data-stu-id="f88a2-134">Allocator.</span></span> <span data-ttu-id="f88a2-135">O alocador é o objeto que cria os buffers que contêm os dados.</span><span class="sxs-lookup"><span data-stu-id="f88a2-135">The allocator is the object that creates the buffers that hold the data.</span></span> <span data-ttu-id="f88a2-136">Os Pins devem concordar com qual PIN fornecerá o alocador.</span><span class="sxs-lookup"><span data-stu-id="f88a2-136">The pins must agree which pin will provide the allocator.</span></span> <span data-ttu-id="f88a2-137">Eles também devem concordar com o tamanho dos buffers, o número de buffers a serem criados e outras propriedades de buffer.</span><span class="sxs-lookup"><span data-stu-id="f88a2-137">They must also agree on the size of the buffers, the number of buffers to create, and other buffer properties.</span></span>

<span data-ttu-id="f88a2-138">As classes base implementam uma estrutura para essas negociações.</span><span class="sxs-lookup"><span data-stu-id="f88a2-138">The base classes implement a framework for these negotiations.</span></span> <span data-ttu-id="f88a2-139">Você deve concluir os detalhes substituindo vários métodos na classe base.</span><span class="sxs-lookup"><span data-stu-id="f88a2-139">You must complete the details by overriding various methods in the base class.</span></span> <span data-ttu-id="f88a2-140">O conjunto de métodos que você deve substituir depende da classe e da funcionalidade do seu filtro.</span><span class="sxs-lookup"><span data-stu-id="f88a2-140">The set of methods that you must override depends on the class and on the functionality of your filter.</span></span> <span data-ttu-id="f88a2-141">Para obter mais informações, consulte [como os filtros se conectam](how-filters-connect.md).</span><span class="sxs-lookup"><span data-stu-id="f88a2-141">For more information, see [How Filters Connect](how-filters-connect.md).</span></span>

<span data-ttu-id="f88a2-142">**Processando e entregando dados**</span><span class="sxs-lookup"><span data-stu-id="f88a2-142">**Processing and Delivering Data**</span></span>

<span data-ttu-id="f88a2-143">A função principal da maioria dos filtros é processar e entregar dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="f88a2-143">The primary function of most filters is to process and deliver media data.</span></span> <span data-ttu-id="f88a2-144">Como isso ocorre depende do tipo de filtro:</span><span class="sxs-lookup"><span data-stu-id="f88a2-144">How that occurs depends on the type of filter:</span></span>

-   <span data-ttu-id="f88a2-145">Uma fonte Push tem um thread de trabalho que preenche continuamente os exemplos com os dados e os entrega.</span><span class="sxs-lookup"><span data-stu-id="f88a2-145">A push source has a worker thread that continuously fills samples with data and delivers them downstream.</span></span>
-   <span data-ttu-id="f88a2-146">Uma fonte de pull espera por seu vizinho downstream para solicitar um exemplo.</span><span class="sxs-lookup"><span data-stu-id="f88a2-146">A pull source waits for its downstream neighbor to request a sample.</span></span> <span data-ttu-id="f88a2-147">Ele responde gravando dados em um exemplo e entregando o exemplo ao filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="f88a2-147">It responds by writing data into a sample and delivering the sample to the downstream filter.</span></span> <span data-ttu-id="f88a2-148">O filtro downstream cria o thread que orienta o fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="f88a2-148">The downstream filter creates the thread that drives the data flow.</span></span>
-   <span data-ttu-id="f88a2-149">Um filtro de transformação tem exemplos entregues a ele pelo vizinho upstream.</span><span class="sxs-lookup"><span data-stu-id="f88a2-149">A transform filter has samples delivered to it by its upstream neighbor.</span></span> <span data-ttu-id="f88a2-150">Quando recebe um exemplo, ele processa os dados e os entrega por downstream.</span><span class="sxs-lookup"><span data-stu-id="f88a2-150">When it receives a sample, it processes the data and delivers it downstream.</span></span>
-   <span data-ttu-id="f88a2-151">Um filtro de renderizador recebe amostras de upstream e os agenda para renderização com base nos carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="f88a2-151">A renderer filter receives samples from upstream, and schedules them for rendering based on the time stamps.</span></span>

<span data-ttu-id="f88a2-152">Outras tarefas relacionadas ao streaming incluem a liberação de dados do grafo, o tratamento do fim do fluxo e a resposta a solicitações de busca.</span><span class="sxs-lookup"><span data-stu-id="f88a2-152">Other tasks related to streaming include flushing data from the graph, handling the end of the stream, and responding to seek requests.</span></span> <span data-ttu-id="f88a2-153">Para obter mais informações sobre esses problemas, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="f88a2-153">For more information about these issues, see the following topics:</span></span>

-   [<span data-ttu-id="f88a2-154">Fluxo de dados para os desenvolvedores de filtro</span><span class="sxs-lookup"><span data-stu-id="f88a2-154">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
-   [<span data-ttu-id="f88a2-155">Gerenciamento de controle de qualidade</span><span class="sxs-lookup"><span data-stu-id="f88a2-155">Quality-Control Management</span></span>](quality-control-management.md)
-   [<span data-ttu-id="f88a2-156">Threads e seções críticas</span><span class="sxs-lookup"><span data-stu-id="f88a2-156">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)

<span data-ttu-id="f88a2-157">**COM suporte a**</span><span class="sxs-lookup"><span data-stu-id="f88a2-157">**Supporting COM**</span></span>

<span data-ttu-id="f88a2-158">Os filtros do DirectShow são objetos COM, normalmente empacotados em DLLs.</span><span class="sxs-lookup"><span data-stu-id="f88a2-158">DirectShow filters are COM objects, typically packaged in DLLs.</span></span> <span data-ttu-id="f88a2-159">A biblioteca de classes base implementa uma estrutura para dar suporte a COM.</span><span class="sxs-lookup"><span data-stu-id="f88a2-159">The base class library implements a framework for supporting COM.</span></span> <span data-ttu-id="f88a2-160">Ele é descrito na seção [DirectShow e com](directshow-and-com.md).</span><span class="sxs-lookup"><span data-stu-id="f88a2-160">It is described in the section [DirectShow and COM](directshow-and-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f88a2-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f88a2-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f88a2-162">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="f88a2-162">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



