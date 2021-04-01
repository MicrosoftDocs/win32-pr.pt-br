---
title: Controle SCROLLBAR
description: Define um controle de barra de rolagem.
ms.assetid: 9b0b60b1-4b4b-494e-90d0-aaa67e7ea88c
keywords:
- Menus de controle de barra de ROLAgem e outros recursos
topic_type:
- apiref
api_name:
- SCROLLBAR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ef4069988603c7c89ec2ed8a363d3515a0b8bb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084541"
---
# <a name="scrollbar-control"></a>Controle SCROLLBAR

Define um controle de barra de rolagem. O controle é um retângulo que contém uma caixa de rolagem e tem setas de direção em ambas as extremidades. O controle de barra de rolagem envia uma mensagem de notificação para seu pai sempre que o usuário clica no controle. O pai é responsável por atualizar a posição da caixa de rolagem. Os controles de barra de rolagem podem ser posicionados em qualquer lugar em uma janela e usados sempre que necessário para fornecer a entrada de rolagem.

``` syntax
SCROLLBAR id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

Zero ou uma combinação dos seguintes estilos: **WS \_ TabStop**, **WS \_ Group** e **WS \_ desabilitados**.

Além desses estilos, o parâmetro *Style* pode conter uma combinação (ou nenhum) dos estilos de classe ScrollBar.

Se você não especificar um estilo, o estilo padrão será **SBS \_ na horizontal**.

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md). Observe que você não pode especificar o texto para este controle.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso da instrução **ScrollBar** :

``` syntax
#define IDC_SCROLLBARV                  1010

SCROLLBAR IDC_SCROLLBARV, 7, 55, 187, 44, SBS_VERT
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Barras de rolagem](../controls/about-scroll-bars.md)
</dt> </dl>

 

 