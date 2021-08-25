---
description: Criando nós de saída
ms.assetid: 6e548f2a-77cd-460e-9ffd-c098f6ee75eb
title: Criando nós de saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6af2842458fb360374d34583b15bfbf5005b2f2bbdd8b32332bc6756ca4e8157
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943016"
---
# <a name="creating-output-nodes"></a>Criando nós de saída

Um nó de saída representa um sink de fluxo em um sink de mídia. Há duas maneiras de inicializar um nó de saída:

-   De um ponteiro para o sink de fluxo.
-   De um ponteiro para um objeto de ativação para o sink de mídia.

Se você for carregar a topologia dentro do caminho de mídia protegido (PMP), deverá usar um objeto de ativação para que o sink de mídia possa ser criado dentro do processo protegido. A primeira abordagem (usando um ponteiro para o sink de fluxo) não funciona com o PMP.

## <a name="creating-an-output-node-from-a-stream-sink"></a>Criando um nó de saída de um sink de fluxo

Para criar um nó de saída de um sink de fluxo, faça o seguinte:

1.  Crie uma instância do sink de mídia.
2.  Use a interface [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) do sink de mídia para obter um ponteiro para o sink de fluxo desejado. (A interface **IMFMediaSink** tem vários métodos que retornam ponteiros para um sink de fluxo.)
3.  Chame [**MFCreateTopologyNode com o**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) sinalizador **MF \_ TOPOLOGY OUTPUT \_ \_ NODE** para criar o nó de saída.
4.  Chame [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) e passe um ponteiro para a interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) do fluxo.
5.  De definir [**o \_ atributo MF TOPNODE \_ NOSHUTDOWN \_ ON \_ REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) **como FALSE** (opcional, mas recomendado).
6.  Chame [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para adicionar o nó à topologia.

O exemplo a seguir cria e inicializa um nó de saída de um sink de fluxo.


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



Quando o aplicativo desliga a Sessão de Mídia, a Sessão de Mídia desliga automaticamente o sink de mídia. Portanto, você não pode usar o sink de mídia com outra instância da Sessão de Mídia.

## <a name="creating-an-output-node-from-an-activation-object"></a>Criando um nó de saída de um objeto de ativação

Qualquer sink de mídia confiável deve fornecer um objeto de ativação para que o sink de mídia possa ser criado dentro do processo protegido. Para obter mais informações, consulte [Objetos de ativação](activation-objects.md). A função específica que cria o objeto de ativação dependerá do sink de mídia.

Para criar um nó de saída de um objeto de ativação, faça o seguinte:

1.  Crie o objeto de ativação e receba um ponteiro para a interface [**IMFActivate do**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) objeto de ativação.
2.  Chame [**MFCreateTopologyNode com o**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) sinalizador **MF \_ TOPOLOGY OUTPUT \_ \_ NODE** para criar o nó de saída.
3.  Opcionalmente, de definir [**o atributo \_ STREAMID TOPONODE \_ MF**](mf-toponode-streamid-attribute.md) no nó para especificar o identificador de fluxo do sink de fluxo. Se você omitir esse atributo, o nó assume como padrão o uso do sink 0 do fluxo.
4.  De acordo [**com o \_ atributo \_ NOSHUTDOWN \_ ON \_ REMOVE do MF TOPNODE COMO**](mf-toponode-noshutdown-on-remove-attribute.md) **TRUE** (opcional, mas recomendado).
5.  Chame [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) e passe o [**ponteiro IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
6.  Chame [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para adicionar o nó à topologia.

O exemplo a seguir cria e inicializa um nó de saída de um objeto de ativação.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Criando topologias](creating-topologies.md)
</dt> <dt>

[Sinks de mídia](media-sinks.md)
</dt> <dt>

[Topologias](topologies.md)
</dt> </dl>

 

 



