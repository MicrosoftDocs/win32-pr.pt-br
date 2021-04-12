---
title: Instrução de estilo
description: Define o estilo de janela da caixa de diálogo. O estilo da janela especifica se a caixa é uma janela pop-up ou filho.
ms.assetid: 5ede57ad-5fa5-414c-9823-e66994826027
keywords:
- Menus de instrução de estilo e outros recursos
topic_type:
- apiref
api_name:
- STYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67cd8f6af4a6baa2f36b66855cbe9faa2b0e5120
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365953"
---
# <a name="style-statement"></a>Instrução de estilo

Define o estilo de janela da caixa de diálogo. O estilo da janela especifica se a caixa é uma janela pop-up ou filho.

``` syntax
STYLE style
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

O estilo da janela. Esse parâmetro pode ser um valor inteiro ou uma combinação de valores de estilo de janela (como **WS \_ Caption** e **WS \_ SYSMENU**) e valores de estilo de caixa de diálogo (como o **DS \_ Center**).

</dd> </dl>

Para obter uma lista de estilos de janela, consulte [estilos de janela](/windows/desktop/winmsg/window-styles). Para obter uma lista de estilos de caixa de diálogo, consulte [estilos de modelo de caixa de diálogo](../dlgbox/about-dialog-boxes.md). Se você usar os valores de estilo da janela ou da caixa de diálogo, deverá incluir Windows. h.

 

 