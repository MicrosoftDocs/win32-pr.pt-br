---
description: Inicia o failback para uma máquina virtual de recuperação.
ms.assetid: F4AE1911-46B2-4412-A17F-3CA7D388276F
title: Msvm_ReplicationService::InitiateFailback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailback
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b573cf1a0347e8df55b239451d9b99f3d416ebd5b3d0d61e662b6023f07a5b2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644942"
---
# <a name="msvm_replicationserviceinitiatefailback-method"></a>Método Msvm \_ ReplicationService::InitiateFailback

Inicia o failback para uma máquina virtual de recuperação.

## <a name="syntax"></a>Sintaxe


```C++
uint32 InitiateFailback(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [in]  string                 RecoveryPointIdentifier,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ComputerSystem* \[ Em\]
</dt> <dd>

Uma referência a uma [**instância \_ do ComputerSystem cim**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa a máquina virtual para a qual iniciar um failback.

</dd> <dt>

*ReplicationSettingData* \[ Em\]
</dt> <dd>

Uma representação de cadeia de caracteres de uma instância inserida da [**classe Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) que define as configurações de replicação para o failback.

</dd> <dt>

*RecoveryPointIdentifier* \[ Em\]
</dt> <dd>

Entrada opcional que identifica o ponto de recuperação para o qual o failback é solicitado.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096 e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob.**](/previous-versions//cc136808(v=vs.85)) Essa referência pode ser usada para monitorar o progresso e para obter o resultado do método .

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

**InitiateFailback** funciona em uma máquina virtual de recuperação e leva a máquina virtual para *o estado WaitingForFailback.* **InitiateFailback** encaminha a solicitação de failback para o provedor correspondente, que ressíncrona o ponto de recuperação do lado novo primário. Após a conclusão do failback do ponto de recuperação solicitado, o estado de replicação passa *para o estado FailbackCompleted.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                                 |
| Namespace<br/>                | \\\\Virtualização \\ raiz \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

