---
description: Este tópico é a etapa 2 do tutorial de reprodução de áudio/vídeo no DirectShow.
ms.assetid: 61106781-d10c-41a8-993e-121e0a1e4c4d
title: 'Etapa 2: declarar CVideoRenderer e classes derivadas'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11474c57e70d8632a53ac0b858d61d2bddf1e86b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780042"
---
# <a name="step-2-declare-cvideorenderer-and-derived-classes"></a>Etapa 2: declarar CVideoRenderer e classes derivadas

Este tópico é a etapa 2 do tutorial de [reprodução de áudio/vídeo no DirectShow](audio-video-playback-in-directshow.md). O código completo é mostrado no exemplo do tópico [reprodução do DirectShow](directshow-playback-example.md).

O DirectShow fornece vários filtros diferentes que renderizam vídeo:

-   [**Filtro de processador de vídeo avançado**](enhanced-video-renderer-filter.md) (EVR)
-   [Filtro de processador de mixagem de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9)
-   [Filtro de processador de mixagem de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7)

Para obter mais informações sobre as diferenças entre esses filtros, consulte [escolhendo o processador de vídeo correto](choosing-the-right-renderer.md).

Neste tutorial, a seguinte classe abstrata é usada para encapsular o filtro de processador de vídeo.


```C++
// Abstract class to manage the video renderer filter.
// Specific implementations handle the VMR-7, VMR-9, or EVR filter.

class CVideoRenderer
{
public:
    virtual ~CVideoRenderer() {};
    virtual BOOL    HasVideo() const = 0;
    virtual HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd) = 0;
    virtual HRESULT FinalizeGraph(IGraphBuilder *pGraph) = 0;
    virtual HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc) = 0;
    virtual HRESULT Repaint(HWND hwnd, HDC hdc) = 0;
    virtual HRESULT DisplayModeChanged() = 0;
};
```



Observações:

-   O `HasVideo` método retornará **true** se o processador de vídeo tiver sido criado.
-   O `AddToGraph` método adiciona o renderizador de vídeo ao gráfico de filtro.
-   O `FinalizeGraph` método conclui a etapa de criação de grafo.
-   O `UpdateVideoWindow` método atualiza o retângulo de destino do vídeo.
-   O `Repaint` método redesenha o quadro de vídeo atual.
-   O `DisplayModeChanged` método manipula as alterações no modo de exibição.

Cada um desses métodos é descrito em detalhes posteriormente neste tutorial.

Em seguida, declare uma classe derivada para encapsular cada um dos três renderizadores de vídeo: o EVR, o VMR-9 e o VMR-7.

### <a name="cevr-class"></a>Classe CEVR

A `CEVR` classe gerencia o EVR. Ele contém um ponteiro para as interfaces [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) e [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) do EVR.


```C++
// Manages the EVR video renderer filter.

class CEVR : public CVideoRenderer
{
    IBaseFilter            *m_pEVR;
    IMFVideoDisplayControl *m_pVideoDisplay;

public:
    CEVR();
    ~CEVR();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr9-class"></a>Classe CVMR9

A `CVMR9` classe gerencia o VMR-9. Ele contém um ponteiro para a interface [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .


```C++
// Manages the VMR-9 video renderer filter.

class CVMR9 : public CVideoRenderer
{
    IVMRWindowlessControl9 *m_pWindowless;

public:
    CVMR9();
    ~CVMR9();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr7-class"></a>Classe CVMR7

A `CVMR7` classe gerencia o VMR-7. Ele contém um ponteiro para a interface [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .


```C++
// Manages the VMR-7 video renderer filter.

class CVMR7 : public CVideoRenderer
{
    IVMRWindowlessControl   *m_pWindowless;

public:
    CVMR7();
    ~CVMR7();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



Em seguida: [etapa 3: criar o grafo de filtro](step-3--build-the-filter-graph.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo no DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Usando o processador de mixagem de vídeo](using-the-video-mixing-renderer.md)
</dt> <dt>

[Renderização de vídeo](video-rendering.md)
</dt> </dl>

 

 
