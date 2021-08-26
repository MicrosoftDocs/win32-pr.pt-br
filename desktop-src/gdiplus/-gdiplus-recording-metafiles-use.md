---
description: A classe Metafile, que herda da classe Image, permite que você grave uma sequência de comandos de desenho.
ms.assetid: 062de6c2-9f82-415d-860e-2d1afd2ac027
title: Gravando metaarquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 047cdce842a9b44096ebd0f866e1b1551a5f951e138557062dff5e8f8d54f3ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014776"
---
# <a name="recording-metafiles"></a>Gravando metaarquivos

A classe [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , que herda da classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , permite que você grave uma sequência de comandos de desenho. Os comandos gravados podem ser armazenados na memória, salvos em um arquivo ou salvos em um fluxo. Os metaarquivos podem conter gráficos vetoriais, imagens rasterizadas e texto.

O exemplo a seguir cria um objeto de [**metarquivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) . O código usa o objeto **Metafile** para gravar uma sequência de comandos gráficos e, em seguida, salva os comandos gravados em um arquivo chamado SampleMetafile. EMF. Observe que o construtor de **metarquivo** recebe um identificador de contexto de dispositivo e o construtor de [**gráficos**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) recebe o endereço do objeto de **metarquivo** . A gravação é interrompida (e os comandos gravados são salvos no arquivo) quando o objeto de **gráficos** sai do escopo. As duas últimas linhas de código exibem o metarquivo, criando um novo objeto de **gráfico** e passando o endereço do objeto de **metarquivo** para o método **DrawImage** desse objeto **gráfico** . Observe que o código usa o mesmo objeto de **metarquivo** para gravar e exibir (reproduzir) o metarquivo.


```
Metafile metafile(L"SampleMetafile.emf", hdc); 
{
   Graphics graphics(&metafile);
   Pen greenPen(Color(255, 0, 255, 0));
   SolidBrush solidBrush(Color(255, 0, 0, 255));

   // Add a rectangle and an ellipse to the metafile.
   graphics.DrawRectangle(&greenPen, Rect(50, 10, 25, 75));
   graphics.DrawEllipse(&greenPen, Rect(100, 10, 25, 75));

   // Add an ellipse (drawn with antialiasing) to the metafile.
   graphics.SetSmoothingMode(SmoothingModeHighQuality);
   graphics.DrawEllipse(&greenPen, Rect(150, 10, 25, 75));

   // Add some text (drawn with antialiasing) to the metafile.
   FontFamily fontFamily(L"Arial");
   Font font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   
   graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
   graphics.RotateTransform(30.0f);
   graphics.DrawString(L"Smooth Text", 11, &font, 
      PointF(50.0f, 50.0f), &solidBrush);
} // End of recording metafile.

// Play back the metafile.
Graphics playbackGraphics(hdc);
playbackGraphics.DrawImage(&metafile, 200, 100);
```



> [!Note]  
> Para gravar um metarquivo, você deve construir um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) com base em um objeto de [**metarquivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) . A gravação do metarquivo termina quando esse objeto **gráfico** é excluído ou sai do escopo.

 

Um metarquivo contém seu próprio estado de gráfico, que é definido pelo objeto de [**gráficos**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) usado para gravar o metarquivo. Todas as propriedades do objeto **gráfico** (região do clipe, transformação do mundo, modo de suavização e similares) que você definir durante a gravação do metarquivo serão armazenadas no metarquivo. Quando você exibir o metarquivo, o desenho será feito de acordo com as propriedades armazenadas.

No exemplo a seguir, suponha que o modo de suavização foi definido como SmoothingModeNormal durante a gravação do metarquivo. Embora o modo de suavização do objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) usado para reprodução seja definido como SmoothingModeHighQuality, o metarquivo será reproduzido de acordo com a configuração SmoothingModeNormal. É o modo de suavização definido durante a gravação que é importante, não o modo de suavização definido antes da reprodução.


```
graphics.SetSmoothingMode(SmoothingModeHighQuality);
graphics.DrawImage(&meta, 0, 0);
```



 

 



