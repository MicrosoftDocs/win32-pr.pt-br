---
title: Interoperação com GDI
description: O DirectWrite fornece um caminho de migração do e de alguma interoperabilidade com o modelo de fonte da GDI, bem como interfaces para renderização de texto em um bitmap que pode ser desenhado em uma janela.
ms.assetid: fb73e07b-60fb-4726-bd5b-c14d61ace186
keywords:
- Interoperação DirectWrite, GDI
- DirectWrite, interoperabilidade
- interoperabilidade
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41c7c99e6bfac0aabddd4a1568b64cd425ccb25b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007590"
---
# <a name="interoperating-with-gdi"></a><span data-ttu-id="ddad7-108">Interoperação com GDI</span><span class="sxs-lookup"><span data-stu-id="ddad7-108">Interoperating with GDI</span></span>

<span data-ttu-id="ddad7-109">O [DirectWrite](direct-write-portal.md) fornece um caminho de migração do e de alguma interoperabilidade com o modelo de fonte da GDI, bem como interfaces para renderização de texto em um bitmap que pode ser desenhado em uma janela.</span><span class="sxs-lookup"><span data-stu-id="ddad7-109">[DirectWrite](direct-write-portal.md) provides a migration path from, and some interoperability with, GDI's font model, as well as interfaces for rendering text to a bitmap that can then be drawn on a window.</span></span>

<span data-ttu-id="ddad7-110">Esta visão geral contém as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="ddad7-110">This overview contains the following parts:</span></span>

-   [<span data-ttu-id="ddad7-111">Introdução</span><span class="sxs-lookup"><span data-stu-id="ddad7-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="ddad7-112">Parte 1: IDWriteGdiInterop</span><span class="sxs-lookup"><span data-stu-id="ddad7-112">Part 1: IDWriteGdiInterop</span></span>](#part-1-idwritegdiinterop)
-   [<span data-ttu-id="ddad7-113">Parte 2: objetos Font</span><span class="sxs-lookup"><span data-stu-id="ddad7-113">Part 2: Font Objects</span></span>](#part-2-font-objects)
-   [<span data-ttu-id="ddad7-114">Parte 3: renderizando</span><span class="sxs-lookup"><span data-stu-id="ddad7-114">Part 3: Rendering</span></span>](#part-3-rendering)

## <a name="introduction"></a><span data-ttu-id="ddad7-115">Introdução</span><span class="sxs-lookup"><span data-stu-id="ddad7-115">Introduction</span></span>

<span data-ttu-id="ddad7-116">O [DirectWrite](direct-write-portal.md) fornece métodos para converter entre a estrutura LOGFONT do GDI e as interfaces de fonte DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="ddad7-116">[DirectWrite](direct-write-portal.md) provides methods for converting between GDI's LOGFONT structure and DirectWrite font interfaces.</span></span> <span data-ttu-id="ddad7-117">Isso permite que você use GDI para algumas ou toda a enumeração e seleção de fontes, aproveitando a funcionalidade e o desempenho aprimorados do DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="ddad7-117">This allows you to use GDI for some or all of the font enumeration and selection, while taking advantage of the improved functionality and performance of DirectWrite.</span></span> <span data-ttu-id="ddad7-118">DirectWrite também tem interfaces para renderização em um bitmap se você quiser exibir texto em uma superfície GDI.</span><span class="sxs-lookup"><span data-stu-id="ddad7-118">DirectWrite also has interfaces for rendering to a bitmap if you want to display text on a GDI surface.</span></span>

## <a name="part-1-idwritegdiinterop"></a><span data-ttu-id="ddad7-119">Parte 1: IDWriteGdiInterop</span><span class="sxs-lookup"><span data-stu-id="ddad7-119">Part 1: IDWriteGdiInterop</span></span>

<span data-ttu-id="ddad7-120">A interface [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) é usada para converter entre as estruturas de fonte GDI e as interfaces de fonte [DirectWrite](direct-write-portal.md) e também para criar um objeto [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) .</span><span class="sxs-lookup"><span data-stu-id="ddad7-120">The [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) interface is used to convert between GDI font structures and [DirectWrite](direct-write-portal.md) font interfaces, and also to create an [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object.</span></span> <span data-ttu-id="ddad7-121">Obtenha um objeto **IDWriteGdiInterop** usando o método [**IDWriteFactory:: GetGdiInterop**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop) , conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="ddad7-121">Get an **IDWriteGdiInterop** object by using the [**IDWriteFactory::GetGdiInterop**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop) method, as shown in the following code.</span></span>


```C++
// Create a GDI interop interface.
if (SUCCEEDED(hr))
{
    hr = g_pDWriteFactory->GetGdiInterop(&g_pGdiInterop);
}
```



## <a name="part-2-font-objects"></a><span data-ttu-id="ddad7-122">Parte 2: objetos Font</span><span class="sxs-lookup"><span data-stu-id="ddad7-122">Part 2: Font Objects</span></span>

<span data-ttu-id="ddad7-123">O GDI usa a estrutura LOGFONT para armazenar informações sobre a fonte e o estilo de texto.</span><span class="sxs-lookup"><span data-stu-id="ddad7-123">GDI uses the LOGFONT structure to store information about the font and style of text.</span></span> <span data-ttu-id="ddad7-124">O método [**IDWriteGdiInterop:: CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont) converterá uma estrutura LOGFONT em um objeto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) , como visto no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="ddad7-124">The [**IDWriteGdiInterop::CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont) method will convert a LOGFONT structure to an [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object, as seen in the following code.</span></span>


```C++
// Convert to a DirectWrite font.
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateFontFromLOGFONT(&lf, &pFont);
}
```



<span data-ttu-id="ddad7-125">No entanto, o [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) não encapsula todas as mesmas informações que um LOGFONT.</span><span class="sxs-lookup"><span data-stu-id="ddad7-125">However, [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) does not encapsulate all of the same information that a LOGFONT does.</span></span> <span data-ttu-id="ddad7-126">Uma estrutura LOGFONT contém o tamanho da fonte, o peso, o estilo, o sublinhado, o riscado, o nome da face da fonte e outras informações.</span><span class="sxs-lookup"><span data-stu-id="ddad7-126">A LOGFONT structure contains the font size, weight, style, underline, strikeout, font face name, and some other information.</span></span> <span data-ttu-id="ddad7-127">Os objetos **IDWriteFont** contêm informações sobre uma fonte e seu peso e estilo, mas não o tamanho da fonte, sublinhado e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="ddad7-127">**IDWriteFont** objects contain information about a font and its weight and style, but not the font size, underline, and so on.</span></span> <span data-ttu-id="ddad7-128">Com o [DirectWrite](direct-write-portal.md), elementos de informações de formatação como esses são encapsulados por um objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) ou, para intervalos de texto específicos, um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="ddad7-128">With [DirectWrite](direct-write-portal.md), formatting information elements such as these are encapsulated by an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object or, for specific ranges of text, an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="ddad7-129">Você tem a opção de converter um [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) em um LOGFONT usando o [**IDWriteGdiInterop:: ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont).</span><span class="sxs-lookup"><span data-stu-id="ddad7-129">You do have the option to convert a [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) to a LOGFONT by using the [**IDWriteGdiInterop::ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont).</span></span>

## <a name="part-3-rendering"></a><span data-ttu-id="ddad7-130">Parte 3: renderizando</span><span class="sxs-lookup"><span data-stu-id="ddad7-130">Part 3: Rendering</span></span>

<span data-ttu-id="ddad7-131">Para renderizar o texto DirectWrite em uma superfície GDI, use um processador de texto personalizado.</span><span class="sxs-lookup"><span data-stu-id="ddad7-131">To render DirectWrite text to a GDI surface you use a custom text renderer.</span></span> <span data-ttu-id="ddad7-132">Consulte o tópico [renderizar em uma superfície GDI](render-to-a-gdi-surface.md) .</span><span class="sxs-lookup"><span data-stu-id="ddad7-132">See the [Render to a GDI Surface](render-to-a-gdi-surface.md) topic.</span></span>

 

 