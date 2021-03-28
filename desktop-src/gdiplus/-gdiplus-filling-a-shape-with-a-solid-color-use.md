---
description: Para preencher uma forma com uma cor sólida, crie um objeto SolidBrush e, em seguida, passe o endereço desse objeto SolidBrush como um argumento para um dos métodos Fill da classe Graphics.
ms.assetid: cedef138-5047-4a72-8b89-5a95062a351c
title: Preenchendo uma forma com uma cor sólida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c4a6221d84c4a891d377d974f168468917799e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988878"
---
# <a name="filling-a-shape-with-a-solid-color"></a>Preenchendo uma forma com uma cor sólida

Para preencher uma forma com uma cor sólida, crie um objeto [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) e, em seguida, passe o endereço desse objeto **SolidBrush** como um argumento para um dos métodos Fill da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . O exemplo a seguir mostra como preencher uma elipse com a cor vermelho:


```
SolidBrush solidBrush(Color(255, 255, 0, 0));
stat = graphics.FillEllipse(&solidBrush, 0, 0, 100, 60);
```



No exemplo anterior, o construtor [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) usa uma referência de objeto de [**cor**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) como seu único argumento. Os valores usados pelo construtor **Color** representam os componentes alfa, Red, Green e Blue da cor. Cada um desses valores deve estar no intervalo de 0 a 255. O primeiro 255 indica que a cor é totalmente opaca e o segundo 255 indica que o componente vermelho é de intensidade total. Os dois zeros indicam que os componentes verde e azul têm uma intensidade igual a 0.

Os quatro números (0, 0, 100, 60) passados para o método [**Graphics:: FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) especificam o local e o tamanho do retângulo delimitador para a elipse. O retângulo tem um canto superior esquerdo de (0, 0), uma largura de 100 e uma altura de 60.

 

 
