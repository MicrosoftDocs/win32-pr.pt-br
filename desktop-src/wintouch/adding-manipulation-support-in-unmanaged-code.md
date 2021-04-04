---
title: Adicionando suporte à manipulação em código não gerenciado
description: Esta seção explica como adicionar suporte de manipulação a código não gerenciado implementando um coletor de eventos para a \_ interface IManipulationEvents.
ms.assetid: 7d8c6230-eaca-43c7-ad2f-651851b69d7f
keywords:
- Windows Touch, manipulações
- Windows Touch, interface _IManipulationEvents
- Windows Touch, interface IManipulationProcessor
- manipulações, adicionando suporte em código não gerenciado
- manipulações, suporte a código não gerenciado
- manipulações, suporte no código não gerenciado
- manipulações, _IManipulationEvents interface
- manipulações, interface IManipulationProcessor
- Interface _IManipulationEvents, suporte a manipulação em código não gerenciado
- Interface IManipulationProcessor, suporte à manipulação em código não gerenciado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a2e000b6d3518c4e90eb5ae03b581e81037edf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084758"
---
# <a name="adding-manipulation-support-in-unmanaged-code"></a>Adicionando suporte à manipulação em código não gerenciado

Esta seção explica como adicionar suporte de manipulação a código não gerenciado implementando um coletor de eventos para a interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .

A imagem a seguir descreve a arquitetura de manipulação.

![ilustração que mostra as mensagens de toque do Windows que são passadas para o processador de manipulação de um objeto, que manipula eventos com a \- interface imanipulationevents](images/manipulation-arch.png)

Os dados de toque recebidos do [**WM \_ Touch**](wm-touchdown.md) messages são passados para o [**IMANIPULATIONPROCESSOR**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) junto com a ID de contato da mensagem de toque. Com base na sequência de mensagens, a interface **IManipulationProcessor** calculará que tipo de transformação está sendo executada e quais os valores associados a essa transformação são. Em seguida, o **IManipulationProcessor** gerará [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) que são manipulados por um coletor de eventos. O coletor de eventos pode usar esses valores para executar operações personalizadas no objeto que está sendo transformado.

Para adicionar suporte à manipulação ao seu aplicativo, você deve seguir estas etapas:

1.  Implemente um coletor de eventos para a interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .
2.  Crie uma instância de uma interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .
3.  Crie uma instância do seu coletor de eventos e configure eventos de toque.
4.  Enviar dados de evento de toque para o processador de manipulação.

Esta seção explica as etapas que você deve seguir para adicionar suporte à manipulação ao seu aplicativo. O código é fornecido em cada etapa para você começar.

> [!Note]  
> Você não pode usar manipulações e gestos ao mesmo tempo porque as mensagens de gesto e toque são mutuamente exclusivas.

### <a name="implement-an-event-sink-for-_imanipualtionevents-interface"></a>Implementar um coletor de eventos para a \_ interface IManipualtionEvents

Antes de criar uma instância do coletor de eventos, você deve criar uma classe que implemente a interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) para eventos. Este é o coletor de eventos. Eventos gerados pela interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) são tratados pelo seu coletor de eventos. O código a seguir mostra um cabeçalho de exemplo para uma classe que herda a interface **\_ IManipulationEvents** .

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

Dado o cabeçalho, você deve criar uma implementação da interface de eventos para que sua classe execute as ações que você deseja que o processador de manipulação realize. O código a seguir é um modelo que implementa a funcionalidade mínima de um coletor de eventos para a interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .

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

Preste atenção extra às implementações dos métodos [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)e [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) na classe. Esses são os métodos mais prováveis na interface que exigirão que você execute operações com base nas informações de manipulação que são passadas no evento. Observe também que o segundo parâmetro no construtor é o objeto usado nas manipulações de evento. No código usado para produzir o exemplo, o hWnd do aplicativo é enviado ao construtor para que ele possa ser reposicionado e redimensionado.

### <a name="create-an-instance-of-an-imanipulationprocessor-interface"></a>Criar uma instância de uma interface IManipulationProcessor

No código em que você usará as manipulações, será necessário criar uma instância de uma interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) . Primeiro, você deve adicionar suporte para a classe Manipulations. O código a seguir mostra como você pode fazer isso em sua classe.

```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;     
```

Depois que você tiver a variável para o processador de manipulação e tiver incluído os cabeçalhos para as manipulações, você precisará criar uma instância da interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) . Este é um objeto COM. Portanto, você deve chamar [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)e, em seguida, criar uma instância de sua referência para o **IManipulationProcessor**. O código a seguir mostra como você pode criar uma instância dessa interface.

```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
```

### <a name="create-an-instance-of-your-event-sink-and-set-up-touch-events"></a>Criar uma instância do seu coletor de eventos e configurar eventos de toque

Inclua a definição de sua classe de coletor de eventos em seu código e, em seguida, adicione uma variável para a classe de coletor de eventos Manipulation. O exemplo de código a seguir inclui o cabeçalho para a implementação de classe e configura uma variável global para armazenar o coletor de eventos.

```C++
//Include your definition of the event sink, CManipulationEventSink.h in this case
#include "CManipulationEventSink.h"    
     
// Set up a variable to point to the manipulation event sink implementation class    
CManipulationEventSink* g_pManipulationEventSink;   
```

Depois de ter a variável e incluir sua definição para a nova classe de coletor de eventos, você pode construir a classe usando o processador de manipulação que você configurou na etapa anterior. O código a seguir mostra como uma instância dessa classe seria criada a partir de **OnInitDialog**.

```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```

> [!Note]  
> A maneira como você cria uma instância do seu coletor de eventos depende do que você está fazendo com os dados de manipulação. Na maioria dos casos, você criará um coletor de eventos do processador de manipulação que não tem o mesmo construtor que este exemplo.

### <a name="send-touch-event-data-to-the-manipulation-processor"></a>Enviar dados de evento de toque para o processador de manipulação

Agora que o processador de manipulação e o coletor de eventos foram configurados, você deve alimentar os dados de toque no processador de manipulação para disparar eventos de manipulação.

> [!Note]  
> Esse é o mesmo procedimento discutido em [introdução com mensagens de toque do Windows](getting-started-with-multi-touch-messages.md).

Primeiro, você criará um código para decodificar as mensagens do [**WM \_ Touch**](wm-touchdown.md) e enviá-las para a interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) para gerar eventos. O código a seguir mostra uma implementação de exemplo que é chamada do método **WndProc** e retorna um **LRESULT** para mensagens.

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

Agora que você tem um método utilitário para decodificar a mensagem do [**WM \_ Touch**](wm-touchdown.md) , você deve passar as mensagens do **WM \_ Touch** para a função utilitário do seu método **WndProc** . O código a seguir mostra como você pode fazer isso.

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

Os métodos personalizados que você implementou em seu coletor de eventos agora devem funcionar. Neste exemplo, tocar na janela irá movê-la.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Manipulações](getting-started-with-manipulations.md)
</dt> </dl>


 