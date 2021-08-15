---
description: 'A ilustração a seguir mostra duas curvas: uma aberta e outra fechada.'
ms.assetid: e0fb8ba1-1783-4b36-93d8-f1242425d8bd
title: Curvas abertas e fechadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 383f7c68909a73291c00c6e760d1cc6554b061d5749b33e6e90ba3a986c71906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885121"
---
# <a name="open-and-closed-curves"></a>Curvas abertas e fechadas

A ilustração a seguir mostra duas curvas: uma aberta e outra fechada.

![ilustração de uma curva aberta (uma linha curva) e uma curva fechada (a estrutura de uma forma)](images/aboutgdip02-art24.png)

Curvas fechadas têm um interior e, portanto, podem ser preenchidas com um pincel. a [**classe Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) no Windows GDI+ fornece os seguintes métodos para preencher figuras e curvas fechadas: [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)), [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)), [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)), [FillPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)), [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)), [**graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)e [**graphics:: FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion). Sempre que você chamar um desses métodos, deverá passar o endereço de um dos tipos de pincel específicos ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)ou [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) como um argumento.

O método [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) é um complemento para o método [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) . Assim como o método DrawArc desenha uma parte da estrutura de tópicos de uma elipse, o método FillPie preenche uma parte do interior de uma elipse. O exemplo a seguir desenha um arco e preenche a parte correspondente do interior da elipse.


```
myGraphics.FillPie(&mySolidBrush, 0, 0, 140, 70, 0, 120);
myGraphics.DrawArc(&myPen, 0, 0, 140, 70, 0, 120);
```



A ilustração a seguir mostra o arco e a pizza preenchida.

![ilustração mostrando um segmento de uma elipse preenchida](images/aboutgdip02-art25.png)

O método [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) é um complemento para o método [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) . Ambos os métodos fecham automaticamente a curva conectando o ponto final ao ponto inicial. O exemplo a seguir desenha uma curva que passa por (0, 0), (60, 20) e (40, 50). Em seguida, a curva é fechada automaticamente conectando (40, 50) ao ponto inicial (0, 0), e o interior é preenchido com uma cor sólida.


```
Point myPointArray[] =
   {Point(10, 10), Point(60, 20),Point(40, 50)};
myGraphics.DrawClosedCurve(&myPen, myPointArray, 3);
myGraphics.FillClosedCurve(&mySolidBrush, myPointArray, 3, FillModeAlternate)
```



Um caminho pode consistir em várias figuras (subcaminhos). O método [**Graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) preenche o interior de cada figura. Se uma figura não for fechada, o método **Graphics:: FillPath** preencherá a área que seria incluída se a figura fosse fechada. O exemplo a seguir desenha e preenche um caminho que consiste em um arco, um spline Cardeal, uma cadeia de caracteres e uma pizza.


```
myGraphics.FillPath(&mySolidBrush, &myGraphicsPath);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



A ilustração a seguir mostra o caminho antes e depois que ele é preenchido com um pincel sólido. Observe que o texto na cadeia de caracteres é descrito, mas não preenchido, pelo método [**Graphics::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) . É o método [**Graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) que pinta os Interiors dos caracteres na cadeia de caracteres.

![ilustração que duas vezes mostra texto e uma curva aberta e fechada; Eles estão vazios na primeira vez e são preenchidos da segunda vez](images/aboutgdip02-art26.png)

 

 



