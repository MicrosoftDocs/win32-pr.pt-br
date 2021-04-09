---
title: Atualizar o Gerenciador de animação e desenhar quadros
description: Cada vez que um aplicativo agenda um storyboard, o aplicativo deve fornecer a hora atual ao Gerenciador de animação.
ms.assetid: c4f746c3-e47c-4b82-a41b-e2c0d177d097
keywords:
- objetos do Gerenciador de animação animação do Windows, atualizando
- Animação de objetos de temporizador de animação do Windows, conectando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9a48e8d6e273174e502c374727e69b61bc478d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007648"
---
# <a name="update-the-animation-manager-and-draw-frames"></a><span data-ttu-id="28ea9-105">Atualizar o Gerenciador de animação e desenhar quadros</span><span class="sxs-lookup"><span data-stu-id="28ea9-105">Update the Animation Manager and Draw Frames</span></span>

<span data-ttu-id="28ea9-106">Cada vez que um aplicativo agenda um storyboard, o aplicativo deve fornecer a hora atual ao Gerenciador de animação.</span><span class="sxs-lookup"><span data-stu-id="28ea9-106">Each time an application schedules a storyboard, the application must supply the current time to the animation manager.</span></span> <span data-ttu-id="28ea9-107">A hora atual também é necessária ao direcionar o Gerenciador de animação para atualizar seu estado e definir todas as variáveis de animação para os valores interpolados apropriados.</span><span class="sxs-lookup"><span data-stu-id="28ea9-107">The current time is also required when directing the animation manager to update its state and set all animation variables to the appropriate interpolated values.</span></span>

## <a name="overview"></a><span data-ttu-id="28ea9-108">Visão geral</span><span class="sxs-lookup"><span data-stu-id="28ea9-108">Overview</span></span>

<span data-ttu-id="28ea9-109">Há duas configurações com suporte na animação do Windows: animação orientada por aplicativo e animação orientada por temporizador.</span><span class="sxs-lookup"><span data-stu-id="28ea9-109">There are two configurations supported by Windows Animation: application-driven animation and timer-driven animation.</span></span>

<span data-ttu-id="28ea9-110">Para usar a animação orientada por aplicativo em seu aplicativo, você deve atualizar o Gerenciador de animação antes de desenhar cada quadro e usar um mecanismo apropriado para desenhar quadros com frequência suficiente para animação.</span><span class="sxs-lookup"><span data-stu-id="28ea9-110">To use application-driven animation in your application, you must update the animation manager before drawing each frame and use an appropriate mechanism to draw frames frequently enough for animation.</span></span> <span data-ttu-id="28ea9-111">Um aplicativo que usa animação orientada por aplicativo pode usar qualquer mecanismo para determinar a hora atual, mas o objeto de temporizador de animação do Windows retorna um tempo preciso nas unidades aceitas pelo Gerenciador de animação.</span><span class="sxs-lookup"><span data-stu-id="28ea9-111">An application using application-driven animation can use any mechanism to determine the current time, but the Windows Animation timer object returns a precise time in the units accepted by the animation manager.</span></span> <span data-ttu-id="28ea9-112">Para evitar um desenho desnecessário quando nenhuma animação estiver sendo executada, você também deverá fornecer um manipulador de eventos de gerente para iniciar o redesenho quando as animações forem agendadas e verificar depois de cada quadro se o redesenho pode ser suspenso.</span><span class="sxs-lookup"><span data-stu-id="28ea9-112">To avoid unnecessary drawing when no animations are playing, you should also provide a manager event handler to start redrawing when animations are scheduled and check after each frame whether redrawing can be suspended.</span></span> <span data-ttu-id="28ea9-113">Para obter mais informações, consulte [animação orientada por aplicativo](scenic-animation-api-overview.md).</span><span class="sxs-lookup"><span data-stu-id="28ea9-113">For more information, see [Application-Driven Animation](scenic-animation-api-overview.md).</span></span>

<span data-ttu-id="28ea9-114">Na configuração controlada por aplicativo, um aplicativo pode chamar o método [**IUIAnimationManager:: GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) para verificar se as animações estão agendadas no momento e continuam a desenhar quadros se estiverem.</span><span class="sxs-lookup"><span data-stu-id="28ea9-114">In the application-driven configuration, an application can call the [**IUIAnimationManager::GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) method to verify that animations are currently scheduled and continue to draw frames if they are.</span></span> <span data-ttu-id="28ea9-115">Como o redesenho é interrompido quando não há animações agendadas, é necessário reiniciá-lo na próxima vez que uma animação for agendada.</span><span class="sxs-lookup"><span data-stu-id="28ea9-115">Because redrawing stops when there are no animations scheduled, it is necessary to restart it the next time an animation is scheduled.</span></span> <span data-ttu-id="28ea9-116">Um aplicativo pode registrar um manipulador de eventos de Gerenciador para ser notificado quando o status do Gerenciador de animação mudar de ocioso (nenhuma animação está agendada no momento) para ocupado.</span><span class="sxs-lookup"><span data-stu-id="28ea9-116">An application can register a manager event handler to be notified when the status of the animation manager changes from idle (no animations are currently scheduled) to busy.</span></span>

<span data-ttu-id="28ea9-117">Para usar a animação orientada por temporizador em seu aplicativo, você deve conectar o Gerenciador de animação a um temporizador de animação e fornecer um manipulador de eventos de temporizador.</span><span class="sxs-lookup"><span data-stu-id="28ea9-117">To use timer-driven animation in your application, you must connect the animation manager to an animation timer and provide a timer event handler.</span></span> <span data-ttu-id="28ea9-118">Quando o Gerenciador de animação está conectado a um temporizador, o temporizador pode informar ao gerente quando o estado da animação deve ser atualizado à medida que o tempo progride.</span><span class="sxs-lookup"><span data-stu-id="28ea9-118">When the animation manager is connected to a timer, the timer can tell the manager when the animation state should be updated as time progresses.</span></span> <span data-ttu-id="28ea9-119">O aplicativo deve desenhar um quadro para cada tique-timer.</span><span class="sxs-lookup"><span data-stu-id="28ea9-119">The application should draw a frame for each timer tick.</span></span> <span data-ttu-id="28ea9-120">O Gerenciador de animação pode, por sua vez, dizer ao temporizador quando há animações sendo executadas, portanto, o temporizador pode desligar fora durante períodos ociosos quando o redesenho é desnecessário.</span><span class="sxs-lookup"><span data-stu-id="28ea9-120">The animation manager can in turn tell the timer when there are animations playing, so the timer can shut itself off during idle periods when redrawing is unnecessary.</span></span> <span data-ttu-id="28ea9-121">Para evitar o desenho desnecessário quando nenhuma animação está sendo executada, você deve configurar o temporizador para se desabilitá-lo automaticamente.</span><span class="sxs-lookup"><span data-stu-id="28ea9-121">To avoid unnecessary drawing when no animations are playing, you should configure the timer to disable itself automatically.</span></span> <span data-ttu-id="28ea9-122">Para obter mais informações, consulte [animação orientada por temporizador](scenic-animation-api-overview.md).</span><span class="sxs-lookup"><span data-stu-id="28ea9-122">For more information, see [Timer-Driven Animation](scenic-animation-api-overview.md).</span></span>

## <a name="example-code"></a><span data-ttu-id="28ea9-123">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="28ea9-123">Example Code</span></span>

-   [<span data-ttu-id="28ea9-124">Animação orientada por aplicativo</span><span class="sxs-lookup"><span data-stu-id="28ea9-124">Application-Driven Animation</span></span>](#application-driven-animation)
-   [<span data-ttu-id="28ea9-125">Animação orientada por temporizador</span><span class="sxs-lookup"><span data-stu-id="28ea9-125">Timer-Driven Animation</span></span>](#timer-driven-animation)

### <a name="application-driven-animation"></a><span data-ttu-id="28ea9-126">Application-Driven animação</span><span class="sxs-lookup"><span data-stu-id="28ea9-126">Application-Driven Animation</span></span>

<span data-ttu-id="28ea9-127">O código de exemplo a seguir é extraído de ManagerEventHandler. h da [animação](application-driven-animation-sample.md) de exemplos de animação do Windows e [layout de grade](/windows/desktop/UIAnimation/grid-layout-sample).</span><span class="sxs-lookup"><span data-stu-id="28ea9-127">The following example code is taken from ManagerEventHandler.h from the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample).</span></span> <span data-ttu-id="28ea9-128">Ele define o manipulador de eventos de Gerenciador.</span><span class="sxs-lookup"><span data-stu-id="28ea9-128">It defines the manager event handler.</span></span>


```C++
#include "UIAnimationHelper.h"

// Event handler object for manager status changes

class CManagerEventHandler :
    public CUIAnimationManagerEventHandlerBase<CManagerEventHandler>
{
public:

    static HRESULT
    CreateInstance
    (
        CMainWindow *pMainWindow,
        IUIAnimationManagerEventHandler **ppManagerEventHandler
    ) throw()
    {
        CManagerEventHandler *pManagerEventHandler;
        HRESULT hr = CUIAnimationCallbackBase::CreateInstance(
            ppManagerEventHandler,
            &pManagerEventHandler
            );
        if (SUCCEEDED(hr))
        {
            pManagerEventHandler->m_pMainWindow = pMainWindow;
        }
        
        return hr;
    }

    // IUIAnimationManagerEventHandler

    IFACEMETHODIMP
    OnManagerStatusChanged
    (
        UI_ANIMATION_MANAGER_STATUS newStatus,
        UI_ANIMATION_MANAGER_STATUS previousStatus
    )
    {
        HRESULT hr = S_OK;

        if (newStatus == UI_ANIMATION_MANAGER_BUSY)
        {
            hr = m_pMainWindow->Invalidate();
        }

        return hr;
    }

    ...

};
```



<span data-ttu-id="28ea9-129">O código de exemplo a seguir é retirado de MainWindow. cpp da animação de exemplo de animação [orientada por aplicativo](application-driven-animation-sample.md)do Windows; consulte CMainWindow:: InitializeAnimation.</span><span class="sxs-lookup"><span data-stu-id="28ea9-129">The following example code is taken from MainWindow.cpp from the Windows Animation sample [Application-Driven Animation](application-driven-animation-sample.md); see CMainWindow::InitializeAnimation.</span></span> <span data-ttu-id="28ea9-130">Este exemplo cria uma instância do manipulador de eventos de Gerenciador usando o método [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) e o passa para o Gerenciador de animação usando o método [**IUIAnimationManager:: SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) .</span><span class="sxs-lookup"><span data-stu-id="28ea9-130">This example creates an instance of the manager event handler using the [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) method and passes it to the animation manager using the [**IUIAnimationManager::SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) method.</span></span>


```C++
// Create and set the ManagerEventHandler to start updating when animations are scheduled

IUIAnimationManagerEventHandler *pManagerEventHandler;
HRESULT hr = CManagerEventHandler::CreateInstance(
    this,
    &pManagerEventHandler
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->SetManagerEventHandler(
        pManagerEventHandler
        );
    pManagerEventHandler->Release();
}
```



<span data-ttu-id="28ea9-131">Como o manipulador de eventos de Gerenciador retém uma referência ao objeto de janela principal, o manipulador de eventos de Gerenciador deve ser limpo (passando **NULL** para [**SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)) ou o Gerenciador de animação deve ser completamente liberado antes que a janela principal seja destruída.</span><span class="sxs-lookup"><span data-stu-id="28ea9-131">Because the manager event handler retains a reference to the main window object, the manager event handler should be cleared (by passing **NULL** to [**SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)) or the animation manager should be completely released before the main window is destroyed.</span></span>

<span data-ttu-id="28ea9-132">O código de exemplo a seguir é extraído de MainWindow. cpp na animação de exemplo de animação [orientada por aplicativo](application-driven-animation-sample.md)do Windows; consulte o método CMainWindow:: OnPaint.</span><span class="sxs-lookup"><span data-stu-id="28ea9-132">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Application-Driven Animation](application-driven-animation-sample.md); see the CMainWindow::OnPaint method.</span></span> <span data-ttu-id="28ea9-133">Ele chama o método [**IUIAnimationManager:: getTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) para recuperar o tempo nas unidades exigidas pelo método [**IUIAnimationManager:: Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) .</span><span class="sxs-lookup"><span data-stu-id="28ea9-133">It calls the [**IUIAnimationManager::GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) method to retrieve the time in the units required by the [**IUIAnimationManager::Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) method.</span></span>


```C++
// Update the animation manager with the current time

UI_ANIMATION_SECONDS secondsNow;
HRESULT hr = m_pAnimationTimer->GetTime(
    &secondsNow
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->Update(
        secondsNow
        );

    ...

}
```



<span data-ttu-id="28ea9-134">O código de exemplo a seguir é extraído de MainWindow. cpp da [animação](application-driven-animation-sample.md) de exemplos de animação do Windows e [layout de grade](/windows/desktop/UIAnimation/grid-layout-sample); consulte o método CMainWindow:: OnPaint.</span><span class="sxs-lookup"><span data-stu-id="28ea9-134">The following example code is taken from MainWindow.cpp from the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::OnPaint method.</span></span> <span data-ttu-id="28ea9-135">Ele pressupõe que o aplicativo está usando uma API de gráficos que sincroniza automaticamente com a taxa de atualização do monitor (como Direct2D com suas configurações padrão). nesse caso, uma chamada para a função [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) é suficiente para garantir que o código de pintura será chamado novamente quando for o momento de desenhar o próximo quadro.</span><span class="sxs-lookup"><span data-stu-id="28ea9-135">It assumes that the application is using a graphics API that automatically synchronizes to the monitor refresh rate (such as Direct2D with its default settings), in which case a call to the [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function is enough to ensure that the painting code will be called again when it is time to draw the next frame.</span></span> <span data-ttu-id="28ea9-136">Em vez de chamar **InvalidateRect** incondicionalmente, é melhor verificar se ainda há animações agendadas usando [**GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus).</span><span class="sxs-lookup"><span data-stu-id="28ea9-136">Rather than call **InvalidateRect** unconditionally, it is better to check if there are still any animations scheduled using [**GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus).</span></span>


```C++
// Read the values of the animation variables and draw the client area

hr = DrawClientArea();
if (SUCCEEDED(hr))
{          
    // Continue redrawing the client area as long as there are animations scheduled
    UI_ANIMATION_MANAGER_STATUS status;
    hr = m_pAnimationManager->GetStatus(
        &status
        );
    if (SUCCEEDED(hr))
    {
        if (status == UI_ANIMATION_MANAGER_BUSY)
        {
            InvalidateRect(
                m_hwnd,
                NULL,
                FALSE
                );
        }
    }
}
```



### <a name="timer-driven-animation"></a><span data-ttu-id="28ea9-137">Timer-Driven animação</span><span class="sxs-lookup"><span data-stu-id="28ea9-137">Timer-Driven Animation</span></span>

<span data-ttu-id="28ea9-138">O código de exemplo a seguir é extraído de TimerEventHandler. h da animação de exemplo de animação [orientada por temporizador](timer-driven-animation-sample.md)do Windows.</span><span class="sxs-lookup"><span data-stu-id="28ea9-138">The following example code is taken from TimerEventHandler.h from the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="28ea9-139">O código de exemplo define o manipulador de eventos do temporizador, que invalida a área do cliente da janela para causar um redesenho após cada atualização do estado da animação.</span><span class="sxs-lookup"><span data-stu-id="28ea9-139">The example code defines the timer event handler, which invalidates the window's client area to cause a repaint after each update of the animation state.</span></span>


```C++
#include "UIAnimationHelper.h"

// Event handler object for timer events

class CTimerEventHandler :
    public CUIAnimationTimerEventHandlerBase<CTimerEventHandler>
{
public:

    static HRESULT
    CreateInstance
    (
        CMainWindow *pMainWindow,
        IUIAnimationTimerEventHandler **ppTimerEventHandler
    ) throw()
    {
        CTimerEventHandler *pTimerEventHandler;
        HRESULT hr = CUIAnimationCallbackBase::CreateInstance(
            ppTimerEventHandler,
            &pTimerEventHandler
            );

        if (SUCCEEDED(hr))
        {
            pTimerEventHandler->m_pMainWindow = pMainWindow;
        }
        
        return hr;
    }

    // IUIAnimationTimerEventHandler

    IFACEMETHODIMP
    OnPreUpdate()
    {
        return S_OK;
    }

    IFACEMETHODIMP
    OnPostUpdate()
    {
        HRESULT hr = m_pMainWindow->Invalidate();

        return hr;
    }

    IFACEMETHODIMP
    OnRenderingTooSlow
    (
        UINT32 /* fps */
    )
    {
        return S_OK;
    }

    ...

};
```



<span data-ttu-id="28ea9-140">O código de exemplo a seguir é extraído de MainWindow. cpp da animação de exemplo de animação [orientada por temporizador](timer-driven-animation-sample.md)do Windows; consulte CMainWindow:: InitializeAnimation.</span><span class="sxs-lookup"><span data-stu-id="28ea9-140">The following example code is taken from MainWindow.cpp from the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see CMainWindow::InitializeAnimation.</span></span> <span data-ttu-id="28ea9-141">Este exemplo cria uma instância do manipulador de eventos de timer usando o método [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) e o passa para o temporizador usando o método [**IUIAnimationTimer:: SetTimerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) .</span><span class="sxs-lookup"><span data-stu-id="28ea9-141">This example creates an instance of the timer event handler using the [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) method and passes it to the timer using the [**IUIAnimationTimer::SetTimerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) method.</span></span> <span data-ttu-id="28ea9-142">Como o manipulador de eventos de timer retém uma referência ao objeto de janela principal, o manipulador de eventos de timer deve ser limpo (passando **NULL** para **SetTimerEventHandler**) ou o timer foi completamente liberado antes que a janela principal seja destruída.</span><span class="sxs-lookup"><span data-stu-id="28ea9-142">Because the timer event handler retains a reference to the main window object, the timer event handler should be cleared (by passing **NULL** to **SetTimerEventHandler**) or the timer completely released before the main window is destroyed.</span></span>


```C++
// Create and set the timer event handler

IUIAnimationTimerEventHandler *pTimerEventHandler;
hr = CTimerEventHandler::CreateInstance(
    this,
    &pTimerEventHandler
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationTimer->SetTimerEventHandler(
        pTimerEventHandler
        );
    pTimerEventHandler->Release();
}
```



<span data-ttu-id="28ea9-143">O código de exemplo a seguir é extraído de MainWindow. cpp na animação de exemplo de animação [orientada por temporizador](timer-driven-animation-sample.md)do Windows; consulte o método CMainWindow:: InitializeAnimation.</span><span class="sxs-lookup"><span data-stu-id="28ea9-143">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::InitializeAnimation method.</span></span> <span data-ttu-id="28ea9-144">Ele chama o método [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no objeto do Gerenciador de animação para obter um ponteiro para [**IUIAnimationTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler), em seguida, conecta os objetos [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) e [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) definindo o Gerenciador de animação como o manipulador de atualização do temporizador usando o método [**IUIAnimationTimer:: SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler) .</span><span class="sxs-lookup"><span data-stu-id="28ea9-144">It calls the [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the animation manager object to get a pointer to [**IUIAnimationTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler), then connects the [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) and [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) objects by setting the animation manager as the timer's update handler using the [**IUIAnimationTimer::SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler) method.</span></span> <span data-ttu-id="28ea9-145">Observe que não é necessário limpar explicitamente essa conexão; a conexão é limpa com segurança depois que o aplicativo libera o Gerenciador de animação e o temporizador de animação.</span><span class="sxs-lookup"><span data-stu-id="28ea9-145">Note that it is not necessary to explicitly clear this connection; the connection is cleared safely after the application releases both the animation manager and the animation timer.</span></span>


```C++
// Connect the animation manager to the timer

IUIAnimationTimerUpdateHandler *pTimerUpdateHandler;
hr = m_pAnimationManager->QueryInterface(
    IID_PPV_ARGS(&pTimerUpdateHandler)
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationTimer->SetTimerUpdateHandler(
        pTimerUpdateHandler
        UI_ANIMATION_IDLE_BEHAVIOR_DISABLE  // timer will shut itself off when there are no animations playing
        );
    pTimerUpdateHandler->Release();
    if (SUCCEEDED(hr))
    {
        // Create and set the timer event handler

        ...

    }
}
```



<span data-ttu-id="28ea9-146">Se **a \_ \_ \_ \_ desabilitação do comportamento ocioso da animação da interface do usuário** não for usada, também será necessário habilitar o temporizador para iniciar a marcação.</span><span class="sxs-lookup"><span data-stu-id="28ea9-146">If **UI\_ANIMATION\_IDLE\_BEHAVIOR\_DISABLE** is not used, it is also necessary to enable the timer to start it ticking.</span></span>

## <a name="previous-step"></a><span data-ttu-id="28ea9-147">Etapa anterior</span><span class="sxs-lookup"><span data-stu-id="28ea9-147">Previous Step</span></span>

<span data-ttu-id="28ea9-148">Antes de iniciar esta etapa, você deve ter concluído esta etapa: [criar variáveis de animação](create-animation-variables.md).</span><span class="sxs-lookup"><span data-stu-id="28ea9-148">Before starting this step, you should have completed this step: [Create Animation Variables](create-animation-variables.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="28ea9-149">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="28ea9-149">Next Step</span></span>

<span data-ttu-id="28ea9-150">Depois de concluir esta etapa, a próxima etapa é: [ler os valores da variável de animação](updating---application-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="28ea9-150">After completing this step, the next step is: [Read the Animation Variable Values](updating---application-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="28ea9-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="28ea9-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28ea9-152">**IUIAnimationManager:: GetStatus**</span><span class="sxs-lookup"><span data-stu-id="28ea9-152">**IUIAnimationManager::GetStatus**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus)
</dt> <dt>

[<span data-ttu-id="28ea9-153">**IUIAnimationManager::SetManagerEventHandler**</span><span class="sxs-lookup"><span data-stu-id="28ea9-153">**IUIAnimationManager::SetManagerEventHandler**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)
</dt> <dt>

[<span data-ttu-id="28ea9-154">**IUIAnimationManager:: atualizar**</span><span class="sxs-lookup"><span data-stu-id="28ea9-154">**IUIAnimationManager::Update**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update)
</dt> <dt>

[<span data-ttu-id="28ea9-155">**IUIAnimationTimer:: getTime**</span><span class="sxs-lookup"><span data-stu-id="28ea9-155">**IUIAnimationTimer::GetTime**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[<span data-ttu-id="28ea9-156">**IUIAnimationTimer::SetTimerUpdateHandler**</span><span class="sxs-lookup"><span data-stu-id="28ea9-156">**IUIAnimationTimer::SetTimerUpdateHandler**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler)
</dt> <dt>

<span data-ttu-id="28ea9-157">[**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="28ea9-157">[**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="28ea9-158">[**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="28ea9-158">[**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="28ea9-159">Visão geral da animação do Windows</span><span class="sxs-lookup"><span data-stu-id="28ea9-159">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 