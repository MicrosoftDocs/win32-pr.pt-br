---
title: Expondo controles com base em controles do sistema
description: Expondo controles com base em controles do sistema
ms.assetid: 9291b79e-3ed0-4f3c-a610-38215d84f5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2fe31eae8c2283c020de93b0c1f3350bd0f417
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366476"
---
# <a name="exposing-controls-based-on-system-controls"></a><span data-ttu-id="6bf44-103">Expondo controles com base em controles do sistema</span><span class="sxs-lookup"><span data-stu-id="6bf44-103">Exposing Controls Based on System Controls</span></span>

<span data-ttu-id="6bf44-104">Você deve considerar o uso de alguma forma de anotação dinâmica — direta, mapa de valor ou servidor — antes de tentar a técnica descrita nesta seção.</span><span class="sxs-lookup"><span data-stu-id="6bf44-104">You should consider using some form of Dynamic Annotation—Direct, Value Map, or Server—before attempting the technique described in this section.</span></span> <span data-ttu-id="6bf44-105">Para obter mais informações, consulte [API de anotação dinâmica](dynamic-annotation-api.md).</span><span class="sxs-lookup"><span data-stu-id="6bf44-105">For more information, see [Dynamic Annotation API](dynamic-annotation-api.md).</span></span>

<span data-ttu-id="6bf44-106">Na maioria dos casos, a Microsoft Acessibilidade Ativa expõe informações sobre os controles de subclasse ou de subclasse.</span><span class="sxs-lookup"><span data-stu-id="6bf44-106">In most cases, Microsoft Active Accessibility exposes information about superclassed or subclassed controls.</span></span> <span data-ttu-id="6bf44-107">A superclasse e a subclasse permitem que um desenvolvedor de aplicativo crie um controle personalizado com a funcionalidade básica de um controle do sistema e inclua aprimoramentos fornecidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6bf44-107">Superclassing and subclassing allow an application developer to create a custom control with the basic functionality of a system control and include enhancements provided by the application.</span></span> <span data-ttu-id="6bf44-108">Um controle superclasse tem um nome de classe de janela diferente do controle do sistema no qual ele se baseia.</span><span class="sxs-lookup"><span data-stu-id="6bf44-108">A superclassed control has a different window class name than the system control on which it is based.</span></span> <span data-ttu-id="6bf44-109">Um controle de subclasse tem o mesmo nome de classe de janela.</span><span class="sxs-lookup"><span data-stu-id="6bf44-109">A subclassed control has the same window class name.</span></span> <span data-ttu-id="6bf44-110">Para obter mais informações sobre a superclasse e a subclasse, consulte a documentação do SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="6bf44-110">For more information about superclassing and subclassing, see the Windows Software Development Kit (SDK) documentation.</span></span>

<span data-ttu-id="6bf44-111">Como a Microsoft Acessibilidade Ativa expõe informações sobre controles fornecidos pelo sistema, a Microsoft Acessibilidade Ativa expõe o controle modificado, a menos que um controle de subclasse ou de subclasse seja significativamente diferente do controle base.</span><span class="sxs-lookup"><span data-stu-id="6bf44-111">Because Microsoft Active Accessibility exposes information about system-provided controls, Microsoft Active Accessibility exposes the modified control unless a superclassed or subclassed control is significantly different from the base control.</span></span> <span data-ttu-id="6bf44-112">Para determinar se o controle modificado está acessível, os desenvolvedores de aplicativos devem usar utilitários como [inspecionar](inspect-objects.md) e [Inspetor de eventos acessível](accessible-event-watcher.md) para comparar o comportamento do controle modificado com o controle de base.</span><span class="sxs-lookup"><span data-stu-id="6bf44-112">To determine if the modified control is accessible, application developers should use utilities such as [Inspect](inspect-objects.md) and [Accessible Event Watcher](accessible-event-watcher.md) to compare the behavior of the modified control with the base control.</span></span>

<span data-ttu-id="6bf44-113">Se, depois de usar esses utilitários, você determinar que o controle modificado não está acessível, você deve tratar o controle como qualquer outro controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="6bf44-113">If after using these utilities you determine that the modified control is not accessible, you must treat the control as any other custom control.</span></span> <span data-ttu-id="6bf44-114">O controle deve disparar eventos, e o procedimento de janela do aplicativo deve responder à mensagem do [**WM \_ GetObject**](wm-getobject.md)fornecendo uma interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que os aplicativos cliente usam para obter informações sobre o controle.</span><span class="sxs-lookup"><span data-stu-id="6bf44-114">The control must trigger events, and the application's window procedure must respond to the [**WM\_GETOBJECT**](wm-getobject.md)message by supplying an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface that client applications use to obtain information about the control.</span></span>

## <a name="createstdaccessibleproxy-and-createstdaccessibleobject"></a><span data-ttu-id="6bf44-115">CreateStdAccessibleProxy e CreateStdAccessibleObject</span><span class="sxs-lookup"><span data-stu-id="6bf44-115">CreateStdAccessibleProxy and CreateStdAccessibleObject</span></span>

<span data-ttu-id="6bf44-116">Se todas ou a maior parte das propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do controle modificado forem as mesmas do controle base, use [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) ou [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) para simplificar a implementação da interface **IAccessible** do controle.</span><span class="sxs-lookup"><span data-stu-id="6bf44-116">If all or most of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties for the modified control are the same as the base control, use [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) or [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) to simplify the implementation of the control's **IAccessible** interface.</span></span>

> [!Note]  
> <span data-ttu-id="6bf44-117">Ao superclasse ou subclasse de um controle acessível, lembre-se de que o objeto recuperado pela função [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) pode implementar mais do que apenas a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="6bf44-117">When superclassing or subclassing an accessible control, be aware that the object retrieved by the [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) function may implement more than just the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="6bf44-118">Ele pode incluir outras interfaces, como [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant).</span><span class="sxs-lookup"><span data-stu-id="6bf44-118">It may include other interfaces such as [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant).</span></span> <span data-ttu-id="6bf44-119">Talvez seja necessário encapsular essas interfaces adicionais para manter o suporte de acessibilidade fornecido pelo implementação original do controle.</span><span class="sxs-lookup"><span data-stu-id="6bf44-119">You might need to wrap these additional interfaces to retain the accessibility support provided by the original implemenation of the control.</span></span>

 

<span data-ttu-id="6bf44-120">As funções [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) e [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) recuperam um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para o controle do sistema especificado.</span><span class="sxs-lookup"><span data-stu-id="6bf44-120">The [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) and [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) functions retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer for the specified system control.</span></span> <span data-ttu-id="6bf44-121">A diferença nessas funções é que **CreateStdAccessibleObject** usa o nome de classe da janela obtido de seu parâmetro *HWND* , enquanto **CreateStdAccessibleProxy** usa o nome de classe da janela especificado em seu parâmetro *szClassName* .</span><span class="sxs-lookup"><span data-stu-id="6bf44-121">The difference in these functions is that **CreateStdAccessibleObject** uses the window class name obtained from its *hwnd* parameter whereas **CreateStdAccessibleProxy** uses the window class name specified in its *szClassName* parameter.</span></span> <span data-ttu-id="6bf44-122">Portanto, se você decidir usar essas funções, use **CreateStdAccessibleProxy** para expor informações sobre controles superclasses e qualquer função com controles de subclasse.</span><span class="sxs-lookup"><span data-stu-id="6bf44-122">Therefore, if you decide to use these functions, use **CreateStdAccessibleProxy** to expose information about superclassed controls, and either function with subclassed controls.</span></span>

<span data-ttu-id="6bf44-123">Depois de obter um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para o controle do sistema, use o ponteiro em sua implementação da interface **IAccessible** para o controle modificado.</span><span class="sxs-lookup"><span data-stu-id="6bf44-123">After obtaining an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer to the system control, use the pointer in your implementation of the **IAccessible** interface for the modified control.</span></span> <span data-ttu-id="6bf44-124">Se uma propriedade ou método para o controle modificado for o mesmo que o controle base, use o ponteiro **IAccessible** para retornar as informações fornecidas pelo controle de base.</span><span class="sxs-lookup"><span data-stu-id="6bf44-124">If a property or method for the modified control is the same as the base control, use the **IAccessible** pointer to return the information provided by the base control.</span></span> <span data-ttu-id="6bf44-125">Se uma propriedade para o controle modificado for diferente do controle base, substitua a propriedade do controle base.</span><span class="sxs-lookup"><span data-stu-id="6bf44-125">If a property for the modified control is different from the base control, override the base control's property.</span></span>

<span data-ttu-id="6bf44-126">No exemplo a seguir, **CAccCustomButton** é a classe definida pelo aplicativo derivada de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="6bf44-126">In the following example, **CAccCustomButton** is the application-defined class derived from [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="6bf44-127">A variável de membro **m \_ pAccDefaultButton** é um ponteiro para uma interface **IAccessible** que foi recuperada de [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) durante o procedimento de inicialização do controle.</span><span class="sxs-lookup"><span data-stu-id="6bf44-127">The member variable **m\_pAccDefaultButton** is a pointer to an **IAccessible** interface that was retrieved from [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) during the initialization procedure for the control.</span></span> <span data-ttu-id="6bf44-128">Neste exemplo, a propriedade **role** do controle personalizado é igual à propriedade **role** do controle do sistema, portanto, a propriedade **role** do controle base é retornada.</span><span class="sxs-lookup"><span data-stu-id="6bf44-128">In this example, the **Role** property for the custom control is the same as the **Role** property of the system control, so the **Role** property of the base control is returned.</span></span> <span data-ttu-id="6bf44-129">No entanto, a propriedade **Description** é diferente da do controle base, portanto, essa propriedade é substituída.</span><span class="sxs-lookup"><span data-stu-id="6bf44-129">However, the **Description** property is different from that of the base control, so this property is overridden.</span></span>


```C++
HRESULT CAccCustomButton::Initialize( HWND hWnd, HINSTANCE hInst )
{
.
.
.
    hr = CreateStdAccessibleObject( m_hWnd, 
                                    OBJID_CLIENT, 
                                    IID_IAccessible, 
                                    (void **) &m__pAccDefaultButton );
.
.
.
}

STDMETHODIMP CAccCustomButton::get_accRole( VARIANT varID )
{
    return m_pAccDefaultButton->get_accRole(varID);
}


STDMETHODIMP CAccCustomButton::get_accDescription( VARIANT varChild,
                                                   BSTR* pszDesc )
{
    TCHAR   szString[256];
    OLECHAR wszString[256];

    LoadString( m_hInst, ID_DESCRIPTION, szString, 256 );
    MultiByteToWideChar( CP_ACP, 0, szString, -1, wszString, 256 );
   *pszDesc = SysAllocString( wszString );
   if ( !pszDesc )
       return S_OK;
   else
       return E_OUTOFMEMORY;
}
```



<span data-ttu-id="6bf44-130">Para obter mais informações sobre as propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e métodos de controles do sistema, consulte [o apêndice A: referência de elementos da interface do usuário com suporte](appendix-a--supported-user-interface-elements-reference.md).</span><span class="sxs-lookup"><span data-stu-id="6bf44-130">For more information about the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods of system controls, see [Appendix A: Supported User Interface Elements Reference](appendix-a--supported-user-interface-elements-reference.md).</span></span>

 

 