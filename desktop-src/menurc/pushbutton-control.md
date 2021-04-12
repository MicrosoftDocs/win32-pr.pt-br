---
title: Controle de pressão (menus e outros recursos)
description: Define um controle de botão de ação. O controle é um retângulo com cantos arredondados contendo o texto fornecido. O texto é centralizado no controle. O controle envia uma mensagem para seu pai sempre que o usuário escolhe o controle.
ms.assetid: c5fbcfb7-1b7d-4199-acac-d11bfd899298
keywords:
- Menus de controle de pressão e outros recursos
topic_type:
- apiref
api_name:
- PUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a303121b7c0eee7ac57fc369164547bd3ae6b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294058"
---
# <a name="pushbutton-control"></a>Controle de supressão

Define um controle de botão de ação. O controle é um retângulo com cantos arredondados contendo o texto fornecido. O texto é centralizado no controle. O controle envia uma mensagem para seu pai sempre que o usuário escolhe o controle.

``` syntax
PUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

Estilos para o botão de pressão, que pode ser uma combinação do estilo de **\_ pressão de BS** e dos seguintes estilos: **WS \_ TabStop**, **WS \_ Disabled** e **WS \_ Group**.

Se você não especificar um estilo, o estilo padrão será `BS_PUSHBUTTON | WS_TABSTOP` .

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso da instrução de **pressão** :

``` syntax
PUSHBUTTON "ON", 7, 10, 10, 20, 10
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[Botões de push](https://www.bing.com/search?q=Push+Buttons)
</dt> </dl>

 

 