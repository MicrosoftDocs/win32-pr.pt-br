---
title: Controle DEFPUSHBUTTON
description: Define um controle de botão de push padrão.
ms.assetid: 17b2ffcb-0611-4d92-9108-bf27b1c07049
keywords:
- Menus de controle do DEFPUSHBUTTON e outros recursos
topic_type:
- apiref
api_name:
- DEFPUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49b958e60d812c3372ad6a6e6ed2a8d02d56c0f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105768681"
---
# <a name="defpushbutton-control"></a>Controle DEFPUSHBUTTON

Define um controle de botão de push padrão. O controle é um pequeno retângulo com um contorno em negrito que representa a resposta padrão para o usuário. O texto fornecido é exibido dentro do botão. O controle realça o botão da maneira usual quando o usuário clica no mouse e envia uma mensagem para a janela pai.

``` syntax
DEFPUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*texto*
</dt> <dd>

Texto que deve ser centralizado na área retangular do controle.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

Estilos de controle. Esse valor pode ser uma combinação dos seguintes estilos: **BS \_ DEFPUSHBUTTON**, **WS \_ TabStop**, **WS \_ Group** e **WS \_ Disabled**.

Se você não especificar um estilo, o estilo padrão será `BS_DEFPUSHBUTTON | WS_TABSTOP` .

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).

## <a name="examples"></a>Exemplos

Este exemplo define um controle de botão de push padrão que é rotulado como cancelar:

``` syntax
DEFPUSHBUTTON "Cancel", 101, 10, 10, 24, 50
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Botões de push](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[**BOTÃO**](pushbutton-control.md)
</dt> <dt>

[**ÍNDICES**](radiobutton-control.md)
</dt> </dl>

 

 




