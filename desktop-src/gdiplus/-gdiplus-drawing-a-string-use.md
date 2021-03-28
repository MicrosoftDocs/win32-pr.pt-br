---
description: O tópico desenhando uma linha mostra como escrever um aplicativo do Windows que usa o Windows GDI+ para desenhar uma linha.
ms.assetid: fcf45b19-456c-4551-8901-d587a73a5638
title: Desenhar uma cadeia de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a88e76fd38dd640a402edf202dc6cdbd3008a76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165466"
---
# <a name="drawing-a-string"></a><span data-ttu-id="8ce67-103">Desenhar uma cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="8ce67-103">Drawing a String</span></span>

<span data-ttu-id="8ce67-104">O tópico [desenhando uma linha](-gdiplus-drawing-a-line-use.md) mostra como escrever um aplicativo do Windows que usa o Windows GDI+ para desenhar uma linha.</span><span class="sxs-lookup"><span data-stu-id="8ce67-104">The topic [Drawing a Line](-gdiplus-drawing-a-line-use.md) shows how to write a Windows application that uses Windows GDI+ to draw a line.</span></span> <span data-ttu-id="8ce67-105">Para desenhar uma cadeia de caracteres, substitua a função **OnPaint** mostrada no tópico pela seguinte função **OnPaint** :</span><span class="sxs-lookup"><span data-stu-id="8ce67-105">To draw a string, replace the **OnPaint** function shown in that topic with the following **OnPaint** function:</span></span>


```
VOID OnPaint(HDC hdc)
{
   Graphics    graphics(hdc);
   SolidBrush  brush(Color(255, 0, 0, 255));
   FontFamily  fontFamily(L"Times New Roman");
   Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   PointF      pointF(10.0f, 20.0f);
   
   graphics.DrawString(L"Hello World!", -1, &font, pointF, &brush);
}
```



<span data-ttu-id="8ce67-106">O código anterior cria vários objetos GDI+.</span><span class="sxs-lookup"><span data-stu-id="8ce67-106">The previous code creates several GDI+ objects.</span></span> <span data-ttu-id="8ce67-107">O objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornece o método [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) , que faz o desenho real.</span><span class="sxs-lookup"><span data-stu-id="8ce67-107">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object provides the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method, which does the actual drawing.</span></span> <span data-ttu-id="8ce67-108">O objeto [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) especifica a cor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8ce67-108">The [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object specifies the color of the string.</span></span>

<span data-ttu-id="8ce67-109">O construtor [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) recebe um único argumento de cadeia de caracteres que identifica a família de fontes.</span><span class="sxs-lookup"><span data-stu-id="8ce67-109">The [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) constructor receives a single, string argument that identifies the font family.</span></span> <span data-ttu-id="8ce67-110">O endereço do objeto **FontFamily** é o primeiro argumento passado para o construtor [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="8ce67-110">The address of the **FontFamily** object is the first argument passed to the [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) constructor.</span></span> <span data-ttu-id="8ce67-111">O segundo argumento passado para o construtor de [fonte](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(constfont_)) especifica o tamanho da fonte e o terceiro argumento especifica o estilo.</span><span class="sxs-lookup"><span data-stu-id="8ce67-111">The second argument passed to the [Font](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(constfont_)) constructor specifies the font size, and the third argument specifies the style.</span></span> <span data-ttu-id="8ce67-112">O valor **FontStyleRegular** é um membro da enumeração [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) , que é declarado em Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="8ce67-112">The value **FontStyleRegular** is a member of the [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) enumeration, which is declared in Gdiplusenums.h.</span></span> <span data-ttu-id="8ce67-113">O último argumento para o construtor de **fonte** indica que o tamanho da fonte (24, nesse caso) é medido em pixels.</span><span class="sxs-lookup"><span data-stu-id="8ce67-113">The last argument to the **Font** constructor indicates that the size of the font (24 in this case) is measured in pixels.</span></span> <span data-ttu-id="8ce67-114">O valor **UnitPixel** é um membro da enumeração de [**unidade**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-unit) .</span><span class="sxs-lookup"><span data-stu-id="8ce67-114">The value **UnitPixel** is a member of the [**Unit**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-unit) enumeration.</span></span>

<span data-ttu-id="8ce67-115">O primeiro argumento passado para o método [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) é o endereço de uma cadeia de caracteres largos.</span><span class="sxs-lookup"><span data-stu-id="8ce67-115">The first argument passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method is the address of a wide-character string.</span></span> <span data-ttu-id="8ce67-116">O segundo argumento, – 1, especifica que a cadeia de caracteres é terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="8ce67-116">The second argument, –1, specifies that the string is null terminated.</span></span> <span data-ttu-id="8ce67-117">(Se a cadeia de caracteres não for terminada em nulo, o segundo argumento deverá especificar o número de caracteres largos na cadeia de caracteres.) O terceiro argumento é o endereço do objeto [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="8ce67-117">(If the string is not null terminated, the second argument should specify the number of wide characters in the string.) The third argument is the address of the [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span> <span data-ttu-id="8ce67-118">O quarto argumento é uma referência a um objeto [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) que especifica o local onde a cadeia de caracteres será desenhada.</span><span class="sxs-lookup"><span data-stu-id="8ce67-118">The fourth argument is a reference to a [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) object that specifies the location where the string will be drawn.</span></span> <span data-ttu-id="8ce67-119">O último argumento é o endereço do objeto [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) , que especifica a cor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8ce67-119">The last argument is the address of the [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object, which specifies the color of the string.</span></span>

 

 
