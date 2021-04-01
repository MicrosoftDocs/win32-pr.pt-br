---
title: Controle LISTBOX (menus e outros recursos)
description: Define controles comumente usados para uma caixa de diálogo ou janela. O controle é um retângulo que contém uma lista de cadeias de caracteres (como nomes de filename) da qual o usuário pode selecionar.
ms.assetid: 78f6d36e-5079-4f04-87e4-ca55a1161a51
keywords:
- Menus de controle de caixa de listagem e outros recursos
topic_type:
- apiref
api_name:
- LISTBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f062387463917438a988c3b023ca656beef722
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084527"
---
# <a name="listbox-control"></a>Controle LISTBOX

Define controles comumente usados para uma caixa de diálogo ou janela. O controle é um retângulo que contém uma lista de cadeias de caracteres (como nomes de filename) da qual o usuário pode selecionar.

A instrução **ListBox** , que só pode ser usada em uma [**DIALOGEX**](dialogex-resource.md) ou instrução de **janela** , define o identificador, as dimensões e os atributos de uma janela de controle.

``` syntax
LISTBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

Estilos de controle. Esse valor pode ser uma combinação dos estilos de classe da caixa de listagem e de qualquer um dos seguintes estilos: **WS \_ Border** e **WS \_ VSCROLL**.

Se você não especificar um estilo, o estilo padrão será `LBS_NOTIFY | WS_BORDER` .

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).

## <a name="examples"></a>Exemplos

Este exemplo define um controle de caixa de listagem cujo identificador é 101:

``` syntax
LISTBOX 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**COMBOBOX**](combobox-control.md)
</dt> <dt>

[Caixas de listagem](../controls/about-list-boxes.md)
</dt> </dl>

 

 