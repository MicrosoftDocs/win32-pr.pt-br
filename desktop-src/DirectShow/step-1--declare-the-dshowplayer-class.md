---
description: Este tópico é a etapa 1 do tutorial de reprodução de áudio/vídeo no DirectShow.
ms.assetid: 3ccd201d-e60d-40bf-a602-6d42df03b36b
title: 'Etapa 1: declarar a classe DShowPlayer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22ff36a76be8017f7b468815cf572514900f8d11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766260"
---
# <a name="step-1-declare-the-dshowplayer-class"></a><span data-ttu-id="7d538-103">Etapa 1: declarar a classe DShowPlayer</span><span class="sxs-lookup"><span data-stu-id="7d538-103">Step 1: Declare the DShowPlayer Class</span></span>

<span data-ttu-id="7d538-104">Este tópico é a etapa 1 do tutorial de [reprodução de áudio/vídeo no DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="7d538-104">This topic is step 1 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="7d538-105">O código completo é mostrado no exemplo do tópico [reprodução do DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="7d538-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="7d538-106">Neste tutorial, a `DShowPlayer` classe gerencia toda a funcionalidade do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7d538-106">In this tutorial, the `DShowPlayer` class manages all DirectShow functionality.</span></span> <span data-ttu-id="7d538-107">Essa classe é declarada como folows.</span><span class="sxs-lookup"><span data-stu-id="7d538-107">This class is declared as folows.</span></span>


```C++
#include <new>
#include <windows.h>
#include <dshow.h>


enum PlaybackState
{
    STATE_NO_GRAPH,
    STATE_RUNNING,
    STATE_PAUSED,
    STATE_STOPPED,
};

const UINT WM_GRAPH_EVENT = WM_APP + 1;

typedef void (CALLBACK *GraphEventFN)(HWND hwnd, long eventCode, LONG_PTR param1, LONG_PTR param2);

class DShowPlayer
{
public:
    DShowPlayer(HWND hwnd);
    ~DShowPlayer();

    PlaybackState State() const { return m_state; }

    HRESULT OpenFile(PCWSTR pszFileName);
    
    HRESULT Play();
    HRESULT Pause();
    HRESULT Stop();

    BOOL    HasVideo() const;
    HRESULT UpdateVideoWindow(const LPRECT prc);
    HRESULT Repaint(HDC hdc);
    HRESULT DisplayModeChanged();

    HRESULT HandleGraphEvent(GraphEventFN pfnOnGraphEvent);

private:
    HRESULT InitializeGraph();
    void    TearDownGraph();
    HRESULT CreateVideoRenderer();
    HRESULT RenderStreams(IBaseFilter *pSource);

    PlaybackState   m_state;

    HWND m_hwnd; // Video window. This window also receives graph events.

    IGraphBuilder   *m_pGraph;
    IMediaControl   *m_pControl;
    IMediaEventEx   *m_pEvent;
    CVideoRenderer  *m_pVideo;
};
```





<span data-ttu-id="7d538-108">Observações:</span><span class="sxs-lookup"><span data-stu-id="7d538-108">Notes:</span></span>

-   <span data-ttu-id="7d538-109">A `PlaybackState` Enumeração descreve o estado atual do `DShowPlayer` objeto.</span><span class="sxs-lookup"><span data-stu-id="7d538-109">The `PlaybackState` enumeration describes the current state of the `DShowPlayer` object.</span></span>
-   <span data-ttu-id="7d538-110">O evento de grafo do WM constante \_ \_ define uma mensagem de janela privada.</span><span class="sxs-lookup"><span data-stu-id="7d538-110">The constant WM\_GRAPH\_EVENT defines a private window message.</span></span> <span data-ttu-id="7d538-111">Essa mensagem é usada para notificar o aplicativo sobre eventos de gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="7d538-111">This message is used to notify the application about filter graph events.</span></span> <span data-ttu-id="7d538-112">Consulte [Step 6: tratar eventos de grafo](step-6--handle-graph-events.md).</span><span class="sxs-lookup"><span data-stu-id="7d538-112">See [Step 6: Handle Graph Events](step-6--handle-graph-events.md).</span></span>
-   <span data-ttu-id="7d538-113">`GraphEventFN` é um ponteiro para uma função de retorno de chamada para manipular eventos de gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="7d538-113">`GraphEventFN` is a pointer to a callback function for handling filter graph events.</span></span> <span data-ttu-id="7d538-114">O aplicativo implementa essa função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="7d538-114">The application implements this callback function.</span></span>
-   <span data-ttu-id="7d538-115">A variável de membro *m \_ pVideo* fornece um wrapper para os vários renderizadores de vídeo do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7d538-115">The *m\_pVideo* member variable provides a wrapper for the various DirectShow video renderers.</span></span> <span data-ttu-id="7d538-116">Consulte [Step 2: declare CVideoRenderer e classes derivadas](step-2--declare-cvideorenderer-and-derived-classes.md).</span><span class="sxs-lookup"><span data-stu-id="7d538-116">See [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>
-   <span data-ttu-id="7d538-117">Ao longo deste tutorial, a função [SafeRelease](../medfound/saferelease.md) é usada para liberar ponteiros de interface com.</span><span class="sxs-lookup"><span data-stu-id="7d538-117">Throughout this tutorial, the [SafeRelease](../medfound/saferelease.md) function is used to release COM interface pointers.</span></span>

<span data-ttu-id="7d538-118">Em seguida: [etapa 2: declarar CVideoRenderer e classes derivadas](step-2--declare-cvideorenderer-and-derived-classes.md).</span><span class="sxs-lookup"><span data-stu-id="7d538-118">Next: [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d538-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d538-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d538-120">Reprodução de áudio/vídeo no DirectShow</span><span class="sxs-lookup"><span data-stu-id="7d538-120">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> </dl>

 

 
