---
title: Bloco de rascunho do Windows usando o exemplo de Stylus em tempo real (C++)
description: Examine um exemplo do Windows Touch Touchpad C++ (MTScratchpadRTStylus), que mostra como usar as mensagens do Windows Touch para desenhar rastreamentos de pontos de toque em uma janela.
ms.assetid: c72ddc71-48b7-4c26-af2b-10919038eaf8
keywords:
- Windows Touch, exemplos de código
- Windows Touch, código de exemplo
- Windows Touch, amostras de bloco de rascunho
- Amostras de bloco de rascunho
- Windows Touch, objeto de caneta em tempo real (RTS)
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 42e32e66942f3dcfad11b8b777e846e0cee6c0b3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406289"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a>Bloco de rascunho do Windows usando o exemplo de Stylus em tempo real (C++)

O exemplo de bloco de rascunho do Windows ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp)) mostra como usar mensagens de toque do Windows para desenhar rastreamentos dos pontos de toque em uma janela. O rastreamento do dedo principal, aquele que foi colocado no digitalizador primeiro, é desenhado em preto. Os dedos secundários são desenhados em seis outras cores: vermelho, verde, azul, ciano, magenta e amarelo. A captura de tela a seguir mostra como o aplicativo pode ser examinado durante a execução.

![captura de tela mostrando o exemplo de bloco de rascunho de toque do Windows usando a caneta em tempo real, com uma linha verde, vermelha, três preta e azul na tela](images/mtscratchpadrtstylus.png)

Para este exemplo, o objeto de Stylus (RTS) em tempo real é criado e o suporte para vários pontos de contato está habilitado. Um plug-in DynamicRenderer é adicionado ao RTS para renderizar o conteúdo. Um plug-in, **CSyncEventHandlerRTS**, é implementado para rastrear o número de dedos e alterar a cor que o renderizador dinâmico está desenhando. Com ambos os plug-ins na pilha de plug-in de RTS, o aplicativo de bloco de rascunho do Windows irá renderizar o contato principal em preto e o restante dos contatos nas várias cores.

O código a seguir mostra como o objeto RTS é criado com suporte para vários pontos de contato.

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

O código a seguir mostra como o plug-in de processamento dinâmico é criado e adicionado ao RTS.

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

O código a seguir altera a cor de traço da caneta para o manipulador de eventos **StylusDown** no **CSyncEventHandlerRTS**, um plug-in de RTS personalizado.

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

Quando o valor de *m_nContacts* for incrementado, ele alterará o conjunto de cores no processador dinâmico. Os traços que não forem o contato primário serão desenhados com cores diferentes.

## <a name="related-topics"></a>Tópicos relacionados

[Aplicativo de bloco de rascunho multitoque (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [aplicativo de bloco de rascunho multitoque (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [exemplos de toque do Windows](windows-touch-samples.md)
