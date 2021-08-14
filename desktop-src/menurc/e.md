---
title: E (menus e outros recursos)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 14e12ba3-8451-4a93-a555-e1c9e6040a67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4f2423b002afe055c425978a643753e029d817eee5e7eccfc4379d2410f88ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461246"
---
# <a name="e-menus-and-other-resources"></a>E (menus e outros recursos)

[A](a.md) [B](b.md) [C](c.md) D E [F](f.md) G H [i](i.md) J K L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z

<dl> <dt>

<span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**Menus vazios não são permitidos**
</dt> <dd>

Uma palavra-chave **end** é exibida antes de qualquer item de menu ser definido na instrução de [**menu**](menu-resource.md) . os menus vazios não são permitidos pelo compilador de recursos do Microsoft Windows 32 (RC). Certifique-se de que você não tem aspas de abertura dentro da instrução de **menu** .

</dd> <dt>

<span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**FIM esperado na caixa de diálogo**
</dt> <dd>

A palavra-chave **end** deve aparecer no final de uma instrução de [**diálogo**](dialog-resource.md) . Verifique se não há aspas de abertura à esquerda da instrução anterior.

</dd> <dt>

<span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**FIM esperado no menu**
</dt> <dd>

A palavra-chave **end** deve aparecer no final de uma instrução de [**menu**](menu-resource.md) . Verifique se não há instruções **begin** e **end** incompatíveis.

</dd> <dt>

<span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Erro Creatingresource-nome**
</dt> <dd>

o compilador de recursos do Microsoft Windows 32 (RC) não pôde criar o recurso binário especificado (. RES). Certifique-se de que ele não está sendo criado em uma unidade somente leitura. Use a opção **/v** para descobrir se o arquivo está sendo criado.

</dd> <dt>

<span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Vírgula esperada na tabela do acelerador**
</dt> <dd>

o compilador de recursos do Microsoft Windows 32 (RC) requer uma vírgula entre os parâmetros *event* e *idvalue* na instrução [**accelerators**](accelerators-resource.md) .

</dd> <dt>

<span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Nome de classe de controle esperado**
</dt> <dd>

O parâmetro de *classe* de uma instrução de [**controle**](control-control.md) na instrução da [**caixa de diálogo**](dialog-resource.md) deve ser um dos seguintes tipos de controle: **Button**, [**ComboBox**](combobox-control.md), **Edit**, [**ListBox**](listbox-control.md), [**ScrollBar**](scrollbar-control.md), **static** ou User-defined. Verifique se a classe está grafada corretamente.

</dd> <dt>

<span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Nome de face da fonte esperado**
</dt> <dd>

O parâmetro de *tipo* da instrução **Font** na instrução da [**caixa de diálogo**](dialog-resource.md) deve ser uma cadeia de caracteres entre aspas duplas ("). Esse parâmetro especifica o nome de uma fonte.

</dd> <dt>

<span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Valor de ID esperado para MenuItem**
</dt> <dd>

A instrução de [**menu**](menu-resource.md) deve conter uma instrução [**MenuItem**](menuitem-statement.md) , que tem um inteiro ou uma constante simbólica no parâmetro *MenuID* .

</dd> <dt>

<span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Cadeia de menu esperada**
</dt> <dd>

Cada instrução [**MenuItem**](menuitem-statement.md) e [**Popup**](popup-resource.md) deve conter um parâmetro de *texto* . Esse parâmetro é uma cadeia de caracteres entre aspas duplas (") que especifica o nome do item de menu ou menu pop-up. Uma instrução **SEparadora MenuItem** não requer nenhuma cadeia de caracteres entre aspas.

</dd> <dt>

<span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Valor de comando numérico esperado**
</dt> <dd>

o compilador de recursos do Microsoft Windows (RC) estava esperando um parâmetro numérico *idvalue* na instrução [**accelerators**](accelerators-resource.md) . Certifique-se de que você usou uma instrução de [**\# definição**](-define.md) para especificar o valor e que a constante usada esteja grafada corretamente.

</dd> <dt>

<span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Constante numérica esperada na tabela de cadeia de caracteres**
</dt> <dd>

Uma constante numérica, definida em uma instrução de [**\# definição**](-define.md) , deve seguir imediatamente a palavra-chave **begin** em uma instrução [**STRINGTABLE**](stringtable-resource.md) .

</dd> <dt>

<span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Tamanho de ponto numérico esperado**
</dt> <dd>

O parâmetro de *pontos* da instrução de [**fonte**](font-statement.md) na instrução de [**diálogo**](dialog-resource.md) deve ser um valor de tamanho de ponto inteiro.

</dd> <dt>

<span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Constante de caixa de diálogo numérica esperada**
</dt> <dd>

Uma instrução de [**caixa de diálogo**](dialog-resource.md) requer valores inteiros para os parâmetros *x*, *y*, *Width* e *Height* . Verifique se esses valores, que estão incluídos após a palavra-chave da **caixa de diálogo** , não são negativos.

</dd> <dt>

<span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Cadeia de caracteres esperada em STRINGTABLE**
</dt> <dd>

Uma cadeia de caracteres é esperada após cada parâmetro de *stringid* numérico em uma instrução [**STRINGTABLE**](stringtable-resource.md) .

</dd> <dt>

<span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Cadeia de caracteres esperada ou comando acelerador de constante**
</dt> <dd>

o compilador de recursos do Microsoft Windows (RC) não pôde determinar qual chave estava sendo configurada para o acelerador. O parâmetro de *evento* na instrução [**Accelerators**](accelerators-resource.md) pode ser inválido.

</dd> <dt>

<span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**VALOR esperado, bloco ou palavra-chave END.**
</dt> <dd>

A estrutura [**VERSIONINFO**](versioninfo-resource.md) requer um **valor**, um **bloco** ou uma palavra-chave **end** .

</dd> <dt>

<span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Esperando número para ID**
</dt> <dd>

É esperado um número para o parâmetro de *ID* de uma instrução de [**controle**](control-control.md) na instrução da [**caixa de diálogo**](dialog-resource.md) . Verifique se você tem um número ou uma instrução de [**\# definição**](-define.md) para o identificador de controle.

</dd> <dt>

<span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Esperando cadeia de caracteres entre aspas para a chave**
</dt> <dd>

A cadeia de caracteres de chave após a palavra-chave de **bloco** ou **valor** deve ser colocada entre aspas duplas.

</dd> <dt>

<span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Esperando cadeia de caracteres entre aspas na classe da caixa de diálogo**
</dt> <dd>

O parâmetro de *classe* da instrução de [**classe**](class-statement.md) na instrução da [**caixa de diálogo**](dialog-resource.md) deve ser um inteiro ou uma cadeia de caracteres entre aspas duplas (").

</dd> <dt>

<span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Esperando cadeia de caracteres entre aspas no título da caixa de diálogo**
</dt> <dd>

O parâmetro *CaptionText* da instrução [**Caption**](caption-statement.md) na instrução [**Dialog**](dialog-resource.md) deve ser uma cadeia de caracteres, entre aspas duplas (").

</dd> </dl>

 

 




