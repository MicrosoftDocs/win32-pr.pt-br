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
# <a name="create-a-storyboard-and-add-transitions"></a><span data-ttu-id="05dea-107">Criar um storyboard e adicionar transições</span><span class="sxs-lookup"><span data-stu-id="05dea-107">Create a Storyboard and Add Transitions</span></span>

<span data-ttu-id="05dea-108">Para criar uma animação, um aplicativo deve construir um Storyboard.</span><span class="sxs-lookup"><span data-stu-id="05dea-108">To create an animation, an application must construct a storyboard.</span></span>

## <a name="overview"></a><span data-ttu-id="05dea-109">Visão geral</span><span class="sxs-lookup"><span data-stu-id="05dea-109">Overview</span></span>

<span data-ttu-id="05dea-110">As etapas gerais para construir um storyboard são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="05dea-110">The general steps for constructing a storyboard are as follows:</span></span>

1.  <span data-ttu-id="05dea-111">Criar um storyboard</span><span class="sxs-lookup"><span data-stu-id="05dea-111">Create a storyboard</span></span>
2.  <span data-ttu-id="05dea-112">Criar uma ou mais transições</span><span class="sxs-lookup"><span data-stu-id="05dea-112">Create one or more transitions</span></span>
3.  <span data-ttu-id="05dea-113">Adicionar as transições ao storyboard, especificando quais variáveis eles animam</span><span class="sxs-lookup"><span data-stu-id="05dea-113">Add the transitions to the storyboard, specifying which variables they animate</span></span>

<span data-ttu-id="05dea-114">Um storyboard vazio pode ser criado usando o Gerenciador de animação.</span><span class="sxs-lookup"><span data-stu-id="05dea-114">An empty storyboard can be created using the animation manager.</span></span> <span data-ttu-id="05dea-115">O aplicativo deve preencher cada Storyboard com transições.</span><span class="sxs-lookup"><span data-stu-id="05dea-115">The application must populate each storyboard with transitions.</span></span> <span data-ttu-id="05dea-116">Cada transição especifica como uma variável de animação única é alterada em um determinado intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="05dea-116">Each transition specifies how a single animation variable changes over a given time interval.</span></span> <span data-ttu-id="05dea-117">As transições podem ser criadas usando o componente de biblioteca de transição incluído na animação do Windows.</span><span class="sxs-lookup"><span data-stu-id="05dea-117">Transitions can be created using the transition library component included in Windows Animation.</span></span> <span data-ttu-id="05dea-118">Como alternativa, um aplicativo pode criar suas próprias transições personalizadas ou usar uma biblioteca de transição de terceiros.</span><span class="sxs-lookup"><span data-stu-id="05dea-118">Alternately, an application can create its own custom transitions or use a transition library from a third party.</span></span> <span data-ttu-id="05dea-119">Quando o aplicativo adiciona uma transição a um storyboard, ele especifica a variável de animação que a transição irá animar.</span><span class="sxs-lookup"><span data-stu-id="05dea-119">When the application adds a transition to a storyboard, it specifies which animation variable the transition will animate.</span></span>

<span data-ttu-id="05dea-120">Um storyboard pode incluir transições em uma ou mais variáveis de animação.</span><span class="sxs-lookup"><span data-stu-id="05dea-120">A storyboard may include transitions on one or more animation variables.</span></span> <span data-ttu-id="05dea-121">Storyboards mais complexos podem usar quadros-chave para sincronizar o início ou o fim das transições ou para especificar partes do Storyboard que devem se repetir (um número fixo de vezes ou indefinidamente).</span><span class="sxs-lookup"><span data-stu-id="05dea-121">More complex storyboards can use keyframes to synchronize the starts or ends of transitions, or to specify portions of the storyboard that should repeat (a fixed number of times or indefinitely).</span></span>

## <a name="example-code"></a><span data-ttu-id="05dea-122">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="05dea-122">Example Code</span></span>

<span data-ttu-id="05dea-123">O código de exemplo a seguir é extraído de MainWindow. cpp na animação de exemplo de animação [orientada por temporizador](timer-driven-animation-sample.md)do Windows; consulte o método CMainWindow:: ChangeColor.</span><span class="sxs-lookup"><span data-stu-id="05dea-123">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::ChangeColor method.</span></span> <span data-ttu-id="05dea-124">Este exemplo cria o storyboard (etapa 1) usando o método [**IUIAnimationManager:: createstoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) , cria as transições (etapa 2) usando o método [**IUIAnimationTransitionLibrary:: CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) e adiciona as transições ao storyboard (etapa 3) usando o método [**IUIAnimationStoryboard:: addtransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) .</span><span class="sxs-lookup"><span data-stu-id="05dea-124">This example creates the storyboard (step 1) using the [**IUIAnimationManager::CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) method, creates the transitions (step 2) using the [**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) method, and adds the transitions to the storyboard (step 3) using the [**IUIAnimationStoryboard::AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) method.</span></span>


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



## <a name="previous-step"></a><span data-ttu-id="05dea-125">Etapa anterior</span><span class="sxs-lookup"><span data-stu-id="05dea-125">Previous Step</span></span>

<span data-ttu-id="05dea-126">Antes de iniciar esta etapa, você deve ter concluído esta etapa: [ler os valores da variável de animação](updating---application-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="05dea-126">Before starting this step, you should have completed this step: [Read the Animation Variable Values](updating---application-driven-animation.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="05dea-127">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="05dea-127">Next Step</span></span>

<span data-ttu-id="05dea-128">Depois de concluir esta etapa, a próxima etapa é: [agendar um storyboard](scheduling-a-storyboard.md).</span><span class="sxs-lookup"><span data-stu-id="05dea-128">After completing this step, the next step is: [Schedule a Storyboard](scheduling-a-storyboard.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="05dea-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="05dea-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05dea-130">**IUIAnimationManager:: createstoryboard**</span><span class="sxs-lookup"><span data-stu-id="05dea-130">**IUIAnimationManager::CreateStoryboard**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard)
</dt> <dt>

[<span data-ttu-id="05dea-131">**IUIAnimationStoryboard:: addtransição**</span><span class="sxs-lookup"><span data-stu-id="05dea-131">**IUIAnimationStoryboard::AddTransition**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition)
</dt> <dt>

[<span data-ttu-id="05dea-132">**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**</span><span class="sxs-lookup"><span data-stu-id="05dea-132">**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition)
</dt> <dt>

[<span data-ttu-id="05dea-133">Visão geral do storyboard</span><span class="sxs-lookup"><span data-stu-id="05dea-133">Storyboard Overview</span></span>](storyboard-construction.md)
</dt> </dl>

 

 




