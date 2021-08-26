---
title: Recurso pop-up
description: Define um item de menu que pode conter itens de menu e submenus.
ms.assetid: afca21c7-605e-4354-b6ec-576b81389b69
keywords:
- Menus de recursos pop-up e outros recursos
topic_type:
- apiref
api_name:
- POPUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f134b2d5801bc5003be6f45b42d13f1668c2e684b5f63fe0aed1f2c9c0400860
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952336"
---
# <a name="popup-resource"></a>Recurso pop-up

Define um item de menu que pode conter itens de menu e submenus.

``` syntax
POPUP text, [optionlist] {item-definitions ...}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*texto*
</dt> <dd>

Cadeia de caracteres que contém o nome do menu. Essa cadeia de caracteres deve ser colocada entre aspas duplas (**"**).

</dd> <dt>

<span id="optionlist"></span><span id="OPTIONLIST"></span>*opção*
</dt> <dd>

Esse parâmetro especifica opções de menu redefinidas que especificam a aparência do item de menu. Esse parâmetro opcional pode ser um ou mais dos seguintes.



| Opção           | Descrição                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CHECK**      | O item de menu tem uma marca de seleção ao lado dele. Essa opção não é válida para um menu de nível superior.                                                                                 |
| **ESMAECIDO**       | O item de menu está inicialmente inativo e aparece no menu em cinza ou em uma tonalidade clareada da cor do texto do menu. Esta opção não pode ser usada com a opção **inativa** . |
| **AJUDA**         | Identifica um item de ajuda. O item de menu é colocado na posição mais à direita na barra de menus.                                                                            |
| **INATIVO**     | O item de menu é exibido, mas não pode ser selecionado. Esta opção não pode ser usada com a opção **cinza** .                                                              |
| **MENUBARBREAK** | O mesmo que **MENUBREAK** , exceto que para menus pop-up, ele separa a nova coluna da coluna antiga com uma linha vertical.                                             |
| **MENUBREAK**    | Coloca o item de menu em uma nova linha para itens de barra de menus estáticos. Para menus, ele coloca o item de menu em uma nova coluna sem linha de divisão entre as colunas.           |



 

</dd> </dl>

Alguns atributos também têm suporte para compatibilidade com versões anteriores. Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso da instrução **Popup** :

``` syntax
chem MENU
{
    POPUP "&Elements"
    {
         MENUITEM "&Oxygen", 200
         MENUITEM "&Carbon", 201, CHECKED
         MENUITEM "&Hydrogen", 202
         MENUITEM SEPARATOR
         MENUITEM "&Sulfur", 203
         MENUITEM "Ch&lorine", 204
    } 
    POPUP "&Compounds"
    {
         POPUP "&Sugars"
         {
            MENUITEM "&Glucose", 301
            MENUITEM "&Sucrose", 302, CHECKED
            MENUITEM "&Lactose", 303, MENUBREAK
            MENUITEM "&Fructose", 304
         }
         POPUP "&Acids"
         {
              "&Hydrochloric", 401
              "&Sulfuric", 402
         }
    }
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ADICIONARMENU**](menu-resource.md)
</dt> <dt>

[**MENUITEM**](menuitem-statement.md)
</dt> </dl>

 

 




