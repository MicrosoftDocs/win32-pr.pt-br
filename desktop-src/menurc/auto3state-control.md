---
title: Controle AUTO3STATE
description: Define uma caixa de seleção automática de três estados.
ms.assetid: 8b27367c-30d0-4591-93d0-756c65255b26
keywords:
- Menus de controle AUTO3STATE e outros recursos
topic_type:
- apiref
api_name:
- AUTO3STATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 318d43f0b6d8a16d6e76ae3d12f934e41e265197690a955cfe148dd71176f440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735208"
---
# <a name="auto3state-control"></a>Controle AUTO3STATE

Define uma caixa de seleção automática de três estados. O controle é uma caixa aberta com o texto determinado posicionado à direita da caixa. Quando escolhida, a caixa avança automaticamente entre três estados: marcado, desmarcado e desabilitado (es cinza). O controle envia uma mensagem para seu pai sempre que o usuário escolhe o controle.

``` syntax
AUTO3STATE text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos para o controle , que pode ser uma combinação do estilo **BS \_ AUTO3STATE** e os seguintes estilos: **WS \_ TABSTOP,** **WS \_ DISABLED** e **WS \_ GROUP**.

Se você não especificar um estilo, o estilo padrão será `BS_AUTO3STATE | WS_TABSTOP` .

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [Common Control Parameters](common-control-parameters.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**AUTOCHECKBOX**](autocheckbox-control.md)
</dt> <dt>

[Caixas de seleção](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**Checkbox**](checkbox-control.md)
</dt> <dt>

[**Controle**](control-control.md)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> <dt>

[Estilos de janela](/windows/desktop/winmsg/window-styles)
</dt> </dl>

 

 