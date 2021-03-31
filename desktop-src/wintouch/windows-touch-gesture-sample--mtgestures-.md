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
# <a name="windows-touch-gesture-sample-mtgestures"></a><span data-ttu-id="59740-110">Exemplo de gesto de toque do Windows (MTGestures)</span><span class="sxs-lookup"><span data-stu-id="59740-110">Windows Touch Gesture Sample (MTGestures)</span></span>

<span data-ttu-id="59740-111">Esta seção descreve o exemplo de gesto de toque do Windows.</span><span class="sxs-lookup"><span data-stu-id="59740-111">This section describes the Windows Touch Gesture sample.</span></span>

<span data-ttu-id="59740-112">O exemplo de gesto de toque do Windows demonstra como usar mensagens de gesto para converter, girar e dimensionar uma caixa renderizada pelo Graphics Device Interface (GDI) manipulando a mensagem de [**WM_GESTURE**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="59740-112">The Windows Touch Gesture sample demonstrates how to use gesture messages to translate, rotate, and scale a box rendered by the Graphics Device Interface (GDI) by handling the [**WM_GESTURE**](wm-gesture.md) message.</span></span> <span data-ttu-id="59740-113">A captura de tela a seguir mostra como a amostra parece quando está em execução.</span><span class="sxs-lookup"><span data-stu-id="59740-113">The following screen shot shows how the sample looks when it is running.</span></span>

![captura de tela mostrando o exemplo do gesto de toque do Windows quando ele está em execução, com um retângulo branco girado e com contorno preto na tela](images/mtgestures.png)

<span data-ttu-id="59740-115">Para este exemplo, as mensagens de gesto são passadas para um mecanismo de gesto, que chama métodos em objetos de desenho para converter, girar e dimensionar um objeto que tem métodos para lidar com esses comandos.</span><span class="sxs-lookup"><span data-stu-id="59740-115">For this sample, gesture messages are passed to a gesture engine, which then calls methods on drawing objects to translate, rotate, and scale an object that has methods for handling these commands.</span></span> <span data-ttu-id="59740-116">Para ajudar a mostrar como o exemplo funciona, considere as etapas para usar o comando tocar com dois dedos para habilitar ou desabilitar linhas diagonais na caixa renderizada.</span><span class="sxs-lookup"><span data-stu-id="59740-116">To help show how the sample works, consider the steps for using the two-finger tap command to enable or disable diagonal lines in the rendered box.</span></span> <span data-ttu-id="59740-117">Um usuário executa o gesto de toque com dois dedos, que gera uma mensagem que é manipulada pelo programa.</span><span class="sxs-lookup"><span data-stu-id="59740-117">A user performs the two-finger tap gesture, which generates a message that is handled by the program.</span></span> <span data-ttu-id="59740-118">Quando a mensagem for tratada, ela alternará um booliano para renderizar diagonais no objeto de desenho e o objeto renderizará as linhas diagonais.</span><span class="sxs-lookup"><span data-stu-id="59740-118">When the message is handled, it will toggle a Boolean for rendering diagonals on the drawing object, and the object will then render the diagonal lines.</span></span>

<span data-ttu-id="59740-119">O código a seguir mostra como as mensagens de gestos são passadas para o mecanismo de gesto do método WndProc.</span><span class="sxs-lookup"><span data-stu-id="59740-119">The following code shows how gesture messages are passed to the gesture engine from the WndProc method.</span></span>

```C++
    case WM_GESTURE:
        // The gesture-processing code is implemented in the CGestureEngine
        // class.
        return g_cGestureEngine.WndProc(hWnd,wParam,lParam);
        break;
```

<span data-ttu-id="59740-120">O código a seguir mostra como o mecanismo de gestos manipula o comando TAP com dois dedos.</span><span class="sxs-lookup"><span data-stu-id="59740-120">The following code shows how the gesture engine handles the two-finger tap command.</span></span>

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

<span data-ttu-id="59740-121">O código a seguir mostra como o objeto de desenho alterna suas diagonais.</span><span class="sxs-lookup"><span data-stu-id="59740-121">The following code shows how the drawing object toggles its diagonals.</span></span>

```C++
void ToggleDrawDiagonals(void){_bDrawDiagonals = !_bDrawDiagonals;}
```

<span data-ttu-id="59740-122">O código a seguir mostra como o objeto renderiza linhas diagonais em seu método Draw.</span><span class="sxs-lookup"><span data-stu-id="59740-122">The following code shows how the object renders diagonal lines in its draw method.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="59740-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="59740-123">Related topics</span></span>

<span data-ttu-id="59740-124">[Aplicativo de gestos multitoque (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [aplicativo de gestos multitoque (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), exemplos de [toque do Windows](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="59740-124">[Multi-touch Gestures Application (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [Multi-touch Gestures Application (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
