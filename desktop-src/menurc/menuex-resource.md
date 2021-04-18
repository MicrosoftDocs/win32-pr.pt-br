---
title: Recurso MENUEX
description: Define o conteúdo de um recurso de menu. | Recurso MENUEX
ms.assetid: a83e1e78-2af4-4257-906e-7eb6d98bcbc8
keywords:
- Menus de recursos do MENUEX e outros recursos
topic_type:
- apiref
api_name:
- MENUEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ed379fb97d2795a166571fb48cde2c233021a33
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105764183"
---
# <a name="menuex-resource"></a>Recurso MENUEX

Define o conteúdo de um recurso de menu. Um recurso de menu é uma coleção de informações que define a aparência e a função de um menu de aplicativo. Um menu é uma ferramenta de entrada especial que permite que um usuário selecione comandos e abra submenus de uma lista de itens de menu. Ele também define o seguinte:

-   Identificadores de ajuda em menus.
-   Identificadores em menus.
-   Uso dos sinalizadores de tipo **MFT \_ \** _ e sinalizadores de estado _*MFS \_ \**_ . Para obter mais informações sobre esses sinalizadores, consulte a estrutura [_ *MENUITEMINFO* *](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .

``` syntax
menuID MENUEX{ [{[MENUITEM itemText [,[id][, [type][, state]]]] | 
    POPUP itemText [,[id][, [type][, [state][, helpID]]]] { popupBody } } . . .]}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="MENUITEM"></span><span id="menuitem"></span>[**MENUITEM**](menuitem-statement.md)
</dt> <dd>

Define um item de menu.

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*Texto*
</dt> <dd>

Cadeia de caracteres que contém o texto do item de menu. Para obter mais informações, consulte [**MenuItem**](menuitem-statement.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*sessão*
</dt> <dd>

Expressão numérica que indica o identificador do item de menu.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*Escreva*
</dt> <dd>

Expressão numérica que indica o tipo do item de menu para usar os valores de tipo de MFT predefinidos \_ \* , inclua a seguinte instrução no arquivo. rc:`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*status*
</dt> <dd>

Expressão numérica que indica o estado do item de menu para usar os valores de estado de MFS predefinidos \_ \* , inclua a seguinte instrução em seu. Arquivo RC:`#include "winuser.h"`

</dd> </dl> </dd> <dt>

<span id="POPUP"></span><span id="popup"></span>[**POP-up**](popup-resource.md)
</dt> <dd>

Define um item de menu que tem um submenu associado a ele.

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*Texto*
</dt> <dd>

Cadeia de caracteres que contém o texto do item de menu.

</dd> <dt>

<span id="id"></span><span id="ID"></span>*sessão*
</dt> <dd>

Expressão numérica que indica o identificador do item de menu.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*Escreva*
</dt> <dd>

Expressão numérica que indica o tipo do item de menu para usar os valores de tipo de MFT predefinidos \_ \* , inclua a seguinte instrução em seu. Arquivo RC:`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*status*
</dt> <dd>

Expressão numérica que indica o estado do item de menu para usar os valores de estado de MFS predefinidos \_ \* , inclua a seguinte instrução no arquivo. rc:`#include "winuser.h"`

</dd> <dt>

<span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*HelpID*
</dt> <dd>

Expressão numérica que indica o identificador usado para identificar o menu durante o processamento da [**\_ ajuda do WM**](../shell/wm-help.md) .

</dd> </dl> </dd> <dt>

<span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*
</dt> <dd>

Contém qualquer combinação das instruções [**MenuItem**](menuitem-statement.md) e [**Popup**](popup-resource.md) .

</dd> </dl>

Alguns atributos também têm suporte para compatibilidade com versões anteriores. Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).

## <a name="remarks"></a>Comentários

As operações aritméticas e booleanas válidas que podem estar contidas em qualquer uma das expressões numéricas nas instruções de **MENUEX** são as seguintes:

-   Adicionar (' + ')
-   Subtrair ('-')
-   Menos unário ('-')
-   Não unário (' ~ ')
-   E (' & ')
-   OU (' \| ')

## <a name="see-also"></a>Confira também

<dl> <dt>

[Uso de Menus](./using-menus.md)
</dt> <dt>

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**CARACTERÍSTICAS**](characteristics-statement.md)
</dt> <dt>

[**'**](dialog-resource.md)
</dt> <dt>

[**IDIOMA**](language-statement.md)
</dt> <dt>

[**ADICIONARMENU**](menu-resource.md)
</dt> <dt>

[**MENUITEM**](menuitem-statement.md)
</dt> <dt>

[**POP-up**](popup-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Versão**](version-statement.md)
</dt> </dl>

 

 
