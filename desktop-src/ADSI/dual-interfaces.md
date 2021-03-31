---
title: Interfaces duplas (ADSI)
description: Use interfaces COM para acessar as propriedades e os métodos em qualquer objeto ADSI do provedor.
ms.assetid: 6f3fd725-d660-4cc3-8de2-8ed7800b1141
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34c858275098dd82362d229bc9e1cc35b544c55
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641821"
---
# <a name="dual-interfaces-adsi"></a><span data-ttu-id="97f3f-103">Interfaces duplas (ADSI)</span><span class="sxs-lookup"><span data-stu-id="97f3f-103">Dual Interfaces (ADSI)</span></span>

<span data-ttu-id="97f3f-104">Use interfaces COM para acessar as propriedades e os métodos em qualquer objeto ADSI do provedor.</span><span class="sxs-lookup"><span data-stu-id="97f3f-104">Use COM interfaces to access the properties and methods on any provider ADSI objects.</span></span> <span data-ttu-id="97f3f-105">Uma propriedade somente leitura é mapeada para uma entrada de interface do formulário **Get \_ <PropertyName>**.</span><span class="sxs-lookup"><span data-stu-id="97f3f-105">A read-only property maps to an interface entry of the form **get\_<PropertyName>**.</span></span> <span data-ttu-id="97f3f-106">Uma propriedade de leitura/gravação é mapeada para duas entradas de interface do formulário **Get \_ <PropertyName>** e **Put \_ <PropertyName>**.</span><span class="sxs-lookup"><span data-stu-id="97f3f-106">A read/write property maps to two interface entries of the form **get\_<PropertyName>** and **put\_<PropertyName>**.</span></span>

<span data-ttu-id="97f3f-107">Todos os métodos em uma interface COM devem:</span><span class="sxs-lookup"><span data-stu-id="97f3f-107">All methods on a COM interface must:</span></span>

-   <span data-ttu-id="97f3f-108">Retornar um valor HRESULT para indicar êxito ou falha.</span><span class="sxs-lookup"><span data-stu-id="97f3f-108">Return an HRESULT value to indicate success or failure.</span></span> <span data-ttu-id="97f3f-109">O tipo **HRESULT** é abordado na especificação com.</span><span class="sxs-lookup"><span data-stu-id="97f3f-109">The **HRESULT** type is discussed in the COM specification.</span></span>
-   <span data-ttu-id="97f3f-110">Em chamadas para **QueryInterface**, retorna **E \_ nointerface** para interfaces não implementadas.</span><span class="sxs-lookup"><span data-stu-id="97f3f-110">On calls to **QueryInterface**, return **E\_NOINTERFACE** for unimplemented interfaces.</span></span>
-   <span data-ttu-id="97f3f-111">Retornar **E \_ NOTIMPL** para métodos não implementados em interfaces que, de outra forma, são implementadas.</span><span class="sxs-lookup"><span data-stu-id="97f3f-111">Return **E\_NOTIMPL** for unimplemented methods on interfaces that are otherwise implemented.</span></span>
-   <span data-ttu-id="97f3f-112">**\_ \_ \_ Não \_ há** suporte para retornar a propriedade Ads para propriedades de interface que não têm suporte.</span><span class="sxs-lookup"><span data-stu-id="97f3f-112">Return **E\_ADS\_PROPERTY\_NOT\_SUPPORTED** for interface properties that are not supported.</span></span>

<span data-ttu-id="97f3f-113">Para manter a compatibilidade com os controladores de automação, todos os parâmetros e tipos de retorno devem estar dentro do subconjunto definido pelo tipo de dados variante de automação.</span><span class="sxs-lookup"><span data-stu-id="97f3f-113">To retain compatibility with Automation controllers, all parameters and return types should be within the subset defined by the Automation VARIANT data type.</span></span> <span data-ttu-id="97f3f-114">Para obter mais informações, consulte **Variant** e **VARIANTARG** no SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="97f3f-114">For more information, see **VARIANT** and **VARIANTARG** in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="97f3f-115">Um provedor Active Directory objeto pode expor interfaces que usam tipos de dados diferentes daqueles no subconjunto de **variantes** .</span><span class="sxs-lookup"><span data-stu-id="97f3f-115">A provider Active Directory object can expose interfaces that use data types other than those in the **VARIANT** subset.</span></span> <span data-ttu-id="97f3f-116">No entanto, os controladores de automação, como Visual Basic, não são capazes de chamar essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="97f3f-116">However, Automation controllers such as Visual Basic are not able to call those interfaces.</span></span> <span data-ttu-id="97f3f-117">A maioria das interfaces de provedor ADSI é derivada de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e pode ser usada como ponteiros de interface **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="97f3f-117">Most ADSI provider interfaces are derived from [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) and can be used as **IDispatch** interface pointers.</span></span> <span data-ttu-id="97f3f-118">No entanto, as interfaces ADSI [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)e [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) não são derivadas de **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="97f3f-118">However, the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), and [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) ADSI interfaces are not derived from **IDispatch**.</span></span>

 

 