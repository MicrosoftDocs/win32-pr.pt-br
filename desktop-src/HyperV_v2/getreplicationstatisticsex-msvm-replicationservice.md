---
description: Recupera as estatísticas de replicação que estão associadas ao relacionamento de replicação especificado da máquina virtual.
ms.assetid: AB46894A-CBED-40DF-86B9-B578603B0341
title: 'Método Msvm_ReplicationService:: GetReplicationStatisticsEx'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7fdb60addc94094082fe83e70af06a2f5ae11f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770221"
---
# <a name="msvm_replicationservicegetreplicationstatisticsex-method"></a><span data-ttu-id="825aa-103">\_Método Msvm ReplicationService:: GetReplicationStatisticsEx</span><span class="sxs-lookup"><span data-stu-id="825aa-103">Msvm\_ReplicationService::GetReplicationStatisticsEx method</span></span>

<span data-ttu-id="825aa-104">Recupera as estatísticas de replicação que estão associadas ao relacionamento de replicação especificado da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="825aa-104">Retrieves the replication statistics that are associated with the specified replication relationship of the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="825aa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="825aa-105">Syntax</span></span>


```C++
uint32 GetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="825aa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="825aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="825aa-107">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="825aa-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="825aa-108">Uma referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual para a qual recuperar as estatísticas de replicação.</span><span class="sxs-lookup"><span data-stu-id="825aa-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="825aa-109">*ReplicationRelationship* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="825aa-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="825aa-110">Uma representação de cadeia de caracteres de uma instância inserida da classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) que define a relação de replicação para a qual recuperar as estatísticas de replicação.</span><span class="sxs-lookup"><span data-stu-id="825aa-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="825aa-111">*ReplicationStatistics* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="825aa-111">*ReplicationStatistics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="825aa-112">Se for bem-sucedido, o receberá uma instância inserida da classe [**Msvm \_ ReplicationStatistics**](msvm-replicationstatistics.md) que contém as estatísticas de replicação para a relação de replicação solicitada.</span><span class="sxs-lookup"><span data-stu-id="825aa-112">If successful, receives an embedded instance of the [**Msvm\_ReplicationStatistics**](msvm-replicationstatistics.md) class that contains the replication statistics for the requested replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="825aa-113">*ReplicationHealthIssues* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="825aa-113">*ReplicationHealthIssues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="825aa-114">Se for bem-sucedido, o receberá uma matriz de instâncias inseridas da classe de [**\_ erro Msvm**](msvm-error.md) que indicam quaisquer erros ou avisos de replicação para a máquina virtual solicitada.</span><span class="sxs-lookup"><span data-stu-id="825aa-114">If successful, receives an array of embedded instances of the [**Msvm\_Error**](msvm-error.md) class that indicate any replication warnings or errors for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="825aa-115">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="825aa-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="825aa-116">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="825aa-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="825aa-117">Essa referência poderá ser **nula** se a tarefa for concluída.</span><span class="sxs-lookup"><span data-stu-id="825aa-117">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="825aa-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="825aa-118">Return value</span></span>

<span data-ttu-id="825aa-119">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="825aa-119">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="825aa-120">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="825aa-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="825aa-121">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="825aa-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="825aa-122">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="825aa-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="825aa-123">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="825aa-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="825aa-124">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="825aa-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="825aa-125">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="825aa-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="825aa-126">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="825aa-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="825aa-127">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="825aa-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="825aa-128">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="825aa-128">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="825aa-129">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="825aa-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="825aa-130">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="825aa-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="825aa-131">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="825aa-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="825aa-132">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="825aa-132">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="825aa-133">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="825aa-133">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="825aa-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="825aa-134">Requirements</span></span>



| <span data-ttu-id="825aa-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="825aa-135">Requirement</span></span> | <span data-ttu-id="825aa-136">Valor</span><span class="sxs-lookup"><span data-stu-id="825aa-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="825aa-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="825aa-137">Minimum supported client</span></span><br/> | <span data-ttu-id="825aa-138">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="825aa-138">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="825aa-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="825aa-139">Minimum supported server</span></span><br/> | <span data-ttu-id="825aa-140">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="825aa-140">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="825aa-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="825aa-141">Namespace</span></span><br/>                | <span data-ttu-id="825aa-142">\\\\\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="825aa-142">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="825aa-143">MOF</span><span class="sxs-lookup"><span data-stu-id="825aa-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="825aa-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="825aa-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="825aa-145">DLL</span><span class="sxs-lookup"><span data-stu-id="825aa-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="825aa-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="825aa-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="825aa-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="825aa-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="825aa-148">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="825aa-148">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="825aa-149">**ResetReplicationStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="825aa-149">**ResetReplicationStatisticsEx**</span></span>](resetreplicationstatisticsex-msvm-replicationservice.md)
</dt> </dl>

 

