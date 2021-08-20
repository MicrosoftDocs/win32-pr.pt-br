---
title: Criar um storyboard e adicionar transições
description: Para criar uma animação, um aplicativo deve construir um storyboard.
ms.assetid: e2641c93-e520-4749-a98e-5a58c175fdb9
keywords:
- storyboards Windows Animação, criando
- storyboards Windows Animação, adicionando transições
- transições Windows Animação , criando
- faz transições Windows Animação, adicionando ao storyboard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f992ae7720fea692d5e0b813e6cb9c35fab61d4bf2c781c928d9c8fcd08adb33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999636"
---
# <a name="create-a-storyboard-and-add-transitions"></a>Criar um storyboard e adicionar transições

Para criar uma animação, um aplicativo deve construir um storyboard.

## <a name="overview"></a>Visão geral

As etapas gerais para construir um storyboard são as seguintes:

1.  Criar um storyboard
2.  Criar uma ou mais transições
3.  Adicione as transições para o storyboard, especificando quais variáveis elas animam

Um storyboard vazio pode ser criado usando o gerenciador de animação. O aplicativo deve preencher cada storyboard com transições. Cada transição especifica como uma única variável de animação muda durante um determinado intervalo de tempo. As transições podem ser criadas usando o componente de biblioteca de transição incluído Windows Animation. Como alternativa, um aplicativo pode criar suas próprias transições personalizadas ou usar uma biblioteca de transição de terceiros. Quando o aplicativo adiciona uma transição a um storyboard, ele especifica qual variável de animação a transição animará.

Um storyboard pode incluir transições em uma ou mais variáveis de animação. Storyboards mais complexos podem usar keyframes para sincronizar os inícios ou as extremidades de transições ou especificar partes do storyboard que devem ser repetidas (um número fixo de vezes ou indefinidamente).

## <a name="example-code"></a>Código de exemplo

O código de exemplo a seguir é retirado de MainWindow.cpp no exemplo de animação Windows animação orientada [por temporizador](timer-driven-animation-sample.md); consulte o método CMainWindow::ChangeColor. Este exemplo cria o storyboard (etapa 1) usando o método [**IUIAnimationManager::CreateStoryboard,**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) cria as transições (etapa 2) usando o método [**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) e adiciona as transições ao storyboard (etapa 3) usando o método [**IUIAnimationStoryboard::AddTransition.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition)


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

Antes de iniciar esta etapa, você deve ter concluído esta etapa: [Ler os Valores da Variável de Animação](updating---application-driven-animation.md).

## <a name="next-step"></a>Próxima etapa

Depois de concluir esta etapa, a próxima etapa é: [Agendar um Storyboard.](scheduling-a-storyboard.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IUIAnimationManager::CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard)
</dt> <dt>

[**IUIAnimationStoryboard::AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition)
</dt> <dt>

[**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition)
</dt> <dt>

[Visão geral do storyboard](storyboard-construction.md)
</dt> </dl>

 

 




