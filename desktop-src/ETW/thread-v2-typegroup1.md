---
description: Thread_V2_TypeGroup1 classe - essa classe é a classe de tipo de evento para eventos de início e término de thread. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: c24b4bc9-2a05-444c-be41-b4dfd0511b93
title: Thread_V2_TypeGroup1 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2_TypeGroup1
- Thread_V2_TypeGroup1.ProcessId
- Thread_V2_TypeGroup1.TThreadId
- Thread_V2_TypeGroup1.StackBase
- Thread_V2_TypeGroup1.StackLimit
- Thread_V2_TypeGroup1.UserStackBase
- Thread_V2_TypeGroup1.UserStackLimit
- Thread_V2_TypeGroup1.StartAddr
- Thread_V2_TypeGroup1.Win32StartAddr
- Thread_V2_TypeGroup1.TebBase
- Thread_V2_TypeGroup1.SubProcessTag
api_type:
- NA
api_location: ''
ms.openlocfilehash: 15b24c827d99386206b778675f93fbe1a507cf0ec849caa066e0a438f413d101
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814007"
---
# <a name="thread_v2_typegroup1-class"></a>Classe \_ \_ TypeGroup1 do Thread V2

Essa classe é a classe de tipo de evento para eventos de início e término de thread.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V2_TypeGroup1 : Thread_V2
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  uint32 TebBase;
  uint32 SubProcessTag;
};
```

## <a name="members"></a>Membros

A **classe \_ \_ TypeGroup1 do Thread V2** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ \_ TypeGroup1 do Thread V2** tem essas propriedades.

<dl> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(1), Format("x")
</dt> </dl>

Identificador de processo do thread envolvido no evento.

</dd> <dt>

StackBase
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(3), Pointer
</dt> </dl>

Endereço base da pilha do thread.

</dd> <dt>

StackLimit
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(4), Pointer
</dt> </dl>

Limite da pilha do thread.

</dd> <dt>

StartAddr
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(7), Pointer
</dt> </dl>

Endereço de memória no qual o rastreamento é iniciado.

</dd> <dt>

SubProcessTag
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(10), Format("x")
</dt> </dl>

Identifica o serviço se o thread pertence a um serviço; caso contrário, zero.

</dd> <dt>

TebBase
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(9), Pointer
</dt> </dl>

Endereço base do bloco de ambiente de thread.

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(2), Format("x")
</dt> </dl>

Identificador de thread do thread envolvido no evento.

</dd> <dt>

UserStackBase
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(5), Pointer
</dt> </dl>

Endereço base da pilha de modo de usuário do thread.

</dd> <dt>

UserStackLimit
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(6), Pointer
</dt> </dl>

Limite da pilha de modo de usuário do thread.

</dd> <dt>

Win32StartAddr
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(8), Pointer
</dt> </dl>

Endereço inicial da função a ser executada por esse thread.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os tipos de evento DCStart e DCEnd enumeram os threads que estão sendo executados no momento em que a sessão do kernel é iniciada e termina, respectivamente.

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

 

 




