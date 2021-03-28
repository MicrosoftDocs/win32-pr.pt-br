---
description: Representa a classe de tipo de evento para eventos de identificador de objeto relacionados ao início e ao fim da coleta de dados.
ms.assetid: 96231819-f4ca-4c5c-bc19-4a76add5d3cf
title: Classe ObHandleRundownEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleRundownEvent
- ObHandleRundownEvent.Handle
- ObHandleRundownEvent.Object
- ObHandleRundownEvent.ObjectName
- ObHandleRundownEvent.ObjectType
- ObHandleRundownEvent.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5477acc1851d9799fe2bf68f9b867ab3f4c032fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968042"
---
# <a name="obhandlerundownevent-class"></a>Classe ObHandleRundownEvent

Representa a classe de tipo de evento para eventos de identificador de objeto relacionados ao início e ao fim da coleta de dados. Esse evento envolve a enumeração de todos os identificadores quando o encerramento é executado.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, EventType{38,39}, EventTypeName{HandleDCStart,HandleDCEnd}]
class ObHandleRundownEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
  uint32 ProcessId;
};
```

## <a name="members"></a>Membros

A classe **ObHandleRundownEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **ObHandleRundownEvent** tem essas propriedades.

<dl> <dt>

**Handle**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

O identificador de objeto.

</dd> <dt>

**Objeto**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)
</dt> </dl>

O objeto.

</dd> <dt>

**ObjectName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)
</dt> </dl>

O nome do objeto.

</dd> <dt>

**ObjectType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)
</dt> </dl>

O tipo de objeto.

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

O identificador de processo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |



 

 




