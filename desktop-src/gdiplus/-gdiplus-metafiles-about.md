---
description: Windows GDI+ fornece a classe Metafile para que você possa registrar e exibir metadados.
ms.assetid: a9f9bac4-f3c7-44a1-9f0f-59ff1a27b077
title: Metadados (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 190d03edd8857da3e840c2b3fde04314fa1fb1ddb01c8e69c684bccecf3e708d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778676"
---
# <a name="metafiles-gdi"></a>Metadados (GDI+)

Windows GDI+ fornece a classe [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) para que você possa registrar e exibir metadados. Um metarquivo, também chamado de uma imagem de vetor, é uma imagem que é armazenada como uma sequência de comandos e configurações de desenho. Os comandos e as configurações registrados em um **objeto Metafile** podem ser armazenados na memória ou salvos em um arquivo ou fluxo.

GDI+ pode exibir metarquivos que foram armazenados nos seguintes formatos:

-   Windows Formato de metarquivo (WMF)
-   EMF (Metarquivo Avançado)
-   EMF+

GDI+ pode registrar metarquivos nos formatos EMF e EMF+, mas não no formato WMF.

EMF+ é uma extensão para EMF que permite que GDI+ registros sejam armazenados. Há duas variações no formato EMF+: Apenas EMF+ e EMF+ Duplo. Somente metadados em EMF+ contêm apenas GDI+ registros. Esses metadados podem ser exibidos por GDI+, mas não por Windows Graphics Device Interface (GDI). Os metadados duplos EMF+ contêm GDI+ e GDI. Cada GDI+ registro em um metadado duplo EMF+ é emparelhado com um registro GDI alternativo. Esses metadados podem ser exibidos por GDI+ ou por GDI.

O exemplo a seguir registra uma configuração e um comando de desenho em um arquivo de disco. Observe que o exemplo cria um objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e que o construtor para o objeto **Graphics** recebe o endereço de um [**objeto Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) como um argumento.


```
myMetafile = new Metafile(L"MyDiskFile.emf", hdc);
myGraphics = new Graphics(myMetafile);
   myPen = new Pen(Color(255, 0, 0, 200));
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->DrawLine(myPen, 0, 0, 60, 40);
delete myGraphics;
delete myPen;
delete myMetafile;
```



Como mostra o exemplo anterior, a [**classe Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) é a chave para registrar instruções e configurações em um [**objeto Metafile.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) Qualquer chamada feita a um método de **um objeto Graphics** pode ser registrada em um **objeto Metafile.** Da mesma forma, você pode definir qualquer propriedade de **um objeto Graphics** e registrar essa configuração em um **objeto Metafile.** A gravação termina quando o **objeto Graphics** é excluído ou sai do escopo.

O exemplo a seguir exibe o metadado criado no exemplo anterior. O metarquivo é exibido com seu canto superior esquerdo em (100, 100).


```
Graphics myGraphics(hdc);
Image myImage(L"MyDiskFile.emf");
myGraphics.DrawImage(&myImage, 100, 100);
```



O exemplo a seguir registra várias configurações de propriedade (região de recorte, transformação mundial e modo de suavização) em um [**objeto Metafile.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) Em seguida, o código registra várias instruções de desenho. As instruções e as configurações são salvas em um arquivo de disco.


```
myMetafile = new Metafile(L"MyDiskFile2.emf", hdc); 
myGraphics = new Graphics(myMetafile);
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->RotateTransform(30);

   // Create an elliptical clipping region.
   GraphicsPath myPath;
   myPath.AddEllipse(0, 0, 200, 100);
   Region myRegion(&myPath);
   myGraphics->SetClip(&myRegion);

   Pen myPen(Color(255, 0, 0, 255));
   myGraphics->DrawPath(&myPen, &myPath);

   for(INT j = 0; j <= 300; j += 10)
   {
      myGraphics->DrawLine(&myPen, 0, 0, 300 - j, j);
   }
delete myGraphics;
delete myMetafile;
```



O exemplo a seguir exibe a imagem de metadados criada no exemplo anterior.


```
myGraphics = new Graphics(hdc);
myMetafile = new Metafile(L"MyDiskFile.emf");
myGraphics->DrawImage(myMetafile, 10, 10);
```



A ilustração a seguir mostra a saída do código anterior. Observe a antialiação, a região de recorte elíptico e a rotação de 30 graus.

![captura de tela de uma janela que contém uma elipse preenchida com linhas originadas em um ponto fora da elipse](images/aboutgdip05-art00.png)

 

 



