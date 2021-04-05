---
description: Criando nós de saída
ms.assetid: 6e548f2a-77cd-460e-9ffd-c098f6ee75eb
title: Criando nós de saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4388258c82c12f8473dc07df83ba3b9467eed7e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826737"
---
# <a name="creating-output-nodes"></a><span data-ttu-id="a84dc-103">Criando nós de saída</span><span class="sxs-lookup"><span data-stu-id="a84dc-103">Creating Output Nodes</span></span>

<span data-ttu-id="a84dc-104">Um nó de saída representa um coletor de fluxo em um coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="a84dc-104">An output node represents a stream sink on a media sink.</span></span> <span data-ttu-id="a84dc-105">Há duas maneiras de inicializar um nó de saída:</span><span class="sxs-lookup"><span data-stu-id="a84dc-105">There are two ways to initialize an output node:</span></span>

-   <span data-ttu-id="a84dc-106">De um ponteiro para o coletor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="a84dc-106">From a pointer to the stream sink.</span></span>
-   <span data-ttu-id="a84dc-107">De um ponteiro para um objeto de ativação para o coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="a84dc-107">From a pointer to an activation object for the media sink.</span></span>

<span data-ttu-id="a84dc-108">Se você pretende carregar a topologia dentro do caminho de mídia protegido (PMP), deve usar um objeto de ativação para que o coletor de mídia possa ser criado dentro do processo protegido.</span><span class="sxs-lookup"><span data-stu-id="a84dc-108">If you are going to load the topology inside the protected media path (PMP), you must use an activation object, so that the media sink can be created inside the protected process.</span></span> <span data-ttu-id="a84dc-109">A primeira abordagem (usando um ponteiro para o coletor de fluxo) não funciona com o PMP.</span><span class="sxs-lookup"><span data-stu-id="a84dc-109">The first approach (using a pointer to the stream sink) does not work with the PMP.</span></span>

## <a name="creating-an-output-node-from-a-stream-sink"></a><span data-ttu-id="a84dc-110">Criando um nó de saída de um coletor de fluxo</span><span class="sxs-lookup"><span data-stu-id="a84dc-110">Creating an Output Node from a Stream Sink</span></span>

<span data-ttu-id="a84dc-111">Para criar um nó de saída de um coletor de fluxo, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a84dc-111">To create an output node from a stream sink, do the following:</span></span>

1.  <span data-ttu-id="a84dc-112">Crie uma instância do coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="a84dc-112">Create an instance of the media sink.</span></span>
2.  <span data-ttu-id="a84dc-113">Use a interface [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) do coletor de mídia para obter um ponteiro para o coletor de fluxo desejado.</span><span class="sxs-lookup"><span data-stu-id="a84dc-113">Use the media sink's [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface to get a pointer to the desired stream sink.</span></span> <span data-ttu-id="a84dc-114">(A interface **IMFMediaSink** tem vários métodos que retornam ponteiros para um coletor de fluxo.)</span><span class="sxs-lookup"><span data-stu-id="a84dc-114">(The **IMFMediaSink** interface has several methods that return pointers to a stream sink.)</span></span>
3.  <span data-ttu-id="a84dc-115">Chame [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) com o sinalizador de **\_ nó de \_ saída \_ da topologia MF** para criar o nó de saída.</span><span class="sxs-lookup"><span data-stu-id="a84dc-115">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_OUTPUT\_NODE** flag to create the output node.</span></span>
4.  <span data-ttu-id="a84dc-116">Chame [**IMFTopologyNode:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) e transmita um ponteiro para a interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) do coletor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="a84dc-116">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in a pointer to the stream sink's [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span>
5.  <span data-ttu-id="a84dc-117">Defina o [**\_ TOPONODE MF \_ parashutdown \_ no atributo \_ Remove**](mf-toponode-noshutdown-on-remove-attribute.md) como **false** (opcional, mas recomendado).</span><span class="sxs-lookup"><span data-stu-id="a84dc-117">Set the [**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) attribute to **FALSE** (optional but recommended).</span></span>
6.  <span data-ttu-id="a84dc-118">Chame [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para adicionar o nó à topologia.</span><span class="sxs-lookup"><span data-stu-id="a84dc-118">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="a84dc-119">O exemplo a seguir cria e inicializa um nó de saída de um coletor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="a84dc-119">The following example creates and initializes an output node from a stream sink.</span></span>


```C++
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFStreamSink *pStreamSink, // Stream sink.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    IMFTopologyNode *pNode = NULL;
    HRESULT hr = S_OK;
    
    // Create the node.
    hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pStreamSink);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    if (SUCCEEDED(hr))
    {
        hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, TRUE);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    if (pNode)
    {
        pNode->Release();
    }
    return hr;
}
```



<span data-ttu-id="a84dc-120">Quando o aplicativo desliga a sessão de mídia, a sessão de mídia desliga automaticamente o coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="a84dc-120">When the application shuts down the Media Session, the Media Session automatically shuts down the media sink.</span></span> <span data-ttu-id="a84dc-121">Portanto, você não pode usar novamente o coletor de mídia com outra instância da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="a84dc-121">Therefore, you cannot re-use the media sink with another instance of the Media Session.</span></span>

## <a name="creating-an-output-node-from-an-activation-object"></a><span data-ttu-id="a84dc-122">Criando um nó de saída de um objeto de ativação</span><span class="sxs-lookup"><span data-stu-id="a84dc-122">Creating an Output Node from an Activation Object</span></span>

<span data-ttu-id="a84dc-123">Qualquer coletor de mídia confiável deve fornecer um objeto de ativação, para que o coletor de mídia possa ser criado dentro do processo protegido.</span><span class="sxs-lookup"><span data-stu-id="a84dc-123">Any trusted media sink must provide an activation object, so that the media sink can be created inside the protected process.</span></span> <span data-ttu-id="a84dc-124">Para obter mais informações, consulte [objetos de ativação](activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a84dc-124">For more information, see [Activation Objects](activation-objects.md).</span></span> <span data-ttu-id="a84dc-125">A função específica que cria o objeto de ativação dependerá do coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="a84dc-125">The particular function that creates the activation object will depend on the media sink.</span></span>

<span data-ttu-id="a84dc-126">Para criar um nó de saída de um objeto de ativação, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a84dc-126">To create an output node from an activation object, do the following:</span></span>

1.  <span data-ttu-id="a84dc-127">Crie o objeto de ativação e obtenha um ponteiro para a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) do objeto de ativação.</span><span class="sxs-lookup"><span data-stu-id="a84dc-127">Create the activation object and get a pointer to the activation object's [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
2.  <span data-ttu-id="a84dc-128">Chame [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) com o sinalizador de **\_ nó de \_ saída \_ da topologia MF** para criar o nó de saída.</span><span class="sxs-lookup"><span data-stu-id="a84dc-128">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_OUTPUT\_NODE** flag to create the output node.</span></span>
3.  <span data-ttu-id="a84dc-129">Opcionalmente, defina o atributo [**MF \_ TOPONODE \_ streamid**](mf-toponode-streamid-attribute.md) no nó para especificar o identificador de fluxo do coletor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="a84dc-129">Optionally, set the [**MF\_TOPONODE\_STREAMID**](mf-toponode-streamid-attribute.md) attribute on the node to specify the stream identifier of the stream sink.</span></span> <span data-ttu-id="a84dc-130">Se você omitir esse atributo, o nó usará como padrão o coletor de fluxo 0.</span><span class="sxs-lookup"><span data-stu-id="a84dc-130">If you omit this attribute, the node defaults to using stream sink 0.</span></span>
4.  <span data-ttu-id="a84dc-131">Defina o [**\_ TOPONODE MF \_ parashutdown \_ no atributo \_ Remove**](mf-toponode-noshutdown-on-remove-attribute.md) como **true** (opcional, mas recomendado).</span><span class="sxs-lookup"><span data-stu-id="a84dc-131">Set the [**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) attribute to **TRUE** (optional but recommended).</span></span>
5.  <span data-ttu-id="a84dc-132">Chame [**IMFTopologyNode:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) e passe o ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="a84dc-132">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>
6.  <span data-ttu-id="a84dc-133">Chame [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para adicionar o nó à topologia.</span><span class="sxs-lookup"><span data-stu-id="a84dc-133">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="a84dc-134">O exemplo a seguir cria e inicializa um nó de saída de um objeto de ativação.</span><span class="sxs-lookup"><span data-stu-id="a84dc-134">The following example creates and initializes an output node from an activation object.</span></span>


```C++
// Add an output node to a topology.
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // Media sink activation object.
    DWORD dwId,                 // Identifier of the stream sink.
    IMFTopologyNode **ppNode)   // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the object pointer.
    hr = pNode->SetObject(pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the stream sink ID attribute.
    hr = pNode->SetUINT32(MF_TOPONODE_STREAMID, dwId);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, FALSE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="a84dc-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a84dc-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a84dc-136">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="a84dc-136">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="a84dc-137">Criando topologias</span><span class="sxs-lookup"><span data-stu-id="a84dc-137">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="a84dc-138">Coletores de mídia</span><span class="sxs-lookup"><span data-stu-id="a84dc-138">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="a84dc-139">Topologias</span><span class="sxs-lookup"><span data-stu-id="a84dc-139">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



