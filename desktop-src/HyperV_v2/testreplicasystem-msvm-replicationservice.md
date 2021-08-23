---
description: Cria uma nova réplica de uma máquina virtual com o instantâneo especificado para fins de teste.
ms.assetid: 447f3c8f-8c57-4874-9466-91c6aea533bc
title: Método TestReplicaSystem da Msvm_ReplicationService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicaSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d23a97e43dce07d8c0ac0b06f2b488f5966ee63d82f5d92eacac017dc8e05de1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870246"
---
# <a name="testreplicasystem-method-of-the-msvm_replicationservice-class"></a>Método TestReplicaSystem da classe Msvm \_ ReplicationService

Cria uma nova réplica de uma máquina virtual com o instantâneo especificado para fins de teste.

## <a name="syntax"></a>Sintaxe


```mof
uint32 TestReplicaSystem(
  [in]  CIM_ComputerSystem           REF ComputerSystem,
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ComputerSystem* \[ Em\]
</dt> <dd>

Uma referência a uma [**instância \_ do ComputerSystem cim**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa a máquina virtual para a qual a replicação deve ser testada.

</dd> <dt>

*SnapshotSettingData* \[ Em\]
</dt> <dd>

Uma referência a uma [**instância do CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) que representa o instantâneo usado para criar o sistema de failover de teste. Se esse parâmetro for **Nulo,** o failover será executado fora do ponto mais recente no tempo.

</dd> <dt>

*ResultingSystem* \[ out\]
</dt> <dd>

Se uma máquina virtual for definida com êxito, o receberá uma referência a uma instância da classe [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa a máquina virtual de teste recém-definida. Quando esse sistema não for mais necessário, destrói-o chamando o [**método DestroySystem.**](destroysystem-msvm-virtualsystemmanagementservice.md)

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
</dt> </dl>

 

