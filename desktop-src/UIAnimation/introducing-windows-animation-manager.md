---
title: Atualizar o Gerenciador de Animação e desenhar quadros
description: Sempre que um aplicativo agenda um storyboard, o aplicativo deve fornecer a hora atual para o gerenciador de animação.
ms.assetid: c4f746c3-e47c-4b82-a41b-e2c0d177d097
keywords:
- objetos do gerenciador de animação Windows Animação , atualizando
- objetos de temporizador de animação Windows Animação , conectando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd6c2c971783e13e00a45fe045be2624234f4165dc9fba1e50b11f88c69b68c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118847357"
---
# <a name="update-the-animation-manager-and-draw-frames"></a>Atualizar o Gerenciador de Animação e desenhar quadros

Sempre que um aplicativo agenda um storyboard, o aplicativo deve fornecer a hora atual para o gerenciador de animação. A hora atual também é necessária ao direcionar o gerenciador de animação para atualizar seu estado e definir todas as variáveis de animação para os valores interpolados apropriados.

## <a name="overview"></a>Visão geral

Há duas configurações com suporte da animação Windows: animação controlada por aplicativo e animação controlada por temporizador.

Para usar a animação controlada por aplicativo em seu aplicativo, você deve atualizar o gerenciador de animação antes de desenhar cada quadro e usar um mecanismo apropriado para desenhar quadros com frequência suficiente para animação. Um aplicativo que usa animação controlada por aplicativo pode usar qualquer mecanismo para determinar a hora atual, mas o objeto de temporizador animação Windows retorna um tempo preciso nas unidades aceitas pelo gerenciador de animação. Para evitar desenho desnecessário quando nenhuma animação estiver sendo realizada, você também deve fornecer um manipulador de eventos de gerente para começar a redesenhar quando as animações são agendadas e verificar após cada quadro se o redesenho pode ser suspenso. Para obter mais informações, consulte [Animação controlada por aplicativo.](scenic-animation-api-overview.md)

Na configuração controlada por aplicativo, um aplicativo pode chamar o método [**IUIAnimationManager::GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) para verificar se as animações estão agendadas no momento e continuar a desenhar quadros se elas estão. Como o redesenhar para quando não há animações agendadas, é necessário reiniciá-la na próxima vez que uma animação for agendada. Um aplicativo pode registrar um manipulador de eventos do gerenciador para ser notificado quando o status do gerenciador de animação mudar de ocioso (nenhuma animação está agendada no momento) para ocupado.

Para usar a animação controlada por temporizador em seu aplicativo, você deve conectar o gerenciador de animação a um temporizador de animação e fornecer um manipulador de eventos de temporizador. Quando o gerenciador de animação está conectado a um temporizador, o temporizador pode dizer ao gerente quando o estado de animação deve ser atualizado conforme o tempo avança. O aplicativo deve desenhar um quadro para cada tique do temporizador. O gerenciador de animação pode, por sua vez, dizer ao temporizador quando há animações em reprodução, para que o temporizador possa desligar a si mesmo durante períodos ociosos quando redesenhar for desnecessário. Para evitar o desenho desnecessário quando nenhuma animação estiver em reprodução, você deve configurar o temporizador para desabilitar a si mesmo automaticamente. Para obter mais informações, consulte [Animação controlada por temporizador.](scenic-animation-api-overview.md)

## <a name="example-code"></a>Código de exemplo

-   [Animação controlada por aplicativo](#application-driven-animation)
-   [Animação controlada por temporizador](#timer-driven-animation)

### <a name="application-driven-animation"></a>Application-Driven animação

O código de exemplo a seguir é retirado de ManagerEventHandler.h dos [exemplos](application-driven-animation-sample.md) de Animação do Windows animação controlada por aplicativo e [layout de grade.](/windows/desktop/UIAnimation/grid-layout-sample) Ele define o manipulador de eventos do gerenciador.


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



O código de exemplo a seguir é retirado de MainWindow.cpp do exemplo de animação Windows animação controlada por [aplicativo](application-driven-animation-sample.md); consulte CMainWindow::InitializeAnimation. Este exemplo cria uma instância do manipulador de eventos do gerenciador usando o método [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) e a passa para o gerenciador de animação usando o método [**IUIAnimationManager::SetManagerEventHandler.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)


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



Como o manipulador de eventos do gerenciador mantém uma referência ao objeto de janela principal, o manipulador de eventos do gerenciador deve ser limpo (passando **NULL** para [**SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)) ou o gerenciador de animação deve ser completamente liberado antes que a janela principal seja destruída.

O código de exemplo a seguir é retirado de MainWindow.cpp no exemplo de animação Windows animação controlada [por aplicativo](application-driven-animation-sample.md); consulte o método CMainWindow::OnPaint. Ele chama o [**método IUIAnimationManager::GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) para recuperar o tempo nas unidades exigidas pelo [**método IUIAnimationManager::Update.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update)


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



O código de exemplo a seguir é retirado de MainWindow.cpp dos [exemplos](application-driven-animation-sample.md) de animação Windows animação controlada por aplicativo e [layout de grade](/windows/desktop/UIAnimation/grid-layout-sample); consulte o método CMainWindow::OnPaint. Ele pressuporá que o aplicativo está usando uma API de elementos gráficos que sincroniza automaticamente com a taxa de atualização do monitor (como Direct2D com suas configurações padrão), caso em que uma chamada para a função [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) é suficiente para garantir que o código de pintura seja chamado novamente quando for hora de desenhar o próximo quadro. Em vez de **chamar InvalidateRect** incondicionalmente, é melhor verificar se ainda há animações agendadas usando [**GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus).


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

O código de exemplo a seguir é retirado de TimerEventHandler.h do exemplo de animação Windows animação orientada por [temporizador.](timer-driven-animation-sample.md) O código de exemplo define o manipulador de eventos do temporizador, que invalida a área de cliente da janela para causar uma nova reintação após cada atualização do estado de animação.


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



O código de exemplo a seguir é retirado de MainWindow.cpp do exemplo de animação Windows animação orientada por [temporizador](timer-driven-animation-sample.md); consulte CMainWindow::InitializeAnimation. Este exemplo cria uma instância do manipulador de eventos de temporizador usando o método [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) e a passa para o temporizador usando o método [**IUIAnimationTimer::SetTimerEventHandler.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) Como o manipulador de eventos do temporizador mantém uma referência ao objeto de janela principal, o manipulador de eventos do temporizador deve ser limpo (passando **NULL** para **SetTimerEventHandler**) ou o temporizador completamente liberado antes que a janela principal seja destruída.


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



O código de exemplo a seguir é retirado de MainWindow.cpp no exemplo de animação Windows animação orientada por [temporizador](timer-driven-animation-sample.md); consulte o método CMainWindow::InitializeAnimation. Ele chama o método [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no objeto do gerenciador de animação para obter um ponteiro para [**IUIAnimationTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler)e, em seguida, conecta os objetos [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) e [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) definindo o gerenciador de animação como o manipulador de atualização do temporizador usando o método [**IUIAnimationTimer::SetTimerUpdateHandler.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler) Observe que não é necessário limpar explicitamente essa conexão; a conexão é limpa com segurança depois que o aplicativo libera o gerenciador de animação e o temporizador de animação.


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



Se **a FUNÇÃO \_ DESABILITAR COMPORTAMENTO \_ OCIOSO \_ \_** DA ANIMAÇÃO da Interface do Usuário não for usada, também será necessário habilitar o temporizador para inciá-lo.

## <a name="previous-step"></a>Etapa anterior

Antes de iniciar esta etapa, você deve ter concluído esta etapa: Criar [Variáveis de Animação](create-animation-variables.md).

## <a name="next-step"></a>Próxima etapa

Depois de concluir esta etapa, a próxima etapa é: Ler [os Valores da Variável de Animação](updating---application-driven-animation.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IUIAnimationManager::GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus)
</dt> <dt>

[**IUIAnimationManager::SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)
</dt> <dt>

[**IUIAnimationManager::Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update)
</dt> <dt>

[**IUIAnimationTimer::GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[**IUIAnimationTimer::SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler)
</dt> <dt>

[**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))
</dt> <dt>

[**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))
</dt> <dt>

[Windows Visão geral da animação](scenic-animation-api-overview.md)
</dt> </dl>

 

 