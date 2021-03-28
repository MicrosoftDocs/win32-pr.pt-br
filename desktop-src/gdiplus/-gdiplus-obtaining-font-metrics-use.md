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
# <a name="obtaining-font-metrics"></a><span data-ttu-id="3de57-103">Obtendo métricas de fonte</span><span class="sxs-lookup"><span data-stu-id="3de57-103">Obtaining Font Metrics</span></span>

<span data-ttu-id="3de57-104">A classe [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) fornece os seguintes métodos que recuperam várias métricas para uma combinação específica de família/estilo:</span><span class="sxs-lookup"><span data-stu-id="3de57-104">The [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) class provides the following methods that retrieve various metrics for a particular family/style combination:</span></span>

-   <span data-ttu-id="3de57-105">[**FontFamily:: GetEmHeight**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="3de57-105">[**FontFamily::GetEmHeight**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight)(FontStyle)</span></span>
-   <span data-ttu-id="3de57-106">[**FontFamily:: GetCellAscent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="3de57-106">[**FontFamily::GetCellAscent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent)(FontStyle)</span></span>
-   <span data-ttu-id="3de57-107">[**FontFamily:: GetCellDescent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="3de57-107">[**FontFamily::GetCellDescent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent)(FontStyle)</span></span>
-   <span data-ttu-id="3de57-108">[**FontFamily:: GetLineSpacing**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="3de57-108">[**FontFamily::GetLineSpacing**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing)(FontStyle)</span></span>

<span data-ttu-id="3de57-109">Os números retornados por esses métodos estão em unidades de design de fontes, portanto, eles são independentes do tamanho e das unidades de um objeto de [**fonte**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) específico.</span><span class="sxs-lookup"><span data-stu-id="3de57-109">The numbers returned by these methods are in font design units, so they are independent of the size and units of a particular [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span>

<span data-ttu-id="3de57-110">A ilustração a seguir mostra o espaçamento ascendente, descendente e linha.</span><span class="sxs-lookup"><span data-stu-id="3de57-110">The following illustration shows ascent, descent, and line spacing.</span></span>

![diagrama de dois caracteres em linhas adjacentes, mostrando células ascendentes, descendente de célula e espaçamento de linha](images/fontstext7a.png)

<span data-ttu-id="3de57-112">O exemplo a seguir exibe as métricas para o estilo normal da família de fontes Arial.</span><span class="sxs-lookup"><span data-stu-id="3de57-112">The following example displays the metrics for the regular style of the Arial font family.</span></span> <span data-ttu-id="3de57-113">O código também cria um objeto [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) (com base na família Arial) com tamanho de 16 pixels e exibe as métricas (em pixels) para esse objeto de **fonte** específico.</span><span class="sxs-lookup"><span data-stu-id="3de57-113">The code also creates a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object (based on the Arial family) with size 16 pixels and displays the metrics (in pixels) for that particular **Font** object.</span></span>


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



<span data-ttu-id="3de57-114">A ilustração a seguir mostra a saída do código anterior.</span><span class="sxs-lookup"><span data-stu-id="3de57-114">The following illustration shows the output of the preceding code.</span></span>

![captura de tela de uma janela com texto que informa o tamanho e a altura da fonte e o espaçamento ascendente, descendente e linha](images/fontstext8.png)

<span data-ttu-id="3de57-116">Observe as duas primeiras linhas de saída na ilustração anterior.</span><span class="sxs-lookup"><span data-stu-id="3de57-116">Note the first two lines of output in the preceding illustration.</span></span> <span data-ttu-id="3de57-117">O objeto [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) retorna um tamanho de 16 e o objeto [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) retorna uma altura de 2.048.</span><span class="sxs-lookup"><span data-stu-id="3de57-117">The [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object returns a size of 16, and the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object returns an em height of 2,048.</span></span> <span data-ttu-id="3de57-118">Esses dois números (16 e 2.048) são a chave para converter entre as unidades de design de fonte e as unidades (neste caso, pixels) do objeto de **fonte** .</span><span class="sxs-lookup"><span data-stu-id="3de57-118">These two numbers (16 and 2,048) are the key to converting between font design units and the units (in this case pixels) of the **Font** object.</span></span>

<span data-ttu-id="3de57-119">Por exemplo, você pode converter o ascendente de unidades de design em pixels da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3de57-119">For example, you can convert the ascent from design units to pixels as follows:</span></span>

![equação que multiplica as unidades de design de 1854 por 16 pixels divididos por 2048 unidades de design, iguais a 14,484375 pixels](images/fontstext9.png)

<span data-ttu-id="3de57-121">O código anterior posiciona o texto verticalmente, definindo o membro de dados *y* de um objeto [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) .</span><span class="sxs-lookup"><span data-stu-id="3de57-121">The preceding code positions text vertically by setting the *y* data member of a [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) object.</span></span> <span data-ttu-id="3de57-122">A coordenada y é aumentada em `font.GetHeight(0.0f)` para cada nova linha de texto.</span><span class="sxs-lookup"><span data-stu-id="3de57-122">The y-coordinate is increased by `font.GetHeight(0.0f)` for each new line of text.</span></span> <span data-ttu-id="3de57-123">O método [**Font:: GetHeight**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal)) de um objeto [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) retorna o espaçamento de linha (em pixels) para esse objeto **Font** específico.</span><span class="sxs-lookup"><span data-stu-id="3de57-123">The [**Font::GetHeight**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal)) method of a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object returns the line spacing (in pixels) for that particular **Font** object.</span></span> <span data-ttu-id="3de57-124">Neste exemplo, o número retornado pela **fonte:: GetHeight** é 18,398438.</span><span class="sxs-lookup"><span data-stu-id="3de57-124">In this example, the number returned by **Font::GetHeight** is 18.398438.</span></span> <span data-ttu-id="3de57-125">Observe que isso é o mesmo que o número obtido pela conversão da métrica de espaçamento de linha em pixels.</span><span class="sxs-lookup"><span data-stu-id="3de57-125">Note that this is the same as the number obtained by converting the line spacing metric to pixels.</span></span>

 

 
