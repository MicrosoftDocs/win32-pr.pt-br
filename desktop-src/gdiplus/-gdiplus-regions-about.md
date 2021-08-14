---
description: Uma região é uma parte da superfície de exibição.
ms.assetid: eb78d7a0-6293-487f-88c5-88ba455b965f
title: Regiões (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd15a7a25b341556b312c540f6fa4caf870da75aa4973be1d7c1e8102511e6ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885008"
---
# <a name="regions-gdi"></a>Regiões (GDI+)

Uma região é uma parte da superfície de exibição. Regiões podem ser simples (um único retângulo) ou complexas (uma combinação de polígonos e curvas fechadas). A ilustração a seguir mostra duas regiões: uma construída com base em um retângulo e outra construída com base em um demarcador.

![ilustração mostrando uma região retangular transparente sobrepondo uma forma curva opaca](images/aboutgdip02-art27.png)

Regiões geralmente são usadas para recortes e testes de clique. O recorte envolve restringir o desenho a uma determinada região da tela, geralmente a parte da tela que precisa ser atualizada. O teste de clique envolve a verificação para ver se o cursor está em uma determinada região da tela quando um botão do mouse é pressionado.

Você pode construir uma região de um retângulo ou de um caminho. Você também pode criar regiões complexas combinando regiões existentes. A [**classe Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) fornece os seguintes métodos para combinar regiões: [Intersect](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstregion)), [Union](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstregion)), [Xor](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_)), [Exclude](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion))e [**Region::Complement**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-complement(inconstgraphicspath)).

A interseção de duas regiões é o conjunto de todos os pontos que pertencem a ambas as regiões. A união é o conjunto de todos os pontos que pertencem a uma, outra ou ambas as regiões. O complemento de uma região é o conjunto de todos os pontos que não estão na região. A ilustração a seguir mostra a interseção e a união das duas regiões na figura anterior.

![ilustração mostrando a interseção das regiões na ilustração anterior e sua interseção](images/aboutgdip02-art28.png)

O [método Xor,](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_)) aplicado a um par de regiões, produz uma região que contém todos os pontos que pertencem a uma região ou outra, mas não a ambos. O [método Exclude,](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion)) aplicado a um par de regiões, produz uma região que contém todos os pontos na primeira região que não estão na segunda região. A ilustração a seguir mostra as regiões resultantes da aplicação dos métodos Xor e Exclude às duas regiões mostradas no início deste tópico.

![ilustração mostrando as partes em uma das regiões, mas não em ambas, e a parte do retângulo que não se sobrepõe à região curva](images/aboutgdip02-art29.png)

Para preencher uma região, você precisa de um [**objeto Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) um [**objeto Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) e um [**objeto Region.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) O **objeto Graphics** fornece o método [**Graphics::FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion) e o objeto **Brush** armazena atributos do preenchimento, como cor ou padrão. O exemplo a seguir preenche uma região com uma cor sólida.


```
myGraphics.FillRegion(&mySolidBrush, &myRegion);
```



 

 
