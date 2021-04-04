---
title: Controle AUTO3STATE
description: Define uma caixa de seleção automática de três Estados.
ms.assetid: 8b27367c-30d0-4591-93d0-756c65255b26
keywords:
- Menus de controle do AUTO3STATE e outros recursos
topic_type:
- apiref
api_name:
- AUTO3STATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de184a639de7beee7ac05bdf63609ae29a0f034b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084502"
---
# <a name="auto3state-control"></a>Controle AUTO3STATE

Define uma caixa de seleção automática de três Estados. O controle é uma caixa aberta com o texto fornecido posicionado à direita da caixa. Quando escolhido, a caixa avança automaticamente entre três Estados: marcada, desmarcada e desabilitada (cinza). O controle envia uma mensagem para seu pai sempre que o usuário escolhe o controle.

``` syntax
AUTO3STATE text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

Estilos para o controle, que pode ser uma combinação do estilo **BS \_ AUTO3STATE** e dos seguintes estilos: **WS \_ TabStop**, **WS \_ Disabled** e **WS \_ Group**.

Se você não especificar um estilo, o estilo padrão será `BS_AUTO3STATE | WS_TABSTOP` .

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**CAIXA de seleção automarca**](autocheckbox-control.md)
</dt> <dt>

[Caixas de seleção](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**VERIFICAÇÃO**](checkbox-control.md)
</dt> <dt>

[**CONTROLO**](control-control.md)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> <dt>

[Estilos de janela](/windows/desktop/winmsg/window-styles)
</dt> </dl>

 

 