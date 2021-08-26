---
title: Controle RADIOBUTTON
description: Define um controle de botão de opção.
ms.assetid: c427080f-0408-42b4-8888-7333f3eb985d
keywords:
- Menus de controle RADIOBUTTON e outros recursos
topic_type:
- apiref
api_name:
- RADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18b01d6b2313ec4b881f182fd4a4ca34cf5bbf713dca9f329173d1817132606d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952246"
---
# <a name="radiobutton-control"></a>Controle RADIOBUTTON

Define um controle de botão de opção. O controle é um círculo pequeno que tem o texto fornecido ao lado dele, normalmente à direita. O controle realça o círculo e envia uma mensagem para sua janela pai quando o usuário seleciona o botão. O controle remove o realce e envia uma mensagem quando o botão é selecionado na próxima vez.

``` syntax
RADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

Estilos para o botão de opção, que pode ser uma combinação de estilos de classe de botão e os seguintes estilos: **WS \_ TabStop**, **WS \_ Disabled** e **WS \_ Group**.

Se você não especificar um estilo, o estilo padrão será `BS_RADIOBUTTON | WS_TABSTOP` .

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso da instrução **RadioButton** :

``` syntax
RADIOBUTTON "Italic", 100, 10, 10, 40, 10
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[Botões de opção](https://www.bing.com/search?q=Radio+Buttons)
</dt> </dl>

 

 