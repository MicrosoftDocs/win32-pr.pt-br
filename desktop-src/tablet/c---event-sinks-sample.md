---
description: Este programa demonstra como você pode criar um aplicativo que captura eventos de InkCollector usando apenas o C++. Este programa cocria um objeto InkCollector para habilitar a tinta na janela. Ele exibe uma caixa de mensagem sempre que um evento Stroke é recebido.
ms.assetid: 91450559-ae47-457a-a709-b4e4e78bde22
title: Exemplo de coletores de eventos do C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e950254293b676088d8b281624c089b098e5dca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813611"
---
# <a name="c-event-sinks-sample"></a>Exemplo de coletores de eventos do C++

Este programa demonstra como você pode criar um aplicativo que captura eventos de InkCollector usando apenas o C++. Este programa cocria um objeto [**InkCollector**](inkcollector-class.md) para habilitar a tinta na janela. Ele exibe uma caixa de mensagem sempre que um evento [**Stroke**](inkcollector-stroke.md) é recebido.

## <a name="defining-a-wrapper-for-ink-collector-events"></a>Definindo um wrapper para eventos do coletor de tinta

A `InkCollectorEvents` classe lida com a passagem de eventos do coletor de tinta do coletor de tinta para o usuário desta classe. O `AdviseInkCollector` método configura a conexão entre o objeto [**InkCollector**](inkcollector-class.md) e essa classe. O `Invoke` método converte a notificação de evento [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) em uma chamada para uma função virtual que o usuário dessa classe pode substituir para processar um evento específico.

> [!Note]  
> Você deve fazer mais do que substituir a função virtual para um manipulador de eventos para obter esse evento. Para todos os eventos, exceto os padrão, você precisa chamar o método [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) do coletor de tinta para garantir a obtenção de um evento. Em segundo lugar, esse objeto é empacotado em thread livre, de modo que todos os manipuladores de eventos implementados também precisam ser segmentados gratuitamente. De importância específica é usar APIs do Windows, o que pode fazer com que um comutador para outro thread como o manipulador de eventos não tenha garantia de estar em execução no mesmo thread que a janela conectada ao coletor de tinta.

 


```C++
// Invoke translates from IDispatch to an event callout
//  that can be overriden by a subclass of this class.
STDMETHOD(Invoke)(
   DISPID dispidMember, 
    REFIID riid,
    LCID lcid, 
    WORD /*wFlags*/, 
    DISPPARAMS* pdispparams, 
    VARIANT* pvarResult,
    EXCEPINFO* /*pexcepinfo*/, 
    UINT* /*puArgErr*/)
{
    switch(dispidMember)
    {
        case DISPID_ICEStroke:
            Stroke(
                (IInkCursor*) pdispparams->rgvarg[2].pdispVal,
                (IInkStrokeDisp*) pdispparams->rgvarg[1].pdispVal,
                (VARIANT_BOOL *)pdispparams->rgvarg[0].pboolVal);
            break;
        ...
    }
    return S_OK;
}

virtual void Stroke(
    IInkCursor* Cursor,
    IInkStrokeDisp* Stroke,
    VARIANT_BOOL *Cancel)
{
    // This is a place holder designed to be overridden by
    //  user of this class.
    return;
}
...
```



O `Init` método chama [CoCreateFreeThreadedMarshaler](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) para configurar um marshaler livre de threads.


```C++
// Init: set up free threaded marshaller.
HRESULT Init()
{
    return CoCreateFreeThreadedMarshaler(this, &m_punkFTM);
}
```



O `AdviseInkCollector` método configura a conexão entre o objeto [**InkCollector**](inkcollector-class.md) e essa classe. Primeiro, ele recupera um ponto de conexão para o coletor de tinta. Em seguida, ele recupera um ponteiro para o para `IInkCollectorEvents` que ele possa estabelecer uma conexão de consultoria com o controle.


```C++
// Set up connection between sink and InkCollector
HRESULT AdviseInkCollector(
    IInkCollector *pIInkCollector)
{
    // Get the connection point container
    IConnectionPointContainer *pIConnectionPointContainer;
    HRESULT hr = pIInkCollector->QueryInterface(IID_IConnectionPointContainer, (void **) &pIConnectionPointContainer);
        
    if (FAILED(hr))
        ...
    
    // Find the connection point for Ink Collector events
    hr = pIConnectionPointContainer->FindConnectionPoint(__uuidof(_IInkCollectorEvents), &m_pIConnectionPoint);
        
    if (SUCCEEDED(hr))
    {
        // Hook up sink to connection point
        hr = m_pIConnectionPoint->Advise(this, &m_dwCookie);
    }
    
    if (FAILED(hr))
        ...
    
    // Don't need the connection point container any more.
    pIConnectionPointContainer->Release();
    return hr;
}
```



O `UnadviseInkCollector` método libera as conexões que o objeto tem ao controle.


```C++
// Remove the connection of the sink to the Ink Collector
HRESULT UnadviseInkCollector()
{
    HRESULT hr = m_pIConnectionPoint->Unadvise(m_dwCookie);m_pIConnectionPoint->Release();
m_pIConnectionPoint = NULL;
    return hr;
}
```



## <a name="defining-an-ink-collector-events-handler"></a>Definindo um manipulador de eventos do coletor de tinta

A classe CMyInkEvents substitui o comportamento padrão do manipulador de eventos [**Stroke**](inkcollector-stroke.md) da classe InkCollectorEvents. O método Stroke exibe uma caixa de mensagem quando o [**InkCollector**](inkcollector-class.md) recebe um evento **Stroke** .


```C++
class CMyInkEvents : public InkCollectorEvents
{
public:

    // Event: Stroke
    virtual void Stroke(
        IInkCursor* Cursor,
        IInkStrokeDisp* Stroke,
        VARIANT_BOOL *Cancel)
    {
        // Demonstrate that the event notification was received.
        MessageBox(m_hWnd, "Stroke Event", "Event Received", MB_OK);
    }
    
    CMyInkEvents()
    {
        m_hWnd = NULL;
    }
    
    HRESULT Init(
        HWND hWnd)
    {
        m_hWnd = hWnd;
        return InkCollectorEvents::Init();
    }    
    
    HWND m_hWnd;
};
```



## <a name="defining-an-ink-collector-wrapper"></a>Definindo um wrapper do coletor de tinta

O método Init da classe CMyInkCollector declara e inicializa um objeto CMyInkEvents. Em seguida, ele cria um objeto [**InkCollector**](inkcollector-class.md) e associa o coletor de tinta e o manipulador de eventos. Por fim, o **InkCollector** é anexado à janela e habilitado.


```C++
// Handle all initializaton
HRESULT Init(
HWND hWnd)
{
    // Initialize event sink. This consists of setting
    //  up the free threaded marshaler.
    HRESULT hr = m_InkEvents.Init(hWnd);

    if (FAILED(hr))
        ...

    // Create the ink collector
    hr = CoCreateInstance(CLSID_InkCollector, NULL, CLSCTX_ALL, IID_IInkCollector, (void **) &m_pInkCollector);

    if (FAILED(hr))
        ...

    // Set up connection between Ink Collector and our event sink
    hr = m_InkEvents.AdviseInkCollector(m_pInkCollector);

    if (FAILED(hr))
        ...

    // Attach Ink Collector to window
    hr = m_pInkCollector->put_hWnd((long) hWnd);

    if (FAILED(hr))
        ...

    // Allow Ink Collector to receive input.
    return m_pInkCollector->put_Enabled(VARIANT_TRUE);
}
```



## <a name="accessing-the-tablet-pc-interfaces-and-the-wrapper-classes"></a>Acessando as interfaces do Tablet PC e as classes de wrapper

Primeiro, inclua os cabeçalhos para interfaces de automação do Tablet PC. Eles são instalados com o Microsoft <entity type="reg"/> Windows <entity type="reg"/> XP Tablet PC Edition Development Kit 1,7.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



Em seguida, inclua os cabeçalhos para as classes wrapper e o manipulador de eventos [**InkCollector**](inkcollector-class.md) foi definido.


```C++
#include "TpcConpt.h"
#include "EventSink.h"
```



## <a name="calling-the-wrapper-classes"></a>Chamando as classes de wrapper

Quando a janela é criada, o procedimento de janela cria um wrapper do coletor de tinta e inicializa o wrapper. Quando a janela é destruída, o procedimento de janela exclui o wrapper do coletor de tinta. O wrapper do coletor de tinta lida com a criação e a exclusão de seu manipulador de eventos associado.


```C++
case WM_CREATE:

    // Allocate and initialize memory for object
    pmic = new CMyInkCollector();

    if (pmic != NULL)
    {
        // Real initialization. This consists of creating
        //  an ink collector object and attaching it to
        //  the current window. 
        if (SUCCEEDED(pmic->Init(hWnd)))
        {
            return 0;
        }
        
        // Failure free resources.
        delete pmic;
        pmic = NULL;
    }
    
    return -1;
...
case WM_DESTROY:
    // The destructor for the object handles releasing the
    //  InkCollector and disconnecting the InkCollector
    //  from the object's event sink. 
    delete pmic;
    pmic = NULL;
    PostQuitMessage(0);
    break;
```



 

 
