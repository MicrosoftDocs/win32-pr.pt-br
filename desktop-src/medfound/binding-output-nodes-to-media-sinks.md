---
description: Associando nós de saída a coletores de mídia
ms.assetid: d4f93f34-0af1-431f-9333-70ea09691b64
title: Associando nós de saída a coletores de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cbea075badf74ac9e0e9354d82f4100a6167a0c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104506336"
---
# <a name="binding-output-nodes-to-media-sinks"></a><span data-ttu-id="ca73a-103">Associando nós de saída a coletores de mídia</span><span class="sxs-lookup"><span data-stu-id="ca73a-103">Binding Output Nodes to Media Sinks</span></span>

<span data-ttu-id="ca73a-104">Este tópico descreve como inicializar os nós de saída em uma topologia, se você estiver usando o carregador de topologia fora da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="ca73a-104">This topic describes how to initialize the output nodes in a topology, if you are using the topology loader outside of the Media Session.</span></span> <span data-ttu-id="ca73a-105">Um nó de saída inicialmente contém um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="ca73a-105">An output node initially contains one of the following:</span></span>

-   <span data-ttu-id="ca73a-106">Um ponteiro [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .</span><span class="sxs-lookup"><span data-stu-id="ca73a-106">An [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer.</span></span>
-   <span data-ttu-id="ca73a-107">Um ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="ca73a-107">An [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>

<span data-ttu-id="ca73a-108">No último caso, o ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) deve ser convertido em um ponteiro [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) antes que o carregador de topologia resolva a topologia.</span><span class="sxs-lookup"><span data-stu-id="ca73a-108">In the latter case, the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer must be converted to an [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer before the topology loader resolves the topology.</span></span> <span data-ttu-id="ca73a-109">Na maioria dos cenários, o processo funciona da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ca73a-109">In most scenarios, the process works as follows:</span></span>

1.  <span data-ttu-id="ca73a-110">O aplicativo enfileira uma topologia parcial na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="ca73a-110">The application queues a partial topology on the Media Session.</span></span>
2.  <span data-ttu-id="ca73a-111">Para todos os nós de saída, a sessão de mídia converte ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) em ponteiros [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .</span><span class="sxs-lookup"><span data-stu-id="ca73a-111">For all output nodes, the Media Session converts [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers to [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointers.</span></span> <span data-ttu-id="ca73a-112">Esse processo é chamado de *Associação* do nó de saída a um coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="ca73a-112">This process is called *binding* the output node to a media sink.</span></span>
3.  <span data-ttu-id="ca73a-113">A sessão de mídia envia a topologia modificada para o método [**IMFTopoLoader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) .</span><span class="sxs-lookup"><span data-stu-id="ca73a-113">The Media Session sends the modified topology to the [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method.</span></span>

<span data-ttu-id="ca73a-114">No entanto, se você estiver usando o carregador de topologia diretamente (fora da mídia sessão), seu aplicativo deverá associar os nós de saída antes de chamar [**IMFTopoLoader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load).</span><span class="sxs-lookup"><span data-stu-id="ca73a-114">However, if you are using the topology loader directly (outside of the media sesssion), your application must bind the output nodes prior to calling [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load).</span></span> <span data-ttu-id="ca73a-115">Para associar um nó de saída, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ca73a-115">To bind an output node, do the following:</span></span>

1.  <span data-ttu-id="ca73a-116">Chame [**IMFTopologyNode:: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) para obter o ponteiro de objeto do nó.</span><span class="sxs-lookup"><span data-stu-id="ca73a-116">Call [**IMFTopologyNode::GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) to get the node's object pointer.</span></span>
2.  <span data-ttu-id="ca73a-117">Consulte o ponteiro do objeto para a interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .</span><span class="sxs-lookup"><span data-stu-id="ca73a-117">Query the object pointer for the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span> <span data-ttu-id="ca73a-118">Se essa chamada for bem sucedido, não há nada mais a fazer, então ignore as etapas restantes.</span><span class="sxs-lookup"><span data-stu-id="ca73a-118">If this call succeeds, there is nothing more to do, so skip the remaining steps.</span></span>
3.  <span data-ttu-id="ca73a-119">Se a etapa anterior tiver falhado, consulte o ponteiro do objeto para a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="ca73a-119">If the previous step failed, query the object pointer for the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
4.  <span data-ttu-id="ca73a-120">Crie o coletor de mídia chamando [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="ca73a-120">Create the media sink by calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> <span data-ttu-id="ca73a-121">Especifique **o \_ IMFMediaSink de IID** para obter um ponteiro para a interface [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) do coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="ca73a-121">Specify **IID\_IMFMediaSink** to get a pointer to the media sink's [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface.</span></span>
5.  <span data-ttu-id="ca73a-122">Consulte o nó para o atributo [**MF \_ TOPONODE \_ streamid**](mf-toponode-streamid-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="ca73a-122">Query the node for the [**MF\_TOPONODE\_STREAMID**](mf-toponode-streamid-attribute.md) attribute.</span></span> <span data-ttu-id="ca73a-123">O valor desse atributo é o identificador do coletor de fluxo para este nó.</span><span class="sxs-lookup"><span data-stu-id="ca73a-123">The value of this attribute is the identifier of the stream sink for this node.</span></span> <span data-ttu-id="ca73a-124">Se o atributo **MF \_ TOPONODE \_ streamid** não estiver definido, o identificador de fluxo padrão será zero.</span><span class="sxs-lookup"><span data-stu-id="ca73a-124">If the **MF\_TOPONODE\_STREAMID** attribute is not set, the default stream identifier is zero.</span></span>
6.  <span data-ttu-id="ca73a-125">O coletor de fluxo apropriado já pode existir no coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="ca73a-125">The appropriate stream sink might already exist on the media sink.</span></span> <span data-ttu-id="ca73a-126">Para verificar, chame [**IMFMediaSink:: GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) no coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="ca73a-126">To check, call [**IMFMediaSink::GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) on the media sink.</span></span> <span data-ttu-id="ca73a-127">Se o coletor de fluxo existir, o método retornará um ponteiro para sua interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .</span><span class="sxs-lookup"><span data-stu-id="ca73a-127">If the stream sink exists, the method returns a pointer to its [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span> <span data-ttu-id="ca73a-128">Se essa chamada falhar, tente adicionar um novo coletor de fluxo chamando [**IMFMediaSink:: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span><span class="sxs-lookup"><span data-stu-id="ca73a-128">If this call fails, try to add a new stream sink by calling [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span></span> <span data-ttu-id="ca73a-129">Se ambas as chamadas falharem, isso significa que o coletor de mídia não oferece suporte ao identificador de fluxo solicitado e esse nó de topologia não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="ca73a-129">If both calls fail, it means the media sink does not support the requested stream identifier, and this topology node is not configured correctly.</span></span> <span data-ttu-id="ca73a-130">Retorne um código de erro e pule a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="ca73a-130">Return an error code and skip the next step.</span></span>
7.  <span data-ttu-id="ca73a-131">Chame [**IMFTopologyNode:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject), passando o ponteiro [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) da etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="ca73a-131">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject), passing in the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer from the previous step.</span></span> <span data-ttu-id="ca73a-132">Essa chamada substitui o ponteiro de objeto do nó, para que o nó contenha um ponteiro para o coletor de fluxo, em vez de um ponteiro para o objeto de ativação.</span><span class="sxs-lookup"><span data-stu-id="ca73a-132">This call replaces the node's object pointer, so that the node contains a pointer to the stream sink, instead of a pointer to the activation object.</span></span>

<span data-ttu-id="ca73a-133">O código a seguir mostra como associar um nó de saída.</span><span class="sxs-lookup"><span data-stu-id="ca73a-133">The following code shows how to bind an output node.</span></span>


```C++
// BindOutputNode
// Sets the IMFStreamSink pointer on an output node.

HRESULT BindOutputNode(IMFTopologyNode *pNode)
{
    IUnknown *pNodeObject = NULL;
    IMFActivate *pActivate = NULL;
    IMFStreamSink *pStream = NULL;
    IMFMediaSink *pSink = NULL;

    // Get the node's object pointer.
    HRESULT hr = pNode->GetObject(&pNodeObject);
    if (FAILED(hr))
    {
        return hr;
    }

    // The object pointer should be one of the following:
    // 1. An activation object for the media sink.
    // 2. The stream sink.

    // If it's #2, then we're already done.

    // First, check if it's an activation object.
    hr = pNodeObject->QueryInterface(IID_PPV_ARGS(&pActivate));

    if (SUCCEEDED(hr))
    {
        DWORD dwStreamID = 0;

        // The object pointer is an activation object. 
        
        // Try to create the media sink.
        hr = pActivate->ActivateObject(IID_PPV_ARGS(&pSink));

        // Look up the stream ID. (Default to zero.)

        if (SUCCEEDED(hr))
        {
           dwStreamID = MFGetAttributeUINT32(pNode, MF_TOPONODE_STREAMID, 0);
        }

        // Now try to get or create the stream sink.

        // Check if the media sink already has a stream sink with the requested ID.

        if (SUCCEEDED(hr))
        {
            hr = pSink->GetStreamSinkById(dwStreamID, &pStream);
            if (FAILED(hr))
            {
                // Try to add a new stream sink.
                hr = pSink->AddStreamSink(dwStreamID, NULL, &pStream);
            }
        }

        // Replace the node's object pointer with the stream sink. 
        if (SUCCEEDED(hr))
        {
            hr = pNode->SetObject(pStream);
        }
    }
    else
    {
        // Not an activation object. Is it a stream sink?
        hr = pNodeObject->QueryInterface(IID_PPV_ARGS(&pStream));
    }

    SafeRelease(&pNodeObject);
    SafeRelease(&pActivate);
    SafeRelease(&pStream);
    SafeRelease(&pSink);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="ca73a-134">Este exemplo usa a função [SafeRelease](saferelease.md) para liberar ponteiros de interface.</span><span class="sxs-lookup"><span data-stu-id="ca73a-134">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

<span data-ttu-id="ca73a-135">O exemplo a seguir mostra como associar todos os nós de saída em uma topologia.</span><span class="sxs-lookup"><span data-stu-id="ca73a-135">The next example shows how to bind all of the output nodes in a topology.</span></span> <span data-ttu-id="ca73a-136">Este exemplo usa o método [**IMFTopology:: GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) para obter uma coleção de nós de saída da topologia.</span><span class="sxs-lookup"><span data-stu-id="ca73a-136">This example uses the [**IMFTopology::GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) method to get a collection of output nodes from the topology.</span></span> <span data-ttu-id="ca73a-137">Em seguida, ele chama a função mostrada no exemplo anterior em cada um desses nós por vez.</span><span class="sxs-lookup"><span data-stu-id="ca73a-137">Then it calls the function shown in the previous example on each of those nodes in turn.</span></span>


```C++
// BindOutputNodes
// Sets the IMFStreamSink pointers on all of the output nodes in a topology.

HRESULT BindOutputNodes(IMFTopology *pTopology)
{
    DWORD cNodes = 0;

    IMFCollection *pCol = NULL;
    IUnknown *pUnk = NULL;
    IMFTopologyNode *pNode = NULL;

    // Get the collection of output nodes. 
    HRESULT hr = pTopology->GetOutputNodeCollection(&pCol);
    
    // Enumerate all of the nodes in the collection.
    if (SUCCEEDED(hr))
    {
        hr = pCol->GetElementCount(&cNodes);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cNodes; i++)
        {
            hr = pCol->GetElement(i, &pUnk);

            if (FAILED(hr)) { break; }

            hr = pUnk->QueryInterface(IID_IMFTopologyNode, (void**)&pNode);

            if (FAILED(hr)) { break; }

            // Bind this node.
            hr = BindOutputNode(pNode);

            if (FAILED(hr)) { break; }
        }
    }

    SafeRelease(&pCol);
    SafeRelease(&pUnk);
    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="ca73a-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ca73a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca73a-139">Criação de topologia avançada</span><span class="sxs-lookup"><span data-stu-id="ca73a-139">Advanced Topology Building</span></span>](advanced-topology-building.md)
</dt> <dt>

[<span data-ttu-id="ca73a-140">Coletores de mídia</span><span class="sxs-lookup"><span data-stu-id="ca73a-140">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="ca73a-141">**IMFTopoLoader**</span><span class="sxs-lookup"><span data-stu-id="ca73a-141">**IMFTopoLoader**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)
</dt> </dl>

 

 



