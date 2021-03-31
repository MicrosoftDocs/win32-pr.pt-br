---
title: Exemplo de gesto de toque do Windows (MTGestures)
description: Esta seção descreve o exemplo de gesto de toque do Windows.
ms.assetid: 04166c9c-5de7-409e-9d5e-dd210a3a3f11
keywords:
- Windows Touch, exemplos de código
- Windows Touch, código de exemplo
- Toque do Windows, gestos
- Toque do Windows, exemplos de gesto
- Amostras de gesto
- gestos, código de exemplo
- gestos, exemplos de código
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 0e01d97e844af37caeb5c33f3cb780601da4629d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640132"
---
# <a name="windows-touch-gesture-sample-mtgestures"></a>Exemplo de gesto de toque do Windows (MTGestures)

Esta seção descreve o exemplo de gesto de toque do Windows.

O exemplo de gesto de toque do Windows demonstra como usar mensagens de gesto para converter, girar e dimensionar uma caixa renderizada pelo Graphics Device Interface (GDI) manipulando a mensagem de [**WM_GESTURE**](wm-gesture.md) . A captura de tela a seguir mostra como a amostra parece quando está em execução.

![captura de tela mostrando o exemplo do gesto de toque do Windows quando ele está em execução, com um retângulo branco girado e com contorno preto na tela](images/mtgestures.png)

Para este exemplo, as mensagens de gesto são passadas para um mecanismo de gesto, que chama métodos em objetos de desenho para converter, girar e dimensionar um objeto que tem métodos para lidar com esses comandos. Para ajudar a mostrar como o exemplo funciona, considere as etapas para usar o comando tocar com dois dedos para habilitar ou desabilitar linhas diagonais na caixa renderizada. Um usuário executa o gesto de toque com dois dedos, que gera uma mensagem que é manipulada pelo programa. Quando a mensagem for tratada, ela alternará um booliano para renderizar diagonais no objeto de desenho e o objeto renderizará as linhas diagonais.

O código a seguir mostra como as mensagens de gestos são passadas para o mecanismo de gesto do método WndProc.

```C++
    case WM_GESTURE:
        // The gesture-processing code is implemented in the CGestureEngine
        // class.
        return g_cGestureEngine.WndProc(hWnd,wParam,lParam);
        break;
```

O código a seguir mostra como o mecanismo de gestos manipula o comando TAP com dois dedos.

```C++
// Two-finger tap command
void CMyGestureEngine::ProcessTwoFingerTap(void)
{
    if(_pcRect)
    {
        _pcRect->ToggleDrawDiagonals();
    }
}
```

O código a seguir mostra como o objeto de desenho alterna suas diagonais.

```C++
void ToggleDrawDiagonals(void){_bDrawDiagonals = !_bDrawDiagonals;}
```

O código a seguir mostra como o objeto renderiza linhas diagonais em seu método Draw.

```C++
    if(_bDrawDiagonals)
    {
        // draw diagonals
        MoveToEx(hdc,ptRect[0].x,ptRect[0].y,NULL);
        LineTo(hdc,ptRect[2].x,ptRect[2].y);
        MoveToEx(hdc,ptRect[1].x,ptRect[1].y,NULL);
        LineTo(hdc,ptRect[3].x,ptRect[3].y);
    }
```

## <a name="related-topics"></a>Tópicos relacionados

[Aplicativo de gestos multitoque (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [aplicativo de gestos multitoque (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), exemplos de [toque do Windows](windows-touch-samples.md)
