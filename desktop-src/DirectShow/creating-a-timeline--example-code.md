---
description: 'Criando uma linha do tempo: código de exemplo'
ms.assetid: efe6e8d7-2465-4374-8c99-a410091f8d46
title: 'Criando uma linha do tempo: código de exemplo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877bd79b055171dfa5bd12cff0ae257d60e76a16
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105787395"
---
# <a name="creating-a-timeline-example-code"></a><span data-ttu-id="f09c0-103">Criando uma linha do tempo: código de exemplo</span><span class="sxs-lookup"><span data-stu-id="f09c0-103">Creating a Timeline: Example Code</span></span>

<span data-ttu-id="f09c0-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="f09c0-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="f09c0-105">O exemplo de código a seguir mostra como criar e visualizar uma linha do tempo nos [serviços de edição do DirectShow](directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="f09c0-105">The following code example shows how to create and preview a timeline in [DirectShow Editing Services](directshow-editing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="f09c0-106">Para fins de brevidade, o código de exemplo não executa nenhuma verificação de erro.</span><span class="sxs-lookup"><span data-stu-id="f09c0-106">For the sake of brevity, the sample code performs no error checking.</span></span> <span data-ttu-id="f09c0-107">Em um aplicativo real, você deve verificar os valores de retorno das chamadas de método para garantir que nenhum tenha falhado.</span><span class="sxs-lookup"><span data-stu-id="f09c0-107">In a real application, you should check the return values of method calls to make sure none has failed.</span></span>

 


```C++
#include <dshow.h>
#include <qedit.h>

// Preview a timeline.
void PreviewTL(IAMTimeline *pTL, IRenderEngine *pRender) 
{
    IGraphBuilder   *pGraph = NULL;
    IMediaControl   *pControl = NULL;
    IMediaEvent     *pEvent = NULL;

    // Build the graph.
    pRender->SetTimelineObject(pTL);
    pRender->ConnectFrontEnd( );
    pRender->RenderOutputPins( );

    // Run the graph.
    pRender->GetFilterGraph(&pGraph);
    pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
    pControl->Run();

    long evCode;
    pEvent->WaitForCompletion(INFINITE, &evCode);
    pControl->Stop();

    // Clean up.
    pEvent->Release();
    pControl->Release();
    pGraph->Release();
}

void main( void )
{
    // Start by making an empty timeline.

    IAMTimeline    *pTL = NULL;
    CoInitialize(NULL);
    CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);

    // GROUP: Add a video group to the timeline. 

    IAMTimelineGroup    *pGroup = NULL;
    IAMTimelineObj      *pGroupObj = NULL;
    pTL->CreateEmptyNode(&pGroupObj, TIMELINE_MAJOR_TYPE_GROUP);
    pGroupObj->QueryInterface(IID_IAMTimelineGroup, (void **)&pGroup);

    // Set the group media type. This example sets the type to "video" and
    // lets DES pick the default settings. For a more detailed example,
    // see "Setting the Group Media Type."
    AM_MEDIA_TYPE mtGroup;  
    ZeroMemory(&mtGroup, sizeof(AM_MEDIA_TYPE));
    mtGroup.majortype = MEDIATYPE_Video;
    pGroup->SetMediaType(&mtGroup);
    pTL->AddGroup(pGroupObj);
    pGroupObj->Release();

    // TRACK: Add a track to the group. 

    IAMTimelineObj      *pTrackObj;
    IAMTimelineTrack    *pTrack;
    IAMTimelineComp     *pComp = NULL;

    pTL->CreateEmptyNode(&pTrackObj, TIMELINE_MAJOR_TYPE_TRACK);
    pGroup->QueryInterface(IID_IAMTimelineComp, (void **)&pComp);
    pComp->VTrackInsBefore(pTrackObj, 0);
    pTrackObj->QueryInterface(IID_IAMTimelineTrack, (void **)&pTrack);

    pTrackObj->Release();
    pComp->Release();    
    pGroup->Release();

    // SOURCE: Add a source to the track.

    IAMTimelineSrc *pSource = NULL;
    IAMTimelineObj *pSourceObj;
    pTL->CreateEmptyNode(&pSourceObj, TIMELINE_MAJOR_TYPE_SOURCE);
    pSourceObj->QueryInterface(IID_IAMTimelineSrc, (void **)&pSource);

    // Set the times and the file name.
    pSourceObj->SetStartStop(0, 50000000);
    BSTR bstrFile = SysAllocString(OLESTR("C:\\example.avi"));
    pSource->SetMediaName(bstrFile); 
    SysFreeString(bstrFile);
    pSource->SetMediaTimes(40000000, 140000000);
    pTrack->SrcAdd(pSourceObj);

    pSourceObj->Release();
    pSource->Release();
    pTrack->Release();

    // Preview the timeline.
    IRenderEngine *pRenderEngine = NULL;
    CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
        IID_IRenderEngine, (void**) &pRenderEngine);
    PreviewTL(pTL, pRenderEngine);

    // Clean up.
    pRenderEngine->ScrapIt();
    pRenderEngine->Release();
    pTL->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a><span data-ttu-id="f09c0-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f09c0-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f09c0-109">Construindo uma linha do tempo</span><span class="sxs-lookup"><span data-stu-id="f09c0-109">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



