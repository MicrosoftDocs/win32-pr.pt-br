---
description: Este tópico descreve como gravar texto em um OM XPS.
ms.assetid: 5552b7b0-1c95-43fa-ad06-c167c69c5a56
title: Gravar texto em um OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cca953d5281620cf7b7d9b7b07c133bee0d4de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170355"
---
# <a name="write-text-to-an-xps-om"></a><span data-ttu-id="32e3c-103">Gravar texto em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="32e3c-103">Write Text to an XPS OM</span></span>

<span data-ttu-id="32e3c-104">Este tópico descreve como gravar texto em um OM XPS.</span><span class="sxs-lookup"><span data-stu-id="32e3c-104">This topic describes how to write text to an XPS OM.</span></span>

<span data-ttu-id="32e3c-105">O texto é colocado em um OM XPS criando e Formatando uma interface [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) e, em seguida, adicionando a interface **IXpsOMGlyphs** à lista de objetos visuais da página ou da tela.</span><span class="sxs-lookup"><span data-stu-id="32e3c-105">Text is placed in an XPS OM by creating and formatting an [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) interface and then adding the **IXpsOMGlyphs** interface to the page's or canvas' list of visual objects.</span></span> <span data-ttu-id="32e3c-106">Cada interface **IXpsOMGlyphs** representa uma execução de glifo, que é uma execução contínua de caracteres que compartilham um formato comum.</span><span class="sxs-lookup"><span data-stu-id="32e3c-106">Each **IXpsOMGlyphs** interface represents a glyph run, which is a continuous run of characters that share a common format.</span></span> <span data-ttu-id="32e3c-107">Quando um elemento de formato de caractere (como o tipo ou tamanho da fonte) é alterado ou quando uma linha é interrompida, uma nova interface **IXpsOMGlyphs** deve ser criada e adicionada à lista de objetos visuais.</span><span class="sxs-lookup"><span data-stu-id="32e3c-107">When a character format element (such as font type or size) changes or when a line breaks, a new **IXpsOMGlyphs** interface must be created and added to the list of visual objects.</span></span>

<span data-ttu-id="32e3c-108">Algumas das propriedades de uma execução de glifo podem ser definidas usando os métodos da interface [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) .</span><span class="sxs-lookup"><span data-stu-id="32e3c-108">Some of the properties of a glyph run can be set by using the methods of the [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) interface.</span></span> <span data-ttu-id="32e3c-109">Algumas propriedades, no entanto, interagem com outras pessoas e devem ser definidas usando uma interface [**IXpsOMGlyphsEditor**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor) .</span><span class="sxs-lookup"><span data-stu-id="32e3c-109">Some properties, however, interact with others and must be set by using an [**IXpsOMGlyphsEditor**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor) interface.</span></span>

<span data-ttu-id="32e3c-110">Antes de usar os exemplos de código a seguir em seu programa, leia o aviso de isenção de responsabilidade em [tarefas comuns de programação de documentos XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="32e3c-110">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="32e3c-111">Exemplo de código</span><span class="sxs-lookup"><span data-stu-id="32e3c-111">Code Example</span></span>

### <a name="create-a-glyph-run-from-a-string"></a><span data-ttu-id="32e3c-112">Criar uma execução de glifo a partir de uma cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="32e3c-112">Create a glyph run from a string</span></span>

<span data-ttu-id="32e3c-113">Uma execução de glifo normalmente é criada em várias etapas que incluem o carregamento dos recursos de fonte usados pela execução de glifos, a definição de um pincel de preenchimento, a especificação do tamanho da fonte e do local inicial e a definição da cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="32e3c-113">A glyph run is commonly created in several steps that include loading the font resources that are used by the glyph run, setting a fill brush, specifying the font size and starting location, and setting the Unicode string.</span></span>

<span data-ttu-id="32e3c-114">A seção a seguir do exemplo de código contém uma rotina que aceita algumas variáveis, incluindo o tamanho da fonte, a cor e o local e os caracteres a serem gravados.</span><span class="sxs-lookup"><span data-stu-id="32e3c-114">The following section of the code example contains a routine that accepts some variables, including the font size, color and location, and the characters to be written.</span></span> <span data-ttu-id="32e3c-115">Em seguida, o código cria uma execução de glifo e, em seguida, adiciona-o a uma página.</span><span class="sxs-lookup"><span data-stu-id="32e3c-115">The code then creates a glyph run and then adds it to a page.</span></span> <span data-ttu-id="32e3c-116">O exemplo de código pressupõe que a inicialização descrita em [inicializar um om XPS](xps-object-model-initialization.md) ocorreu e que o documento tem pelo menos uma página.</span><span class="sxs-lookup"><span data-stu-id="32e3c-116">The code example assumes that the initialization described in [Initialize an XPS OM](xps-object-model-initialization.md) has occurred and that the document has at least one page.</span></span> <span data-ttu-id="32e3c-117">Para obter mais informações sobre como criar um OM XPS em branco, consulte [criar um om XPS em branco](create-a-blank-xps-om.md).</span><span class="sxs-lookup"><span data-stu-id="32e3c-117">For more information about creating a blank XPS OM, refer to [Create a Blank XPS OM](create-a-blank-xps-om.md).</span></span>


```C++
// Write Text to an XPS OM
HRESULT
WriteText_AddTextToPage(
            // A pre-created object factory
    __in    IXpsOMObjectFactory   *xpsFactory,
            // The font resource to use for this run
    __in    IXpsOMFontResource    *xpsFont,
            // The font size
    __in    float                 fontEmSize,
            // The solid color brush to use for the font
    __in    IXpsOMSolidColorBrush *xpsBrush,
            // The starting location of this glyph run
    __in    XPS_POINT             *origin,
            // The text to use for this run
    __in    LPCWSTR               unicodeString,
            // The page on which to write this glyph run
    __inout IXpsOMPage            *xpsPage        
)
{
    // The data type definitions are included in this function
    // for the convenience of this code example. In an actual
    // implementation they would probably belong in a header file.
    HRESULT                       hr = S_OK;
    XPS_POINT                     glyphsOrigin = {origin->x, origin->y};
    IXpsOMGlyphsEditor            *glyphsEditor = NULL;
    IXpsOMGlyphs                  *xpsGlyphs = NULL;
    IXpsOMVisualCollection        *pageVisuals = NULL;

    // Create a new Glyphs object and set its properties.
    hr = xpsFactory->CreateGlyphs(xpsFont, &xpsGlyphs);
    hr = xpsGlyphs->SetOrigin(&glyphsOrigin);
    hr = xpsGlyphs->SetFontRenderingEmSize(fontEmSize);
    hr = xpsGlyphs->SetFillBrushLocal(xpsBrush);

    // Some properties are inter-dependent so they
    //    must be changed by using a GlyphsEditor.
    hr = xpsGlyphs->GetGlyphsEditor(&glyphsEditor);
    hr = glyphsEditor->SetUnicodeString(unicodeString);
    hr = glyphsEditor->ApplyEdits();

    // Add the new Glyphs object to the page
    hr = xpsPage->GetVisuals(&pageVisuals);
    hr = pageVisuals->Append(xpsGlyphs);

    // Release interface pointers.
    if (NULL != xpsGlyphs) xpsGlyphs->Release();
    if (NULL != glyphsEditor) glyphsEditor->Release();
    if (NULL != pageVisuals) pageVisuals->Release();

    return hr;
}
```



### <a name="load-and-create-resources"></a><span data-ttu-id="32e3c-118">Carregar e criar recursos</span><span class="sxs-lookup"><span data-stu-id="32e3c-118">Load and create resources</span></span>

<span data-ttu-id="32e3c-119">A criação de uma interface [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) requer um recurso de fonte.</span><span class="sxs-lookup"><span data-stu-id="32e3c-119">Creation of an [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) interface requires a font resource.</span></span> <span data-ttu-id="32e3c-120">Em muitos casos, um bloco de texto usa a mesma fonte e cor.</span><span class="sxs-lookup"><span data-stu-id="32e3c-120">In many cases, a block of text uses the same font and color.</span></span> <span data-ttu-id="32e3c-121">Portanto, esta seção do exemplo de código criará as interfaces de recurso de fonte que serão usadas nas chamadas que colocam o texto na página.</span><span class="sxs-lookup"><span data-stu-id="32e3c-121">Hence, this section of the code example will create the font resource interfaces that will be used in the calls that place the text on the page.</span></span>


```C++
    // fontFileName is the name of the font file and it 
    //  is defined outside of this example.

    HRESULT                       hr = S_OK;

    GUID                          fontNameGuid;
    WCHAR                         guidString[128] = {0};
    WCHAR                         uriString[256] = {0};

    IStream                       *fontStream  = NULL;
    IOpcPartUri                   *fontUri = NULL;
    IXpsOMFontResource            *fontResource = NULL;
    IXpsOMVisualCollection        *pageVisuals = NULL;
    IXpsOMPage                    *page = NULL;
    IXpsOMVisual                  *canvasVisual = NULL;
    IXpsOMSolidColorBrush         *xpsTextColor = NULL;
    XPS_COLOR                     xpsColorBodyText;
 
    // Create font stream.
    hr = xpsFactory->CreateReadOnlyStreamOnFile ( 
        fontFileName, &fontStream );
    
    // Create new obfuscated part name for this resource using a GUID.
    hr = CoCreateGuid( &fontNameGuid );
    hr = StringFromGUID2( 
            fontNameGuid, 
            guidString, 
            ARRAYSIZE(guidString));

    // Create a URI string for this font resource that will place 
    //  the font part in the /Resources/Fonts folder of the package.
    wcscpy_s(uriString, ARRAYSIZE(uriString), L"/Resources/Fonts/");

    // Create the part name using the GUID string as the name and 
    //  ".odttf" as the extension GUID string start and ends with 
    //  curly braces so they are removed.
    wcsncat_s(uriString, ARRAYSIZE(uriString), 
        guidString + 1, wcslen(guidString) - 2); 
    wcscat_s(uriString, ARRAYSIZE(uriString), L".odttf");

    // Create the font URI interface.
    hr = xpsFactory->CreatePartUri(
        uriString,
        &fontUri);
    // Create the font resource.
    hr = xpsFactory->CreateFontResource(
        fontStream,
        XPS_FONT_EMBEDDING_OBFUSCATED,
        fontUri,
        FALSE,     // isObfSourceStream
        &fontResource);
    if (NULL != fontUri) fontUri->Release();

    // Create the brush to use for the font.
    xpsColorBodyText.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColorBodyText.value.sRGB.alpha = 0xFF;
    xpsColorBodyText.value.sRGB.red = 0x00;
    xpsColorBodyText.value.sRGB.green = 0x00;
    xpsColorBodyText.value.sRGB.blue = 0x00;

    hr = xpsFactory->CreateSolidColorBrush( 
        &xpsColorBodyText,
        NULL, // This color type does not use a color profile resource.             
        &xpsTextColor);

    // xpsTextColor is released after it has been used.
```



### <a name="draw-text-in-a-page"></a><span data-ttu-id="32e3c-122">Desenhar texto em uma página</span><span class="sxs-lookup"><span data-stu-id="32e3c-122">Draw text in a page</span></span>

<span data-ttu-id="32e3c-123">A seção final do exemplo de código cria as execuções de glifo para cada execução de texto formatado da mesma forma.</span><span class="sxs-lookup"><span data-stu-id="32e3c-123">The final section of the code example creates the glyph runs for each run of similarly formatted text.</span></span> <span data-ttu-id="32e3c-124">Para executar o código nesta seção final, a interface **xpsFactory** , bem como o recurso de fonte e um pincel de cor de texto, são necessários e devem ter sido instanciadas e inicializadas.</span><span class="sxs-lookup"><span data-stu-id="32e3c-124">To execute the code in this final section, the **xpsFactory** interface as well as the font resource and a text color brush are necessary and must have been instantiated and initialized.</span></span> <span data-ttu-id="32e3c-125">Neste exemplo, a função descrita na primeira seção é usada para criar as execuções de glifo e adicioná-las à página.</span><span class="sxs-lookup"><span data-stu-id="32e3c-125">In this example, the function described in the first section is used to create the glyph runs and to add them to the page.</span></span>


```C++
    // The following interfaces are created outside of this example.

    // The page on which to place the text.
    IXpsOMPage                *page = NULL;

    // The object factory used by this program.
    IXpsOMObjectFactory       *xpsFactory = NULL;

    // The font resource created in the previous snippet.
    IXpsOMFontResource        *fontResource = NULL;

    // The color brush created in the previous snippet.
    IXpsOMSolidColorBrush     *xpsTextColor = NULL;

    // The following variables are defined outside of this example.

    // An array of pointers to the Unicode strings to write.
    LPCWSTR                   *textRuns = NULL;

    // An array of start points that correspond to the 
    //    strings in textRuns.
    XPS_POINT                 *startPoints = NULL;

    // The number of text runs to add to the page.
    UINT32                    numRuns = 0;            

    HRESULT                   hr = S_OK;

    FLOAT                     fontSize = 7.56f;
    UINT32                    thisRun;

    // Add all the text runs to the page.
    thisRun = 0;
    while (thisRun < numRuns) {  
        hr = WriteText_AddTextToPage(
            xpsFactory, 
            fontResource,
            fontSize,
            xpsTextColor,
            &startPoints[thisRun],
            textRuns[thisRun],
            page);
        thisRun++;
    }
```



## <a name="related-topics"></a><span data-ttu-id="32e3c-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32e3c-126">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="32e3c-127">**Próximas etapas**</span><span class="sxs-lookup"><span data-stu-id="32e3c-127">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="32e3c-128">Navegar no OM XPS</span><span class="sxs-lookup"><span data-stu-id="32e3c-128">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="32e3c-129">Desenhar gráficos em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="32e3c-129">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="32e3c-130">Coloque as imagens em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="32e3c-130">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="32e3c-131">Gravar um OM XPS em um documento XPS</span><span class="sxs-lookup"><span data-stu-id="32e3c-131">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[<span data-ttu-id="32e3c-132">Imprimir um OM XPS</span><span class="sxs-lookup"><span data-stu-id="32e3c-132">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="32e3c-133">**Usado nesta seção**</span><span class="sxs-lookup"><span data-stu-id="32e3c-133">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="32e3c-134">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="32e3c-134">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="32e3c-135">**IXpsOMFontResource**</span><span class="sxs-lookup"><span data-stu-id="32e3c-135">**IXpsOMFontResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)
</dt> <dt>

[<span data-ttu-id="32e3c-136">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="32e3c-136">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)
</dt> <dt>

[<span data-ttu-id="32e3c-137">**IXpsOMGlyphsEditor**</span><span class="sxs-lookup"><span data-stu-id="32e3c-137">**IXpsOMGlyphsEditor**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor)
</dt> <dt>

[<span data-ttu-id="32e3c-138">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="32e3c-138">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="32e3c-139">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="32e3c-139">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="32e3c-140">**IXpsOMSolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="32e3c-140">**IXpsOMSolidColorBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[<span data-ttu-id="32e3c-141">**IXpsOMVisual**</span><span class="sxs-lookup"><span data-stu-id="32e3c-141">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)
</dt> <dt>

[<span data-ttu-id="32e3c-142">**IXpsOMVisualCollection**</span><span class="sxs-lookup"><span data-stu-id="32e3c-142">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

<span data-ttu-id="32e3c-143">**Para obter mais informações**</span><span class="sxs-lookup"><span data-stu-id="32e3c-143">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="32e3c-144">Inicializar um OM XPS</span><span class="sxs-lookup"><span data-stu-id="32e3c-144">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="32e3c-145">Referência da API do documento XPS</span><span class="sxs-lookup"><span data-stu-id="32e3c-145">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="32e3c-146">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="32e3c-146">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
