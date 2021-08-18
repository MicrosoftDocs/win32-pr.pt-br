---
title: Adicionando suporte à manipulação em código não manipulado
description: Esta seção explica como adicionar suporte de manipulação ao código não gerenciamento implementando um sink de evento para a \_ interface IManipulationEvents.
ms.assetid: 7d8c6230-eaca-43c7-ad2f-651851b69d7f
keywords:
- Windows Toque, manipulações
- Windows Touch,_IManipulationEvents interface
- Windows Touch, interface IManipulationProcessor
- manipulações, adicionando suporte em código não manipulado
- manipulações, suporte a código não manipulado
- manipulações, suporte em código não manipulado
- manipulações, _IManipulationEvents interface
- manipulations,interface IManipulationProcessor
- _IManipulationEvents interface, suporte à manipulação em código não gerenciamento
- Interface IManipulationProcessor, suporte à manipulação em código não gerenciamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ff526c128b6da83fae3a74b88cd3bb21bc3a81c507c0a76a7c70dbddc5f76d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709996"
---
# <a name="adding-manipulation-support-in-unmanaged-code"></a>Adicionando suporte à manipulação em código não manipulado

Esta seção explica como adicionar suporte de manipulação ao código não gerenciamento implementando um sink de evento para a interface [**\_ IManipulationEvents.**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents)

A imagem a seguir descreve a arquitetura de manipulação.

![ilustração que mostra as mensagens de toque do Windows que são passadas para o processador de manipulação de um objeto , que manipula eventos com a \- interface imanipulationevents](images/manipulation-arch.png)

Os dados de toque recebidos das [**mensagens WM \_ TOUCH**](wm-touchdown.md) são passados para [**o IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) junto com a ID de contato da mensagem de toque. Com base na sequência de mensagens, a interface **IManipulationProcessor** calculará que tipo de transformação está sendo executada e quais são os valores associados a essa transformação. O **IManipulationProcessor** gerará [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) que são manipulados por um sink de evento. O sink de evento pode usar esses valores para executar operações personalizadas no objeto que está sendo transformado.

Para adicionar suporte de manipulação ao seu aplicativo, você deve seguir estas etapas:

1.  Implemente um sink de evento para a interface [**\_ IManipulationEvents.**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents)
2.  Crie uma instância de uma [**interface IManipulationProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
3.  Crie uma instância do seu sink de eventos e configurar eventos de toque.
4.  Envie dados de evento de toque para o processador de manipulação.

Esta seção explica as etapas que você deve seguir para adicionar suporte de manipulação ao seu aplicativo. O código é fornecido em cada etapa para começar.

> [!Note]  
> Você não pode usar manipulações e gestos ao mesmo tempo porque mensagens de gesto e toque são mutuamente exclusivas.

### <a name="implement-an-event-sink-for-_imanipualtionevents-interface"></a>Implementar um sink de eventos \_ para interface IManipualtionEvents

Antes de criar uma instância do seu sink de eventos, você deve criar uma classe que implemente a interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) para eventos. Esse é o seu sink de eventos. Os eventos gerados pela interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) são manipulados pelo seu sink de evento. O código a seguir mostra um header de exemplo para uma classe que herda a interface **\_ IManipulationEvents.**

```C++
// Manipulation Header Files
#include <comdef.h>
#include <manipulations.h>
#include <ocidl.h>

class CManipulationEventSink : _IManipulationEvents
{
public:
    CManipulationEventSink(IManipulationProcessor *manip, HWND hWnd);

    int GetStartedEventCount();
    int GetDeltaEventCount();
    int GetCompletedEventCount();
    double CManipulationEventSink::GetX();
    double CManipulationEventSink::GetY();        

    ~CManipulationEventSink();

    //////////////////////////////
    // IManipulationEvents methods
    //////////////////////////////
    virtual HRESULT STDMETHODCALLTYPE ManipulationStarted( 
        /* [in] */ FLOAT x,
        /* [in] */ FLOAT y);
    
    virtual HRESULT STDMETHODCALLTYPE ManipulationDelta( 
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
        /* [in] */ FLOAT cumulativeRotation);
    
    virtual HRESULT STDMETHODCALLTYPE ManipulationCompleted( 
        /* [in] */ FLOAT x,
        /* [in] */ FLOAT y,
        /* [in] */ FLOAT cumulativeTranslationX,
        /* [in] */ FLOAT cumulativeTranslationY,
        /* [in] */ FLOAT cumulativeScale,
        /* [in] */ FLOAT cumulativeExpansion,
        /* [in] */ FLOAT cumulativeRotation);

    ////////////////////////////////////////////////////////////
    // IUnknown methods
    ////////////////////////////////////////////////////////////
    STDMETHOD_(ULONG, AddRef)(void);
    STDMETHOD_(ULONG, Release)(void);
    STDMETHOD(QueryInterface)(REFIID riid, LPVOID *ppvObj);

private:
    double m_fX;
    double m_fY;

    int m_cRefCount;
    int m_cStartedEventCount;
    int m_cDeltaEventCount;
    int m_cCompletedEventCount;

    IManipulationProcessor* m_pManip;

    IConnectionPointContainer* m_pConPointContainer;
    IConnectionPoint* m_pConnPoint;
    
    HWND m_hWnd;
};     
```

Considerando o header, você deve criar uma implementação da interface de eventos para que sua classe execute as ações que você deseja que o processador de manipulação execute. O código a seguir é um modelo que implementa a funcionalidade mínima de um sink de evento para a interface [**\_ IManipulationEvents.**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents)

```C++
#include "stdafx.h"
#include "cmanipulationeventsink.h"

CManipulationEventSink::CManipulationEventSink(IManipulationProcessor *manip, HWND hWnd)
{
    m_hWnd = hWnd;

    //Set initial ref count to 1.
    m_cRefCount = 1;

    m_pManip = manip;
    m_pManip->put_PivotRadius(-1);

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = manip->QueryInterface(
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

int CManipulationEventSink::GetStartedEventCount()
{
    return m_cStartedEventCount;
}

int CManipulationEventSink::GetDeltaEventCount()
{
    return m_cDeltaEventCount;
}

int CManipulationEventSink::GetCompletedEventCount()
{
    return m_cCompletedEventCount;
}

double CManipulationEventSink::GetX()
{
    return m_fX;
}

double CManipulationEventSink::GetY()
{
    return m_fY;
}

CManipulationEventSink::~CManipulationEventSink()
{
    //Cleanup.
}

///////////////////////////////////
//Implement IManipulationEvents
///////////////////////////////////

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;
    
    return S_OK;
}

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
    MoveWindow(m_hWnd,                                                     // the window to move
               static_cast<int>(rect.left + (translationDeltaX / 100.0f)), // the x position
               static_cast<int>(rect.top + (translationDeltaY/100.0f)),    // the y position
               static_cast<int>(oldWidth * scaleDelta),                    // width
               static_cast<int>(oldHeight * scaleDelta),                   // height
               TRUE);                                                      // redraw
                     
    return S_OK;
}

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

    return S_OK;
}


/////////////////////////////////
//Implement IUnknown
/////////////////////////////////

ULONG CManipulationEventSink::AddRef(void) 
{
    return ++m_cRefCount;
}

ULONG CManipulationEventSink::Release(void)
{ 
    m_cRefCount --;

    if(0 == m_cRefCount) {
        delete this;
        return 0;
    }

    return m_cRefCount;
}

HRESULT CManipulationEventSink::QueryInterface(REFIID riid, LPVOID *ppvObj) 
{
    if (IID__IManipulationEvents == riid) {
        *ppvObj = (_IManipulationEvents *)(this); AddRef(); return S_OK;
    } else if (IID_IUnknown == riid) {
        *ppvObj = (IUnknown *)(this); AddRef(); return S_OK;
    } else {
        return E_NOINTERFACE;
    }
}         
```

Preste atenção extra às implementações dos métodos [**ManipulationStarted,**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted) [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)e [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) na classe . Esses são os métodos mais prováveis na interface que exigirão que você execute operações com base nas informações de manipulação passadas no evento. Observe também que o segundo parâmetro no construtor é o objeto usado nas manipulações de eventos. No código usado para produzir o exemplo, o hWnd para o aplicativo é enviado ao construtor para que ele possa ser reposicionado e reposicionado.

### <a name="create-an-instance-of-an-imanipulationprocessor-interface"></a>Criar uma instância de uma interface IManipulationProcessor

No código em que você usará manipulações, você deve criar uma instância de uma interface [**IManipulationProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) Primeiro, você deve adicionar suporte para a classe de manipulações. O código a seguir mostra como você pode fazer isso em sua classe.

```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;     
```

Depois de ter sua variável para o processador de manipulação e incluir os headers para manipulações, você precisa criar uma instância da interface [**IManipulationProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) Esse é um objeto COM. Portanto, você deve chamar [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)e, em seguida, criar uma instância de sua referência para **o IManipulationProcessor**. O código a seguir mostra como você pode criar uma instância dessa interface.

```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
```

### <a name="create-an-instance-of-your-event-sink-and-set-up-touch-events"></a>Criar uma instância do seu Sink de Eventos e configurar Eventos de Toque

Inclua a definição da classe do seu sink de evento ao seu código e adicione uma variável para a classe de sink de evento de manipulação. O exemplo de código a seguir inclui o header para a implementação de classe e configura uma variável global para armazenar o sink de eventos.

```C++
//Include your definition of the event sink, CManipulationEventSink.h in this case
#include "CManipulationEventSink.h"    
     
// Set up a variable to point to the manipulation event sink implementation class    
CManipulationEventSink* g_pManipulationEventSink;   
```

Depois de ter a variável e incluir sua definição para a nova classe de sink de evento, você pode construir a classe usando o processador de manipulação que você definiu na etapa anterior. O código a seguir mostra como uma instância dessa classe seria criada de **OnInitDialog.**

```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```

> [!Note]  
> A maneira como você cria uma instância do seu sink de evento depende do que você está fazendo com os dados de manipulação. Na maioria dos casos, você criará um sink de eventos do processador de manipulação que não tem o mesmo construtor que este exemplo.

### <a name="send-touch-event-data-to-the-manipulation-processor"></a>Enviar dados de evento de toque para o processador de manipulação

Agora que você tem o processador de manipulação e o sink de eventos definidos, você deve alimentar dados de toque para o processador de manipulação para disparar eventos de manipulação.

> [!Note]  
> Esse é o mesmo procedimento discutido no Ponto de Partida [com Windows Touch Messages](getting-started-with-multi-touch-messages.md).

Primeiro, você criará um código para decodificar as mensagens [**WM \_ TOUCH**](wm-touchdown.md) e enviá-las para a interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) para gerar eventos. O código a seguir mostra uma implementação de exemplo que é chamada do **método WndProc** e retorna um **LRESULT** para mensagens.

```C++
LRESULT OnTouch(HWND hWnd, WPARAM wParam, LPARAM lParam )
{
  UINT cInputs = LOWORD(wParam);
  PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
  
  BOOL bHandled = FALSE;
  
  if (NULL != pInputs) {
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
      cInputs,
      pInputs,
      sizeof(TOUCHINPUT))) {      
      for (UINT i=0; i<cInputs; i++){
        if (pInputs[i].dwFlags & TOUCHEVENTF_DOWN){
            g_pIManipProc->ProcessDown(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
        if (pInputs[i].dwFlags & TOUCHEVENTF_UP){
            g_pIManipProc->ProcessUp(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
        if (pInputs[i].dwFlags & TOUCHEVENTF_MOVE){
            g_pIManipProc->ProcessMove(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
      }      
    } else {
      // GetLastError() and error handling
    }
    delete [] pInputs;
  } else {
    // error handling, presumably out of memory
  }
  if (bHandled){
    // if you don't want to pass to DefWindowProc, close the touch input handle
    if (!CloseTouchInputHandle((HTOUCHINPUT)lParam)) {
        // error handling
    }
    return 0;
  }else{
    return DefWindowProc(hWnd, WM_TOUCH, wParam, lParam);
  }
}
```

Agora que você tem um método utilitário para decodificar a mensagem [**WM \_ TOUCH,**](wm-touchdown.md) você deve passar as mensagens **WM \_ TOUCH** para a função de utilitário do **método WndProc.** O código a seguir mostra como você pode fazer isso.

```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
    case WM_COMMAND:
        wmId    = LOWORD(wParam);
        wmEvent = HIWORD(wParam);
        // Parse the menu selections:
        switch (wmId)
        {
        case IDM_ABOUT:
            DialogBox(hInst, MAKEINTRESOURCE(IDD_ABOUTBOX), hWnd, About);
            break;
        case IDM_EXIT:
            DestroyWindow(hWnd);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
        }
        break;
    case WM_TOUCH:
        return OnTouch(hWnd, wParam, lParam);
    case WM_PAINT:
        hdc = BeginPaint(hWnd, &ps);
        // TODO: Add any drawing code here...
        EndPaint(hWnd, &ps);
        break;
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```

Os métodos personalizados que você implementou no seu sink de eventos agora devem funcionar. Neste exemplo, tocar na janela a move.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Manipulações](getting-started-with-manipulations.md)
</dt> </dl>


 