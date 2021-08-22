---
description: A interface C++ para Windows GDI+ contém cerca de 40 classes, 50 enumerações e 6 estruturas. Também há algumas funções que não são membros de nenhuma classe.
ms.assetid: 46051bfa-b842-4e4e-bda8-e9003b5b5da4
title: A estrutura da interface baseada em classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30909917ad89a65e88c4ca31ca229a5f25d503bced7a9cac81e4199ced1ba7d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830656"
---
# <a name="the-structure-of-the-class-based-interface"></a>A estrutura da interface baseada em classe

A interface C++ para Windows GDI+ contém cerca de 40 classes, 50 enumerações e 6 estruturas. Também há algumas funções que não são membros de nenhuma classe.

Você deve indicar que o namespace Gdiplus está sendo usado antes que qualquer GDI+ funções sejam chamadas. A instrução a seguir indica que o namespace Gdiplus está sendo usado no aplicativo.

`using namespace Gdiplus;`

A [**classe Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) é o núcleo da interface GDI+; é a classe que, na verdade, desenha linhas, curvas, figuras, imagens e texto.

Muitas classes trabalham em conjunto com a [**classe Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Por exemplo, o método [Graphics::D rawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) recebe um ponteiro para um objeto [**Pen,**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) que contém atributos (cor, largura, estilo de traço e outros) da linha a ser desenhada. O [método Graphics::FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) pode receber um ponteiro para um objeto [**LinearGradientBrush,**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) que funciona com o objeto **Graphics** para preencher um retângulo com uma cor que muda gradualmente. [**Objetos Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) e [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) influenciam a maneira como **um objeto Graphics** desenha texto. Um [**objeto Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) armazena e manipula a transformação do mundo de um objeto **Gráfico,** que é usado para girar, dimensionar e inverter imagens.

Determinadas classes servem principalmente como tipos de dados estruturados. Algumas dessas classes (por exemplo, [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect), [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point)e [**Size**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-size)) são para fins gerais. Outros são para fins especializados e são considerados classes auxiliares. Por exemplo, a [**classe BitmapData**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-bitmapdata) é um auxiliar para a classe [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) e a classe [**PathData**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pathdata) é um auxiliar para a [**classe GraphicsPath.**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) GDI+ também define algumas estruturas que são usadas para organizar dados. Por exemplo, a estrutura [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) contém um par de [**objetos Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) que formam uma entrada em uma tabela de conversão de cores.

GDI+ define várias enumerações, que são coleções de constantes relacionadas. Por exemplo, a enumeração [**LineJoin**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin) contém os elementos [****LineJoinBevel****,](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin) [***LineJoinMiter***](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)e [****LineJoinRound****](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin), que especificam estilos que podem ser usados para unir duas linhas.

GDI+ fornece algumas funções que não fazem parte de nenhuma classe. Duas dessas funções são [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) e [**GdiplusShutdown.**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) Você deve chamar **GdiplusStartup** antes de fazer qualquer outra chamada GDI+ e chamar **GdiplusShutdown** quando terminar de usar GDI+.

 

 
