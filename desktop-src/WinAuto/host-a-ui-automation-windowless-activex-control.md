---
title: Hospedar um controle ActiveX sem janela de automação da interface do usuário
description: Saiba como criar um contêiner de controle que pode hospedar controles Microsoft ActiveX sem janelas que implementam a automação da interface do usuário da Microsoft.
ms.assetid: A0F82968-F434-4F5E-8052-CF7CE65DB120
keywords:
- Automação da interface do usuário, controle ActiveX sem janela
- Controle ActiveX sem janela, automação da interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77026d923ea6f0d2536cbd6a94966ec858443258
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294111"
---
# <a name="host-a-ui-automation-windowless-activex-control"></a><span data-ttu-id="416ae-105">Hospedar um controle ActiveX sem janela de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="416ae-105">Host a UI Automation Windowless ActiveX Control</span></span>

<span data-ttu-id="416ae-106">Saiba como criar um contêiner de controle que pode hospedar controles Microsoft ActiveX sem janelas que implementam a automação da interface do usuário da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="416ae-106">Learn how to create a control container that can host windowless Microsoft ActiveX controls that implement Microsoft UI Automation.</span></span> <span data-ttu-id="416ae-107">Usando as etapas descritas aqui, você pode garantir que qualquer controle sem janela da automação da interface do usuário hospedado em seu contêiner de controle seja acessível a aplicativos cliente de tecnologia assistencial (AT).</span><span class="sxs-lookup"><span data-stu-id="416ae-107">By using the steps described here, you can ensure that any UI Automation windowless controls that are hosted in your control container are accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="416ae-108">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="416ae-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="416ae-109">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="416ae-109">Technologies</span></span>

-   [<span data-ttu-id="416ae-110">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="416ae-110">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="416ae-111">Automação da Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="416ae-111">UI Automation</span></span>](entry-uiauto-win32.md)

### <a name="prerequisites"></a><span data-ttu-id="416ae-112">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="416ae-112">Prerequisites</span></span>

-   <span data-ttu-id="416ae-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="416ae-113">C/C++</span></span>
-   <span data-ttu-id="416ae-114">Programação do COM (Microsoft Win32 e Component Object Model)</span><span class="sxs-lookup"><span data-stu-id="416ae-114">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="416ae-115">Controles ActiveX sem janela</span><span class="sxs-lookup"><span data-stu-id="416ae-115">Windowless ActiveX controls</span></span>
-   <span data-ttu-id="416ae-116">Provedores de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="416ae-116">UI Automation providers</span></span>

## <a name="instructions"></a><span data-ttu-id="416ae-117">Instruções</span><span class="sxs-lookup"><span data-stu-id="416ae-117">Instructions</span></span>

### <a name="step-1-provide-the-irawelementprovidersimple-interface-on-behalf-of-the-windowless-control"></a><span data-ttu-id="416ae-118">Etapa 1: forneça a interface IRawElementProviderSimple em nome do controle sem janela.</span><span class="sxs-lookup"><span data-stu-id="416ae-118">Step 1: Provide the IRawElementProviderSimple interface on behalf of the windowless control.</span></span>

<span data-ttu-id="416ae-119">Sempre que o sistema precisar do ponteiro [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) para a raiz de um controle sem janela, o sistema consultará o contêiner de controle.</span><span class="sxs-lookup"><span data-stu-id="416ae-119">Whenever the system needs the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pointer for the root of a windowless control, the system queries the control container.</span></span> <span data-ttu-id="416ae-120">Para recuperar o ponteiro, o contêiner chama a implementação de controle sem janela do método [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="416ae-120">To retrieve the pointer, the container calls the windowless control's implementation of the [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method.</span></span>

<span data-ttu-id="416ae-121">Se o contêiner de controle tiver uma implementação de automação de interface do usuário, ele poderá retornar o ponteiro [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) do controle sem janela para o sistema.</span><span class="sxs-lookup"><span data-stu-id="416ae-121">If the control container has a UI Automation implementation, it can return the windowless control's [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pointer to the system.</span></span>

<span data-ttu-id="416ae-122">Se o contêiner de controle tiver uma implementação de Acessibilidade Ativa da Microsoft, chame a função [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) para obter um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que represente o controle e, em seguida, retorne o ponteiro da interface **IAccessible** para o sistema.</span><span class="sxs-lookup"><span data-stu-id="416ae-122">If the control container has a Microsoft Active Accessibility implementation, call the [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) function to obtain an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer that represents the control, and then return the **IAccessible** interface pointer to the system.</span></span>

### <a name="step-2-implement-the-irawelementproviderwindowlesssite-interface"></a><span data-ttu-id="416ae-123">Etapa 2: implementar a interface IRawElementProviderWindowlessSite.</span><span class="sxs-lookup"><span data-stu-id="416ae-123">Step 2: Implement the IRawElementProviderWindowlessSite interface.</span></span>

<span data-ttu-id="416ae-124">Um contêiner de controle implementa a interface [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) habilita um controle sem janela baseado na automação da interface do usuário para comunicar suas informações de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="416ae-124">A control container implements the [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) interface enable a windowless control that is based on UI Automation to communicate its accessibility information.</span></span>

1.  <span data-ttu-id="416ae-125">Implemente [**IRawElementProviderWindowlessSite:: GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix).</span><span class="sxs-lookup"><span data-stu-id="416ae-125">Implement [**IRawElementProviderWindowlessSite::GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix).</span></span>

    <span data-ttu-id="416ae-126">Um fragmento de controle sem janela deve criar uma ID de tempo de execução exclusiva para si mesmo.</span><span class="sxs-lookup"><span data-stu-id="416ae-126">A windowless control fragment must create a unique runtime ID for itself.</span></span> <span data-ttu-id="416ae-127">Para criar sua ID de tempo de execução, um fragmento de controle sem janela recupera um valor de prefixo chamando o método [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) do site de controle e, em seguida, acrescenta ao prefixo um valor inteiro que é exclusivo em relação a todos os outros fragmentos no controle sem janela.</span><span class="sxs-lookup"><span data-stu-id="416ae-127">To create its runtime ID, a windowless control fragment retrieves a prefix value by calling the control site's [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method, and then appends to the prefix an integer value that is unique relative to all other fragments in the windowless control.</span></span>

    <span data-ttu-id="416ae-128">O site de controle para um controle sem janela deve implementar o método [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) formando um **SafeArray** que contém a constante **UiaAppendRuntimeId**, seguido por um valor inteiro que é exclusivo para o site.</span><span class="sxs-lookup"><span data-stu-id="416ae-128">The control site for a windowless control should implement the [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) method by forming a **SAFEARRAY** that contains the constant **UiaAppendRuntimeId**, followed by an integer value that is unique to the site.</span></span>

    <span data-ttu-id="416ae-129">Este exemplo mostra como retornar um prefixo de ID de tempo de execução para um controle sem janela.</span><span class="sxs-lookup"><span data-stu-id="416ae-129">This example shows how to return a runtime ID prefix for a windowless control.</span></span>

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetRuntimeIdPrefix(   
         SAFEARRAY **ppsaPrefix)   
    {   
        if (ppsaPrefix == NULL) 
        {
            return E_INVALIDARG;
        }

        // m_siteIndex is the index of the windowless control's
        // site. It is defined by the control container.
        int rId[] = { UiaAppendRuntimeId, m_siteIndex };
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 0, 2);  
        if (psa == NULL)
        {
            return E_OUTOFMEMORY;
        }

        for (LONG i = 0; i < 2; i++)
        {
            SafeArrayPutElement(psa, &i, (void*)&(rId[i]));
        }

        *ppsaPrefix = psa;  
        return S_OK;  
    }  
    ```

    

2.  <span data-ttu-id="416ae-130">Implemente o método [**IRawElementProviderWindowlessSite:: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) .</span><span class="sxs-lookup"><span data-stu-id="416ae-130">Implement the [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method.</span></span>

    <span data-ttu-id="416ae-131">Um controle que implementa a automação da interface do usuário deve retornar um ponteiro para o provedor de fragmento pai do controle.</span><span class="sxs-lookup"><span data-stu-id="416ae-131">A control that implements UI Automation must return a pointer to the control's parent fragment provider.</span></span>

    <span data-ttu-id="416ae-132">Para retornar o pai do fragmento, um objeto que implementa a interface [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) deve ser capaz de implementar o método [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) .</span><span class="sxs-lookup"><span data-stu-id="416ae-132">To return the parent of the fragment, an object that implements the [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) interface must be able to implement the [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method.</span></span> <span data-ttu-id="416ae-133">A implementação de **Navigate** é difícil para um controle sem janela porque o controle pode não conseguir determinar seu local na árvore acessível do objeto pai.</span><span class="sxs-lookup"><span data-stu-id="416ae-133">Implementing **Navigate** is difficult for a windowless control because the control might be unable to determine its location in the accessible tree of the parent object.</span></span> <span data-ttu-id="416ae-134">O método [**IRawElementProviderWindowlessSite:: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) permite que o controle sem janela consulte seu site para o fragmento adjacente e, em seguida, retorne esse fragmento para o cliente que chamou **Navigate**.</span><span class="sxs-lookup"><span data-stu-id="416ae-134">The [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) method enables the windowless control to query its site for the adjacent fragment, and then return that fragment to the client that called **Navigate**.</span></span>

    <span data-ttu-id="416ae-135">Este exemplo mostra como um contêiner de controle recupera o fragmento pai de um controle sem janela.</span><span class="sxs-lookup"><span data-stu-id="416ae-135">This example shows how a control container retrieves the parent fragment of a windowless control.</span></span>

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetAdjacentFragment(
            enum NavigateDirection direction, IRawElementProviderFragment **ppFragment)   
    {
        if (ppFragment == NULL)
        {
            return E_INVALIDARG;
        }
        
        *ppFragment = NULL;
        HRESULT hr = S_OK;

        switch (direction)
        {
            case NavigateDirection_Parent:
                {  
                    IRawElementProviderSimple *pSimple = NULL;

                    // Call an application-defined function to retrieve the
                    // parent provider interface.
                    hr = GetParentProvider(&pSimple);  
                    if (SUCCEEDED(hr))  
                    {  
                        // Get the parent's IRawElementProviderFragment interface.
                        hr = pSimple->QueryInterface(IID_PPV_ARGS(ppFragment));  
                        pSimple->Release();  
                    } 
                }  
                break;  
      
            case NavigateDirection_FirstChild:
            case NavigateDirection_LastChild:
                hr = E_INVALIDARG;
                break;

            // Ignore NavigateDirection_NextSibling and NavigateDirection_PreviousSibling
            // because there are no adjacent fragments.
            default:  
                break;  
        }  
      
        return hr;  
    }   
    ```

    

### <a name="step-3-optional-implement-the-irawelementproviderhostingaccessibles-interface"></a><span data-ttu-id="416ae-136">Etapa 3: opcional: implementar a interface IRawElementProviderHostingAccessibles.</span><span class="sxs-lookup"><span data-stu-id="416ae-136">Step 3: Optional: Implement the IRawElementProviderHostingAccessibles interface.</span></span>

<span data-ttu-id="416ae-137">Implemente a interface [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) se o seu contêiner de controle tiver uma implementação de provedor de automação de interface do usuário que seja a raiz de uma árvore de acessibilidade que inclui controles ActiveX sem janela que dão suporte ao Microsoft acessibilidade ativa.</span><span class="sxs-lookup"><span data-stu-id="416ae-137">Implement the [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) interface if your control container has a UI Automation provider implementation that is the root of an accessibility tree that includes windowless ActiveX controls that support Microsoft Active Accessibility.</span></span> <span data-ttu-id="416ae-138">A interface **IRawElementProviderHostingAccessibles** tem um método único, [**GetEmbeddedAccessibles**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles), que recupera os ponteiros da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de todos os controles ActiveX sem janela baseados no Microsoft acessibilidade ativa que são hospedados pelo seu contêiner de controle.</span><span class="sxs-lookup"><span data-stu-id="416ae-138">The **IRawElementProviderHostingAccessibles** interface has a single method, [**GetEmbeddedAccessibles**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles), which retrieves the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointers of all Microsoft Active Accessibility-based windowless ActiveX controls that are hosted by your control container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="416ae-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="416ae-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="416ae-140">Como hospedar um controle ActiveX sem janela do MSAA</span><span class="sxs-lookup"><span data-stu-id="416ae-140">How to Host an MSAA Windowless ActiveX Control</span></span>](host-an-msaa-windowless-activex-control.md)
</dt> <dt>

[<span data-ttu-id="416ae-141">Acessibilidade de controle ActiveX sem janela</span><span class="sxs-lookup"><span data-stu-id="416ae-141">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 