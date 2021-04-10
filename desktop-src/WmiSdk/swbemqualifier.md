---
description: Você pode usar as propriedades do objeto SWbemQualifier para representar um único qualificador de uma classe, instância, propriedade ou parâmetro de método WMI. Este objeto não pode ser criado pela chamada VBScript CreateObject.
ms.assetid: b5dbe98a-e1d8-4679-a563-c88760d08b79
ms.tgt_platform: multiple
title: Objeto SWbemQualifier (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifier
- ISWbemQualifier
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5e9a49832ffa1e38fbe6ee0f71e1f6a39c1b0ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165189"
---
# <a name="swbemqualifier-object"></a><span data-ttu-id="34233-104">Objeto SWbemQualifier</span><span class="sxs-lookup"><span data-stu-id="34233-104">SWbemQualifier object</span></span>

<span data-ttu-id="34233-105">Você pode usar as propriedades do objeto **SWbemQualifier** para representar um único qualificador de uma classe, instância, propriedade ou parâmetro de método WMI.</span><span class="sxs-lookup"><span data-stu-id="34233-105">You can use the properties of the **SWbemQualifier** object to represent a single qualifier of a WMI class, instance, property, or method parameter.</span></span> <span data-ttu-id="34233-106">Este objeto não pode ser criado pela chamada VBScript [CreateObject](creating-an-object-using-vbscript.md) .</span><span class="sxs-lookup"><span data-stu-id="34233-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="34233-107">Membros</span><span class="sxs-lookup"><span data-stu-id="34233-107">Members</span></span>

<span data-ttu-id="34233-108">O objeto **SWbemQualifier** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="34233-108">The **SWbemQualifier** object has these types of members:</span></span>

-   [<span data-ttu-id="34233-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="34233-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="34233-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="34233-110">Properties</span></span>

<span data-ttu-id="34233-111">O objeto **SWbemQualifier** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="34233-111">The **SWbemQualifier** object has these properties.</span></span>



| <span data-ttu-id="34233-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="34233-112">Property</span></span>                                                                       | <span data-ttu-id="34233-113">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="34233-113">Access type</span></span>           | <span data-ttu-id="34233-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="34233-114">Description</span></span>                                                                                           |
|:-------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34233-115">**Isemendado**</span><span class="sxs-lookup"><span data-stu-id="34233-115">**IsAmended**</span></span>](swbemqualifier-isamended.md)<br/>                       | <span data-ttu-id="34233-116">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34233-116">Read-only</span></span><br/>  | <span data-ttu-id="34233-117">Valor booliano que indica se este qualificador foi localizado usando uma operação de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="34233-117">Boolean value that indicates if this qualifier has been localized using a merge operation.</span></span><br/> |
| [<span data-ttu-id="34233-118">**IsLocal**</span><span class="sxs-lookup"><span data-stu-id="34233-118">**IsLocal**</span></span>](swbemqualifier-islocal.md)<br/>                           | <span data-ttu-id="34233-119">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34233-119">Read-only</span></span><br/>  | <span data-ttu-id="34233-120">Valor booliano que indica se esse qualificador é local.</span><span class="sxs-lookup"><span data-stu-id="34233-120">Boolean value that indicates if this qualifier is local.</span></span><br/>                                   |
| [<span data-ttu-id="34233-121">**IsOverridable**</span><span class="sxs-lookup"><span data-stu-id="34233-121">**IsOverridable**</span></span>](swbemqualifier-isoverridable.md)<br/>               | <span data-ttu-id="34233-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="34233-122">Read/write</span></span><br/> | <span data-ttu-id="34233-123">Valor booliano que indica se este qualificador pode ser substituído quando propagado.</span><span class="sxs-lookup"><span data-stu-id="34233-123">Boolean value that indicates if this qualifier can be overridden when propagated.</span></span><br/>          |
| [<span data-ttu-id="34233-124">**Nome**</span><span class="sxs-lookup"><span data-stu-id="34233-124">**Name**</span></span>](swbemqualifier-name.md)<br/>                                 | <span data-ttu-id="34233-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34233-125">Read-only</span></span><br/>  | <span data-ttu-id="34233-126">Nome deste qualificador.</span><span class="sxs-lookup"><span data-stu-id="34233-126">Name of this qualifier.</span></span><br/>                                                                    |
| [<span data-ttu-id="34233-127">**PropagatesToInstance**</span><span class="sxs-lookup"><span data-stu-id="34233-127">**PropagatesToInstance**</span></span>](swbemqualifier-propagatestoinstance.md)<br/> | <span data-ttu-id="34233-128">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="34233-128">Read/write</span></span><br/> | <span data-ttu-id="34233-129">Valor booliano que indica se esse qualificador pode ser propagado para uma instância.</span><span class="sxs-lookup"><span data-stu-id="34233-129">Boolean value that indicates if this qualifier can be propagated to an instance.</span></span><br/>           |
| [<span data-ttu-id="34233-130">**PropagatesToSubClass**</span><span class="sxs-lookup"><span data-stu-id="34233-130">**PropagatesToSubClass**</span></span>](swbemqualifier-propagatestosubclass.md)<br/> | <span data-ttu-id="34233-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34233-131">Read-only</span></span><br/>  | <span data-ttu-id="34233-132">Valor booliano que indica se esse qualificador pode ser propagado para uma subclasse.</span><span class="sxs-lookup"><span data-stu-id="34233-132">Boolean value that indicates if this qualifier can be propagated to a subclass.</span></span><br/>            |
| [<span data-ttu-id="34233-133">**Valor**</span><span class="sxs-lookup"><span data-stu-id="34233-133">**Value**</span></span>](swbemqualifier-value.md)<br/>                               | <span data-ttu-id="34233-134">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="34233-134">Read/write</span></span><br/> | <span data-ttu-id="34233-135">Valor de variante deste qualificador.</span><span class="sxs-lookup"><span data-stu-id="34233-135">Variant value of this qualifier.</span></span> <span data-ttu-id="34233-136">Essa é a propriedade padrão deste objeto.</span><span class="sxs-lookup"><span data-stu-id="34233-136">This is the default property of this object.</span></span><br/>              |



 

## <a name="requirements"></a><span data-ttu-id="34233-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34233-137">Requirements</span></span>



| <span data-ttu-id="34233-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="34233-138">Requirement</span></span> | <span data-ttu-id="34233-139">Valor</span><span class="sxs-lookup"><span data-stu-id="34233-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34233-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34233-140">Minimum supported client</span></span><br/> | <span data-ttu-id="34233-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34233-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="34233-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34233-142">Minimum supported server</span></span><br/> | <span data-ttu-id="34233-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34233-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="34233-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="34233-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="34233-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="34233-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="34233-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="34233-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="34233-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="34233-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="34233-148">DLL</span><span class="sxs-lookup"><span data-stu-id="34233-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34233-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34233-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="34233-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="34233-150">CLSID</span></span><br/>                    | <span data-ttu-id="34233-151">\_SWBEMQUALIFIER CLSID</span><span class="sxs-lookup"><span data-stu-id="34233-151">CLSID\_SWbemQualifier</span></span><br/>                                                        |
| <span data-ttu-id="34233-152">IID</span><span class="sxs-lookup"><span data-stu-id="34233-152">IID</span></span><br/>                      | <span data-ttu-id="34233-153">ISWbemQualifier de IID \_</span><span class="sxs-lookup"><span data-stu-id="34233-153">IID\_ISWbemQualifier</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="34233-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="34233-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34233-155">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="34233-155">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




