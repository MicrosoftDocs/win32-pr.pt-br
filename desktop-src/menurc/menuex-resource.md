---
title: Recurso MENUEX
description: Define o conteúdo de um recurso de menu. | Recurso MENUEX
ms.assetid: a83e1e78-2af4-4257-906e-7eb6d98bcbc8
keywords:
- Menuex menus de recursos e outros recursos
topic_type:
- apiref
api_name:
- MENUEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec78bd0d33b48b11de77fe7742affb4265160752ffad30d72ecf3e9c173bb77c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825936"
---
# <a name="menuex-resource"></a>Recurso MENUEX

Define o conteúdo de um recurso de menu. Um recurso de menu é uma coleção de informações que define a aparência e a função de um menu de aplicativo. Um menu é uma ferramenta de entrada especial que permite que um usuário selecione comandos e abra submenus em uma lista de itens de menu. Ele também define o seguinte:

-   Identificadores de ajuda em menus.
-   Identificadores em menus.
-   Uso dos sinalizadores de tipo **MFT \_ \** _ e _*sinalizadores de estado \_ \* MFS.*_ Para obter mais informações sobre esses sinalizadores, consulte a [estrutura _ *MENUITEMINFO.* *](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)

``` syntax
menuID MENUEX{ [{[MENUITEM itemText [,[id][, [type][, state]]]] | 
    POPUP itemText [,[id][, [type][, [state][, helpID]]]] { popupBody } } . . .]}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="MENUITEM"></span><span id="menuitem"></span>[**Menuitem**](menuitem-statement.md)
</dt> <dd>

Define um item de menu.

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*
</dt> <dd>

Cadeia de caracteres que contém o texto do item de menu. Para obter mais informações, consulte [**MENUITEM**](menuitem-statement.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Expressão numérica que indica o identificador do item de menu.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*Tipo*
</dt> <dd>

Expressão numérica que indica o tipo do item de menu Para usar os valores de tipo MFT predefinidos, inclua a seguinte instrução \_ \* no arquivo .rc:`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*Estado*
</dt> <dd>

Expressão numérica que indica o estado do item de menu Para usar os valores de estado predefinidos do MFS, inclua a \_ \* instrução a seguir em seu . Arquivo RC:`#include "winuser.h"`

</dd> </dl> </dd> <dt>

<span id="POPUP"></span><span id="popup"></span>[**Popup**](popup-resource.md)
</dt> <dd>

Define um item de menu que tem um submenu associado a ele.

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*
</dt> <dd>

Cadeia de caracteres que contém o texto do item de menu.

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Expressão numérica que indica o identificador do item de menu.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*Tipo*
</dt> <dd>

Expressão numérica que indica o tipo do item de menu Para usar os valores de tipo MFT predefinidos, inclua a \_ \* instrução a seguir em seu . Arquivo RC:`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*Estado*
</dt> <dd>

Expressão numérica que indica o estado do item de menu Para usar os valores de estado predefinidos do MFS, inclua a seguinte instrução \_ \* no arquivo .rc:`#include "winuser.h"`

</dd> <dt>

<span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*
</dt> <dd>

Expressão numérica que indica o identificador usado para identificar o menu durante o processamento [**\_ da AJUDA do WM.**](../shell/wm-help.md)

</dd> </dl> </dd> <dt>

<span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*
</dt> <dd>

Contém qualquer combinação das instruções [**MENUITEM**](menuitem-statement.md) e [**POPUP.**](popup-resource.md)

</dd> </dl>

Determinados atributos também têm suporte para compatibilidade com backward. Para obter mais informações, consulte [Common Resource Attributes](common-resource-attributes.md).

## <a name="remarks"></a>Comentários

As operações aritméticas e boolianas válidas que podem ser contidas em qualquer uma das expressões numéricas nas instruções de **MENUEX** são as opções a seguir:

-   Adicionar ('+')
-   Subtrair ('-')
-   Subtração unária ('-')
-   NOT unário ('~')
-   AND ('&')
-   OR (' \| ')

## <a name="see-also"></a>Confira também

<dl> <dt>

[Uso de Menus](./using-menus.md)
</dt> <dt>

[**Aceleradores**](accelerators-resource.md)
</dt> <dt>

[**Características**](characteristics-statement.md)
</dt> <dt>

[**Diálogo**](dialog-resource.md)
</dt> <dt>

[**Língua**](language-statement.md)
</dt> <dt>

[**Menu**](menu-resource.md)
</dt> <dt>

[**Menuitem**](menuitem-statement.md)
</dt> <dt>

[**Popup**](popup-resource.md)
</dt> <dt>

[**Rcdata**](rcdata-resource.md)
</dt> <dt>

[**Stringtable**](stringtable-resource.md)
</dt> <dt>

[**Versão**](version-statement.md)
</dt> </dl>

 

 
