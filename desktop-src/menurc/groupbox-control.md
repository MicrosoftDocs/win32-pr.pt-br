---
title: Controle GROUPBOX (menus e outros recursos)
description: Define um controle de caixa de grupo. O controle é um retângulo que reúne outros controles. Os controles são agrupados desenhando uma borda ao redor deles e exibindo o texto determinado no canto superior esquerdo.
ms.assetid: ffca7b68-0326-4fbe-8330-7d1151abb14a
keywords:
- Menus de controle GROUPBOX e outros recursos
topic_type:
- apiref
api_name:
- GROUPBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05fb8e795cfe483d16406f07fffd2a26df14cebc3c38a07fbef7f2cb78cc245a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602076"
---
# <a name="groupbox-control"></a>Controle GROUPBOX

Define um controle de caixa de grupo. O controle é um retângulo que reúne outros controles. Os controles são agrupados desenhando uma borda ao redor deles e exibindo o texto determinado no canto superior esquerdo.

A **instrução GROUPBOX,** que só pode ser usada em uma instrução [**DIALOGEX,**](dialogex-resource.md) define o texto, o identificador, as dimensões e os atributos de uma janela de controle.

``` syntax
GROUPBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos de controle. Esse valor pode ser uma combinação do estilo de classe de botão **BS \_ GROUPBOX** e dos estilos **\_ TABSTOP** e WS DISABLED do **WS. \_**

Se você não especificar um estilo, o estilo padrão será **BS \_ GROUPBOX.**

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [Common Control Parameters](common-control-parameters.md).

## <a name="remarks"></a>Comentários

Quando o estilo contém **\_ TABSTOP** do WS ou o texto especifica um acelerador, a tabulação ou pressionando a tecla de aceleração move o foco para o primeiro controle dentro do grupo.

## <a name="examples"></a>Exemplos

Este exemplo define um controle de caixa de grupo rotulado como Opções:

``` syntax
GROUPBOX "Options", 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Caixas de grupo](https://www.bing.com/search?q=Group+Boxes)
</dt> </dl>

 

 




