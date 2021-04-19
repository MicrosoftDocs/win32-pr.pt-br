---
title: Layout e formatação de texto
description: O DirectWrite fornece duas interfaces para formatar o texto IDWriteTextFormat e IDWriteTextLayout.
ms.assetid: a68963a6-e486-4881-8ad6-873173396fca
keywords:
- DirectWrite, formatação de texto
- DirectWrite, layout
- DirectWrite, interface IDWriteTextFormat
- DirectWrite, interface IDWriteTextLayout
- Interface IDWriteTextFormat
- Interface IDWriteTextLayout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e5790742a3d3caf7f962a6b5e2b3111c626f28
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380750"
---
# <a name="text-formatting-and-layout"></a><span data-ttu-id="82a37-109">Layout e formatação de texto</span><span class="sxs-lookup"><span data-stu-id="82a37-109">Text Formatting and Layout</span></span>

<span data-ttu-id="82a37-110">O [DirectWrite](direct-write-portal.md) fornece duas interfaces para formatar texto: [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span><span class="sxs-lookup"><span data-stu-id="82a37-110">[DirectWrite](direct-write-portal.md) provides two interfaces for formatting text: [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span></span> <span data-ttu-id="82a37-111">**IDWriteTextFormat** descreve apenas o formato de texto e é usado em casos em que uma cadeia de caracteres inteira deve ter o mesmo tamanho de fonte, estilo, peso e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="82a37-111">**IDWriteTextFormat** describes only the format for text and is used in cases when an entire string is to be the same font size, style, weight and so on.</span></span> <span data-ttu-id="82a37-112">Por outro lado, **IDWriteTextLayout** encapsula uma cadeia de caracteres de texto e a formatação para os intervalos especificados da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="82a37-112">On the other hand, **IDWriteTextLayout** encapsulates both a text string and the formatting for specified ranges of the string.</span></span> <span data-ttu-id="82a37-113">Este documento descreve cada interface e seus usos.</span><span class="sxs-lookup"><span data-stu-id="82a37-113">This document describes each interface and their uses.</span></span> <span data-ttu-id="82a37-114">Para obter mais informações sobre a criação e os métodos dessas interfaces, consulte as páginas de referência do [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e do [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="82a37-114">For more information about the creation and methods of these interfaces, see the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) reference pages.</span></span>

<span data-ttu-id="82a37-115">Este documento contém as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="82a37-115">This document contains the following parts:</span></span>

-   [<span data-ttu-id="82a37-116">IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="82a37-116">IDWriteTextFormat</span></span>](#modifying-an-idwritetextformat)
    -   [<span data-ttu-id="82a37-117">Modificando um IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="82a37-117">Modifying an IDWriteTextFormat</span></span>](#modifying-an-idwritetextformat)
-   [<span data-ttu-id="82a37-118">IDWriteTextLayout</span><span class="sxs-lookup"><span data-stu-id="82a37-118">IDWriteTextLayout</span></span>](#idwritetextlayout)
    -   [<span data-ttu-id="82a37-119">Formatando um intervalo de texto</span><span class="sxs-lookup"><span data-stu-id="82a37-119">Formatting a range of text</span></span>](#formatting-a-range-of-text)
    -   [<span data-ttu-id="82a37-120">Opções de renderização</span><span class="sxs-lookup"><span data-stu-id="82a37-120">Rendering Options</span></span>](#rendering-options)

## <a name="idwritetextformat"></a><span data-ttu-id="82a37-121">IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="82a37-121">IDWriteTextFormat</span></span>

<span data-ttu-id="82a37-122">Um objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) é usado para:</span><span class="sxs-lookup"><span data-stu-id="82a37-122">An [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object is used to:</span></span>

-   <span data-ttu-id="82a37-123">Descreva o formato de uma cadeia de caracteres inteira ao renderizar.</span><span class="sxs-lookup"><span data-stu-id="82a37-123">Describe the format for an entire string when rendering.</span></span> <span data-ttu-id="82a37-124">Para renderizar uma cadeia de caracteres com vários formatos, use um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="82a37-124">To render a string with multiple formats, use an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>
-   <span data-ttu-id="82a37-125">Especifique o formato de texto padrão ao criar um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="82a37-125">Specify the default text format when creating an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="82a37-126">Para criar um objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , use o método [**IDWriteFactory:: CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) e especifique a família de fontes, a coleção de fontes, a espessura da fonte, o tamanho da fonte (em DIPs) e o nome da localidade.</span><span class="sxs-lookup"><span data-stu-id="82a37-126">To create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object, you use the [**IDWriteFactory::CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) method and specify the font family, font collection, font weight, font size (in DIPs), locale name.</span></span>

### <a name="modifying-an-idwritetextformat"></a><span data-ttu-id="82a37-127">Modificando um IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="82a37-127">Modifying an IDWriteTextFormat</span></span>

<span data-ttu-id="82a37-128">Depois que uma interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) é criada, alguns valores não podem ser alterados: a família de fontes, a coleção, o peso e o tamanho, bem como o nome da localidade.</span><span class="sxs-lookup"><span data-stu-id="82a37-128">Once an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface is created, some values cannot be changed: the font family, collection, weight, and size, as well the locale name.</span></span> <span data-ttu-id="82a37-129">Para alterar esses valores, um novo objeto **IDWriteTextFormat** deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="82a37-129">To change these values, a new **IDWriteTextFormat** object must be created.</span></span>

<span data-ttu-id="82a37-130">O [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) permite que você altere as propriedades acima sem recriar nada.</span><span class="sxs-lookup"><span data-stu-id="82a37-130">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) enables you to change the properties above without recreating anything.</span></span> <span data-ttu-id="82a37-131">O [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) permite que você faça alterações de formato que se apliquem ao texto inteiro, como alinhamento de texto.</span><span class="sxs-lookup"><span data-stu-id="82a37-131">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) enables you to make format changes that apply to the entire text, such as text alignment.</span></span> <span data-ttu-id="82a37-132">Se você quiser aplicar formatação a intervalos de caracteres específicos, faça isso usando um **IDWriteTextLayout**.</span><span class="sxs-lookup"><span data-stu-id="82a37-132">If you want to apply formatting to specific character ranges, you should do so by using a **IDWriteTextLayout**.</span></span>

<span data-ttu-id="82a37-133">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) fornece métodos para definir o alinhamento de texto, direção de fluxo, parada de tabulação incremental, espaçamento de linha, alinhamento de parágrafo, corte e quebra automática de texto.</span><span class="sxs-lookup"><span data-stu-id="82a37-133">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) provides methods to set the text alignment, flow direction, incremental tab stop, line spacing, paragraph alignment, trimming, and word wrapping.</span></span> <span data-ttu-id="82a37-134">Essas propriedades podem ser alteradas a qualquer momento após a criação do objeto **IDWriteTextFormat** .</span><span class="sxs-lookup"><span data-stu-id="82a37-134">These properties can be changed at any time after the creation of the **IDWriteTextFormat** object.</span></span>

## <a name="idwritetextlayout"></a><span data-ttu-id="82a37-135">IDWriteTextLayout</span><span class="sxs-lookup"><span data-stu-id="82a37-135">IDWriteTextLayout</span></span>

<span data-ttu-id="82a37-136">A interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , ao contrário de [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), representa um bloco de texto e a formatação associada.</span><span class="sxs-lookup"><span data-stu-id="82a37-136">The [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface, unlike [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), represents both a block of text and the associated formatting.</span></span> <span data-ttu-id="82a37-137">**IDWriteTextFormat** representa informações de formatação inicial.</span><span class="sxs-lookup"><span data-stu-id="82a37-137">**IDWriteTextFormat** represents initial formatting information.</span></span> <span data-ttu-id="82a37-138">O exemplo a seguir mostra como criar um objeto **IDWriteTextLayout** usando [**IDWriteFactory:: CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout).</span><span class="sxs-lookup"><span data-stu-id="82a37-138">The following example shows how to create an **IDWriteTextLayout** object using [**IDWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout).</span></span>


```C++
// Create a text layout using the text format.
if (SUCCEEDED(hr))
{
    RECT rect;
    GetClientRect(hwnd_, &rect); 
    float width  = rect.right  / dpiScaleX_;
    float height = rect.bottom / dpiScaleY_;

    hr = pDWriteFactory_->CreateTextLayout(
        wszText_,      // The string to be laid out and formatted.
        cTextLength_,  // The length of the string.
        pTextFormat_,  // The text format to apply to the string (contains font information, etc).
        width,         // The width of the layout box.
        height,        // The height of the layout box.
        &pTextLayout_  // The IDWriteTextLayout interface pointer.
        );
}

```



<span data-ttu-id="82a37-139">O texto em um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) não pode ser alterado depois que o objeto é criado.</span><span class="sxs-lookup"><span data-stu-id="82a37-139">The text in an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object cannot be changed once the object is created.</span></span> <span data-ttu-id="82a37-140">Para alterar o texto, você deve excluir o objeto existente e criar um novo objeto **IDWriteTextLayout** .</span><span class="sxs-lookup"><span data-stu-id="82a37-140">To change the text you must delete the existing object and create a new **IDWriteTextLayout** object.</span></span>

<span data-ttu-id="82a37-141">Você pode usar um [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) para formatar os intervalos de texto especificados.</span><span class="sxs-lookup"><span data-stu-id="82a37-141">You can use an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) to format specified ranges of text.</span></span> <span data-ttu-id="82a37-142">O **IDWriteTextLayout** também fornece métodos para alterar o estilo e o peso da fonte e adicionar recursos de fonte OpenType e teste de clique.</span><span class="sxs-lookup"><span data-stu-id="82a37-142">**IDWriteTextLayout** also provides methods for changing font style and weight, and adding OpenType font features and hit testing.</span></span> <span data-ttu-id="82a37-143">Para obter mais informações e uma lista completa de métodos, consulte a página de referência do [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="82a37-143">For more information and a complete list of methods see the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) reference page.</span></span>

### <a name="formatting-a-range-of-text"></a><span data-ttu-id="82a37-144">Formatando um intervalo de texto</span><span class="sxs-lookup"><span data-stu-id="82a37-144">Formatting a range of text</span></span>

<span data-ttu-id="82a37-145">O [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) fornece vários métodos para formatar intervalos de texto.</span><span class="sxs-lookup"><span data-stu-id="82a37-145">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) provides several methods to format ranges of text.</span></span> <span data-ttu-id="82a37-146">Cada um desses métodos usa uma estrutura de [**\_ \_ intervalo de texto DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) como um parâmetro para especificar a posição do texto inicial dentro da cadeia de caracteres e o comprimento do intervalo a ser formatado.</span><span class="sxs-lookup"><span data-stu-id="82a37-146">Each of these methods takes a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) structure as a parameter to specify the starting text position within the string and the length of the range to format.</span></span> <span data-ttu-id="82a37-147">O exemplo a seguir mostra como definir a espessura da fonte de um intervalo de texto para negrito.</span><span class="sxs-lookup"><span data-stu-id="82a37-147">The following example shows how to set the font weight of a range of text to bold.</span></span>


```C++
// Set the font weight to bold for the first 5 letters.
DWRITE_TEXT_RANGE textRange = {0, 5};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}

```



### <a name="rendering-options"></a><span data-ttu-id="82a37-148">Opções de renderização</span><span class="sxs-lookup"><span data-stu-id="82a37-148">Rendering Options</span></span>

<span data-ttu-id="82a37-149">O texto com formatação descrita por apenas um objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) pode ser renderizado com [Direct2D](../direct2d/direct2d-portal.md), no entanto, há mais algumas opções para renderizar um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="82a37-149">Text with formatting described by only a [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object can be rendered with [Direct2D](../direct2d/direct2d-portal.md), however, there are a few more options for rendering an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="82a37-150">A cadeia de caracteres descrita por um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) pode ser renderizada usando os métodos abaixo.</span><span class="sxs-lookup"><span data-stu-id="82a37-150">The string described by an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object can be rendered using the methods below.</span></span>

1.  <span data-ttu-id="82a37-151">[Renderizar usando Direct2D](rendering-by-using-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="82a37-151">[Render using Direct2D](rendering-by-using-direct2d.md).</span></span>
2.  <span data-ttu-id="82a37-152">[Renderizar usando um processador de texto personalizado](how-to-implement-a-custom-text-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="82a37-152">[Render using a custom text renderer](how-to-implement-a-custom-text-renderer.md).</span></span>
3.  <span data-ttu-id="82a37-153">[Renderizar para uma superfície GDI](render-to-a-gdi-surface.md).</span><span class="sxs-lookup"><span data-stu-id="82a37-153">[Render to a GDI surface](render-to-a-gdi-surface.md).</span></span>

 

 
