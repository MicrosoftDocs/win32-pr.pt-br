---
description: Representa uma coleção de sistemas virtuais.
ms.assetid: acf51beb-1103-43a4-8dc5-1a7f2a0482be
title: Classe Msvm_VirtualSystemCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemCollection
- Msvm_VirtualSystemCollection.CollectionID
- Msvm_VirtualSystemCollection.ElementName
- Msvm_VirtualSystemCollection.LastApplyConsistencyLevel
- Msvm_VirtualSystemCollection.LastApplyVirtualMachineIds
- Msvm_VirtualSystemCollection.LastApplyTime
- Msvm_VirtualSystemCollection.FailedOverReplicationType
- Msvm_VirtualSystemCollection.ReplicationMode
- Msvm_VirtualSystemCollection.ReplicationState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a9746356744f2743a8d6656ef4c61044223be113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370602"
---
# <a name="msvm_virtualsystemcollection-class"></a><span data-ttu-id="cd422-103">\_Classe Msvm VirtualSystemCollection</span><span class="sxs-lookup"><span data-stu-id="cd422-103">Msvm\_VirtualSystemCollection class</span></span>

<span data-ttu-id="cd422-104">Representa uma coleção de sistemas virtuais.</span><span class="sxs-lookup"><span data-stu-id="cd422-104">Represents a collection of virtual systems.</span></span>

<span data-ttu-id="cd422-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="cd422-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd422-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd422-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemCollection : CIM_CollectionOfMSEs
{
  string   CollectionID;
  string   ElementName;
  uint16   LastApplyConsistencyLevel;
  String   LastApplyVirtualMachineIds[];
  DateTime LastApplyTime;
  uint16   FailedOverReplicationType;
  uint16   ReplicationMode;
  uint16   ReplicationState;
};
```

## <a name="members"></a><span data-ttu-id="cd422-107">Membros</span><span class="sxs-lookup"><span data-stu-id="cd422-107">Members</span></span>

<span data-ttu-id="cd422-108">A classe **Msvm \_ VirtualSystemCollection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cd422-108">The **Msvm\_VirtualSystemCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="cd422-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cd422-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd422-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cd422-110">Properties</span></span>

<span data-ttu-id="cd422-111">A classe **Msvm \_ VirtualSystemCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cd422-111">The **Msvm\_VirtualSystemCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd422-112">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="cd422-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd422-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd422-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd422-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd422-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd422-115">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionId"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cd422-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cd422-116">A identificação exclusiva do objeto de coleção.</span><span class="sxs-lookup"><span data-stu-id="cd422-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="cd422-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="cd422-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd422-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd422-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd422-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd422-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd422-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="cd422-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="cd422-121">Um nome definido pelo usuário para a coleção.</span><span class="sxs-lookup"><span data-stu-id="cd422-121">An user-defined name for the collection.</span></span> <span data-ttu-id="cd422-122">Observe que isso não é garantido como exclusivo.</span><span class="sxs-lookup"><span data-stu-id="cd422-122">Note this is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="cd422-123">**FailedOverReplicationType**</span><span class="sxs-lookup"><span data-stu-id="cd422-123">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd422-124">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd422-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd422-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd422-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd422-126">Tipo de failover que foi executado para a coleção do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="cd422-126">Type of failover that was performed for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="cd422-127">Adicionado no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="cd422-127">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="cd422-128">**Nenhum** (0)</span><span class="sxs-lookup"><span data-stu-id="cd422-128">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="cd422-129">**Regular** (1)</span><span class="sxs-lookup"><span data-stu-id="cd422-129">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="cd422-130">**Planejado** (2)</span><span class="sxs-lookup"><span data-stu-id="cd422-130">**Planned** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cd422-131">**LastApplyConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="cd422-131">**LastApplyConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd422-132">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd422-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd422-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd422-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd422-134">Nível de consistência do último Delta aplicado.</span><span class="sxs-lookup"><span data-stu-id="cd422-134">Consistency level of the last applied delta.</span></span>

> [!Note]  
> <span data-ttu-id="cd422-135">Adicionado no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="cd422-135">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cd422-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="cd422-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="cd422-137"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Consistente** com o aplicativo (1)</span><span class="sxs-lookup"><span data-stu-id="cd422-137"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="cd422-138">O último Delta aplicado indica um ponto no tempo em que o sistema virtual estava no estado consistente do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cd422-138">The last applied delta indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="cd422-139"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Falha consistente** (2)</span><span class="sxs-lookup"><span data-stu-id="cd422-139"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cd422-140">O último Delta aplicado indica um ponto no tempo em que o sistema virtual estava em estado consistente de falha.</span><span class="sxs-lookup"><span data-stu-id="cd422-140">The last applied delta indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>

<span data-ttu-id="cd422-141"><span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>**Falha de grupo consistente** (3)</span><span class="sxs-lookup"><span data-stu-id="cd422-141"><span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>**Group Crash Consistent** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cd422-142">O último Delta aplicado indica um ponto no tempo em que o grupo estava em estado de falha consistente.</span><span class="sxs-lookup"><span data-stu-id="cd422-142">The last applied delta indicates a point in time when the group was in crash consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cd422-143">**LastApplyTime**</span><span class="sxs-lookup"><span data-stu-id="cd422-143">**LastApplyTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd422-144">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd422-144">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="cd422-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd422-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd422-146">A hora em que a última replicação é aplicada na recuperação para a coleção do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="cd422-146">The time at which the last replication is applied on recovery for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="cd422-147">Adicionado no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="cd422-147">Added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="cd422-148">**LastApplyVirtualMachineIds**</span><span class="sxs-lookup"><span data-stu-id="cd422-148">**LastApplyVirtualMachineIds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd422-149">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd422-149">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="cd422-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd422-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd422-151">Matriz de IDs de máquina virtual que foram aplicadas com êxito no último ciclo de aplicação.</span><span class="sxs-lookup"><span data-stu-id="cd422-151">Array of Virtual Machine Ids which were successfully applied in last apply cycle.</span></span>

> [!Note]  
> <span data-ttu-id="cd422-152">Adicionado no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="cd422-152">Added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="cd422-153">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="cd422-153">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd422-154">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd422-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd422-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd422-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd422-156">Tipo de replicação para a coleção do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="cd422-156">Replication type for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="cd422-157">Adicionado no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="cd422-157">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="cd422-158">**Nenhum** (0)</span><span class="sxs-lookup"><span data-stu-id="cd422-158">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="cd422-159">**Primário** (1)</span><span class="sxs-lookup"><span data-stu-id="cd422-159">**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="cd422-160">**Réplica** (2)</span><span class="sxs-lookup"><span data-stu-id="cd422-160">**Replica** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="cd422-161">**Réplica de teste** (3)</span><span class="sxs-lookup"><span data-stu-id="cd422-161">**Test Replica** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cd422-162">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="cd422-162">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd422-163">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd422-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd422-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd422-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd422-165">Estado de replicação para a coleção do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="cd422-165">Replication state for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="cd422-166">Adicionado no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="cd422-166">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="cd422-167">**Desabilitado** (0)</span><span class="sxs-lookup"><span data-stu-id="cd422-167">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="cd422-168">**Pronto para replicação** (1)</span><span class="sxs-lookup"><span data-stu-id="cd422-168">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="cd422-169">**Aguardando para concluir a replicação inicial** (2)</span><span class="sxs-lookup"><span data-stu-id="cd422-169">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="cd422-170">**Replicando** (3)</span><span class="sxs-lookup"><span data-stu-id="cd422-170">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_initiated"></span><span id="failover_initiated"></span><span id="FAILOVER_INITIATED"></span>

<span data-ttu-id="cd422-171">**Failover iniciado** (4)</span><span class="sxs-lookup"><span data-stu-id="cd422-171">**Failover initiated** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="cd422-172">**Recuperado** (5)</span><span class="sxs-lookup"><span data-stu-id="cd422-172">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="cd422-173">**Confirmado** (6)</span><span class="sxs-lookup"><span data-stu-id="cd422-173">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="cd422-174">**Suspenso** (7)</span><span class="sxs-lookup"><span data-stu-id="cd422-174">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="cd422-175">**Crítico** (8)</span><span class="sxs-lookup"><span data-stu-id="cd422-175">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="cd422-176">**Aguardando para iniciar a ressincronização** (9)</span><span class="sxs-lookup"><span data-stu-id="cd422-176">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="cd422-177">**Ressincronização** (10)</span><span class="sxs-lookup"><span data-stu-id="cd422-177">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned_failover_initiatedRepurpose_initiatedTest_failover_initiatedPartially_enabled"></span><span id="planned_failover_initiatedrepurpose_initiatedtest_failover_initiatedpartially_enabled"></span><span id="PLANNED_FAILOVER_INITIATEDREPURPOSE_INITIATEDTEST_FAILOVER_INITIATEDPARTIALLY_ENABLED"></span>

<span data-ttu-id="cd422-178">Failover **planejado InitiatedRepurpose initiatedTest failover initiatedPartially habilitado** (11)</span><span class="sxs-lookup"><span data-stu-id="cd422-178">**Planned failover initiatedRepurpose initiatedTest failover initiatedPartially enabled** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_disabled"></span><span id="partially_disabled"></span><span id="PARTIALLY_DISABLED"></span>

<span data-ttu-id="cd422-179">**Parcialmente desabilitado** (12)</span><span class="sxs-lookup"><span data-stu-id="cd422-179">**Partially disabled** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_recovered"></span><span id="partially_recovered"></span><span id="PARTIALLY_RECOVERED"></span>

<span data-ttu-id="cd422-180">**Parcialmente recuperado** (13)</span><span class="sxs-lookup"><span data-stu-id="cd422-180">**Partially recovered** (13)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cd422-181">(14)</span><span class="sxs-lookup"><span data-stu-id="cd422-181">(14)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cd422-182">(15)</span><span class="sxs-lookup"><span data-stu-id="cd422-182">(15)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cd422-183">(16)</span><span class="sxs-lookup"><span data-stu-id="cd422-183">(16)</span></span>


<span data-ttu-id="cd422-184"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cd422-184"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="cd422-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd422-185">Requirements</span></span>



| <span data-ttu-id="cd422-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd422-186">Requirement</span></span> | <span data-ttu-id="cd422-187">Valor</span><span class="sxs-lookup"><span data-stu-id="cd422-187">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd422-188">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd422-188">Minimum supported client</span></span><br/> | <span data-ttu-id="cd422-189">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="cd422-189">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="cd422-190">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd422-190">Minimum supported server</span></span><br/> | <span data-ttu-id="cd422-191">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cd422-191">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="cd422-192">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd422-192">Namespace</span></span><br/>                | <span data-ttu-id="cd422-193">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="cd422-193">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cd422-194">MOF</span><span class="sxs-lookup"><span data-stu-id="cd422-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd422-195"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd422-195"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd422-196">DLL</span><span class="sxs-lookup"><span data-stu-id="cd422-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd422-197"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cd422-197"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cd422-198">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd422-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd422-199">**CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="cd422-199">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> </dl>

 

