---
description: Contém informações que o Gerenciador de Arquivos usa para adicionar uma cadeia de caracteres de Ajuda para um menu ou item de comando da barra de ferramentas.
title: FMS_HELPSTRING (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b3ae7f86-5d58-47fa-87bd-e4e6a3541a93
ms.openlocfilehash: 85c7c94f91cad962239745d5dffa82898ef4ad0539431122106f7d85fdaff1c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224115"
---
# <a name="fms_helpstring-structure"></a>Estrutura HELPSTRING do FMS \_

Contém informações que o Gerenciador de Arquivos usa para adicionar uma cadeia de caracteres de Ajuda para um menu ou item de comando da barra de ferramentas.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _FMS_HELPSTRING {
  INT       idCommand;
  HMENU     hMenu;
  __wchar_t szHelp[128];
} FMS_HELPSTRING;
```



## <a name="members"></a>Membros

<dl> <dt>

**idCommand**
</dt> <dd>

Tipo: **INT**

</dd> <dd>

O identificador do item de comando.

</dd> <dt>

**Hmenu**
</dt> <dd>

Tipo: **HMENU**

</dd> <dd>

O identificador da barra de menus.

</dd> <dt>

**szHelp**
</dt> <dd>

Tipo: **\_ \_ wchar \_ t \[ 128 \]**

</dd> <dd>

A cadeia de caracteres terminada em nulo que recebe o texto da Ajuda.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FMEVENT \_ HELPMENUITEM**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




