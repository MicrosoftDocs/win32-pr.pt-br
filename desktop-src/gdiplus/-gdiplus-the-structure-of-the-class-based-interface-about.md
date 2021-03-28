---
description: A interface C++ para o Windows GDI+ contém cerca de 40 classes, 50 enumerações e 6 estruturas. Também há algumas funções que não são membros de nenhuma classe.
ms.assetid: 46051bfa-b842-4e4e-bda8-e9003b5b5da4
title: A estrutura da interface baseada em classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2627d695330c316a57c2593e75233d73b27a1524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988748"
---
# <a name="the-structure-of-the-class-based-interface"></a>A estrutura da interface baseada em classe

A interface C++ para o Windows GDI+ contém cerca de 40 classes, 50 enumerações e 6 estruturas. Também há algumas funções que não são membros de nenhuma classe.

Você deve indicar que o namespace gdiplus está sendo usado antes de qualquer função GDI+ ser chamada. A instrução a seguir indica que o namespace gdiplus está sendo usado no aplicativo.

`using namespace Gdiplus;`

A classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) é o núcleo da interface GDI+; é a classe que realmente desenha linhas, curvas, figuras, imagens e texto.

Muitas classes funcionam junto com a classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Por exemplo, o método [Graphics::D rawline](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) recebe um ponteiro para um objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) , que contém atributos (cor, largura, estilo tracejado e similares) da linha a ser desenhada. O método [Graphics:: FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) pode receber um ponteiro para um objeto [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) , que funciona com o objeto **Graphics** para preencher um retângulo com uma cor que muda gradualmente. Os objetos [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) e [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) influenciam a maneira como um objeto **Graphics** Desenha texto. Um objeto de [**matriz**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) armazena e manipula a transformação mundial de um objeto **gráfico** , que é usado para girar, dimensionar e inverter imagens.

Determinadas classes servem principalmente como tipos de dados estruturados. Algumas dessas classes (por exemplo, [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect), [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point)e [**size**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-size)) são para fins gerais. Outras são para fins especializados e são consideradas classes auxiliares. Por exemplo, a classe [**BitmapData**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-bitmapdata) é um auxiliar para a classe [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) e a classe [**PathData**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pathdata) é um auxiliar para a classe [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) . O GDI+ também define algumas estruturas que são usadas para organizar dados. Por exemplo, a estrutura [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) contém um par de objetos [**coloridos**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) que formam uma entrada em uma tabela de conversão de cor.

O GDI+ define várias enumerações, que são coleções de constantes relacionadas. Por exemplo, a enumeração [**LineJoin**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin) contém os elementos [* * * * LineJoinBevel * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)* *, [* * * * LineJoinMiter * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)* e [* * * * LineJoinRound * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)*, que especificam os estilos que podem ser usados para unir duas linhas.

O GDI+ fornece algumas funções que não fazem parte de nenhuma classe. Duas dessas funções são [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) e [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown). Você deve chamar **GdiplusStartup** antes de fazer qualquer outra chamada GDI+ e deve chamar **GdiplusShutdown** quando tiver terminado de usar o GDI+.

 

 
