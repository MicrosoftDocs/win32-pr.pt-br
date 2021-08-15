---
title: Controle LISTBOX (menus e outros recursos)
description: Define controles comumente usados para uma caixa de diálogo ou janela. O controle é um retângulo que contém uma lista de cadeias de caracteres (como nomes de arquivo) do qual o usuário pode selecionar.
ms.assetid: 78f6d36e-5079-4f04-87e4-ca55a1161a51
keywords:
- Menus de controle LISTBOX e outros recursos
topic_type:
- apiref
api_name:
- LISTBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 676ea07f7d66a0d84997f0b2b22b9973c326db0fb603caedcc631caeffffaf98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119226339"
---
# <a name="listbox-control"></a>Controle LISTBOX

Define controles comumente usados para uma caixa de diálogo ou janela. O controle é um retângulo que contém uma lista de cadeias de caracteres (como nomes de arquivo) do qual o usuário pode selecionar.

A **instrução LISTBOX,** que só pode ser usada em uma instrução [**DIALOGEX**](dialogex-resource.md) ou **WINDOW,** define o identificador, as dimensões e os atributos de uma janela de controle.

``` syntax
LISTBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos de controle. Esse valor pode ser uma combinação dos estilos de classe de caixa de listagem e qualquer um dos seguintes estilos: **WS \_ BORDER** e **WS \_ VSCROLL.**

Se você não especificar um estilo, o estilo padrão será `LBS_NOTIFY | WS_BORDER` .

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [Common Control Parameters](common-control-parameters.md).

## <a name="examples"></a>Exemplos

Este exemplo define um controle de caixa de listagem cujo identificador é 101:

``` syntax
LISTBOX 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Combobox**](combobox-control.md)
</dt> <dt>

[Caixas de listagem](../controls/about-list-boxes.md)
</dt> </dl>

 

 