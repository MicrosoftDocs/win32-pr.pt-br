---
description: Você pode usar o método DrawString da classe Graphics para desenhar texto em um local especificado ou dentro de um retângulo especificado.
ms.assetid: a873c132-f232-4144-bcc3-ca200055074c
title: Desenhar texto (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e16ed49a5ab92380b42ed3316346ac547f95be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091470"
---
# <a name="drawing-text-gdi"></a><span data-ttu-id="5650b-103">Desenhar texto (GDI+)</span><span class="sxs-lookup"><span data-stu-id="5650b-103">Drawing Text (GDI+)</span></span>

<span data-ttu-id="5650b-104">Você pode usar o método [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para desenhar texto em um local especificado ou dentro de um retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="5650b-104">You can use the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw text at a specified location or within a specified rectangle.</span></span>

-   [<span data-ttu-id="5650b-105">Texto de desenho em um local especificado</span><span class="sxs-lookup"><span data-stu-id="5650b-105">Drawing Text at a Specified Location</span></span>](#drawing-text-at-a-specified-location)
-   [<span data-ttu-id="5650b-106">Desenhar texto em um retângulo</span><span class="sxs-lookup"><span data-stu-id="5650b-106">Drawing Text in a Rectangle</span></span>](#drawing-text-in-a-rectangle)

## <a name="drawing-text-at-a-specified-location"></a><span data-ttu-id="5650b-107">Texto de desenho em um local especificado</span><span class="sxs-lookup"><span data-stu-id="5650b-107">Drawing Text at a Specified Location</span></span>

<span data-ttu-id="5650b-108">Para desenhar texto em um local especificado, você precisa de objetos [**gráficos**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf)e [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="5650b-108">To draw text at a specified location, you need [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf), and [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

<span data-ttu-id="5650b-109">O exemplo a seguir desenha a cadeia de caracteres "Olá" no local (30, 10).</span><span class="sxs-lookup"><span data-stu-id="5650b-109">The following example draws the string "Hello" at location (30, 10).</span></span> <span data-ttu-id="5650b-110">A família de fontes é Times New Roman.</span><span class="sxs-lookup"><span data-stu-id="5650b-110">The font family is Times New Roman.</span></span> <span data-ttu-id="5650b-111">A fonte, que é um membro individual da família de fontes, é Times New Roman, tamanho 24 pixels, estilo regular.</span><span class="sxs-lookup"><span data-stu-id="5650b-111">The font, which is an individual member of the font family, is Times New Roman, size 24 pixels, regular style.</span></span> <span data-ttu-id="5650b-112">Suponha que **gráficos** seja um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) existente.</span><span class="sxs-lookup"><span data-stu-id="5650b-112">Assume that **graphics** is an existing [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
PointF      pointF(30.0f, 10.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(L"Hello", -1, &font, pointF, &solidBrush);

```

<span data-ttu-id="5650b-113">A ilustração a seguir mostra a saída do código anterior.</span><span class="sxs-lookup"><span data-stu-id="5650b-113">The following illustration shows the output of the preceding code.</span></span>

![captura de tela de uma pequena janela que contém o texto "Olá"](images/fontstext1.png)

<span data-ttu-id="5650b-115">No exemplo anterior, o construtor [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) recebe uma cadeia de caracteres que identifica a família de fontes.</span><span class="sxs-lookup"><span data-stu-id="5650b-115">In the preceding example, the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) constructor receives a string that identifies the font family.</span></span> <span data-ttu-id="5650b-116">O endereço do objeto **FontFamily** é passado como o primeiro argumento para o construtor [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="5650b-116">The address of the **FontFamily** object is passed as the first argument to the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) constructor.</span></span> <span data-ttu-id="5650b-117">O segundo argumento passado para o construtor **Font** especifica o tamanho da fonte medida em unidades fornecidas pelo quarto argumento.</span><span class="sxs-lookup"><span data-stu-id="5650b-117">The second argument passed to the **Font** constructor specifies the size of the font measured in units given by the fourth argument.</span></span> <span data-ttu-id="5650b-118">O terceiro argumento especifica o estilo (regular, negrito, itálico e assim por diante) da fonte.</span><span class="sxs-lookup"><span data-stu-id="5650b-118">The third argument specifies the style (regular, bold, italic, and so on) of the font.</span></span>

<span data-ttu-id="5650b-119">O método [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) recebe cinco argumentos.</span><span class="sxs-lookup"><span data-stu-id="5650b-119">The [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method receives five arguments.</span></span> <span data-ttu-id="5650b-120">O primeiro argumento é a cadeia de caracteres a ser desenhada, e o segundo argumento é o comprimento (em caracteres, não bytes) dessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5650b-120">The first argument is the string to be drawn, and the second argument is the length (in characters, not bytes) of that string.</span></span> <span data-ttu-id="5650b-121">Se a cadeia de caracteres for terminada em nulo, você poderá passar – 1 para o comprimento.</span><span class="sxs-lookup"><span data-stu-id="5650b-121">If the string is null-terminated, you can pass –1 for the length.</span></span> <span data-ttu-id="5650b-122">O terceiro argumento é o endereço do objeto de [**fonte**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) que foi construído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5650b-122">The third argument is the address of the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object that was constructed previously.</span></span> <span data-ttu-id="5650b-123">O quarto argumento é um objeto [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) que contém as coordenadas do canto superior esquerdo da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5650b-123">The fourth argument is a [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) object that contains the coordinates of the upper-left corner of the string.</span></span> <span data-ttu-id="5650b-124">O quinto argumento é o endereço de um objeto [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) que será usado para preencher os caracteres da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5650b-124">The fifth argument is the address of a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object that will be used to fill the characters of the string.</span></span>

## <a name="drawing-text-in-a-rectangle"></a><span data-ttu-id="5650b-125">Desenhar texto em um retângulo</span><span class="sxs-lookup"><span data-stu-id="5650b-125">Drawing Text in a Rectangle</span></span>

<span data-ttu-id="5650b-126">Um dos métodos [**drawstring**](https://www.bing.com/search?q=**DrawString**) da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) tem um parâmetro *RectF* .</span><span class="sxs-lookup"><span data-stu-id="5650b-126">One of the [**DrawString**](https://www.bing.com/search?q=**DrawString**) methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class has a *RectF* parameter.</span></span> <span data-ttu-id="5650b-127">Chamando esse método **drawstring** , você pode desenhar o texto que encapsula um retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="5650b-127">By calling that **DrawString** method, you can draw text that wraps in a specified rectangle.</span></span> <span data-ttu-id="5650b-128">Para desenhar texto em um retângulo, você precisa de objetos **gráficos**, [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf)e [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="5650b-128">To draw text in a rectangle, you need **Graphics**, [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf), and [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

<span data-ttu-id="5650b-129">O exemplo a seguir cria um retângulo com o canto superior esquerdo (30, 10), largura 100 e altura 122.</span><span class="sxs-lookup"><span data-stu-id="5650b-129">The following example creates a rectangle with upper-left corner (30, 10), width 100, and height 122.</span></span> <span data-ttu-id="5650b-130">Em seguida, o código desenha uma cadeia de caracteres dentro desse retângulo.</span><span class="sxs-lookup"><span data-stu-id="5650b-130">Then the code draws a string inside that rectangle.</span></span> <span data-ttu-id="5650b-131">A cadeia de caracteres é restrita ao retângulo e encapsulada de forma que palavras individuais não sejam quebradas.</span><span class="sxs-lookup"><span data-stu-id="5650b-131">The string is restricted to the rectangle and wraps in such a way that individual words are not broken.</span></span>

```
WCHAR string[] = 
   L"Draw text in a rectangle by passing a RectF to the DrawString method.";

FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 100.0f, 122.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(string, -1, &font, rectF, NULL, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
```

<span data-ttu-id="5650b-132">A ilustração a seguir mostra o texto desenhado no retângulo.</span><span class="sxs-lookup"><span data-stu-id="5650b-132">The following illustration shows the text drawn in the rectangle.</span></span>

![captura de tela de uma pequena janela contendo um recangle, dentro do qual aparece a primeira parte de uma sentença](images/fontstext2.png)

<span data-ttu-id="5650b-134">No exemplo anterior, o quarto argumento passado para o método [**drawstring**](https://www.bing.com/search?q=**DrawString**) é um objeto [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) que especifica o retângulo delimitador para o texto.</span><span class="sxs-lookup"><span data-stu-id="5650b-134">In the preceding example, the fourth argument passed to the [**DrawString**](https://www.bing.com/search?q=**DrawString**) method is a [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) object that specifies the bounding rectangle for the text.</span></span> <span data-ttu-id="5650b-135">O quinto parâmetro é do tipo [**StringFormat**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)— o argumento é **nulo** porque nenhuma formatação de cadeia de caracteres especial é necessária.</span><span class="sxs-lookup"><span data-stu-id="5650b-135">The fifth parameter is of type [**StringFormat**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)— the argument is **NULL** because no special string formatting is required.</span></span>
