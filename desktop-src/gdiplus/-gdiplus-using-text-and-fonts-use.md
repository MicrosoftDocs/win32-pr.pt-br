---
description: Windows GDI+ fornece várias classes que formam a base para desenhar texto.
ms.assetid: 12bc38c3-5fbc-4d7b-902c-92a5f5057473
title: Usando texto e fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2cffc8c36da4c9dd8bbc78c6660a7cc85094071350003c5b23ce4d6a6ce7cad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359596"
---
# <a name="using-text-and-fonts"></a>Usando texto e fontes

Windows GDI+ fornece várias classes que formam a base para desenhar texto. A [**classe Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) tem vários métodos [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) que permitem especificar vários recursos de texto, como localização, retângulo delimitado, fonte e formato. Outras classes que contribuem para a renderização de texto incluem [**FontFamily,**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**StringFormat,**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection)e [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection).

Os tópicos a seguir abrangem texto e fontes mais detalhadamente:

-   [Construindo fontes e famílias de fontes](-gdiplus-constructing-font-families-and-fonts-use.md)
-   [Desenhando texto](-gdiplus-drawing-text-use.md)
-   [Formatando texto](-gdiplus-formatting-text-use.md)
-   [Enumeração de fontes instaladas](-gdiplus-enumerating-installed-fonts-use.md)
-   [Criar uma coleções de fontes privadas](-gdiplus-creating-a-private-font-collection-use.md)
-   [Obtendo métricas de fonte](-gdiplus-obtaining-font-metrics-use.md)
-   [Antialiasing com texto](-gdiplus-antialiasing-with-text-use.md)

 

 



