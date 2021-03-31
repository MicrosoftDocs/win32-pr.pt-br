---
title: Controle de caixa de seleção
description: Define um controle de caixa de seleção automática.
ms.assetid: 086f5dd3-267f-4ec6-be37-4e9402f7aede
keywords:
- Menus de controle de caixa de seleção AUTOe outros recursos
topic_type:
- apiref
api_name:
- AUTOCHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 842bb3ede2b1f96f3e5b343e351e047d112a8403
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640664"
---
# <a name="autocheckbox-control"></a>Controle de caixa de seleção

Define um controle de caixa de seleção automática. O controle é um pequeno retângulo (caixa de seleção) que tem o texto especificado exibido ao lado (normalmente, à direita). Quando o usuário escolhe o controle, o controle realça o retângulo e envia uma mensagem para sua janela pai.

A instrução **AUTOCHECKBOX** só pode ser usada no corpo de uma instrução [**Dialog**](dialog-resource.md) ou [**DIALOGEX**](dialogex-resource.md) .

``` syntax
AUTOCHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

Estilos do controle. Esse valor pode ser uma combinação dos estilos de classe de botão **BS \_ AUTOCHECKBOX** e **WS \_ TabStop** e **WS \_ Group** .

Se você não especificar um estilo, o estilo padrão será `BS_AUTOCHECKBOX | WS_TABSTOP` .

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).

## <a name="see-also"></a>Consulte também

<dl> <dt>

[**AUTO3STATE**](auto3state-control.md)
</dt> <dt>

[Estilos de botão](../controls/button-styles.md)
</dt> <dt>

[**VERIFICAÇÃO**](checkbox-control.md)
</dt> <dt>

[**CONTROLO**](control-control.md)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> </dl>

 

 