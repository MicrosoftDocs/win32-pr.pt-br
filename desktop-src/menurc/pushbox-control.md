---
title: Controle PUSHBOX
description: Define um controle de caixa de push, que é idêntico a um botão de pressão, exceto pelo fato de que ele não exibe uma face de botões ou quadro; somente o texto é exibido.
ms.assetid: b4e9d3f5-fcc4-40e1-90af-53d14e4638bf
keywords:
- Menus de controle do PUSHBOX e outros recursos
topic_type:
- apiref
api_name:
- PUSHBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e3e81e11c7d9a87c4f5501b114ef77cdb88b07
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104084183"
---
# <a name="pushbox-control"></a>Controle PUSHBOX

Define um controle de caixa de push, que é idêntico a um botão de [**pressão**](pushbutton-control.md), exceto pelo fato de que ele não exibe uma face de botões ou quadro; somente o texto é exibido.

``` syntax
PUSHBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

Estilos para o PUSHBOX, que pode ser uma combinação do estilo **BS \_ PUSHBOX** e os seguintes estilos: **WS \_ TabStop**, **WS \_ Disabled** e **WS \_ Group**.

Se você não especificar um estilo, o estilo padrão será `BS_PUSHBOX | WS_TABSTOP` .

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Botões de push](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[**BOTÃO**](pushbutton-control.md)
</dt> </dl>

 

 




