---
description: Criando nós de transformação
ms.assetid: d70a3c2b-2f0e-4e29-9a8f-84a50d9f1682
title: Criando nós de transformação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f39eed9f49e10501fadc00f47b57cf95705a7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501190"
---
# <a name="creating-transform-nodes"></a><span data-ttu-id="a8f16-103">Criando nós de transformação</span><span class="sxs-lookup"><span data-stu-id="a8f16-103">Creating Transform Nodes</span></span>

<span data-ttu-id="a8f16-104">Um nó de transformação representa uma Media Foundation transformação (MFT), como um decodificador ou um codificador.</span><span class="sxs-lookup"><span data-stu-id="a8f16-104">A transform node represents a Media Foundation transform (MFT), such as a decoder or encoder.</span></span> <span data-ttu-id="a8f16-105">Há várias maneiras diferentes de inicializar um nó de transformação:</span><span class="sxs-lookup"><span data-stu-id="a8f16-105">There are several different ways to initialize a transform node:</span></span>

-   <span data-ttu-id="a8f16-106">De um ponteiro para o MFT.</span><span class="sxs-lookup"><span data-stu-id="a8f16-106">From a pointer to the MFT.</span></span>
-   <span data-ttu-id="a8f16-107">De um CLSID para o MFT.</span><span class="sxs-lookup"><span data-stu-id="a8f16-107">From a CLSID for the MFT.</span></span>
-   <span data-ttu-id="a8f16-108">De um ponteiro para um objeto de ativação para o MFT.</span><span class="sxs-lookup"><span data-stu-id="a8f16-108">From a pointer to an activation object for the MFT.</span></span>

<span data-ttu-id="a8f16-109">Se você pretende carregar a topologia dentro do caminho de mídia protegido (PMP), você deve usar o CLSID ou um objeto de ativação, para que o MFT possa ser criado dentro do processo protegido.</span><span class="sxs-lookup"><span data-stu-id="a8f16-109">If you are going to load the topology inside the protected media path (PMP), you must use either the CLSID or an activation object, so that the MFT can be created inside the protected process.</span></span> <span data-ttu-id="a8f16-110">A primeira abordagem (usando um ponteiro para o MFT) não funciona com o PMP.</span><span class="sxs-lookup"><span data-stu-id="a8f16-110">The first approach (using a pointer to the MFT) does not work with the PMP.</span></span>

## <a name="creating-a-transform-node-from-an-mft"></a><span data-ttu-id="a8f16-111">Criando um nó de transformação de um MFT</span><span class="sxs-lookup"><span data-stu-id="a8f16-111">Creating a Transform Node from an MFT</span></span>

<span data-ttu-id="a8f16-112">Para criar um nó de transformação de um MFT, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a8f16-112">To create a transform node from an MFT, do the following:</span></span>

1.  <span data-ttu-id="a8f16-113">Crie uma instância do MFT e obtenha um ponteiro para a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) do MFT.</span><span class="sxs-lookup"><span data-stu-id="a8f16-113">Create an instance of the MFT and get a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface of the MFT.</span></span>
2.  <span data-ttu-id="a8f16-114">Chame [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) com o sinalizador de **\_ nó de \_ transformação \_ de topologia MF** para criar o nó de transformação.</span><span class="sxs-lookup"><span data-stu-id="a8f16-114">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="a8f16-115">Chame [**IMFTopologyNode:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) e passe o ponteiro [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="a8f16-115">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointer.</span></span>
4.  <span data-ttu-id="a8f16-116">Chame [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para adicionar o nó à topologia.</span><span class="sxs-lookup"><span data-stu-id="a8f16-116">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="a8f16-117">O exemplo a seguir cria e inicializa um nó de transformação de um MFT.</span><span class="sxs-lookup"><span data-stu-id="a8f16-117">The following example creates and initializes a transform node from an MFT.</span></span>


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    IMFTransform *pMFT,         // MFT.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pMFT);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="creating-a-transform-node-from-a-clsid"></a><span data-ttu-id="a8f16-118">Criando um nó de transformação de um CLSID</span><span class="sxs-lookup"><span data-stu-id="a8f16-118">Creating a Transform Node from a CLSID</span></span>

<span data-ttu-id="a8f16-119">Para criar um nó de transformação de um CLSID, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a8f16-119">To create a transform node from a CLSID, do the following:</span></span>

1.  <span data-ttu-id="a8f16-120">Localize o CLSID do MFT.</span><span class="sxs-lookup"><span data-stu-id="a8f16-120">Find the CLSID of the MFT.</span></span> <span data-ttu-id="a8f16-121">Você pode usar a função [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) para localizar os CLSIDs de MFTs por categoria, como decodificadores ou codificadores.</span><span class="sxs-lookup"><span data-stu-id="a8f16-121">You can use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function to find the CLSIDs of MFTs by category, such as decoders or encoders.</span></span> <span data-ttu-id="a8f16-122">Você também pode saber o CLSID de uma determinada MFT que deseja usar (por exemplo, se você implementou sua própria MFT personalizada).</span><span class="sxs-lookup"><span data-stu-id="a8f16-122">You might also know the CLSID of a particular MFT that you want to use (for example, if you implemented your own custom MFT).</span></span>
2.  <span data-ttu-id="a8f16-123">Chame [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) com o sinalizador de **\_ nó de \_ transformação \_ de topologia MF** para criar o nó de transformação.</span><span class="sxs-lookup"><span data-stu-id="a8f16-123">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="a8f16-124">Defina o **atributo \_ \_ \_ messageobjectid do TOPONODE de transformação MF** no nó.</span><span class="sxs-lookup"><span data-stu-id="a8f16-124">Set the **MF\_TOPONODE\_TRANSFORM\_OBJECTID** attribute on the node.</span></span> <span data-ttu-id="a8f16-125">O valor do atributo é o CLSID.</span><span class="sxs-lookup"><span data-stu-id="a8f16-125">The attribute value is the CLSID.</span></span>
4.  <span data-ttu-id="a8f16-126">Chame [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para adicionar o nó à topologia.</span><span class="sxs-lookup"><span data-stu-id="a8f16-126">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="a8f16-127">O exemplo a seguir cria e inicializa um nó de transformação de um CLSID.</span><span class="sxs-lookup"><span data-stu-id="a8f16-127">The following example creates and initializes a transform node from a CLSID.</span></span>


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    const CLSID& clsid,         // CLSID of the MFT.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the CLSID attribute.

    if (SUCCEEDED(hr))
    {
        hr = pNode->SetGUID(MF_TOPONODE_TRANSFORM_OBJECTID, clsid);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="creating-a-transform-node-from-an-activation-object"></a><span data-ttu-id="a8f16-128">Criando um nó de transformação a partir de um objeto de ativação</span><span class="sxs-lookup"><span data-stu-id="a8f16-128">Creating a Transform Node from an Activation Object</span></span>

<span data-ttu-id="a8f16-129">Alguns MFTs fornecem objetos de ativação.</span><span class="sxs-lookup"><span data-stu-id="a8f16-129">Some MFTs provide activation objects.</span></span> <span data-ttu-id="a8f16-130">Por exemplo, a função [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) retorna um objeto de ativação para o codificador de áudio do Windows Media (WMA).</span><span class="sxs-lookup"><span data-stu-id="a8f16-130">For example, the [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) function returns an activation object for the Windows Media Audio (WMA) encoder.</span></span> <span data-ttu-id="a8f16-131">A função exata depende do MFT.</span><span class="sxs-lookup"><span data-stu-id="a8f16-131">The exact function depends on the MFT.</span></span> <span data-ttu-id="a8f16-132">Nem todo MFT fornece um objeto de ativação.</span><span class="sxs-lookup"><span data-stu-id="a8f16-132">Not every MFT provides an activation object.</span></span> <span data-ttu-id="a8f16-133">Para obter mais informações, consulte [objetos de ativação](activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a8f16-133">For more information, see [Activation Objects](activation-objects.md).</span></span>

<span data-ttu-id="a8f16-134">Você também pode obter um objeto de ativação de MFT chamando a função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="a8f16-134">You can also get an MFT activation object by calling the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="a8f16-135">Para criar um nó de transformação a partir de um objeto de ativação, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a8f16-135">To create a transform node from an activation object, do the following:</span></span>

1.  <span data-ttu-id="a8f16-136">Crie o objeto de ativação e obtenha um ponteiro para a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) do objeto de ativação.</span><span class="sxs-lookup"><span data-stu-id="a8f16-136">Create the activation object and get a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface of the activation object.</span></span>
2.  <span data-ttu-id="a8f16-137">Chame [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) com o sinalizador de **\_ nó de \_ transformação \_ de topologia MF** para criar o nó de transformação.</span><span class="sxs-lookup"><span data-stu-id="a8f16-137">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="a8f16-138">Chame [**IMFTopologyNode:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) e passe o ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="a8f16-138">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>
4.  <span data-ttu-id="a8f16-139">Chame [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para adicionar o nó à topologia.</span><span class="sxs-lookup"><span data-stu-id="a8f16-139">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="a8f16-140">O exemplo a seguir cria e inicializa um nó de transformação de um objeto de ativação.</span><span class="sxs-lookup"><span data-stu-id="a8f16-140">The following example creates and initializes a transform node from an activation object.</span></span>


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // MFT activation object.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pActivate);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="a8f16-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a8f16-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8f16-142">Criando topologias</span><span class="sxs-lookup"><span data-stu-id="a8f16-142">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="a8f16-143">Topologias</span><span class="sxs-lookup"><span data-stu-id="a8f16-143">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="a8f16-144">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="a8f16-144">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



