---
title: Controle SCROLLBAR
description: Define um controle de barra de rolagem.
ms.assetid: 9b0b60b1-4b4b-494e-90d0-aaa67e7ea88c
keywords:
- Menus de controle SCROLLBAR e outros recursos
topic_type:
- apiref
api_name:
- SCROLLBAR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b03865f66a06198cc1b1b78f8bb0b0213d998b7e5407506e4b8ed64ed9efaf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733434"
---
# <a name="scrollbar-control"></a>Controle SCROLLBAR

Define um controle de barra de rolagem. O controle é um retângulo que contém uma caixa de rolagem e tem setas de direção em ambas as extremidades. O controle de barra de rolagem envia uma mensagem de notificação para seu pai sempre que o usuário clica no mouse no controle. O pai é responsável por atualizar a posição da caixa de rolagem. Os controles de barra de rolagem podem ser posicionados em qualquer lugar em uma janela e usados sempre que necessário para fornecer entrada de rolagem.

``` syntax
SCROLLBAR id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Zero ou uma combinação dos seguintes estilos: **WS \_ TABSTOP,** **WS \_ GROUP** e **WS \_ DISABLED.**

Além desses estilos, o parâmetro *de* estilo pode conter uma combinação (ou nenhum) dos estilos da classe SCROLLBAR.

Se você não especificar um estilo, o estilo padrão será **SBS \_ HORZ.**

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [Common Control Parameters](common-control-parameters.md). Observe que você não pode especificar texto para esse controle.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso da **instrução SCROLLBAR:**

``` syntax
#define IDC_SCROLLBARV                  1010

SCROLLBAR IDC_SCROLLBARV, 7, 55, 187, 44, SBS_VERT
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Barras de rolagem](../controls/about-scroll-bars.md)
</dt> </dl>

 

 