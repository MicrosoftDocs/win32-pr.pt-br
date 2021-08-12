---
description: Windows GDI+ fornece vários níveis de qualidade para desenhar texto. Normalmente, a renderização de qualidade mais alta leva mais tempo de processamento do que a renderização de qualidade inferior.
ms.assetid: 780d97ec-f446-4d19-837f-517a7d6dd27d
title: Antialiasing com texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9411206351340f58b63196ff880745743ad92325918b112ad2ddb5bcb8591e9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118249920"
---
# <a name="antialiasing-with-text"></a>Antialiasing com texto

Windows GDI+ fornece vários níveis de qualidade para desenhar texto. Normalmente, a renderização de qualidade mais alta leva mais tempo de processamento do que a renderização de qualidade inferior.

O nível de qualidade é uma propriedade da [**classe Graphics.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Para definir o nível de qualidade, chame o [**método Graphics::SetTextRenderingHint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) de **um objeto Graphics.** O **método Graphics::SetTextRenderingHint** recebe um dos elementos da enumeração [**TextRenderingHint,**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) que é declarada em Gdiplusenums.h.

GDI+ fornece antialiasing tradicional e um novo tipo de antialiasing com base na tecnologia de exibição Microsoft ClearType disponível somente no Windows XP e no Windows Server 2003 e versões posteriores do Windows. A suavização ClearType aprimora a capacidade de leitura em monitores DE COR DO LCD que têm uma interface digital, como os monitores em laptops e telas de área de trabalho simples de alta qualidade. A capacidade de leitura em telas CRT também é um pouco aprimorada.

ClearType depende da orientação e da ordenação das faixas DE LCD. Atualmente, ClearType é implementado somente para faixas verticais que são RGB ordenadas. Isso pode ser uma preocupação se você estiver usando um computador tablet, em que a exibição pode ser orientada em qualquer direção ou se você estiver usando uma tela que pode ser transformada de paisagem em retrato.

O exemplo a seguir desenha texto com duas configurações de qualidade diferentes:


```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 32, FontStyleRegular, UnitPixel);
SolidBrush  solidBrush(Color(255, 0, 0, 255));
WCHAR       string1[] = L"SingleBitPerPixel";
WCHAR       string2[] = L"AntiAlias";

graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);
graphics.DrawString(string1, -1, &font, PointF(10.0f, 10.0f), &solidBrush);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
graphics.DrawString(string2, -1, &font, PointF(10.0f, 60.0f), &solidBrush);
            
```



A ilustração a seguir mostra a saída do código anterior.

![captura de tela de uma cadeia de caracteres cujos caracteres têm bordas irregulares contrastadas com uma com bordas suaves](images/fontstext10.png)

 

 



