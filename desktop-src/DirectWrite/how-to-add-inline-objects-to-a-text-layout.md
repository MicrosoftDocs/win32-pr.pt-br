---
title: Como adicionar objetos embutidos a um layout de texto
description: Fornece um breve tutorial sobre como adicionar objetos embutidos a um aplicativo DirectWrite que exibe texto usando a interface IDWriteTextLayout.
ms.assetid: 6aa9d17c-ee30-497f-9c73-ec2fa079222b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d9ef34e38ec9b84afd887e565e76efb9618b88
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104555504"
---
# <a name="how-to-add-inline-objects-to-a-text-layout"></a><span data-ttu-id="1f625-103">Como adicionar objetos embutidos a um layout de texto</span><span class="sxs-lookup"><span data-stu-id="1f625-103">How to Add Inline Objects to a Text Layout</span></span>

<span data-ttu-id="1f625-104">Fornece um breve tutorial sobre como adicionar objetos embutidos a um aplicativo [DirectWrite](direct-write-portal.md) que exibe texto usando a interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="1f625-104">Provides a short tutorial on adding inline objects to a [DirectWrite](direct-write-portal.md) application that displays text using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

<span data-ttu-id="1f625-105">O produto final deste tutorial é um aplicativo que exibe o texto com uma imagem embutida inserida nela, conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f625-105">The end product of this tutorial is an application that displays text with an inline image embedded in it, as shown in the following screen shot.</span></span>

![captura de tela do "exemplo de objeto embutido" com uma imagem inserida](images/inlineobject.png)

<span data-ttu-id="1f625-107">Este tutorial contém as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="1f625-107">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="1f625-108">Etapa 1: criar um layout de texto.</span><span class="sxs-lookup"><span data-stu-id="1f625-108">Step 1: Create a Text Layout.</span></span>](#step-1-create-a-text-layout)
-   [<span data-ttu-id="1f625-109">Etapa 2: definir uma classe derivada da interface IDWriteInlineObject.</span><span class="sxs-lookup"><span data-stu-id="1f625-109">Step 2: Define a class derived from the IDWriteInlineObject interface.</span></span>](#step-2-define-a-class-derived-from-the-idwriteinlineobject-interface)
-   [<span data-ttu-id="1f625-110">Etapa 3: implementar a classe de objeto embutido.</span><span class="sxs-lookup"><span data-stu-id="1f625-110">Step 3: Implement the Inline Object Class.</span></span>](#step-3-implement-the-inline-object-class)
    -   [<span data-ttu-id="1f625-111">O construtor.</span><span class="sxs-lookup"><span data-stu-id="1f625-111">The Constructor.</span></span>](#the-constructor)
    -   [<span data-ttu-id="1f625-112">O método Draw.</span><span class="sxs-lookup"><span data-stu-id="1f625-112">The Draw Method.</span></span>](#the-draw-method)
    -   [<span data-ttu-id="1f625-113">O método getmetrics.</span><span class="sxs-lookup"><span data-stu-id="1f625-113">The GetMetrics Method.</span></span>](#the-getmetrics-method)
    -   [<span data-ttu-id="1f625-114">O método GetOverhangMetrics.</span><span class="sxs-lookup"><span data-stu-id="1f625-114">The GetOverhangMetrics Method.</span></span>](#the-getoverhangmetrics-method)
    -   [<span data-ttu-id="1f625-115">O método GetBreakConditions.</span><span class="sxs-lookup"><span data-stu-id="1f625-115">The GetBreakConditions Method.</span></span>](#the-getbreakconditions-method)
-   [<span data-ttu-id="1f625-116">Etapa 4: Crie uma instância da classe InlineImage e adicione-a ao layout de texto.</span><span class="sxs-lookup"><span data-stu-id="1f625-116">Step 4: Create an Instance of the InlineImage Class and Add it to the Text Layout.</span></span>](#step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="1f625-117">Etapa 1: criar um layout de texto.</span><span class="sxs-lookup"><span data-stu-id="1f625-117">Step 1: Create a Text Layout.</span></span>

<span data-ttu-id="1f625-118">Para começar, você precisará de um aplicativo com um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="1f625-118">To begin, you will need an application with an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="1f625-119">Se você já tiver um aplicativo que exibe texto com um layout de texto, pule para a etapa 2.</span><span class="sxs-lookup"><span data-stu-id="1f625-119">If you already have an application that displays text with a text layout, skip to Step 2.</span></span>

<span data-ttu-id="1f625-120">Para adicionar um layout de texto, você deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1f625-120">To add a text layout you must do the following:</span></span>

1.  <span data-ttu-id="1f625-121">Declare um ponteiro para uma interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) como um membro da classe.</span><span class="sxs-lookup"><span data-stu-id="1f625-121">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="1f625-122">No final do método CreateDeviceIndependentResources, crie um objeto de interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chamando o método [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="1f625-122">At the end of the CreateDeviceIndependentResources method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>
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

    

3.  <span data-ttu-id="1f625-123">Em seguida, você deve alterar a chamada para o método [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) para [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f625-123">Then, you must change the call to the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method to [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), as shown in the following code.</span></span>
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

## <a name="step-2-define-a-class-derived-from-the-idwriteinlineobject-interface"></a><span data-ttu-id="1f625-124">Etapa 2: definir uma classe derivada da interface IDWriteInlineObject.</span><span class="sxs-lookup"><span data-stu-id="1f625-124">Step 2: Define a class derived from the IDWriteInlineObject interface.</span></span>

<span data-ttu-id="1f625-125">O suporte para objetos embutidos no [DirectWrite](direct-write-portal.md) é fornecido pela interface [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) .</span><span class="sxs-lookup"><span data-stu-id="1f625-125">Support for inline objects in [DirectWrite](direct-write-portal.md) is provided by the [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) interface.</span></span> <span data-ttu-id="1f625-126">Para usar objetos embutidos, você deve implementar essa interface.</span><span class="sxs-lookup"><span data-stu-id="1f625-126">To use inline objects, you must implement this interface.</span></span> <span data-ttu-id="1f625-127">Ele manipula o desenho do objeto embutido, bem como fornece métricas e outras informações para o renderizador.</span><span class="sxs-lookup"><span data-stu-id="1f625-127">It handles the drawing of the inline object, as well as providing metrics and other information to the renderer.</span></span>

<span data-ttu-id="1f625-128">Crie um novo arquivo de cabeçalho e declare uma interface chamada InlineImage, derivada de [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject).</span><span class="sxs-lookup"><span data-stu-id="1f625-128">Create a new header file and declare an interface called InlineImage, derived from [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject).</span></span>

<span data-ttu-id="1f625-129">Além de QueryInterface, AddRef e Release herdados de IUnknown, essa classe deve ter os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="1f625-129">In addition to QueryInterface, AddRef, and Release inherited from IUnknown, this class must have the following methods:</span></span>

-   [<span data-ttu-id="1f625-130">**Draw**</span><span class="sxs-lookup"><span data-stu-id="1f625-130">**Draw**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw)
-   [<span data-ttu-id="1f625-131">**Getmetrics**</span><span class="sxs-lookup"><span data-stu-id="1f625-131">**GetMetrics**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics)
-   [<span data-ttu-id="1f625-132">**GetOverhangMetrics**</span><span class="sxs-lookup"><span data-stu-id="1f625-132">**GetOverhangMetrics**</span></span>](idwriteinlineobject-getoverhangmetrics.md)
-   [<span data-ttu-id="1f625-133">**GetBreakConditions**</span><span class="sxs-lookup"><span data-stu-id="1f625-133">**GetBreakConditions**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getbreakconditions)

## <a name="step-3-implement-the-inline-object-class"></a><span data-ttu-id="1f625-134">Etapa 3: implementar a classe de objeto embutido.</span><span class="sxs-lookup"><span data-stu-id="1f625-134">Step 3: Implement the Inline Object Class.</span></span>

<span data-ttu-id="1f625-135">Crie um novo arquivo C++, chamado InlineImage. cpp, para a implementação de classe.</span><span class="sxs-lookup"><span data-stu-id="1f625-135">Create a new C++ file, named InlineImage.cpp, for the class implementation.</span></span> <span data-ttu-id="1f625-136">Além do método LoadBitmapFromFile e dos métodos herdados da interface IUnknown, a classe InlineImage é composta pelos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f625-136">In addition to the LoadBitmapFromFile method and the methods inherited from the IUnknown interface, the InlineImage class is made up of the following methods.</span></span>

### <a name="the-constructor"></a><span data-ttu-id="1f625-137">O construtor.</span><span class="sxs-lookup"><span data-stu-id="1f625-137">The Constructor.</span></span>


```C++
InlineImage::InlineImage(
    ID2D1RenderTarget *pRenderTarget, 
    IWICImagingFactory *pIWICFactory,
    PCWSTR uri
    )
{
    // Save the render target for later.
    pRT_ = pRenderTarget;

    pRT_->AddRef();

    // Load the bitmap from a file.
    LoadBitmapFromFile(
        pRenderTarget,
        pIWICFactory,
        uri,
        &pBitmap_
        );
}
```



<span data-ttu-id="1f625-138">O primeiro argumento do construtor é o ID2D1RenderTarget para o qual a imagem embutida será renderizada.</span><span class="sxs-lookup"><span data-stu-id="1f625-138">The first argument of the constructor is the ID2D1RenderTarget that the inline image will be rendered to.</span></span> <span data-ttu-id="1f625-139">Isso é armazenado para uso posterior durante o desenho.</span><span class="sxs-lookup"><span data-stu-id="1f625-139">This is stored for use later when drawing.</span></span>

<span data-ttu-id="1f625-140">O destino de renderização, IWICImagingFactory e o URI do nome de arquivo são todos passados para o método LoadBitmapFromFile que carrega o bitmap e armazena o tamanho do bitmap (largura e altura) na \_ variável de membro Rect.</span><span class="sxs-lookup"><span data-stu-id="1f625-140">The render target, IWICImagingFactory, and the filename uri are all passed to the LoadBitmapFromFile method that loads the bitmap and stores the bitmap size (width and height) in the rect\_ member variable.</span></span>

### <a name="the-draw-method"></a><span data-ttu-id="1f625-141">O método Draw.</span><span class="sxs-lookup"><span data-stu-id="1f625-141">The Draw Method.</span></span>

<span data-ttu-id="1f625-142">O método [**draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw) é um retorno de chamada que é chamado pelo objeto [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) quando o objeto embutido precisa ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="1f625-142">The [**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw) method is a callback that is called by the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) object when the inline object needs to be drawn.</span></span> <span data-ttu-id="1f625-143">O layout de texto não chama esse método diretamente.</span><span class="sxs-lookup"><span data-stu-id="1f625-143">The text layout does not call this method directly.</span></span>


```C++
HRESULT STDMETHODCALLTYPE InlineImage::Draw(
    __maybenull void* clientDrawingContext,
    IDWriteTextRenderer* renderer,
    FLOAT originX,
    FLOAT originY,
    BOOL isSideways,
    BOOL isRightToLeft,
    IUnknown* clientDrawingEffect
    )
{
    float height    = rect_.bottom - rect_.top;
    float width     = rect_.right  - rect_.left;
    D2D1_RECT_F destRect  = {originX, originY, originX + width, originY + height};

    pRT_->DrawBitmap(pBitmap_, destRect);

    return S_OK;
}
```



<span data-ttu-id="1f625-144">Nesse caso, o desenho do bitmap é feito usando o método [**ID2D1RenderTarget::D rawbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) ; no entanto, qualquer método de desenho pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="1f625-144">In this case, drawing the bitmap is done by using the [**ID2D1RenderTarget::DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) method; however, any method for drawing can be used.</span></span>

### <a name="the-getmetrics-method"></a><span data-ttu-id="1f625-145">O método getmetrics.</span><span class="sxs-lookup"><span data-stu-id="1f625-145">The GetMetrics Method.</span></span>


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetMetrics(
    __out DWRITE_INLINE_OBJECT_METRICS* metrics
    )
{
    DWRITE_INLINE_OBJECT_METRICS inlineMetrics = {};
    inlineMetrics.width     = rect_.right  - rect_.left;
    inlineMetrics.height    = rect_.bottom - rect_.top;
    inlineMetrics.baseline  = baseline_;
    *metrics = inlineMetrics;
    return S_OK;
}
```



<span data-ttu-id="1f625-146">Para o método [**Getmetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) , armazene a largura, a altura e a linha de base em uma estrutura de [**\_ \_ \_ métricas de objeto embutido DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) .</span><span class="sxs-lookup"><span data-stu-id="1f625-146">For the [**GetMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) method, store the width, height and baseline in an [**DWRITE\_INLINE\_OBJECT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) structure.</span></span> <span data-ttu-id="1f625-147">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chama essa função de retorno de chamada para obter a medida do objeto embutido.</span><span class="sxs-lookup"><span data-stu-id="1f625-147">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) calls this callback function to get the measurement of the inline object.</span></span>

### <a name="the-getoverhangmetrics-method"></a><span data-ttu-id="1f625-148">O método GetOverhangMetrics.</span><span class="sxs-lookup"><span data-stu-id="1f625-148">The GetOverhangMetrics Method.</span></span>


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetOverhangMetrics(
    __out DWRITE_OVERHANG_METRICS* overhangs
    )
{
    overhangs->left      = 0;
    overhangs->top       = 0;
    overhangs->right     = 0;
    overhangs->bottom    = 0;
    return S_OK;
}
```



<span data-ttu-id="1f625-149">Nesse caso, nenhuma folga é necessária, portanto, o método [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md) retorna todos os zeros.</span><span class="sxs-lookup"><span data-stu-id="1f625-149">In this case, no overhang is necessary, so the [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md) method returns all zeros.</span></span>

### <a name="the-getbreakconditions-method"></a><span data-ttu-id="1f625-150">O método GetBreakConditions.</span><span class="sxs-lookup"><span data-stu-id="1f625-150">The GetBreakConditions Method.</span></span>


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetBreakConditions(
    __out DWRITE_BREAK_CONDITION* breakConditionBefore,
    __out DWRITE_BREAK_CONDITION* breakConditionAfter
    )
{
    *breakConditionBefore = DWRITE_BREAK_CONDITION_NEUTRAL;
    *breakConditionAfter  = DWRITE_BREAK_CONDITION_NEUTRAL;
    return S_OK;
}
```



## <a name="step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout"></a><span data-ttu-id="1f625-151">Etapa 4: Crie uma instância da classe InlineImage e adicione-a ao layout de texto.</span><span class="sxs-lookup"><span data-stu-id="1f625-151">Step 4: Create an Instance of the InlineImage Class and Add it to the Text Layout.</span></span>

<span data-ttu-id="1f625-152">Por fim, no método CreateDeviceDependentResources, crie uma instância da classe InlineImage e adicione-a ao layout de texto.</span><span class="sxs-lookup"><span data-stu-id="1f625-152">Finally, in the CreateDeviceDependentResources method, create an instance of the InlineImage class and add it to the text layout.</span></span> <span data-ttu-id="1f625-153">Como ele contém uma referência ao [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), que é um recurso dependente de dispositivo, e o [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) é criado usando o destino render, o InlineImage também é dependente de dispositivo e deve ser recriado se o destino de renderização for recriado.</span><span class="sxs-lookup"><span data-stu-id="1f625-153">Because it holds a reference to the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), which is a device dependent resource, and the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is created by using the render target, the InlineImage is also device dependent and must be recreated if the render target is recreated.</span></span>


```C++
// Create an InlineObject.
pInlineImage_ = new InlineImage(pRT_, pWICFactory_, L"img1.jpg");

DWRITE_TEXT_RANGE textRange = {14, 1};

pTextLayout_->SetInlineObject(pInlineImage_, textRange);
```



<span data-ttu-id="1f625-154">O método [**IDWriteTextLayout:: Setinlineobject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject) usa uma estrutura de intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="1f625-154">The [**IDWriteTextLayout::SetInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject) method takes a text range structure.</span></span> <span data-ttu-id="1f625-155">O objeto se aplica ao intervalo especificado aqui e qualquer texto no intervalo será suprimido.</span><span class="sxs-lookup"><span data-stu-id="1f625-155">The object applies to the range specified here, and any text in the range will be suppressed.</span></span> <span data-ttu-id="1f625-156">Se o comprimento do intervalo de texto for 0, o objeto não será desenhado.</span><span class="sxs-lookup"><span data-stu-id="1f625-156">If the length of the text range is 0, the object will not be drawn.</span></span>

<span data-ttu-id="1f625-157">Neste exemplo, há um asterisco ( \* ) como um espaço reservado na posição onde a imagem será exibida.</span><span class="sxs-lookup"><span data-stu-id="1f625-157">In this example, there is an asterisk (\*) as a place holder in the position where the image will be displayed.</span></span>


```C++
// The string to display.  The '*' character will be suppressed by our image.
wszText_ = L"Inline Object * Example";
cTextLength_ = wcslen(wszText_);
```



<span data-ttu-id="1f625-158">Como a classe InlineImage é dependente do [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), você deve liberá-la ao liberar o destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="1f625-158">Since the InlineImage class is dependent on the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), you must release it when you release the render target.</span></span>


```C++
SafeRelease(&pInlineImage_);
```



 

 