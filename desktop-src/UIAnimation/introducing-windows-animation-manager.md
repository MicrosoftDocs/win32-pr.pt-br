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
# <a name="update-the-animation-manager-and-draw-frames"></a>Atualizar o Gerenciador de animação e desenhar quadros

Cada vez que um aplicativo agenda um storyboard, o aplicativo deve fornecer a hora atual ao Gerenciador de animação. A hora atual também é necessária ao direcionar o Gerenciador de animação para atualizar seu estado e definir todas as variáveis de animação para os valores interpolados apropriados.

## <a name="overview"></a>Visão geral

Há duas configurações com suporte na animação do Windows: animação orientada por aplicativo e animação orientada por temporizador.

Para usar a animação orientada por aplicativo em seu aplicativo, você deve atualizar o Gerenciador de animação antes de desenhar cada quadro e usar um mecanismo apropriado para desenhar quadros com frequência suficiente para animação. Um aplicativo que usa animação orientada por aplicativo pode usar qualquer mecanismo para determinar a hora atual, mas o objeto de temporizador de animação do Windows retorna um tempo preciso nas unidades aceitas pelo Gerenciador de animação. Para evitar um desenho desnecessário quando nenhuma animação estiver sendo executada, você também deverá fornecer um manipulador de eventos de gerente para iniciar o redesenho quando as animações forem agendadas e verificar depois de cada quadro se o redesenho pode ser suspenso. Para obter mais informações, consulte [animação orientada por aplicativo](scenic-animation-api-overview.md).

Na configuração controlada por aplicativo, um aplicativo pode chamar o método [**IUIAnimationManager:: GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) para verificar se as animações estão agendadas no momento e continuam a desenhar quadros se estiverem. Como o redesenho é interrompido quando não há animações agendadas, é necessário reiniciá-lo na próxima vez que uma animação for agendada. Um aplicativo pode registrar um manipulador de eventos de Gerenciador para ser notificado quando o status do Gerenciador de animação mudar de ocioso (nenhuma animação está agendada no momento) para ocupado.

Para usar a animação orientada por temporizador em seu aplicativo, você deve conectar o Gerenciador de animação a um temporizador de animação e fornecer um manipulador de eventos de temporizador. Quando o Gerenciador de animação está conectado a um temporizador, o temporizador pode informar ao gerente quando o estado da animação deve ser atualizado à medida que o tempo progride. O aplicativo deve desenhar um quadro para cada tique-timer. O Gerenciador de animação pode, por sua vez, dizer ao temporizador quando há animações sendo executadas, portanto, o temporizador pode desligar fora durante períodos ociosos quando o redesenho é desnecessário. Para evitar o desenho desnecessário quando nenhuma animação está sendo executada, você deve configurar o temporizador para se desabilitá-lo automaticamente. Para obter mais informações, consulte [animação orientada por temporizador](scenic-animation-api-overview.md).

## <a name="example-code"></a>Código de exemplo

-   [Animação orientada por aplicativo](#application-driven-animation)
-   [Animação orientada por temporizador](#timer-driven-animation)

### <a name="application-driven-animation"></a>Application-Driven animação

O código de exemplo a seguir é extraído de ManagerEventHandler. h da [animação](application-driven-animation-sample.md) de exemplos de animação do Windows e [layout de grade](/windows/desktop/UIAnimation/grid-layout-sample). Ele define o manipulador de eventos de Gerenciador.


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



O código de exemplo a seguir é retirado de MainWindow. cpp da animação de exemplo de animação [orientada por aplicativo](application-driven-animation-sample.md)do Windows; consulte CMainWindow:: InitializeAnimation. Este exemplo cria uma instância do manipulador de eventos de Gerenciador usando o método [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) e o passa para o Gerenciador de animação usando o método [**IUIAnimationManager:: SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) .


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



Como o manipulador de eventos de Gerenciador retém uma referência ao objeto de janela principal, o manipulador de eventos de Gerenciador deve ser limpo (passando **NULL** para [**SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)) ou o Gerenciador de animação deve ser completamente liberado antes que a janela principal seja destruída.

O código de exemplo a seguir é extraído de MainWindow. cpp na animação de exemplo de animação [orientada por aplicativo](application-driven-animation-sample.md)do Windows; consulte o método CMainWindow:: OnPaint. Ele chama o método [**IUIAnimationManager:: getTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) para recuperar o tempo nas unidades exigidas pelo método [**IUIAnimationManager:: Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) .


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



O código de exemplo a seguir é extraído de MainWindow. cpp da [animação](application-driven-animation-sample.md) de exemplos de animação do Windows e [layout de grade](/windows/desktop/UIAnimation/grid-layout-sample); consulte o método CMainWindow:: OnPaint. Ele pressupõe que o aplicativo está usando uma API de gráficos que sincroniza automaticamente com a taxa de atualização do monitor (como Direct2D com suas configurações padrão). nesse caso, uma chamada para a função [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) é suficiente para garantir que o código de pintura será chamado novamente quando for o momento de desenhar o próximo quadro. Em vez de chamar **InvalidateRect** incondicionalmente, é melhor verificar se ainda há animações agendadas usando [**GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus).


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



### <a name="timer-driven-animation"></a>Timer-Driven animação

O código de exemplo a seguir é extraído de TimerEventHandler. h da animação de exemplo de animação [orientada por temporizador](timer-driven-animation-sample.md)do Windows. O código de exemplo define o manipulador de eventos do temporizador, que invalida a área do cliente da janela para causar um redesenho após cada atualização do estado da animação.


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



O código de exemplo a seguir é extraído de MainWindow. cpp da animação de exemplo de animação [orientada por temporizador](timer-driven-animation-sample.md)do Windows; consulte CMainWindow:: InitializeAnimation. Este exemplo cria uma instância do manipulador de eventos de timer usando o método [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) e o passa para o temporizador usando o método [**IUIAnimationTimer:: SetTimerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) . Como o manipulador de eventos de timer retém uma referência ao objeto de janela principal, o manipulador de eventos de timer deve ser limpo (passando **NULL** para **SetTimerEventHandler**) ou o timer foi completamente liberado antes que a janela principal seja destruída.


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



O código de exemplo a seguir é extraído de MainWindow. cpp na animação de exemplo de animação [orientada por temporizador](timer-driven-animation-sample.md)do Windows; consulte o método CMainWindow:: InitializeAnimation. Ele chama o método [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no objeto do Gerenciador de animação para obter um ponteiro para [**IUIAnimationTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler), em seguida, conecta os objetos [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) e [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) definindo o Gerenciador de animação como o manipulador de atualização do temporizador usando o método [**IUIAnimationTimer:: SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler) . Observe que não é necessário limpar explicitamente essa conexão; a conexão é limpa com segurança depois que o aplicativo libera o Gerenciador de animação e o temporizador de animação.


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



Se **a \_ \_ \_ \_ desabilitação do comportamento ocioso da animação da interface do usuário** não for usada, também será necessário habilitar o temporizador para iniciar a marcação.

## <a name="previous-step"></a>Etapa anterior

Antes de iniciar esta etapa, você deve ter concluído esta etapa: [criar variáveis de animação](create-animation-variables.md).

## <a name="next-step"></a>Próxima etapa

Depois de concluir esta etapa, a próxima etapa é: [ler os valores da variável de animação](updating---application-driven-animation.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IUIAnimationManager:: GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus)
</dt> <dt>

[**IUIAnimationManager::SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)
</dt> <dt>

[**IUIAnimationManager:: atualizar**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update)
</dt> <dt>

[**IUIAnimationTimer:: getTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[**IUIAnimationTimer::SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler)
</dt> <dt>

[**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))
</dt> <dt>

[**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))
</dt> <dt>

[Visão geral da animação do Windows](scenic-animation-api-overview.md)
</dt> </dl>

 

 