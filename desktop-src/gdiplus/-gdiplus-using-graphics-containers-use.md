---
description: Um objeto Graphics fornece métodos como DrawLine, DrawImage e DrawString para exibir imagens vetoriais, imagens de raster e texto.
ms.assetid: 721d0c1c-d105-4d9f-b5e9-6ca407b28c4e
title: Usando contêineres de elementos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96292395113b80ec79f8b59d4ac7f203c3d1f2d892c2da62ce4957e49b81860d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036284"
---
# <a name="using-graphics-containers"></a>Usando contêineres de elementos gráficos

Um [**objeto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornece métodos como [DrawLine,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))e [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) para exibir imagens vetoriais, imagens de raster e texto. Um **objeto Graphics** também tem várias propriedades que influenciam a qualidade e a orientação dos itens desenhados. Por exemplo, a propriedade de modo de suavização determina se a suavização é aplicada às linhas e curvas e a propriedade de transformação global influencia a posição e a rotação dos itens que são desenhados.

Um [**objeto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) geralmente é associado a um dispositivo de exibição específico. Quando você usa um **objeto Gráficos** para desenhar em uma janela, o **objeto Graphics** também é associado a essa janela específica.

Um [**objeto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) pode ser pensado como um contêiner porque contém um conjunto de propriedades que influenciam o desenho e está vinculado a informações específicas do dispositivo. Você pode criar um contêiner secundário dentro de um objeto **Graphics** existente chamando o [método BeginContainer](/previous-versions//ms535731(v=vs.85)) desse **objeto Graphics.**

Os tópicos a seguir [**abrangem objetos gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e contêineres aninhados mais detalhadamente:

-   [O estado de um objeto de elementos gráficos](-gdiplus-the-state-of-a-graphics-object-use.md)
-   [Contêineres de elementos gráficos aninhados](-gdiplus-nested-graphics-containers-use.md)

 

 
