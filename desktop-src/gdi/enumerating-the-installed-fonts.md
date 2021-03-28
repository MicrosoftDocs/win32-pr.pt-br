---
description: Em alguns casos, um aplicativo deve ser capaz de enumerar as fontes disponíveis e selecionar a mais apropriada para uma determinada operação.
ms.assetid: 18db1b03-6e3c-4be3-b637-a21bf41cc080
title: Enumerando as fontes instaladas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dee38ccf9807371181388536f1230d222d448bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165080"
---
# <a name="enumerating-the-installed-fonts"></a><span data-ttu-id="aaaff-103">Enumerando as fontes instaladas</span><span class="sxs-lookup"><span data-stu-id="aaaff-103">Enumerating the Installed Fonts</span></span>

<span data-ttu-id="aaaff-104">Em alguns casos, um aplicativo deve ser capaz de enumerar as fontes disponíveis e selecionar a mais apropriada para uma determinada operação.</span><span class="sxs-lookup"><span data-stu-id="aaaff-104">In some instances, an application must be able to enumerate the available fonts and select the one most appropriate for a particular operation.</span></span> <span data-ttu-id="aaaff-105">Um aplicativo pode enumerar as fontes disponíveis chamando a função [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) ou [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) .</span><span class="sxs-lookup"><span data-stu-id="aaaff-105">An application can enumerate the available fonts by calling the [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) or [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) function.</span></span> <span data-ttu-id="aaaff-106">Essas funções enviam informações sobre as fontes disponíveis para uma função de retorno de chamada que o aplicativo fornece.</span><span class="sxs-lookup"><span data-stu-id="aaaff-106">These functions send information about the available fonts to a callback function that the application supplies.</span></span> <span data-ttu-id="aaaff-107">A função de retorno de chamada recebe informações em estruturas [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) e [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .</span><span class="sxs-lookup"><span data-stu-id="aaaff-107">The callback function receives information in [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) and [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structures.</span></span> <span data-ttu-id="aaaff-108">(A estrutura [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) contém informações sobre uma fonte TrueType.</span><span class="sxs-lookup"><span data-stu-id="aaaff-108">(The [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure contains information about a TrueType font.</span></span> <span data-ttu-id="aaaff-109">Quando a função de retorno de chamada recebe informações sobre uma fonte não-TrueType, as informações estão contidas em uma estrutura [TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica) .) Usando essas informações, um aplicativo pode limitar as opções do usuário somente às fontes disponíveis.</span><span class="sxs-lookup"><span data-stu-id="aaaff-109">When the callback function receives information about a non-TrueType font, the information is contained in a [TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.) By using this information, an application can limit the user's choices to only those fonts that are available.</span></span>

<span data-ttu-id="aaaff-110">A função [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) é semelhante à função [**EnumFonts**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa) , mas inclui alguma funcionalidade extra.</span><span class="sxs-lookup"><span data-stu-id="aaaff-110">The [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function is similar to the [**EnumFonts**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa) function but includes some extra functionality.</span></span> <span data-ttu-id="aaaff-111">O **EnumFontFamilies** permite que um aplicativo aproveite os estilos disponíveis com fontes TrueType.</span><span class="sxs-lookup"><span data-stu-id="aaaff-111">**EnumFontFamilies** allows an application to take advantage of styles available with TrueType fonts.</span></span> <span data-ttu-id="aaaff-112">Aplicativos novos e atualizados devem usar **EnumFontFamilies** em vez de **EnumFonts**.</span><span class="sxs-lookup"><span data-stu-id="aaaff-112">New and upgraded applications should use **EnumFontFamilies** instead of **EnumFonts**.</span></span>

<span data-ttu-id="aaaff-113">As fontes TrueType são organizadas em um nome de tipo de letra (por exemplo, Courier New) e nomes de estilo (por exemplo, itálico, negrito e negrito extra).</span><span class="sxs-lookup"><span data-stu-id="aaaff-113">TrueType fonts are organized around a typeface name (for example, Courier New) and style names (for example, italic, bold, and extra-bold).</span></span> <span data-ttu-id="aaaff-114">A função [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) enumera todos os estilos associados a um nome de família especificado, e não apenas aos atributos Bold e italic.</span><span class="sxs-lookup"><span data-stu-id="aaaff-114">The [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function enumerates all the styles associated with a specified family name, not simply the bold and italic attributes.</span></span> <span data-ttu-id="aaaff-115">Por exemplo, quando o sistema inclui uma fonte TrueType chamada Courier New Extra-Bold, **EnumFontFamilies** a lista com as outras fontes do Courier New.</span><span class="sxs-lookup"><span data-stu-id="aaaff-115">For example, when the system includes a TrueType font called Courier New Extra-Bold, **EnumFontFamilies** lists it with the other Courier New fonts.</span></span> <span data-ttu-id="aaaff-116">Os recursos do **EnumFontFamilies** são úteis para fontes com estilos muitos ou incomuns e para fontes que cruzam bordas internacionais.</span><span class="sxs-lookup"><span data-stu-id="aaaff-116">The capabilities of **EnumFontFamilies** are helpful for fonts with many or unusual styles and for fonts that cross international borders.</span></span>

<span data-ttu-id="aaaff-117">Se um aplicativo não fornecer um nome de tipo, as funções [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) e [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) fornecerão informações sobre uma fonte em cada família disponível.</span><span class="sxs-lookup"><span data-stu-id="aaaff-117">If an application does not supply a typeface name, the [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) and [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) functions supply information about one font in each available family.</span></span> <span data-ttu-id="aaaff-118">Para enumerar todas as fontes em um contexto de dispositivo, o aplicativo pode especificar **NULL** para o nome de tipo, compilar uma lista de tipos disponíveis e, em seguida, enumerar cada fonte em cada tipo.</span><span class="sxs-lookup"><span data-stu-id="aaaff-118">To enumerate all the fonts in a device context, the application can specify **NULL** for the typeface name, compile a list of the available typefaces, and then enumerate each font in each typeface.</span></span>

<span data-ttu-id="aaaff-119">O exemplo a seguir usa a função [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) para recuperar o número de famílias de fontes rasterizadas, vetoriais e TrueType disponíveis.</span><span class="sxs-lookup"><span data-stu-id="aaaff-119">The following example uses the [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function to retrieve the number of available raster, vector, and TrueType font families.</span></span>


```C++
    UINT uAlignPrev; 
    int aFontCount[] = { 0, 0, 0 }; 
    char szCount[8];
        HRESULT hr;
        size_t * pcch; 
 
    EnumFontFamilies(hdc, (LPCTSTR) NULL, 
        (FONTENUMPROC) EnumFamCallBack, (LPARAM) aFontCount); 
 
    uAlignPrev = SetTextAlign(hdc, TA_UPDATECP); 
 
    MoveToEx(hdc, 10, 50, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of raster fonts: ", 24); 
    itoa(aFontCount[0], szCount, 10); 
        
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    MoveToEx(hdc, 10, 75, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of vector fonts: ", 24); 
    itoa(aFontCount[1], szCount, 10);
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    MoveToEx(hdc, 10, 100, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of TrueType fonts: ", 26); 
    itoa(aFontCount[2], szCount, 10);
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    SetTextAlign(hdc, uAlignPrev); 
 
BOOL CALLBACK EnumFamCallBack(LPLOGFONT lplf, LPNEWTEXTMETRIC lpntm, DWORD FontType, LPVOID aFontCount) 
{ 
    int far * aiFontCount = (int far *) aFontCount; 
 
    // Record the number of raster, TrueType, and vector  
    // fonts in the font-count array.  
 
    if (FontType & RASTER_FONTTYPE) 
        aiFontCount[0]++; 
    else if (FontType & TRUETYPE_FONTTYPE) 
        aiFontCount[2]++; 
    else 
        aiFontCount[1]++; 
 
    if (aiFontCount[0] || aiFontCount[1] || aiFontCount[2]) 
        return TRUE; 
    else 
        return FALSE; 
 
    UNREFERENCED_PARAMETER( lplf ); 
    UNREFERENCED_PARAMETER( lpntm ); 
} 
```



<span data-ttu-id="aaaff-120">Este exemplo usa duas máscaras, RASTER \_ FontType e TrueType \_ FontType, para determinar o tipo de fonte que está sendo enumerada.</span><span class="sxs-lookup"><span data-stu-id="aaaff-120">This example uses two masks, RASTER\_FONTTYPE and TRUETYPE\_FONTTYPE, to determine the type of font being enumerated.</span></span> <span data-ttu-id="aaaff-121">Se o \_ bit FontType de rasterização for definido, a fonte será uma fonte de rasterização.</span><span class="sxs-lookup"><span data-stu-id="aaaff-121">If the RASTER\_FONTTYPE bit is set, the font is a raster font.</span></span> <span data-ttu-id="aaaff-122">Se o \_ bit FontType TrueType for definido, a fonte será uma fonte TrueType.</span><span class="sxs-lookup"><span data-stu-id="aaaff-122">If the TRUETYPE\_FONTTYPE bit is set, the font is a TrueType font.</span></span> <span data-ttu-id="aaaff-123">Se nenhum bit for definido, a fonte será uma fonte vetorial.</span><span class="sxs-lookup"><span data-stu-id="aaaff-123">If neither bit is set, the font is a vector font.</span></span> <span data-ttu-id="aaaff-124">Uma terceira máscara, \_ FontType de dispositivo, é definida quando um dispositivo (por exemplo, uma impressora laser) dá suporte ao download de fontes TrueType; será zero se o dispositivo for um adaptador de vídeo, uma impressora matricial ou outro dispositivo de varredura.</span><span class="sxs-lookup"><span data-stu-id="aaaff-124">A third mask, DEVICE\_FONTTYPE, is set when a device (for example, a laser printer) supports downloading TrueType fonts; it is zero if the device is a display adapter, dot-matrix printer, or other raster device.</span></span> <span data-ttu-id="aaaff-125">Um aplicativo também pode usar a \_ máscara FontType do dispositivo para distinguir fontes de varredura fornecidas pela GDI das fontes fornecidas pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aaaff-125">An application can also use the DEVICE\_FONTTYPE mask to distinguish GDI-supplied raster fonts from device-supplied fonts.</span></span> <span data-ttu-id="aaaff-126">O sistema pode simular atributos em negrito, itálico, sublinhado e riscado para fontes de varredura fornecidas pela GDI, mas não para fontes fornecidas pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aaaff-126">The system can simulate bold, italic, underline, and strikeout attributes for GDI-supplied raster fonts, but not for device-supplied fonts.</span></span>

<span data-ttu-id="aaaff-127">Um aplicativo também pode verificar bits 1 e 2 no membro **tmPitchAndFamily** da estrutura [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) para identificar uma fonte TrueType.</span><span class="sxs-lookup"><span data-stu-id="aaaff-127">An application can also check bits 1 and 2 in the **tmPitchAndFamily** member of the [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure to identify a TrueType font.</span></span> <span data-ttu-id="aaaff-128">Se o bit 1 for 0 e o bit 2 for 1, a fonte será uma fonte TrueType.</span><span class="sxs-lookup"><span data-stu-id="aaaff-128">If bit 1 is 0 and bit 2 is 1, the font is a TrueType font.</span></span>

<span data-ttu-id="aaaff-129">As fontes de vetor são categorizadas como conjunto \_ de caracteres OEM em vez de \_ charset ANSI.</span><span class="sxs-lookup"><span data-stu-id="aaaff-129">Vector fonts are categorized as OEM\_CHARSET instead of ANSI\_CHARSET.</span></span> <span data-ttu-id="aaaff-130">Alguns aplicativos identificam fontes de vetor usando essas informações, verificando o membro **tmCharSet** da estrutura [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .</span><span class="sxs-lookup"><span data-stu-id="aaaff-130">Some applications identify vector fonts by using this information, checking the **tmCharSet** member of the [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure.</span></span> <span data-ttu-id="aaaff-131">Essa categorização geralmente impede que o mapeador de fontes escolha fontes vetoriais, a menos que elas sejam especificamente solicitadas.</span><span class="sxs-lookup"><span data-stu-id="aaaff-131">This categorization usually prevents the font mapper from choosing vector fonts unless they are specifically requested.</span></span> <span data-ttu-id="aaaff-132">(A maioria dos aplicativos não usa mais fontes vetoriais porque seus traços são linhas únicas e demoram mais para serem desenhados do que as fontes TrueType, que oferecem muitos dos mesmos recursos de dimensionamento e rotação que exigiam fontes vetoriais.)</span><span class="sxs-lookup"><span data-stu-id="aaaff-132">(Most applications no longer use vector fonts because their strokes are single lines and they take longer to draw than TrueType fonts, which offer many of the same scaling and rotation features that required vector fonts.)</span></span>

 

 
