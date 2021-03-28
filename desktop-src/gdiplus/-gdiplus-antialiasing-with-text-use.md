---
description: O Windows GDI+ fornece vários níveis de qualidade para o texto de desenho. Normalmente, a renderização de qualidade superior leva mais tempo de processamento do que a renderização de qualidade inferior.
ms.assetid: 780d97ec-f446-4d19-837f-517a7d6dd27d
title: Anti-aliasing com texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c7b7c59a436db6c16251aa8e866648eed5cc51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988928"
---
# <a name="antialiasing-with-text"></a>Anti-aliasing com texto

O Windows GDI+ fornece vários níveis de qualidade para o texto de desenho. Normalmente, a renderização de qualidade superior leva mais tempo de processamento do que a renderização de qualidade inferior.

O nível de qualidade é uma propriedade da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Para definir o nível de qualidade, chame o método [**Graphics:: SetTextRenderingHint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) de um objeto **Graphics** . O método **Graphics:: SetTextRenderingHint** recebe um dos elementos da enumeração [**TextRenderingHint**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) , que é declarado em Gdiplusenums. h.

A GDI+ fornece anti-aliasing tradicional e um novo tipo de anti-aliasing baseado na tecnologia de vídeo Microsoft ClearType disponível somente no Windows XP e no Windows Server 2003 e versões posteriores do Windows. A suavização de ClearType melhora a legibilidade em monitores de LCD colorido que têm uma interface digital, como os monitores em laptops e monitores de área de trabalho plana de alta qualidade. A legibilidade em telas CRT também é um pouco melhor.

O ClearType depende da orientação e da ordenação das faixas do LCD. Atualmente, o ClearType é implementado somente para faixas verticais que são ordenadas como RGB. Isso pode ser uma preocupação se você estiver usando um Tablet PC, onde a exibição pode ser orientada em qualquer direção ou se você estiver usando uma tela que pode ser transformada de paisagem para retrato.

O exemplo a seguir Desenha texto com duas configurações de qualidade diferentes:


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

![captura de tela de uma cadeia cujos caracteres têm bordas denteadas em contraste com uma com bordas suaves](images/fontstext10.png)

 

 



