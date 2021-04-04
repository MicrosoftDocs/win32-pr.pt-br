---
title: Como adicionar efeitos de desenho de cliente a um layout de texto
description: Fornece um breve tutorial sobre como adicionar efeitos de desenho de cliente a um aplicativo DirectWrite que exibe texto usando a interface IDWriteTextLayout e um processador de texto personalizado.
ms.assetid: b66ff814-2113-48b0-8913-3d30a5d20077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338dc1a720bde80c1daf2b4baf7c7a4bad6d2cff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007803"
---
# <a name="how-to-add-client-drawing-effects-to-a-text-layout"></a><span data-ttu-id="6f56e-103">Como adicionar efeitos de desenho de cliente a um layout de texto</span><span class="sxs-lookup"><span data-stu-id="6f56e-103">How to Add Client Drawing Effects to a Text Layout</span></span>

<span data-ttu-id="6f56e-104">Fornece um breve tutorial sobre como adicionar efeitos de desenho de cliente a um aplicativo [DirectWrite](direct-write-portal.md) que exibe texto usando a interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) e um processador de texto personalizado.</span><span class="sxs-lookup"><span data-stu-id="6f56e-104">Provides a short tutorial on adding client drawing effects to a [DirectWrite](direct-write-portal.md) application that displays text using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface and a custom text renderer.</span></span>

<span data-ttu-id="6f56e-105">O produto final deste tutorial é um aplicativo que exibe um texto com intervalos de texto com um efeito de desenho de cor diferente em cada um, conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6f56e-105">The end product of this tutorial is an application that displays text that has ranges of text with a different color drawing effect on each, as shown in the following screen shot.</span></span>

![captura de tela do "exemplo de efeito de desenho de cliente!"](images/drawingeffects.png)

> [!Note]  
> <span data-ttu-id="6f56e-108">Este tutorial deve ser um exemplo simplificado de como criar efeitos de desenho de cliente personalizados, não um exemplo de um método simples para desenhar texto colorido.</span><span class="sxs-lookup"><span data-stu-id="6f56e-108">This tutorial is meant to be a simplified example of how to create custom client drawing effects, not an example of a simple method for drawing color text.</span></span> <span data-ttu-id="6f56e-109">Consulte a página de referência [**IDWriteTextLayout:: SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6f56e-109">See the [**IDWriteTextLayout::SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) reference page for more information.</span></span>

 

<span data-ttu-id="6f56e-110">Este tutorial contém as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="6f56e-110">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="6f56e-111">Etapa 1: criar um layout de texto</span><span class="sxs-lookup"><span data-stu-id="6f56e-111">Step 1: Create a Text Layout</span></span>](#step-1-create-a-text-layout)
-   [<span data-ttu-id="6f56e-112">Etapa 2: implementar uma classe de efeito de desenho personalizado</span><span class="sxs-lookup"><span data-stu-id="6f56e-112">Step 2: Implement a Custom Drawing Effect Class</span></span>](#step-2-implement-a-custom-drawing-effect-class)
-   [<span data-ttu-id="6f56e-113">Etapa 3: implementar uma classe de processador de texto personalizado</span><span class="sxs-lookup"><span data-stu-id="6f56e-113">Step 3: Implement a Custom Text Renderer Class</span></span>](#step-3-implement-a-custom-text-renderer-class)
    -   [<span data-ttu-id="6f56e-114">O Construtor</span><span class="sxs-lookup"><span data-stu-id="6f56e-114">The Constructor</span></span>](#the-constructor)
    -   [<span data-ttu-id="6f56e-115">O método DrawGlyphRun</span><span class="sxs-lookup"><span data-stu-id="6f56e-115">The DrawGlyphRun Method</span></span>](#the-drawglyphrun-method)
    -   [<span data-ttu-id="6f56e-116">O destruidor</span><span class="sxs-lookup"><span data-stu-id="6f56e-116">The Destructor</span></span>](#the-destructor)
-   [<span data-ttu-id="6f56e-117">Etapa 4: criar o processador de texto</span><span class="sxs-lookup"><span data-stu-id="6f56e-117">Step 4: Create the Text Renderer</span></span>](#step-4-create-the-text-renderer)
-   [<span data-ttu-id="6f56e-118">Etapa 5: instanciar os objetos de efeito de desenho de cor</span><span class="sxs-lookup"><span data-stu-id="6f56e-118">Step 5: Instantiate the Color Drawing Effect Objects</span></span>](#step-5-instantiate-the-color-drawing-effect-objects)
-   [<span data-ttu-id="6f56e-119">Etapa 6: definir o efeito de desenho para intervalos de texto específicos</span><span class="sxs-lookup"><span data-stu-id="6f56e-119">Step 6: Set the Drawing Effect for Specific Text Ranges</span></span>](#step-6-set-the-drawing-effect-for-specific-text-ranges)
-   [<span data-ttu-id="6f56e-120">Etapa 7: desenhar o layout de texto usando o renderizador personalizado</span><span class="sxs-lookup"><span data-stu-id="6f56e-120">Step 7: Draw the Text Layout Using the Custom Renderer</span></span>](#step-7-draw-the-text-layout-using-the-custom-renderer)
-   [<span data-ttu-id="6f56e-121">Etapa 8: limpar</span><span class="sxs-lookup"><span data-stu-id="6f56e-121">Step 8: Clean up</span></span>](#step-8-clean-up)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="6f56e-122">Etapa 1: criar um layout de texto</span><span class="sxs-lookup"><span data-stu-id="6f56e-122">Step 1: Create a Text Layout</span></span>

<span data-ttu-id="6f56e-123">Para começar, você precisará de um aplicativo com um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="6f56e-123">To begin, you will need an application with an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="6f56e-124">Se você já tiver um aplicativo que exibe texto com um layout de texto, ou se estiver usando o código de exemplo DrawingEffect personalizado, pule para a etapa 2.</span><span class="sxs-lookup"><span data-stu-id="6f56e-124">If you already have an application that displays text with a text layout, or you are using the Custom DrawingEffect Example Code, skip to Step 2.</span></span>

<span data-ttu-id="6f56e-125">Para adicionar um layout de texto, você deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6f56e-125">To add a text layout you must do the following:</span></span>

1.  <span data-ttu-id="6f56e-126">Declare um ponteiro para uma interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) como um membro da classe.</span><span class="sxs-lookup"><span data-stu-id="6f56e-126">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="6f56e-127">No final do método **CreateDeviceIndependentResources** , crie um objeto de interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chamando o método [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="6f56e-127">At the end of the **CreateDeviceIndependentResources** method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>
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

    

3.  <span data-ttu-id="6f56e-128">Por fim, lembre-se de liberar o layout de texto no destruidor.</span><span class="sxs-lookup"><span data-stu-id="6f56e-128">Finally, remember to release the text layout in the destructor.</span></span>
    ```C++
    SafeRelease(&pTextLayout_);
    ```

    

## <a name="step-2-implement-a-custom-drawing-effect-class"></a><span data-ttu-id="6f56e-129">Etapa 2: implementar uma classe de efeito de desenho personalizado</span><span class="sxs-lookup"><span data-stu-id="6f56e-129">Step 2: Implement a Custom Drawing Effect Class</span></span>

<span data-ttu-id="6f56e-130">Além dos métodos herdados de IUnknown, uma interface de efeito de desenho de cliente personalizada não tem requisitos sobre o que deve ser implementado.</span><span class="sxs-lookup"><span data-stu-id="6f56e-130">Other than the methods inherited from IUnknown, a custom client drawing effect interface has no requirements as to what it must implement.</span></span> <span data-ttu-id="6f56e-131">Nesse caso, a classe **ColorDrawingEffect** simplesmente mantém um valor [**\_ \_ F de cor de d2d1**](../direct2d/d2d1-color-f.md) e declara métodos para obter e definir esse valor, bem como um construtor que pode definir a cor inicialmente.</span><span class="sxs-lookup"><span data-stu-id="6f56e-131">In this case, the **ColorDrawingEffect** class simply holds a [**D2D1\_COLOR\_F**](../direct2d/d2d1-color-f.md) value and declares methods to get and set this value, as well as a constructor that can set the color initially.</span></span>

<span data-ttu-id="6f56e-132">Depois que um efeito de desenho de cliente é aplicado a um intervalo de texto em um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , o efeito de desenho é passado para o método [**IDWriteTextRenderer::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) de qualquer execução de glifo que deve ser renderizada.</span><span class="sxs-lookup"><span data-stu-id="6f56e-132">After a client drawing effect is applied to a text range in a [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, the drawing effect is passed to the [**IDWriteTextRenderer::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method of any glyph run that is to be rendered.</span></span> <span data-ttu-id="6f56e-133">Os métodos do efeito de desenho ficam disponíveis para o processador de texto.</span><span class="sxs-lookup"><span data-stu-id="6f56e-133">The methods of the drawing effect are then available to the text renderer.</span></span>

<span data-ttu-id="6f56e-134">Um efeito de desenho de cliente pode ser tão complexo quanto você deseja fazê-lo, com mais informações do que neste exemplo, além de fornecer métodos para alterar glifos, criar objetos a serem usados para desenhar e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6f56e-134">A client drawing effect can be as complex as you want to make it, carrying more information than in this example, as well as providing methods to alter glyphs, create objects to be used for drawing, and so on.</span></span>

## <a name="step-3-implement-a-custom-text-renderer-class"></a><span data-ttu-id="6f56e-135">Etapa 3: implementar uma classe de processador de texto personalizado</span><span class="sxs-lookup"><span data-stu-id="6f56e-135">Step 3: Implement a Custom Text Renderer Class</span></span>

<span data-ttu-id="6f56e-136">Para tirar proveito de um efeito de desenho de cliente, você deve implementar um processador de texto personalizado.</span><span class="sxs-lookup"><span data-stu-id="6f56e-136">In order to take advantage of a client drawing effect, you must implement a custom text renderer.</span></span> <span data-ttu-id="6f56e-137">Esse processador de texto aplicará o efeito de desenho passado para ele pelo método [**bruto IDWriteTextLayout::D**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) para a execução de glifo que está sendo desenhada.</span><span class="sxs-lookup"><span data-stu-id="6f56e-137">This text renderer will apply the drawing effect passed to it by the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method to the glyph run being drawn.</span></span>

### <a name="the-constructor"></a><span data-ttu-id="6f56e-138">O Construtor</span><span class="sxs-lookup"><span data-stu-id="6f56e-138">The Constructor</span></span>

<span data-ttu-id="6f56e-139">O construtor do renderizador de texto personalizado armazena o objeto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) que será usado para criar objetos [Direct2D](../direct2d/direct2d-portal.md) e o destino de renderização Direct2D no qual o texto será desenhado.</span><span class="sxs-lookup"><span data-stu-id="6f56e-139">The constructor for the custom text renderer stores the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object that will be used to create [Direct2D](../direct2d/direct2d-portal.md) objects, and the Direct2D render target that the text will be drawn on to.</span></span>


```C++
CustomTextRenderer::CustomTextRenderer(
    ID2D1Factory* pD2DFactory, 
    ID2D1HwndRenderTarget* pRT
    )
:
cRefCount_(0), 
pD2DFactory_(pD2DFactory), 
pRT_(pRT)
{
    pD2DFactory_->AddRef();
    pRT_->AddRef();
}
```



### <a name="the-drawglyphrun-method"></a><span data-ttu-id="6f56e-140">O método DrawGlyphRun</span><span class="sxs-lookup"><span data-stu-id="6f56e-140">The DrawGlyphRun Method</span></span>

<span data-ttu-id="6f56e-141">Uma execução de glifo é um conjunto de glifos que compartilham o mesmo formato, incluindo o efeito de desenho do cliente.</span><span class="sxs-lookup"><span data-stu-id="6f56e-141">A glyph run is a set of glyphs that share the same format, including the client drawing effect.</span></span> <span data-ttu-id="6f56e-142">O método [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) cuida da renderização de texto para uma execução de glifo especificada.</span><span class="sxs-lookup"><span data-stu-id="6f56e-142">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method takes care of the text rendering for a specified glyph run.</span></span>

<span data-ttu-id="6f56e-143">Primeiro, crie um [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) e um [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)e recupere a estrutura de tópicos de execução de glifo usando [**IDWriteFontFace:: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline).</span><span class="sxs-lookup"><span data-stu-id="6f56e-143">First, create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and an [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink), and then retrieve the glyph run outline by using [**IDWriteFontFace::GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline).</span></span> <span data-ttu-id="6f56e-144">Em seguida, transforme a origem da geometria usando o método [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory:: CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) , conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="6f56e-144">Then transform the origin of the geometry by using the [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory::CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method, as shown in the following code.</span></span>


```C++
HRESULT hr = S_OK;

// Create the path geometry.
ID2D1PathGeometry* pPathGeometry = NULL;
hr = pD2DFactory_->CreatePathGeometry(
        &pPathGeometry
        );

// Write to the path geometry using the geometry sink.
ID2D1GeometrySink* pSink = NULL;
if (SUCCEEDED(hr))
{
    hr = pPathGeometry->Open(
        &pSink
        );
}

// Get the glyph run outline geometries back from DirectWrite and place them within the
// geometry sink.
if (SUCCEEDED(hr))
{
    hr = glyphRun->fontFace->GetGlyphRunOutline(
        glyphRun->fontEmSize,
        glyphRun->glyphIndices,
        glyphRun->glyphAdvances,
        glyphRun->glyphOffsets,
        glyphRun->glyphCount,
        glyphRun->isSideways,
        glyphRun->bidiLevel%2,
        pSink
        );
}

// Close the geometry sink
if (SUCCEEDED(hr))
{
    hr = pSink->Close();
}

// Initialize a matrix to translate the origin of the glyph run.
D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
    1.0f, 0.0f,
    0.0f, 1.0f,
    baselineOriginX, baselineOriginY
    );

// Create the transformed geometry
ID2D1TransformedGeometry* pTransformedGeometry = NULL;
if (SUCCEEDED(hr))
{
    hr = pD2DFactory_->CreateTransformedGeometry(
        pPathGeometry,
        &matrix,
        &pTransformedGeometry
        );
}
```



<span data-ttu-id="6f56e-145">Em seguida, declare um objeto de pincel sólido [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="6f56e-145">Next, declare a [Direct2D](../direct2d/direct2d-portal.md) solid brush object.</span></span>


```C++
ID2D1SolidColorBrush* pBrush = NULL;
```



<span data-ttu-id="6f56e-146">Se o parâmetro *clientDrawingEffect* não for nulo, consulte o objeto para a interface **ColorDrawingEffect** .</span><span class="sxs-lookup"><span data-stu-id="6f56e-146">If the *clientDrawingEffect* parameter is not NULL, query the object for the **ColorDrawingEffect** interface.</span></span> <span data-ttu-id="6f56e-147">Isso funcionará porque você definirá essa classe como o efeito de desenho do cliente em intervalos de texto do objeto de layout de texto.</span><span class="sxs-lookup"><span data-stu-id="6f56e-147">This will work because you will set this class as the client drawing effect on text ranges of the text layout object.</span></span>

<span data-ttu-id="6f56e-148">Depois de ter um ponteiro para a interface **ColorDrawingEffect** , você pode recuperar o [**valor \_ \_ F de cor de d2d1**](../direct2d/d2d1-color-f.md) que ele armazena usando o método **GetColor** .</span><span class="sxs-lookup"><span data-stu-id="6f56e-148">Once you have a pointer to the **ColorDrawingEffect** interface, you can retrieve the [**D2D1\_COLOR\_F**](../direct2d/d2d1-color-f.md) value that it stores using the **GetColor** method.</span></span> <span data-ttu-id="6f56e-149">Em seguida, use **a \_ cor d2d1 \_ F** para criar um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) nessa cor.</span><span class="sxs-lookup"><span data-stu-id="6f56e-149">Then, use the **D2D1\_COLOR\_F** to create a [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) in that color.</span></span>

<span data-ttu-id="6f56e-150">Se o parâmetro *clientDrawingEffect* for **nulo**, basta criar um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)preto.</span><span class="sxs-lookup"><span data-stu-id="6f56e-150">If the *clientDrawingEffect* parameter is **NULL**, then just create a black [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>


```C++
// If there is a drawing effect create a color brush using it, otherwise create a black brush.
if (clientDrawingEffect != NULL)
{
    // Go from IUnknown to ColorDrawingEffect.
    ColorDrawingEffect *colorDrawingEffect;

    clientDrawingEffect->QueryInterface(__uuidof(ColorDrawingEffect), reinterpret_cast<void**>(&colorDrawingEffect));

    // Get the color from the ColorDrawingEffect object.
    D2D1_COLOR_F color;

    colorDrawingEffect->GetColor(&color);

    // Create the brush using the color pecified by our ColorDrawingEffect object.
    if (SUCCEEDED(hr))
    {
        hr = pRT_->CreateSolidColorBrush(
            color,
            &pBrush);
    }

    SafeRelease(&colorDrawingEffect);
}
else
{
    // Create a black brush.
    if (SUCCEEDED(hr))
    {
        hr = pRT_->CreateSolidColorBrush(
            D2D1::ColorF(
            D2D1::ColorF::Black
            ),
            &pBrush);
    }
}
```



<span data-ttu-id="6f56e-151">Por fim, desenhe a geometria da estrutura de tópicos e preencha-a usando o pincel de cor sólida que você acabou de criar.</span><span class="sxs-lookup"><span data-stu-id="6f56e-151">Finally, draw the outline geometry and fill it using the solid color brush that you just created.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Draw the outline of the glyph run
    pRT_->DrawGeometry(
        pTransformedGeometry,
        pBrush
        );

    // Fill in the glyph run
    pRT_->FillGeometry(
        pTransformedGeometry,
        pBrush
        );
}
```



### <a name="the-destructor"></a><span data-ttu-id="6f56e-152">O destruidor</span><span class="sxs-lookup"><span data-stu-id="6f56e-152">The Destructor</span></span>

<span data-ttu-id="6f56e-153">Não se esqueça de liberar a fábrica [Direct2D](../direct2d/direct2d-portal.md) e o destino de renderização no destruidor.</span><span class="sxs-lookup"><span data-stu-id="6f56e-153">Don't forget to release the [Direct2D](../direct2d/direct2d-portal.md) factory and render target in the destructor.</span></span>


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
}
```



## <a name="step-4-create-the-text-renderer"></a><span data-ttu-id="6f56e-154">Etapa 4: criar o processador de texto</span><span class="sxs-lookup"><span data-stu-id="6f56e-154">Step 4: Create the Text Renderer</span></span>

<span data-ttu-id="6f56e-155">Nos recursos **CreateDeviceDependent** , crie o objeto de processador de texto personalizado.</span><span class="sxs-lookup"><span data-stu-id="6f56e-155">In the **CreateDeviceDependent** resources, create the custom text renderer object.</span></span> <span data-ttu-id="6f56e-156">É dependente de dispositivo porque usa o **ID2D1RenderTarget**, que é dependente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f56e-156">It is device dependent because it uses the **ID2D1RenderTarget**, which is itself device dependent.</span></span>


```C++
// Create the text renderer
pTextRenderer_ = new CustomTextRenderer(
                        pD2DFactory_,
                        pRT_
                        );
```



## <a name="step-5-instantiate-the-color-drawing-effect-objects"></a><span data-ttu-id="6f56e-157">Etapa 5: instanciar os objetos de efeito de desenho de cor</span><span class="sxs-lookup"><span data-stu-id="6f56e-157">Step 5: Instantiate the Color Drawing Effect Objects</span></span>

<span data-ttu-id="6f56e-158">Crie uma instância de objetos **ColorDrawingEffect** em vermelho, verde e azul.</span><span class="sxs-lookup"><span data-stu-id="6f56e-158">Instantiate **ColorDrawingEffect** objects in red, green, and blue.</span></span>


```C++
// Instantiate some custom color drawing effects.
redDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Red
        )
    );

blueDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Blue
        )
    );

greenDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Green
        )
    );
```



## <a name="step-6-set-the-drawing-effect-for-specific-text-ranges"></a><span data-ttu-id="6f56e-159">Etapa 6: definir o efeito de desenho para intervalos de texto específicos</span><span class="sxs-lookup"><span data-stu-id="6f56e-159">Step 6: Set the Drawing Effect for Specific Text Ranges</span></span>

<span data-ttu-id="6f56e-160">Defina o efeito de desenho para intervalos específicos de texto usando o método [**IDWriteTextLayou:: SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) e um struct de [**\_ \_ intervalo de texto DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) .</span><span class="sxs-lookup"><span data-stu-id="6f56e-160">Set the drawing effect for specific ranges of text by using the [**IDWriteTextLayou::SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) method and a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) struct.</span></span>


```C++
// Set the drawing effects.

// Red.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {0,
                                   14};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(redDrawingEffect_, textRange);
    }
}

// Blue.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {14,
                                   7};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(blueDrawingEffect_, textRange);
    }
}

// Green.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {21,
                                   8};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(greenDrawingEffect_, textRange);
    }
}
```



## <a name="step-7-draw-the-text-layout-using-the-custom-renderer"></a><span data-ttu-id="6f56e-161">Etapa 7: desenhar o layout de texto usando o renderizador personalizado</span><span class="sxs-lookup"><span data-stu-id="6f56e-161">Step 7: Draw the Text Layout Using the Custom Renderer</span></span>

<span data-ttu-id="6f56e-162">Você deve chamar o método [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) em vez dos métodos [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) ou [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="6f56e-162">You must call the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method rather than the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) or [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) methods.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



## <a name="step-8-clean-up"></a><span data-ttu-id="6f56e-163">Etapa 8: limpar</span><span class="sxs-lookup"><span data-stu-id="6f56e-163">Step 8: Clean up</span></span>

<span data-ttu-id="6f56e-164">No destruidor DemoApp, libere o renderizador de texto personalizado.</span><span class="sxs-lookup"><span data-stu-id="6f56e-164">In the DemoApp destructor, release the custom text renderer.</span></span>


```C++
SafeRelease(&pTextRenderer_);
```



<span data-ttu-id="6f56e-165">Depois disso, adicione o código para liberar as classes de efeito de desenho do cliente.</span><span class="sxs-lookup"><span data-stu-id="6f56e-165">After that, add code to release the client drawing effect classes.</span></span>


```C++
SafeRelease(&redDrawingEffect_);
SafeRelease(&blueDrawingEffect_);
SafeRelease(&greenDrawingEffect_);
```



 

 