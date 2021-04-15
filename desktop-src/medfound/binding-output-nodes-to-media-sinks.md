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
# <a name="binding-output-nodes-to-media-sinks"></a>Associando nós de saída a coletores de mídia

Este tópico descreve como inicializar os nós de saída em uma topologia, se você estiver usando o carregador de topologia fora da sessão de mídia. Um nó de saída inicialmente contém um dos seguintes:

-   Um ponteiro [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .
-   Um ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .

No último caso, o ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) deve ser convertido em um ponteiro [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) antes que o carregador de topologia resolva a topologia. Na maioria dos cenários, o processo funciona da seguinte maneira:

1.  O aplicativo enfileira uma topologia parcial na sessão de mídia.
2.  Para todos os nós de saída, a sessão de mídia converte ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) em ponteiros [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) . Esse processo é chamado de *Associação* do nó de saída a um coletor de mídia.
3.  A sessão de mídia envia a topologia modificada para o método [**IMFTopoLoader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) .

No entanto, se você estiver usando o carregador de topologia diretamente (fora da mídia sessão), seu aplicativo deverá associar os nós de saída antes de chamar [**IMFTopoLoader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load). Para associar um nó de saída, faça o seguinte:

1.  Chame [**IMFTopologyNode:: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) para obter o ponteiro de objeto do nó.
2.  Consulte o ponteiro do objeto para a interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) . Se essa chamada for bem sucedido, não há nada mais a fazer, então ignore as etapas restantes.
3.  Se a etapa anterior tiver falhado, consulte o ponteiro do objeto para a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .
4.  Crie o coletor de mídia chamando [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). Especifique **o \_ IMFMediaSink de IID** para obter um ponteiro para a interface [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) do coletor de mídia.
5.  Consulte o nó para o atributo [**MF \_ TOPONODE \_ streamid**](mf-toponode-streamid-attribute.md) . O valor desse atributo é o identificador do coletor de fluxo para este nó. Se o atributo **MF \_ TOPONODE \_ streamid** não estiver definido, o identificador de fluxo padrão será zero.
6.  O coletor de fluxo apropriado já pode existir no coletor de mídia. Para verificar, chame [**IMFMediaSink:: GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) no coletor de mídia. Se o coletor de fluxo existir, o método retornará um ponteiro para sua interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) . Se essa chamada falhar, tente adicionar um novo coletor de fluxo chamando [**IMFMediaSink:: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink). Se ambas as chamadas falharem, isso significa que o coletor de mídia não oferece suporte ao identificador de fluxo solicitado e esse nó de topologia não está configurado corretamente. Retorne um código de erro e pule a próxima etapa.
7.  Chame [**IMFTopologyNode:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject), passando o ponteiro [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) da etapa anterior. Essa chamada substitui o ponteiro de objeto do nó, para que o nó contenha um ponteiro para o coletor de fluxo, em vez de um ponteiro para o objeto de ativação.

O código a seguir mostra como associar um nó de saída.


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
> Este exemplo usa a função [SafeRelease](saferelease.md) para liberar ponteiros de interface.

 

O exemplo a seguir mostra como associar todos os nós de saída em uma topologia. Este exemplo usa o método [**IMFTopology:: GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) para obter uma coleção de nós de saída da topologia. Em seguida, ele chama a função mostrada no exemplo anterior em cada um desses nós por vez.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criação de topologia avançada](advanced-topology-building.md)
</dt> <dt>

[Coletores de mídia](media-sinks.md)
</dt> <dt>

[**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)
</dt> </dl>

 

 



