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
ms.openlocfilehash: 04bb39e0c3ecb73facf09e962d2d189bd6ac59449908c0ed9e0214aa5551595e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644813"
---
# <a name="msvm_virtualsystemcollection-class"></a>\_Classe Msvm VirtualSystemCollection

Representa uma coleção de sistemas virtuais.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

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

## <a name="members"></a>Membros

A classe **Msvm \_ VirtualSystemCollection** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ VirtualSystemCollection** tem essas propriedades.

<dl> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionId"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

A identificação exclusiva do objeto de coleção.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")
</dt> </dl>

Um nome definido pelo usuário para a coleção. Observe que isso não é garantido como exclusivo.

</dd> <dt>

**FailedOverReplicationType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de failover que foi executado para a coleção do sistema virtual.

> [!Note]  
> adicionado em Windows 10, versão 1703.

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nenhum** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Regular** (1)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Planejado** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**LastApplyConsistencyLevel**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nível de consistência do último Delta aplicado.

> [!Note]  
> adicionado em Windows 10, versão 1703.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Consistente** com o aplicativo (1)


</dt> <dd>

O último Delta aplicado indica um ponto no tempo em que o sistema virtual estava no estado consistente do aplicativo.

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Falha consistente** (2)


</dt> <dd>

O último Delta aplicado indica um ponto no tempo em que o sistema virtual estava em estado consistente de falha.

</dd> <dt>

<span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>

<span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>**Falha de grupo consistente** (3)


</dt> <dd>

O último Delta aplicado indica um ponto no tempo em que o grupo estava em estado de falha consistente.

</dd> </dl>

</dd> <dt>

**LastApplyTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A hora em que a última replicação é aplicada na recuperação para a coleção do sistema virtual.

> [!Note]  
> adicionado em Windows 10, versão 1703.

 

</dd> <dt>

**LastApplyVirtualMachineIds**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de IDs de máquina virtual que foram aplicadas com êxito no último ciclo de aplicação.

> [!Note]  
> adicionado em Windows 10, versão 1703.

 

</dd> <dt>

**ReplicationMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de replicação para a coleção do sistema virtual.

> [!Note]  
> adicionado em Windows 10, versão 1703.

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nenhum** (0)


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

**Primário** (1)


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

**Réplica** (2)


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

**Réplica de teste** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Estado de replicação para a coleção do sistema virtual.

> [!Note]  
> adicionado em Windows 10, versão 1703.

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Desabilitado** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

**Pronto para replicação** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

**Aguardando para concluir a replicação inicial** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

**Replicando** (3)


</dt> <dd></dd> <dt>

<span id="Failover_initiated"></span><span id="failover_initiated"></span><span id="FAILOVER_INITIATED"></span>

**Failover iniciado** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

**Recuperado** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

**Confirmado** (6)


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

**Suspenso** (7)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Crítico** (8)


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

**Aguardando para iniciar a ressincronização** (9)


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

**Ressincronização** (10)


</dt> <dd></dd> <dt>

<span id="Planned_failover_initiatedRepurpose_initiatedTest_failover_initiatedPartially_enabled"></span><span id="planned_failover_initiatedrepurpose_initiatedtest_failover_initiatedpartially_enabled"></span><span id="PLANNED_FAILOVER_INITIATEDREPURPOSE_INITIATEDTEST_FAILOVER_INITIATEDPARTIALLY_ENABLED"></span>

Failover **planejado InitiatedRepurpose initiatedTest failover initiatedPartially habilitado** (11)


</dt> <dd></dd> <dt>

<span id="Partially_disabled"></span><span id="partially_disabled"></span><span id="PARTIALLY_DISABLED"></span>

**Parcialmente desabilitado** (12)


</dt> <dd></dd> <dt>

<span id="Partially_recovered"></span><span id="partially_recovered"></span><span id="PARTIALLY_RECOVERED"></span>

**Parcialmente recuperado** (13)


</dt> <dd></dd> <dt>



 (14)


</dt> <dd></dd> <dt>



 (15)


</dt> <dd></dd> <dt>



 (16)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md)
</dt> </dl>

 

