---
title: Controle AUTORADIOBUTTON
description: Define um controle de botão de opção automático. Esse controle executa automaticamente a exclusão mútua com os outros controles AUTORADIOBUTTON no mesmo grupo. Quando o botão é escolhido, o aplicativo é notificado com bilhão \_ clicado.
ms.assetid: af843084-5213-4934-b291-0787b88ef62d
keywords:
- Menus de controle de AUTORADIOBUTTON e outros recursos
topic_type:
- apiref
api_name:
- AUTORADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67395437303de0adc8c1af226210f8ca2f45958d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638519"
---
# <a name="autoradiobutton-control"></a>Controle AUTORADIOBUTTON

Define um controle de botão de opção automático. Esse controle executa automaticamente a exclusão mútua com os outros controles **AUTORADIOBUTTON** no mesmo grupo. Quando o botão é escolhido, o aplicativo é notificado com **bilhão \_ clicado**.

``` syntax
AUTORADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*texto*
</dt> <dd>

Texto que será exibido ao lado do botão de opção.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

Estilos para o botão de opção automático, que pode ser uma combinação de estilos de classe de botão e os seguintes estilos: **WS \_ TabStop**, **WS \_ Disabled** e **WS \_ Group**.

Se você não especificar um estilo, o estilo padrão será `BS_AUTORADIOBUTTON | WS_TABSTOP` .

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**CONTROLO**](control-control.md)
</dt> <dt>

[Botões de opção](https://www.bing.com/search?q=Radio+Buttons)
</dt> <dt>

[**ÍNDICES**](radiobutton-control.md)
</dt> </dl>

 

 




