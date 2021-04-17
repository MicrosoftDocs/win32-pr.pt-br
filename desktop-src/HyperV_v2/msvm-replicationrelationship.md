---
description: Representa o status de replicação para um relacionamento de replicação.
ms.assetid: F11EFF86-5CC9-4310-8254-B310C54B561D
title: Classe Msvm_ReplicationRelationship
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationRelationship
- Msvm_ReplicationRelationship.InstanceID
- Msvm_ReplicationRelationship.ReplicationState
- Msvm_ReplicationRelationship.ReplicationHealth
- Msvm_ReplicationRelationship.FailedOverReplicationType
- Msvm_ReplicationRelationship.LastReplicationType
- Msvm_ReplicationRelationship.LastApplicationConsistentReplicationTime
- Msvm_ReplicationRelationship.LastReplicationTime
- Msvm_ReplicationRelationship.LastApplyTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04665f96f4ec77501ee0b161d816c84943ca2c98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748177"
---
# <a name="msvm_replicationrelationship-class"></a><span data-ttu-id="1c6f6-103">\_Classe Msvm ReplicationRelationship</span><span class="sxs-lookup"><span data-stu-id="1c6f6-103">Msvm\_ReplicationRelationship class</span></span>

<span data-ttu-id="1c6f6-104">Representa o status de replicação para um relacionamento de replicação.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-104">Represents replication status for a replication relationship.</span></span> <span data-ttu-id="1c6f6-105">Como você pode ter várias replicações para cada máquina virtual de réplica, você pode usar essa classe para identificar cada relação de replicação.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-105">Because you can have multiple replications for each replica virtual machine, you can use this class to identify each replication relationship.</span></span>

<span data-ttu-id="1c6f6-106">A sintaxe a seguir é simplificada do código MOF e inclui essas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-106">The following syntax is simplified from MOF code and includes these inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c6f6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c6f6-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationRelationship : CIM_ManagedSystemElement
{
  string   InstanceID;
  uint16   ReplicationState;
  uint16   ReplicationHealth;
  uint16   FailedOverReplicationType;
  uint16   LastReplicationType;
  datetime LastApplicationConsistentReplicationTime;
  datetime LastReplicationTime;
  datetime LastApplyTime;
};
```

## <a name="members"></a><span data-ttu-id="1c6f6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1c6f6-108">Members</span></span>

<span data-ttu-id="1c6f6-109">A classe **Msvm \_ ReplicationRelationship** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1c6f6-109">The **Msvm\_ReplicationRelationship** class has these types of members:</span></span>

-   [<span data-ttu-id="1c6f6-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1c6f6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c6f6-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1c6f6-111">Properties</span></span>

<span data-ttu-id="1c6f6-112">A classe **Msvm \_ ReplicationRelationship** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-112">The **Msvm\_ReplicationRelationship** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c6f6-113">**FailedOverReplicationType**</span><span class="sxs-lookup"><span data-stu-id="1c6f6-113">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6f6-114">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c6f6-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c6f6-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c6f6-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c6f6-116">O tipo de failover que foi executado para a relação de replicação.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-116">The type of failover that was performed for the replication relationship.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="1c6f6-117">**Nenhum** (0)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-117">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="1c6f6-118">**Regular** (1)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-118">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="1c6f6-119">**Consistente** com o aplicativo (2)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-119">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="1c6f6-120">**Planejado** (3)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-120">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c6f6-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1c6f6-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6f6-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1c6f6-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c6f6-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c6f6-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c6f6-124">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="1c6f6-124">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="1c6f6-125">Identifica a relação de replicação.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-125">Identifies replication relationship.</span></span> <span data-ttu-id="1c6f6-126">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1c6f6-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="1c6f6-127">Esta propriedade tem este formato:</span><span class="sxs-lookup"><span data-stu-id="1c6f6-127">This property has this format:</span></span>

<span data-ttu-id="1c6f6-128">**Microsoft: <vmid> \\ HVR \\<0/1>**</span><span class="sxs-lookup"><span data-stu-id="1c6f6-128">**Microsoft:<vmid>\\HVR\\<0/1>**</span></span>

<span data-ttu-id="1c6f6-129">0 indica primário e 1 indica [replicação estendida](#extended-replication).</span><span class="sxs-lookup"><span data-stu-id="1c6f6-129">0 indicates primary and 1 indicates [extended replication](#extended-replication).</span></span>

</dd> <dt>

<span data-ttu-id="1c6f6-130">**LastApplicationConsistentReplicationTime**</span><span class="sxs-lookup"><span data-stu-id="1c6f6-130">**LastApplicationConsistentReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6f6-131">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1c6f6-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1c6f6-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c6f6-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c6f6-133">A data e a hora em que a última replicação consistente do aplicativo é recebida na recuperação para o relacionamento de replicação.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-133">The date and time at which the last application consistent replication is received on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="1c6f6-134">**LastApplyTime**</span><span class="sxs-lookup"><span data-stu-id="1c6f6-134">**LastApplyTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6f6-135">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1c6f6-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1c6f6-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c6f6-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c6f6-137">A data e a hora em que a última replicação é aplicada na recuperação para o relacionamento de replicação.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-137">The date and time at which the last replication is applied on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="1c6f6-138">**LastReplicationTime**</span><span class="sxs-lookup"><span data-stu-id="1c6f6-138">**LastReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6f6-139">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1c6f6-139">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1c6f6-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c6f6-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c6f6-141">A data e a hora em que a última replicação é recebida na recuperação para o relacionamento de replicação.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-141">The date and time at which the last replication is received on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="1c6f6-142">**LastReplicationType**</span><span class="sxs-lookup"><span data-stu-id="1c6f6-142">**LastReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6f6-143">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c6f6-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c6f6-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c6f6-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c6f6-145">O tipo da última replicação recebida para a relação de replicação.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-145">The type of the last replication that was received for the replication relationship.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="1c6f6-146">**Nenhum** (0)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-146">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="1c6f6-147">**Regular** (1)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-147">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="1c6f6-148">**Consistente** com o aplicativo (2)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-148">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="1c6f6-149">**Planejado** (3)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-149">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c6f6-150">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="1c6f6-150">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6f6-151">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c6f6-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c6f6-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c6f6-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c6f6-153">Integridade da replicação para o relacionamento de replicação.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-153">Replication health for the replication relationship.</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1c6f6-154">**Não aplicável** (0)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-154">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="1c6f6-155">**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-155">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="1c6f6-156">**Aviso** (2)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-156">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="1c6f6-157">**Crítico** (3)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-157">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c6f6-158">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="1c6f6-158">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c6f6-159">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c6f6-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c6f6-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c6f6-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c6f6-161">Estado de replicação para a relação de replicação.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-161">Replication state for the replication relationship.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1c6f6-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (0)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="1c6f6-163"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Pronto para replicação** (1)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-163"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="1c6f6-164"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Aguardando para concluir a replicação inicial** (2)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-164"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="1c6f6-165"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicando** (3)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-165"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="1c6f6-166"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replicação sincronizada concluída** (4)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-166"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="1c6f6-167"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recuperado** (5)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-167"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="1c6f6-168"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Confirmado** (6)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-168"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="1c6f6-169"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspenso** (7)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-169"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="1c6f6-170"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (8)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-170"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="1c6f6-171"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Aguardando para iniciar a ressincronização** (9)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-171"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="1c6f6-172"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Ressincronização** (10)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-172"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="1c6f6-173"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Ressincronização suspensa** (11)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-173"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="1c6f6-174"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover em andamento** (12)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-174"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="1c6f6-175"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback em andamento** (13)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-175"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="1c6f6-176"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback concluído** (14)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-176"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback complete** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span data-ttu-id="1c6f6-177"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Atualização de disco em andamento** (15)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-177"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Disk update in progress** (15)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="1c6f6-178">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-178">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span data-ttu-id="1c6f6-179"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Atualização de disco crítica** (16)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-179"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Disk update critical** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="1c6f6-180">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-180">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c6f6-181"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (17)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-181"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (17)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="1c6f6-182">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-182">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="1c6f6-183"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Replicação de redefinição em andamento** (18)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-183"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Repurpose replication in progress** (18)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="1c6f6-184">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-184">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span data-ttu-id="1c6f6-185"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Preparado para replicação de sincronização** (19)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-185"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Prepared for sync replication** (19)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="1c6f6-186">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-186">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span data-ttu-id="1c6f6-187"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Preparado para replicação inversa de grupo** (20)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-187"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Prepared for group reverse replication** (20)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="1c6f6-188">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-188">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span data-ttu-id="1c6f6-189"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill em andamento** (21)</span><span class="sxs-lookup"><span data-stu-id="1c6f6-189"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill in progress** (21)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="1c6f6-190">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-190">This property was added in Windows 10, version 1703.</span></span>

 

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c6f6-191">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c6f6-191">Remarks</span></span>

### <a name="extended-replication"></a><span data-ttu-id="1c6f6-192">Replicação estendida</span><span class="sxs-lookup"><span data-stu-id="1c6f6-192">Extended replication</span></span>

<span data-ttu-id="1c6f6-193">O recurso de replicação do Hyper-V no Windows 8 permite que máquinas virtuais executadas em um servidor Hyper-V no site primário sejam replicadas com eficiência para outro servidor Hyper-V no site secundário.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-193">The Hyper-V replication feature in Windows 8 allows virtual machines that run on a Hyper-V server at the primary site to be efficiently replicated to another Hyper-V server at the secondary site.</span></span>

<span data-ttu-id="1c6f6-194">O recurso de replicação do Hyper-V no Windows 8.1 permite que um usuário estenda a relação de replicação do site secundário em diante para um terceiro site.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-194">The Hyper-V replication feature in Windows 8.1 enables a user to extend the replication relationship from the secondary site onwards to a third site.</span></span> <span data-ttu-id="1c6f6-195">O terceiro site pode ser um host Hyper-V previamente provisionado como um servidor de recuperação ou um provedor de replicação externo.</span><span class="sxs-lookup"><span data-stu-id="1c6f6-195">The third site can be a Hyper-V host pre-provisioned as a recovery server or external replication provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c6f6-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c6f6-196">Requirements</span></span>



| <span data-ttu-id="1c6f6-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c6f6-197">Requirement</span></span> | <span data-ttu-id="1c6f6-198">Valor</span><span class="sxs-lookup"><span data-stu-id="1c6f6-198">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c6f6-199">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c6f6-199">Minimum supported client</span></span><br/> | <span data-ttu-id="1c6f6-200">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1c6f6-200">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1c6f6-201">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c6f6-201">Minimum supported server</span></span><br/> | <span data-ttu-id="1c6f6-202">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="1c6f6-202">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1c6f6-203">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c6f6-203">Namespace</span></span><br/>                | <span data-ttu-id="1c6f6-204">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1c6f6-204">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1c6f6-205">MOF</span><span class="sxs-lookup"><span data-stu-id="1c6f6-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c6f6-206"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c6f6-206"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c6f6-207">DLL</span><span class="sxs-lookup"><span data-stu-id="1c6f6-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c6f6-208"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1c6f6-208"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1c6f6-209">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c6f6-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c6f6-210">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="1c6f6-210">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="1c6f6-211">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="1c6f6-211">**CIM\_ManagedSystemElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)
</dt> </dl>

 

