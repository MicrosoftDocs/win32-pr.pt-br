---
title: Controle COMBOBOX (menus e outros recursos)
description: Define um controle de caixa de combinação (uma caixa de combinação).
ms.assetid: 0a0fcfa8-b65c-44c1-89d8-f5020af10f0f
keywords:
- Menus de controle de COMBOBOX e outros recursos
topic_type:
- apiref
api_name:
- COMBOBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 311cb45282b949a166add8d3aececc0698803fe5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365906"
---
# <a name="combobox-control"></a>Controle COMBOBOX

Define um controle de caixa de combinação (uma caixa de combinação). Uma caixa de combinação consiste em uma caixa de texto estática ou em uma caixa de edição combinada com uma caixa de listagem. A caixa de listagem pode ser exibida em todos os momentos ou obtida pelo usuário. Se a caixa de combinação contiver uma caixa de texto estática, a caixa de texto sempre exibirá a seleção (se houver) na parte da caixa de listagem da caixa de combinação. Se ele usar uma caixa de edição, o usuário poderá digitar a seleção desejada; a caixa de listagem realça o primeiro item (se houver) que corresponde ao que o usuário inseriu na caixa de edição. O usuário pode selecionar o item realçado na caixa de listagem para concluir a escolha. Além disso, a caixa de combinação pode ser desenhada pelo proprietário e da altura fixa ou variável.

``` syntax
COMBOBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

Estilos de controle. Esse valor pode ser uma combinação dos estilos de classe COMBOBOX e de qualquer um dos seguintes estilos **: \_ WS TabStop**, **WS \_ Group**, **WS \_ VSCROLL** e **WS \_ Disabled**.

Se você não especificar um estilo, o estilo padrão será `CBS_SIMPLE | WS_TABSTOP` .

</dd> </dl>

O parâmetro *Height* aplica-se à altura de uma caixa de combinação com uma lista suspensa totalmente expandida.

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).

## <a name="examples"></a>Exemplos

Este exemplo define um controle de caixa de combinação com uma barra de rolagem vertical:

``` syntax
COMBOBOX 777, 10, 10, 50, 54, CBS_SIMPLE | WS_VSCROLL | WS_TABSTOP 
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Caixas de combinação](../controls/about-combo-boxes.md)
</dt> </dl>

 

 