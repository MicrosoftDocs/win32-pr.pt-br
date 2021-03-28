---
description: Para aplicar formatação especial ao texto, inicialize um objeto StringFormat e passe o endereço desse objeto para o método DrawString da classe Graphics.
ms.assetid: 4014a602-88f6-4fac-b4b2-3dafdcff8f33
title: Formatar texto (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6b2cc6109e7b946e9b4e98645c9445b8268bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563243"
---
# <a name="formatting-text-gdi"></a><span data-ttu-id="5feab-103">Formatar texto (GDI+)</span><span class="sxs-lookup"><span data-stu-id="5feab-103">Formatting Text (GDI+)</span></span>

<span data-ttu-id="5feab-104">Para aplicar formatação especial ao texto, inicialize um objeto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) e passe o endereço desse objeto para o método [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="5feab-104">To apply special formatting to text, initialize a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object and pass the address of that object to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span>

<span data-ttu-id="5feab-105">Para desenhar texto formatado em um retângulo, você precisa de objetos [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)e [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="5feab-105">To draw formatted text in a rectangle, you need [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), and [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

-   [<span data-ttu-id="5feab-106">Alinhando texto</span><span class="sxs-lookup"><span data-stu-id="5feab-106">Aligning Text</span></span>](#aligning-text)
-   [<span data-ttu-id="5feab-107">Configurando paradas de tabulação</span><span class="sxs-lookup"><span data-stu-id="5feab-107">Setting Tab Stops</span></span>](#setting-tab-stops)
-   [<span data-ttu-id="5feab-108">Desenho de texto vertical</span><span class="sxs-lookup"><span data-stu-id="5feab-108">Drawing Vertical Text</span></span>](#drawing-vertical-text)

## <a name="aligning-text"></a><span data-ttu-id="5feab-109">Alinhando texto</span><span class="sxs-lookup"><span data-stu-id="5feab-109">Aligning Text</span></span>

<span data-ttu-id="5feab-110">O exemplo a seguir desenha o texto em um retângulo.</span><span class="sxs-lookup"><span data-stu-id="5feab-110">The following example draws text in a rectangle.</span></span> <span data-ttu-id="5feab-111">Cada linha de texto é centralizada (lado a lado) e todo o bloco de texto é centralizado (de cima para baixo) no retângulo.</span><span class="sxs-lookup"><span data-stu-id="5feab-111">Each line of text is centered (side to side), and the entire block of text is centered (top to bottom) in the rectangle.</span></span>


```
WCHAR string[] = 
   L"Use StringFormat and RectF objects to center text in a rectangle.";
                       
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 120.0f, 140.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

// Center-justify each line of text.
stringFormat.SetAlignment(StringAlignmentCenter);

// Center the block of text (top to bottom) in the rectangle.
stringFormat.SetLineAlignment(StringAlignmentCenter);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



<span data-ttu-id="5feab-112">A ilustração a seguir mostra o retângulo e o texto centralizado.</span><span class="sxs-lookup"><span data-stu-id="5feab-112">The following illustration shows the rectangle and the centered text.</span></span>

![captura de tela de uma janela que contém um retângulo, que contém seis linhas de texto, centralizado horizontalmente](images/fontstext3.png)

<span data-ttu-id="5feab-114">O código anterior chama dois métodos do objeto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) : [**StringFormat:: setAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) e [**StringFormat:: SetLineAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment).</span><span class="sxs-lookup"><span data-stu-id="5feab-114">The preceding code calls two methods of the [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object: [**StringFormat::SetAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) and [**StringFormat::SetLineAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment).</span></span> <span data-ttu-id="5feab-115">A chamada para **StringFormat:: setAlignment** especifica que cada linha de texto é centralizada no retângulo fornecido pelo terceiro argumento passado para o método [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) .</span><span class="sxs-lookup"><span data-stu-id="5feab-115">The call to **StringFormat::SetAlignment** specifies that each line of text is centered in the rectangle given by the third argument passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method.</span></span> <span data-ttu-id="5feab-116">A chamada para **StringFormat:: SetLineAlignment** especifica que o bloco de texto é centralizado (de cima para baixo) no retângulo.</span><span class="sxs-lookup"><span data-stu-id="5feab-116">The call to **StringFormat::SetLineAlignment** specifies that the block of text is centered (top to bottom) in the rectangle.</span></span>

<span data-ttu-id="5feab-117">O valor [\* \* \* \* StringAlignmentCenter \* \* \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) é um elemento da enumeração **StringAlignment** , que é declarado em Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="5feab-117">The value [\*\*\*\*StringAlignmentCenter\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) is an element of the **StringAlignment** enumeration, which is declared in Gdiplusenums.h.</span></span>

## <a name="setting-tab-stops"></a><span data-ttu-id="5feab-118">Configurando paradas de tabulação</span><span class="sxs-lookup"><span data-stu-id="5feab-118">Setting Tab Stops</span></span>

<span data-ttu-id="5feab-119">Você pode definir tabulações de tabulação para texto chamando o método [**StringFormat:: SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) de um objeto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) e, em seguida, passando o endereço desse objeto **StringFormat** para o método [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="5feab-119">You can set tab stops for text by calling the [**StringFormat::SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) method of a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object and then passing the address of that **StringFormat** object to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span>

<span data-ttu-id="5feab-120">O exemplo a seguir define as paradas de tabulação em 150, 250 e 350.</span><span class="sxs-lookup"><span data-stu-id="5feab-120">The following example sets tab stops at 150, 250, and 350.</span></span> <span data-ttu-id="5feab-121">Em seguida, o código exibe uma lista com guias de nomes e pontuações de teste.</span><span class="sxs-lookup"><span data-stu-id="5feab-121">Then the code displays a tabbed list of names and test scores.</span></span>


```
WCHAR string[150] = 
   L"Name\tTest 1\tTest 2\tTest 3\n";

StringCchCatW(string, 150, L"Joe\t95\t88\t91\n");
StringCchCatW(string, 150, L"Mary\t98\t84\t90\n");
StringCchCatW(string, 150, L"Sam\t42\t76\t98\n");
StringCchCatW(string, 150, L"Jane\t65\t73\t92\n");
                       
FontFamily   fontFamily(L"Courier New");
Font         font(&fontFamily, 12, FontStyleRegular, UnitPoint);
RectF        rectF(10.0f, 10.0f, 450.0f, 100.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));
REAL         tabs[] = {150.0f, 100.0f, 100.0f};

stringFormat.SetTabStops(0.0f, 3, tabs);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



<span data-ttu-id="5feab-122">A ilustração a seguir mostra o texto com guias.</span><span class="sxs-lookup"><span data-stu-id="5feab-122">The following illustration shows the tabbed text.</span></span>

![ilustração de um retângulo que contém quatro colunas de texto; cada coluna é esquerda-alinhado](images/fontstext4.png)

<span data-ttu-id="5feab-124">O código anterior passa três argumentos para o método [**StringFormat:: SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) .</span><span class="sxs-lookup"><span data-stu-id="5feab-124">The preceding code passes three arguments to the [**StringFormat::SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) method.</span></span> <span data-ttu-id="5feab-125">O terceiro argumento é o endereço de uma matriz que contém os deslocamentos da guia.</span><span class="sxs-lookup"><span data-stu-id="5feab-125">The third argument is the address of an array containing the tab offsets.</span></span> <span data-ttu-id="5feab-126">O segundo argumento indica que há três deslocamentos nessa matriz.</span><span class="sxs-lookup"><span data-stu-id="5feab-126">The second argument indicates that there are three offsets in that array.</span></span> <span data-ttu-id="5feab-127">O primeiro argumento passado para **StringFormat:: SetTabStops** é 0, o que indica que o primeiro deslocamento na matriz é medido da posição 0, a borda esquerda do retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="5feab-127">The first argument passed to **StringFormat::SetTabStops** is 0, which indicates that the first offset in the array is measured from position 0, the left edge of the bounding rectangle.</span></span>

## <a name="drawing-vertical-text"></a><span data-ttu-id="5feab-128">Desenho de texto vertical</span><span class="sxs-lookup"><span data-stu-id="5feab-128">Drawing Vertical Text</span></span>

<span data-ttu-id="5feab-129">Você pode usar um objeto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) para especificar que o texto seja desenhado verticalmente em vez de horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="5feab-129">You can use a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object to specify that text be drawn vertically rather than horizontally.</span></span>

<span data-ttu-id="5feab-130">O exemplo a seguir passa o valor [\* \* \* \* StringFormatFlagsDirectionVertical \* \* \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) para o método [**StringFormat:: SetFormatFlags**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags) de um objeto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) .</span><span class="sxs-lookup"><span data-stu-id="5feab-130">The following example passes the value [\*\*\*\*StringFormatFlagsDirectionVertical\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) to the [**StringFormat::SetFormatFlags**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags) method of a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object.</span></span> <span data-ttu-id="5feab-131">O endereço desse objeto **StringFormat** é passado para o método [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="5feab-131">The address of that **StringFormat** object is passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="5feab-132">O valor [\* \* \* \* StringFormatFlagsDirectionVertical \* \* \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) é um elemento da enumeração **StringFormatFlags** , que é declarado em Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="5feab-132">The value [\*\*\*\*StringFormatFlagsDirectionVertical\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) is an element of the **StringFormatFlags** enumeration, which is declared in Gdiplusenums.h.</span></span>


```
WCHAR string[] = L"Vertical text";
                     
FontFamily   fontFamily(L"Lucida Console");
Font         font(&fontFamily, 14, FontStyleRegular, UnitPoint);
PointF       pointF(40.0f, 10.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

stringFormat.SetFormatFlags(StringFormatFlagsDirectionVertical);

graphics.DrawString(string, -1, &font, pointF, &stringFormat, &solidBrush);
            
```



<span data-ttu-id="5feab-133">A ilustração a seguir mostra o texto vertical.</span><span class="sxs-lookup"><span data-stu-id="5feab-133">The following illustration shows the vertical text.</span></span>

![ilustração mostrando uma janela que contém o texto girado 90 graus no sentido horário](images/fontstext5.png)

 

 



