---
title: Windows Gestos de toque no exemplo C (MTGesturesCS)
description: esta seção descreve o exemplo de gestos de toque Windows em C \.
ms.assetid: 4b2d70bb-47e4-4448-97e2-6f6e29d1dfdf
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
ms.openlocfilehash: ac3a7c0772ad7329d14d9909b55f8a60ef6e7d7473a06fcba921297117a00b6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089896"
---
# <a name="windows-touch-gestures-in-c-sample-mtgesturescs"></a>Windows Gestos de toque no exemplo de C# (MTGesturesCS)

esta seção descreve o exemplo de gestos de toque Windows em C#.

este exemplo Windows gestos de toque demonstra como usar mensagens de gesto para converter, girar e dimensionar uma caixa renderizada pelo Graphics Device Interface (GDI) manipulando a mensagem [**WM_GESTURE**](wm-gesture.md) . A captura de tela a seguir mostra como a amostra parece quando está em execução.

![captura de tela mostrando os gestos de toque do Windows no exemplo c nítido quando ele está em execução, com um retângulo branco com contorno preto centralizado na tela](images/mtgesturescs.png)

Para este exemplo, as mensagens de gesto são passadas para um mecanismo de gesto que, em seguida, chama métodos em objetos de desenho para converter, girar e dimensionar um objeto que tem métodos para lidar com esses comandos. Para tornar isso possível em C#, um formulário especial, TouchableForm, é criado para lidar com mensagens de gestos. em seguida, esse formulário usa as mensagens para fazer alterações em um objeto de desenho, drawingobject, para alterar a forma como o objeto é renderizado no método Paint.

Para ajudar a mostrar como o exemplo funciona, considere as etapas para usar o comando Pan para converter a caixa renderizada. Um usuário executa o gesto de panorâmica que gera uma mensagem de [**WM_GESTURE**](wm-gesture.md) com o identificador de gesto GID_PAN. O TouchableForm lida com essas mensagens e atualiza a posição do objeto de desenho, e o objeto será convertido em si.

O código a seguir mostra como o manipulador de gestos recupera os parâmetros da mensagem de [**WM_GESTURE**](wm-gesture.md) e, em seguida, executa a conversão na caixa renderizada por meio de uma chamada para o método move do objeto de desenho.

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

O código a seguir mostra como o método move do objeto de desenho atualiza as variáveis de posição internas.

```CSharp
        public void Move(int deltaX,int deltaY)
        {
            _ptCenter.X += deltaX;
            _ptCenter.Y += deltaY;
        }
```

O código a seguir mostra como a posição é usada no método Paint do objeto de desenho.

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

Gestos de panorâmica farão com que a caixa de desenho seja renderizada como traduzida.

## <a name="related-topics"></a>Tópicos relacionados

[aplicativo de gestos multitoque (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [aplicativo de gestos multitoque (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows toque em exemplos](windows-touch-samples.md)
