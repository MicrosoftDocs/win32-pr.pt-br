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
ms.openlocfilehash: c8ff905475863df11c6fb6529f030f73a4f1b785792be4c5fe8c7ce1142096c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068476"
---
# <a name="msvm_replicationrelationship-class"></a>\_Classe Msvm ReplicationRelationship

Representa o status de replicação para um relacionamento de replicação. Como você pode ter várias replicações para cada máquina virtual de réplica, você pode usar essa classe para identificar cada relação de replicação.

A sintaxe a seguir é simplificada do código MOF e inclui essas propriedades herdadas.

## <a name="syntax"></a>Sintaxe

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

## <a name="members"></a>Membros

A classe **Msvm \_ ReplicationRelationship** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ ReplicationRelationship** tem essas propriedades.

<dl> <dt>

**FailedOverReplicationType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo de failover que foi executado para a relação de replicação.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nenhum** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Regular** (1)


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**Consistente** com o aplicativo (2)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Planejado** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")
</dt> </dl>

Identifica a relação de replicação. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

Esta propriedade tem este formato:

**Microsoft: <vmid> \\ HVR \\<0/1>**

0 indica primário e 1 indica [replicação estendida](#extended-replication).

</dd> <dt>

**LastApplicationConsistentReplicationTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data e a hora em que a última replicação consistente do aplicativo é recebida na recuperação para o relacionamento de replicação.

</dd> <dt>

**LastApplyTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data e a hora em que a última replicação é aplicada na recuperação para o relacionamento de replicação.

</dd> <dt>

**LastReplicationTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data e a hora em que a última replicação é recebida na recuperação para o relacionamento de replicação.

</dd> <dt>

**LastReplicationType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo da última replicação recebida para a relação de replicação.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nenhum** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Regular** (1)


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**Consistente** com o aplicativo (2)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Planejado** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationHealth**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Integridade da replicação para o relacionamento de replicação.

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Não aplicável** (0)


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**OK** (1)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Aviso** (2)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Crítico** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Estado de replicação para a relação de replicação.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Pronto para replicação** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Aguardando para concluir a replicação inicial** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicando** (3)


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replicação sincronizada concluída** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recuperado** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Confirmado** (6)


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspenso** (7)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (8)


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Aguardando para iniciar a ressincronização** (9)


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Ressincronização** (10)


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Ressincronização suspensa** (11)


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover em andamento** (12)


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback em andamento** (13)


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback concluído** (14)


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Atualização de disco em andamento** (15)


</dt> <dd>

> [!Note]  
> essa propriedade foi adicionada em Windows 10, versão 1703.

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Atualização de disco crítica** (16)


</dt> <dd>

> [!Note]  
> essa propriedade foi adicionada em Windows 10, versão 1703.

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (17)


</dt> <dd>

> [!Note]  
> essa propriedade foi adicionada em Windows 10, versão 1703.

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Replicação de redefinição em andamento** (18)


</dt> <dd>

> [!Note]  
> essa propriedade foi adicionada em Windows 10, versão 1703.

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Preparado para replicação de sincronização** (19)


</dt> <dd>

> [!Note]  
> essa propriedade foi adicionada em Windows 10, versão 1703.

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Preparado para replicação inversa de grupo** (20)


</dt> <dd>

> [!Note]  
> essa propriedade foi adicionada em Windows 10, versão 1703.

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill em andamento** (21)


</dt> <dd>

> [!Note]  
> essa propriedade foi adicionada em Windows 10, versão 1703.

 

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentários

### <a name="extended-replication"></a>Replicação estendida

o recurso de replicação do hyper-v no Windows 8 permite que máquinas virtuais executadas em um servidor hyper-v no site primário sejam replicadas com eficiência para outro servidor hyper-v no site secundário.

o recurso de replicação do Hyper-V no Windows 8.1 permite que um usuário estenda a relação de replicação do site secundário em diante para um terceiro site. O terceiro site pode ser um host Hyper-V previamente provisionado como um servidor de recuperação ou um provedor de replicação externo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                                                 |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_MANAGEDSYSTEMELEMENT CIM**](cim-managedsystemelement.md)
</dt> <dt>

[**\_MANAGEDSYSTEMELEMENT CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)
</dt> </dl>

 

