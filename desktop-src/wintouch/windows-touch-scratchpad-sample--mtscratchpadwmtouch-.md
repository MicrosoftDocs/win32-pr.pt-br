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
# <a name="windows-touch-scratchpad-sample-c"></a>Exemplo de bloco de rascunho do Windows (C++)

O [exemplo de bloco de rascunho do Windows](https://github.com/MicrosoftDocs/win32-pr/blob/master/desktop-src/wintouch/windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md) mostra como usar as mensagens do Windows Touch para desenhar rastreamentos dos pontos de toque em uma janela. O rastreamento do dedo principal, aquele que foi colocado no digitalizador primeiro, é desenhado em preto. Os dedos secundários são desenhados em seis outras cores: vermelho, verde, azul, ciano, magenta e amarelo. A imagem a seguir mostra como o aplicativo pode ser examinado durante a execução.

![captura de tela mostrando o bloco de rascunho do Windows Touch, com ondulado vermelho e preto na tela](images/mtscratchpadwmtouch.png)

Para este aplicativo, a janela é registrada como uma janela de toque, as mensagens de toque são interpretadas para adicionar pontos de toque a objetos de traço e os traços de tinta são renderizados na tela no manipulador de mensagens **WM_PAINT** .

O código a seguir mostra como a janela é registrada como uma janela de toque.

```C++
    // Register application window for receiving multitouch input. Use default settings.
    if(!RegisterTouchWindow(hWnd, 0))
    {
        MessageBox(hWnd, L"Cannot register application window for multitouch input", L"Error", MB_OK);
        return FALSE;
    }
```

O código a seguir mostra como as mensagens de toque são usadas para adicionar pontos de toque a traços de tinta.

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

O código a seguir mostra como os traços de tinta são desenhados na tela no manipulador de mensagens de **WM_PAINT** .

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

O código a seguir mostra como o objeto Stroke renderiza os traços para a tela.

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

## <a name="related-topics"></a>Tópicos relacionados

[Exemplo de bloco de rascunho do Windows (C#)](windows-touch-scratchpad-sample-in-c---mtscratchpadwmtouchcs-.md), [aplicativo de bloco de rascunho multitoque (WM_TOUCH/c #)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [aplicativo de bloco de rascunho multitoque (WM_TOUCH/C + +)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), [exemplos de toque do Windows](windows-touch-samples.md)
