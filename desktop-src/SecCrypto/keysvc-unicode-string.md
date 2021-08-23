---
description: A estrutura KEYSVC \_ UNICODE \_ STRING define uma cadeia de caracteres Unicode e um comprimento máximo para a cadeia de caracteres. Essa estrutura é usada pela função RKeyPFXInstall.
ms.assetid: 12142543-5c53-4638-9fd7-f523594142c8
title: KEYSVC_UNICODE_STRING estrutura (Rkeysvcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_UNICODE_STRING
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: ac1e82ab481b9844e8a21940112c6014a19f111cab53db2974c488dff0982027
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622326"
---
# <a name="keysvc_unicode_string-structure"></a>Estrutura KEYSVC \_ UNICODE \_ STRING

A **estrutura KEYSVC \_ UNICODE \_ STRING** define uma cadeia de caracteres [*Unicode*](../secgloss/u-gly.md) e um comprimento máximo para a cadeia de caracteres. Essa estrutura é usada pela [**função RKeyPFXInstall.**](rkeypfxinstall.md)

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _KEYSVC_UNICODE_STRING {
  USHORT Length;
  USHORT MaximumLength;
  USHORT *Buffer;
} KEYSVC_UNICODE_STRING, *PKEYSVC_UNICODE_STRING;
```



## <a name="members"></a>Membros

<dl> <dt>

**Comprimento**
</dt> <dd>

Um **valor USHORT** que especifica o comprimento, em bytes, usado para **Buffer**.

</dd> <dt>

**MaximumLength**
</dt> <dd>

Um **valor USHORT** que especifica o comprimento máximo, em bytes, permitido para **Buffer**.

</dd> <dt>

**Buffer**
</dt> <dd>

Um ponteiro para um **USHORT que** representa a cadeia de caracteres Unicode.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> <dt>

[**KEYSVC \_ BLOB**](keysvc-blob.md)
</dt> </dl>

 

 
