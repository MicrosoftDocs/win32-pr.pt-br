---
title: Gestos do Windows Touch no exemplo C (MTGesturesCS)
description: Esta seção descreve o exemplo de gestos do Windows Touch em C \.
ms.assetid: 4b2d70bb-47e4-4448-97e2-6f6e29d1dfdf
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
ms.openlocfilehash: e6ffc0e8caf63807d4df80a1b96229f2fa7b5ff9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365553"
---
# <a name="windows-touch-gestures-in-c-sample-mtgesturescs"></a><span data-ttu-id="7cdd3-110">Gestos do Windows Touch na amostra do C# (MTGesturesCS)</span><span class="sxs-lookup"><span data-stu-id="7cdd3-110">Windows Touch Gestures in C# Sample (MTGesturesCS)</span></span>

<span data-ttu-id="7cdd3-111">Esta seção descreve o exemplo de gestos do Windows Touch em C#.</span><span class="sxs-lookup"><span data-stu-id="7cdd3-111">This section describes the Windows Touch Gestures sample in C#.</span></span>

<span data-ttu-id="7cdd3-112">Este exemplo de gestos do Windows Touch demonstra como usar mensagens de gesto para converter, girar e dimensionar uma caixa renderizada pelo Graphics Device Interface (GDI) manipulando a mensagem de [**WM_GESTURE**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="7cdd3-112">This Windows Touch Gestures sample demonstrates how to use gesture messages to translate, rotate, and scale a box rendered by the Graphics Device Interface (GDI) by handling the [**WM_GESTURE**](wm-gesture.md) message.</span></span> <span data-ttu-id="7cdd3-113">A captura de tela a seguir mostra como a amostra parece quando está em execução.</span><span class="sxs-lookup"><span data-stu-id="7cdd3-113">The following screen shot shows how the sample looks when it is running.</span></span>

![captura de tela mostrando os gestos de toque do Windows no exemplo c nítido quando ele está em execução, com um retângulo branco com contorno preto centralizado na tela](images/mtgesturescs.png)

<span data-ttu-id="7cdd3-115">Para este exemplo, as mensagens de gesto são passadas para um mecanismo de gesto que, em seguida, chama métodos em objetos de desenho para converter, girar e dimensionar um objeto que tem métodos para lidar com esses comandos.</span><span class="sxs-lookup"><span data-stu-id="7cdd3-115">For this sample, gesture messages are passed to a gesture engine which then calls methods on drawing objects to translate, rotate, and scale an object that has methods for handling these commands.</span></span> <span data-ttu-id="7cdd3-116">Para tornar isso possível em C#, um formulário especial, TouchableForm, é criado para lidar com mensagens de gestos.</span><span class="sxs-lookup"><span data-stu-id="7cdd3-116">To make this possible in C#, a special form, TouchableForm, is created to handle gesture messages.</span></span> <span data-ttu-id="7cdd3-117">Em seguida, esse formulário usa as mensagens para fazer alterações em um objeto de desenho, Drawingobject, para alterar a forma como o objeto é renderizado no método Paint.</span><span class="sxs-lookup"><span data-stu-id="7cdd3-117">This form then uses the messages to make changes on a drawing object, DrawingObject, to change how the object renders in the Paint method.</span></span>

<span data-ttu-id="7cdd3-118">Para ajudar a mostrar como o exemplo funciona, considere as etapas para usar o comando Pan para converter a caixa renderizada.</span><span class="sxs-lookup"><span data-stu-id="7cdd3-118">To help show how the sample works, consider the steps for using the pan command to translate the rendered box.</span></span> <span data-ttu-id="7cdd3-119">Um usuário executa o gesto de panorâmica que gera uma mensagem de [**WM_GESTURE**](wm-gesture.md) com o identificador de gesto GID_PAN.</span><span class="sxs-lookup"><span data-stu-id="7cdd3-119">A user performs the pan gesture which generates a [**WM_GESTURE**](wm-gesture.md) message with the gesture identifier GID_PAN.</span></span> <span data-ttu-id="7cdd3-120">O TouchableForm lida com essas mensagens e atualiza a posição do objeto de desenho, e o objeto será convertido em si.</span><span class="sxs-lookup"><span data-stu-id="7cdd3-120">The TouchableForm handles this messages and updates the position of the drawing object, and the object will then render itself translated.</span></span>

<span data-ttu-id="7cdd3-121">O código a seguir mostra como o manipulador de gestos recupera os parâmetros da mensagem de [**WM_GESTURE**](wm-gesture.md) e, em seguida, executa a conversão na caixa renderizada por meio de uma chamada para o método move do objeto de desenho.</span><span class="sxs-lookup"><span data-stu-id="7cdd3-121">The following code shows how the gesture handler retrieves parameters from the [**WM_GESTURE**](wm-gesture.md) message and then performs translation on the rendered box through a call to the drawing object's move method.</span></span>

```CSharp
            switch (gi.dwID)
            {
                case GID_BEGIN:
                case GID_END:
                    break;
               (...)
                case GID_PAN:
                    switch (gi.dwFlags)
                    {
                        case GF_BEGIN:
                            _ptFirst.X = gi.ptsLocation.x;
                            _ptFirst.Y = gi.ptsLocation.y;
                            _ptFirst = PointToClient(_ptFirst);
                            break;

                        default:
                            // We read the second point of this gesture. It is a
                            // middle point between fingers in this new position
                            _ptSecond.X = gi.ptsLocation.x;
                            _ptSecond.Y = gi.ptsLocation.y;
                            _ptSecond = PointToClient(_ptSecond);

                            // We apply move operation of the object
                            _dwo.Move(_ptSecond.X - _ptFirst.X, _ptSecond.Y - _ptFirst.Y);

                            Invalidate();

                            // We have to copy second point into first one to
                            // prepare for the next step of this gesture.
                            _ptFirst = _ptSecond;
                            break;
                    }
                    break;
```

<span data-ttu-id="7cdd3-122">O código a seguir mostra como o método move do objeto de desenho atualiza as variáveis de posição internas.</span><span class="sxs-lookup"><span data-stu-id="7cdd3-122">The following code shows how the drawing object's move method updates internal position variables.</span></span>

```CSharp
        public void Move(int deltaX,int deltaY)
        {
            _ptCenter.X += deltaX;
            _ptCenter.Y += deltaY;
        }
```

<span data-ttu-id="7cdd3-123">O código a seguir mostra como a posição é usada no método Paint do objeto de desenho.</span><span class="sxs-lookup"><span data-stu-id="7cdd3-123">The following code shows how the position is used in the drawing object's paint method.</span></span>

```CSharp
public void Paint(Graphics graphics)
        {
(...)
            for (int j = 0; j < 5; j++)
            {
                int idx = arrPts[j].X;
                int idy = arrPts[j].Y;

                // rotation
                arrPts[j].X = (int)(idx * dCos + idy * dSin);
                arrPts[j].Y = (int)(idy * dCos - idx * dSin);

                // translation
                arrPts[j].X += _ptCenter.X;
                arrPts[j].Y += _ptCenter.Y;
            }
(...)
        }
```

<span data-ttu-id="7cdd3-124">Gestos de panorâmica farão com que a caixa de desenho seja renderizada como traduzida.</span><span class="sxs-lookup"><span data-stu-id="7cdd3-124">Pan gestures will cause the drawn box to be rendered translated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cdd3-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7cdd3-125">Related topics</span></span>

<span data-ttu-id="7cdd3-126">[Aplicativo de gestos multitoque (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [aplicativo de gestos multitoque (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), exemplos de [toque do Windows](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="7cdd3-126">[Multi-touch Gestures Application (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [Multi-touch Gestures Application (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
