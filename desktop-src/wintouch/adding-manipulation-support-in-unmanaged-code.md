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
# <a name="adding-manipulation-support-in-unmanaged-code"></a><span data-ttu-id="cca7f-113">Adicionando suporte à manipulação em código não gerenciado</span><span class="sxs-lookup"><span data-stu-id="cca7f-113">Adding Manipulation Support in Unmanaged Code</span></span>

<span data-ttu-id="cca7f-114">Esta seção explica como adicionar suporte de manipulação a código não gerenciado implementando um coletor de eventos para a interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .</span><span class="sxs-lookup"><span data-stu-id="cca7f-114">This section explains how to add manipulation support to unmanaged code by implementing an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface.</span></span>

<span data-ttu-id="cca7f-115">A imagem a seguir descreve a arquitetura de manipulação.</span><span class="sxs-lookup"><span data-stu-id="cca7f-115">The following image outlines the manipulation architecture.</span></span>

![ilustração que mostra as mensagens de toque do Windows que são passadas para o processador de manipulação de um objeto, que manipula eventos com a \- interface imanipulationevents](images/manipulation-arch.png)

<span data-ttu-id="cca7f-117">Os dados de toque recebidos do [**WM \_ Touch**](wm-touchdown.md) messages são passados para o [**IMANIPULATIONPROCESSOR**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) junto com a ID de contato da mensagem de toque.</span><span class="sxs-lookup"><span data-stu-id="cca7f-117">Touch data that is received from [**WM\_TOUCH**](wm-touchdown.md) messages is passed to the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) together with the contact ID from the touch message.</span></span> <span data-ttu-id="cca7f-118">Com base na sequência de mensagens, a interface **IManipulationProcessor** calculará que tipo de transformação está sendo executada e quais os valores associados a essa transformação são.</span><span class="sxs-lookup"><span data-stu-id="cca7f-118">Based on the message sequence, the **IManipulationProcessor** interface will calculate what kind of transformation is being performed and what the values associated with this transformation are.</span></span> <span data-ttu-id="cca7f-119">Em seguida, o **IManipulationProcessor** gerará [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) que são manipulados por um coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="cca7f-119">The **IManipulationProcessor** will then generate [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) which are handled by an event sink.</span></span> <span data-ttu-id="cca7f-120">O coletor de eventos pode usar esses valores para executar operações personalizadas no objeto que está sendo transformado.</span><span class="sxs-lookup"><span data-stu-id="cca7f-120">The event sink can then use these values to perform custom operations on the object being transformed.</span></span>

<span data-ttu-id="cca7f-121">Para adicionar suporte à manipulação ao seu aplicativo, você deve seguir estas etapas:</span><span class="sxs-lookup"><span data-stu-id="cca7f-121">To add manipulation support to your application, you must follow these steps:</span></span>

1.  <span data-ttu-id="cca7f-122">Implemente um coletor de eventos para a interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .</span><span class="sxs-lookup"><span data-stu-id="cca7f-122">Implement an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface.</span></span>
2.  <span data-ttu-id="cca7f-123">Crie uma instância de uma interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="cca7f-123">Create an instance of an [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span>
3.  <span data-ttu-id="cca7f-124">Crie uma instância do seu coletor de eventos e configure eventos de toque.</span><span class="sxs-lookup"><span data-stu-id="cca7f-124">Create an instance of your event sink and set up touch events.</span></span>
4.  <span data-ttu-id="cca7f-125">Enviar dados de evento de toque para o processador de manipulação.</span><span class="sxs-lookup"><span data-stu-id="cca7f-125">Send touch event data to the manipulation processor.</span></span>

<span data-ttu-id="cca7f-126">Esta seção explica as etapas que você deve seguir para adicionar suporte à manipulação ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cca7f-126">This section explains the steps that you must follow to add manipulation support to your application.</span></span> <span data-ttu-id="cca7f-127">O código é fornecido em cada etapa para você começar.</span><span class="sxs-lookup"><span data-stu-id="cca7f-127">Code is provided at each step to get you started.</span></span>

> [!Note]  
> <span data-ttu-id="cca7f-128">Você não pode usar manipulações e gestos ao mesmo tempo porque as mensagens de gesto e toque são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="cca7f-128">You cannot use manipulations and gestures at the same time because gesture and touch messages are mutually exclusive.</span></span>

### <a name="implement-an-event-sink-for-_imanipualtionevents-interface"></a><span data-ttu-id="cca7f-129">Implementar um coletor de eventos para a \_ interface IManipualtionEvents</span><span class="sxs-lookup"><span data-stu-id="cca7f-129">Implement an Event Sink for \_IManipualtionEvents Interface</span></span>

<span data-ttu-id="cca7f-130">Antes de criar uma instância do coletor de eventos, você deve criar uma classe que implemente a interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) para eventos.</span><span class="sxs-lookup"><span data-stu-id="cca7f-130">Before you can create an instance of your event sink, you must create a class that implements the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface for eventing.</span></span> <span data-ttu-id="cca7f-131">Este é o coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="cca7f-131">This is your event sink.</span></span> <span data-ttu-id="cca7f-132">Eventos gerados pela interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) são tratados pelo seu coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="cca7f-132">Events generated by the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface are handled by your event sink.</span></span> <span data-ttu-id="cca7f-133">O código a seguir mostra um cabeçalho de exemplo para uma classe que herda a interface **\_ IManipulationEvents** .</span><span class="sxs-lookup"><span data-stu-id="cca7f-133">The following code shows an example header for a class that inherits the **\_IManipulationEvents** interface.</span></span>

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

<span data-ttu-id="cca7f-134">Dado o cabeçalho, você deve criar uma implementação da interface de eventos para que sua classe execute as ações que você deseja que o processador de manipulação realize.</span><span class="sxs-lookup"><span data-stu-id="cca7f-134">Given the header, you must create an implementation of the events interface so that your class performs the actions that you want the manipulation processor to perform.</span></span> <span data-ttu-id="cca7f-135">O código a seguir é um modelo que implementa a funcionalidade mínima de um coletor de eventos para a interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .</span><span class="sxs-lookup"><span data-stu-id="cca7f-135">The following code is a template that implements the minimum functionality of an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface.</span></span>

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

<span data-ttu-id="cca7f-136">Preste atenção extra às implementações dos métodos [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)e [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) na classe.</span><span class="sxs-lookup"><span data-stu-id="cca7f-136">Pay extra attention to implementations of [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta), and [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) methods in the class.</span></span> <span data-ttu-id="cca7f-137">Esses são os métodos mais prováveis na interface que exigirão que você execute operações com base nas informações de manipulação que são passadas no evento.</span><span class="sxs-lookup"><span data-stu-id="cca7f-137">These are the most likely methods in the interface that will require you to perform operations based on the manipulation information that is passed around in the event.</span></span> <span data-ttu-id="cca7f-138">Observe também que o segundo parâmetro no construtor é o objeto usado nas manipulações de evento.</span><span class="sxs-lookup"><span data-stu-id="cca7f-138">Note also that the second parameter in the constructor is the object that is used in the event manipulations.</span></span> <span data-ttu-id="cca7f-139">No código usado para produzir o exemplo, o hWnd do aplicativo é enviado ao construtor para que ele possa ser reposicionado e redimensionado.</span><span class="sxs-lookup"><span data-stu-id="cca7f-139">In the code used for producing the sample, the hWnd for the application is sent to the constructor so that it can be repositioned and resized.</span></span>

### <a name="create-an-instance-of-an-imanipulationprocessor-interface"></a><span data-ttu-id="cca7f-140">Criar uma instância de uma interface IManipulationProcessor</span><span class="sxs-lookup"><span data-stu-id="cca7f-140">Create an instance of an IManipulationProcessor Interface</span></span>

<span data-ttu-id="cca7f-141">No código em que você usará as manipulações, será necessário criar uma instância de uma interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="cca7f-141">In the code where you will use manipulations, you must create an instance of an [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span> <span data-ttu-id="cca7f-142">Primeiro, você deve adicionar suporte para a classe Manipulations.</span><span class="sxs-lookup"><span data-stu-id="cca7f-142">First you must add support for the manipulations class.</span></span> <span data-ttu-id="cca7f-143">O código a seguir mostra como você pode fazer isso em sua classe.</span><span class="sxs-lookup"><span data-stu-id="cca7f-143">The following code shows how you can do this in your class.</span></span>

```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;     
```

<span data-ttu-id="cca7f-144">Depois que você tiver a variável para o processador de manipulação e tiver incluído os cabeçalhos para as manipulações, você precisará criar uma instância da interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="cca7f-144">After you have your variable for the manipulation processor and you have included the headers for manipulations, you have to create an instance of the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span> <span data-ttu-id="cca7f-145">Este é um objeto COM.</span><span class="sxs-lookup"><span data-stu-id="cca7f-145">This is a COM object.</span></span> <span data-ttu-id="cca7f-146">Portanto, você deve chamar [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)e, em seguida, criar uma instância de sua referência para o **IManipulationProcessor**.</span><span class="sxs-lookup"><span data-stu-id="cca7f-146">Therefore, you must call [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), and then create an instance of your reference to the **IManipulationProcessor**.</span></span> <span data-ttu-id="cca7f-147">O código a seguir mostra como você pode criar uma instância dessa interface.</span><span class="sxs-lookup"><span data-stu-id="cca7f-147">The following code shows how you can create an instance of this interface.</span></span>

```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
```

### <a name="create-an-instance-of-your-event-sink-and-set-up-touch-events"></a><span data-ttu-id="cca7f-148">Criar uma instância do seu coletor de eventos e configurar eventos de toque</span><span class="sxs-lookup"><span data-stu-id="cca7f-148">Create an instance of your Event Sink and set up Touch Events</span></span>

<span data-ttu-id="cca7f-149">Inclua a definição de sua classe de coletor de eventos em seu código e, em seguida, adicione uma variável para a classe de coletor de eventos Manipulation.</span><span class="sxs-lookup"><span data-stu-id="cca7f-149">Include the definition for your event sink class to your code and then add a variable for the manipulation event sink class.</span></span> <span data-ttu-id="cca7f-150">O exemplo de código a seguir inclui o cabeçalho para a implementação de classe e configura uma variável global para armazenar o coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="cca7f-150">The following code example includes the header for the class implementation and sets up a global variable to store the event sink.</span></span>

```C++
//Include your definition of the event sink, CManipulationEventSink.h in this case
#include "CManipulationEventSink.h"    
     
// Set up a variable to point to the manipulation event sink implementation class    
CManipulationEventSink* g_pManipulationEventSink;   
```

<span data-ttu-id="cca7f-151">Depois de ter a variável e incluir sua definição para a nova classe de coletor de eventos, você pode construir a classe usando o processador de manipulação que você configurou na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="cca7f-151">After you have the variable and have included your definition for the new event sink class, you can construct the class by using the manipulation processor that you have set up in the previous step.</span></span> <span data-ttu-id="cca7f-152">O código a seguir mostra como uma instância dessa classe seria criada a partir de **OnInitDialog**.</span><span class="sxs-lookup"><span data-stu-id="cca7f-152">The following code shows how an instance of this class would be created from **OnInitDialog**.</span></span>

```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```

> [!Note]  
> <span data-ttu-id="cca7f-153">A maneira como você cria uma instância do seu coletor de eventos depende do que você está fazendo com os dados de manipulação.</span><span class="sxs-lookup"><span data-stu-id="cca7f-153">The way that you create an instance of your event sink depends on what you are doing with the manipulation data.</span></span> <span data-ttu-id="cca7f-154">Na maioria dos casos, você criará um coletor de eventos do processador de manipulação que não tem o mesmo construtor que este exemplo.</span><span class="sxs-lookup"><span data-stu-id="cca7f-154">In most cases, you will create a manipulation processor event sink that does not have the same constructor as this example.</span></span>

### <a name="send-touch-event-data-to-the-manipulation-processor"></a><span data-ttu-id="cca7f-155">Enviar dados de evento de toque para o processador de manipulação</span><span class="sxs-lookup"><span data-stu-id="cca7f-155">Send Touch Event Data to the Manipulation Processor</span></span>

<span data-ttu-id="cca7f-156">Agora que o processador de manipulação e o coletor de eventos foram configurados, você deve alimentar os dados de toque no processador de manipulação para disparar eventos de manipulação.</span><span class="sxs-lookup"><span data-stu-id="cca7f-156">Now that you have your manipulation processor and event sink set up, you must feed touch data to the manipulation processor to trigger manipulation events.</span></span>

> [!Note]  
> <span data-ttu-id="cca7f-157">Esse é o mesmo procedimento discutido em [introdução com mensagens de toque do Windows](getting-started-with-multi-touch-messages.md).</span><span class="sxs-lookup"><span data-stu-id="cca7f-157">This is the same procedure as discussed in [Getting Started with Windows Touch Messages](getting-started-with-multi-touch-messages.md).</span></span>

<span data-ttu-id="cca7f-158">Primeiro, você criará um código para decodificar as mensagens do [**WM \_ Touch**](wm-touchdown.md) e enviá-las para a interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) para gerar eventos.</span><span class="sxs-lookup"><span data-stu-id="cca7f-158">First, you will create some code to decode the [**WM\_TOUCH**](wm-touchdown.md) messages and send them to the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface to raise events.</span></span> <span data-ttu-id="cca7f-159">O código a seguir mostra uma implementação de exemplo que é chamada do método **WndProc** e retorna um **LRESULT** para mensagens.</span><span class="sxs-lookup"><span data-stu-id="cca7f-159">The following code shows an example implementation that is called from the **WndProc** method and return an **LRESULT** for messaging.</span></span>

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

<span data-ttu-id="cca7f-160">Agora que você tem um método utilitário para decodificar a mensagem do [**WM \_ Touch**](wm-touchdown.md) , você deve passar as mensagens do **WM \_ Touch** para a função utilitário do seu método **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="cca7f-160">Now that you have a utility method for decoding the [**WM\_TOUCH**](wm-touchdown.md) message, you must pass the **WM\_TOUCH** messages to the utility function from your **WndProc** method.</span></span> <span data-ttu-id="cca7f-161">O código a seguir mostra como você pode fazer isso.</span><span class="sxs-lookup"><span data-stu-id="cca7f-161">The following code shows how you can do this.</span></span>

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

<span data-ttu-id="cca7f-162">Os métodos personalizados que você implementou em seu coletor de eventos agora devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="cca7f-162">The custom methods that you have implemented in your event sink should now work.</span></span> <span data-ttu-id="cca7f-163">Neste exemplo, tocar na janela irá movê-la.</span><span class="sxs-lookup"><span data-stu-id="cca7f-163">In this example, touching the window will move it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cca7f-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cca7f-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cca7f-165">Manipulações</span><span class="sxs-lookup"><span data-stu-id="cca7f-165">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>


 