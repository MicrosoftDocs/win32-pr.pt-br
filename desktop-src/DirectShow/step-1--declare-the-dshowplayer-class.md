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
# <a name="step-1-declare-the-dshowplayer-class"></a>Etapa 1: declarar a classe DShowPlayer

Este tópico é a etapa 1 do tutorial de [reprodução de áudio/vídeo no DirectShow](audio-video-playback-in-directshow.md). O código completo é mostrado no exemplo do tópico [reprodução do DirectShow](directshow-playback-example.md).

Neste tutorial, a `DShowPlayer` classe gerencia toda a funcionalidade do DirectShow. Essa classe é declarada como folows.


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





Observações:

-   A `PlaybackState` Enumeração descreve o estado atual do `DShowPlayer` objeto.
-   O evento de grafo do WM constante \_ \_ define uma mensagem de janela privada. Essa mensagem é usada para notificar o aplicativo sobre eventos de gráfico de filtro. Consulte [Step 6: tratar eventos de grafo](step-6--handle-graph-events.md).
-   `GraphEventFN` é um ponteiro para uma função de retorno de chamada para manipular eventos de gráfico de filtro. O aplicativo implementa essa função de retorno de chamada.
-   A variável de membro *m \_ pVideo* fornece um wrapper para os vários renderizadores de vídeo do DirectShow. Consulte [Step 2: declare CVideoRenderer e classes derivadas](step-2--declare-cvideorenderer-and-derived-classes.md).
-   Ao longo deste tutorial, a função [SafeRelease](../medfound/saferelease.md) é usada para liberar ponteiros de interface com.

Em seguida: [etapa 2: declarar CVideoRenderer e classes derivadas](step-2--declare-cvideorenderer-and-derived-classes.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo no DirectShow](audio-video-playback-in-directshow.md)
</dt> </dl>

 

 
