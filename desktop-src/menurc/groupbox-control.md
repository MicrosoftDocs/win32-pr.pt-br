---
title: Controle GROUPBOX (menus e outros recursos)
description: Define um controle de caixa de grupo. O controle é um retângulo que agrupa outros controles juntos. Os controles são agrupados desenhando uma borda em torno deles e exibindo o texto fornecido no canto superior esquerdo.
ms.assetid: ffca7b68-0326-4fbe-8330-7d1151abb14a
keywords:
- Menus de controle de GROUPBOX e outros recursos
topic_type:
- apiref
api_name:
- GROUPBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f77461099362e4f100924f82d95dffa09a94fa
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104006857"
---
# <a name="groupbox-control"></a>Controle GROUPBOX

Define um controle de caixa de grupo. O controle é um retângulo que agrupa outros controles juntos. Os controles são agrupados desenhando uma borda em torno deles e exibindo o texto fornecido no canto superior esquerdo.

A instrução **GroupBox** , que pode ser usada somente em uma instrução [**DIALOGEX**](dialogex-resource.md) , define o texto, o identificador, as dimensões e os atributos de uma janela de controle.

``` syntax
GROUPBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

Estilos de controle. Esse valor pode ser uma combinação do botão classe estilo **BS \_ GroupBox** e os estilos **WS \_ TabStop** e **WS \_ Disabled** .

Se você não especificar um estilo, o estilo padrão será **BS \_ GroupBox**.

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).

## <a name="remarks"></a>Comentários

Quando o estilo contém **WS \_ TabStop** ou o texto especifica um acelerador, a Tabulação ou o pressionamento da tecla acelerador move o foco para o primeiro controle dentro do grupo.

## <a name="examples"></a>Exemplos

Este exemplo define um controle de caixa de grupo que é rotulado como opções:

``` syntax
GROUPBOX "Options", 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Caixas de grupo](https://www.bing.com/search?q=Group+Boxes)
</dt> </dl>

 

 




