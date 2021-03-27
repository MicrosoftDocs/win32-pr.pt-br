---
description: O Windows GDI+ fornece várias classes que formam a base para o desenho de texto.
ms.assetid: 12bc38c3-5fbc-4d7b-902c-92a5f5057473
title: Usando texto e fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f28ec157888dcf45b309237eb0f7eefff17808c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501657"
---
# <a name="using-text-and-fonts"></a>Usando texto e fontes

O Windows GDI+ fornece várias classes que formam a base para o desenho de texto. A classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) tem vários métodos [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) que permitem especificar vários recursos de texto, como local, retângulo delimitador, fonte e formato. Outras classes que contribuem para a renderização de texto incluem [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection)e [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection).

Os tópicos a seguir abordam texto e fontes com mais detalhes:

-   [Construindo fontes e famílias de fontes](-gdiplus-constructing-font-families-and-fonts-use.md)
-   [Texto de desenho](-gdiplus-drawing-text-use.md)
-   [Formatando texto](-gdiplus-formatting-text-use.md)
-   [Enumeração de fontes instaladas](-gdiplus-enumerating-installed-fonts-use.md)
-   [Criar uma coleções de fontes privadas](-gdiplus-creating-a-private-font-collection-use.md)
-   [Obtendo métricas de fonte](-gdiplus-obtaining-font-metrics-use.md)
-   [Anti-aliasing com texto](-gdiplus-antialiasing-with-text-use.md)

 

 



