---
description: Inicia a replicação de uma máquina virtual.
ms.assetid: 58e89329-1ad4-4473-856d-ebfd7a863fa8
title: Método StartReplication da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.StartReplication
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4702b5b73a989e2889bf1da9e4d284afdfe5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296281"
---
# <a name="startreplication-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="ed925-103">Método StartReplication da \_ classe ReplicationService Msvm</span><span class="sxs-lookup"><span data-stu-id="ed925-103">StartReplication method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="ed925-104">Inicia a replicação de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ed925-104">Starts the replication of a virtual machine.</span></span> <span data-ttu-id="ed925-105">Quando um cliente chama esse método para uma máquina virtual de réplica, ele inicia a replicação com a réplica estendida.</span><span class="sxs-lookup"><span data-stu-id="ed925-105">When a client calls this method for a replica virtual machine, it starts the replication with extended replica.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed925-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed925-106">Syntax</span></span>


```mof
uint32 StartReplication(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  uint16                 InitialReplicationType,
  [in]  string                 InitialReplicationExportLocation,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ed925-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed925-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed925-108">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ed925-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed925-109">Uma referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual para a qual a replicação deve ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="ed925-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be started.</span></span>

</dd> <dt>

<span data-ttu-id="ed925-110">*InitialReplicationType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ed925-110">*InitialReplicationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed925-111">O tipo de transferência a ser usado para executar a replicação inicial.</span><span class="sxs-lookup"><span data-stu-id="ed925-111">The type of transfer to be used for performing the initial replication.</span></span>

<dt>

<span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>

<span data-ttu-id="ed925-112"><span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>**Transferência de rede** (1)</span><span class="sxs-lookup"><span data-stu-id="ed925-112"><span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>**Network Transfer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ed925-113">Transferência de rede.</span><span class="sxs-lookup"><span data-stu-id="ed925-113">Network transfer.</span></span>

</dd> <dt>

<span id="Export"></span><span id="export"></span><span id="EXPORT"></span>

<span data-ttu-id="ed925-114"><span id="Export"></span><span id="export"></span><span id="EXPORT"></span>**Exportar** (2)</span><span class="sxs-lookup"><span data-stu-id="ed925-114"><span id="Export"></span><span id="export"></span><span id="EXPORT"></span>**Export** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ed925-115">Exportar.</span><span class="sxs-lookup"><span data-stu-id="ed925-115">Export.</span></span>

</dd> <dt>

<span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>

<span data-ttu-id="ed925-116"><span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**Transferência de rede propagada** (3)</span><span class="sxs-lookup"><span data-stu-id="ed925-116"><span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**Seeded Network Transfer** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ed925-117">Transferência de rede propagada.</span><span class="sxs-lookup"><span data-stu-id="ed925-117">Seeded network transfer.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ed925-118">*InitialReplicationExportLocation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ed925-118">*InitialReplicationExportLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed925-119">Se *InitialReplicationType* for 2 (Export), esse parâmetro conterá o caminho totalmente qualificado do diretório no qual a replicação inicial será exportada.</span><span class="sxs-lookup"><span data-stu-id="ed925-119">If *InitialReplicationType* is 2 (Export), this parameter contains the fully qualified path of the directory to which the initial replication is to be exported.</span></span> <span data-ttu-id="ed925-120">Esse parâmetro não é usado para outros valores de *InitialReplicationType* e pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ed925-120">This parameter is not used for other values of *InitialReplicationType*, and can be **Null**.</span></span> <span data-ttu-id="ed925-121">Esse diretório pode ser reutilizado para exportar várias replicações de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ed925-121">This directory can be reused for exporting multiple virtual machine replication.</span></span> <span data-ttu-id="ed925-122">Esse método coloca cada replicação de máquina virtual em um subdiretório separado sob esse caminho.</span><span class="sxs-lookup"><span data-stu-id="ed925-122">This method places each virtual machine replication in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="ed925-123">*StartTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ed925-123">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed925-124">A hora de início agendada para a replicação inicial na conexão de rede com o servidor de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ed925-124">The scheduled start time for the initial replication over the network connection to recovery server.</span></span> <span data-ttu-id="ed925-125">Esse parâmetro é ignorado quando *InitialReplicationType* é 2 (Export).</span><span class="sxs-lookup"><span data-stu-id="ed925-125">This parameter is ignored when *InitialReplicationType* is 2 (Export).</span></span> <span data-ttu-id="ed925-126">Se esse parâmetro for **nulo**, a replicação inicial será iniciada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="ed925-126">If this parameter is **Null**, the initial replication starts immediately.</span></span>

</dd> <dt>

<span data-ttu-id="ed925-127">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="ed925-127">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed925-128">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ed925-128">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed925-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed925-129">Return value</span></span>

<span data-ttu-id="ed925-130">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed925-130">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ed925-131">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="ed925-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ed925-132">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="ed925-132">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ed925-133">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="ed925-133">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ed925-134">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="ed925-134">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ed925-135">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="ed925-135">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ed925-136">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="ed925-136">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ed925-137">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="ed925-137">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ed925-138">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="ed925-138">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ed925-139">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="ed925-139">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ed925-140">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="ed925-140">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ed925-141">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="ed925-141">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ed925-142">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="ed925-142">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ed925-143">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="ed925-143">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="ed925-144">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="ed925-144">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ed925-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed925-145">Requirements</span></span>



| <span data-ttu-id="ed925-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed925-146">Requirement</span></span> | <span data-ttu-id="ed925-147">Valor</span><span class="sxs-lookup"><span data-stu-id="ed925-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed925-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed925-148">Minimum supported client</span></span><br/> | <span data-ttu-id="ed925-149">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ed925-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ed925-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed925-150">Minimum supported server</span></span><br/> | <span data-ttu-id="ed925-151">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ed925-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ed925-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed925-152">Namespace</span></span><br/>                | <span data-ttu-id="ed925-153">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ed925-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ed925-154">MOF</span><span class="sxs-lookup"><span data-stu-id="ed925-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed925-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed925-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed925-156">DLL</span><span class="sxs-lookup"><span data-stu-id="ed925-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed925-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ed925-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ed925-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed925-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed925-159">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="ed925-159">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

