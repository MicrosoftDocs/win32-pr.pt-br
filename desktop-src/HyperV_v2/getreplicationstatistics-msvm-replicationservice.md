---
description: Recupera estatísticas de replicação para uma máquina virtual e atua na relação de replicação primária da máquina virtual.
ms.assetid: 24f3f572-fa85-4680-be77-7e835e6471c5
title: Método GetReplicationStatistics da classe Msvm_ReplicationService dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 767ea873b725523e3d430708dc5485d3d24c62e07e5cebac001b020ee996bd63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392909"
---
# <a name="getreplicationstatistics-method-of-the-msvm_replicationservice-class"></a>Método GetReplicationStatistics da classe Msvm \_ ReplicationService

Recupera estatísticas de replicação para uma máquina virtual e atua na relação de replicação primária da máquina virtual.

> [!Note]  
> Começando com Windows 8.1, recomendamos não usar **mais GetReplicationStatistics** para recuperar estatísticas de replicação. Em vez disso, [**use GetReplicationStatisticsEx.**](getreplicationstatisticsex-msvm-replicationservice.md)

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ComputerSystem* \[ Em\]
</dt> <dd>

Uma referência a uma [**instância \_ do ComputerSystem cim**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa a máquina virtual para a qual recuperar as estatísticas de replicação.

</dd> <dt>

*ReplicationStatistics* \[ out\]
</dt> <dd>

Se for bem-sucedido, receberá uma instância inserida da [**classe Msvm \_ ReplicationStatistics**](msvm-replicationstatistics.md) que contém as estatísticas de replicação para a máquina virtual solicitada.

</dd> <dt>

*ReplicationHealthIssues* \[ out\]
</dt> <dd>

Se for bem-sucedido, receberá uma matriz de instâncias inseridas da [**classe Erro \_ Msvm**](msvm-error.md) que indicam avisos de replicação ou erros para a máquina virtual solicitada.

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

**O sistema está em usado** (32774)
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

[**ResetReplicationStatistics**](resetreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

