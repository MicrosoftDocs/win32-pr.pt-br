---
description: O objeto SWbemPrivilege representa um único privilégio. Este objeto não pode ser criado pela chamada VBScript CreateObject.
ms.assetid: 18ee4587-6347-4075-b5e9-c5fb02f3cbf7
ms.tgt_platform: multiple
title: Objeto SWbemPrivilege (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege
- ISWbemPrivilege
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c3be448b4088011cd4d628a7d98b448af550b010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011752"
---
# <a name="swbemprivilege-object"></a><span data-ttu-id="8a0bd-104">Objeto SWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="8a0bd-104">SWbemPrivilege object</span></span>

<span data-ttu-id="8a0bd-105">O objeto **SWbemPrivilege** representa um único privilégio.</span><span class="sxs-lookup"><span data-stu-id="8a0bd-105">The **SWbemPrivilege** object represents a single privilege.</span></span> <span data-ttu-id="8a0bd-106">Este objeto não pode ser criado pela chamada VBScript **CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="8a0bd-106">This object cannot be created by the VBScript **CreateObject** call.</span></span>

## <a name="members"></a><span data-ttu-id="8a0bd-107">Membros</span><span class="sxs-lookup"><span data-stu-id="8a0bd-107">Members</span></span>

<span data-ttu-id="8a0bd-108">O objeto **SWbemPrivilege** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8a0bd-108">The **SWbemPrivilege** object has these types of members:</span></span>

-   [<span data-ttu-id="8a0bd-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8a0bd-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8a0bd-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8a0bd-110">Properties</span></span>

<span data-ttu-id="8a0bd-111">O objeto **SWbemPrivilege** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8a0bd-111">The **SWbemPrivilege** object has these properties.</span></span>



| <span data-ttu-id="8a0bd-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="8a0bd-112">Property</span></span>                                                     | <span data-ttu-id="8a0bd-113">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="8a0bd-113">Access type</span></span>           | <span data-ttu-id="8a0bd-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a0bd-114">Description</span></span>                                                                      |
|:-------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="8a0bd-115">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="8a0bd-115">**Displayname**</span></span>](swbemprivilege-displayname.md)<br/> | <span data-ttu-id="8a0bd-116">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a0bd-116">Read-only</span></span><br/>  | <span data-ttu-id="8a0bd-117">Nome de exibição deste privilégio.</span><span class="sxs-lookup"><span data-stu-id="8a0bd-117">Display name of this privilege.</span></span><br/>                                       |
| [<span data-ttu-id="8a0bd-118">**Identificador**</span><span class="sxs-lookup"><span data-stu-id="8a0bd-118">**Identifier**</span></span>](swbemprivilege-identifier.md)<br/>   | <span data-ttu-id="8a0bd-119">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8a0bd-119">Read/write</span></span><br/> | <span data-ttu-id="8a0bd-120">Inteiro que representa o privilégio que está sendo definido ou recuperado.</span><span class="sxs-lookup"><span data-stu-id="8a0bd-120">Integer that represents the privilege that is being set or retrieved.</span></span><br/> |
| [<span data-ttu-id="8a0bd-121">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="8a0bd-121">**IsEnabled**</span></span>](swbemprivilege-isenabled.md)<br/>     | <span data-ttu-id="8a0bd-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8a0bd-122">Read/write</span></span><br/> | <span data-ttu-id="8a0bd-123">Valor booliano que indica se esse privilégio está habilitado.</span><span class="sxs-lookup"><span data-stu-id="8a0bd-123">Boolean value that indicates if this privilege is enabled.</span></span><br/>            |
| [<span data-ttu-id="8a0bd-124">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8a0bd-124">**Name**</span></span>](swbemprivilege-name.md)<br/>               | <span data-ttu-id="8a0bd-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a0bd-125">Read-only</span></span><br/>  | <span data-ttu-id="8a0bd-126">Nome deste privilégio.</span><span class="sxs-lookup"><span data-stu-id="8a0bd-126">Name of this privilege.</span></span><br/>                                               |



 

## <a name="requirements"></a><span data-ttu-id="8a0bd-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a0bd-127">Requirements</span></span>



| <span data-ttu-id="8a0bd-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a0bd-128">Requirement</span></span> | <span data-ttu-id="8a0bd-129">Valor</span><span class="sxs-lookup"><span data-stu-id="8a0bd-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a0bd-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a0bd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8a0bd-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a0bd-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8a0bd-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a0bd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8a0bd-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a0bd-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8a0bd-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8a0bd-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a0bd-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a0bd-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a0bd-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8a0bd-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="8a0bd-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8a0bd-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8a0bd-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8a0bd-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a0bd-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a0bd-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8a0bd-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="8a0bd-140">CLSID</span></span><br/>                    | <span data-ttu-id="8a0bd-141">\_SWBEMPRIVILEGE CLSID</span><span class="sxs-lookup"><span data-stu-id="8a0bd-141">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="8a0bd-142">IID</span><span class="sxs-lookup"><span data-stu-id="8a0bd-142">IID</span></span><br/>                      | <span data-ttu-id="8a0bd-143">ISWbemPrivilege de IID \_</span><span class="sxs-lookup"><span data-stu-id="8a0bd-143">IID\_ISWbemPrivilege</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="8a0bd-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a0bd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a0bd-145">Executando operações privilegiadas</span><span class="sxs-lookup"><span data-stu-id="8a0bd-145">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="8a0bd-146">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="8a0bd-146">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




