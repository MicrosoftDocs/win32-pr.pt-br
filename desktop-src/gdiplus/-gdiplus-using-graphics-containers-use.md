---
description: Um objeto gráfico fornece métodos como DrawLine, DrawImage e DrawString para exibir imagens vetoriais, imagens rasterizadas e texto.
ms.assetid: 721d0c1c-d105-4d9f-b5e9-6ca407b28c4e
title: Usando contêineres de elementos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80570f3a45c8d67b36f677fc404dcd63581e7938
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967739"
---
# <a name="using-graphics-containers"></a>Usando contêineres de elementos gráficos

Um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornece métodos como [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))e [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) para exibir imagens vetoriais, imagens rasterizadas e texto. Um objeto **gráfico** também tem várias propriedades que influenciam a qualidade e a orientação dos itens que são desenhados. Por exemplo, a propriedade de modo de suavização determina se a suavização é aplicada às linhas e curvas e a propriedade de transformação global influencia a posição e a rotação dos itens que são desenhados.

Um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) geralmente é associado a um dispositivo de vídeo específico. Quando você usa um objeto **Graphics** para desenhar em uma janela, o objeto **Graphics** também é associado a essa janela específica.

Um objeto de [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) pode ser considerado um contêiner porque contém um conjunto de propriedades que influenciam o desenho e é vinculado a informações específicas do dispositivo. Você pode criar um contêiner secundário dentro de um objeto **gráfico** existente chamando o método [BeginContainer](/previous-versions//ms535731(v=vs.85)) do objeto **Graphics** .

Os tópicos a seguir abordam objetos [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e contêineres aninhados com mais detalhes:

-   [O estado de um objeto de elementos gráficos](-gdiplus-the-state-of-a-graphics-object-use.md)
-   [Contêineres de elementos gráficos aninhados](-gdiplus-nested-graphics-containers-use.md)

 

 
