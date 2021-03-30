---
description: Uma figura fechada, como um retângulo ou uma elipse, consiste em uma estrutura de tópicos e um interior.
ms.assetid: 889558d5-9181-43ff-b862-e92966324208
title: Pincéis e formas preenchidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb772be88ce26325337fd9c88fc0319631895e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555652"
---
# <a name="brushes-and-filled-shapes"></a>Pincéis e formas preenchidas

Uma figura fechada, como um retângulo ou uma elipse, consiste em uma estrutura de tópicos e um interior. A estrutura de tópicos é desenhada com um objeto de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e o interior é preenchido com um objeto de [**pincel**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) . O Windows GDI+ fornece várias classes de pincel para preencher os interiores de figuras fechadas: [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)e [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush). Todas essas classes herdam da classe **Brush** . A ilustração a seguir mostra um retângulo preenchido com um pincel sólido e uma elipse preenchida com um pincel de hachura.

![ilustração mostrando um retângulo azul e uma elipse magenta preenchida com um padrão de hachura azul](images/aboutgdip02-art17.png)

 

-   [Pincéis Sólidos](#solid-brushes)
-   [Pincéis de Hachura](#hatch-brushes)
-   [Pincéis de Textura](#texture-brushes)
-   [Pincéis de Gradiente](#gradient-brushes)

## <a name="solid-brushes"></a>Pincéis Sólidos

Para preencher uma forma fechada, você precisa de um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e um objeto de [**pincel**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) . O objeto **Graphics** fornece métodos, como [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) e [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_)), e o objeto **Brush** armazena os atributos do preenchimento, como Color e Pattern. O endereço do objeto **Brush** é passado como um dos argumentos para o método Fill. O exemplo a seguir preenche uma elipse com uma cor vermelha sólida.


```
SolidBrush mySolidBrush(Color(255, 255, 0, 0));
myGraphics.FillEllipse(&mySolidBrush, 0, 0, 60, 40);
```



Observe que, no exemplo anterior, o pincel é do tipo [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), que é herdado de [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush).

## <a name="hatch-brushes"></a>Pincéis de Hachura

Ao preencher uma forma com um pincel de hachura, é necessário especificar uma cor de primeiro plano, uma cor da tela de fundo e um estilo de hachura. A cor de primeiro plano é a cor da hachura.


```
HatchBrush myHatchBrush(
   HatchStyleVertical, 
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0));
```



O GDI+ fornece mais de 50 estilos de hachura, especificados em [**HatchStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle). Os três estilos mostrados na ilustração a seguir são horizontal, ForwardDiagonal e Cross.

![ilustração mostrando três elipses com cor azul, cada uma com um estilo de hachura diferente](images/aboutgdip02-art18.png)

 

## <a name="texture-brushes"></a>Pincéis de Textura

Com um pincel de textura, é possível preencher uma forma com um padrão armazenado em um bitmap. Por exemplo, suponha que a imagem a seguir seja armazenada em um arquivo de disco chamado MyTexture.bmp.

![captura de tela de um quadrado pequeno preenchido com várias cores](images/aboutgdip02-art19.png)

O exemplo a seguir preenche uma elipse repetindo a imagem armazenada em MyTexture.bmp.


```
Image myImage(L"MyTexture.bmp");
TextureBrush myTextureBrush(&myImage);
myGraphics.FillEllipse(&myTextureBrush, 0, 0, 100, 50);
```



A ilustração a seguir mostra a elipse preenchida.

![ilustração mostrando uma elipse preenchida com o padrão definido anteriormente](images/aboutgdip02-art20.png)

 

## <a name="gradient-brushes"></a>Pincéis de Gradiente

Você pode usar um pincel de gradiente para preencher uma forma com uma cor que muda gradualmente de uma parte da forma para outra. Por exemplo, um pincel de gradiente horizontal mudará a cor à medida que você mover do lado esquerdo de uma figura para o lado direito. O exemplo a seguir preenche uma elipse com um pincel de gradiente horizontal que muda de azul para verde à medida que você move do lado esquerdo da elipse para o lado direito.


```
LinearGradientBrush myLinearGradientBrush(
   myRect,
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0),
   LinearGradientModeHorizontal);
myGraphics.FillEllipse(&myLinearGradientBrush, myRect); 
```



A ilustração a seguir mostra a elipse preenchida.

![ilustração mostrando uma elipse com preenchimento gradual: azul à direita para verde à esquerda](images/aboutgdip02-art21.png)

Um pincel de gradiente de caminho pode ser configurado para alterar a cor à medida que você passa do centro de uma figura para o limite.

![ilustration de uma elipse que é azul escuro no centro, sombreamento para azul claro na borda](images/aboutgdip02-art22.png)

Pincéis de gradiente de caminho são bastante flexíveis. O pincel de gradiente usado para preencher o triângulo nas seguintes ilustrações altera gradualmente de vermelho no centro para cada uma das três cores diferentes nos vértices.

![ilustração de um triângulo que é vermelho no centro, sombreamento para uma cor diferente em cada vértice](images/aboutgdip02-art23.png)

 

 



