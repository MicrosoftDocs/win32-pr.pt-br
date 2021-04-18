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
# <a name="creating-source-nodes"></a>Criando nós de origem

Um nó de origem representa um fluxo de uma fonte de mídia. O nó de origem deve conter ponteiros para a origem de mídia, o descritor de apresentação e o descritor de fluxo.

Para adicionar um nó de origem a uma topologia, faça o seguinte:

1.  Chame [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) com o sinalizador de **\_ \_ \_ nó SOURCESTREAM de topologia MF** para criar o nó de origem.
2.  Defina o atributo de [**\_ \_ origem MF TOPONODE**](mf-toponode-source-attribute.md) no nó, com um ponteiro para a origem da mídia.
3.  Defina o atributo do [**\_ \_ \_ descritor de apresentação TOPONODE MF**](mf-toponode-presentation-descriptor-attribute.md) no nó, com um ponteiro para o descritor de apresentação da origem da mídia.
4.  Defina o atributo do [**\_ \_ \_ descritor de fluxo TOPONODE MF**](mf-toponode-stream-descriptor-attribute.md) no nó, com um ponteiro para o descritor de fluxo para o fluxo.
5.  Chame [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para adicionar o nó à topologia.

O exemplo a seguir cria e inicializa um nó de origem.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando topologias](creating-topologies.md)
</dt> <dt>

[Fontes de mídia](media-sources.md)
</dt> <dt>

[Topologias](topologies.md)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



