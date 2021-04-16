---
title: Ler os valores da variável de animação
description: Cada vez que seu aplicativo pinta, ele deve ler os valores atuais das variáveis de animação que representam as características visuais a serem animadas.
ms.assetid: 7abf084a-31f5-4e32-bfd1-e88fbc2bf63d
keywords:
- variáveis de animação animação do Windows, lendo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16187547bb3efd99a2f45a8fcc0668a6b6603efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105794580"
---
# <a name="read-the-animation-variable-values"></a>Ler os valores da variável de animação

Cada vez que seu aplicativo pinta, ele deve ler os valores atuais das variáveis de animação que representam as características visuais a serem animadas.

## <a name="overview"></a>Visão geral

Ao desenhar um quadro, um aplicativo pode usar o método [**IUIAnimationVariable:: GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) ou [**IUIAnimationVariable:: getintegervalue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) para solicitar os valores de qualquer variável de animação que afetará visuais dentro do quadro. É possível recortar uma variável de animação para um intervalo de valores ([**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) e [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)) e solicitar que seu valor seja arredondado para um inteiro usando um [**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)(esquema de arredondamento especificado).

Em vez de ler os valores de todas as variáveis para cada quadro, um aplicativo pode usar o método [**IUIAnimationVariable:: SetVariableChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) ou [**IUIAnimationVariable:: SetVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) para registrar um ou mais manipuladores de alteração de variável para receber notificações somente quando houver uma alteração no valor das variáveis ([**IUIAnimationVariableChangeHandler:: OnValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged)) ou valor arredondado ([**IUIAnimationVariableIntegerChangeHandler:: OnIntegerValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)). Para identificar as variáveis passadas para manipuladores de alteração de variáveis, um aplicativo pode aplicar marcas a variáveis usando o método [**IUIAnimationVariable:: SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) . Esses são objetos (IUnknown \* ), pares de inteiros que são interpretados pelo aplicativo.

## <a name="example-code"></a>Código de exemplo

O código de exemplo a seguir é extraído de miniatura. cpp no [layout de grade](/windows/desktop/UIAnimation/grid-layout-sample)de exemplo de animação do Windows; consulte o método CMainWindow:: render. Ele usa o método [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) para ler os valores como valores de ponto flutuante.


```C++
// Get the x-coordinate and y-coordinate animation variable values

DOUBLE x=0;
hr = m_pAnimationVariableX->GetValue(&x);
if (SUCCEEDED(hr))
{
    DOUBLE y=0;
    hr = m_pAnimationVariableY->GetValue(&y);
    if (SUCCEEDED(hr))
    {
        // Draw the object

        ...

    }
}
```



O código de exemplo a seguir é extraído de MainWindow. cpp na animação de exemplo de animação [orientada por temporizador](timer-driven-animation-sample.md)do Windows; consulte o método CMainWindow::D rawBackground. Ele usa o método [**Getinteirovalue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) para ler os valores como valores inteiros.


```C++
// Get the RGB animation variable values

INT32 red;
HRESULT hr = m_pAnimationVariableRed->GetIntegerValue(
    &red
    );
if (SUCCEEDED(hr))
{
    INT32 green;
    hr = m_pAnimationVariableGreen->GetIntegerValue(
        &green
        );
    if (SUCCEEDED(hr))
    {
        INT32 blue;
        hr = m_pAnimationVariableBlue->GetIntegerValue(
            &blue
            );
        if (SUCCEEDED(hr))
        {
            // Set the RGB of the background brush to the new animated value

            ...
                
            // Paint the background

            ...

        }
    }

    ...

}
```



## <a name="previous-step"></a>Etapa anterior

Antes de iniciar esta etapa, você deve ter concluído esta etapa: [atualizar o Gerenciador de animação e desenhar quadros](introducing-windows-animation-manager.md).

## <a name="next-step"></a>Próxima etapa

Depois de concluir esta etapa, a próxima etapa é: [criar um storyboard e adicionar transições](updating---timer-driven-animation.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IUIAnimationVariable:: getinteirovalue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue)
</dt> <dt>

[**IUIAnimationVariable:: GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue)
</dt> <dt>

[Visão geral da animação do Windows](scenic-animation-api-overview.md)
</dt> </dl>

 

 