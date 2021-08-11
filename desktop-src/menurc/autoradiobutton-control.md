---
title: Controle AUTORADIOBUTTON
description: Define um controle de botão de opção automático. Esse controle executa automaticamente a exclusão mútua com os outros controles AUTORADIOBUTTON no mesmo grupo. Quando o botão é escolhido, o aplicativo é notificado com BN \_ CLICKED.
ms.assetid: af843084-5213-4934-b291-0787b88ef62d
keywords:
- Menus de controle AUTORADIOBUTTON e Outros Recursos
topic_type:
- apiref
api_name:
- AUTORADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c8a966a21b07744ce05063ae8c68f09156c47717fcff825875f82b4535f945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235645"
---
# <a name="autoradiobutton-control"></a>Controle AUTORADIOBUTTON

Define um controle de botão de opção automático. Esse controle executa automaticamente a exclusão mútua com os outros **controles AUTORADIOBUTTON** no mesmo grupo. Quando o botão é escolhido, o aplicativo é notificado com **BN \_ CLICKED**.

``` syntax
AUTORADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Texto*
</dt> <dd>

Texto que será exibido ao lado do botão de rádio.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos para o botão de opção automático, que pode ser uma combinação de estilos de classe BUTTON e os seguintes estilos: **WS \_ TABSTOP,** **WS \_ DISABLED** e **WS \_ GROUP**.

Se você não especificar um estilo, o estilo padrão será `BS_AUTORADIOBUTTON | WS_TABSTOP` .

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [Common Control Parameters](common-control-parameters.md).

## <a name="see-also"></a>Veja também

<dl> <dt>

[**Controle**](control-control.md)
</dt> <dt>

[Botões](https://www.bing.com/search?q=Radio+Buttons)
</dt> <dt>

[**Radiobutton**](radiobutton-control.md)
</dt> </dl>

 

 




