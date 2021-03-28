---
description: Contém informações que o Gerenciador de arquivos usa para adicionar uma cadeia de caracteres de ajuda para um menu ou item de comando de barra de ferramentas.
title: Estrutura de FMS_HELPSTRING (Wfext. h)
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
ms.openlocfilehash: c934409712ae740797eb3b5af0b55c50ff125342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988998"
---
# <a name="fms_helpstring-structure"></a>\_Estrutura HelpString do FMS

Contém informações que o Gerenciador de arquivos usa para adicionar uma cadeia de caracteres de ajuda para um menu ou item de comando de barra de ferramentas.

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

Tipo: **int**

</dd> <dd>

O identificador do item de comando.

</dd> <dt>

**hMenu**
</dt> <dd>

Tipo: **HMENU**

</dd> <dd>

O identificador da barra de menus.

</dd> <dt>

**szHelp**
</dt> <dd>

Tipo: **\_ \_ WCHAR \_ t \[ 128 \]**

</dd> <dd>

A cadeia de caracteres terminada em nulo que recebe o texto de ajuda.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FMEVENT \_ HELPMENUITEM**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




