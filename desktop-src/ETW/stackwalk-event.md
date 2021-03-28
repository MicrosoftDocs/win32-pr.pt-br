---
description: Essa classe é a classe de tipo de evento para eventos de rastreamento de pilha.
ms.assetid: 05117bd6-a39c-42f3-8aed-c6f758f946c6
title: Classe StackWalk_Event
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk_Event
- StackWalk_Event.EventTimeStamp
- StackWalk_Event.StackProcess
- StackWalk_Event.StackThread
- StackWalk_Event.Stack1
- StackWalk_Event.Stack192
api_type:
- NA
api_location: ''
ms.openlocfilehash: 746a7f2a9b5f6bb6316bf0d0e20e5645cea15a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968033"
---
# <a name="stackwalk_event-class"></a>\_Classe de evento StackWalk

Essa classe é a classe de tipo de evento para eventos de rastreamento de pilha.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{32}, EventTypeName{"Stack"}]
class StackWalk_Event : StackWalk
{
  uint64 EventTimeStamp;
  uint32 StackProcess;
  uint32 StackThread;
  uint32 Stack1;
  uint32 Stack192;
};
```

## <a name="members"></a>Membros

A classe de **\_ evento StackWalk** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ evento StackWalk** tem essas propriedades.

<dl> <dt>

**EventTimeStamp**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1)
</dt> </dl>

Carimbo de data/hora do evento original do cabeçalho do evento. Use este carimbo de data/hora para corresponder a pilha a um evento.

</dd> <dt>

**Stack1**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (4), ponteiro
</dt> </dl>

Endereço da chamada.

</dd> <dt>

**Stack192**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (195), ponteiro
</dt> </dl>

Endereço da chamada.

</dd> <dt>

**StackProcess**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2), formato ("x")
</dt> </dl>

O identificador de processo do evento original.

</dd> <dt>

**StackThread**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (3)
</dt> </dl>

O identificador de thread do evento original.

</dd> </dl>

## <a name="remarks"></a>Comentários

Observe que a classe não mostra todas as propriedades **Stack * n*** que existem entre **Stack1** e **Stack192**. Use o tamanho do evento para determinar quantas propriedades **Stack * n*** contêm endereços válidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



 

 




