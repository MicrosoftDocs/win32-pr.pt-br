---
title: Bloco de rascunho do Windows usando o exemplo de Stylus em tempo real (C++)
description: O exemplo de bloco de rascunho do Windows (MTScratchpadRTStylus) mostra como usar mensagens de toque do Windows para desenhar rastreamentos dos pontos de toque em uma janela.
ms.assetid: c72ddc71-48b7-4c26-af2b-10919038eaf8
keywords:
- Windows Touch, exemplos de código
- Windows Touch, código de exemplo
- Windows Touch, amostras de bloco de rascunho
- Amostras de bloco de rascunho
- Windows Touch, objeto de caneta em tempo real (RTS)
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 94d425bcb39dd35d3bd71636fb19b6b408af9477
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105771423"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a><span data-ttu-id="67692-108">Bloco de rascunho do Windows usando o exemplo de Stylus em tempo real (C++)</span><span class="sxs-lookup"><span data-stu-id="67692-108">Windows Touch Scratchpad using the Real-time Stylus Sample (C++)</span></span>

<span data-ttu-id="67692-109">O exemplo de bloco de rascunho do Windows ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp)) mostra como usar mensagens de toque do Windows para desenhar rastreamentos dos pontos de toque em uma janela.</span><span class="sxs-lookup"><span data-stu-id="67692-109">The Windows Touch Scratchpad sample ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp)) shows how to use Windows Touch messages to draw traces of the touch points to a window.</span></span> <span data-ttu-id="67692-110">O rastreamento do dedo principal, aquele que foi colocado no digitalizador primeiro, é desenhado em preto.</span><span class="sxs-lookup"><span data-stu-id="67692-110">The trace of the primary finger, the one that was put on the digitizer first, is drawn in black.</span></span> <span data-ttu-id="67692-111">Os dedos secundários são desenhados em seis outras cores: vermelho, verde, azul, ciano, magenta e amarelo.</span><span class="sxs-lookup"><span data-stu-id="67692-111">Secondary fingers are drawn in six other colors: red, green, blue, cyan, magenta, and yellow.</span></span> <span data-ttu-id="67692-112">A captura de tela a seguir mostra como o aplicativo pode ser examinado durante a execução.</span><span class="sxs-lookup"><span data-stu-id="67692-112">The following screen shot shows how the application could look while running.</span></span>

![captura de tela mostrando o exemplo de bloco de rascunho de toque do Windows usando a caneta em tempo real, com uma linha verde, vermelha, três preta e azul na tela](images/mtscratchpadrtstylus.png)

<span data-ttu-id="67692-114">Para este exemplo, o objeto de Stylus (RTS) em tempo real é criado e o suporte para vários pontos de contato está habilitado.</span><span class="sxs-lookup"><span data-stu-id="67692-114">For this sample, the Real-time Stylus (RTS) object is created and support for multiple contact points is enabled.</span></span> <span data-ttu-id="67692-115">Um plug-in DynamicRenderer é adicionado ao RTS para renderizar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="67692-115">A DynamicRenderer plug-in is added to the RTS to render content.</span></span> <span data-ttu-id="67692-116">Um plug-in, **CSyncEventHandlerRTS**, é implementado para rastrear o número de dedos e alterar a cor que o renderizador dinâmico está desenhando.</span><span class="sxs-lookup"><span data-stu-id="67692-116">A plug-in, **CSyncEventHandlerRTS**, is implemented to track down the number of fingers and to change the color that the dynamic renderer is drawing.</span></span> <span data-ttu-id="67692-117">Com ambos os plug-ins na pilha de plug-in de RTS, o aplicativo de bloco de rascunho do Windows irá renderizar o contato principal em preto e o restante dos contatos nas várias cores.</span><span class="sxs-lookup"><span data-stu-id="67692-117">With both plug-ins in the RTS plug-in stack, the Windows Touch Scratchpad application will render the primary contact in black and the rest of the contacts in the various colors.</span></span>

<span data-ttu-id="67692-118">O código a seguir mostra como o objeto RTS é criado com suporte para vários pontos de contato.</span><span class="sxs-lookup"><span data-stu-id="67692-118">The following code shows how the RTS object is created with support for multiple contact points.</span></span>

```C++
IRealTimeStylus* CreateRealTimeStylus(HWND hWnd)
{
    // Check input argument
    if (hWnd == NULL)
    {
        ASSERT(hWnd && L"CreateRealTimeStylus: invalid argument hWnd");
        return NULL;
    }

    // Create RTS object
    IRealTimeStylus* pRealTimeStylus = NULL;
    HRESULT hr = CoCreateInstance(CLSID_RealTimeStylus, NULL, CLSCTX_ALL, IID_PPV_ARGS(&pRealTimeStylus));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: failed to CoCreateInstance of RealTimeStylus");
        return NULL;
    }

    // Attach RTS object to a window
    hr = pRealTimeStylus->put_HWND((HANDLE_PTR)hWnd);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: failed to set window handle");
        pRealTimeStylus->Release();
        return NULL;
    }

    // Register RTS object for receiving multi-touch input.
    IRealTimeStylus3* pRealTimeStylus3 = NULL;
    hr = pRealTimeStylus->QueryInterface(&pRealTimeStylus3);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: cannot access IRealTimeStylus3");
        pRealTimeStylus->Release();
        return NULL;
    }
    hr = pRealTimeStylus3->put_MultiTouchEnabled(TRUE);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: failed to enable multi-touch");
        pRealTimeStylus->Release();
        pRealTimeStylus3->Release();
        return NULL;
    }
    pRealTimeStylus3->Release();

    return pRealTimeStylus;
}
```

<span data-ttu-id="67692-119">O código a seguir mostra como o plug-in de processamento dinâmico é criado e adicionado ao RTS.</span><span class="sxs-lookup"><span data-stu-id="67692-119">The following code shows how the dynamic renderer plug-in is created and added to the RTS.</span></span>

```C++
IDynamicRenderer* CreateDynamicRenderer(IRealTimeStylus* pRealTimeStylus)
{
    // Check input argument
    if (pRealTimeStylus == NULL)
    {
        ASSERT(pRealTimeStylus && L"CreateDynamicRenderer: invalid argument RealTimeStylus");
        return NULL;
    }

    // Get window handle from RTS object
    HWND hWnd = NULL;
    HRESULT hr = pRealTimeStylus->get_HWND((HANDLE_PTR*)&hWnd);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to get window handle");
        return NULL;
    }

    // Create DynamicRenderer object
    IDynamicRenderer* pDynamicRenderer = NULL;
    hr = CoCreateInstance(CLSID_DynamicRenderer, NULL, CLSCTX_ALL, IID_PPV_ARGS(&pDynamicRenderer));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to CoCreateInstance of DynamicRenderer");
        return NULL;
    }

    // Add DynamicRenderer to the RTS object as a synchronous plugin
    IStylusSyncPlugin* pSyncDynamicRenderer = NULL;
    hr = pDynamicRenderer->QueryInterface(&pSyncDynamicRenderer);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to access IStylusSyncPlugin of DynamicRenderer");
        pDynamicRenderer->Release();
        return NULL;
    }

    hr = pRealTimeStylus->AddStylusSyncPlugin(
        0,                      // insert plugin at position 0 in the sync plugin list
        pSyncDynamicRenderer);  // plugin to be inserted - DynamicRenderer
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to add DynamicRenderer to the RealTimeStylus plugins");
        pDynamicRenderer->Release();
        pSyncDynamicRenderer->Release();
        return NULL;
    }

    // Attach DynamicRenderer to the same window RTS object is attached to
    hr = pDynamicRenderer->put_HWND((HANDLE_PTR)hWnd);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to set window handle");
        pDynamicRenderer->Release();
        pSyncDynamicRenderer->Release();
        return NULL;
    }

    pSyncDynamicRenderer->Release();

    return pDynamicRenderer;
}
```

<span data-ttu-id="67692-120">O código a seguir altera a cor de traço da caneta para o manipulador de eventos **StylusDown** no **CSyncEventHandlerRTS**, um plug-in de RTS personalizado.</span><span class="sxs-lookup"><span data-stu-id="67692-120">The following code changes the stylus stroke color for the **StylusDown** event handler in the **CSyncEventHandlerRTS**, a custom RTS plug-in.</span></span>

```C++
HRESULT CSyncEventHandlerRTS::StylusDown(
    IRealTimeStylus* /* piRtsSrc */,
    const StylusInfo* /* pStylusInfo */,
    ULONG /* cPropCountPerPkt */,
    LONG* /* pPacket */,
    LONG** /* ppInOutPkt */)
{
    // Get DrawingAttributes of DynamicRenderer
    IInkDrawingAttributes* pDrawingAttributesDynamicRenderer;
    HRESULT hr = g_pDynamicRenderer->get_DrawingAttributes(&pDrawingAttributesDynamicRenderer);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CSyncEventHandlerRTS::StylusDown: failed to get RTS's drawing attributes");
        return hr;
    }

    // Set new stroke color to the DrawingAttributes of the DynamicRenderer
    // If there are no fingers down, this is a primary contact
    hr = pDrawingAttributesDynamicRenderer->put_Color(GetTouchColor(m_nContacts == 0));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CSyncEventHandlerRTS::StylusDown: failed to set color");
        pDrawingAttributesDynamicRenderer->Release();
        return hr;
    }

    pDrawingAttributesDynamicRenderer->Release();

    ++m_nContacts;  // Increment finger-down counter

    return S_OK;
}
```

<span data-ttu-id="67692-121">Quando o valor de *m_nContacts* for incrementado, ele alterará o conjunto de cores no processador dinâmico.</span><span class="sxs-lookup"><span data-stu-id="67692-121">When the *m_nContacts* value is incremented, it will change the color set in the dynamic renderer.</span></span> <span data-ttu-id="67692-122">Os traços que não forem o contato primário serão desenhados com cores diferentes.</span><span class="sxs-lookup"><span data-stu-id="67692-122">Strokes that are not the primary contact will be drawn with different colors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67692-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="67692-123">Related topics</span></span>

<span data-ttu-id="67692-124">[Aplicativo de bloco de rascunho multitoque (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [aplicativo de bloco de rascunho multitoque (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [exemplos de toque do Windows](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="67692-124">[Multi-touch Scratchpad Application (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [Multi-touch Scratchpad Application (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
