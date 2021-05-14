---
description: Contém informações sobre um botão que uma DLL de extensão do Gerenciador de arquivos está adicionando à barra de ferramentas do Gerenciador de arquivos.
title: Estrutura de EXT_BUTTON (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXT_BUTTON
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8cd29a06-0f38-4285-9092-647a391b72d7
ms.openlocfilehash: 6d1505ef7b330f0e935136eacaf808da3add8cd8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843147"
---
# <a name="ext_button-structure"></a>\_Estrutura do botão ext

Contém informações sobre um botão que uma DLL de extensão do Gerenciador de arquivos está adicionando à barra de ferramentas do Gerenciador de arquivos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagEXT_BUTTON {
  WORD idCommand;
  WORD idsHelp;
  WORD fsStyle;
} EXT_BUTTON, *LPEXT_BUTTON;
```



## <a name="members"></a>Membros

<dl> <dt>

**idCommand**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Um identificador de comando para o botão.

</dd> <dt>

**idsHelp**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O identificador da cadeia de caracteres de ajuda para o botão.

</dd> <dt>

**fsStyle**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O estilo do botão.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FMEVENT \_ TOOLBARLOAD**](fmevent-toolbarload.md)
</dt> <dt>

[**TOOLBARLOAD do FMS \_**](fms-toolbarload.md)
</dt> </dl>

 

 




