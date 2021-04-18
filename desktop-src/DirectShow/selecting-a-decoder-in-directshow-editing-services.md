---
description: Selecionando um decodificador nos serviços de edição do DirectShow
ms.assetid: dc6b0445-7fc1-4331-9000-a652b44a8364
title: Selecionando um decodificador nos serviços de edição do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956ad0284722eb394590b1b0065f167c55b3cf51
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456572"
---
# <a name="selecting-a-decoder-in-directshow-editing-services"></a><span data-ttu-id="de04a-103">Selecionando um decodificador nos serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="de04a-103">Selecting a Decoder in DirectShow Editing Services</span></span>

<span data-ttu-id="de04a-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="de04a-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="de04a-105">Quando os [serviços de edição do DirectShow](directshow-editing-services.md) (des) renderizam um projeto de edição de vídeo, o mecanismo de renderização seleciona automaticamente os decodificadores necessários.</span><span class="sxs-lookup"><span data-stu-id="de04a-105">When [DirectShow Editing Services](directshow-editing-services.md) (DES) renders a video editing project, the Rendering Engine automatically selects the necessary decoders.</span></span> <span data-ttu-id="de04a-106">Isso pode acontecer dentro do método [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) ou, mais dinamicamente, durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="de04a-106">This may happen inside the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method, or else dynamically during rendering.</span></span>

<span data-ttu-id="de04a-107">Um usuário pode instalar vários decodificadores que são capazes de decodificar um arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="de04a-107">A user might install several decoders that are capable of decoding a particular file.</span></span> <span data-ttu-id="de04a-108">Quando vários decodificadores estão disponíveis, o DES usa o algoritmo de [conexão inteligente](intelligent-connect.md) para selecionar o decodificador.</span><span class="sxs-lookup"><span data-stu-id="de04a-108">When multiple decoders are available, DES uses the [Intelligent Connect](intelligent-connect.md) algorithm to select the decoder.</span></span>

<span data-ttu-id="de04a-109">Não há como o aplicativo especificar diretamente qual decodificador usar.</span><span class="sxs-lookup"><span data-stu-id="de04a-109">There is no way for the application to specify directly which decoder to use.</span></span> <span data-ttu-id="de04a-110">No entanto, você pode escolher o decodificador indiretamente por meio da interface de retorno de chamada [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) .</span><span class="sxs-lookup"><span data-stu-id="de04a-110">However, you can choose the decoder indirectly through the [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) callback interface.</span></span> <span data-ttu-id="de04a-111">Ao implementar essa interface em seu aplicativo, você pode receber notificações durante o processo de criação de grafo e rejeitar determinados filtros do grafo.</span><span class="sxs-lookup"><span data-stu-id="de04a-111">By implementing this interface in your application, you can receive notifications during the graph-building process and reject certain filters from the graph.</span></span>

<span data-ttu-id="de04a-112">Comece implementando uma classe que expõe a interface [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) :</span><span class="sxs-lookup"><span data-stu-id="de04a-112">Start by implementing a class that exposes the [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) interface:</span></span>


```C++
class GraphBuilderCB : public IAMGraphBuilderCallback
{
public:
     // Method declarations (not shown).
};
```



<span data-ttu-id="de04a-113">Em seguida, crie uma instância do Gerenciador do grafo de filtro e registre sua classe para receber notificações de retorno de chamada:</span><span class="sxs-lookup"><span data-stu-id="de04a-113">Then create an instance of the Filter Graph Manager and register your class to receive callback notifications:</span></span>


```C++
// Declare an instance of the callback object.
GraphBuilderCB GraphCB; 

// Create the Filter Graph Manager.
CComPtr<IGraphBuilder> pGraph;
hr = pGraph.CoCreateInstance(CLSID_FilterGraph);
if (FAILED(hr))
{
    // Handle error (not shown).
}
// Register to receive the callbacks.
CComQIPtr<IObjectWithSite> pSite(pGraph);
if (pSite)
{
    hr = pSite->SetSite((IUnknown*)&GraphCB);
}
```



<span data-ttu-id="de04a-114">Em seguida, crie o mecanismo de renderização e chame o método [**IRenderEngine:: SetFilterGraph**](irenderengine-setfiltergraph.md) com um ponteiro para o Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="de04a-114">Next, create the Render Engine and call the [**IRenderEngine::SetFilterGraph**](irenderengine-setfiltergraph.md) method with a pointer to the Filter Graph Manager.</span></span> <span data-ttu-id="de04a-115">Isso garante que o mecanismo de renderização não crie seu próprio Gerenciador de gráfico de filtro, mas, em vez disso, usa a instância que você configurou para retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="de04a-115">This ensures that the Render Engine does not create its own Filter Graph Manager, but instead uses the instance that you have configured for callbacks.</span></span>


```C++
CComPtr<IRenderEngine> pRender;
hr = pRender.CoCreateInstance(CLSID_RenderEngine);
if (FAILED(hr))
{
    // Handle error (not shown).
}

hr = pRender->SetFilterGraph(pGraph);
```



<span data-ttu-id="de04a-116">Quando o projeto é renderizado, o método [**IAMGraphBuilderCallback:: SelectedFilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) do aplicativo é chamado imediatamente antes de o Gerenciador de gráfico de filtro criar um novo filtro.</span><span class="sxs-lookup"><span data-stu-id="de04a-116">When the project is rendered, the application's [**IAMGraphBuilderCallback::SelectedFilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) method is called immediately before the Filter Graph Manager creates a new filter.</span></span> <span data-ttu-id="de04a-117">O método **SelectedFilter** recebe um ponteiro para uma interface **IMoniker** que representa um moniker para o filtro.</span><span class="sxs-lookup"><span data-stu-id="de04a-117">The **SelectedFilter** method receives a pointer to an **IMoniker** interface that represents a moniker for the filter.</span></span> <span data-ttu-id="de04a-118">Examine o moniker e, se você decidir rejeitar o filtro, retorne um código de falha do método **SelectedFilter** .</span><span class="sxs-lookup"><span data-stu-id="de04a-118">Examine the moniker, and if you decide to reject the filter, return a failure code from the **SelectedFilter** method.</span></span>

<span data-ttu-id="de04a-119">A parte difícil é identificar quais monikers representam decodificadores — e, em particular, quais monikers representam os decodificadores que você deseja rejeitar.</span><span class="sxs-lookup"><span data-stu-id="de04a-119">The difficult part is to identify which monikers represent decoders — and in particular, which monikers represent decoders that you want to reject.</span></span> <span data-ttu-id="de04a-120">Uma solução é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="de04a-120">One solution is the following:</span></span>

-   <span data-ttu-id="de04a-121">Antes de renderizar o projeto, use o método [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) para criar uma lista de filtros que são registrados como aceitando o tipo de entrada desejado.</span><span class="sxs-lookup"><span data-stu-id="de04a-121">Before rendering the project, use the [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method to create a list of filters that are registered as accepting the desired input type.</span></span> <span data-ttu-id="de04a-122">Para tipos de compactação de vídeo ou áudio, essa lista deve ser mapeada para um conjunto de decodificadores.</span><span class="sxs-lookup"><span data-stu-id="de04a-122">For video or audio compression types, this list should map to a set of decoders.</span></span>
-   <span data-ttu-id="de04a-123">O método **EnumMatchingFilters** retorna uma coleção de monikers.</span><span class="sxs-lookup"><span data-stu-id="de04a-123">The **EnumMatchingFilters** method returns a collection of monikers.</span></span> <span data-ttu-id="de04a-124">Para cada moniker na coleção, obtenha a propriedade **DisplayName** , conforme descrito em [usando o mapeador de filtro](using-the-filter-mapper.md).</span><span class="sxs-lookup"><span data-stu-id="de04a-124">For each moniker in the collection, get the **DisplayName** property, as described in [Using the Filter Mapper](using-the-filter-mapper.md).</span></span>
-   <span data-ttu-id="de04a-125">Armazene uma lista dos nomes de exibição, mas omita o nome de exibição que corresponde ao filtro que você deseja usar para decodificação.</span><span class="sxs-lookup"><span data-stu-id="de04a-125">Store a list of the display names, but omit the display name that matches the filter you want to use for decoding.</span></span> <span data-ttu-id="de04a-126">Os nomes de exibição dos filtros de software têm o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="de04a-126">Display names for software filters have the following form:</span></span>

    ```C++
    OLESTR("@device:sw:{CategoryGUID}\{FilterCLSID}");
    ```

    

    <span data-ttu-id="de04a-127">onde</span><span class="sxs-lookup"><span data-stu-id="de04a-127">where</span></span>

    ```C++
    CategoryGUID
    ```

    

    <span data-ttu-id="de04a-128">é o GUID da categoria de filtro e</span><span class="sxs-lookup"><span data-stu-id="de04a-128">is the GUID of the filter category, and</span></span>

    ```C++
    FilterCLSID
    ```

    

    <span data-ttu-id="de04a-129">é o CLSID do filtro.</span><span class="sxs-lookup"><span data-stu-id="de04a-129">is the filter's CLSID.</span></span> <span data-ttu-id="de04a-130">Para DMOs, o formato é o mesmo, mas é alterado `sw` para `dmo` .</span><span class="sxs-lookup"><span data-stu-id="de04a-130">For DMOs, the format is the same, but change `sw` to `dmo`.</span></span>

    <span data-ttu-id="de04a-131">Agora, a lista contém nomes de exibição para cada filtro que gera o tipo de mídia desejado, mas não é seu filtro preferido.</span><span class="sxs-lookup"><span data-stu-id="de04a-131">The list now contains display names for every filter that outputs the desired media type but is not your preferred filter.</span></span>

-   <span data-ttu-id="de04a-132">No método **SelectedFilter** , obtenha a propriedade **DisplayName** no moniker proposto e verifique-a na lista armazenada.</span><span class="sxs-lookup"><span data-stu-id="de04a-132">In the **SelectedFilter** method, get the **DisplayName** property on the proposed moniker and check it against the stored list.</span></span> <span data-ttu-id="de04a-133">Se o nome de exibição corresponder a uma entrada na lista, rejeite esse filtro.</span><span class="sxs-lookup"><span data-stu-id="de04a-133">If the display name matches an entry in the list, reject that filter.</span></span> <span data-ttu-id="de04a-134">Caso contrário, aceite-o retornando S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="de04a-134">Otherwise, accept it by returning S\_OK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de04a-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="de04a-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de04a-136">Renderizando um projeto</span><span class="sxs-lookup"><span data-stu-id="de04a-136">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



