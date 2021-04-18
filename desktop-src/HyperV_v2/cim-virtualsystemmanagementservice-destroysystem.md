---
description: Destrói um sistema virtual.
ms.assetid: 8d2504dc-ce23-4257-9dfd-6a35dfd84b2d
title: Método DestroySystem da classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 41355970bb70063b8e90deb8f49b5e6f4b439017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759250"
---
# <a name="destroysystem-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="3abf2-103">Método DestroySystem da \_ classe VIRTUALSYSTEMMANAGEMENTSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="3abf2-103">DestroySystem method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="3abf2-104">Destrói um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="3abf2-104">Destroys a virtual system.</span></span>

<span data-ttu-id="3abf2-105">O sistema virtual referenciado é destruído, incluindo todos os elementos com escopo definido por ele.</span><span class="sxs-lookup"><span data-stu-id="3abf2-105">The referenced virtual system is destroyed, including any elements scoped by it.</span></span> <span data-ttu-id="3abf2-106">Os recursos virtuais são retornados para seus pools de recursos, o que pode implicar a destruição desses recursos (dependente de implementação).</span><span class="sxs-lookup"><span data-stu-id="3abf2-106">Virtual resources are returned to their resource pools, which may imply the destruction of those resources (implementation dependent).</span></span> <span data-ttu-id="3abf2-107">Se o sistema virtual estiver ativo quando a operação for chamada, ele será desativado primeiro e depois destruído.</span><span class="sxs-lookup"><span data-stu-id="3abf2-107">If the virtual system is active when the operation is invoked, it is first deactivated and then destroyed.</span></span> <span data-ttu-id="3abf2-108">Se os instantâneos foram criados a partir do sistema virtual, eles também são destruídos.</span><span class="sxs-lookup"><span data-stu-id="3abf2-108">If snapshots were created from the virtual system, these are destroyed as well.</span></span>

## <a name="syntax"></a><span data-ttu-id="3abf2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3abf2-109">Syntax</span></span>


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3abf2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3abf2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3abf2-111">*AffectedSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3abf2-111">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3abf2-112">Referência a uma instância da classe [**CIM \_ ComputerSystem**](cim-computersystem.md) que representa o sistema de computador virtual a ser destruído.</span><span class="sxs-lookup"><span data-stu-id="3abf2-112">Reference to an instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) representing the virtual computer system that is to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="3abf2-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="3abf2-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3abf2-114">Se a operação for de longa execução, opcionalmente, [**um \_ ConcreteJob CIM**](cim-concretejob.md) que representa o trabalho poderá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="3abf2-114">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3abf2-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3abf2-115">Return value</span></span>

<span data-ttu-id="3abf2-116">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="3abf2-116">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="3abf2-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="3abf2-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3abf2-118">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="3abf2-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3abf2-119">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="3abf2-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3abf2-120">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="3abf2-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3abf2-121">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="3abf2-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3abf2-122">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="3abf2-122">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3abf2-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3abf2-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3abf2-124">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="3abf2-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3abf2-125">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="3abf2-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="3abf2-126">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="3abf2-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3abf2-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3abf2-127">Requirements</span></span>



| <span data-ttu-id="3abf2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3abf2-128">Requirement</span></span> | <span data-ttu-id="3abf2-129">Valor</span><span class="sxs-lookup"><span data-stu-id="3abf2-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3abf2-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3abf2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3abf2-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3abf2-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="3abf2-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3abf2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3abf2-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3abf2-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="3abf2-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="3abf2-134">Namespace</span></span><br/>                | <span data-ttu-id="3abf2-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="3abf2-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3abf2-136">MOF</span><span class="sxs-lookup"><span data-stu-id="3abf2-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3abf2-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3abf2-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3abf2-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3abf2-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3abf2-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3abf2-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3abf2-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="3abf2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3abf2-141">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3abf2-141">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




