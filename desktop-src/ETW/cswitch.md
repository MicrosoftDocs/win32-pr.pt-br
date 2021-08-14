---
description: Essa classe é a classe de tipo de evento para eventos de alternância de contexto. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 3f9f84d0-18a9-493c-b104-8236b2bd8404
title: Classe CSwitch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSwitch
- CSwitch.NewThreadId
- CSwitch.OldThreadId
- CSwitch.NewThreadPriority
- CSwitch.OldThreadPriority
- CSwitch.PreviousCState
- CSwitch.SpareByte
- CSwitch.OldThreadWaitReason
- CSwitch.OldThreadWaitMode
- CSwitch.OldThreadState
- CSwitch.OldThreadWaitIdealProcessor
- CSwitch.NewThreadWaitTime
- CSwitch.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 09efeac38babb057621cb6f25d14d3a631c12242e91982ae3ab9e79570416be5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118395342"
---
# <a name="cswitch-class"></a>Classe CSwitch

Essa classe é a classe de tipo de evento para eventos de alternância de contexto.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{36}, EventTypeName{"CSwitch"}]
class CSwitch : Thread_V2
{
  uint32 NewThreadId;
  uint32 OldThreadId;
  sint8  NewThreadPriority;
  sint8  OldThreadPriority;
  uint8  PreviousCState;
  sint8  SpareByte;
  sint8  OldThreadWaitReason;
  sint8  OldThreadWaitMode;
  sint8  OldThreadState;
  sint8  OldThreadWaitIdealProcessor;
  uint32 NewThreadWaitTime;
  uint32 Reserved;
};
```

## <a name="members"></a>Membros

A classe **CSwitch** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CSwitch** tem essas propriedades.

<dl> <dt>

**NewThreadId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1), formato ("x")
</dt> </dl>

Nova ID de thread após a opção.

</dd> <dt>

**NewThreadPriority**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (3)
</dt> </dl>

Prioridade do thread do novo thread.

</dd> <dt>

**NewThreadWaitTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (11), formato ("x")
</dt> </dl>

Tempo de espera para o novo thread.

</dd> <dt>

**OldThreadId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2), formato ("x")
</dt> </dl>

ID de thread anterior.

</dd> <dt>

**OldThreadPriority**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (4)
</dt> </dl>

Prioridade de thread do thread anterior.

</dd> <dt>

**OldThreadState**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (9)
</dt> </dl>

Estado do thread anterior. Estes são os valores de estado possíveis:

| Estado | Descrição                                   |
|-------|-----------------------------------------------|
| 0     | Inicializado                                   |
| 1     | Ready                                         |
| 2     | Executando                                       |
| 3     | Standby                                       |
| 4     | Terminado                                    |
| 5     | Aguardando                                       |
| 6     | Transição                                    |
| 7     | DeferredReady (adicionado ao Windows Server 2003) |



 

</dd> <dt>

**OldThreadWaitIdealProcessor**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (10), formato ("x")
</dt> </dl>

Tempo de espera ideal do thread anterior.

</dd> <dt>

**OldThreadWaitMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (8)
</dt> </dl>

Modo de espera para o thread anterior. O valores possíveis são os seguintes:

| Estado | Descrição |
|-------|-------------|
| 0     | KernelMode  |
| 1     | Modo    |



 

</dd> <dt>

**OldThreadWaitReason**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (7)
</dt> </dl>

Motivo de espera para o thread anterior. O valores possíveis são os seguintes:

| Estado | Descrição       |
|-------|-------------------|
| 0     | Executivo         |
| 1     | FreePage          |
| 2     | PageIn            |
| 3     | PoolAllocation    |
| 4     | DelayExecution    |
| 5     | Suspenso         |
| 6     | Solicitação de pedido       |
| 7     | WrExecutive       |
| 8     | WrFreePage        |
| 9     | WrPageIn          |
| 10    | WrPoolAllocation  |
| 11    | WrDelayExecution  |
| 12    | WrSuspended       |
| 13    | WrUserRequest     |
| 14    | WrEventPair       |
| 15    | WrQueue           |
| 16    | WrLpcReceive      |
| 17    | WrLpcReply        |
| 18    | WrVirtualMemory   |
| 19    | WrPageOut         |
| 20    | WrRevous      |
| 21    | WrKeyedEvent      |
| 22    | WrTerminated      |
| 23    | WrProcessInSwap   |
| 24    | WrCpuRateControl  |
| 25    | WrCalloutStack    |
| 26    | WrKernel          |
| 27    | WrResource        |
| 28    | WrPushLock        |
| 29    | WrMutex           |
| 30    | WrQuantumEnd      |
| 31    | WrDispatchInt     |
| 32    | WrPreempted       |
| 33    | WrYieldExecution  |
| 34    | WrFastMutex       |
| 35    | WrGuardedMutex    |
| 36    | WrRundown         |
| 37    | MaximumWaitReason |



 

</dd> <dt>

**PreviousCState**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(5)
</dt> </dl>

O índice do estado C que foi usado pela última vez pelo processador. Um valor de 0 representa o estado ocioso mais claro com valores mais altos que representam estados C mais profundos.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(12)
</dt> </dl>

Reservado.

</dd> <dt>

**SpareByte**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(6)
</dt> </dl>

Não usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esses eventos produzem um alto volume de eventos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Thread**](thread.md)
</dt> <dt>

[**Thread \_ V2**](thread-v2.md)
</dt> </dl>

 

 




