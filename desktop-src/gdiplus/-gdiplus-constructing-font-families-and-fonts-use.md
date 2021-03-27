---
description: O Windows GDI+ agrupa fontes com a mesma face de tipos, mas estilos diferentes em famílias de fontes.
ms.assetid: 57428fae-6af4-47a5-a499-717dc378767a
title: Construindo fontes e famílias de fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2761923847a15be6b1ad51eec0d683129b70b349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988887"
---
# <a name="constructing-font-families-and-fonts"></a>Construindo fontes e famílias de fontes

O Windows GDI+ agrupa fontes com a mesma face de tipos, mas estilos diferentes em famílias de fontes. Por exemplo, a família de fonte Arial contém as seguintes fontes:

-   Arial Regular
-   Arial Bold
-   Arial Italic
-   Arial Bold Italic

O GDI+ usa quatro estilos para formar famílias: regular, negrito, itálico e negrito itálico. Adjetivos como *estreito* e *arredondado* não são considerados estilos; em vez disso, eles são parte do nome da família. Por exemplo, Arial Narrow é uma família de fontes cujos membros são os seguintes:

-   Arial Narrow Regular
-   Arial Narrow Bold
-   Arial Narrow Italic
-   Arial Narrow Bold Italic

Antes de poder desenhar o texto com o GDI+, você precisa construir um objeto [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) e um objeto [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) . Os objetos **FontFamily** especifica a face de tipos (por exemplo, Arial) e o objeto **Font** especifica o tamanho, o estilo e as unidades.

O exemplo a seguir constrói uma fonte Arial de estilo regular com um tamanho de 16 pixels:


```
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 16, FontStyleRegular, UnitPixel);
            
```



No código anterior, o primeiro argumento passado para o construtor [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) é o endereço do objeto [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) . O segundo argumento especifica o tamanho da fonte medido em unidades identificadas pelo quarto argumento. O terceiro argumento identifica o estilo.

* * * * [UnitPixel * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) * * é um membro da enumeração **de unidade** e [* * * * FontStyleRegular * * * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) é um membro da enumeração **FontStyle** . Ambas as enumerações são declaradas em Gdiplusenums. h.

 

 



