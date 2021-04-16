---
description: Solicita que o estado de replicação da máquina virtual seja alterado para o valor especificado e atue na relação de replicação primária da máquina virtual.
ms.assetid: 65FCDADD-1C50-4816-B10B-A951D1FC9C3B
title: Método RequestReplicationStateChange da classe Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 32f0136662f043627a5fad152ee0e0aaa1845e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505687"
---
# <a name="requestreplicationstatechange-method-of-the-msvm_computersystem-class"></a>Método RequestReplicationStateChange da classe de \_ ComputerSystem Msvm

Solicita que o estado de replicação da máquina virtual seja alterado para o valor especificado e atue na relação de replicação primária da máquina virtual. Enquanto a alteração de estado estiver em andamento, a propriedade **replicationstate** será alterada para o valor do parâmetro *requestedstate* . Esse método só tem suporte para instâncias da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representam uma máquina virtual.

> [!Note]  
> A partir do Windows 8.1, recomendamos não usar o **RequestReplicationStateChange** para solicitar a alteração do estado de replicação. Em vez disso, use [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md).

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 RequestReplicationStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Requestedstate* \[ no\]
</dt> <dd>

O novo estado de replicação. O deve ser um dos valores a seguir.

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Pronto para iniciar a replicação inicial** (1)


</dt> <dd>

Pronto para iniciar a replicação inicial.

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Aguardando para concluir a replicação inicial** (2)


</dt> <dd>

Aguardando para concluir a replicação inicial.

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicando** (3)


</dt> <dd>

Replicando.

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replicação sincronizada concluída** (4)


</dt> <dd>

Replicação sincronizada concluída.

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (7)


</dt> <dd>

Suspender a replicação.

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancelar ressincronização** (9)


</dt> <dd>

Cancele a ressincronização.

</dd> </dl> </dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Uma referência opcional a um objeto [**Msvm \_ ConcreteJob**](msvm-concretejob.md) que é retornado se a operação é executada de forma assíncrona. Se estiver presente, a referência retornada poderá ser usada para monitorar o progresso e obter o resultado do método.

</dd> <dt>

*TimeoutPeriod* \[ no\]
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um dos valores a seguir.



| Código/valor de retorno                                                                                                                                                                | Descrição                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Concluído sem erro**</dt> <dt>0</dt> </dl>                    | Êxito<br/>                                                                                                          |
| <dl> <dt>**Parâmetros de método verificados-trabalho iniciado**</dt> <dt>4096</dt> </dl> | A transição é assíncrona.<br/>                                                                                  |
| <dl> <dt>32768</dt> <dt>**com falha**</dt> </dl>                                 |                                                                                                                             |
| <dl> <dt>**Acesso negado**</dt> <dt>32769</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**Sem suporte**</dt> <dt>32770</dt> </dl>                          |                                                                                                                             |
| <dl> O <dt>**status é desconhecido**</dt> <dt>32771</dt> </dl>                      |                                                                                                                             |
| <dl> <dt>**Tempo limite**</dt> <dt>32772</dt> </dl>                                |                                                                                                                             |
| <dl> <dt>**Parâmetro inválido**</dt> <dt>32773</dt> </dl>                      | Não há suporte para o valor especificado em um dos parâmetros.<br/>                                                   |
| <dl> O <dt>**sistema está em uso**</dt> <dt>32774</dt> </dl>                       |                                                                                                                             |
| <dl> <dt>**Estado inválido para esta operação**</dt> <dt>32775</dt> </dl>       | O valor especificado no parâmetro *requestedstate* não tem suporte no modo de replicação ou no estado atual.<br/> |
| <dl> <dt>**Tipo de dados incorreto**</dt> <dt>32776</dt> </dl>                    |                                                                                                                             |
| <dl> O <dt>**sistema não está disponível**</dt> <dt>32777</dt> </dl>                |                                                                                                                             |
| <dl> <dt>**Memória insuficiente**</dt> <dt>32778</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**Arquivo não encontrado**</dt> <dt>32779</dt> </dl>                         |                                                                                                                             |



 

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

[**Msvm \_ ComputerSystem**](msvm-computersystem.md)
</dt> </dl>

 

 




