---
description: Cria um novo relacionamento de replicação para uma máquina virtual. Quando um cliente chama esse método para uma máquina virtual de réplica, ele estende a relação de replicação para o provedor especificado.
ms.assetid: 44d3b5aa-46c2-4fe9-9a1d-6ee699d3640d
title: Método CreateReplicationRelationship da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.CreateReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c44628aef9aa278170a1292a74621419bb6256b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780539"
---
# <a name="createreplicationrelationship-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="67040-104">Método CreateReplicationRelationship da \_ classe ReplicationService Msvm</span><span class="sxs-lookup"><span data-stu-id="67040-104">CreateReplicationRelationship method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="67040-105">Cria um novo relacionamento de replicação para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="67040-105">Creates a new replication relationship for a virtual machine.</span></span> <span data-ttu-id="67040-106">Quando um cliente chama esse método para uma máquina virtual de réplica, ele estende a relação de replicação para o provedor especificado.</span><span class="sxs-lookup"><span data-stu-id="67040-106">When a client calls this method for a replica virtual machine, it extends the replication relationship to the specified provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="67040-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67040-107">Syntax</span></span>


```mof
uint32 CreateReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="67040-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67040-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67040-109">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="67040-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67040-110">Uma referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual para a qual a replicação deve ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="67040-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="67040-111">*ReplicationSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="67040-111">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67040-112">Uma representação de cadeia de caracteres de uma instância da classe [**Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) que define as configurações de replicação para a nova relação de replicação a ser criada para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="67040-112">A string representation of an instance of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the replication settings for the new replication relationship to be created for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="67040-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="67040-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67040-114">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="67040-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67040-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="67040-115">Return value</span></span>

<span data-ttu-id="67040-116">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="67040-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="67040-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="67040-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="67040-118">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="67040-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="67040-119">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="67040-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="67040-120">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="67040-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="67040-121">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="67040-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="67040-122">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="67040-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="67040-123">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="67040-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="67040-124">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="67040-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="67040-125">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="67040-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="67040-126">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="67040-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="67040-127">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="67040-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="67040-128">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="67040-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="67040-129">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="67040-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="67040-130">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="67040-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="67040-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="67040-131">Remarks</span></span>

<span data-ttu-id="67040-132">**CreateReplicationRelationship** usa uma FRSD (instância [**\_ ReplicationSettingData Msvm**](msvm-replicationsettingdata.md) ) como entrada.</span><span class="sxs-lookup"><span data-stu-id="67040-132">**CreateReplicationRelationship** takes an [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) instance (FRSD) as input.</span></span> <span data-ttu-id="67040-133">O FRSD associado para a máquina virtual como o provedor host-to-host é a opção padrão.</span><span class="sxs-lookup"><span data-stu-id="67040-133">The associated FRSD for the virtual machine as host-to-host provider is the default choice.</span></span> <span data-ttu-id="67040-134">O FRSD de entrada é validado para configurações válidas para cada propriedade para o provedor padrão.</span><span class="sxs-lookup"><span data-stu-id="67040-134">Input FRSD is validated for valid settings for each property for the default provider.</span></span> <span data-ttu-id="67040-135">Esta tabela resume as diferenças de validação em relação ao provedor externo.</span><span class="sxs-lookup"><span data-stu-id="67040-135">This table summarizes the validation differences with respect to the external provider.</span></span>



| <span data-ttu-id="67040-136">Propriedade</span><span class="sxs-lookup"><span data-stu-id="67040-136">Property</span></span>                                             | <span data-ttu-id="67040-137">Provedores externos</span><span class="sxs-lookup"><span data-stu-id="67040-137">External providers</span></span>                                 |
|------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="67040-138">Replicationprovider</span><span class="sxs-lookup"><span data-stu-id="67040-138">ReplicationProvider</span></span>                                  | <span data-ttu-id="67040-139">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="67040-139">Same as default provider</span></span>                           |
| <span data-ttu-id="67040-140">AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="67040-140">AuthenticationType</span></span>                                   | <span data-ttu-id="67040-141">Ignored</span><span class="sxs-lookup"><span data-stu-id="67040-141">Ignored</span></span>                                            |
| <span data-ttu-id="67040-142">CertificateThumbPrint</span><span class="sxs-lookup"><span data-stu-id="67040-142">CertificateThumbPrint</span></span>                                | <span data-ttu-id="67040-143">Ignored</span><span class="sxs-lookup"><span data-stu-id="67040-143">Ignored</span></span>                                            |
| <span data-ttu-id="67040-144">RootCertificateThumbPrint (RO)</span><span class="sxs-lookup"><span data-stu-id="67040-144">RootCertificateThumbPrint (RO)</span></span>                       | <span data-ttu-id="67040-145">Ignored</span><span class="sxs-lookup"><span data-stu-id="67040-145">Ignored</span></span>                                            |
| <span data-ttu-id="67040-146">CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="67040-146">CompressionEnabled</span></span>                                   | <span data-ttu-id="67040-147">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="67040-147">Same as default provider</span></span>                           |
| <span data-ttu-id="67040-148">BypassProxyServer</span><span class="sxs-lookup"><span data-stu-id="67040-148">BypassProxyServer</span></span>                                    | <span data-ttu-id="67040-149">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="67040-149">Same as default provider</span></span>                           |
| <span data-ttu-id="67040-150">RecoveryConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="67040-150">RecoveryConnectionPoint</span></span>                              | <span data-ttu-id="67040-151">Ignorado \* (pode alterar se o provedor tiver requisito)</span><span class="sxs-lookup"><span data-stu-id="67040-151">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="67040-152">RecoveryHostSystem (RO)</span><span class="sxs-lookup"><span data-stu-id="67040-152">RecoveryHostSystem (RO)</span></span>                              | <span data-ttu-id="67040-153">Ignored</span><span class="sxs-lookup"><span data-stu-id="67040-153">Ignored</span></span>                                            |
| <span data-ttu-id="67040-154">PrimaryConnectionPoint (RO)</span><span class="sxs-lookup"><span data-stu-id="67040-154">PrimaryConnectionPoint (RO)</span></span>                          | <span data-ttu-id="67040-155">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="67040-155">Same as default provider</span></span>                           |
| <span data-ttu-id="67040-156">PrimaryHostSystem (RO)</span><span class="sxs-lookup"><span data-stu-id="67040-156">PrimaryHostSystem (RO)</span></span>                               | <span data-ttu-id="67040-157">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="67040-157">Same as default provider</span></span>                           |
| <span data-ttu-id="67040-158">RecoveryServerPortNumber</span><span class="sxs-lookup"><span data-stu-id="67040-158">RecoveryServerPortNumber</span></span>                             | <span data-ttu-id="67040-159">Ignorado \* (pode alterar se o provedor tiver requisito)</span><span class="sxs-lookup"><span data-stu-id="67040-159">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="67040-160">ReplicateHostKvpItems</span><span class="sxs-lookup"><span data-stu-id="67040-160">ReplicateHostKvpItems</span></span>                                | <span data-ttu-id="67040-161">Ignored</span><span class="sxs-lookup"><span data-stu-id="67040-161">Ignored</span></span>                                            |
| <span data-ttu-id="67040-162">ApplicationConsistentSnapshotInterval</span><span class="sxs-lookup"><span data-stu-id="67040-162">ApplicationConsistentSnapshotInterval</span></span>                | <span data-ttu-id="67040-163">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="67040-163">Same as default provider</span></span>                           |
| <span data-ttu-id="67040-164">RecoveryHistory</span><span class="sxs-lookup"><span data-stu-id="67040-164">RecoveryHistory</span></span>                                      | <span data-ttu-id="67040-165">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="67040-165">Same as default provider</span></span>                           |
| <span data-ttu-id="67040-166">IncludedDisks\[\]</span><span class="sxs-lookup"><span data-stu-id="67040-166">IncludedDisks\[\]</span></span>                                    | <span data-ttu-id="67040-167">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="67040-167">Same as default provider</span></span>                           |
| <span data-ttu-id="67040-168">AutoResynchronizeEnabled</span><span class="sxs-lookup"><span data-stu-id="67040-168">AutoResynchronizeEnabled</span></span>                             | <span data-ttu-id="67040-169">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="67040-169">Same as default provider</span></span>                           |
| <span data-ttu-id="67040-170">AutoResynchronizeIntervalStart</span><span class="sxs-lookup"><span data-stu-id="67040-170">AutoResynchronizeIntervalStart</span></span>                       | <span data-ttu-id="67040-171">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="67040-171">Same as default provider</span></span>                           |
| <span data-ttu-id="67040-172">AutoResynchronizeIntervalEnd</span><span class="sxs-lookup"><span data-stu-id="67040-172">AutoResynchronizeIntervalEnd</span></span>                         | <span data-ttu-id="67040-173">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="67040-173">Same as default provider</span></span>                           |
| <span data-ttu-id="67040-174">EnableWriteOrderPreservationAcrossDisks (preterido)</span><span class="sxs-lookup"><span data-stu-id="67040-174">EnableWriteOrderPreservationAcrossDisks (Deprecated)</span></span> | <span data-ttu-id="67040-175">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="67040-175">Same as default provider</span></span>                           |
| <span data-ttu-id="67040-176">ReplicationInterval</span><span class="sxs-lookup"><span data-stu-id="67040-176">ReplicationInterval</span></span>                                  | <span data-ttu-id="67040-177">Mesmo que o provedor padrão</span><span class="sxs-lookup"><span data-stu-id="67040-177">Same as default provider</span></span>                           |



 

## <a name="requirements"></a><span data-ttu-id="67040-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67040-178">Requirements</span></span>



| <span data-ttu-id="67040-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="67040-179">Requirement</span></span> | <span data-ttu-id="67040-180">Valor</span><span class="sxs-lookup"><span data-stu-id="67040-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67040-181">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67040-181">Minimum supported client</span></span><br/> | <span data-ttu-id="67040-182">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="67040-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="67040-183">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67040-183">Minimum supported server</span></span><br/> | <span data-ttu-id="67040-184">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="67040-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="67040-185">Namespace</span><span class="sxs-lookup"><span data-stu-id="67040-185">Namespace</span></span><br/>                | <span data-ttu-id="67040-186">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="67040-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="67040-187">MOF</span><span class="sxs-lookup"><span data-stu-id="67040-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67040-188"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67040-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="67040-189">DLL</span><span class="sxs-lookup"><span data-stu-id="67040-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67040-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="67040-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="67040-191">Confira também</span><span class="sxs-lookup"><span data-stu-id="67040-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67040-192">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="67040-192">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="67040-193">**RemoveReplicationRelationshipEx**</span><span class="sxs-lookup"><span data-stu-id="67040-193">**RemoveReplicationRelationshipEx**</span></span>](removereplicationrelationshipex-msvm-replicationservice.md)
</dt> </dl>

 

