---
title: Usando anotação direta
description: Usando anotação direta
ms.assetid: d9d78e74-dcab-4974-945f-e8c5d42c04b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f0bdea5af896329b6836d21ca1dcee25bc2739
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294235"
---
# <a name="using-direct-annotation"></a><span data-ttu-id="160e4-103">Usando anotação direta</span><span class="sxs-lookup"><span data-stu-id="160e4-103">Using Direct Annotation</span></span>

<span data-ttu-id="160e4-104">**Para usar a anotação direta para substituir o valor de uma propriedade**</span><span class="sxs-lookup"><span data-stu-id="160e4-104">**To use direct annotation to override the value of a property**</span></span>

1.  <span data-ttu-id="160e4-105">Use a função [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ou [CoCreateInstanceEx](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) para criar o objeto [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="160e4-105">Use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) or [CoCreateInstanceEx](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) function to create the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) object.</span></span>
2.  <span data-ttu-id="160e4-106">Chame [**IAccPropServices:: SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop), passando o **HWND**, a ID do objeto, a ID filho, a propriedade a ser substituída e uma [variante](/windows/win32/api/oaidl/ns-oaidl-variant) que contém o novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="160e4-106">Call [**IAccPropServices::SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop), passing the **HWND**, object ID, child ID, the property to be overridden, and a [VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) containing the new value of the property.</span></span> <span data-ttu-id="160e4-107">Esta etapa anota o valor.</span><span class="sxs-lookup"><span data-stu-id="160e4-107">This step annotates the value.</span></span>
3.  <span data-ttu-id="160e4-108">Libere os ponteiros de interface e a memória livre.</span><span class="sxs-lookup"><span data-stu-id="160e4-108">Release the interface pointers and free memory.</span></span>

<span data-ttu-id="160e4-109">O exemplo a seguir mostra como anotar a propriedade [**role**](role-property.md) de um controle de texto estático.</span><span class="sxs-lookup"><span data-stu-id="160e4-109">The following example shows how to annotate the [**Role**](role-property.md) property of a static text control.</span></span>


```C++
HRESULT CMyTextControl::SetAccessibleProperties()
{
  // COM is assumed to be initialized...
  IAccPropServices* pAccPropServices = NULL;

  HRESULT hr = CoCreateInstance(CLSID_AccPropServices,
    NULL, CLSCTX_SERVER, IID_IAccPropServices, 
    (void**)&pAccPropServices);

  if (SUCCEEDED(hr))
  {
    // Annotating the Role of this object to be STATICTEXT
    VARIANT var;
    var.vt = VT_I4;
    var.lVal = ROLE_SYSTEM_STATICTEXT;

    hr = pAccPropServices->SetHwndProp(_hwnd,
      OBJID_CLIENT,
      CHILDID_SELF,
      PROPID_ACC_ROLE,
      var);

    pAccPropServices->Release();
  }
  return hr;
}
```



## <a name="properties-supported-when-specifying-a-value"></a><span data-ttu-id="160e4-110">Propriedades com suporte ao especificar um valor</span><span class="sxs-lookup"><span data-stu-id="160e4-110">Properties Supported When Specifying a Value</span></span>

<span data-ttu-id="160e4-111">As seguintes propriedades do Microsoft Acessibilidade Ativa podem ser anotadas ao especificar um valor (em que o valor deve ser do tipo anotado) para anotação direta.</span><span class="sxs-lookup"><span data-stu-id="160e4-111">The following Microsoft Active Accessibility properties can be annotated when specifying a value (where the value must be of the noted type) for direct annotation.</span></span> <span data-ttu-id="160e4-112">Para substituir ou adicionar uma propriedade de automação da interface do usuário da Microsoft a um controle, você pode especificar a ID da propriedade de automação da interface do usuário em vez da ID da Propriedade do Microsoft Acessibilidade Ativa.</span><span class="sxs-lookup"><span data-stu-id="160e4-112">To override or add a Microsoft UI Automation property to a control, you can specify the UI Automation property ID instead of the Microsoft Active Accessibility property ID.</span></span> <span data-ttu-id="160e4-113">Para obter uma lista de IDs de automação de interface do usuário, consulte [identificadores de propriedade](uiauto-entry-propids.md).</span><span class="sxs-lookup"><span data-stu-id="160e4-113">For a list of UI Automation IDs, see [Property Identifiers](uiauto-entry-propids.md).</span></span>



| <span data-ttu-id="160e4-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="160e4-114">Property</span></span>                      | <span data-ttu-id="160e4-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="160e4-115">Type</span></span>     |
|-------------------------------|----------|
| <span data-ttu-id="160e4-116">\_nome da ACC de Propid \_</span><span class="sxs-lookup"><span data-stu-id="160e4-116">PROPID\_ACC\_NAME</span></span>             | <span data-ttu-id="160e4-117">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="160e4-117">VT\_BSTR</span></span> |
| <span data-ttu-id="160e4-118">\_Descrição da ACC de Propid \_</span><span class="sxs-lookup"><span data-stu-id="160e4-118">PROPID\_ACC\_DESCRIPTION</span></span>      | <span data-ttu-id="160e4-119">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="160e4-119">VT\_BSTR</span></span> |
| <span data-ttu-id="160e4-120">\_função de ACC de Propid \_</span><span class="sxs-lookup"><span data-stu-id="160e4-120">PROPID\_ACC\_ROLE</span></span>             | <span data-ttu-id="160e4-121">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="160e4-121">VT\_I4</span></span>   |
| <span data-ttu-id="160e4-122">\_estado de ACC de Propid \_</span><span class="sxs-lookup"><span data-stu-id="160e4-122">PROPID\_ACC\_STATE</span></span>            | <span data-ttu-id="160e4-123">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="160e4-123">VT\_I4</span></span>   |
| <span data-ttu-id="160e4-124">\_ajuda de ACC de Propid \_</span><span class="sxs-lookup"><span data-stu-id="160e4-124">PROPID\_ACC\_HELP</span></span>             | <span data-ttu-id="160e4-125">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="160e4-125">VT\_BSTR</span></span> |
| <span data-ttu-id="160e4-126">PROPID \_ ACC \_ KEYBOARDSHORTCUT</span><span class="sxs-lookup"><span data-stu-id="160e4-126">PROPID\_ACC\_KEYBOARDSHORTCUT</span></span> | <span data-ttu-id="160e4-127">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="160e4-127">VT\_BSTR</span></span> |
| <span data-ttu-id="160e4-128">PROPID \_ ACC \_ DEFAULTACTION</span><span class="sxs-lookup"><span data-stu-id="160e4-128">PROPID\_ACC\_DEFAULTACTION</span></span>    | <span data-ttu-id="160e4-129">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="160e4-129">VT\_BSTR</span></span> |
| <span data-ttu-id="160e4-130">PROPID \_ ACC \_ VALUEMAP</span><span class="sxs-lookup"><span data-stu-id="160e4-130">PROPID\_ACC\_VALUEMAP</span></span>         | <span data-ttu-id="160e4-131">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="160e4-131">VT\_BSTR</span></span> |
| <span data-ttu-id="160e4-132">PROPID \_ ACC \_ ROLEMAP</span><span class="sxs-lookup"><span data-stu-id="160e4-132">PROPID\_ACC\_ROLEMAP</span></span>          | <span data-ttu-id="160e4-133">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="160e4-133">VT\_BSTR</span></span> |
| <span data-ttu-id="160e4-134">PROPID \_ ACC \_ STATEMAP</span><span class="sxs-lookup"><span data-stu-id="160e4-134">PROPID\_ACC\_STATEMAP</span></span>         | <span data-ttu-id="160e4-135">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="160e4-135">VT\_BSTR</span></span> |



 

 

 