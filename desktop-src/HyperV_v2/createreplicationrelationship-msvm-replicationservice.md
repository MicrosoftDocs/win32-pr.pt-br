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
# <a name="createreplicationrelationship-method-of-the-msvm_replicationservice-class"></a>Método CreateReplicationRelationship da \_ classe ReplicationService Msvm

Cria um novo relacionamento de replicação para uma máquina virtual. Quando um cliente chama esse método para uma máquina virtual de réplica, ele estende a relação de replicação para o provedor especificado.

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

*ComputerSystem* \[ no\]
</dt> <dd>

Uma referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual para a qual a replicação deve ser habilitada.

</dd> <dt>

*ReplicationSettingData* \[ no\]
</dt> <dd>

Uma representação de cadeia de caracteres de uma instância da classe [**Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) que define as configurações de replicação para a nova relação de replicação a ser criada para a máquina virtual.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Parâmetros de método marcados-trabalho iniciado** (4096)
</dt> <dt>

**Falha** (32768)
</dt> <dt>

**Acesso negado** (32769)
</dt> <dt>

**Sem suporte** (32770)
</dt> <dt>

O **status é desconhecido** (32771)
</dt> <dt>

**Tempo limite** (32772)
</dt> <dt>

**Parâmetro inválido** (32773)
</dt> <dt>

O **sistema está em uso** (32774)
</dt> <dt>

**Estado inválido para esta operação** (32775)
</dt> <dt>

**Tipo de dados incorreto** (32776)
</dt> <dt>

O **sistema não está disponível** (32777)
</dt> <dt>

**Memória insuficiente** (32778)
</dt> <dt>

**Arquivo não encontrado** (32779)
</dt> </dl>

## <a name="remarks"></a>Comentários

**CreateReplicationRelationship** usa uma FRSD (instância [**\_ ReplicationSettingData Msvm**](msvm-replicationsettingdata.md) ) como entrada. O FRSD associado para a máquina virtual como o provedor host-to-host é a opção padrão. O FRSD de entrada é validado para configurações válidas para cada propriedade para o provedor padrão. Esta tabela resume as diferenças de validação em relação ao provedor externo.



| Propriedade                                             | Provedores externos                                 |
|------------------------------------------------------|----------------------------------------------------|
| Replicationprovider                                  | Mesmo que o provedor padrão                           |
| AuthenticationType                                   | Ignored                                            |
| CertificateThumbPrint                                | Ignored                                            |
| RootCertificateThumbPrint (RO)                       | Ignored                                            |
| CompressionEnabled                                   | Mesmo que o provedor padrão                           |
| BypassProxyServer                                    | Mesmo que o provedor padrão                           |
| RecoveryConnectionPoint                              | Ignorado \* (pode alterar se o provedor tiver requisito) |
| RecoveryHostSystem (RO)                              | Ignored                                            |
| PrimaryConnectionPoint (RO)                          | Mesmo que o provedor padrão                           |
| PrimaryHostSystem (RO)                               | Mesmo que o provedor padrão                           |
| RecoveryServerPortNumber                             | Ignorado \* (pode alterar se o provedor tiver requisito) |
| ReplicateHostKvpItems                                | Ignored                                            |
| ApplicationConsistentSnapshotInterval                | Mesmo que o provedor padrão                           |
| RecoveryHistory                                      | Mesmo que o provedor padrão                           |
| IncludedDisks\[\]                                    | Mesmo que o provedor padrão                           |
| AutoResynchronizeEnabled                             | Mesmo que o provedor padrão                           |
| AutoResynchronizeIntervalStart                       | Mesmo que o provedor padrão                           |
| AutoResynchronizeIntervalEnd                         | Mesmo que o provedor padrão                           |
| EnableWriteOrderPreservationAcrossDisks (preterido) | Mesmo que o provedor padrão                           |
| ReplicationInterval                                  | Mesmo que o provedor padrão                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> <dt>

[**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)
</dt> </dl>

 

