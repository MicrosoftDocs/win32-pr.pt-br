---
description: Uma classe abstrata da qual todas as classes de rastreamento de eventos são derivadas.
ms.assetid: 03eea902-5050-4ab2-8a72-9bff7777e234
title: Classe EventTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace
- EventTrace.EventSize
- EventTrace.ReservedHeaderField
- EventTrace.EventType
- EventTrace.TraceLevel
- EventTrace.TraceVersion
- EventTrace.ThreadId
- EventTrace.TimeStamp
- EventTrace.EventGuid
- EventTrace.KernelTime
- EventTrace.UserTime
- EventTrace.InstanceId
- EventTrace.ParentGuid
- EventTrace.ParentInstanceId
- EventTrace.MofData
- EventTrace.MofLength
api_type:
- NA
api_location: ''
ms.openlocfilehash: f04399942b39a2da5b746933884a436a65bb370c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647376"
---
# <a name="eventtrace-class"></a>Classe EventTrace

Uma classe abstrata da qual todas as classes de rastreamento de eventos são derivadas.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[abstract]
class EventTrace
{
  uint16 EventSize;
  uint16 ReservedHeaderField;
  uint8  EventType;
  uint8  TraceLevel;
  uint16 TraceVersion;
  uint64 ThreadId;
  uint64 TimeStamp;
  uint8  EventGuid[];
  uint32 KernelTime;
  uint32 UserTime;
  uint32 InstanceId;
  uint8  ParentGuid[];
  uint32 ParentInstanceId;
  uint32 MofData;
  uint32 MofLength;
};
```

## <a name="members"></a>Membros

A classe **EventTrace** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **EventTrace** tem essas propriedades.

<dl> <dt>

**EventGuid**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (8), **máx** . (16)
</dt> </dl>

GUID da classe de rastreamento de eventos deste evento.

</dd> <dt>

**Eventos de**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (1)
</dt> </dl>

Número total de bytes do evento.

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (3)
</dt> </dl>

Tipo de evento definido pelo provedor. Informa qual classe de tipo de evento deve ser usada para decifrar os dados de evento definidos pelo provedor (os dados apontados por **MofData**.

</dd> <dt>

**InstanceId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (11)
</dt> </dl>

Identificador desta instância de evento.

</dd> <dt>

**Kerneltime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (9)
</dt> </dl>

Tempo de execução decorrido para instruções do modo kernel, em tiques de CPU.

</dd> <dt>

**MofData**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (14), **ponteiro**
</dt> </dl>

Ponteiro para os dados de evento específicos do provedor.

</dd> <dt>

**MofLength**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (15)
</dt> </dl>

Comprimento dos dados de evento específicos do provedor.

</dd> <dt>

**ParentGuid**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (12), **máx** . (16)
</dt> </dl>

GUID da classe de rastreamento de eventos da instância pai.

</dd> <dt>

**ParentInstanceId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (13)
</dt> </dl>

Identificador dos dados da instância pai.

</dd> <dt>

**ReservedHeaderField**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (2)
</dt> </dl>

Reservado.

</dd> <dt>

**ThreadId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (6), **ponteiro**
</dt> </dl>

Identifica o thread que gerou o evento.

</dd> <dt>

**Estampa**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (7)
</dt> </dl>

Contém a data e a hora em que o evento ocorreu.

</dd> <dt>

**TraceLevel**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (4)
</dt> </dl>

Valor definido pelo provedor que define o nível de severidade usado para gerar o evento.

</dd> <dt>

**TraceVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (5)
</dt> </dl>

Número de versão definido pelo provedor da classe de rastreamento de eventos usada para gerar o evento.

</dd> <dt>

**Usertime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (10)
</dt> </dl>

Tempo de execução decorrido para instruções do modo de usuário, em tiques de CPU.

</dd> </dl>

## <a name="remarks"></a>Comentários

Não use essas propriedades.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| MOF<br/>                      | <dl> <dt>WMI. mof</dt> </dl> |



 

 




