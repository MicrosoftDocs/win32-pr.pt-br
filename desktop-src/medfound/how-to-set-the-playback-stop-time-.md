---
description: Este tópico descreve como definir uma hora de parada para reprodução ao usar a sessão de mídia.
ms.assetid: B8BA2154-2824-4573-AE71-853EB8AB911D
title: Como definir a hora de parada da reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c14145f798795dfeb8116195afad2f020eb4219b9c2529f96b8fa904f2e1d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465996"
---
# <a name="how-to-set-the-playback-stop-time"></a>Como definir a hora de parada da reprodução

Este tópico descreve como definir uma hora de parada para reprodução ao usar a [sessão de mídia](media-session.md).

## <a name="setting-the-stop-time-before-playback-begins"></a>Definir o tempo de parada antes da reprodução começar

Antes de colocar uma topologia em fila para reprodução, você pode especificar a hora de parada usando o atributo [MF \_ TOPONODE \_ MEDIASTOP](mf-toponode-mediastop-attribute.md) . Para cada nó de saída na topologia, defina o valor de TOPONODE MF \_ \_ MEDIASTOP como a hora de parada em unidades de 100 nanossegundos.

Observe que a definição desse atributo após o início da reprodução não tem nenhum efeito. Portanto, defina o atributo antes de chamar [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).

O código a seguir mostra como definir a hora de parada em uma topologia existente.


```C++
template <class Q>
HRESULT GetCollectionObject(IMFCollection *pCollection, DWORD dwIndex, Q **ppObject)
{
    *ppObject = NULL;   // zero output

    IUnknown *pUnk = NULL;
    HRESULT hr = pCollection->GetElement(dwIndex, &pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_PPV_ARGS(ppObject));
        pUnk->Release();
    }
    return hr;
}

HRESULT SetMediaStop(IMFTopology *pTopology, const LONGLONG& stop)
{
    IMFCollection *pCol = NULL;
    DWORD cNodes;

    HRESULT hr = pTopology->GetSourceNodeCollection(&pCol);
    if (SUCCEEDED(hr))
    {
        hr = pCol->GetElementCount(&cNodes);
    }
    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cNodes; i++)
        {
            IMFTopologyNode *pNode;
            hr = GetCollectionObject(pCol, i, &pNode);
            if (SUCCEEDED(hr))
            {
                pNode->SetUINT64(MF_TOPONODE_MEDIASTOP, stop);
            }
            pNode->Release();
        }
    }
    SafeRelease(&pCol);
    return hr;
}
```



## <a name="setting-the-stop-time-after-playback-has-started"></a>Definindo a hora de parada após a reprodução ser iniciada

Há uma maneira de definir o tempo de parada após a [sessão de mídia](media-session.md) iniciar a reprodução, usando a interface [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) .

> [!IMPORTANT]
> Essa interface tem uma limitação séria, pois a hora de parada é especificada como um valor de 32 bits. Isso significa que o tempo máximo de parada que você pode definir usando essa interface é de 0xFFFFFFFF, ou apenas mais de 7 minutos. Essa limitação é devido a uma definição de estrutura incorreta.

 

Para definir a hora de parada usando a interface [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) , execute as etapas a seguir.

1.  Chame [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obter a interface [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) da sessão de mídia.
2.  Chame [**IMFTopology:: Gettopologiaid**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) para obter a ID da topologia de reprodução.
3.  Para cada nó de saída na topologia, chame [**IMFTopologyNodeAttributeEditor:: UpdateNodeAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes). Esse método usa a ID de topologia e um ponteiro para uma estrutura de [**\_ \_ atualização de atributo MFTOPONODE**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) . Inicialize a estrutura da seguinte maneira.

    | Membro               | Valor                                                                                                               |
    |----------------------|---------------------------------------------------------------------------------------------------------------------|
    | **NodeId**           | A ID do nó. Para obter a ID do nó, chame Call [**IMFTopologyNode:: GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid). |
    | **guidAttributeKey** | **\_TOPONODE MF \_ MEDIASTOP**                                                                                         |
    | **attrType**         | **\_Atributo MF \_ UINT64**                                                                                           |
    | **u64**              | A hora de parada, em unidades de 100 a nanossegundos.                                                                             |

    

     

Tenha cuidado para definir o valor de **attrType** corretamente. Embora **u64** seja um tipo de 32 bits, o método requer que **attrType** seja definido como **o \_ atributo MF \_ UINT64**.

O código a seguir mostra essas etapas.


```C++
HRESULT SetMediaStopDynamic(IMFMediaSession *pSession, IMFTopology *pTopology, const LONGLONG& stop)
{
    if (stop > MAXUINT32)
    {
        return E_INVALIDARG;
    }

    IMFTopologyNodeAttributeEditor *pAttr = NULL;
    IMFCollection *pCol = NULL;
    IMFTopologyNode *pNode = NULL;

    HRESULT hr = MFGetService(pSession, MF_TOPONODE_ATTRIBUTE_EDITOR_SERVICE, IID_PPV_ARGS(&pAttr));
    if (FAILED(hr))
    {
        goto done;
    }

    TOPOID id;
    hr = pTopology->GetTopologyID(&id);
    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cNodes;
    hr = pTopology->GetSourceNodeCollection(&pCol);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pCol->GetElementCount(&cNodes);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cNodes; i++)
    {
        IMFTopologyNode *pNode;
        hr = GetCollectionObject(pCol, i, &pNode);
        if (FAILED(hr))
        {
            goto done;
        }

        TOPOID nodeID;
        hr = pNode->GetTopoNodeID(&nodeID);
        if (FAILED(hr))
        {
            goto done;
        }

        MFTOPONODE_ATTRIBUTE_UPDATE update;
        update.NodeId = nodeID;
        update.guidAttributeKey = MF_TOPONODE_MEDIASTOP;
        update.attrType = MF_ATTRIBUTE_UINT64;
        update.u64 = (UINT32)stop;

        hr = pAttr->UpdateNodeAttributes(id, 1, &update);
        if (FAILED(hr))
        {
            goto done;
        }
        SafeRelease(&pNode);
    }

done:
    SafeRelease(&pNode);
    SafeRelease(&pCol);
    SafeRelease(&pAttr);
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo](audio-video-playback.md)
</dt> </dl>

 

 



