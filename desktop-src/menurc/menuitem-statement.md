---
title: Instrução MENUITEM
description: Define um item de menu.
ms.assetid: b154211a-5267-4dcf-9e70-ac36671d10d3
keywords:
- Menus de instrução MENUITEM e outros recursos
topic_type:
- apiref
api_name:
- MENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45bca50025e1c9136c22166d6d3f758c5c9b5819a9328d33d375195285f1d4f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092186"
---
# <a name="menuitem-statement"></a>Instrução MENUITEM

Define um item de menu.

``` syntax
MENUITEM text, result, [optionlist]  
MENUITEM SEPARATOR
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*texto*
</dt> <dd>

O nome do item de menu.

A cadeia de caracteres pode conter os caracteres de escape **\\ t** e **\\ a**. O caractere **\\ t** insere uma guia na cadeia de caracteres e é usado para alinhar o texto em colunas. Os caracteres de tabulação devem ser usados somente em menus, não em barras de menus. (Para obter informações sobre menus, consulte [**recurso pop-up**](popup-resource.md).) O caractere **\\ um** alinha todo o texto que o segue à direita até a barra de menus ou menu pop-up.

</dd> <dt>

<span id="result"></span><span id="RESULT"></span>*disso*
</dt> <dd>

Um número que especifica o resultado gerado quando o usuário seleciona o item de menu. Esse parâmetro usa um valor inteiro. Menu – os resultados do item são sempre inteiros; Quando o usuário clica no nome do item de menu, o resultado é enviado para a janela que possui o menu.

</dd> <dt>

<span id="optionlist"></span><span id="OPTIONLIST"></span>*opção*
</dt> <dd>

A aparência do item de menu. Esse parâmetro opcional usa uma ou mais das seguintes opções de menu redefinida, separadas por vírgulas ou espaços.



| Opção           | Descrição                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CHECK**      | O item de menu tem uma marca de seleção ao lado dele.                                                                                                                                |
| **ESMAECIDO**       | O item de menu está inicialmente inativo e aparece no menu em cinza ou em uma tonalidade clareada da cor do texto do menu. Esta opção não pode ser usada com a opção **inativa** . |
| **AJUDA**         | Identifica um item de ajuda. Essa opção não tem efeito sobre a aparência do item de menu.                                                                                 |
| **INATIVO**     | O item de menu é exibido, mas não pode ser selecionado. Esta opção não pode ser usada com a opção **cinza** .                                                              |
| **MENUBARBREAK** | O mesmo que **MENUBREAK** , exceto que para menus pop-up, ele separa a nova coluna da coluna antiga com uma linha vertical.                                             |
| **MENUBREAK**    | Coloca o item de menu em uma nova linha para itens de barra de menus estáticos. Para menus, ele coloca o item de menu em uma nova coluna sem linha de divisão entre as colunas.           |



 

</dd> <dt>

<span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**SEPARADOR MENUITEM**
</dt> <dd>

O formulário **SEparador MenuItem** da instrução **MenuItem** cria um item de menu inativo que serve como uma barra de divisão entre dois itens de menu ativos em um menu.

</dd> </dl>

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso das instruções de **SEparador** **MenuItem** e MenuItem:

``` syntax
MENUITEM "&Roman", 206, CHECKED, GRAYED
MENUITEM SEPARATOR
MENUITEM "&Blackletter", 301
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ADICIONARMENU**](menu-resource.md)
</dt> <dt>

[**POP-up**](popup-resource.md)
</dt> </dl>

 

 




