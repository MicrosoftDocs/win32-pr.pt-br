---
title: MENUEX_TEMPLATE_ITEM estrutura
description: Define um item de menu em um modelo de menu estendido. Essa definição de estrutura é apenas para explicação; ele não está presente em nenhum arquivo de header padrão.
ms.assetid: f6e2fd0a-16b8-48e3-8597-341085a7adbd
keywords:
- menus MENUEX_TEMPLATE_ITEM estrutura e outros recursos
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_ITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6352c7ce596a59d69b21f1ba424ac50b471e13cd97320f0df184bce2e1abd295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733901"
---
# <a name="menuex_template_item-structure"></a>Estrutura DE \_ ITEM DE MODELO \_ MENUEX

Define um item de menu em um modelo de menu estendido. Essa definição de estrutura é apenas para explicação; ele não está presente em nenhum arquivo de header padrão.

## <a name="syntax"></a>Sintaxe

```C++
typedef struct {
  DWORD dwType;
  DWORD dwState;
  UINT  uId;
  WORD  wFlags;
  WCHAR szText[1];
} MENUEX_TEMPLATE_ITEM;
```

## <a name="members"></a>Membros

<dl> <dt>

**Dwtype**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O tipo de item de menu. Esse membro pode ser uma combinação dos valores de tipo (começando com MFT) listados com a [**estrutura MENUITEMINFO.**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)

</dd> <dt>

**Dwstate**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O estado do item de menu. Esse membro pode ser uma combinação dos valores de estado (começando com MFS) listados com a [**estrutura MENUITEMINFO.**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)

</dd> <dt>

**Uid**
</dt> <dd>

Tipo: **UINT**

</dd> <dd>

O identificador do item de menu. Esse é um valor definido pelo aplicativo que identifica o item de menu. Em um recurso de menu estendido, os itens que abrem menus suspensos ou submenus, bem como itens de comando, podem ter identificadores.

</dd> <dt>

**Wflags**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Especifica se o item de menu é o último item na barra de menus, menu suspenso, submenu ou menu de atalho e se é um item que abre um menu suspenso ou submenu. Esse membro pode ser zero ou mais desses valores. Para aplicativos de 32 bits, esse membro é uma palavra; para aplicativos de 16 bits, é um byte.

<dt>

0x80
</dt> <dd>

A estrutura define o último item de menu na barra de menus, menu suspenso, submenu ou menu de atalho.

</dd> <dt>

0x01
</dt> <dd>

A estrutura define um item que abre um menu suspenso ou submenu. As estruturas subsequentes definem itens de menu no submenu ou menu suspenso correspondente.

</dd> </dl> </dd> <dt>

**szText**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

O texto do item de menu. Esse membro é uma cadeia de caracteres Unicode terminada em nulo, alinhada em um limite de palavra. O tamanho da definição do item de menu varia dependendo do comprimento dessa cadeia de caracteres.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um modelo de menu estendido consiste em uma estrutura [**DE \_ \_ HEADER DE MODELO MENUEX**](menuex-template-header.md) seguida por uma ou mais estruturas de ITEM DE MODELO MENUEX contíguas. **\_ \_** As **\_ estruturas \_ MENUEX TEMPLATE ITEM,** que são variáveis de comprimento, são alinhadas em limites **DWORD.** Para criar um menu de um modelo de menu estendido na memória, use a [**função LoadMenuIndirect.**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[**HEADER \_ DO MODELO MENUEX \_**](menuex-template-header.md)
</dt> <dt>

[**Menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Menus](menus.md)
</dt> </dl>

 

 





