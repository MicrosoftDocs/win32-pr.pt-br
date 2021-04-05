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
# <a name="creating-output-nodes"></a>Criando nós de saída

Um nó de saída representa um coletor de fluxo em um coletor de mídia. Há duas maneiras de inicializar um nó de saída:

-   De um ponteiro para o coletor de fluxo.
-   De um ponteiro para um objeto de ativação para o coletor de mídia.

Se você pretende carregar a topologia dentro do caminho de mídia protegido (PMP), deve usar um objeto de ativação para que o coletor de mídia possa ser criado dentro do processo protegido. A primeira abordagem (usando um ponteiro para o coletor de fluxo) não funciona com o PMP.

## <a name="creating-an-output-node-from-a-stream-sink"></a>Criando um nó de saída de um coletor de fluxo

Para criar um nó de saída de um coletor de fluxo, faça o seguinte:

1.  Crie uma instância do coletor de mídia.
2.  Use a interface [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) do coletor de mídia para obter um ponteiro para o coletor de fluxo desejado. (A interface **IMFMediaSink** tem vários métodos que retornam ponteiros para um coletor de fluxo.)
3.  Chame [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) com o sinalizador de **\_ nó de \_ saída \_ da topologia MF** para criar o nó de saída.
4.  Chame [**IMFTopologyNode:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) e transmita um ponteiro para a interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) do coletor de fluxo.
5.  Defina o [**\_ TOPONODE MF \_ parashutdown \_ no atributo \_ Remove**](mf-toponode-noshutdown-on-remove-attribute.md) como **false** (opcional, mas recomendado).
6.  Chame [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para adicionar o nó à topologia.

O exemplo a seguir cria e inicializa um nó de saída de um coletor de fluxo.


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



Quando o aplicativo desliga a sessão de mídia, a sessão de mídia desliga automaticamente o coletor de mídia. Portanto, você não pode usar novamente o coletor de mídia com outra instância da sessão de mídia.

## <a name="creating-an-output-node-from-an-activation-object"></a>Criando um nó de saída de um objeto de ativação

Qualquer coletor de mídia confiável deve fornecer um objeto de ativação, para que o coletor de mídia possa ser criado dentro do processo protegido. Para obter mais informações, consulte [objetos de ativação](activation-objects.md). A função específica que cria o objeto de ativação dependerá do coletor de mídia.

Para criar um nó de saída de um objeto de ativação, faça o seguinte:

1.  Crie o objeto de ativação e obtenha um ponteiro para a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) do objeto de ativação.
2.  Chame [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) com o sinalizador de **\_ nó de \_ saída \_ da topologia MF** para criar o nó de saída.
3.  Opcionalmente, defina o atributo [**MF \_ TOPONODE \_ streamid**](mf-toponode-streamid-attribute.md) no nó para especificar o identificador de fluxo do coletor de fluxo. Se você omitir esse atributo, o nó usará como padrão o coletor de fluxo 0.
4.  Defina o [**\_ TOPONODE MF \_ parashutdown \_ no atributo \_ Remove**](mf-toponode-noshutdown-on-remove-attribute.md) como **true** (opcional, mas recomendado).
5.  Chame [**IMFTopologyNode:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) e passe o ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .
6.  Chame [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para adicionar o nó à topologia.

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

[Coletores de mídia](media-sinks.md)
</dt> <dt>

[Topologias](topologies.md)
</dt> </dl>

 

 



