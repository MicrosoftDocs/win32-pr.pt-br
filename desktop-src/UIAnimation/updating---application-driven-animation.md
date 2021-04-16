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
# <a name="read-the-animation-variable-values"></a><span data-ttu-id="0bdd6-104">Ler os valores da variável de animação</span><span class="sxs-lookup"><span data-stu-id="0bdd6-104">Read the Animation Variable Values</span></span>

<span data-ttu-id="0bdd6-105">Cada vez que seu aplicativo pinta, ele deve ler os valores atuais das variáveis de animação que representam as características visuais a serem animadas.</span><span class="sxs-lookup"><span data-stu-id="0bdd6-105">Each time your application paints, it should read the current values of the animation variables that represent the visual characteristics to be animated.</span></span>

## <a name="overview"></a><span data-ttu-id="0bdd6-106">Visão geral</span><span class="sxs-lookup"><span data-stu-id="0bdd6-106">Overview</span></span>

<span data-ttu-id="0bdd6-107">Ao desenhar um quadro, um aplicativo pode usar o método [**IUIAnimationVariable:: GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) ou [**IUIAnimationVariable:: getintegervalue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) para solicitar os valores de qualquer variável de animação que afetará visuais dentro do quadro.</span><span class="sxs-lookup"><span data-stu-id="0bdd6-107">When drawing a frame, an application can use the [**IUIAnimationVariable::GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) or [**IUIAnimationVariable::GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) method to request the values of any animation variables that will affect visuals within the frame.</span></span> <span data-ttu-id="0bdd6-108">É possível recortar uma variável de animação para um intervalo de valores ([**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) e [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)) e solicitar que seu valor seja arredondado para um inteiro usando um [**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)(esquema de arredondamento especificado).</span><span class="sxs-lookup"><span data-stu-id="0bdd6-108">It is possible to clip an animation variable to a range of values ([**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) and [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)), and to request its value be rounded to an integer using a specified rounding scheme ([**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)).</span></span>

<span data-ttu-id="0bdd6-109">Em vez de ler os valores de todas as variáveis para cada quadro, um aplicativo pode usar o método [**IUIAnimationVariable:: SetVariableChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) ou [**IUIAnimationVariable:: SetVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) para registrar um ou mais manipuladores de alteração de variável para receber notificações somente quando houver uma alteração no valor das variáveis ([**IUIAnimationVariableChangeHandler:: OnValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged)) ou valor arredondado ([**IUIAnimationVariableIntegerChangeHandler:: OnIntegerValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)).</span><span class="sxs-lookup"><span data-stu-id="0bdd6-109">Instead of reading the values of all variables for every frame, an application can use the [**IUIAnimationVariable::SetVariableChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) or [**IUIAnimationVariable::SetVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) method to register one or more variable change handlers to receive notifications only when there is a change to the variables' value ([**IUIAnimationVariableChangeHandler::OnValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged)) or rounded value ([**IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)).</span></span> <span data-ttu-id="0bdd6-110">Para identificar as variáveis passadas para manipuladores de alteração de variáveis, um aplicativo pode aplicar marcas a variáveis usando o método [**IUIAnimationVariable:: SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) .</span><span class="sxs-lookup"><span data-stu-id="0bdd6-110">To identify the variables passed to variable change handlers, an application can apply tags to variables using the [**IUIAnimationVariable::SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) method.</span></span> <span data-ttu-id="0bdd6-111">Esses são objetos (IUnknown \* ), pares de inteiros que são interpretados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0bdd6-111">These are object (IUnknown\*), integer pairs that are interpreted by the application.</span></span>

## <a name="example-code"></a><span data-ttu-id="0bdd6-112">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="0bdd6-112">Example Code</span></span>

<span data-ttu-id="0bdd6-113">O código de exemplo a seguir é extraído de miniatura. cpp no [layout de grade](/windows/desktop/UIAnimation/grid-layout-sample)de exemplo de animação do Windows; consulte o método CMainWindow:: render.</span><span class="sxs-lookup"><span data-stu-id="0bdd6-113">The following example code is taken from Thumbnail.cpp in the Windows Animation sample [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::Render method.</span></span> <span data-ttu-id="0bdd6-114">Ele usa o método [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) para ler os valores como valores de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="0bdd6-114">It uses the [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) method to read the values as floating-point values.</span></span>


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



<span data-ttu-id="0bdd6-115">O código de exemplo a seguir é extraído de MainWindow. cpp na animação de exemplo de animação [orientada por temporizador](timer-driven-animation-sample.md)do Windows; consulte o método CMainWindow::D rawBackground.</span><span class="sxs-lookup"><span data-stu-id="0bdd6-115">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::DrawBackground method.</span></span> <span data-ttu-id="0bdd6-116">Ele usa o método [**Getinteirovalue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) para ler os valores como valores inteiros.</span><span class="sxs-lookup"><span data-stu-id="0bdd6-116">It uses the [**GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) method to read the values as integer values.</span></span>


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



## <a name="previous-step"></a><span data-ttu-id="0bdd6-117">Etapa anterior</span><span class="sxs-lookup"><span data-stu-id="0bdd6-117">Previous Step</span></span>

<span data-ttu-id="0bdd6-118">Antes de iniciar esta etapa, você deve ter concluído esta etapa: [atualizar o Gerenciador de animação e desenhar quadros](introducing-windows-animation-manager.md).</span><span class="sxs-lookup"><span data-stu-id="0bdd6-118">Before starting this step, you should have completed this step: [Update the Animation Manager and Draw Frames](introducing-windows-animation-manager.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="0bdd6-119">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="0bdd6-119">Next Step</span></span>

<span data-ttu-id="0bdd6-120">Depois de concluir esta etapa, a próxima etapa é: [criar um storyboard e adicionar transições](updating---timer-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="0bdd6-120">After completing this step, the next step is: [Create a Storyboard and Add Transitions](updating---timer-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bdd6-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0bdd6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bdd6-122">**IUIAnimationVariable:: getinteirovalue**</span><span class="sxs-lookup"><span data-stu-id="0bdd6-122">**IUIAnimationVariable::GetIntegerValue**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue)
</dt> <dt>

[<span data-ttu-id="0bdd6-123">**IUIAnimationVariable:: GetValue**</span><span class="sxs-lookup"><span data-stu-id="0bdd6-123">**IUIAnimationVariable::GetValue**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue)
</dt> <dt>

[<span data-ttu-id="0bdd6-124">Visão geral da animação do Windows</span><span class="sxs-lookup"><span data-stu-id="0bdd6-124">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 