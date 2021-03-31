---
title: Controle STATE3
description: Define um controle de caixa de seleção de três Estados. O controle é idêntico a uma caixa de seleção, exceto que ele tem três Estados marcados, desmarcados e desabilitados (acinzentados).
ms.assetid: 74659827-ce46-4d36-a5e2-3a97e8fd1c04
keywords:
- Menus de controle do STATE3 e outros recursos
topic_type:
- apiref
api_name:
- STATE3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24333fa9567db5613896f26429b72ff68e029335
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638445"
---
# <a name="state3-control"></a>Controle STATE3

Define um controle de caixa de seleção de três Estados. O controle é idêntico a uma [**caixa de seleção**](checkbox-control.md), exceto pelo fato de que ele tem três Estados: marcada, desmarcada e desabilitada (cinza).

``` syntax
STATE3 text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*texto*
</dt> <dd>

Texto a ser exibido à direita do controle.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

Estilos de controle. Esse valor pode ser uma combinação do botão classe estilo **BS \_ 3STATE** e os estilos **WS \_ TabStop** e **WS \_ Group** .

Se você não especificar um estilo, o estilo padrão será `BS_3STATE | WS_TABSTOP` .

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
</dt> </dl>

 

 




