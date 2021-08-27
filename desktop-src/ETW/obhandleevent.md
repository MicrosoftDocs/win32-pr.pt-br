---
description: Representa a classe de tipo de evento para eventos de criação ou fechamento de identificador.
ms.assetid: 39d27cdf-fa51-4fb1-8998-7150ca627eff
title: Classe ObHandleEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleEvent
- ObHandleEvent.Handle
- ObHandleEvent.Object
- ObHandleEvent.ObjectName
- ObHandleEvent.ObjectType
api_type:
- NA
api_location: ''
ms.openlocfilehash: eec4e0eb00f7c821e3977f448d9c1af7e286d72a21a0a1b9473a6d3cd8fa3451
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083216"
---
# <a name="obhandleevent-class"></a>Classe ObHandleEvent

Representa a classe de tipo de evento para eventos de criação ou fechamento de identificador.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, EventType{32,33}, EventTypeName{CreateHandle,CloseHandle}]
class ObHandleEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
};
```

## <a name="members"></a>Membros

A **classe ObHandleEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe ObHandleEvent** tem essas propriedades.

<dl> <dt>

**Handle**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**formato**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

O identificador de objeto.

</dd> <dt>

**Objeto**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Formato**](event-tracing-mof-qualifiers.md) ("x"), [**Ponteiro**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)
</dt> </dl>

O objeto.

</dd> <dt>

**ObjectName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**formato**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)
</dt> </dl>

O nome do objeto.

</dd> <dt>

**ObjectType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

O tipo de objeto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |



 

 




