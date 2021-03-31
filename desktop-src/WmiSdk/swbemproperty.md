---
description: O objeto SWbemProperty representa uma única propriedade WMI de um objeto gerenciado. Este objeto não pode ser criado pela chamada VBScript CreateObject.
ms.assetid: 2ddcfffa-a7b4-4fd6-926d-411de27f6212
ms.tgt_platform: multiple
title: Objeto SWbemProperty (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty
- ISWbemProperty
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9c71db4063f5de6b48b2e8213f21ca1320a880fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171970"
---
# <a name="swbemproperty-object"></a><span data-ttu-id="c52b9-104">Objeto SWbemProperty</span><span class="sxs-lookup"><span data-stu-id="c52b9-104">SWbemProperty object</span></span>

<span data-ttu-id="c52b9-105">O objeto **SWbemProperty** representa uma única propriedade WMI de um objeto gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c52b9-105">The **SWbemProperty** object represents a single WMI property of a managed object.</span></span> <span data-ttu-id="c52b9-106">Este objeto não pode ser criado pela chamada VBScript [CreateObject](creating-an-object-using-vbscript.md) .</span><span class="sxs-lookup"><span data-stu-id="c52b9-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="c52b9-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c52b9-107">Members</span></span>

<span data-ttu-id="c52b9-108">O objeto **SWbemProperty** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c52b9-108">The **SWbemProperty** object has these types of members:</span></span>

-   [<span data-ttu-id="c52b9-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c52b9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c52b9-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c52b9-110">Properties</span></span>

<span data-ttu-id="c52b9-111">O objeto **SWbemProperty** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c52b9-111">The **SWbemProperty** object has these properties.</span></span>



| <span data-ttu-id="c52b9-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c52b9-112">Property</span></span>                                                     | <span data-ttu-id="c52b9-113">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="c52b9-113">Access type</span></span>           | <span data-ttu-id="c52b9-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="c52b9-114">Description</span></span>                                                                                                                   |
|:-------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c52b9-115">**CIMType**</span><span class="sxs-lookup"><span data-stu-id="c52b9-115">**CIMType**</span></span>](swbemproperty-cimtype.md)<br/>          | <span data-ttu-id="c52b9-116">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c52b9-116">Read-only</span></span><br/>  | <span data-ttu-id="c52b9-117">Tipo desta propriedade.</span><span class="sxs-lookup"><span data-stu-id="c52b9-117">Type of this property.</span></span><br/>                                                                                             |
| [<span data-ttu-id="c52b9-118">**IsArray**</span><span class="sxs-lookup"><span data-stu-id="c52b9-118">**IsArray**</span></span>](swbemproperty-isarray.md)<br/>          | <span data-ttu-id="c52b9-119">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c52b9-119">Read-only</span></span><br/>  | <span data-ttu-id="c52b9-120">Valor booliano que indica se essa propriedade tem um tipo de matriz.</span><span class="sxs-lookup"><span data-stu-id="c52b9-120">Boolean value that indicates if this property has an array type.</span></span><br/>                                                   |
| [<span data-ttu-id="c52b9-121">**IsLocal**</span><span class="sxs-lookup"><span data-stu-id="c52b9-121">**IsLocal**</span></span>](swbemproperty-islocal.md)<br/>          | <span data-ttu-id="c52b9-122">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c52b9-122">Read-only</span></span><br/>  | <span data-ttu-id="c52b9-123">Valor booliano que indica se essa propriedade é local.</span><span class="sxs-lookup"><span data-stu-id="c52b9-123">Boolean value that indicates if this property is local.</span></span><br/>                                                            |
| [<span data-ttu-id="c52b9-124">**Name**</span><span class="sxs-lookup"><span data-stu-id="c52b9-124">**Name**</span></span>](swbemproperty-name.md)<br/>                | <span data-ttu-id="c52b9-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c52b9-125">Read-only</span></span><br/>  | <span data-ttu-id="c52b9-126">Nome dessa propriedade WMI.</span><span class="sxs-lookup"><span data-stu-id="c52b9-126">Name of this WMI property.</span></span><br/>                                                                                         |
| [<span data-ttu-id="c52b9-127">**Ter**</span><span class="sxs-lookup"><span data-stu-id="c52b9-127">**Origin**</span></span>](swbemproperty-origin.md)<br/>            | <span data-ttu-id="c52b9-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c52b9-128">Read-only</span></span><br/>  | <span data-ttu-id="c52b9-129">Contém a classe de origem desta propriedade.</span><span class="sxs-lookup"><span data-stu-id="c52b9-129">Contains the originating class of this property.</span></span><br/>                                                                   |
| [<span data-ttu-id="c52b9-130">**Qualificadores\_**</span><span class="sxs-lookup"><span data-stu-id="c52b9-130">**Qualifiers\_**</span></span>](swbemproperty-qualifiers-.md)<br/> | <span data-ttu-id="c52b9-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c52b9-131">Read-only</span></span><br/>  | <span data-ttu-id="c52b9-132">Um objeto [**SWbemQualifierSet**](swbemqualifierset.md) , que é a coleção de qualificadores para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c52b9-132">An [**SWbemQualifierSet**](swbemqualifierset.md) object, which is the collection of qualifiers for this property.</span></span><br/> |
| [<span data-ttu-id="c52b9-133">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c52b9-133">**Value**</span></span>](swbemproperty-value.md)<br/>              | <span data-ttu-id="c52b9-134">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c52b9-134">Read/write</span></span><br/> | <span data-ttu-id="c52b9-135">Valor real dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c52b9-135">Actual value of this property.</span></span> <span data-ttu-id="c52b9-136">Esta é a propriedade de automação padrão deste objeto.</span><span class="sxs-lookup"><span data-stu-id="c52b9-136">This is the default automation property of this object.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="c52b9-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c52b9-137">Requirements</span></span>



| <span data-ttu-id="c52b9-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="c52b9-138">Requirement</span></span> | <span data-ttu-id="c52b9-139">Valor</span><span class="sxs-lookup"><span data-stu-id="c52b9-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c52b9-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c52b9-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c52b9-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c52b9-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c52b9-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c52b9-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c52b9-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c52b9-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c52b9-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c52b9-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="c52b9-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c52b9-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c52b9-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c52b9-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="c52b9-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c52b9-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c52b9-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c52b9-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c52b9-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c52b9-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c52b9-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="c52b9-150">CLSID</span></span><br/>                    | <span data-ttu-id="c52b9-151">\_SWBEMPROPERTY CLSID</span><span class="sxs-lookup"><span data-stu-id="c52b9-151">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="c52b9-152">IID</span><span class="sxs-lookup"><span data-stu-id="c52b9-152">IID</span></span><br/>                      | <span data-ttu-id="c52b9-153">ISWbemProperty de IID \_</span><span class="sxs-lookup"><span data-stu-id="c52b9-153">IID\_ISWbemProperty</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="c52b9-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="c52b9-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c52b9-155">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="c52b9-155">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




