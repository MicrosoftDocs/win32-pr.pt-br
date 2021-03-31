---
title: Manipulando inércia em código não gerenciado
description: Esta seção explica como usar a interface IInertiaProcessor para manipular o inércia no código não gerenciado.
ms.assetid: 3261b461-add2-4e92-9a51-b2d46630fb4f
keywords:
- Windows Touch, inércia
- Windows Touch, processador de manipulação
- inércia, código não gerenciado
- inércia, interface IInertiaProcessor
- inércia, processador de manipulação
- processador de manipulação, inércia
- Interface IInertiaProcessor, código não gerenciado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3de56d06547f426de252a89ef5172df3fe4ca439
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005001"
---
# <a name="handling-inertia-in-unmanaged-code"></a>Manipulando inércia em código não gerenciado

Esta seção explica como usar a interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) para manipular o inércia no código não gerenciado.

## <a name="overview"></a>Visão geral

Para usar o inércia em código não gerenciado, você deve implementar coletores de eventos para o processador de manipulação e o processador inércia. Comece adicionando o suporte à manipulação ao seu aplicativo, conforme descrito na seção [adicionando suporte à manipulação ao código não gerenciado](adding-manipulation-support-in-unmanaged-code.md). Observe que o suporte à manipulação exige que você use mensagens de toque em vez de mensagens de gesto para alimentar os dados de evento ao processador de manipulação. Depois que a manipulação estiver funcionando, você também deverá implementar um segundo coletor de eventos para os eventos que a interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) irá gerar ou precisará modificar o coletor de eventos existente para acomodar os eventos gerados pelas interfaces **IInertiaProcessor** e [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) . Para os fins deste exemplo, é mais fácil iniciar a partir do coletor de eventos criado para a seção adicionar suporte de manipulação a código não gerenciado e adicionar um segundo construtor que funciona com o processador inércia em vez do processador de manipulação. Dessa forma, a implementação do coletor de eventos pode funcionar para o processador de manipulação ou para o processador inércia. Além de adicionar um segundo construtor, o coletor de eventos terá uma variável indicando se ele executará as operações com base na entrada inércia em vez da entrada de manipulação.

### <a name="add-inertia-support-to-a-manipulation-processor-event-sink"></a>Adicionar suporte a inércia a um coletor de eventos do processador de manipulação

O código a seguir mostra o novo Construtor de coletor de eventos, novas variáveis de membro para uma interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) e um sinalizador que indica se o coletor está extrapolando para inércia.


```C++
    CManipulationEventSink(IManipulationProcessor *pManip, IInertiaProcessor *pInert, HWND hWnd);
    CManipulationEventSink(IInertiaProcessor *pInert, HWND hWnd);
```




```C++
    IInertiaProcessor*      m_pInert;
    BOOL fExtrapolating; 
```



Depois que o cabeçalho de sua classe tiver os novos construtores e um sinalizador indicando se você está extrapolando, você pode implementar seu coletor de eventos para ter blocos de manipulação separados para os eventos [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) e eventos [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) . O construtor que aceita um **IManipulationProcessor** e um **IInertiaProcessor** deve definir o sinalizador **fExtrapolating** como false, o que indica que esse é um manipulador de eventos **IManipulationProcessor** . O código a seguir mostra como o construtor de um coletor de eventos que usa o **IManipulationProcessor** pode ser implementado.


```C++
CManipulationEventSink::CManipulationEventSink(IManipulationProcessor *pManip, IInertiaProcessor *pInert, HWND hWnd)
{
    m_hWnd = hWnd;

    //Set initial ref count to 1.
    m_cRefCount = 1;

    fExtrapolating=FALSE;

    m_pManip = pManip;
    
    m_pInert = pInert;
    
    m_pManip->put_PivotRadius(-1);

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = pManip->QueryInterface(
      IID_IConnectionPointContainer, 
          (LPVOID*) &spConnectionContainer
        );
    //hr = manip->QueryInterface(&spConnectionContainer);
    if (spConnectionContainer == NULL){
        // something went wrong, try to gracefully quit
        
    }

    //Get a connection point.
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(_IManipulationEvents), &m_pConnPoint);
    if (m_pConnPoint == NULL){
        // something went wrong, try to gracefully quit
    }

    DWORD dwCookie;

    //Advise.
    hr = m_pConnPoint->Advise(this, &dwCookie);
}
```



O código a seguir mostra como o construtor de um coletor de eventos que usa o [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) pode ser implementado. Esse construtor define o sinalizador **fExtrapolating** como true, indicando que essa instância da classe de coletor de eventos executará a extrapolação e executará quaisquer operações de movimentação que foram executadas anteriormente pelos eventos do processador de manipulação.


```C++
CManipulationEventSink::CManipulationEventSink(IInertiaProcessor *pInert, HWND hWnd)
{
    m_hWnd = hWnd;

    m_pInert = pInert;
    //Set initial ref count to 1.
    m_cRefCount = 1;

    fExtrapolating=TRUE;

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = pInert->QueryInterface(
      IID_IConnectionPointContainer, 
          (LPVOID*) &spConnectionContainer
        );
    //hr = manip->QueryInterface(&spConnectionContainer);
    if (spConnectionContainer == NULL){
        // something went wrong, try to gracefully quit        
    }

    //Get a connection point.
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(_IManipulationEvents), &m_pConnPoint);
    if (m_pConnPoint == NULL){
        // something went wrong, try to gracefully quit
    }
    DWORD dwCookie;

    //Advise.
    hr = m_pConnPoint->Advise(this, &dwCookie);
}   
```



> [!Note]  
> A implementação da classe do coletor de eventos do coletor de eventos do processador de manipulação é reutilizada como um coletor de eventos para o processador inércia.

 

Agora, quando você constrói essa classe, **CManipulationEventSink**, ela pode ser construída como um coletor de eventos para um processador de manipulação ou como um coletor de eventos para um processador inércia. Quando ele é construído como um coletor de eventos do processador inércia, ele terá o sinalizador **fExtrapolating** definido como true, indicando que os eventos Manipulation devem ser extrapolados.

> [!Note]  
> [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted) será gerado pelas interfaces [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) e [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .

 

Quando a manipulação é iniciada, as propriedades da interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) são definidas. O código a seguir mostra como o evento iniciado é manipulado.


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;       

    // set origins in manipulation processor
    m_pInert->put_InitialOriginX(x);
    m_pInert->put_InitialOriginY(y);
    
    RECT screenRect;

    HWND desktop = GetDesktopWindow();
    GetClientRect(desktop, &screenRect);

    // physics settings
    // deceleration is units per square millisecond
    m_pInert->put_DesiredDeceleration(.1f);

    // set the boundaries        
    screenRect.left-= 1024;
    m_pInert->put_BoundaryLeft  ( static_cast<float>(screenRect.left   * 100));
    m_pInert->put_BoundaryTop   ( static_cast<float>(screenRect.top    * 100));
    m_pInert->put_BoundaryRight ( static_cast<float>(screenRect.right  * 100));
    m_pInert->put_BoundaryBottom( static_cast<float>(screenRect.bottom * 100));
    
    
    // Elastic boundaries - I set these to 90% of the screen 
    // so... 5% at left, 95% right, 5% top,  95% bottom
    // Values are whole numbers because units are in centipixels
    m_pInert->put_ElasticMarginLeft  (static_cast<float>(screenRect.left   * 5));
    m_pInert->put_ElasticMarginTop   (static_cast<float>(screenRect.top    * 5));
    m_pInert->put_ElasticMarginRight (static_cast<float>(screenRect.right  * 95));
    m_pInert->put_ElasticMarginBottom(static_cast<float>(screenRect.bottom * 95));
    
    
    return S_OK;
}
```



Neste exemplo, os deltas de manipulação são usados para mover a janela. O código a seguir mostra como o evento Delta é manipulado.


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y,
    /* [in] */ FLOAT translationDeltaX,
    /* [in] */ FLOAT translationDeltaY,
    /* [in] */ FLOAT scaleDelta,
    /* [in] */ FLOAT expansionDelta,
    /* [in] */ FLOAT rotationDelta,
    /* [in] */ FLOAT cumulativeTranslationX,
    /* [in] */ FLOAT cumulativeTranslationY,
    /* [in] */ FLOAT cumulativeScale,
    /* [in] */ FLOAT cumulativeExpansion,
    /* [in] */ FLOAT cumulativeRotation)
{
    m_cDeltaEventCount ++;
        
    RECT rect;
            
    GetWindowRect(m_hWnd, &rect);
        
    int oldWidth =  rect.right-rect.left;
    int oldHeight = rect.bottom-rect.top;            

    // scale and translate the window size / position    
    MoveWindow(m_hWnd,                                              // the window to move
        static_cast<int>(rect.left + (translationDeltaX / 100.0f)), // the x position
        static_cast<int>(rect.top + (translationDeltaY/100.0f)),    // the y position
        static_cast<int>(oldWidth * scaleDelta),                    // width
        static_cast<int>(oldHeight * scaleDelta),                   // height
        TRUE);                                                      // redraw
                     
    return S_OK;
}
```



Neste exemplo, a manipulação de eventos concluídos inicia ou interrompe um temporizador que chamará o [**processo**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) na interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) . O código a seguir mostra como o evento de manipulação concluído é manipulado.


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationCompleted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y,
    /* [in] */ FLOAT cumulativeTranslationX,
    /* [in] */ FLOAT cumulativeTranslationY,
    /* [in] */ FLOAT cumulativeScale,
    /* [in] */ FLOAT cumulativeExpansion,
    /* [in] */ FLOAT cumulativeRotation)
{
    m_cCompletedEventCount ++;

    m_fX = x;
    m_fY = y;

    // place your code handler here to do any operations based on the manipulation   
    
    if (fExtrapolating){
        //Inertia Complete, stop the timer used for processing      
        KillTimer(m_hWnd,0);        
    }else{ 
        // setup velocities for inertia processor
        float vX = 0.0f;
        float vY = 0.0f;
        float vA = 0.0f;
        m_pManip->GetVelocityX(&vX);
        m_pManip->GetVelocityY(&vY);
        m_pManip->GetAngularVelocity(&vA);

        // complete any previous processing
        m_pInert->Complete();
        
        // Reset sets the  initial timestamp
        m_pInert->Reset();
                
        // 
        m_pInert->put_InitialVelocityX(vX);
        m_pInert->put_InitialVelocityY(vY);        
        
        m_pInert->put_InitialOriginX(x);
        m_pInert->put_InitialOriginY(y);
        
           
        // Start a timer
        SetTimer(m_hWnd,0, 50, 0);        
    }

    return S_OK;
}
```



O código a seguir mostra como você pode interpretar mensagens de **\_ temporizador do WM** em **WndProc** para executar chamadas para [**processar**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) na interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .


```C++
case WM_TIMER:       
  if (g_pIInertProc){
    BOOL b;       
    g_pIInertProc->Process(&b);        
  }
  break;
```



### <a name="coinitialize-the-inertia-processor-and-manipulation-processor-and-initialize-the-event-sinks"></a>CoInitialize o processador inércia e o processador de manipulação e inicializar os coletores de eventos

Depois que o coletor de eventos for modificado para dar suporte ao [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) e ao [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor), você estará pronto para inicializar os coletores de eventos e configurá-los para execução a partir do seu aplicativo. O código a seguir mostra como os ponteiros de interface são alocados.


```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;
IInertiaProcessor*      g_pIInertProc;
```



O exemplo de código a seguir mostra como criar uma instância de suas interfaces.


```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
   
   hr = CoCreateInstance(CLSID_InertiaProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIInertProc)
   );
```



O exemplo de código a seguir mostra como construir os coletores de eventos de acordo com os ponteiros de interface e registrar a janela para entrada por toque.


```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, g_pIInertProc, hWnd);
   g_pManipulationEventSink = new CManipulationEventSink(g_pIInertProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Inércia](getting-started-with-inertia.md)
</dt> </dl>

 

 




