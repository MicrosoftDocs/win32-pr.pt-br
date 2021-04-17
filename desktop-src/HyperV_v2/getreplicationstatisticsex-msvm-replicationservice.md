---
description: Recupera as estatísticas de replicação que estão associadas ao relacionamento de replicação especificado da máquina virtual.
ms.assetid: AB46894A-CBED-40DF-86B9-B578603B0341
title: 'Método Msvm_ReplicationService:: GetReplicationStatisticsEx'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7fdb60addc94094082fe83e70af06a2f5ae11f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770221"
---
# <a name="msvm_replicationservicegetreplicationstatisticsex-method"></a>\_Método Msvm ReplicationService:: GetReplicationStatisticsEx

Recupera as estatísticas de replicação que estão associadas ao relacionamento de replicação especificado da máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
uint32 GetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ComputerSystem* \[ no\]
</dt> <dd>

Uma referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual para a qual recuperar as estatísticas de replicação.

</dd> <dt>

*ReplicationRelationship* \[ no\]
</dt> <dd>

Uma representação de cadeia de caracteres de uma instância inserida da classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) que define a relação de replicação para a qual recuperar as estatísticas de replicação.

</dd> <dt>

*ReplicationStatistics* \[ fora\]
</dt> <dd>

Se for bem-sucedido, o receberá uma instância inserida da classe [**Msvm \_ ReplicationStatistics**](msvm-replicationstatistics.md) que contém as estatísticas de replicação para a relação de replicação solicitada.

</dd> <dt>

*ReplicationHealthIssues* \[ fora\]
</dt> <dd>

Se for bem-sucedido, o receberá uma matriz de instâncias inseridas da classe de [**\_ erro Msvm**](msvm-error.md) que indicam quaisquer erros ou avisos de replicação para a máquina virtual solicitada.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)). Essa referência poderá ser **nula** se a tarefa for concluída.

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

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                                 |
| Namespace<br/>                | \\\\\\Virtualização \\ v2 de raiz<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> <dt>

[**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md)
</dt> </dl>

 

