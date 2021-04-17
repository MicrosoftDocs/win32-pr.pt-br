---
description: A estrutura PROPERTYINSTEX define uma instância de forma livre e de propriedade estendida.
ms.assetid: a2316baf-07e2-4617-bb35-e20cfb11fbcb
title: Estrutura PROPERTYINSTEX (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINSTEX
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f7b196d30e96f9d047f7f923d969d65a918aa4f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787044"
---
# <a name="propertyinstex-structure"></a>Estrutura PROPERTYINSTEX

A estrutura **PROPERTYINSTEX** define uma instância de forma livre e de propriedade estendida.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PROPERTYINSTEX {
  WORD    Length;
  WORD    LengthEx;
  ULPVOID lpData;
  union {
    BYTE          Byte[];
    WORD          Word[];
    DWORD         Dword[];
    LARGE_INTEGER LargeInt[];
    SYSTEMTIME    SysTime[];
    TYPED_STRING  TypedString;
  };
} PROPERTYINSTEX;
```



## <a name="members"></a>Membros

<dl> <dt>

**Comprimento**
</dt> <dd>

Comprimento dos dados em bytes.

</dd> <dt>

**LengthEx**
</dt> <dd>

Comprimento dos dados estendidos.

</dd> <dt>

**lpData**
</dt> <dd>

Ponteiro para os dados estendidos.

</dd> <dt>

**Byte**
</dt> <dd>

Ponteiro para os dados de **byte** .

</dd> <dt>

**Word**
</dt> <dd>

Ponteiro para os dados do **Word** .

</dd> <dt>

**DWORD**
</dt> <dd>

Ponteiro para os dados **DWORD** .

</dd> <dt>

**LargeInt**
</dt> <dd>

Ponteiro para os dados de **LARGEINT** .

</dd> <dt>

**SysTime**
</dt> <dd>

Ponteiro para os dados de **SYSTEMTIME** .

</dd> <dt>

**Tipo de**
</dt> <dd>

Uma cadeia de caracteres tipada que pode ter dados estendidos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




