---
description: Recupera as estatísticas de replicação para uma máquina virtual e atua na relação de replicação primária da máquina virtual.
ms.assetid: 24f3f572-fa85-4680-be77-7e835e6471c5
title: Método GetReplicationStatistics da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9dff711830ccdb805c362961671dff28f5bf0b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768510"
---
# <a name="getreplicationstatistics-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="8e259-103">Método GetReplicationStatistics da \_ classe ReplicationService Msvm</span><span class="sxs-lookup"><span data-stu-id="8e259-103">GetReplicationStatistics method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="8e259-104">Recupera as estatísticas de replicação para uma máquina virtual e atua na relação de replicação primária da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8e259-104">Retrieves replication statistics for a virtual machine and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="8e259-105">A partir do Windows 8.1, recomendamos não usar o **GetReplicationStatistics** para recuperar estatísticas de replicação.</span><span class="sxs-lookup"><span data-stu-id="8e259-105">Starting with Windows 8.1, we recommend not to use **GetReplicationStatistics** anymore to retrieve replication statistics.</span></span> <span data-ttu-id="8e259-106">Em vez disso, use [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md).</span><span class="sxs-lookup"><span data-stu-id="8e259-106">Instead, use [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8e259-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e259-107">Syntax</span></span>


```mof
uint32 GetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8e259-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e259-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e259-109">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8e259-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e259-110">Uma referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual para a qual recuperar as estatísticas de replicação.</span><span class="sxs-lookup"><span data-stu-id="8e259-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="8e259-111">*ReplicationStatistics* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8e259-111">*ReplicationStatistics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e259-112">Se for bem-sucedido, o receberá uma instância inserida da classe [**Msvm \_ ReplicationStatistics**](msvm-replicationstatistics.md) que contém as estatísticas de replicação para a máquina virtual solicitada.</span><span class="sxs-lookup"><span data-stu-id="8e259-112">If successful, receives an embedded instance of the [**Msvm\_ReplicationStatistics**](msvm-replicationstatistics.md) class that contains the replication statistics for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="8e259-113">*ReplicationHealthIssues* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8e259-113">*ReplicationHealthIssues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e259-114">Se for bem-sucedido, o receberá uma matriz de instâncias inseridas da classe de [**\_ erro Msvm**](msvm-error.md) que indicam quaisquer erros ou avisos de replicação para a máquina virtual solicitada.</span><span class="sxs-lookup"><span data-stu-id="8e259-114">If successful, receives an array of embedded instances of the [**Msvm\_Error**](msvm-error.md) class that indicate any replication warnings or errors for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="8e259-115">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="8e259-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e259-116">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8e259-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e259-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8e259-117">Return value</span></span>

<span data-ttu-id="8e259-118">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e259-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8e259-119">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="8e259-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8e259-120">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="8e259-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8e259-121">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="8e259-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="8e259-122">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="8e259-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="8e259-123">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="8e259-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="8e259-124">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="8e259-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="8e259-125">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="8e259-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="8e259-126">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="8e259-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="8e259-127">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="8e259-127">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="8e259-128">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="8e259-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="8e259-129">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="8e259-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="8e259-130">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="8e259-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="8e259-131">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="8e259-131">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="8e259-132">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="8e259-132">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8e259-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e259-133">Requirements</span></span>



| <span data-ttu-id="8e259-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e259-134">Requirement</span></span> | <span data-ttu-id="8e259-135">Valor</span><span class="sxs-lookup"><span data-stu-id="8e259-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e259-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e259-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8e259-137">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8e259-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8e259-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e259-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8e259-139">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8e259-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8e259-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e259-140">Namespace</span></span><br/>                | <span data-ttu-id="8e259-141">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8e259-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8e259-142">MOF</span><span class="sxs-lookup"><span data-stu-id="8e259-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e259-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e259-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e259-144">DLL</span><span class="sxs-lookup"><span data-stu-id="8e259-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e259-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8e259-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8e259-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e259-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e259-147">**ResetReplicationStatistics**</span><span class="sxs-lookup"><span data-stu-id="8e259-147">**ResetReplicationStatistics**</span></span>](resetreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="8e259-148">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="8e259-148">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

