---
description: Embora as funções discutidas anteriormente funcionem bem para muitas linguagens, elas podem não lidar com as necessidades de scripts complexos.
ms.assetid: a60b50c8-13e8-4c61-989f-187bb67cf929
title: Scripts complexos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c149aa1d9a6f5caf78fec5227f25aa30146fc273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827671"
---
# <a name="complex-scripts"></a>Scripts complexos

Embora as funções discutidas anteriormente funcionem bem para muitas linguagens, elas podem não lidar com as necessidades de scripts complexos. *Scripts complexos* são linguagens cujo formulário impresso não é renderizado de uma maneira simples. Por exemplo, um script complexo pode permitir renderização bidirecional, formatação contextual de glifos ou caracteres de combinação. Devido a esses requisitos especiais, o controle da saída de texto deve ser muito flexível.

As funções que exibem [**texto TextOut,**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext)e [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) foram estendidas para dar suporte a scripts complexos. Em geral, esse suporte é transparente para o aplicativo. No entanto, os aplicativos devem salvar caracteres em um buffer e exibir uma linha inteira de texto ao mesmo tempo, para que os módulos de modelagem de script complexos possam usar o contexto para reordenar e gerar glifos corretamente. Além disso, como a largura de um glifo pode variar por contexto, os aplicativos devem usar [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) para determinar o comprimento da linha em vez de usar larguras de caracteres em cache.

Além disso, aplicativos complexos com reconhecimento de script devem considerar a adição de suporte à ordem de leitura da direita para a esquerda e ao alinhamento à direita para seus aplicativos. Você pode alternar a ordem de leitura ou o alinhamento entre a esquerda e a direita com o seguinte código:


```C++
// Save lAlign (this example uses static variables) 
static LONG lAlign = TA_LEFT;

// When user toggles alignment (assuming TA_CENTER is not supported). 

lAlign = TA_RIGHT;

// When the user toggles reading order. 

lAlign = TA_RTLREADING;

// Before calling ExtTextOut, for example, when processing WM_PAINT  

SetTextAlign (hDc, lAlign);
```



Para alternar os dois atributos de uma vez, execute a instrução a seguir e chame [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) e [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), conforme mostrado anteriormente:


```C++
lAlign = TA_RIGHT^TA_RTLREADING;  //pre-inline !
```



Você também pode processar scripts complexos com o Uniscribe. O Uniscribe é um conjunto de funções que permitem um grau de controle detalhado para scripts complexos. Para obter mais informações, consulte [Uniscribe](../intl/uniscribe.md) e [processamento de scripts complexos](../intl/processing-complex-scripts.md).

 

 
