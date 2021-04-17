---
description: A \_ estrutura de cadeia de caracteres Unicode KEYSVC \_ define uma cadeia de caracteres Unicode e um comprimento máximo para a cadeia de caracteres. Essa estrutura é usada pela função RKeyPFXInstall.
ms.assetid: 12142543-5c53-4638-9fd7-f523594142c8
title: Estrutura de KEYSVC_UNICODE_STRING (Rkeysvcc. h)
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
ms.openlocfilehash: 5424fa103b2bbbadd735dbda0bb92f9dea21787b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782948"
---
# <a name="keysvc_unicode_string-structure"></a>\_Estrutura de \_ cadeia de caracteres Unicode KEYSVC

A estrutura de **\_ cadeia de \_ caracteres Unicode KEYSVC** define uma cadeia de caracteres [*Unicode*](../secgloss/u-gly.md) e um comprimento máximo para a cadeia de caracteres. Essa estrutura é usada pela função [**RKeyPFXInstall**](rkeypfxinstall.md) .

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

Um valor **UShort** que especifica o comprimento, em bytes, usado para o **buffer**.

</dd> <dt>

**MaximumLength**
</dt> <dd>

Um valor **UShort** que especifica o comprimento máximo, em bytes, permitido para o **buffer**.

</dd> <dt>

**Buffer**
</dt> <dd>

Um ponteiro para um **UShort** que representa a cadeia de caracteres Unicode.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> <dt>

[**\_blob KEYSVC**](keysvc-blob.md)
</dt> </dl>

 

 
