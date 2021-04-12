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
# <a name="create-animation-variables"></a><span data-ttu-id="45470-104">Criar variáveis de animação</span><span class="sxs-lookup"><span data-stu-id="45470-104">Create Animation Variables</span></span>

<span data-ttu-id="45470-105">Um aplicativo deve criar uma variável de animação para cada característica visual que seja animada usando a animação do Windows.</span><span class="sxs-lookup"><span data-stu-id="45470-105">An application must create an animation variable for each visual characteristic that is to be animated using Windows Animation.</span></span>

## <a name="overview"></a><span data-ttu-id="45470-106">Visão geral</span><span class="sxs-lookup"><span data-stu-id="45470-106">Overview</span></span>

<span data-ttu-id="45470-107">As variáveis de animação são criadas usando o Gerenciador de animação, e o aplicativo deve reter uma referência para cada, desde que seja necessário.</span><span class="sxs-lookup"><span data-stu-id="45470-107">Animation variables are created using the animation manager, and the application should retain a reference to each for as long as it is needed.</span></span> <span data-ttu-id="45470-108">Seu aplicativo geralmente criará cada variável de animação ao mesmo tempo que o objeto visual que ele anima.</span><span class="sxs-lookup"><span data-stu-id="45470-108">Your application will generally create each animation variable at the same time as the visual object it animates.</span></span>

<span data-ttu-id="45470-109">Quando uma variável de animação é criada, seu valor inicial deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="45470-109">When an animation variable is created, its initial value must be specified.</span></span> <span data-ttu-id="45470-110">Depois disso, seu valor só pode ser alterado agendando storyboards que o animam.</span><span class="sxs-lookup"><span data-stu-id="45470-110">Thereafter, its value can only be altered by scheduling storyboards that animate it.</span></span>

<span data-ttu-id="45470-111">As variáveis de animação são passadas como parâmetros quando os storyboards são construídos, portanto, o aplicativo não deve liberá-las até que as características visuais que elas representam não precisem mais ser animadas, normalmente quando os objetos visuais associados estão prestes a serem destruídos.</span><span class="sxs-lookup"><span data-stu-id="45470-111">Animation variables are passed as parameters when storyboards are constructed, so the application should not release them until the visual characteristics they represent no longer need to be animated, typically when the associated visual objects are about to be destroyed.</span></span>

## <a name="example-code"></a><span data-ttu-id="45470-112">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="45470-112">Example Code</span></span>

-   [<span data-ttu-id="45470-113">Animação de cores</span><span class="sxs-lookup"><span data-stu-id="45470-113">Animating Colors</span></span>](#animating-colors)
-   [<span data-ttu-id="45470-114">Animando coordenadas x e y</span><span class="sxs-lookup"><span data-stu-id="45470-114">Animating x and y Coordinates</span></span>](#animating-x-and-y-coordinates)

### <a name="animating-colors"></a><span data-ttu-id="45470-115">Animação de cores</span><span class="sxs-lookup"><span data-stu-id="45470-115">Animating Colors</span></span>

<span data-ttu-id="45470-116">O código de exemplo a seguir é extraído de MainWindow. cpp [na animação de](application-driven-animation-sample.md) exemplos de animação do Windows e [animação orientada por temporizador](timer-driven-animation-sample.md).</span><span class="sxs-lookup"><span data-stu-id="45470-116">The following example code is taken from MainWindow.cpp in the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="45470-117">No exemplo, três variáveis de animação são criadas usando [**CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) para representar cores de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="45470-117">In the example, three animation variables are created using [**CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) to represent background colors.</span></span> <span data-ttu-id="45470-118">O código também usa os métodos [**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) e [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) para controlar o valor da variável de animação.</span><span class="sxs-lookup"><span data-stu-id="45470-118">The code also uses the [**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) and [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) methods to control the value of the animation variable.</span></span>


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



<span data-ttu-id="45470-119">Observe as seguintes definições de MainWindow. h.</span><span class="sxs-lookup"><span data-stu-id="45470-119">Note the following definitions from MainWindow.h.</span></span>


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



### <a name="animating-x-and-y-coordinates"></a><span data-ttu-id="45470-120">Animando coordenadas x e y</span><span class="sxs-lookup"><span data-stu-id="45470-120">Animating x and y Coordinates</span></span>

<span data-ttu-id="45470-121">O código de exemplo a seguir é extraído de thumbnail. cpp no [exemplo de layout da grade](/windows/desktop/UIAnimation/grid-layout-sample)de animação do Windows; consulte o método CMainWindow:: CreateAnimationVariables.</span><span class="sxs-lookup"><span data-stu-id="45470-121">The following example code is taken from Thumbnail.cpp in the Windows Animation [Grid Layout Sample](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::CreateAnimationVariables method.</span></span> <span data-ttu-id="45470-122">Duas variáveis de animação são criadas para representar as coordenadas X e Y de cada objeto.</span><span class="sxs-lookup"><span data-stu-id="45470-122">Two animation variables are created to represent the X and Y coordinates of each object.</span></span>


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



<span data-ttu-id="45470-123">Observe as seguintes definições de thumbnail. h.</span><span class="sxs-lookup"><span data-stu-id="45470-123">Note the following definitions from Thumbnail.h.</span></span>


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



<span data-ttu-id="45470-124">As variáveis de animação são números de ponto flutuante, mas seus valores também podem ser buscados como inteiros.</span><span class="sxs-lookup"><span data-stu-id="45470-124">Animation variables are floating-point numbers, but their values can be fetched as integers, too.</span></span> <span data-ttu-id="45470-125">Por padrão, cada valor será arredondado para o número inteiro mais próximo, mas é possível substituir o modo de arredondamento usado para uma variável.</span><span class="sxs-lookup"><span data-stu-id="45470-125">By default, each value will be rounded to the nearest integer, but it is possible to override the rounding mode used for a variable.</span></span> <span data-ttu-id="45470-126">O código de exemplo a seguir usa o método [**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) para especificar que os valores sempre devem ser arredondados para baixo.</span><span class="sxs-lookup"><span data-stu-id="45470-126">The following example code uses the [**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) method to specify that the values should always be rounded down.</span></span>


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



## <a name="previous-step"></a><span data-ttu-id="45470-127">Etapa anterior</span><span class="sxs-lookup"><span data-stu-id="45470-127">Previous Step</span></span>

<span data-ttu-id="45470-128">Antes de iniciar esta etapa, você deve ter concluído esta etapa: [criar os objetos de animação principais](adding-animation-to-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="45470-128">Before starting this step, you should have completed this step: [Create the Main Animation Objects](adding-animation-to-an-application.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="45470-129">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="45470-129">Next Step</span></span>

<span data-ttu-id="45470-130">Depois de concluir esta etapa, a próxima etapa é: [atualizar o Gerenciador de animação e desenhar quadros](introducing-windows-animation-manager.md).</span><span class="sxs-lookup"><span data-stu-id="45470-130">After completing this step, the next step is: [Update the Animation Manager and Draw Frames](introducing-windows-animation-manager.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="45470-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="45470-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45470-132">**IUIAnimationManager::CreateAnimationVariable**</span><span class="sxs-lookup"><span data-stu-id="45470-132">**IUIAnimationManager::CreateAnimationVariable**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable)
</dt> <dt>

[<span data-ttu-id="45470-133">**IUIAnimationVariable::SetLowerBound**</span><span class="sxs-lookup"><span data-stu-id="45470-133">**IUIAnimationVariable::SetLowerBound**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound)
</dt> <dt>

[<span data-ttu-id="45470-134">**IUIAnimationVariable::SetRoundingMode**</span><span class="sxs-lookup"><span data-stu-id="45470-134">**IUIAnimationVariable::SetRoundingMode**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)
</dt> <dt>

[<span data-ttu-id="45470-135">**IUIAnimationVariable::SetUpperBound**</span><span class="sxs-lookup"><span data-stu-id="45470-135">**IUIAnimationVariable::SetUpperBound**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)
</dt> <dt>

[<span data-ttu-id="45470-136">Visão geral da animação do Windows</span><span class="sxs-lookup"><span data-stu-id="45470-136">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 