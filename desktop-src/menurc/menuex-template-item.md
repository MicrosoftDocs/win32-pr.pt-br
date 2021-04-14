---
title: Estrutura de MENUEX_TEMPLATE_ITEM
description: Define um item de menu em um modelo de menu estendido. Esta definição de estrutura é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: f6e2fd0a-16b8-48e3-8597-341085a7adbd
keywords:
- MENUEX_TEMPLATE_ITEM de menus de estrutura e outros recursos
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_ITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca1f73d1174590db5948f54f5c51c91a8c65a8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499681"
---
# <a name="menuex_template_item-structure"></a>Estrutura de item de \_ modelo MENUEX \_

Define um item de menu em um modelo de menu estendido. Esta definição de estrutura é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.

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

**dwType**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O tipo de item de menu. Esse membro pode ser uma combinação dos valores de tipo (começando com MFT) listados com a estrutura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .

</dd> <dt>

**dwState**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O estado do item de menu. Esse membro pode ser uma combinação dos valores de estado (começando com MFS) listados com a estrutura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .

</dd> <dt>

**uId**
</dt> <dd>

Tipo: **uint**

</dd> <dd>

O identificador do item de menu. Esse é um valor definido pelo aplicativo que identifica o item de menu. Em um recurso de menu estendido, os itens que abrem menus ou submenus suspensos, bem como itens de comando, podem ter identificadores.

</dd> <dt>

**wFlags**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Especifica se o item de menu é o último item na barra de menus, no menu suspenso, no submenu ou no menu de atalho e se é um item que abre um menu suspenso ou submenu. Esse membro pode ser zero ou mais desses valores. Para aplicativos de 32 bits, esse membro é uma palavra; para aplicativos de 16 bits, é um byte.

<dt>

0x80
</dt> <dd>

A estrutura define o último item de menu na barra de menus, no menu suspenso, no submenu ou no menu de atalho.

</dd> <dt>

0x01
</dt> <dd>

A estrutura define um item que abre um menu suspenso ou submenu. As estruturas subsequentes definem itens de menu no menu suspenso ou submenu suspenso correspondente.

</dd> </dl> </dd> <dt>

**szText**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

O texto do item de menu. Este membro é uma cadeia de caracteres Unicode terminada em nulo, alinhada em um limite de palavra. O tamanho da definição do item de menu varia dependendo do comprimento dessa cadeia de caracteres.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um modelo de menu estendido consiste em uma estrutura de [**\_ \_ cabeçalho de modelo MENUEX**](menuex-template-header.md) seguida por uma ou mais estruturas de **\_ \_ item de modelo MENUEX** contíguas. As estruturas de **\_ \_ item de modelo MENUEX** , que são variáveis de comprimento, são alinhadas nos limites **DWORD** . Para criar um menu a partir de um modelo de menu estendido na memória, use a função [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .

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

[**\_cabeçalho do modelo MENUEX \_**](menuex-template-header.md)
</dt> <dt>

[**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Menus](menus.md)
</dt> </dl>

 

 





