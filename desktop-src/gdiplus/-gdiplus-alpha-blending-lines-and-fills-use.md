---
description: no Windows GDI+, uma cor é um valor de 32 bits com 8 bits cada para alfa, vermelho, verde e azul.
ms.assetid: f8c22d1a-b96b-4d16-928e-20adbae4c4a7
title: Combinação alfa em linhas e preenchimentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64096bbabc632ad7c2b159191ad21b3b09f3801a486f27679118008e4927e88f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977796"
---
# <a name="alpha-blending-lines-and-fills"></a>Combinação alfa em linhas e preenchimentos

no Windows GDI+, uma cor é um valor de 32 bits com 8 bits cada para alfa, vermelho, verde e azul. O valor alfa indica a transparência da cor – a extensão a qual a cor é combinada com a cor da tela de fundo. Os valores alfa variam de 0 a 255, em que 0 representa uma cor totalmente transparente e 255 representa uma cor totalmente opaca.

A combinação alfa é uma combinação de pixel por pixel da fonte e dos dados de cor da tela de fundo. Cada um dos três componentes (vermelho, verde, azul) de uma cor de origem é combinado com o componente correspondente da cor da tela de fundo de acordo com a seguinte fórmula:

displayColor = sourceColor × alfa / 255 + backgroundColor × (255 – alfa) / 255

Por exemplo, suponha que o componente vermelho da cor da fonte é 150 e o componente vermelho da cor da tela de fundo é 100. Se o valor alfa for 200, o componente vermelho da cor resultante será calculado da seguinte maneira:

150 × 200 / 255 + 100 × (255 – 200) / 255 = 139

Os tópicos a seguir abordam a mistura alfa em mais detalhes:

-   [Desenhar linhas opacas e semitransparentes](-gdiplus-drawing-opaque-and-semitransparent-lines-use.md)
-   [Desenho com pincéis opacos e semitransparentes](-gdiplus-drawing-with-opaque-and-semitransparent-brushes-use.md)
-   [Usando o modo de composição para controlar a mesclagem alfa](-gdiplus-using-compositing-mode-to-control-alpha-blending-use.md)
-   [Uso de uma matriz de cores para definir valores alfa em imagens](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md)
-   [Definindo os valores Alfa de pixels individuais](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md)

 

 



