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
# <a name="creating-transform-nodes"></a>Criando nós de transformação

Um nó de transformação representa uma Media Foundation transformação (MFT), como um decodificador ou um codificador. Há várias maneiras diferentes de inicializar um nó de transformação:

-   De um ponteiro para o MFT.
-   De um CLSID para o MFT.
-   De um ponteiro para um objeto de ativação para o MFT.

Se você pretende carregar a topologia dentro do caminho de mídia protegido (PMP), você deve usar o CLSID ou um objeto de ativação, para que o MFT possa ser criado dentro do processo protegido. A primeira abordagem (usando um ponteiro para o MFT) não funciona com o PMP.

## <a name="creating-a-transform-node-from-an-mft"></a>Criando um nó de transformação de um MFT

Para criar um nó de transformação de um MFT, faça o seguinte:

1.  Crie uma instância do MFT e obtenha um ponteiro para a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) do MFT.
2.  Chame [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) com o sinalizador de **\_ nó de \_ transformação \_ de topologia MF** para criar o nó de transformação.
3.  Chame [**IMFTopologyNode:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) e passe o ponteiro [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .
4.  Chame [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para adicionar o nó à topologia.

O exemplo a seguir cria e inicializa um nó de transformação de um MFT.


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



## <a name="creating-a-transform-node-from-a-clsid"></a>Criando um nó de transformação de um CLSID

Para criar um nó de transformação de um CLSID, faça o seguinte:

1.  Localize o CLSID do MFT. Você pode usar a função [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) para localizar os CLSIDs de MFTs por categoria, como decodificadores ou codificadores. Você também pode saber o CLSID de uma determinada MFT que deseja usar (por exemplo, se você implementou sua própria MFT personalizada).
2.  Chame [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) com o sinalizador de **\_ nó de \_ transformação \_ de topologia MF** para criar o nó de transformação.
3.  Defina o **atributo \_ \_ \_ messageobjectid do TOPONODE de transformação MF** no nó. O valor do atributo é o CLSID.
4.  Chame [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para adicionar o nó à topologia.

O exemplo a seguir cria e inicializa um nó de transformação de um CLSID.


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



## <a name="creating-a-transform-node-from-an-activation-object"></a>Criando um nó de transformação a partir de um objeto de ativação

Alguns MFTs fornecem objetos de ativação. Por exemplo, a função [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) retorna um objeto de ativação para o codificador de áudio do Windows Media (WMA). A função exata depende do MFT. Nem todo MFT fornece um objeto de ativação. Para obter mais informações, consulte [objetos de ativação](activation-objects.md).

Você também pode obter um objeto de ativação de MFT chamando a função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

Para criar um nó de transformação a partir de um objeto de ativação, faça o seguinte:

1.  Crie o objeto de ativação e obtenha um ponteiro para a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) do objeto de ativação.
2.  Chame [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) com o sinalizador de **\_ nó de \_ transformação \_ de topologia MF** para criar o nó de transformação.
3.  Chame [**IMFTopologyNode:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) e passe o ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .
4.  Chame [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) para adicionar o nó à topologia.

O exemplo a seguir cria e inicializa um nó de transformação de um objeto de ativação.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando topologias](creating-topologies.md)
</dt> <dt>

[Topologias](topologies.md)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



