---
description: Modifica as configurações de replicação para uma máquina virtual. Quando um cliente chama esse método para uma máquina virtual de réplica, ele modifica as configurações de replicação do relacionamento de replicação com a réplica estendida.
ms.assetid: e68514a5-f508-4047-8dcc-6a95f3e3353e
title: Método ModifyReplicationSettings da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyReplicationSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d1c932f06350324e0d84559724f7ba0412dfb3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760858"
---
# <a name="modifyreplicationsettings-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="e70f5-104">Método ModifyReplicationSettings da \_ classe ReplicationService Msvm</span><span class="sxs-lookup"><span data-stu-id="e70f5-104">ModifyReplicationSettings method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="e70f5-105">Modifica as configurações de replicação para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70f5-105">Modifies the replication settings for a virtual machine.</span></span> <span data-ttu-id="e70f5-106">Quando um cliente chama esse método para uma máquina virtual de réplica, ele modifica as configurações de replicação do relacionamento de replicação com a réplica estendida.</span><span class="sxs-lookup"><span data-stu-id="e70f5-106">When a client calls this method for a replica virtual machine, it modifies the replication settings of the replication relationship with the extended replica.</span></span>

## <a name="syntax"></a><span data-ttu-id="e70f5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e70f5-107">Syntax</span></span>


```mof
uint32 ModifyReplicationSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e70f5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e70f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e70f5-109">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e70f5-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e70f5-110">Uma referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual para a qual as configurações de replicação devem ser modificadas.</span><span class="sxs-lookup"><span data-stu-id="e70f5-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication settings should be modified.</span></span>

</dd> <dt>

<span data-ttu-id="e70f5-111">*ReplicationSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e70f5-111">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e70f5-112">Uma representação de cadeia de caracteres da classe [**Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) que define as novas configurações de replicação.</span><span class="sxs-lookup"><span data-stu-id="e70f5-112">A string representation of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the new replication settings.</span></span>

</dd> <dt>

<span data-ttu-id="e70f5-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="e70f5-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e70f5-114">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e70f5-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e70f5-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e70f5-115">Return value</span></span>

<span data-ttu-id="e70f5-116">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e70f5-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e70f5-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="e70f5-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e70f5-118">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="e70f5-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e70f5-119">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="e70f5-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e70f5-120">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="e70f5-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e70f5-121">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="e70f5-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e70f5-122">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="e70f5-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e70f5-123">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="e70f5-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e70f5-124">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e70f5-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e70f5-125">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e70f5-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e70f5-126">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="e70f5-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e70f5-127">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e70f5-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e70f5-128">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="e70f5-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e70f5-129">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e70f5-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="e70f5-130">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="e70f5-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e70f5-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="e70f5-131">Remarks</span></span>

<span data-ttu-id="e70f5-132">**ModifyReplicationSettings** usa uma FRSD (instância [**\_ ReplicationSettingData Msvm**](msvm-replicationsettingdata.md) ) como entrada.</span><span class="sxs-lookup"><span data-stu-id="e70f5-132">**ModifyReplicationSettings** takes an [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) instance (FRSD) as input.</span></span> <span data-ttu-id="e70f5-133">O FRSD associado para a máquina virtual como o provedor host-to-host é a opção padrão.</span><span class="sxs-lookup"><span data-stu-id="e70f5-133">The associated FRSD for the virtual machine as host-to-host provider is the default choice.</span></span> <span data-ttu-id="e70f5-134">O FRSD de entrada é validado para configurações válidas para cada propriedade para o provedor padrão.</span><span class="sxs-lookup"><span data-stu-id="e70f5-134">Input FRSD is validated for valid settings for each property for the default provider.</span></span> <span data-ttu-id="e70f5-135">Esta tabela resume as diferenças de validação em relação ao provedor externo.</span><span class="sxs-lookup"><span data-stu-id="e70f5-135">This table summarizes the validation differences with respect to the external provider.</span></span>



| <span data-ttu-id="e70f5-136">Propriedade</span><span class="sxs-lookup"><span data-stu-id="e70f5-136">Property</span></span>                                             | <span data-ttu-id="e70f5-137">Provedores externos</span><span class="sxs-lookup"><span data-stu-id="e70f5-137">External providers</span></span>                                 |
|------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="e70f5-138">Replicationprovider</span><span class="sxs-lookup"><span data-stu-id="e70f5-138">ReplicationProvider</span></span>                                  | <span data-ttu-id="e70f5-139">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="e70f5-139">Same as default provider</span></span>                           |
| <span data-ttu-id="e70f5-140">AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="e70f5-140">AuthenticationType</span></span>                                   | <span data-ttu-id="e70f5-141">Ignored</span><span class="sxs-lookup"><span data-stu-id="e70f5-141">Ignored</span></span>                                            |
| <span data-ttu-id="e70f5-142">CertificateThumbPrint</span><span class="sxs-lookup"><span data-stu-id="e70f5-142">CertificateThumbPrint</span></span>                                | <span data-ttu-id="e70f5-143">Ignored</span><span class="sxs-lookup"><span data-stu-id="e70f5-143">Ignored</span></span>                                            |
| <span data-ttu-id="e70f5-144">RootCertificateThumbPrint (RO)</span><span class="sxs-lookup"><span data-stu-id="e70f5-144">RootCertificateThumbPrint (RO)</span></span>                       | <span data-ttu-id="e70f5-145">Ignored</span><span class="sxs-lookup"><span data-stu-id="e70f5-145">Ignored</span></span>                                            |
| <span data-ttu-id="e70f5-146">CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="e70f5-146">CompressionEnabled</span></span>                                   | <span data-ttu-id="e70f5-147">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="e70f5-147">Same as default provider</span></span>                           |
| <span data-ttu-id="e70f5-148">BypassProxyServer</span><span class="sxs-lookup"><span data-stu-id="e70f5-148">BypassProxyServer</span></span>                                    | <span data-ttu-id="e70f5-149">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="e70f5-149">Same as default provider</span></span>                           |
| <span data-ttu-id="e70f5-150">RecoveryConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="e70f5-150">RecoveryConnectionPoint</span></span>                              | <span data-ttu-id="e70f5-151">Ignorado \* (pode alterar se o provedor tiver requisito)</span><span class="sxs-lookup"><span data-stu-id="e70f5-151">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="e70f5-152">RecoveryHostSystem (RO)</span><span class="sxs-lookup"><span data-stu-id="e70f5-152">RecoveryHostSystem (RO)</span></span>                              | <span data-ttu-id="e70f5-153">Ignored</span><span class="sxs-lookup"><span data-stu-id="e70f5-153">Ignored</span></span>                                            |
| <span data-ttu-id="e70f5-154">PrimaryConnectionPoint (RO)</span><span class="sxs-lookup"><span data-stu-id="e70f5-154">PrimaryConnectionPoint (RO)</span></span>                          | <span data-ttu-id="e70f5-155">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="e70f5-155">Same as default provider</span></span>                           |
| <span data-ttu-id="e70f5-156">PrimaryHostSystem (RO)</span><span class="sxs-lookup"><span data-stu-id="e70f5-156">PrimaryHostSystem (RO)</span></span>                               | <span data-ttu-id="e70f5-157">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="e70f5-157">Same as default provider</span></span>                           |
| <span data-ttu-id="e70f5-158">RecoveryServerPortNumber</span><span class="sxs-lookup"><span data-stu-id="e70f5-158">RecoveryServerPortNumber</span></span>                             | <span data-ttu-id="e70f5-159">Ignorado \* (pode alterar se o provedor tiver requisito)</span><span class="sxs-lookup"><span data-stu-id="e70f5-159">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="e70f5-160">ReplicateHostKvpItems</span><span class="sxs-lookup"><span data-stu-id="e70f5-160">ReplicateHostKvpItems</span></span>                                | <span data-ttu-id="e70f5-161">Ignored</span><span class="sxs-lookup"><span data-stu-id="e70f5-161">Ignored</span></span>                                            |
| <span data-ttu-id="e70f5-162">ApplicationConsistentSnapshotInterval</span><span class="sxs-lookup"><span data-stu-id="e70f5-162">ApplicationConsistentSnapshotInterval</span></span>                | <span data-ttu-id="e70f5-163">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="e70f5-163">Same as default provider</span></span>                           |
| <span data-ttu-id="e70f5-164">RecoveryHistory</span><span class="sxs-lookup"><span data-stu-id="e70f5-164">RecoveryHistory</span></span>                                      | <span data-ttu-id="e70f5-165">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="e70f5-165">Same as default provider</span></span>                           |
| <span data-ttu-id="e70f5-166">IncludedDisks\[\]</span><span class="sxs-lookup"><span data-stu-id="e70f5-166">IncludedDisks\[\]</span></span>                                    | <span data-ttu-id="e70f5-167">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="e70f5-167">Same as default provider</span></span>                           |
| <span data-ttu-id="e70f5-168">AutoResynchronizeEnabled</span><span class="sxs-lookup"><span data-stu-id="e70f5-168">AutoResynchronizeEnabled</span></span>                             | <span data-ttu-id="e70f5-169">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="e70f5-169">Same as default provider</span></span>                           |
| <span data-ttu-id="e70f5-170">AutoResynchronizeIntervalStart</span><span class="sxs-lookup"><span data-stu-id="e70f5-170">AutoResynchronizeIntervalStart</span></span>                       | <span data-ttu-id="e70f5-171">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="e70f5-171">Same as default provider</span></span>                           |
| <span data-ttu-id="e70f5-172">AutoResynchronizeIntervalEnd</span><span class="sxs-lookup"><span data-stu-id="e70f5-172">AutoResynchronizeIntervalEnd</span></span>                         | <span data-ttu-id="e70f5-173">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="e70f5-173">Same as default provider</span></span>                           |
| <span data-ttu-id="e70f5-174">EnableWriteOrderPreservationAcrossDisks (preterido)</span><span class="sxs-lookup"><span data-stu-id="e70f5-174">EnableWriteOrderPreservationAcrossDisks (Deprecated)</span></span> | <span data-ttu-id="e70f5-175">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="e70f5-175">Same as default provider</span></span>                           |
| <span data-ttu-id="e70f5-176">ReplicationInterval</span><span class="sxs-lookup"><span data-stu-id="e70f5-176">ReplicationInterval</span></span>                                  | <span data-ttu-id="e70f5-177">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="e70f5-177">Same as default provider</span></span>                           |



 

## <a name="requirements"></a><span data-ttu-id="e70f5-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e70f5-178">Requirements</span></span>



| <span data-ttu-id="e70f5-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="e70f5-179">Requirement</span></span> | <span data-ttu-id="e70f5-180">Valor</span><span class="sxs-lookup"><span data-stu-id="e70f5-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e70f5-181">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e70f5-181">Minimum supported client</span></span><br/> | <span data-ttu-id="e70f5-182">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e70f5-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e70f5-183">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e70f5-183">Minimum supported server</span></span><br/> | <span data-ttu-id="e70f5-184">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e70f5-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e70f5-185">Namespace</span><span class="sxs-lookup"><span data-stu-id="e70f5-185">Namespace</span></span><br/>                | <span data-ttu-id="e70f5-186">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e70f5-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e70f5-187">MOF</span><span class="sxs-lookup"><span data-stu-id="e70f5-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e70f5-188"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e70f5-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e70f5-189">DLL</span><span class="sxs-lookup"><span data-stu-id="e70f5-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e70f5-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e70f5-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e70f5-191">Confira também</span><span class="sxs-lookup"><span data-stu-id="e70f5-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e70f5-192">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="e70f5-192">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

