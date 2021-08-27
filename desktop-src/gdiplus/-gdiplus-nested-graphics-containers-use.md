---
description: Windows GDI+ fornece contêineres que você pode usar para substituir ou aumentar temporariamente parte do estado em um objeto Graphics.
ms.assetid: f3fce8ef-903a-4b9d-b76c-562739d02eb3
title: Contêineres de elementos gráficos aninhados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d88b3a768e5b156eb5d28410ad69d58227e9660618764ca4b084b5e35662b839
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114976"
---
# <a name="nested-graphics-containers"></a>Contêineres de elementos gráficos aninhados

Windows GDI+ fornece contêineres que você pode usar para substituir ou aumentar temporariamente parte do estado em [**um objeto Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Crie um contêiner chamando o [**método Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) de **um objeto Graphics.** Você pode chamar **Graphics::BeginContainer** repetidamente para formar contêineres aninhados.

## <a name="transformations-in-nested-containers"></a>Transformações em contêineres aninhados

O exemplo a seguir cria [**um objeto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um contêiner dentro **desse objeto Graphics.** A transformação mundial do **objeto Graphics** é uma conversão de 100 unidades na direção x e 80 unidades na direção y. A transformação global do contêiner é uma rotação de 30 graus. O código faz a chamada


```
DrawRectangle(&pen, -60, -30, 120, 60)
```



Duas vezes. A primeira chamada para [**Graphics::D rawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) *está dentro do contêiner*; ou seja, a chamada está entre as chamadas para [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) [**e Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer). A segunda chamada para **Graphics::D rawRectangle** é após a chamada para **Graphics::EndContainer**.


```
Graphics           graphics(hdc);
Pen                pen(Color(255, 255, 0, 0));
GraphicsContainer  graphicsContainer;

graphics.TranslateTransform(100.0f, 80.0f);

graphicsContainer = graphics.BeginContainer();
   graphics.RotateTransform(30.0f);
   graphics.DrawRectangle(&pen, -60, -30, 120, 60);
graphics.EndContainer(graphicsContainer);

graphics.DrawRectangle(&pen, -60, -30, 120, 60);
```



No código anterior, o retângulo desenhado de dentro do contêiner é transformado primeiro pela transformação mundial do contêiner (rotação) e, em seguida, pela transformação mundial do objeto [**Gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) (tradução). O retângulo desenhado de fora do contêiner é transformado apenas pela transformação mundial do **objeto Gráfico** (tradução). A ilustração a seguir mostra os dois retângulos.

![captura de tela de uma janela com dois retângulos vermelhos centralizados no mesmo ponto, mas com rotações diferentes](images/nestedcontainers1.png)

 

## <a name="clipping-in-nested-containers"></a>Recorte em contêineres aninhados

O exemplo a seguir ilustra como os contêineres aninhados lidam com regiões de recorte. O código cria um [**objeto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um contêiner dentro **desse objeto Graphics.** A região de recorte do **objeto Graphics** é um retângulo e a região de recorte do contêiner é uma elipse. O código faz duas chamadas para o [**método Graphics::D rawLine.**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) A primeira chamada para **Graphics::D rawLine** está dentro do contêiner e a segunda chamada para **Graphics::D rawLine** está fora do contêiner (após a chamada para [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)). A primeira linha é recortada pela interseção das duas áreas de recorte. A segunda linha é recortada apenas pela região de recorte retangular do **objeto Graphics.**


```
Graphics           graphics(hdc);
GraphicsContainer  graphicsContainer;
Pen                redPen(Color(255, 255, 0, 0), 2);
Pen                bluePen(Color(255, 0, 0, 255), 2);
SolidBrush         aquaBrush(Color(255, 180, 255, 255));
SolidBrush         greenBrush(Color(255, 150, 250, 130));

graphics.SetClip(Rect(50, 65, 150, 120));
graphics.FillRectangle(&aquaBrush, 50, 65, 150, 120);

graphicsContainer = graphics.BeginContainer();
   // Create a path that consists of a single ellipse.
   GraphicsPath path;
   path.AddEllipse(75, 50, 100, 150);

  // Construct a region based on the path.
   Region region(&path);
   graphics.FillRegion(&greenBrush, &region);

   graphics.SetClip(&region);
   graphics.DrawLine(&redPen, 50, 0, 350, 300);
graphics.EndContainer(graphicsContainer);

graphics.DrawLine(&bluePen, 70, 0, 370, 300);
```



A ilustração a seguir mostra as duas linhas recortadas.

![ilustração de uma elipse dentro de um retângulo, com uma linha recortada pela elipse e a outra pelo retângulo](images/nestedcontainers2.png)

Como os dois exemplos anteriores mostram, as transformações e áreas de recorte são cumulativas em contêineres aninhados. Se você definir as transformações de mundo do contêiner e do objeto [**Gráficos,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) ambas as transformações serão aplicadas aos itens desenhados de dentro do contêiner. A transformação do contêiner será aplicada primeiro e a transformação do **objeto Gráficos** será aplicada em segundo lugar. Se você definir as regiões de recorte do contêiner e o objeto **Gráficos,** os itens extraídos de dentro do contêiner serão recortados pela interseção das duas regiões de recorte.

## <a name="quality-settings-in-nested-containers"></a>Configurações de qualidade em contêineres aninhados

Configurações de qualidade ( [**SmoothingMode,**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)e assim por diante) em contêineres aninhados não são cumulativas; em vez disso, as configurações de qualidade do contêiner substituem temporariamente as configurações de qualidade de [**um objeto Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Quando você cria um novo contêiner, as configurações de qualidade do contêiner são definidas com valores padrão. Por exemplo, suponha que você tenha um objeto **Graphics** com um modo de suavização [***SmoothingModeAntiAlias****](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode). Quando você cria um contêiner, o modo de suavização dentro do contêiner é o modo de suavização padrão. Você tem a liberdade de definir o modo de suavização do contêiner e os itens desenhados de dentro do contêiner serão desenhados de acordo com o modo é definido por você. Os itens desenhados após a chamada para [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) serão desenhados de acordo com o modo de suavização ([****SmoothingModeAntiAlias****](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)) que estava em funcionamento antes da chamada para [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).

## <a name="several-layers-of-nested-containers"></a>Várias camadas de contêineres aninhados

Você não está limitado a um contêiner em um [**objeto Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) É possível criar uma sequência de contêineres, cada um deles aninhado no anterior e é possível especificar a transformação global, a área de recorte e as configurações de qualidade de cada um desses contêineres aninhados. Se você chamar um método de desenho de dentro do contêiner mais interno, as transformações serão aplicadas em ordem, começando pelo contêiner mais interno e terminando com mais externo. Itens desenhados de dentro do contêiner mais interno serão recortados pela interseção de todas as áreas de recorte.

O exemplo a seguir cria um objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e define sua dica de renderização de texto como [***TextRenderingHintAntiAlias****](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint). O código cria dois contêineres, um aninhado dentro do outro. A dica de renderização de texto do contêiner externo é definida como [***TextRenderingHintSingleBitPerPixel****](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)e a dica de renderização de texto do contêiner interno é definida como [***TextRenderingHintAntiAlias****](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint). O código desenha três cadeias de caracteres: uma do contêiner interno, uma do contêiner externo e outra do **próprio objeto Graphics.**


```
Graphics graphics(hdc);
GraphicsContainer innerContainer;
GraphicsContainer outerContainer;
SolidBrush brush(Color(255, 0, 0, 255));
FontFamily fontFamily(L"Times New Roman");
Font font(&fontFamily, 36, FontStyleRegular, UnitPixel);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);

outerContainer = graphics.BeginContainer();

   graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);

   innerContainer = graphics.BeginContainer();
      graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
      graphics.DrawString(L"Inner Container", 15, &font,
         PointF(20, 10), &brush);
   graphics.EndContainer(innerContainer);

   graphics.DrawString(L"Outer Container", 15, &font, PointF(20, 50), &brush);

graphics.EndContainer(outerContainer);

graphics.DrawString(L"Graphics Object", 15, &font, PointF(20, 90), &brush);
```



A ilustração a seguir mostra as três cadeias de caracteres. As cadeias de caracteres desenhadas do contêiner interno e [**o objeto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) são suavizadas. A cadeia de caracteres desenhada do contêiner externo não é suavizada devido à configuração TextRenderingHintSingleBitPerPixel.

![ilustração de um retângulo que contém a mesma cadeia de caracteres às vezes; somente os caracteres na primeira e na última linha são suaves](images/nestedcontainers3.png)

 

 
