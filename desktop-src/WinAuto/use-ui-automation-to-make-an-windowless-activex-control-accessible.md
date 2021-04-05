---
title: Como usar a automação da interface do usuário para tornar um controle ActiveX sem janela acessível
description: Descreve como usar a automação da interface do usuário da Microsoft \ 32; API para garantir que o controle Microsoft ActiveX sem janela esteja acessível para aplicativos cliente de tecnologia assistencial (AT).
ms.assetid: D584E90D-6537-4F48-8553-0DCA061FAF2A
keywords:
- Controle ActiveX sem janela, acessibilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0ada1d26463b0654c1808f6e4fd43f571687d9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641379"
---
# <a name="how-to-use-ui-automation-to-make-a-windowless-activex-control-accessible"></a><span data-ttu-id="c426b-104">Como usar a automação da interface do usuário para tornar um controle ActiveX sem janela acessível</span><span class="sxs-lookup"><span data-stu-id="c426b-104">How to Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>

<span data-ttu-id="c426b-105">Descreve como usar a API de automação da interface do usuário da Microsoft para garantir que o controle Microsoft ActiveX sem janela esteja acessível a aplicativos cliente de tecnologia assistencial (AT).</span><span class="sxs-lookup"><span data-stu-id="c426b-105">Describes how to use the Microsoft UI Automation API to ensure that your windowless Microsoft ActiveX control is accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c426b-106">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="c426b-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c426b-107">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="c426b-107">Technologies</span></span>

-   [<span data-ttu-id="c426b-108">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="c426b-108">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="c426b-109">Automação da Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="c426b-109">UI Automation</span></span>](entry-uiauto-win32.md)

### <a name="prerequisites"></a><span data-ttu-id="c426b-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="c426b-110">Prerequisites</span></span>

-   <span data-ttu-id="c426b-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="c426b-111">C/C++</span></span>
-   <span data-ttu-id="c426b-112">Programação do COM (Microsoft Win32 e Component Object Model)</span><span class="sxs-lookup"><span data-stu-id="c426b-112">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="c426b-113">Controles ActiveX sem janela</span><span class="sxs-lookup"><span data-stu-id="c426b-113">Windowless ActiveX Controls</span></span>
-   <span data-ttu-id="c426b-114">Provedores de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="c426b-114">UI Automation providers</span></span>

## <a name="instructions"></a><span data-ttu-id="c426b-115">Instruções</span><span class="sxs-lookup"><span data-stu-id="c426b-115">Instructions</span></span>

### <a name="step-1-implement-the-ui-automation-provider-interfaces"></a><span data-ttu-id="c426b-116">Etapa 1: implementar as interfaces do provedor de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c426b-116">Step 1: Implement the UI Automation provider interfaces.</span></span>

<span data-ttu-id="c426b-117">Para tornar seu aplicativo acessível, você deve implementar as interfaces do provedor de automação da interface do usuário para o controle ActiveX sem janela, incluindo [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment), [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)e [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents).</span><span class="sxs-lookup"><span data-stu-id="c426b-117">To make your application accessible, you must implement the UI Automation provider interfaces for your windowless ActiveX control, including [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment), [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), and [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents).</span></span> <span data-ttu-id="c426b-118">Você deve implementar essas interfaces da mesma forma como faria para um controle baseado em janela, exceto conforme descrito nas etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="c426b-118">You should implement these interfaces just as you would for a window-based control, except as described in the following steps.</span></span> <span data-ttu-id="c426b-119">Para obter mais informações sobre como implementar interfaces de provedor UIA, consulte [Guia do programador do provedor de automação de IU](uiauto-providerportal.md).</span><span class="sxs-lookup"><span data-stu-id="c426b-119">For more information about implementing UIA provider interfaces, see [UI Automation Provider Programmer's Guide](uiauto-providerportal.md).</span></span>

### <a name="step-2-implement-the-iserviceprovider-interface"></a><span data-ttu-id="c426b-120">Etapa 2: implementar a interface IServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="c426b-120">Step 2: Implement the IServiceProvider interface.</span></span>

<span data-ttu-id="c426b-121">Quando um cliente precisa de informações de acessibilidade sobre o controle sem janela, o contêiner de controle chama o método **IServiceProvider:: QueryService** do controle para recuperar o ponteiro de interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) para seu controle.</span><span class="sxs-lookup"><span data-stu-id="c426b-121">When a client needs accessibility information about your windowless control, the control container calls your control's **IServiceProvider::QueryService** method to retrieve the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface pointer for your control.</span></span>

<span data-ttu-id="c426b-122">O exemplo a seguir mostra como implementar o método **QueryService** .</span><span class="sxs-lookup"><span data-stu-id="c426b-122">The following example shows how to implement the **QueryService** method.</span></span>


```C++
STDMETHODIMP CMyAccessibleUIAControl::QueryService(REFGUID guidService,
        REFIID riid, void **ppvObject)
{  
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL; 
 
    if (guidService == __uuidof(IRawElementProviderSimple))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-implement-the-irawelementproviderfragmentnavigate-method"></a><span data-ttu-id="c426b-123">Etapa 3: implementar o método IRawElementProviderFragment:: Navigate.</span><span class="sxs-lookup"><span data-stu-id="c426b-123">Step 3: Implement the IRawElementProviderFragment::Navigate method.</span></span>

<span data-ttu-id="c426b-124">Quando o método [**IRawElementProviderFragment:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) do controle sem janela é chamado para navegar até o pai ou um irmão do provedor raiz do controle sem janela, seu método **Navigate** deve delegar ao método [**IRawElementProviderWindowlessSite:: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) do contêiner de controle.</span><span class="sxs-lookup"><span data-stu-id="c426b-124">When your windowless control’s [**IRawElementProviderFragment::Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method is called to navigate to the parent or a sibling of the windowless control's root provider, your **Navigate** method should delegate to the [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method of the control container.</span></span>

<span data-ttu-id="c426b-125">O exemplo a seguir mostra como implementar o método [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) .</span><span class="sxs-lookup"><span data-stu-id="c426b-125">The following example shows how to implement the [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method.</span></span>


```C++
STDMETHODIMP CMyAccessibleUIAControl::Navigate(NavigateDirection direction,
     IRawElementProviderFragment **ppRetVal) 
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  
    
    if (direction == NavigateDirection_Parent)  
    {  
        // Query the control container's windowless site 
        // for the parent.
         if (SUCCEEDED(m_pClientSite->QueryInterface(
                IID_PPV_ARGS(&pWindowlessSite))))  
        {  
            hr =  pWindowlessSite->GetAdjacentFragment(direction, ppRetVal);  
        }  
    }  

    else if (direction == NavigateDirection_FirstChild)  
    {  
        // GetFragmentForChild is an application-defined function that 
        // retrieves the first or last child fragment.
        hr =  GetFragmentForChild(FIRST, ppRetVal);  
    }  

    else if (direction == NavigateDirection_LastChild)  
    {  
        hr = GetFragmentForChild(LAST, ppRetVal);  
    }  

    SafeRelease(&pWindowlessSite);
    return S_OK;   
}
```



### <a name="step-4-implement-the-irawelementproviderfragmentgetruntimeid-method"></a><span data-ttu-id="c426b-126">Etapa 4: implementar o método IRawElementProviderFragment:: GetRuntimeId.</span><span class="sxs-lookup"><span data-stu-id="c426b-126">Step 4: Implement the IRawElementProviderFragment::GetRuntimeId method.</span></span>

<span data-ttu-id="c426b-127">Quando o controle sem janela recebe uma chamada para o método [**IRawElementProviderFragment:: GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) , o controle deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c426b-127">When your windowless control receives a call to its [**IRawElementProviderFragment::GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) method, the control must do the following:</span></span>

1.  <span data-ttu-id="c426b-128">Recupere um prefixo de ID de tempo de execução chamando o método [**IRawElementProviderWindowlessSite:: GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) do site de controle.</span><span class="sxs-lookup"><span data-stu-id="c426b-128">Retrieve a runtime ID prefix by calling the control site's [**IRawElementProviderWindowlessSite::GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method.</span></span>
2.  <span data-ttu-id="c426b-129">Crie uma ID de tempo de execução exclusiva para o controle acrescentando um inteiro ao prefixo de ID de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="c426b-129">Create a unique runtime ID for the control by appending an integer to the runtime ID prefix.</span></span>
3.  <span data-ttu-id="c426b-130">Retornar a ID de tempo de execução para o chamador.</span><span class="sxs-lookup"><span data-stu-id="c426b-130">Return the runtime ID to the caller.</span></span>

<span data-ttu-id="c426b-131">O exemplo a seguir mostra como implementar o método [**GetRuntimeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) .</span><span class="sxs-lookup"><span data-stu-id="c426b-131">The following example shows how to implement the [**GetRuntimeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method.</span></span>


```C++
STDMETHODIMP CMyAccessibleUIAControl::GetRuntimeId(SAFEARRAY **ppRetVal)  
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        // Create a safe array to hold runtime ID.
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 1, 3);  
        if (psa == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Retrieve the runtime ID prefix from the control container. The prefix
        // consists of UiaAppendRuntimeId followed by the windowless site ID.
        if (SUCCEEDED(hr))
        {    
            hr = pWindowlessSite->GetRuntimeIdPrefix(&psa);  
        } 

        if (SUCCEEDED(hr))
        {
        // Append this fragment's ID to the retrieved runtime ID prefix.
            long i = 2;
            hr = SafeArrayPutElement(psa, &i, (void*)&m_Id);        
        }

        if (SUCCEEDED(hr))
        {
            *ppRetVal = psa;  
        }
    }

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



## <a name="related-topics"></a><span data-ttu-id="c426b-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c426b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c426b-133">Usar MSAA para tornar um controle ActiveX sem janela acessível</span><span class="sxs-lookup"><span data-stu-id="c426b-133">Use MSAA to Make a Windowless ActiveX Control Accessible</span></span>](use-msaa-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[<span data-ttu-id="c426b-134">Acessibilidade de controle ActiveX sem janela</span><span class="sxs-lookup"><span data-stu-id="c426b-134">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 