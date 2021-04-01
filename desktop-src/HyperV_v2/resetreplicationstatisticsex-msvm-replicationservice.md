---
description: Redefine as estatísticas de replicação que estão associadas à relação de replicação especificada da máquina virtual especificada.
ms.assetid: 6E49A7C0-2F60-444E-964E-420470EE1538
title: 'Método Msvm_ReplicationService:: ResetReplicationStatisticsEx'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ResetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c1acb234660e71636b4a69a697b11385d65cf1ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829022"
---
# <a name="msvm_replicationserviceresetreplicationstatisticsex-method"></a><span data-ttu-id="dcf3e-103">\_Método Msvm ReplicationService:: ResetReplicationStatisticsEx</span><span class="sxs-lookup"><span data-stu-id="dcf3e-103">Msvm\_ReplicationService::ResetReplicationStatisticsEx method</span></span>

<span data-ttu-id="dcf3e-104">Redefine as estatísticas de replicação que estão associadas à relação de replicação especificada da máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="dcf3e-104">Resets replication statistics that are associated with the specified replication relationship of the specified virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcf3e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dcf3e-105">Syntax</span></span>


```C++
uint32 ResetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="dcf3e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dcf3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcf3e-107">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dcf3e-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf3e-108">Uma referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual habilitada para réplica.</span><span class="sxs-lookup"><span data-stu-id="dcf3e-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the replica-enabled virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="dcf3e-109">*ReplicationRelationship* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dcf3e-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf3e-110">Uma representação de cadeia de caracteres de uma instância inserida da classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) que define a relação de replicação para a qual redefinir as estatísticas de replicação.</span><span class="sxs-lookup"><span data-stu-id="dcf3e-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for which to reset the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="dcf3e-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="dcf3e-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf3e-112">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dcf3e-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="dcf3e-113">Essa referência poderá ser **nula** se a tarefa for concluída.</span><span class="sxs-lookup"><span data-stu-id="dcf3e-113">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcf3e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dcf3e-114">Return value</span></span>

<span data-ttu-id="dcf3e-115">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="dcf3e-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="dcf3e-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="dcf3e-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dcf3e-117">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="dcf3e-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="dcf3e-118">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="dcf3e-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="dcf3e-119">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="dcf3e-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="dcf3e-120">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="dcf3e-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="dcf3e-121">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="dcf3e-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="dcf3e-122">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="dcf3e-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="dcf3e-123">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="dcf3e-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="dcf3e-124">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="dcf3e-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="dcf3e-125">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="dcf3e-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="dcf3e-126">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="dcf3e-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="dcf3e-127">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="dcf3e-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="dcf3e-128">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="dcf3e-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="dcf3e-129">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="dcf3e-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="dcf3e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcf3e-130">Requirements</span></span>



| <span data-ttu-id="dcf3e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcf3e-131">Requirement</span></span> | <span data-ttu-id="dcf3e-132">Valor</span><span class="sxs-lookup"><span data-stu-id="dcf3e-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcf3e-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dcf3e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="dcf3e-134">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dcf3e-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="dcf3e-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dcf3e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="dcf3e-136">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="dcf3e-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dcf3e-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="dcf3e-137">Namespace</span></span><br/>                | <span data-ttu-id="dcf3e-138">\\\\\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="dcf3e-138">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="dcf3e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="dcf3e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dcf3e-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dcf3e-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dcf3e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="dcf3e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcf3e-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dcf3e-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dcf3e-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="dcf3e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcf3e-144">**GetReplicationStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="dcf3e-144">**GetReplicationStatisticsEx**</span></span>](getreplicationstatisticsex-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="dcf3e-145">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="dcf3e-145">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

