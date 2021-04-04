---
title: Exemplo de bloco de rascunho do Windows (C++)
description: O exemplo de bloco de rascunho do Windows mostra como usar as mensagens do Windows Touch para desenhar rastreamentos dos pontos de toque em uma janela.
ms.assetid: 6c4b4595-1e95-499c-b045-b5ae01aa5a6e
keywords:
- Windows Touch, exemplos de código
- Windows Touch, código de exemplo
- Windows Touch, amostras de bloco de rascunho
- Amostras de bloco de rascunho
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: afdd39e886d97671942b4ff67a74c0da75924fbb
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104008566"
---
# <a name="windows-touch-scratchpad-sample-c"></a><span data-ttu-id="7394c-107">Exemplo de bloco de rascunho do Windows (C++)</span><span class="sxs-lookup"><span data-stu-id="7394c-107">Windows Touch Scratchpad Sample (C++)</span></span>

<span data-ttu-id="7394c-108">O [exemplo de bloco de rascunho do Windows](https://github.com/MicrosoftDocs/win32-pr/blob/master/desktop-src/wintouch/windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md) mostra como usar as mensagens do Windows Touch para desenhar rastreamentos dos pontos de toque em uma janela.</span><span class="sxs-lookup"><span data-stu-id="7394c-108">The [Windows Touch Scratchpad sample](https://github.com/MicrosoftDocs/win32-pr/blob/master/desktop-src/wintouch/windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md) shows how to use Windows Touch messages to draw traces of the touch points to a window.</span></span> <span data-ttu-id="7394c-109">O rastreamento do dedo principal, aquele que foi colocado no digitalizador primeiro, é desenhado em preto.</span><span class="sxs-lookup"><span data-stu-id="7394c-109">The trace of the primary finger, the one that was put on the digitizer first, is drawn in black.</span></span> <span data-ttu-id="7394c-110">Os dedos secundários são desenhados em seis outras cores: vermelho, verde, azul, ciano, magenta e amarelo.</span><span class="sxs-lookup"><span data-stu-id="7394c-110">Secondary fingers are drawn in six other colors: red, green, blue, cyan, magenta, and yellow.</span></span> <span data-ttu-id="7394c-111">A imagem a seguir mostra como o aplicativo pode ser examinado durante a execução.</span><span class="sxs-lookup"><span data-stu-id="7394c-111">The following image shows how the application could look while running.</span></span>

![captura de tela mostrando o bloco de rascunho do Windows Touch, com ondulado vermelho e preto na tela](images/mtscratchpadwmtouch.png)

<span data-ttu-id="7394c-113">Para este aplicativo, a janela é registrada como uma janela de toque, as mensagens de toque são interpretadas para adicionar pontos de toque a objetos de traço e os traços de tinta são renderizados na tela no manipulador de mensagens **WM_PAINT** .</span><span class="sxs-lookup"><span data-stu-id="7394c-113">For this application, the window is registered as a touch window, touch messages are interpreted to add touch points to stroke objects, and ink strokes are rendered to the screen in the **WM_PAINT** message handler.</span></span>

<span data-ttu-id="7394c-114">O código a seguir mostra como a janela é registrada como uma janela de toque.</span><span class="sxs-lookup"><span data-stu-id="7394c-114">The following code shows how the window is registered as a touch window.</span></span>

```C++
    // Register application window for receiving multitouch input. Use default settings.
    if(!RegisterTouchWindow(hWnd, 0))
    {
        MessageBox(hWnd, L"Cannot register application window for multitouch input", L"Error", MB_OK);
        return FALSE;
    }
```

<span data-ttu-id="7394c-115">O código a seguir mostra como as mensagens de toque são usadas para adicionar pontos de toque a traços de tinta.</span><span class="sxs-lookup"><span data-stu-id="7394c-115">The following code shows how touch messages are used to add touch points to ink strokes.</span></span>

```C++
        // WM_TOUCH message handlers
        case WM_TOUCH:
            {
                // WM_TOUCH message can contain several messages from different contacts
                // packed together.
                // Message parameters need to be decoded:
                unsigned int numInputs = (unsigned int) wParam; // Number of actual per-contact messages
                TOUCHINPUT* ti = new TOUCHINPUT[numInputs]; // Allocate the storage for the parameters of the per-contact messages
                if(ti == NULL)
                {
                    break;
                }
                // Unpack message parameters into the array of TOUCHINPUT structures, each
                // representing a message for one single contact.
                if(GetTouchInputInfo((HTOUCHINPUT)lParam, numInputs, ti, sizeof(TOUCHINPUT)))
                {
                    // For each contact, dispatch the message to the appropriate message
                    // handler.
                    for(unsigned int i=0; i<numInputs; ++i)
                    {
                        if(ti[i].dwFlags & TOUCHEVENTF_DOWN)
                        {
                            OnTouchDownHandler(hWnd, ti[i]);
                        }
                        else if(ti[i].dwFlags & TOUCHEVENTF_MOVE)
                        {
                            OnTouchMoveHandler(hWnd, ti[i]);
                        }
                        else if(ti[i].dwFlags & TOUCHEVENTF_UP)
                        {
                            OnTouchUpHandler(hWnd, ti[i]);
                        }
                    }
                }
                CloseTouchInputHandle((HTOUCHINPUT)lParam);
                delete [] ti;
            }
            break;
```

<span data-ttu-id="7394c-116">O código a seguir mostra como os traços de tinta são desenhados na tela no manipulador de mensagens de **WM_PAINT** .</span><span class="sxs-lookup"><span data-stu-id="7394c-116">The following code shows how the ink strokes are drawn to the screen in the **WM_PAINT** message handler.</span></span>

```C++
        case WM_PAINT:
            hdc = BeginPaint(hWnd, &ps);
            // Full redraw: draw complete collection of finished strokes and
            // also all the strokes that are currently in drawing.
            g_StrkColFinished.Draw(hdc);
            g_StrkColDrawing.Draw(hdc);
            EndPaint(hWnd, &ps);
            break;
```

<span data-ttu-id="7394c-117">O código a seguir mostra como o objeto Stroke renderiza os traços para a tela.</span><span class="sxs-lookup"><span data-stu-id="7394c-117">The following code shows how the stroke object renders strokes to the screen.</span></span>

```C++
void CStroke::Draw(HDC hDC) const
{
    if(m_nCount < 2)
    {
        return;
    }

    HPEN hPen = CreatePen(PS_SOLID, 3, m_clr);
    HGDIOBJ hOldPen = SelectObject(hDC, hPen);
    Polyline(hDC, m_arrData, m_nCount);
    SelectObject(hDC, hOldPen);
    DeleteObject(hPen);
}
```

## <a name="related-topics"></a><span data-ttu-id="7394c-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7394c-118">Related topics</span></span>

<span data-ttu-id="7394c-119">[Exemplo de bloco de rascunho do Windows (C#)](windows-touch-scratchpad-sample-in-c---mtscratchpadwmtouchcs-.md), [aplicativo de bloco de rascunho multitoque (WM_TOUCH/c #)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [aplicativo de bloco de rascunho multitoque (WM_TOUCH/C + +)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), [exemplos de toque do Windows](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="7394c-119">[Windows Touch Scratchpad Sample (C#)](windows-touch-scratchpad-sample-in-c---mtscratchpadwmtouchcs-.md), [Multi-touch Scratchpad Application (WM_TOUCH/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [Multi-touch Scratchpad Application (WM_TOUCH/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
