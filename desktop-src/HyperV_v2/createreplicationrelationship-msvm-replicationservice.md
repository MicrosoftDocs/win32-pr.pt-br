---
description: Cria uma nova relação de replicação para uma máquina virtual. Quando um cliente chama esse método para uma máquina virtual de réplica, ele estende a relação de replicação para o provedor especificado.
ms.assetid: 44d3b5aa-46c2-4fe9-9a1d-6ee699d3640d
title: Método CreateReplicationRelationship da classe Msvm_ReplicationService dados
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
ms.openlocfilehash: d9b61c2339a426314d5c62fe5481b51ba3960c2650ccbdc40b9b9ebd4761cfc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150079"
---
# <a name="createreplicationrelationship-method-of-the-msvm_replicationservice-class"></a>Método CreateReplicationRelationship da classe Msvm \_ ReplicationService

Cria uma nova relação de replicação para uma máquina virtual. Quando um cliente chama esse método para uma máquina virtual de réplica, ele estende a relação de replicação para o provedor especificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CreateReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ComputerSystem* \[ Em\]
</dt> <dd>

Uma referência a uma [**instância \_ do ComputerSystem cim**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa a máquina virtual para a qual a replicação deve ser habilitada.

</dd> <dt>

*ReplicationSettingData* \[ Em\]
</dt> <dd>

Uma representação de cadeia de caracteres de uma instância da classe [**Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) que define as configurações de replicação para a nova relação de replicação a ser criada para a máquina virtual.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096 e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Parâmetros de método verificados – Trabalho iniciado** (4096)
</dt> <dt>

**Falha** (32768)
</dt> <dt>

**Acesso negado** (32769)
</dt> <dt>

**Sem suporte** (32770)
</dt> <dt>

**O status é desconhecido** (32771)
</dt> <dt>

**Tempoout** (32772)
</dt> <dt>

**Parâmetro inválido** (32773)
</dt> <dt>

**O sistema está em uso** (32774)
</dt> <dt>

**Estado inválido para esta operação** (32775)
</dt> <dt>

**Tipo de dados incorreto** (32776)
</dt> <dt>

**O sistema não está disponível** (32777)
</dt> <dt>

**Memória sem memória** (32778)
</dt> <dt>

**Arquivo não encontrado** (32779)
</dt> </dl>

## <a name="remarks"></a>Comentários

**CreateReplicationRelationship** aceita uma [**instância Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) (FRSD) como entrada. O FRSD associado para a máquina virtual como provedor de host para host é a opção padrão. O FRSD de entrada é validado para configurações válidas para cada propriedade para o provedor padrão. Esta tabela resume as diferenças de validação em relação ao provedor externo.



| Propriedade                                             | Provedores externos                                 |
|------------------------------------------------------|----------------------------------------------------|
| ReplicationProvider                                  | O mesmo que o provedor padrão                           |
| AuthenticationType                                   | Ignored                                            |
| Certificatethumbprint                                | Ignored                                            |
| RootCertificateThumbPrint (RO)                       | Ignored                                            |
| Compressionenabled                                   | O mesmo que o provedor padrão                           |
| BypassProxyServer                                    | O mesmo que o provedor padrão                           |
| RecoveryConnectionPoint                              | Ignorado \* (pode mudar se o provedor tiver requisitos) |
| RecoveryHostSystem (RO)                              | Ignored                                            |
| PrimaryConnectionPoint (RO)                          | O mesmo que o provedor padrão                           |
| PrimaryHostSystem (RO)                               | O mesmo que o provedor padrão                           |
| RecoveryServerPortNumber                             | Ignorado \* (pode mudar se o provedor tiver requisitos) |
| ReplicateHostKvpItems                                | Ignored                                            |
| ApplicationConsistentSnapshotInterval                | O mesmo que o provedor padrão                           |
| RecoveryHistory                                      | O mesmo que o provedor padrão                           |
| IncludedDisks\[\]                                    | O mesmo que o provedor padrão                           |
| AutoResynchronizeEnabled                             | O mesmo que o provedor padrão                           |
| AutoResynchronizeIntervalStart                       | O mesmo que o provedor padrão                           |
| AutoResynchronizeIntervalEnd                         | O mesmo que o provedor padrão                           |
| EnableWriteOrderPreservationAcrossDisks (preterido) | O mesmo que o provedor padrão                           |
| ReplicationInterval                                  | O mesmo que o provedor padrão                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> <dt>

[**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)
</dt> </dl>

 

