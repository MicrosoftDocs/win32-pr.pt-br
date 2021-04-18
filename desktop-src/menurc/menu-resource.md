---
title: Recurso de MENU
description: Define o conteúdo de um recurso de menu. | Recurso de MENU
ms.assetid: fcb420b6-d42e-4044-89ee-028eed1f21ee
keywords:
- Menus de recursos de MENU e outros recursos
topic_type:
- apiref
api_name:
- MENU
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5cdb564c7bf012255b339a13691d2ecf214a86
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105787685"
---
# <a name="menu-resource"></a>Recurso de MENU

Define o conteúdo de um recurso de menu. Um recurso de menu é uma coleção de informações que define a aparência e a função de um menu de aplicativo. Um menu é uma ferramenta de entrada especial que permite que um usuário selecione comandos e abra submenus de uma lista de itens de menu.

``` syntax
menuID MENU  [optional-statements]  {item-definitions ... }
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*menu de atalho*
</dt> <dd>

Número que identifica o menu. Esse valor é uma cadeia de caracteres exclusiva ou um valor inteiro não assinado de 16 bits no intervalo de 1 a 65.535.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instruções opcionais*
</dt> <dd>

Esse parâmetro pode ser zero de mais das instruções a seguir.



| Instrução                                                        | Descrição                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Características**](characteristics-statement.md) *DWORD*     | Informações definidas pelo usuário sobre um recurso que pode ser usado por ferramentas que lêem e gravam arquivos de recursos. Para obter mais informações, consulte [**características**](characteristics-statement.md). |
| [](language-statement.md) *Idioma* do idioma, *subidioma* | Idioma do recurso. Para obter mais informações, consulte [**Language**](language-statement.md).                                                                                            |
| [](version-statement.md) *DWORD* da versão                     | Número de versão definido pelo usuário para o recurso que pode ser usado por ferramentas que lêem e gravam arquivos de recursos. Para obter mais informações, consulte [**versão**](version-statement.md).              |



 

</dd> </dl>

Alguns atributos também têm suporte para compatibilidade com versões anteriores. Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).

## <a name="examples"></a>Exemplos

Veja a seguir um exemplo de uma instrução de **menu** completa:

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

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**CARACTERÍSTICAS**](characteristics-statement.md)
</dt> <dt>

[**IDIOMA**](language-statement.md)
</dt> <dt>

[**MENUEX**](menuex-resource.md)
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

 

 
