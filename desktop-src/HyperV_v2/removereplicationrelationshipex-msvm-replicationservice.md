---
description: Remove a relação de replicação da máquina virtual especificada.
ms.assetid: 0D5013CE-7BAE-4A99-ABF2-F1ECC644A1B2
title: 'Método Msvm_ReplicationService:: RemoveReplicationRelationshipEx'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveReplicationRelationshipEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c57ed7f9a88789d04a20de0fd199d460b47c1eb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764680"
---
# <a name="msvm_replicationserviceremovereplicationrelationshipex-method"></a><span data-ttu-id="d3c41-103">\_Método Msvm ReplicationService:: RemoveReplicationRelationshipEx</span><span class="sxs-lookup"><span data-stu-id="d3c41-103">Msvm\_ReplicationService::RemoveReplicationRelationshipEx method</span></span>

<span data-ttu-id="d3c41-104">Remove a relação de replicação da máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="d3c41-104">Removes the specified virtual machine replication relationship.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3c41-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3c41-105">Syntax</span></span>


```C++
uint32 RemoveReplicationRelationshipEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="d3c41-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3c41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3c41-107">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d3c41-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c41-108">Uma referência a uma instância de [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa a máquina virtual para a qual a replicação será removida.</span><span class="sxs-lookup"><span data-stu-id="d3c41-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to remove the replication.</span></span>

</dd> <dt>

<span data-ttu-id="d3c41-109">*ReplicationRelationship* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d3c41-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c41-110">Uma representação de cadeia de caracteres de uma instância inserida da classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) que define a relação de replicação a ser removida.</span><span class="sxs-lookup"><span data-stu-id="d3c41-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship to remove.</span></span>

</dd> <dt>

<span data-ttu-id="d3c41-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="d3c41-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c41-112">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d3c41-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="d3c41-113">Essa referência poderá ser **nula** se a tarefa for concluída.</span><span class="sxs-lookup"><span data-stu-id="d3c41-113">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3c41-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3c41-114">Return value</span></span>

<span data-ttu-id="d3c41-115">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d3c41-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d3c41-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="d3c41-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d3c41-117">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="d3c41-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d3c41-118">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="d3c41-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d3c41-119">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="d3c41-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d3c41-120">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="d3c41-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d3c41-121">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="d3c41-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d3c41-122">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="d3c41-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d3c41-123">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="d3c41-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d3c41-124">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="d3c41-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d3c41-125">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="d3c41-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d3c41-126">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="d3c41-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d3c41-127">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="d3c41-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d3c41-128">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="d3c41-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="d3c41-129">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="d3c41-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="d3c41-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3c41-130">Remarks</span></span>

<span data-ttu-id="d3c41-131">Para uma máquina virtual de réplica, a replicação primária não poderá ser removida se a replicação estendida estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="d3c41-131">For a replica virtual machine, primary replication can't be removed if extended replication is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3c41-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3c41-132">Requirements</span></span>



| <span data-ttu-id="d3c41-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3c41-133">Requirement</span></span> | <span data-ttu-id="d3c41-134">Valor</span><span class="sxs-lookup"><span data-stu-id="d3c41-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c41-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3c41-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d3c41-136">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d3c41-136">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="d3c41-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3c41-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d3c41-138">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="d3c41-138">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d3c41-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="d3c41-139">Namespace</span></span><br/>                | <span data-ttu-id="d3c41-140">\\\\\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d3c41-140">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="d3c41-141">MOF</span><span class="sxs-lookup"><span data-stu-id="d3c41-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3c41-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3c41-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3c41-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d3c41-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3c41-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d3c41-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d3c41-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3c41-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3c41-146">**CreateReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="d3c41-146">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="d3c41-147">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="d3c41-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

