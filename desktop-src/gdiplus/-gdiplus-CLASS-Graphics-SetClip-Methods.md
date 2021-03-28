---
description: Este tópico lista os métodos SetClip da classe Graphics. Para obter uma lista completa de métodos para a classe Graphics, consulte gráficos.
ms.assetid: e8348373-da79-4d33-8bea-d594985493d4
title: Métodos gráficos. SetClip
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 488d617dfb53343fc728fff722c0c0bc1db57335
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169113"
---
# <a name="graphicssetclip-methods"></a>Métodos gráficos. SetClip

Este tópico lista os métodos SetClip da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Para obter uma lista completa de métodos para a classe **Graphics** , consulte [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetClip (HRGN, CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inhrgn_incombinemode))                     | O método [**Graphics:: SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inhrgn_incombinemode)) atualiza a região de recorte desse objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para uma região que é a combinação de si mesmo e uma região GDI.<br/>                                                                                                                                                                                                          |
| [**SetClip (Rect&, CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrect__incombinemode))   | O método [**Graphics:: SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrect__incombinemode)) atualiza a região de recorte desse objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para uma região que é a combinação de si mesmo e um retângulo.<br/>                                                                                                                                                                                          |
| [**SetClip (RectF&, CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrectf__incombinemode)) | O método [**Graphics:: SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrectf__incombinemode)) atualiza a região de recorte desse objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para uma região que é a combinação de si mesmo e um retângulo.<br/>                                                                                                                                                                                         |
| [**SetClip (região \* , CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode))               | O método [**Graphics:: SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) atualiza a região de recorte desse objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para uma região que é a combinação de si mesma e a região especificada por um objeto [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) .<br/>                                                                                                                                      |
| [**SetClip (gráficos \* , CombineMode)**](/previous-versions//ms535823(v=vs.85))                  | O método [**Graphics:: SetClip**](/previous-versions//ms535823(v=vs.85)) atualiza a região de recorte deste objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para uma região que é a combinação de si mesmo e a região de recorte de outro objeto **gráfico** .<br/>                                                                                                                                                                       |
| [**SetClip (GraphicsPath \* , CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode))           | O método [**Graphics:: SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode)) atualiza a região de recorte deste objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para uma região que é a combinação de si mesmo e a região especificada por um caminho gráfico. Se uma figura no caminho não for fechada, esse método tratará a figura não fechada como se ela fosse fechada por uma linha reta que conecta os pontos inicial e final da figura.<br/> |



 

 
