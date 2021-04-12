---
title: Criar variáveis de animação
description: Um aplicativo deve criar uma variável de animação para cada característica visual que seja animada usando a animação do Windows.
ms.assetid: 360aa157-cb50-400a-b373-45885410469d
keywords:
- variáveis de animação animação do Windows, criando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c059a924e22700bb4abd794435ad708a2775a9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366525"
---
# <a name="create-animation-variables"></a>Criar variáveis de animação

Um aplicativo deve criar uma variável de animação para cada característica visual que seja animada usando a animação do Windows.

## <a name="overview"></a>Visão geral

As variáveis de animação são criadas usando o Gerenciador de animação, e o aplicativo deve reter uma referência para cada, desde que seja necessário. Seu aplicativo geralmente criará cada variável de animação ao mesmo tempo que o objeto visual que ele anima.

Quando uma variável de animação é criada, seu valor inicial deve ser especificado. Depois disso, seu valor só pode ser alterado agendando storyboards que o animam.

As variáveis de animação são passadas como parâmetros quando os storyboards são construídos, portanto, o aplicativo não deve liberá-las até que as características visuais que elas representam não precisem mais ser animadas, normalmente quando os objetos visuais associados estão prestes a serem destruídos.

## <a name="example-code"></a>Código de exemplo

-   [Animação de cores](#animating-colors)
-   [Animando coordenadas x e y](#animating-x-and-y-coordinates)

### <a name="animating-colors"></a>Animação de cores

O código de exemplo a seguir é extraído de MainWindow. cpp [na animação de](application-driven-animation-sample.md) exemplos de animação do Windows e [animação orientada por temporizador](timer-driven-animation-sample.md). No exemplo, três variáveis de animação são criadas usando [**CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) para representar cores de plano de fundo. O código também usa os métodos [**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) e [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) para controlar o valor da variável de animação.


```
const DOUBLE INITIAL_RED = COLOR_MAX;
const DOUBLE INITIAL_GREEN = COLOR_MAX;
const DOUBLE INITIAL_BLUE = COLOR_MAX;

HRESULT hr = m_pAnimationManager->CreateAnimationVariable(
    INITIAL_RED,
    &m_pAnimationVariableRed
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationVariableRed->SetLowerBound(COLOR_MIN);
    if (SUCCEEDED(hr))
    {
        hr = m_pAnimationVariableRed->SetUpperBound(COLOR_MAX);
        if (SUCCEEDED(hr))
        {
            hr = m_pAnimationManager->CreateAnimationVariable(
                INITIAL_GREEN,
                &m_pAnimationVariableGreen
                );
            if (SUCCEEDED(hr))
            {
                hr = m_pAnimationVariableGreen->SetLowerBound(COLOR_MIN);
                if (SUCCEEDED(hr))
                {
                    hr = m_pAnimationVariableGreen->SetUpperBound(COLOR_MAX);
                    if (SUCCEEDED(hr))
                    {
                        hr = m_pAnimationManager->CreateAnimationVariable(
                            INITIAL_BLUE,
                            &m_pAnimationVariableBlue
                            );
                        if (SUCCEEDED(hr))
                        {
                            hr = m_pAnimationVariableBlue->SetLowerBound(COLOR_MIN);
                            if (SUCCEEDED(hr))
                            {
                                hr = m_pAnimationVariableBlue->SetUpperBound(COLOR_MAX);
                            }
                        }
                    }
                }
            }
        }
    }
}
```



Observe as seguintes definições de MainWindow. h.


```
class CMainWindow
{

    ...

private:

    // Animated Variables

    IUIAnimationVariable *m_pAnimationVariableRed;
    IUIAnimationVariable *m_pAnimationVariableGreen;
    IUIAnimationVariable *m_pAnimationVariableBlue;

    ...

};
```



### <a name="animating-x-and-y-coordinates"></a>Animando coordenadas x e y

O código de exemplo a seguir é extraído de thumbnail. cpp no [exemplo de layout da grade](/windows/desktop/UIAnimation/grid-layout-sample)de animação do Windows; consulte o método CMainWindow:: CreateAnimationVariables. Duas variáveis de animação são criadas para representar as coordenadas X e Y de cada objeto.


```C++
// Create the animation variables for the x and y coordinates

hr = m_pAnimationManager->CreateAnimationVariable(
    xInitial,
    &m_pAnimationVariableX
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->CreateAnimationVariable(
        yInitial,
        &m_pAnimationVariableY
        );

    ...

}
```



Observe as seguintes definições de thumbnail. h.


```
class CThumbnail
{
public:

    ...

    // X and Y Animation Variables

    IUIAnimationVariable *m_pAnimationVariableX;
    IUIAnimationVariable *m_pAnimationVariableY;

    ...

};
```



As variáveis de animação são números de ponto flutuante, mas seus valores também podem ser buscados como inteiros. Por padrão, cada valor será arredondado para o número inteiro mais próximo, mas é possível substituir o modo de arredondamento usado para uma variável. O código de exemplo a seguir usa o método [**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) para especificar que os valores sempre devem ser arredondados para baixo.


```C++
hr = m_pAnimationVariableX->SetRoundingMode(
    UI_ANIMATION_ROUNDING_MODE_FLOOR
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationVariableY->SetRoundingMode(
        UI_ANIMATION_ROUNDING_MODE_FLOOR
        );

    ...

}
```



## <a name="previous-step"></a>Etapa anterior

Antes de iniciar esta etapa, você deve ter concluído esta etapa: [criar os objetos de animação principais](adding-animation-to-an-application.md).

## <a name="next-step"></a>Próxima etapa

Depois de concluir esta etapa, a próxima etapa é: [atualizar o Gerenciador de animação e desenhar quadros](introducing-windows-animation-manager.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IUIAnimationManager::CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable)
</dt> <dt>

[**IUIAnimationVariable::SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound)
</dt> <dt>

[**IUIAnimationVariable::SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)
</dt> <dt>

[**IUIAnimationVariable::SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)
</dt> <dt>

[Visão geral da animação do Windows](scenic-animation-api-overview.md)
</dt> </dl>

 

 