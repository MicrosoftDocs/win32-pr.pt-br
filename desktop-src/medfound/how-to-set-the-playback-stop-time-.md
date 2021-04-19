---
description: Este tópico descreve como definir uma hora de parada para reprodução ao usar a sessão de mídia.
ms.assetid: B8BA2154-2824-4573-AE71-853EB8AB911D
title: Como definir a hora de parada da reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65269260b1e40d7907f0233fad653deb9636848b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771488"
---
# <a name="how-to-set-the-playback-stop-time"></a><span data-ttu-id="51cd0-103">Como definir a hora de parada da reprodução</span><span class="sxs-lookup"><span data-stu-id="51cd0-103">How to Set the Playback Stop Time</span></span>

<span data-ttu-id="51cd0-104">Este tópico descreve como definir uma hora de parada para reprodução ao usar a [sessão de mídia](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="51cd0-104">This topic describes how to set a stop time for playback when using the [Media Session](media-session.md).</span></span>

## <a name="setting-the-stop-time-before-playback-begins"></a><span data-ttu-id="51cd0-105">Definir o tempo de parada antes da reprodução começar</span><span class="sxs-lookup"><span data-stu-id="51cd0-105">Setting the Stop Time Before Playback Begins</span></span>

<span data-ttu-id="51cd0-106">Antes de colocar uma topologia em fila para reprodução, você pode especificar a hora de parada usando o atributo [MF \_ TOPONODE \_ MEDIASTOP](mf-toponode-mediastop-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="51cd0-106">Before you queue a topology for playback, you can specify the stop time by using the [MF\_TOPONODE\_MEDIASTOP](mf-toponode-mediastop-attribute.md) attribute.</span></span> <span data-ttu-id="51cd0-107">Para cada nó de saída na topologia, defina o valor de TOPONODE MF \_ \_ MEDIASTOP como a hora de parada em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="51cd0-107">For each output node in the topology, set the value of the MF\_TOPONODE\_MEDIASTOP to the stop time in 100-nanosecond units.</span></span>

<span data-ttu-id="51cd0-108">Observe que a definição desse atributo após o início da reprodução não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="51cd0-108">Note that setting this attribute after playback starts has no effect.</span></span> <span data-ttu-id="51cd0-109">Portanto, defina o atributo antes de chamar [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="51cd0-109">Therefore, set the attribute before calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>

<span data-ttu-id="51cd0-110">O código a seguir mostra como definir a hora de parada em uma topologia existente.</span><span class="sxs-lookup"><span data-stu-id="51cd0-110">The following code shows how to set the stop time on an existing topology.</span></span>


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



## <a name="setting-the-stop-time-after-playback-has-started"></a><span data-ttu-id="51cd0-111">Definindo a hora de parada após a reprodução ser iniciada</span><span class="sxs-lookup"><span data-stu-id="51cd0-111">Setting the Stop Time After Playback Has Started</span></span>

<span data-ttu-id="51cd0-112">Há uma maneira de definir o tempo de parada após a [sessão de mídia](media-session.md) iniciar a reprodução, usando a interface [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) .</span><span class="sxs-lookup"><span data-stu-id="51cd0-112">There is a way to set the stop time after the [Media Session](media-session.md) starts playback, by using the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="51cd0-113">Essa interface tem uma limitação séria, pois a hora de parada é especificada como um valor de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="51cd0-113">This interface has a serious limitation, because the stop time is specified as a 32-bit value.</span></span> <span data-ttu-id="51cd0-114">Isso significa que o tempo máximo de parada que você pode definir usando essa interface é de 0xFFFFFFFF, ou apenas mais de 7 minutos.</span><span class="sxs-lookup"><span data-stu-id="51cd0-114">That means the maximum stop time that you can set using this interface is 0xFFFFFFFF, or just over 7 minutes.</span></span> <span data-ttu-id="51cd0-115">Essa limitação é devido a uma definição de estrutura incorreta.</span><span class="sxs-lookup"><span data-stu-id="51cd0-115">This limitation is due to an incorrect structure definition.</span></span>

 

<span data-ttu-id="51cd0-116">Para definir a hora de parada usando a interface [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) , execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="51cd0-116">To set the stop time using the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface, perform the following steps.</span></span>

1.  <span data-ttu-id="51cd0-117">Chame [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obter a interface [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="51cd0-117">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface from the Media Session.</span></span>
2.  <span data-ttu-id="51cd0-118">Chame [**IMFTopology:: Gettopologiaid**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) para obter a ID da topologia de reprodução.</span><span class="sxs-lookup"><span data-stu-id="51cd0-118">Call [**IMFTopology::GetTopologyID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) to get the ID of the playback topology.</span></span>
3.  <span data-ttu-id="51cd0-119">Para cada nó de saída na topologia, chame [**IMFTopologyNodeAttributeEditor:: UpdateNodeAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes).</span><span class="sxs-lookup"><span data-stu-id="51cd0-119">For each output node in the topology, call [**IMFTopologyNodeAttributeEditor::UpdateNodeAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes).</span></span> <span data-ttu-id="51cd0-120">Esse método usa a ID de topologia e um ponteiro para uma estrutura de [**\_ \_ atualização de atributo MFTOPONODE**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) .</span><span class="sxs-lookup"><span data-stu-id="51cd0-120">This method takes the topology ID and a pointer to a [**MFTOPONODE\_ATTRIBUTE\_UPDATE**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) structure.</span></span> <span data-ttu-id="51cd0-121">Inicialize a estrutura da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="51cd0-121">Initialize the structure as follows.</span></span>

    | <span data-ttu-id="51cd0-122">Membro</span><span class="sxs-lookup"><span data-stu-id="51cd0-122">Member</span></span>               | <span data-ttu-id="51cd0-123">Valor</span><span class="sxs-lookup"><span data-stu-id="51cd0-123">Value</span></span>                                                                                                               |
    |----------------------|---------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="51cd0-124">**NodeId**</span><span class="sxs-lookup"><span data-stu-id="51cd0-124">**NodeId**</span></span>           | <span data-ttu-id="51cd0-125">A ID do nó.</span><span class="sxs-lookup"><span data-stu-id="51cd0-125">The node ID.</span></span> <span data-ttu-id="51cd0-126">Para obter a ID do nó, chame Call [**IMFTopologyNode:: GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).</span><span class="sxs-lookup"><span data-stu-id="51cd0-126">To get the node ID, call call [**IMFTopologyNode::GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).</span></span> |
    | <span data-ttu-id="51cd0-127">**guidAttributeKey**</span><span class="sxs-lookup"><span data-stu-id="51cd0-127">**guidAttributeKey**</span></span> | <span data-ttu-id="51cd0-128">**\_TOPONODE MF \_ MEDIASTOP**</span><span class="sxs-lookup"><span data-stu-id="51cd0-128">**MF\_TOPONODE\_MEDIASTOP**</span></span>                                                                                         |
    | <span data-ttu-id="51cd0-129">**attrType**</span><span class="sxs-lookup"><span data-stu-id="51cd0-129">**attrType**</span></span>         | <span data-ttu-id="51cd0-130">**\_Atributo MF \_ UINT64**</span><span class="sxs-lookup"><span data-stu-id="51cd0-130">**MF\_ATTRIBUTE\_UINT64**</span></span>                                                                                           |
    | <span data-ttu-id="51cd0-131">**u64**</span><span class="sxs-lookup"><span data-stu-id="51cd0-131">**u64**</span></span>              | <span data-ttu-id="51cd0-132">A hora de parada, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="51cd0-132">The stop time, in 100-nanosecond units.</span></span>                                                                             |

    

     

<span data-ttu-id="51cd0-133">Tenha cuidado para definir o valor de **attrType** corretamente.</span><span class="sxs-lookup"><span data-stu-id="51cd0-133">Be careful to set the value of **attrType** correctly.</span></span> <span data-ttu-id="51cd0-134">Embora **u64** seja um tipo de 32 bits, o método requer que **attrType** seja definido como **o \_ atributo MF \_ UINT64**.</span><span class="sxs-lookup"><span data-stu-id="51cd0-134">Although **u64** is a 32-bit type, the method requires that **attrType** be set to **MF\_ATTRIBUTE\_UINT64**.</span></span>

<span data-ttu-id="51cd0-135">O código a seguir mostra essas etapas.</span><span class="sxs-lookup"><span data-stu-id="51cd0-135">The following code shows these steps.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="51cd0-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="51cd0-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51cd0-137">Reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="51cd0-137">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



