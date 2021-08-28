---
title: Recurso MENU
description: Define o conteúdo de um recurso de menu. | Recurso MENU
ms.assetid: fcb420b6-d42e-4044-89ee-028eed1f21ee
keywords:
- Menus de recurso menu e outros recursos
topic_type:
- apiref
api_name:
- MENU
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2b73afb5ef0547cbbccd8e5fdd87d7581edcaf19d5d73bc49ea3151166d882
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601936"
---
# <a name="menu-resource"></a>Recurso MENU

Define o conteúdo de um recurso de menu. Um recurso de menu é uma coleção de informações que define a aparência e a função de um menu de aplicativo. Um menu é uma ferramenta de entrada especial que permite que um usuário selecione comandos e abra submenus em uma lista de itens de menu.

``` syntax
menuID MENU  [optional-statements]  {item-definitions ... }
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*Menuid*
</dt> <dd>

Número que identifica o menu. Esse valor é uma cadeia de caracteres exclusiva ou um valor inteiro sem sinal de 16 bits exclusivo no intervalo de 1 a 65.535.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*
</dt> <dd>

Esse parâmetro pode ser zero de mais das instruções a seguir.



| Instrução                                                        | Descrição                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CHARACTERISTICS**](characteristics-statement.md) *dword*     | Informações definidas pelo usuário sobre um recurso que pode ser usado por ferramentas que leem e escrevem arquivos de recurso. Para obter mais informações, consulte [**CARACTERÍSTICAS**](characteristics-statement.md). |
| [**Language**](language-statement.md) *language*, *sublanguage* | Idioma do recurso. Para obter mais informações, consulte [**LANGUAGE**](language-statement.md).                                                                                            |
| [**VERSION**](version-statement.md) *dword*                     | Número de versão definido pelo usuário para o recurso que pode ser usado por ferramentas que leem e escrevem arquivos de recurso. Para obter mais informações, consulte [**VERSION**](version-statement.md).              |



 

</dd> </dl>

Determinados atributos também têm suporte para compatibilidade com backward. Para obter mais informações, consulte [Common Resource Attributes](common-resource-attributes.md).

## <a name="examples"></a>Exemplos

Veja a seguir um exemplo de uma **instrução MENU** completa:

``` syntax
sample MENU
{
     MENUITEM "&Soup", 100
     MENUITEM "S&alad", 101
     POPUP "&Entree"
     {
          MENUITEM "&Fish", 200
          MENUITEM "&Chicken", 201, CHECKED
          POPUP "&Beef"
          {
               MENUITEM "&Steak", 301
               MENUITEM "&Prime Rib", 302
          }
     }
     MENUITEM "&Dessert", 103
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Uso de Menus](./using-menus.md)
</dt> <dt>

[**Aceleradores**](accelerators-resource.md)
</dt> <dt>

[**Características**](characteristics-statement.md)
</dt> <dt>

[**Língua**](language-statement.md)
</dt> <dt>

[**MENUEX**](menuex-resource.md)
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

 

 
