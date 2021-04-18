---
description: Criando nós de origem
ms.assetid: 44c26bcd-04a9-48c3-b536-25c2b18c34c1
title: Criando nós de origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b1e882dd6f8e9345244b56eace332c2fad4bc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814073"
---
# <a name="creating-source-nodes"></a><span data-ttu-id="17263-103">Criando nós de origem</span><span class="sxs-lookup"><span data-stu-id="17263-103">Creating Source Nodes</span></span>

<span data-ttu-id="17263-104">Um nó de origem representa um fluxo de uma fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="17263-104">A source node represents one stream from a media source.</span></span> <span data-ttu-id="17263-105">O nó de origem deve conter ponteiros para a origem de mídia, o descritor de apresentação e o descritor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="17263-105">The source node must contain pointers to the media source, the presentation descriptor, and the stream descriptor.</span></span>

<span data-ttu-id="17263-106">Para adicionar um nó de origem a uma topologia, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="17263-106">To add a source node to a topology, do the following:</span></span>

1.  <span data-ttu-id="17263-107">Chame [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) com o sinalizador de **\_ \_ \_ nó SOURCESTREAM de topologia MF** para criar o nó de origem.</span><span class="sxs-lookup"><span data-stu-id="17263-107">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_SOURCESTREAM\_NODE** flag to create the source node.</span></span>
2.  <span data-ttu-id="17263-108">Defina o atributo de [**\_ \_ origem MF TOPONODE**](mf-toponode-source-attribute.md) no nó, com um ponteiro para a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="17263-108">Set the [**MF\_TOPONODE\_SOURCE**](mf-toponode-source-attribute.md) attribute on the node, with a pointer to the media source.</span></span>
3.  <span data-ttu-id="17263-109">Defina o atributo do [**\_ \_ \_ descritor de apresentação TOPONODE MF**](mf-toponode-presentation-descriptor-attribute.md) no nó, com um ponteiro para o descritor de apresentação da origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="17263-109">Set the [**MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR**](mf-toponode-presentation-descriptor-attribute.md) attribute on the node, with a pointer to the presentation descriptor of the media source.</span></span>
4.  <span data-ttu-id="17263-110">Defina o atributo do [**\_ \_ \_ descritor de fluxo TOPONODE MF**](mf-toponode-stream-descriptor-attribute.md) no nó, com um ponteiro para o descritor de fluxo para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="17263-110">Set the [**MF\_TOPONODE\_STREAM\_DESCRIPTOR**](mf-toponode-stream-descriptor-attribute.md) attribute on the node, with a pointer to the stream descriptor for the stream.</span></span>
5.  <span data-ttu-id="17263-111">Chame [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para adicionar o nó à topologia.</span><span class="sxs-lookup"><span data-stu-id="17263-111">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="17263-112">O exemplo a seguir cria e inicializa um nó de origem.</span><span class="sxs-lookup"><span data-stu-id="17263-112">The following example creates and initializes a source node.</span></span>


```C++
// Add a source node to a topology.
HRESULT AddSourceNode(
    IMFTopology *pTopology,           // Topology.
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    IMFStreamDescriptor *pSD,         // Stream descriptor.
    IMFTopologyNode **ppNode)         // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_SOURCESTREAM_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the attributes.
    hr = pNode->SetUnknown(MF_TOPONODE_SOURCE, pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_STREAM_DESCRIPTOR, pSD);
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



## <a name="related-topics"></a><span data-ttu-id="17263-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="17263-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17263-114">Criando topologias</span><span class="sxs-lookup"><span data-stu-id="17263-114">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="17263-115">Fontes de mídia</span><span class="sxs-lookup"><span data-stu-id="17263-115">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="17263-116">Topologias</span><span class="sxs-lookup"><span data-stu-id="17263-116">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="17263-117">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="17263-117">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



