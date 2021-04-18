---
title: Usar MSAA para tornar um controle ActiveX sem janela acessível
description: Descreve como usar o Microsoft Acessibilidade Ativa \ 32; API para garantir que o controle Microsoft ActiveX sem janela esteja acessível para aplicativos cliente de tecnologia assistencial (AT).
ms.assetid: 30F874F9-EA45-4365-8798-FEA011C62DA9
keywords:
- Controle ActiveX, acessibilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3a76aa72fadef502a6a4319284ab34fdd5214d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105813717"
---
# <a name="use-msaa-to-make-a-windowless-activex-control-accessible"></a><span data-ttu-id="11405-104">Usar MSAA para tornar um controle ActiveX sem janela acessível</span><span class="sxs-lookup"><span data-stu-id="11405-104">Use MSAA to make a windowless ActiveX control accessible</span></span>

<span data-ttu-id="11405-105">Descreve como usar a API do Microsoft Acessibilidade Ativa para garantir que o controle Microsoft ActiveX sem janela esteja acessível para aplicativos cliente de tecnologia assistencial (AT).</span><span class="sxs-lookup"><span data-stu-id="11405-105">Describes how to use the Microsoft Active Accessibility API to ensure that your windowless Microsoft ActiveX control is accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="11405-106">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="11405-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="11405-107">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="11405-107">Technologies</span></span>

-   [<span data-ttu-id="11405-108">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="11405-108">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="11405-109">Acessibilidade Ativa da Microsoft</span><span class="sxs-lookup"><span data-stu-id="11405-109">Microsoft Active Accessibility</span></span>](microsoft-active-accessibility.md)

### <a name="prerequisites"></a><span data-ttu-id="11405-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="11405-110">Prerequisites</span></span>

-   <span data-ttu-id="11405-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="11405-111">C/C++</span></span>
-   <span data-ttu-id="11405-112">Programação do COM (Microsoft Win32 e Component Object Model)</span><span class="sxs-lookup"><span data-stu-id="11405-112">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="11405-113">Controles ActiveX sem janela</span><span class="sxs-lookup"><span data-stu-id="11405-113">Windowless ActiveX Controls</span></span>
-   <span data-ttu-id="11405-114">Servidores Microsoft Acessibilidade Ativa</span><span class="sxs-lookup"><span data-stu-id="11405-114">Microsoft Active Accessibility servers</span></span>

## <a name="instructions"></a><span data-ttu-id="11405-115">Instruções</span><span class="sxs-lookup"><span data-stu-id="11405-115">Instructions</span></span>

### <a name="step-1-implement-the-iaccessible-interface"></a><span data-ttu-id="11405-116">Etapa 1: implementar a interface IAccessible.</span><span class="sxs-lookup"><span data-stu-id="11405-116">Step 1: Implement the IAccessible interface.</span></span>

<span data-ttu-id="11405-117">Para tornar o controle ActiveX sem janela acessível, você deve implementar a interface do Microsoft Acessibilidade Ativa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , assim como faria com um controle baseado em janela, exceto conforme descrito nas etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="11405-117">To make your windowless ActiveX control accessible, you must implement the Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface, just as you would for a window-based control, except as described in the following steps.</span></span> <span data-ttu-id="11405-118">Para obter mais informações sobre como implementar o **IAccessible**, consulte o [Guia do desenvolvedor para servidores de acessibilidade ativa](developer-s-guide-for-active-accessibility-servers.md).</span><span class="sxs-lookup"><span data-stu-id="11405-118">For more information about implementing **IAccessible**, see [Developer's Guide for Active Accessibility Servers](developer-s-guide-for-active-accessibility-servers.md).</span></span>

### <a name="step-2-implement-the-iserviceprovider-interface"></a><span data-ttu-id="11405-119">Etapa 2: implementar a interface IServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="11405-119">Step 2: Implement the IServiceProvider interface.</span></span>

<span data-ttu-id="11405-120">Quando um cliente solicita informações de acessibilidade sobre o controle sem janela, o contêiner chama o método [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) do controle para recuperar o ponteiro da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="11405-120">When a client requests accessibility information about your windowless control, the container calls your control's [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method to retrieve the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>

<span data-ttu-id="11405-121">Este exemplo mostra como implementar o método [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="11405-121">This example shows how to implement the [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method.</span></span>


```C++
STDMETHODIMP CMyAccessibleMSAAControl::QueryService(REFGUID guidService, 
        REFIID riid, void **ppvObject)
{      
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL;  

    if (guidService == __uuidof(IAccessible))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-delegate-iaccessibleget_accparent-method-calls-to-the-control-sites-iaccessiblewindowlesssitegetparentaccessible-method"></a><span data-ttu-id="11405-122">Etapa 3: delegar o IAccessible:: get \_ accParent chamadas de método para o método IAccessibleWindowlessSite:: GetParentAccessible do site de controle.</span><span class="sxs-lookup"><span data-stu-id="11405-122">Step 3: Delegate IAccessible::get\_accParent method calls to the control site's IAccessibleWindowlessSite::GetParentAccessible method.</span></span>

<span data-ttu-id="11405-123">Quando um cliente solicita o objeto pai do controle sem janela, o contêiner chama o método [**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) do seu controle.</span><span class="sxs-lookup"><span data-stu-id="11405-123">When a client requests the parent object of your windowless control, the container calls your control's [**IAccessible::get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) method.</span></span> <span data-ttu-id="11405-124">Sua implementação de **Get \_ accParent** deve delegar ao método [**IAccessibleWindowlessSite:: GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) do contêiner.</span><span class="sxs-lookup"><span data-stu-id="11405-124">Your **get\_accParent** implementation should delegate to the [**IAccessibleWindowlessSite::GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) method of the container.</span></span>

<span data-ttu-id="11405-125">Este exemplo mostra como implementar o método [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) .</span><span class="sxs-lookup"><span data-stu-id="11405-125">This example shows how to implement the [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) method.</span></span>


```C++
HRESULT CMyAccessibleMSAAControl::get_accParent(IDispatch **ppdispParent)  
{  
    if (ppdispParent == NULL)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_FALSE;  
    *ppdispParent = NULL;  

    IAccessibleWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        IAccessible *pParentAcc = NULL;
        if (SUCCEEDED(pWindowlessSite->GetParentAccessible(&pParentAcc)))
        {
            hr = pParentAcc->QueryInterface(IID_PPV_ARGS(ppdispParent));  
        }
    }  

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



### <a name="step-4-acquire-a-range-of-object-ids-to-assign-to-the-event-sources-in-your-windowless-control"></a><span data-ttu-id="11405-126">Etapa 4: adquirir um intervalo de IDs de objeto para atribuir às fontes de evento no controle sem janela.</span><span class="sxs-lookup"><span data-stu-id="11405-126">Step 4: Acquire a range of object IDs to assign to the event sources in your windowless control.</span></span>

<span data-ttu-id="11405-127">Assim como os controles baseados em janela, um controle ActiveX sem janela chama a função [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) para notificar os clientes sobre eventos importantes.</span><span class="sxs-lookup"><span data-stu-id="11405-127">Like window-based controls, a windowless ActiveX control calls the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function to notify clients of important events.</span></span> <span data-ttu-id="11405-128">Os parâmetros de função incluem a ID de objeto do item que está gerando o evento.</span><span class="sxs-lookup"><span data-stu-id="11405-128">The function parameters include the object ID of the item that is raising the event.</span></span> <span data-ttu-id="11405-129">O controle sem janela deve atribuir IDs de objeto usando um valor de um intervalo adquirido chamando o método [**IAccessibleWindowlessSite:: AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) do site de controle.</span><span class="sxs-lookup"><span data-stu-id="11405-129">Your windowless control must assign object IDs by using a value from a range acquired by calling the control site’s [**IAccessibleWindowlessSite::AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) method.</span></span>

<span data-ttu-id="11405-130">Este exemplo mostra como adquirir um intervalo de valores de ID de objeto do contêiner de controle.</span><span class="sxs-lookup"><span data-stu-id="11405-130">This example shows how to acquire a range of object ID values from the control container.</span></span>


```C++
IAccessibleWindowlessSite *pWindowlessSite = NULL;

if (SUCCEEDED(m_pClientSite->QueryInterface(
        IID_PPV_ARGS(&pWindowlessSite))))  
{  
    if (FAILED(pWindowlessSite->AcquireObjectIdRange(100, this, 
            &m_idObjectBase)))  
    {  
        m_idObjectBase = -1;  
    } 
}

SafeRelease(&pWindowlessSite);
```



### <a name="step-5-implement-the-iaccessiblehandler-interface"></a><span data-ttu-id="11405-131">Etapa 5: implementar a interface IAccessibleHandler.</span><span class="sxs-lookup"><span data-stu-id="11405-131">Step 5: Implement the IAccessibleHandler interface.</span></span>

<span data-ttu-id="11405-132">Quando um controle sem janela chama a função [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) , o controle Especifica a ID de objeto do item da interface do usuário que está gerando o evento e especifica o contêiner de controle como a janela que responderá às mensagens do [**WM \_ GetObject**](wm-getobject.md) em nome do controle.</span><span class="sxs-lookup"><span data-stu-id="11405-132">When a windowless control calls the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function, the control specifies the object ID of the UI item that is raising the event, and specifies the control container as the window that will respond to [**WM\_GETOBJECT**](wm-getobject.md) messages on behalf of the control.</span></span>

<span data-ttu-id="11405-133">Se um aplicativo cliente responder ao evento, o contêiner de controle receberá uma mensagem do [**WM \_ GetObject**](wm-getobject.md) que inclui a ID de objeto do item da interface do usuário que gerou o evento.</span><span class="sxs-lookup"><span data-stu-id="11405-133">If a client application responds to the event, the control container receives a [**WM\_GETOBJECT**](wm-getobject.md) message that includes the object ID of the UI item that raised the event.</span></span> <span data-ttu-id="11405-134">O contêiner de controle responde pesquisando o controle sem janela que "possui" a ID de objeto e, em seguida, chamando o método [**IAccessibleHandler:: AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) do controle.</span><span class="sxs-lookup"><span data-stu-id="11405-134">The control container responds by looking up the windowless control that "owns" the object ID, and then calling that control's [**IAccessibleHandler::AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) method.</span></span> <span data-ttu-id="11405-135">O método **AccessibleObjectFromID** retorna o ponteiro da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para o item da interface do usuário e o contêiner de controle encaminha o ponteiro para o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="11405-135">The **AccessibleObjectFromID** method returns the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer for the UI item, and the control container forwards the pointer to the client application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11405-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="11405-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11405-137">Usar a automação da interface do usuário para tornar um controle ActiveX sem janela acessível</span><span class="sxs-lookup"><span data-stu-id="11405-137">Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[<span data-ttu-id="11405-138">Acessibilidade de controle ActiveX sem janela</span><span class="sxs-lookup"><span data-stu-id="11405-138">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 