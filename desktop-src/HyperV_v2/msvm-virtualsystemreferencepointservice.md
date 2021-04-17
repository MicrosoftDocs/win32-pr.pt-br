---
description: Descreve um serviço de ponto de referência do sistema virtual.
ms.assetid: 888ecd21-4b59-46a9-b2e1-538e30dd2d1c
title: Classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0614349ed6f6358316826bbfc2cd10ac55cba953
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105758329"
---
# <a name="msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="1117f-103">\_Classe Msvm VirtualSystemReferencePointService</span><span class="sxs-lookup"><span data-stu-id="1117f-103">Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="1117f-104">Descreve um serviço de ponto de referência do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="1117f-104">Describes a virtual system reference point service.</span></span>

<span data-ttu-id="1117f-105">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1117f-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1117f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1117f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="1117f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1117f-107">Members</span></span>

<span data-ttu-id="1117f-108">A classe **Msvm \_ VirtualSystemReferencePointService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1117f-108">The **Msvm\_VirtualSystemReferencePointService** class has these types of members:</span></span>

-   [<span data-ttu-id="1117f-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="1117f-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1117f-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="1117f-110">Methods</span></span>

<span data-ttu-id="1117f-111">A classe **Msvm \_ VirtualSystemReferencePointService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1117f-111">The **Msvm\_VirtualSystemReferencePointService** class has these methods.</span></span>



| <span data-ttu-id="1117f-112">Método</span><span class="sxs-lookup"><span data-stu-id="1117f-112">Method</span></span>                                                                                                       | <span data-ttu-id="1117f-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="1117f-113">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="1117f-114">**CreateReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="1117f-114">**CreateReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-createreferencepoint.md)                 | <span data-ttu-id="1117f-115">Cria um ponto de referência de um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="1117f-115">Creates a reference point of a virtual system.</span></span><br/>            |
| [<span data-ttu-id="1117f-116">**DestroyReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="1117f-116">**DestroyReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-destroyreferencepoint.md)               | <span data-ttu-id="1117f-117">Exclui o ponto de referência especificado.</span><span class="sxs-lookup"><span data-stu-id="1117f-117">Deletes the specified reference point.</span></span><br/>                    |
| [<span data-ttu-id="1117f-118">**ExportReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="1117f-118">**ExportReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-exportreferencepoint.md)                 | <span data-ttu-id="1117f-119">Exporta o ponto de referência do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="1117f-119">Exports the reference point of the virtual system.</span></span><br/>        |
| [<span data-ttu-id="1117f-120">**ImportReferencePointMetadata**</span><span class="sxs-lookup"><span data-stu-id="1117f-120">**ImportReferencePointMetadata**</span></span>](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md) | <span data-ttu-id="1117f-121">Importa os metadados do ponto de referência do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="1117f-121">Imports reference point metadata of the virtual system.</span></span><br/>   |
| [<span data-ttu-id="1117f-122">**RemoveAssociatedData**</span><span class="sxs-lookup"><span data-stu-id="1117f-122">**RemoveAssociatedData**</span></span>](msvm-virtualsystemreferencepointservice-removeassociateddata.md)                 | <span data-ttu-id="1117f-123">Remove o log de dados associado ao ponto de referência.</span><span class="sxs-lookup"><span data-stu-id="1117f-123">Removes the data log associated with the reference point.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1117f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1117f-124">Requirements</span></span>



| <span data-ttu-id="1117f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1117f-125">Requirement</span></span> | <span data-ttu-id="1117f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="1117f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1117f-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1117f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1117f-128">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1117f-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="1117f-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1117f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1117f-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1117f-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1117f-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="1117f-131">Namespace</span></span><br/>                | <span data-ttu-id="1117f-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1117f-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1117f-133">MOF</span><span class="sxs-lookup"><span data-stu-id="1117f-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1117f-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1117f-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1117f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1117f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1117f-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1117f-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1117f-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="1117f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1117f-138">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="1117f-138">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




