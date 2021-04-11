---
title: Criar um storyboard e adicionar transições
description: Para criar uma animação, um aplicativo deve construir um Storyboard.
ms.assetid: e2641c93-e520-4749-a98e-5a58c175fdb9
keywords:
- Animação de storyboards do Windows, criando
- Animação de storyboards do Windows, adicionando transições
- faz a transição da animação do Windows, criando
- faz a transição da animação do Windows, adicionando ao storyboard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee85aac4db11371c9a1e4a2aa254421d217cfd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292601"
---
# <a name="create-a-storyboard-and-add-transitions"></a>Criar um storyboard e adicionar transições

Para criar uma animação, um aplicativo deve construir um Storyboard.

## <a name="overview"></a>Visão geral

As etapas gerais para construir um storyboard são as seguintes:

1.  Criar um storyboard
2.  Criar uma ou mais transições
3.  Adicionar as transições ao storyboard, especificando quais variáveis eles animam

Um storyboard vazio pode ser criado usando o Gerenciador de animação. O aplicativo deve preencher cada Storyboard com transições. Cada transição especifica como uma variável de animação única é alterada em um determinado intervalo de tempo. As transições podem ser criadas usando o componente de biblioteca de transição incluído na animação do Windows. Como alternativa, um aplicativo pode criar suas próprias transições personalizadas ou usar uma biblioteca de transição de terceiros. Quando o aplicativo adiciona uma transição a um storyboard, ele especifica a variável de animação que a transição irá animar.

Um storyboard pode incluir transições em uma ou mais variáveis de animação. Storyboards mais complexos podem usar quadros-chave para sincronizar o início ou o fim das transições ou para especificar partes do Storyboard que devem se repetir (um número fixo de vezes ou indefinidamente).

## <a name="example-code"></a>Código de exemplo

O código de exemplo a seguir é extraído de MainWindow. cpp na animação de exemplo de animação [orientada por temporizador](timer-driven-animation-sample.md)do Windows; consulte o método CMainWindow:: ChangeColor. Este exemplo cria o storyboard (etapa 1) usando o método [**IUIAnimationManager:: createstoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) , cria as transições (etapa 2) usando o método [**IUIAnimationTransitionLibrary:: CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) e adiciona as transições ao storyboard (etapa 3) usando o método [**IUIAnimationStoryboard:: addtransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) .


```C++
const UI_ANIMATION_SECONDS DURATION = 0.5;
const DOUBLE ACCELERATION_RATIO = 0.5;
const DOUBLE DECELERATION_RATIO = 0.5;

// Create a storyboard

IUIAnimationStoryboard *pStoryboard = NULL;
HRESULT hr = m_pAnimationManager->CreateStoryboard(
    &pStoryboard
    );
if (SUCCEEDED(hr))
{
    // Create transitions for the RGB animation variables

    IUIAnimationTransition *pTransitionRed;
    hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
        DURATION,
        red,
        ACCELERATION_RATIO,
        DECELERATION_RATIO,
        &pTransitionRed
        );
    if (SUCCEEDED(hr))
    {
        IUIAnimationTransition *pTransitionGreen;
        hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
            DURATION,
            green,
            ACCELERATION_RATIO,
            DECELERATION_RATIO,
            &pTransitionGreen
            );
        if (SUCCEEDED(hr))
        {
            IUIAnimationTransition *pTransitionBlue;
            hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
                DURATION,
                blue,
                ACCELERATION_RATIO,
                DECELERATION_RATIO,
                &pTransitionBlue
                );
            if (SUCCEEDED(hr))
            {
                // Add transitions to the storyboard

                hr = pStoryboard->AddTransition(
                    m_pAnimationVariableRed,
                    pTransitionRed
                    );
                if (SUCCEEDED(hr))
                {
                    hr = pStoryboard->AddTransition(
                        m_pAnimationVariableGreen,
                        pTransitionGreen
                        );
                    if (SUCCEEDED(hr))
                    {
                        hr = pStoryboard->AddTransition(
                            m_pAnimationVariableBlue,
                            pTransitionBlue
                            );
                        if (SUCCEEDED(hr))
                        {
                            // Get the current time and schedule the storyboard for play

                            ...

}
```



## <a name="previous-step"></a>Etapa anterior

Antes de iniciar esta etapa, você deve ter concluído esta etapa: [ler os valores da variável de animação](updating---application-driven-animation.md).

## <a name="next-step"></a>Próxima etapa

Depois de concluir esta etapa, a próxima etapa é: [agendar um storyboard](scheduling-a-storyboard.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IUIAnimationManager:: createstoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard)
</dt> <dt>

[**IUIAnimationStoryboard:: addtransição**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition)
</dt> <dt>

[**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition)
</dt> <dt>

[Visão geral do storyboard](storyboard-construction.md)
</dt> </dl>

 

 




