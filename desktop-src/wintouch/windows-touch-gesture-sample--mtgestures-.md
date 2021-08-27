---
title: Windows Exemplo de gesto de toque (MTGestures)
description: esta seção descreve o exemplo de gesto de toque Windows.
ms.assetid: 04166c9c-5de7-409e-9d5e-dd210a3a3f11
keywords:
- Windows Toque, exemplos de código
- Windows Toque, código de exemplo
- Windows Toque, gestos
- Windows Toque, exemplos de gestos
- Amostras de gesto
- gestos, código de exemplo
- gestos, exemplos de código
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 656b269eae779cd999680e165ba071d983d18526c2e9b873c5a916d61ccdb9f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110576"
---
# <a name="windows-touch-gesture-sample-mtgestures"></a>Windows Exemplo de gesto de toque (MTGestures)

esta seção descreve o exemplo de gesto de toque Windows.

o exemplo de gesto de toque Windows demonstra como usar mensagens de gesto para converter, girar e dimensionar uma caixa renderizada pelo Graphics Device Interface (GDI) manipulando a mensagem [**WM_GESTURE**](wm-gesture.md) . A captura de tela a seguir mostra como a amostra parece quando está em execução.

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

[aplicativo de gestos multitoque (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [aplicativo de gestos multitoque (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows toque em exemplos](windows-touch-samples.md)
