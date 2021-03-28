---
description: 'A classe FontFamily fornece os seguintes métodos que recuperam várias métricas para uma combinação específica de família/estilo:'
ms.assetid: 3be485d0-9e0d-43e0-813e-668102ebc010
title: Obtendo métricas de fonte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800fcee7dd1729a6fd5e59bb5dd636af89670776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010473"
---
# <a name="obtaining-font-metrics"></a>Obtendo métricas de fonte

A classe [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) fornece os seguintes métodos que recuperam várias métricas para uma combinação específica de família/estilo:

-   [**FontFamily:: GetEmHeight**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight)(FontStyle)
-   [**FontFamily:: GetCellAscent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent)(FontStyle)
-   [**FontFamily:: GetCellDescent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent)(FontStyle)
-   [**FontFamily:: GetLineSpacing**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing)(FontStyle)

Os números retornados por esses métodos estão em unidades de design de fontes, portanto, eles são independentes do tamanho e das unidades de um objeto de [**fonte**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) específico.

A ilustração a seguir mostra o espaçamento ascendente, descendente e linha.

![diagrama de dois caracteres em linhas adjacentes, mostrando células ascendentes, descendente de célula e espaçamento de linha](images/fontstext7a.png)

O exemplo a seguir exibe as métricas para o estilo normal da família de fontes Arial. O código também cria um objeto [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) (com base na família Arial) com tamanho de 16 pixels e exibe as métricas (em pixels) para esse objeto de **fonte** específico.


```
#define INFO_STRING_SIZE 100  // one line of output including null terminator
WCHAR infoString[INFO_STRING_SIZE] = L"";
UINT  ascent;                 // font family ascent in design units
REAL  ascentPixel;            // ascent converted to pixels
UINT  descent;                // font family descent in design units
REAL  descentPixel;           // descent converted to pixels
UINT  lineSpacing;            // font family line spacing in design units
REAL  lineSpacingPixel;       // line spacing converted to pixels
                       
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 16, FontStyleRegular, UnitPixel);
PointF       pointF(10.0f, 10.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 0));

// Display the font size in pixels.
StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE, 
   L"font.GetSize() returns %f.", font.GetSize());

graphics.DrawString(
   infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0);

// Display the font family em height in design units.
StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE, 
   L"fontFamily.GetEmHeight() returns %d.", 
   fontFamily.GetEmHeight(FontStyleRegular));

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down two lines.
pointF.Y += 2.0f * font.GetHeight(0.0f);

// Display the ascent in design units and pixels.
ascent = fontFamily.GetCellAscent(FontStyleRegular);

// 14.484375 = 16.0 * 1854 / 2048
ascentPixel = 
   font.GetSize() * ascent / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString,
   INFO_STRING_SIZE,
   L"The ascent is %d design units, %f pixels.",
   ascent, 
   ascentPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0f);

// Display the descent in design units and pixels.
descent = fontFamily.GetCellDescent(FontStyleRegular);

// 3.390625 = 16.0 * 434 / 2048
descentPixel = 
   font.GetSize() * descent / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE,
   L"The descent is %d design units, %f pixels.",
   descent, 
   descentPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0f);

// Display the line spacing in design units and pixels.
lineSpacing = fontFamily.GetLineSpacing(FontStyleRegular);

// 18.398438 = 16.0 * 2355 / 2048
lineSpacingPixel = 
   font.GetSize() * lineSpacing / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE,
   L"The line spacing is %d design units, %f pixels.",
   lineSpacing, 
   lineSpacingPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);
            
```



A ilustração a seguir mostra a saída do código anterior.

![captura de tela de uma janela com texto que informa o tamanho e a altura da fonte e o espaçamento ascendente, descendente e linha](images/fontstext8.png)

Observe as duas primeiras linhas de saída na ilustração anterior. O objeto [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) retorna um tamanho de 16 e o objeto [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) retorna uma altura de 2.048. Esses dois números (16 e 2.048) são a chave para converter entre as unidades de design de fonte e as unidades (neste caso, pixels) do objeto de **fonte** .

Por exemplo, você pode converter o ascendente de unidades de design em pixels da seguinte maneira:

![equação que multiplica as unidades de design de 1854 por 16 pixels divididos por 2048 unidades de design, iguais a 14,484375 pixels](images/fontstext9.png)

O código anterior posiciona o texto verticalmente, definindo o membro de dados *y* de um objeto [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) . A coordenada y é aumentada em `font.GetHeight(0.0f)` para cada nova linha de texto. O método [**Font:: GetHeight**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal)) de um objeto [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) retorna o espaçamento de linha (em pixels) para esse objeto **Font** específico. Neste exemplo, o número retornado pela **fonte:: GetHeight** é 18,398438. Observe que isso é o mesmo que o número obtido pela conversão da métrica de espaçamento de linha em pixels.

 

 
