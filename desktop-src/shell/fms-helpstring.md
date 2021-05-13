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
ms.openlocfilehash: 4e9521df91619d108c7a03b6574926147fc2b04a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842207"
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

 

 




