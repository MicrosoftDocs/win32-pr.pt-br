---
title: Controle CHECKBOX (Compilador de Recursos)
description: Define um controle de caixa de seleção.
ms.assetid: 24ee25e5-9de2-4843-a55e-96b897f6ae8e
keywords:
- Menus de controle CHECKBOX e outros recursos
topic_type:
- apiref
api_name:
- CHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab103291a919a166d63656718629a7781bdd5f3a4b3023283f2dd114decd966e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461326"
---
# <a name="checkbox-control"></a>Controle CHECKBOX

Define um controle de caixa de seleção. O controle é um retângulo pequeno (caixa de seleção) que tem o texto especificado exibido ao lado dele (normalmente, à direita). Quando o usuário seleciona o controle, o controle realça o retângulo e envia uma mensagem para sua janela pai.

A **instrução CHECKBOX,** que só pode ser usada em uma instrução [**DIALOGEX,**](dialogex-resource.md) define o texto, o identificador, as dimensões e os atributos do controle.

``` syntax
CHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Texto*
</dt> <dd>

Texto que deve ser exibido à direita do controle.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos de controle. Esse valor pode ser uma combinação do estilo de classe de botão **BS \_ CHECKBOX** e dos estilos **WS \_ TABSTOP** e **WS \_ GROUP.**

Se você não especificar um estilo, o estilo padrão será `BS_CHECKBOX | WS_TABSTOP` .

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [Common Control Parameters](common-control-parameters.md).

## <a name="examples"></a>Exemplos

Este exemplo define um controle de caixa de seleção rotulado como Itálico:

``` syntax
CHECKBOX "Italic", 3, 10, 10, 40, 10
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**AUTOCHECKBOX**](autocheckbox-control.md)
</dt> <dt>

[**AUTO3STATE**](auto3state-control.md)
</dt> <dt>

[Caixas de seleção](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**Getdialogbaseunits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> </dl>

 

 