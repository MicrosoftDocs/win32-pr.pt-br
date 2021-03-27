---
description: Essa classe é a classe de tipo de evento para eventos de término de thread. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: c495bf22-04ce-4285-8e7e-152e4ab65823
title: Classe Thread_V1_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup2
- Thread_V1_TypeGroup2.ProcessId
- Thread_V1_TypeGroup2.TThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3e56590127b2317813d7431a1cc646fbe76e35a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502068"
---
# <a name="thread_v1_typegroup2-class"></a>\_ \_ Classe TypeGroup2 de thread v1

Essa classe é a classe de tipo de evento para eventos de término de thread.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{2, 4}, EventTypeName{"End", "DCEnd"}]
class Thread_V1_TypeGroup2 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
};
```

## <a name="members"></a>Membros

A classe **thread \_ v1 \_ TypeGroup2** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **thread \_ v1 \_ TypeGroup2** tem essas propriedades.

<dl> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1)
</dt> </dl>

Identificador de processo do thread envolvido no evento.

**Windows Server 2003:** Contém o qualificador de formato ("x").

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2)
</dt> </dl>

Identificador de thread do thread envolvido no evento.

**Windows Server 2003:** Contém o qualificador de formato ("x").

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Thread \_ v1**](thread-v1.md)
</dt> </dl>

 

 




