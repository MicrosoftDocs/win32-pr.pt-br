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
# <a name="c-event-sinks-sample"></a><span data-ttu-id="2cc2f-105">Exemplo de coletores de eventos do C++</span><span class="sxs-lookup"><span data-stu-id="2cc2f-105">C++ Event Sinks Sample</span></span>

<span data-ttu-id="2cc2f-106">Este programa demonstra como você pode criar um aplicativo que captura eventos de InkCollector usando apenas o C++.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-106">This program demonstrates how you can build an application that captures InkCollector events using only C++.</span></span> <span data-ttu-id="2cc2f-107">Este programa cocria um objeto [**InkCollector**](inkcollector-class.md) para habilitar a tinta na janela.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-107">This program co-creates an [**InkCollector**](inkcollector-class.md) object to ink -enable the window.</span></span> <span data-ttu-id="2cc2f-108">Ele exibe uma caixa de mensagem sempre que um evento [**Stroke**](inkcollector-stroke.md) é recebido.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-108">It displays a message box whenever a [**Stroke**](inkcollector-stroke.md) event is received.</span></span>

## <a name="defining-a-wrapper-for-ink-collector-events"></a><span data-ttu-id="2cc2f-109">Definindo um wrapper para eventos do coletor de tinta</span><span class="sxs-lookup"><span data-stu-id="2cc2f-109">Defining a Wrapper for Ink Collector Events</span></span>

<span data-ttu-id="2cc2f-110">A `InkCollectorEvents` classe lida com a passagem de eventos do coletor de tinta do coletor de tinta para o usuário desta classe.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-110">The `InkCollectorEvents` Class handles passing ink collector events from the ink collector to the user of this class.</span></span> <span data-ttu-id="2cc2f-111">O `AdviseInkCollector` método configura a conexão entre o objeto [**InkCollector**](inkcollector-class.md) e essa classe.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-111">The `AdviseInkCollector` method sets up the connection between the [**InkCollector**](inkcollector-class.md) object and this class.</span></span> <span data-ttu-id="2cc2f-112">O `Invoke` método converte a notificação de evento [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) em uma chamada para uma função virtual que o usuário dessa classe pode substituir para processar um evento específico.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-112">The `Invoke` method converts the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) event notification into a call to a virtual function that the user of this class can override to process a particular event.</span></span>

> [!Note]  
> <span data-ttu-id="2cc2f-113">Você deve fazer mais do que substituir a função virtual para um manipulador de eventos para obter esse evento.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-113">You must do more than override the virtual function for an event handler to get that event.</span></span> <span data-ttu-id="2cc2f-114">Para todos os eventos, exceto os padrão, você precisa chamar o método [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) do coletor de tinta para garantir a obtenção de um evento.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-114">For all but default events, you have to call the ink collector's [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) method to guarantee getting an event.</span></span> <span data-ttu-id="2cc2f-115">Em segundo lugar, esse objeto é empacotado em thread livre, de modo que todos os manipuladores de eventos implementados também precisam ser segmentados gratuitamente.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-115">Secondly, this object marshals itself free threaded so all implemented event handlers need to be free threaded as well.</span></span> <span data-ttu-id="2cc2f-116">De importância específica é usar APIs do Windows, o que pode fazer com que um comutador para outro thread como o manipulador de eventos não tenha garantia de estar em execução no mesmo thread que a janela conectada ao coletor de tinta.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-116">Of particular importance is using Windows APIs, which may cause a switch to another thread as the event handler is not guaranteed to be running on the same thread as the window connected with the ink collector.</span></span>

 


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



<span data-ttu-id="2cc2f-117">O `Init` método chama [CoCreateFreeThreadedMarshaler](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) para configurar um marshaler livre de threads.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-117">The `Init` method calls [CoCreateFreeThreadedMarshaler](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) to set up a free threaded marshaler.</span></span>


```C++
// Init: set up free threaded marshaller.
HRESULT Init()
{
    return CoCreateFreeThreadedMarshaler(this, &m_punkFTM);
}
```



<span data-ttu-id="2cc2f-118">O `AdviseInkCollector` método configura a conexão entre o objeto [**InkCollector**](inkcollector-class.md) e essa classe.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-118">The `AdviseInkCollector` method sets up the connection between the [**InkCollector**](inkcollector-class.md) object and this class.</span></span> <span data-ttu-id="2cc2f-119">Primeiro, ele recupera um ponto de conexão para o coletor de tinta.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-119">It first retrieves a connection point to the ink collector.</span></span> <span data-ttu-id="2cc2f-120">Em seguida, ele recupera um ponteiro para o para `IInkCollectorEvents` que ele possa estabelecer uma conexão de consultoria com o controle.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-120">Then it retrieves a pointer to the `IInkCollectorEvents` so that it may establish an advisory connection to the control.</span></span>


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



<span data-ttu-id="2cc2f-121">O `UnadviseInkCollector` método libera as conexões que o objeto tem ao controle.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-121">The `UnadviseInkCollector` method releases the connections the object has to the control.</span></span>


```C++
// Remove the connection of the sink to the Ink Collector
HRESULT UnadviseInkCollector()
{
    HRESULT hr = m_pIConnectionPoint->Unadvise(m_dwCookie);m_pIConnectionPoint->Release();
m_pIConnectionPoint = NULL;
    return hr;
}
```



## <a name="defining-an-ink-collector-events-handler"></a><span data-ttu-id="2cc2f-122">Definindo um manipulador de eventos do coletor de tinta</span><span class="sxs-lookup"><span data-stu-id="2cc2f-122">Defining an Ink Collector Events Handler</span></span>

<span data-ttu-id="2cc2f-123">A classe CMyInkEvents substitui o comportamento padrão do manipulador de eventos [**Stroke**](inkcollector-stroke.md) da classe InkCollectorEvents.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-123">The CMyInkEvents Class overrides the default behavior of the [**Stroke**](inkcollector-stroke.md) event handler of the InkCollectorEvents Class.</span></span> <span data-ttu-id="2cc2f-124">O método Stroke exibe uma caixa de mensagem quando o [**InkCollector**](inkcollector-class.md) recebe um evento **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="2cc2f-124">The Stroke method displays a message box when the [**InkCollector**](inkcollector-class.md) receives a **Stroke** event.</span></span>


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



## <a name="defining-an-ink-collector-wrapper"></a><span data-ttu-id="2cc2f-125">Definindo um wrapper do coletor de tinta</span><span class="sxs-lookup"><span data-stu-id="2cc2f-125">Defining an Ink Collector Wrapper</span></span>

<span data-ttu-id="2cc2f-126">O método Init da classe CMyInkCollector declara e inicializa um objeto CMyInkEvents.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-126">The CMyInkCollector Class's Init method declares and initializes a CMyInkEvents object.</span></span> <span data-ttu-id="2cc2f-127">Em seguida, ele cria um objeto [**InkCollector**](inkcollector-class.md) e associa o coletor de tinta e o manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-127">It then creates an [**InkCollector**](inkcollector-class.md) object and associates the ink collector and the event handler.</span></span> <span data-ttu-id="2cc2f-128">Por fim, o **InkCollector** é anexado à janela e habilitado.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-128">Finally, the **InkCollector** is attached to the window and enabled.</span></span>


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



## <a name="accessing-the-tablet-pc-interfaces-and-the-wrapper-classes"></a><span data-ttu-id="2cc2f-129">Acessando as interfaces do Tablet PC e as classes de wrapper</span><span class="sxs-lookup"><span data-stu-id="2cc2f-129">Accessing the Tablet PC Interfaces and the Wrapper Classes</span></span>

<span data-ttu-id="2cc2f-130">Primeiro, inclua os cabeçalhos para interfaces de automação do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-130">First, include the headers for Tablet PC Automation interfaces.</span></span> <span data-ttu-id="2cc2f-131">Eles são instalados com o Microsoft <entity type="reg"/> Windows <entity type="reg"/> XP Tablet PC Edition Development Kit 1,7.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-131">These are installed with the Microsoft<entity type="reg"/> Windows<entity type="reg"/> XP Tablet PC Edition Development Kit 1.7.</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="2cc2f-132">Em seguida, inclua os cabeçalhos para as classes wrapper e o manipulador de eventos [**InkCollector**](inkcollector-class.md) foi definido.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-132">Then, include the headers for the wrapper classes and [**InkCollector**](inkcollector-class.md) event handler was defined.</span></span>


```C++
#include "TpcConpt.h"
#include "EventSink.h"
```



## <a name="calling-the-wrapper-classes"></a><span data-ttu-id="2cc2f-133">Chamando as classes de wrapper</span><span class="sxs-lookup"><span data-stu-id="2cc2f-133">Calling the Wrapper Classes</span></span>

<span data-ttu-id="2cc2f-134">Quando a janela é criada, o procedimento de janela cria um wrapper do coletor de tinta e inicializa o wrapper.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-134">When the window is created, the Window procedure creates an ink collector wrapper and initializes the wrapper.</span></span> <span data-ttu-id="2cc2f-135">Quando a janela é destruída, o procedimento de janela exclui o wrapper do coletor de tinta.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-135">When the window is destroyed, the Window procedure deletes the ink collector wrapper.</span></span> <span data-ttu-id="2cc2f-136">O wrapper do coletor de tinta lida com a criação e a exclusão de seu manipulador de eventos associado.</span><span class="sxs-lookup"><span data-stu-id="2cc2f-136">The ink collector wrapper handles the creation and deletion of its associated event handler.</span></span>


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



 

 
