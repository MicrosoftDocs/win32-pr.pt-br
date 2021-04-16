---
title: Controle de caixa de seleção (compilador de recurso)
description: Define um controle de caixa de seleção.
ms.assetid: 24ee25e5-9de2-4843-a55e-96b897f6ae8e
keywords:
- Menus de controle de caixa de seleção e outros recursos
topic_type:
- apiref
api_name:
- CHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57b4a86a2f08baf7d6e3af9960bd68db1eba86f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105761270"
---
# <a name="checkbox-control"></a>Controle de caixa de seleção

Define um controle de caixa de seleção. O controle é um pequeno retângulo (caixa de seleção) que tem o texto especificado exibido ao lado (normalmente, à direita). Quando o usuário seleciona o controle, o controle realça o retângulo e envia uma mensagem para sua janela pai.

A instrução **CheckBox** , que só pode ser usada em uma instrução [**DIALOGEX**](dialogex-resource.md) , define o texto, o identificador, as dimensões e os atributos do controle.

``` syntax
CHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*texto*
</dt> <dd>

Texto a ser exibido à direita do controle.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

Estilos de controle. Esse valor pode ser uma combinação da **\_ caixa de seleção BS** do estilo de classe de botão e dos estilos de **\_ grupo** **WS \_ TabStop** e WS.

Se você não especificar um estilo, o estilo padrão será `BS_CHECKBOX | WS_TABSTOP` .

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).

## <a name="examples"></a>Exemplos

Este exemplo define um controle de caixa de seleção que é rotulado como itálico:

``` syntax
CHECKBOX "Italic", 3, 10, 10, 40, 10
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**CAIXA de seleção automarca**](autocheckbox-control.md)
</dt> <dt>

[**AUTO3STATE**](auto3state-control.md)
</dt> <dt>

[Caixas de seleção](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> </dl>

 

 