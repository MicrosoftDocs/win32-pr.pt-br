---
title: Controle PUSHBOX
description: Define um controle de caixa de push, que é idêntico a um PUSHBUTTON, exceto pelo fato de que ele não exibe um rosto ou quadro de botão; somente o texto é exibido.
ms.assetid: b4e9d3f5-fcc4-40e1-90af-53d14e4638bf
keywords:
- Menus de controle PUSHBOX e outros recursos
topic_type:
- apiref
api_name:
- PUSHBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06135aad813141e15bede8364a71e8fbc3016c7cb79afe0085bb6bc7bbcb2d8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952366"
---
# <a name="pushbox-control"></a>Controle PUSHBOX

Define um controle de caixa de push, que é idêntico a [**um PUSHBUTTON,**](pushbutton-control.md)exceto que ele não exibe um rosto ou quadro de botão; somente o texto é exibido.

``` syntax
PUSHBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos para a caixa de push, que pode ser uma combinação do estilo **BS \_ PUSHBOX** e os seguintes estilos: **WS \_ TABSTOP,** **WS \_ DISABLED** e **WS \_ GROUP.**

Se você não especificar um estilo, o estilo padrão será `BS_PUSHBOX | WS_TABSTOP` .

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [Common Control Parameters](common-control-parameters.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Botões](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[**Botão**](pushbutton-control.md)
</dt> </dl>

 

 




