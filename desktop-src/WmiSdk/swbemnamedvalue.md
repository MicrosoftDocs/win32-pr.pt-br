---
description: O objeto SWbemNamedValue representa um único valor nomeado que pertence ao objeto da coleção SWbemNamedValueSet. Este objeto não pode ser criado pela chamada VBScript CreateObject.
ms.assetid: 3f72afcd-6e10-4200-804d-918e3eb2862f
ms.tgt_platform: multiple
title: Objeto SWbemNamedValue (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValue
- ISWbemNamedValue
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3668321256fea7ed8109e54f6b4df55bbd42867c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751731"
---
# <a name="swbemnamedvalue-object"></a><span data-ttu-id="94b86-104">Objeto SWbemNamedValue</span><span class="sxs-lookup"><span data-stu-id="94b86-104">SWbemNamedValue object</span></span>

<span data-ttu-id="94b86-105">O objeto **SWbemNamedValue** representa um único valor nomeado que pertence ao objeto da coleção [**SWbemNamedValueSet**](swbemnamedvalueset.md) .</span><span class="sxs-lookup"><span data-stu-id="94b86-105">The **SWbemNamedValue** object represents a single named value that belongs to the [**SWbemNamedValueSet**](swbemnamedvalueset.md) collection object.</span></span> <span data-ttu-id="94b86-106">Este objeto não pode ser criado pela chamada VBScript [**CreateObject**](creating-an-object-using-vbscript.md) .</span><span class="sxs-lookup"><span data-stu-id="94b86-106">This object cannot be created by the VBScript [**CreateObject**](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="94b86-107">Membros</span><span class="sxs-lookup"><span data-stu-id="94b86-107">Members</span></span>

<span data-ttu-id="94b86-108">O objeto **SWbemNamedValue** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="94b86-108">The **SWbemNamedValue** object has these types of members:</span></span>

-   [<span data-ttu-id="94b86-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="94b86-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="94b86-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="94b86-110">Properties</span></span>

<span data-ttu-id="94b86-111">O objeto **SWbemNamedValue** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="94b86-111">The **SWbemNamedValue** object has these properties.</span></span>



| <span data-ttu-id="94b86-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="94b86-112">Property</span></span>                                          | <span data-ttu-id="94b86-113">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="94b86-113">Access type</span></span>           | <span data-ttu-id="94b86-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="94b86-114">Description</span></span>                                                                                    |
|:--------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94b86-115">**Nome**</span><span class="sxs-lookup"><span data-stu-id="94b86-115">**Name**</span></span>](swbemnamedvalue-name.md)<br/>   | <span data-ttu-id="94b86-116">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94b86-116">Read-only</span></span><br/>  | <span data-ttu-id="94b86-117">Nome do item **SWbemNamedValue** .</span><span class="sxs-lookup"><span data-stu-id="94b86-117">Name of the **SWbemNamedValue** item.</span></span><br/>                                               |
| [<span data-ttu-id="94b86-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="94b86-118">**Value**</span></span>](swbemnamedvalue-value.md)<br/> | <span data-ttu-id="94b86-119">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94b86-119">Read/write</span></span><br/> | <span data-ttu-id="94b86-120">Valor do item **SWbemNamedValue** .</span><span class="sxs-lookup"><span data-stu-id="94b86-120">Value of the **SWbemNamedValue** item.</span></span> <span data-ttu-id="94b86-121">Essa é a propriedade padrão deste objeto.</span><span class="sxs-lookup"><span data-stu-id="94b86-121">This is the default property of this object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="94b86-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94b86-122">Requirements</span></span>



| <span data-ttu-id="94b86-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="94b86-123">Requirement</span></span> | <span data-ttu-id="94b86-124">Valor</span><span class="sxs-lookup"><span data-stu-id="94b86-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94b86-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94b86-125">Minimum supported client</span></span><br/> | <span data-ttu-id="94b86-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94b86-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94b86-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94b86-127">Minimum supported server</span></span><br/> | <span data-ttu-id="94b86-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94b86-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94b86-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="94b86-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="94b86-130"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="94b86-130"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="94b86-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="94b86-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="94b86-132"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="94b86-132"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="94b86-133">DLL</span><span class="sxs-lookup"><span data-stu-id="94b86-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94b86-134"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94b86-134"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="94b86-135">CLSID</span><span class="sxs-lookup"><span data-stu-id="94b86-135">CLSID</span></span><br/>                    | <span data-ttu-id="94b86-136">\_SWBEMNAMEDVALUE CLSID</span><span class="sxs-lookup"><span data-stu-id="94b86-136">CLSID\_SWbemNamedValue</span></span><br/>                                                       |
| <span data-ttu-id="94b86-137">IID</span><span class="sxs-lookup"><span data-stu-id="94b86-137">IID</span></span><br/>                      | <span data-ttu-id="94b86-138">ISWbemNamedValue de IID \_</span><span class="sxs-lookup"><span data-stu-id="94b86-138">IID\_ISWbemNamedValue</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="94b86-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="94b86-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94b86-140">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="94b86-140">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




