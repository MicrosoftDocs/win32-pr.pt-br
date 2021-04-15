---
description: A interface IKsPropertySet foi originalmente projetada como uma maneira eficiente de definir e recuperar propriedades de dispositivo em drivers WDM, usando KSProxy para converter as chamadas de método COM de modo de usuário em conjuntos de propriedades de modo kernel usados por drivers de classe de streaming WDM. Essa interface agora também é usada para passar informações estritamente entre componentes de software. Em alguns casos, os componentes de software devem implementar essa interface ou também a interface IKsControl (documentada no DirectShow DDK). Por exemplo, se você estiver escrevendo um decodificador MPEG-2 de software para uso com o navegador de DVD, deverá implementar uma dessas interfaces e também oferecer suporte aos conjuntos de propriedades relacionados a DVD que o navegador enviará para o decodificador. Os Pins podem dar suporte a uma dessas interfaces para permitir que outros Pins ou filtros definam ou recuperem suas propriedades. Observe que outra interface por esse nome existe no arquivo de cabeçalho dsound. h. As duas interfaces não são compatíveis. A interface IKsControl, documentada no DirectShow DDK, agora é a interface recomendada para passar os conjuntos de propriedades entre os drivers WDM e os componentes do modo de usuário. .
ms.assetid: df26341d-f2d5-4a4e-954e-705e07415808
title: Interface IKsPropertySet (ksproxy. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 49a1f897d79a7514600f0c6553f931411aae8993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456387"
---
# <a name="ikspropertyset-interface"></a><span data-ttu-id="ca5fd-109">Interface IKsPropertySet</span><span class="sxs-lookup"><span data-stu-id="ca5fd-109">IKsPropertySet interface</span></span>

<span data-ttu-id="ca5fd-110">A `IKsPropertySet` interface foi originalmente projetada como uma maneira eficiente de definir e recuperar propriedades de dispositivo em drivers WDM, usando ksproxy para converter as chamadas de método com de modo de usuário em conjuntos de propriedades de modo kernel usadas por drivers de classe de streaming WDM.</span><span class="sxs-lookup"><span data-stu-id="ca5fd-110">The `IKsPropertySet` interface was originally designed as an efficient way to set and retrieve device properties on WDM drivers, using KSProxy to translate the user-mode COM method calls into the kernel-mode property sets used by WDM streaming class drivers.</span></span> <span data-ttu-id="ca5fd-111">Essa interface agora também é usada para passar informações estritamente entre componentes de software.</span><span class="sxs-lookup"><span data-stu-id="ca5fd-111">This interface is now also used to pass information strictly between software components.</span></span>

<span data-ttu-id="ca5fd-112">Em alguns casos, os componentes de software devem implementar essa interface ou também a interface **IKsControl** (documentada no DirectShow DDK).</span><span class="sxs-lookup"><span data-stu-id="ca5fd-112">In some cases, software components must implement either this interface, or else the **IKsControl** interface (documented in the DirectShow DDK).</span></span> <span data-ttu-id="ca5fd-113">Por exemplo, se você estiver escrevendo um decodificador MPEG-2 de software para uso com o [navegador de DVD](dvd-navigator-filter.md), deverá implementar uma dessas interfaces e também oferecer suporte aos conjuntos de propriedades relacionados a DVD que o navegador enviará para o decodificador.</span><span class="sxs-lookup"><span data-stu-id="ca5fd-113">For example, if you are writing a software MPEG-2 decoder for use with the [DVD Navigator](dvd-navigator-filter.md), you must implement one of these interfaces and also support the DVD-related property sets that the Navigator will send to the decoder.</span></span> <span data-ttu-id="ca5fd-114">Os Pins podem dar suporte a uma dessas interfaces para permitir que outros Pins ou filtros definam ou recuperem suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ca5fd-114">Pins may support one of these interfaces to allow other pins or filters to set or retrieve their properties.</span></span>

> [!Note]  
> <span data-ttu-id="ca5fd-115">Outra interface com esse nome existe no arquivo de cabeçalho dsound. h.</span><span class="sxs-lookup"><span data-stu-id="ca5fd-115">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="ca5fd-116">As duas interfaces não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="ca5fd-116">The two interfaces are not compatible.</span></span> <span data-ttu-id="ca5fd-117">A interface **IKsControl** , documentada no DirectShow DDK, agora é a interface recomendada para passar os conjuntos de propriedades entre os drivers WDM e os componentes do modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="ca5fd-117">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

## <a name="members"></a><span data-ttu-id="ca5fd-118">Membros</span><span class="sxs-lookup"><span data-stu-id="ca5fd-118">Members</span></span>

<span data-ttu-id="ca5fd-119">A interface **IKsPropertySet** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ca5fd-119">The **IKsPropertySet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ca5fd-120">**IKsPropertySet** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ca5fd-120">**IKsPropertySet** also has these types of members:</span></span>

-   [<span data-ttu-id="ca5fd-121">Métodos</span><span class="sxs-lookup"><span data-stu-id="ca5fd-121">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ca5fd-122">Métodos</span><span class="sxs-lookup"><span data-stu-id="ca5fd-122">Methods</span></span>

<span data-ttu-id="ca5fd-123">A interface **IKsPropertySet** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ca5fd-123">The **IKsPropertySet** interface has these methods.</span></span>



| <span data-ttu-id="ca5fd-124">Método</span><span class="sxs-lookup"><span data-stu-id="ca5fd-124">Method</span></span>                                                  | <span data-ttu-id="ca5fd-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca5fd-125">Description</span></span>                                                                          |
|:--------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca5fd-126">**Obter**</span><span class="sxs-lookup"><span data-stu-id="ca5fd-126">**Get**</span></span>](ikspropertyset-get.md)                       | <span data-ttu-id="ca5fd-127">Recupera uma propriedade identificada por um GUID de conjunto de propriedades e uma ID de propriedade.</span><span class="sxs-lookup"><span data-stu-id="ca5fd-127">Retrieves a property identified by a property set GUID and a property ID.</span></span><br/> |
| [<span data-ttu-id="ca5fd-128">**QuerySupported**</span><span class="sxs-lookup"><span data-stu-id="ca5fd-128">**QuerySupported**</span></span>](ikspropertyset-querysupported.md) | <span data-ttu-id="ca5fd-129">Determina se um objeto dá suporte a um conjunto de propriedades especificado.</span><span class="sxs-lookup"><span data-stu-id="ca5fd-129">Determines whether an object supports a specified property set.</span></span><br/>           |
| [<span data-ttu-id="ca5fd-130">**Definição**</span><span class="sxs-lookup"><span data-stu-id="ca5fd-130">**Set**</span></span>](ikspropertyset-set.md)                       | <span data-ttu-id="ca5fd-131">Define uma propriedade identificada por um GUID de conjunto de propriedades e uma ID de propriedade.</span><span class="sxs-lookup"><span data-stu-id="ca5fd-131">Sets a property identified by a property set GUID and a property ID.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="ca5fd-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca5fd-132">Remarks</span></span>

<span data-ttu-id="ca5fd-133">Você deve incluir KS. h antes de ksproxy. h.</span><span class="sxs-lookup"><span data-stu-id="ca5fd-133">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca5fd-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca5fd-134">Requirements</span></span>



| <span data-ttu-id="ca5fd-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca5fd-135">Requirement</span></span> | <span data-ttu-id="ca5fd-136">Valor</span><span class="sxs-lookup"><span data-stu-id="ca5fd-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca5fd-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca5fd-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ca5fd-138">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ca5fd-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ca5fd-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca5fd-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ca5fd-140">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ca5fd-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ca5fd-141">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ca5fd-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca5fd-142"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca5fd-142"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="ca5fd-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca5fd-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="ca5fd-144"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca5fd-144"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca5fd-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca5fd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca5fd-146">Conjuntos de propriedades</span><span class="sxs-lookup"><span data-stu-id="ca5fd-146">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 
