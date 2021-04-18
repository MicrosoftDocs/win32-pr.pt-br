---
description: Esta seção explica como recuperar a marcação MathML do controle de entrada matemática usando o Active Template Library (ATL) e o Component Object Model (COM).
ms.assetid: 352d2a0c-8275-4fe4-b523-4c74126ffadf
title: Recebendo entrada do controle de entrada de matemática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 830c8f57bb7b27c305928cf68b658dcc37ede5d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793340"
---
# <a name="receiving-input-from-the-math-input-control"></a><span data-ttu-id="47306-103">Recebendo entrada do controle de entrada de matemática</span><span class="sxs-lookup"><span data-stu-id="47306-103">Receiving Input from the Math Input Control</span></span>

<span data-ttu-id="47306-104">Esta seção explica como recuperar a marcação MathML do controle de entrada matemática usando o Active Template Library (ATL) e o Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="47306-104">This section explains how to retrieve the MathML markup from the math input control using the Active Template Library (ATL) and the Component Object Model (COM).</span></span>

<span data-ttu-id="47306-105">Para recuperar a equação matemática reconhecida do controle de entrada de matemática, você pode substituir o comportamento que acontece quando o botão de inserção é pressionado.</span><span class="sxs-lookup"><span data-stu-id="47306-105">To retrieve the recognized math equation from the math input control, you can override the behavior that happens when the insert button is pressed.</span></span> <span data-ttu-id="47306-106">Para fazer isso, você precisará configurar um manipulador de eventos que implementa os vários eventos com suporte na interface [**\_ IMathInputControlEvents**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) .</span><span class="sxs-lookup"><span data-stu-id="47306-106">To do this, you will need to set up an event handler that implements the various events that are supported by the [**\_IMathInputControlEvents**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) interface.</span></span> <span data-ttu-id="47306-107">A configuração do manipulador de eventos envolve a execução das seguintes etapas para os eventos aos quais você deseja dar suporte (inserir, nesse caso).</span><span class="sxs-lookup"><span data-stu-id="47306-107">Setting up the events handler involves the performing the following steps for the events you want to support (insert in this case).</span></span>

-   [<span data-ttu-id="47306-108">Criar uma classe de modelo que contém coletores de eventos</span><span class="sxs-lookup"><span data-stu-id="47306-108">Create a template class that contains event sinks</span></span>](#create-a-template-class-that-contains-event-sinks)
-   [<span data-ttu-id="47306-109">Configurar os manipuladores de eventos</span><span class="sxs-lookup"><span data-stu-id="47306-109">Set up the event handlers</span></span>](#set-up-the-event-handlers)
-   [<span data-ttu-id="47306-110">Herdar a classe do manipulador de eventos em sua classe principal</span><span class="sxs-lookup"><span data-stu-id="47306-110">Inherit the event handler class in your main class</span></span>](#inherit-the-event-handler-class-in-your-main-class)
-   [<span data-ttu-id="47306-111">Inicialize sua classe para herdar o (s) coletor (es) de eventos</span><span class="sxs-lookup"><span data-stu-id="47306-111">Initialize your class to inherit the event sink(s)</span></span>](#initialize-your-class-to-inherit-the-event-sinks)

## <a name="create-a-template-class-that-contains-event-sinks"></a><span data-ttu-id="47306-112">Criar uma classe de modelo que contém coletores de eventos</span><span class="sxs-lookup"><span data-stu-id="47306-112">Create a template class that contains event sinks</span></span>

<span data-ttu-id="47306-113">Ao implementar um coletor de eventos que usa o controle de entrada de matemática, você deve primeiro especificar uma ID de coletor. Em seguida, você deve criar uma classe de modelo herdada do evento, do manipulador de controle de eventos e das interfaces de evento de controle de entrada matemática.</span><span class="sxs-lookup"><span data-stu-id="47306-113">When you are implementing an event sink that uses the math input control, you must first specify a sink id. You must then create a template class that inherits from the event, event control handler, and math input control event interfaces.</span></span> <span data-ttu-id="47306-114">O código a seguir mostra como definir uma ID de coletor e criar uma classe de modelo, CMathInputControlEventHandler, que herda das interfaces necessárias.</span><span class="sxs-lookup"><span data-stu-id="47306-114">The following code shows how to set a sink id and create such a template class, CMathInputControlEventHandler, that inherits from the requisite interfaces.</span></span> <span data-ttu-id="47306-115">Essa classe de modelo também é configurada para ter um ponteiro de interface desconhecido privado que será usado para passar o controle de entrada de matemática para ele na inicialização e o \_ membro m ulAdviseCount para contar o número de chamadas para Advise/Unadvise.</span><span class="sxs-lookup"><span data-stu-id="47306-115">This template class also is set up to have a private unknown interface pointer that will be used to pass the math input control to it on initialization and the m\_ulAdviseCount member to count the number of calls to advise / unadvise.</span></span>


```
  
#pragma once
static const int MATHINPUTCONTROL_SINK_ID = 1 ;

template <class T>
class ATL_NO_VTABLE CMathInputControlEventHandler :
    public IDispEventSimpleImpl<MATHINPUTCONTROL_SINK_ID, CMathInputControlEventHandler<T>, &__uuidof(_IMathInputControlEvents)>
{
private:
    IUnknown    *m_pUnknown;
    ULONG m_ulAdviseCount;
    CDialog *m_pMain;

```



> [!Note]  
> <span data-ttu-id="47306-116">O membro **m \_ pMain** deve ser diferente em sua implementação se você não estiver usando uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="47306-116">The member **m\_pMain** should be different in your implementation if you are not using a dialog.</span></span>

 

<span data-ttu-id="47306-117">Agora que você tem a classe de modelo básica, deve fornecer uma declaração de encaminhamento para os manipuladores de eventos que serão substituídos e, em seguida, configurar um mapa do coletor para os eventos que você estará lidando.</span><span class="sxs-lookup"><span data-stu-id="47306-117">Now that you have the basic template class, you must give a forward declaration for the event handlers that you will be overriding and must then set up a sink map for the events you will be handling.</span></span> <span data-ttu-id="47306-118">O código a seguir mostra como configurar manipuladores de eventos para o método [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) , chamado quando um usuário clica no botão Insert no controle de entrada Math e o método [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) , chamado quando um usuário clica no botão Cancel no controle de entrada Math.</span><span class="sxs-lookup"><span data-stu-id="47306-118">The following code shows how to set up event handlers for the [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) method, called when a user clicks the insert button on the math input control, and the [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) method, called when a user clicks the cancel button on the math input control.</span></span>


```
  
public:
    static const _ATL_FUNC_INFO OnMICInsertInfo; // = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
    static const _ATL_FUNC_INFO OnMICCloseInfo;  // = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

    BEGIN_SINK_MAP(CMathInputControlEventHandler)
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICInsert, OnMICInsert, const_cast<_ATL_FUNC_INFO*>(&OnMICInsertInfo))
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICClose, OnMICClose, const_cast<_ATL_FUNC_INFO*>(&OnMICCloseInfo))  
    END_SINK_MAP()
```



<span data-ttu-id="47306-119">Como você estará trabalhando com o controle de entrada de matemática, será útil definir uma referência interna para a interface relevante.</span><span class="sxs-lookup"><span data-stu-id="47306-119">Since you will be working with the math input control, it will be useful to set an internal reference to the relevant interface.</span></span> <span data-ttu-id="47306-120">A função do utilitário a seguir é criada na classe de exemplo para definir essa referência.</span><span class="sxs-lookup"><span data-stu-id="47306-120">The following utility function is created in the example class to set this reference.</span></span>


```
    
  HRESULT Initialize(IUnknown *pUnknown, CDialog *pMain)
  {
    m_pMain  = pMain;
    m_pUnknown = pUnknown;
    m_ulAdviseCount = 0;
    return S_OK;
  }
  
```



## <a name="set-up-the-event-handlers"></a><span data-ttu-id="47306-121">Configurar os manipuladores de eventos</span><span class="sxs-lookup"><span data-stu-id="47306-121">Set up the event handlers</span></span>

<span data-ttu-id="47306-122">Depois de configurar os coletores de eventos, será necessário criar suas implementações dos coletores de eventos.</span><span class="sxs-lookup"><span data-stu-id="47306-122">Once you have set up the event sinks, you will need to create your implementations of the event sinks.</span></span> <span data-ttu-id="47306-123">Em ambos os métodos no exemplo de código a seguir, os coletores de eventos recuperam um identificador para a interface de controle de entrada matemática.</span><span class="sxs-lookup"><span data-stu-id="47306-123">In both of the methods in the following code example, the event sinks retrieve a handle to the math input control interface.</span></span> <span data-ttu-id="47306-124">Na função [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) , o resultado do reconhecimento é exibido como MathML e o controle é oculto.</span><span class="sxs-lookup"><span data-stu-id="47306-124">In the [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) function, the recognition result is displayed as MathML and the control is hidden.</span></span> <span data-ttu-id="47306-125">Na função [**fechar**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) , o controle de entrada de matemática está oculto.</span><span class="sxs-lookup"><span data-stu-id="47306-125">In the [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) function, the math input control is hidden.</span></span>


```
  
    // Methods
    HRESULT __stdcall OnMICInsert( BSTR bstrRecoResult)
    {
        CComQIPtr<IMathInputControl> spMIC(m_pUnknown);
        HRESULT hr=S_OK;
        if (spMIC)
        {           
            MessageBox(NULL,bstrRecoResult,L"Recognition Result",MB_OK);
            hr = spMIC->Hide();
            return hr;  
        }
        return E_FAIL;          
    }

    HRESULT __stdcall OnMICClose()
    {
        CComPtr<IMathInputControl> spMIC;
        HRESULT hr = m_pUnknown->QueryInterface<IMathInputControl>(&spMIC);
        if (SUCCEEDED(hr))
        {           
            hr = spMIC->Hide();
            return hr;  
        }
        return hr;                  
    }
};  
```



## <a name="inherit-the-event-handler-class-in-your-main-class"></a><span data-ttu-id="47306-126">Herdar a classe do manipulador de eventos em sua classe principal</span><span class="sxs-lookup"><span data-stu-id="47306-126">Inherit the event handler class in your main class</span></span>

<span data-ttu-id="47306-127">Depois de implementar a classe de modelo, você precisará herdá-la na classe em que você configurará seu controle de entrada matemática.</span><span class="sxs-lookup"><span data-stu-id="47306-127">After you have your template class implemented, you will need to inherit it into the class that you will be setting up your math input control in.</span></span> <span data-ttu-id="47306-128">Para os fins deste guia, essa classe é uma caixa de diálogo, CMIC \_ test \_ EVENTSDlg.</span><span class="sxs-lookup"><span data-stu-id="47306-128">For the purposes of this guide, this class is a dialog, CMIC\_TEST\_EVENTSDlg.</span></span> <span data-ttu-id="47306-129">No cabeçalho da caixa de diálogo, os cabeçalhos de requisito devem ser incluídos e a classe de modelo que você criou deve ser herdada.</span><span class="sxs-lookup"><span data-stu-id="47306-129">In the dialog header, the requisite headers must be included and the template class you created must be inherited.</span></span> <span data-ttu-id="47306-130">A classe que você está herdando e os manipuladores de eventos devem ter declarações de encaminhamento para que o modelo possa ser implementado.</span><span class="sxs-lookup"><span data-stu-id="47306-130">The class you're inheriting within and the event handlers must have forward declarations so that the template can be implemented.</span></span> <span data-ttu-id="47306-131">O exemplo de código a seguir mostra como isso é feito.</span><span class="sxs-lookup"><span data-stu-id="47306-131">The following code example shows how this is done.</span></span>


```
#pragma once
#include <atlbase.h>
#include <atlwin.h>

// include for MIC
#include "micaut.h"

// include for event sinks
#include <iacom.h>
#include "mathinputcontroleventhandler.h"

class CMIC_TEST_EVENTSDlg;

const _ATL_FUNC_INFO CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::OnMICInsertInfo = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
const _ATL_FUNC_INFO CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::OnMICCloseInfo = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

// CMIC_TEST_EVENTSDlg dialog
class CMIC_TEST_EVENTSDlg : public CDialog,
    public CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>
{
  public:
  CComPtr<IMathInputControl> m_spMIC; // Math Input Control

  
```



> [!Note]  
> <span data-ttu-id="47306-132">O tipo de modelo, **CMIC \_ test \_ EventsDlg**, será diferente, a menos que você tenha nomeado sua classe da mesma forma que o exemplo.</span><span class="sxs-lookup"><span data-stu-id="47306-132">The template type, **CMIC\_TEST\_EventsDlg**, will be different unless you have named your class the same as the example.</span></span>

 

## <a name="initialize-your-class-to-inherit-the-event-sinks"></a><span data-ttu-id="47306-133">Inicialize sua classe para herdar o (s) coletor (es) de eventos</span><span class="sxs-lookup"><span data-stu-id="47306-133">Initialize your class to inherit the event sink(s)</span></span>

<span data-ttu-id="47306-134">Depois de configurar sua classe para herdar da classe de modelo, você estará pronto para configurá-la para manipular eventos.</span><span class="sxs-lookup"><span data-stu-id="47306-134">Once you have set up your class to inherit from the template class, you are ready to set it up to handle events.</span></span> <span data-ttu-id="47306-135">Isso consistirá na inicialização da classe para ter um identificador para o controle de entrada matemática e para a classe de chamada.</span><span class="sxs-lookup"><span data-stu-id="47306-135">This will consist of initializing the class to have a handle to the math input control and the calling class.</span></span> <span data-ttu-id="47306-136">Além disso, o controle de entrada de matemática para manipular eventos de deve ser enviado para o método DispEventAdvise que a classe de exemplo CMathInputControlEventHandler herda.</span><span class="sxs-lookup"><span data-stu-id="47306-136">Additionally, the math input control to handle events from must be sent to the DispEventAdvise method that the CMathInputControlEventHandler example class inherits.</span></span> <span data-ttu-id="47306-137">O código a seguir é chamado do método OnInitDialog na classe de exemplo para executar essas ações.</span><span class="sxs-lookup"><span data-stu-id="47306-137">The following code is called from the OnInitDialog method in the example class to perform these actions.</span></span>


```
// includes for implementation
#include "micaut_i.c"

// include for event handler
#include "mathinputcontroleventhandler.h"

...

OnInitDialog{
  ...

  // TODO: Add extra initialization here
  CoInitialize(NULL);
  HRESULT hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
  if (SUCCEEDED(hr)){
    hr = CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::Initialize(m_spMIC, this);
      if (SUCCEEDED(hr)){
        hr = CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::DispEventAdvise(m_spMIC);            
        if (SUCCEEDED(hr)){
          hr = m_spMIC->Show();  
        }
      }
    }
  }  
}
  
```



> [!Note]  
> <span data-ttu-id="47306-138">O tipo de modelo, CMIC \_ test \_ EventsDlg neste exemplo, será diferente, a menos que você tenha nomeado sua classe da mesma forma que o exemplo.</span><span class="sxs-lookup"><span data-stu-id="47306-138">The template type, CMIC\_TEST\_EventsDlg in this example, will be different unless you have named your class the same as the example.</span></span>

 

 

 
