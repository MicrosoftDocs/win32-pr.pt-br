---
title: Mensagem de WM_GETOBJECT (WinUser. h)
description: Enviado pelo Microsoft Acessibilidade Ativa e automação da interface do usuário da Microsoft para obter informações sobre um objeto acessível contido em um aplicativo de servidor.
ms.assetid: 59350aa1-1697-4110-b9a6-f30ee56c4cff
keywords:
- Acessibilidade do Windows WM_GETOBJECT mensagem
topic_type:
- apiref
api_name:
- WM_GETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcac5c7f6dd8203c32b9f6f3c4eb59144cc3f8ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086484"
---
# <a name="wm_getobject-message"></a><span data-ttu-id="f1d3b-104">Mensagem do WM \_ GETobject</span><span class="sxs-lookup"><span data-stu-id="f1d3b-104">WM\_GETOBJECT message</span></span>

<span data-ttu-id="f1d3b-105">Enviado pelo Microsoft Acessibilidade Ativa e automação da interface do usuário da Microsoft para obter informações sobre um objeto acessível contido em um aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="f1d3b-105">Sent by both Microsoft Active Accessibility and Microsoft UI Automation to obtain information about an accessible object contained in a server application.</span></span>

<span data-ttu-id="f1d3b-106">Os aplicativos nunca enviam essa mensagem diretamente.</span><span class="sxs-lookup"><span data-stu-id="f1d3b-106">Applications never send this message directly.</span></span> <span data-ttu-id="f1d3b-107">O Microsoft Acessibilidade Ativa envia essa mensagem em resposta a chamadas para [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)ou [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span><span class="sxs-lookup"><span data-stu-id="f1d3b-107">Microsoft Active Accessibility sends this message in response to calls to [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), or [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span></span> <span data-ttu-id="f1d3b-108">No entanto, os aplicativos de servidor lidam com essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="f1d3b-108">However, server applications handle this message.</span></span> <span data-ttu-id="f1d3b-109">A automação da interface do usuário envia essa mensagem em resposta às chamadas para [**IUIAutomation:: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)e [**getconcentrouelement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)e ao manipular eventos para os quais um cliente se registrou.</span><span class="sxs-lookup"><span data-stu-id="f1d3b-109">UI Automation sends this message in response to calls to [**IUIAutomation::ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint), and [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), and when handling events for which a client has registered.</span></span>


```C++
dwFlags = (WPARAM)(DWORD) wParam;
dwObjId = (LPARAM)(DWORD) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f1d3b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1d3b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1d3b-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="f1d3b-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="f1d3b-112">Fornece informações adicionais sobre a mensagem e é usada somente pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="f1d3b-112">Provides additional information about the message and is used only by the system.</span></span> <span data-ttu-id="f1d3b-113">Os servidores passam *dwFlags* como o parâmetro *wParam* na chamada para [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) ao manipular a mensagem.</span><span class="sxs-lookup"><span data-stu-id="f1d3b-113">Servers pass *dwFlags* as the *wParam* parameter in the call to [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) when handling the message.</span></span>

</dd> <dt>

<span data-ttu-id="f1d3b-114">*dwObjId*</span><span class="sxs-lookup"><span data-stu-id="f1d3b-114">*dwObjId*</span></span> 
</dt> <dd>

<span data-ttu-id="f1d3b-115">Identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="f1d3b-115">Object identifier.</span></span> <span data-ttu-id="f1d3b-116">Esse valor é uma das constantes de [identificador de objeto](object-identifiers.md) ou um identificador de objeto personalizado.</span><span class="sxs-lookup"><span data-stu-id="f1d3b-116">This value is one of the [object identifier](object-identifiers.md) constants or a custom object identifier.</span></span> <span data-ttu-id="f1d3b-117">Um aplicativo de servidor deve verificar esse valor para identificar o tipo de informações que estão sendo solicitadas.</span><span class="sxs-lookup"><span data-stu-id="f1d3b-117">A server application must check this value to identify the type of information being requested.</span></span> <span data-ttu-id="f1d3b-118">Antes de comparar esse valor com os \_ valores de OBJID, o servidor deve convertê-lo em **DWORD**; caso contrário, no Windows de 64 bits, a extensão de sinal do *lParam* pode interferir na comparação.</span><span class="sxs-lookup"><span data-stu-id="f1d3b-118">Before comparing this value against the OBJID\_ values, the server must cast it to **DWORD**; otherwise, on 64-bit Windows, the sign extension of the *lParam* can interfere with the comparison.</span></span>

-   <span data-ttu-id="f1d3b-119">Se *dwObjId* for um dos valores de OBJID \_ como [**OBJID \_ Client**](object-identifiers.md), a solicitação será para um objeto Microsoft acessibilidade ativa que implementa o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="f1d3b-119">If *dwObjId* is one of the OBJID\_ values such as [**OBJID\_CLIENT**](object-identifiers.md), the request is for a Microsoft Active Accessibility object that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span>
-   <span data-ttu-id="f1d3b-120">Se *dwObjId* for igual a **UiaRootObjectId**, a solicitação será para um provedor de automação de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f1d3b-120">If *dwObjId* is equal to **UiaRootObjectId**, the request is for a UI Automation provider.</span></span> <span data-ttu-id="f1d3b-121">Se o servidor estiver implementando a automação da interface do usuário, ele deverá retornar um provedor usando a função [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .</span><span class="sxs-lookup"><span data-stu-id="f1d3b-121">If the server is implementing UI Automation, it should return a provider using the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>
-   <span data-ttu-id="f1d3b-122">Se *dwObjId* for [**OBJID \_ NATIVEOM**](object-identifiers.md), a solicitação será para o modelo de objeto subjacente do controle.</span><span class="sxs-lookup"><span data-stu-id="f1d3b-122">If *dwObjId* is [**OBJID\_NATIVEOM**](object-identifiers.md), the request is for the control's underlying object model.</span></span> <span data-ttu-id="f1d3b-123">Se o controle der suporte a essa solicitação, ele deverá retornar uma interface COM apropriada chamando a função [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .</span><span class="sxs-lookup"><span data-stu-id="f1d3b-123">If the control supports this request, it should return an appropriate COM interface by calling the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>
-   <span data-ttu-id="f1d3b-124">Se *dwObjId* for [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md), a solicitação será para o controle se identificar como um controle padrão do Windows ou um controle comum implementado pela ComCtrl.dll (biblioteca de controle comum).</span><span class="sxs-lookup"><span data-stu-id="f1d3b-124">If *dwObjId* is [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md), the request is for the control to identify itself as a standard Windows control or a common control implemented by the common control library (ComCtrl.dll).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1d3b-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1d3b-125">Return value</span></span>

<span data-ttu-id="f1d3b-126">Se a janela ou o controle não precisar responder a essa mensagem, ele deverá passar a mensagem para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ; caso contrário, a janela ou o controle deve retornar um valor que corresponda à solicitação especificada por *dwObjId*:</span><span class="sxs-lookup"><span data-stu-id="f1d3b-126">If the window or control does not need to respond to this message, it should pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function; otherwise, the window or control should return a value that corresponds to the request specified by *dwObjId*:</span></span>

-   <span data-ttu-id="f1d3b-127">Se a janela ou o controle implementar a automação da interface do usuário, a janela ou o controle deverá retornar o valor obtido por uma chamada para a função [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .</span><span class="sxs-lookup"><span data-stu-id="f1d3b-127">If the window or control implements UI Automation, the window or control should return the value obtained by a call to the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>
-   <span data-ttu-id="f1d3b-128">Se *dwObjId* for [**OBJID \_ NATIVEOM**](object-identifiers.md) e a janela expor um modelo de objeto nativo, o Windows deverá retornar o valor obtido por uma chamada para a função [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .</span><span class="sxs-lookup"><span data-stu-id="f1d3b-128">If *dwObjId* is [**OBJID\_NATIVEOM**](object-identifiers.md) and the window exposes a native Object Model, the windows should return the value obtained by a call to the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>
-   <span data-ttu-id="f1d3b-129">Se *dwObjId* for [**OBJID \_ Client**](object-identifiers.md) e a janela implementar [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), a janela deverá retornar o valor obtido por uma chamada para a função [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .</span><span class="sxs-lookup"><span data-stu-id="f1d3b-129">If *dwObjId* is [**OBJID\_CLIENT**](object-identifiers.md) and the window implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), the window should return the value obtained by a call to the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1d3b-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1d3b-130">Remarks</span></span>

<span data-ttu-id="f1d3b-131">Quando um cliente chama [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) ou qualquer uma das outras funções **AccessibleObjectFrom**_X_ que recuperam uma interface para um objeto, o Microsoft acessibilidade ativa envia a mensagem do **WM \_ GetObject** para o procedimento de janela apropriado no aplicativo de servidor apropriado.</span><span class="sxs-lookup"><span data-stu-id="f1d3b-131">When a client calls [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) or any of the other **AccessibleObjectFrom**_X_ functions that retrieve an interface to an object, Microsoft Active Accessibility sends the **WM\_GETOBJECT** message to the appropriate window procedure within the appropriate server application.</span></span> <span data-ttu-id="f1d3b-132">Ao processar o **WM \_ GetObject**, os aplicativos de servidor chamam [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) e usam o valor de retorno dessa função como o valor de retorno para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="f1d3b-132">While processing **WM\_GETOBJECT**, server applications call [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) and use the return value of this function as the return value for the message.</span></span> <span data-ttu-id="f1d3b-133">O Microsoft Acessibilidade Ativa, em conjunto com a biblioteca COM, executa o marshaling apropriado e passa o ponteiro de interface do servidor de volta para o cliente.</span><span class="sxs-lookup"><span data-stu-id="f1d3b-133">Microsoft Active Accessibility, in conjunction with the COM library, performs the appropriate marshaling and passes the interface pointer from the server back to the client.</span></span>

<span data-ttu-id="f1d3b-134">Os servidores não respondem ao **WM \_ GetObject** antes que o objeto seja totalmente inicializado ou depois que ele começa a ser fechado.</span><span class="sxs-lookup"><span data-stu-id="f1d3b-134">Servers do not respond to **WM\_GETOBJECT** before the object is fully initialized or after it begins to close down.</span></span> <span data-ttu-id="f1d3b-135">Quando um aplicativo cria uma nova janela, o sistema envia [**o \_ objeto \_ de evento CREATE**](event-constants.md) para notificar os clientes antes de enviar a mensagem de [ \_ criação do WM](../winmsg/wm-create.md) para o procedimento de janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1d3b-135">When an application creates a new window, the system sends [**EVENT\_OBJECT\_CREATE**](event-constants.md) to notify clients before it sends the [WM\_CREATE](../winmsg/wm-create.md) message to the application's window procedure.</span></span> <span data-ttu-id="f1d3b-136">Como muitos aplicativos usam \_ o WM Create para iniciar o processo de inicialização, os servidores não respondem à mensagem do **WM \_ GetObject** até concluir o processamento da mensagem de **\_ criação do WM** .</span><span class="sxs-lookup"><span data-stu-id="f1d3b-136">Because many applications use WM\_CREATE to start their initialization process, servers do not respond to the **WM\_GETOBJECT** message until finished processing the **WM\_CREATE** message.</span></span>

<span data-ttu-id="f1d3b-137">Um servidor usa o **WM \_ GetObject** para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="f1d3b-137">A server uses **WM\_GETOBJECT** to perform the following tasks:</span></span>

-   [<span data-ttu-id="f1d3b-138">Criar novos objetos acessíveis</span><span class="sxs-lookup"><span data-stu-id="f1d3b-138">Create New Accessible Objects</span></span>](create-new-accessible-objects.md)
-   [<span data-ttu-id="f1d3b-139">Reutilizar ponteiros existentes para objetos</span><span class="sxs-lookup"><span data-stu-id="f1d3b-139">Reuse Existing Pointers to Objects</span></span>](reuse-existing-pointers-to-objects.md)
-   [<span data-ttu-id="f1d3b-140">Criar novas interfaces para o mesmo objeto</span><span class="sxs-lookup"><span data-stu-id="f1d3b-140">Create New Interfaces to the Same Object</span></span>](create-new-interfaces-to-the-same-object.md)

<span data-ttu-id="f1d3b-141">Para clientes, isso significa que eles podem receber ponteiros de interface distintos para o mesmo elemento de interface do usuário, dependendo da ação do servidor.</span><span class="sxs-lookup"><span data-stu-id="f1d3b-141">For clients, this means that they might receive distinct interface pointers for the same user interface element, depending on the server's action.</span></span> <span data-ttu-id="f1d3b-142">Para determinar se dois ponteiros de interface apontam para o mesmo elemento de interface do usuário, os clientes comparam as propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do objeto.</span><span class="sxs-lookup"><span data-stu-id="f1d3b-142">To determine if two interface pointers point to the same user interface element, clients compare [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties of the object.</span></span> <span data-ttu-id="f1d3b-143">A comparação de ponteiros não funciona.</span><span class="sxs-lookup"><span data-stu-id="f1d3b-143">Comparing pointers does not work.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1d3b-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1d3b-144">Requirements</span></span>



| <span data-ttu-id="f1d3b-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1d3b-145">Requirement</span></span> | <span data-ttu-id="f1d3b-146">Valor</span><span class="sxs-lookup"><span data-stu-id="f1d3b-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1d3b-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1d3b-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f1d3b-148">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f1d3b-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f1d3b-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1d3b-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f1d3b-150">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f1d3b-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f1d3b-151">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="f1d3b-151">Redistributable</span></span><br/>          | <span data-ttu-id="f1d3b-152">Acessibilidade Ativa 1,3 RDK no Windows NT 4,0 com SP6 e posterior e Windows 95</span><span class="sxs-lookup"><span data-stu-id="f1d3b-152">Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95</span></span><br/>              |
| <span data-ttu-id="f1d3b-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1d3b-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1d3b-154"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d3b-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1d3b-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1d3b-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1d3b-156">Como tratar o WM \_ GETobject</span><span class="sxs-lookup"><span data-stu-id="f1d3b-156">How to Handle WM\_GETOBJECT</span></span>](how-to-handle-wm-getobject.md)
</dt> <dt>

[<span data-ttu-id="f1d3b-157">Como o WM \_ GetObject funciona</span><span class="sxs-lookup"><span data-stu-id="f1d3b-157">How WM\_GETOBJECT Works</span></span>](how-wm-getobject-works.md)
</dt> <dt>

[<span data-ttu-id="f1d3b-158">**LresultFromObject**</span><span class="sxs-lookup"><span data-stu-id="f1d3b-158">**LresultFromObject**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
</dt> </dl>

 

