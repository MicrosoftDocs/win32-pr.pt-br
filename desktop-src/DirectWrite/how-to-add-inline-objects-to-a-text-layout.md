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
# <a name="how-to-add-inline-objects-to-a-text-layout"></a>Como adicionar objetos embutidos a um layout de texto

Fornece um breve tutorial sobre como adicionar objetos embutidos a um aplicativo [DirectWrite](direct-write-portal.md) que exibe texto usando a interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

O produto final deste tutorial é um aplicativo que exibe o texto com uma imagem embutida inserida nela, conforme mostrado na captura de tela a seguir.

![captura de tela do "exemplo de objeto embutido" com uma imagem inserida](images/inlineobject.png)

Este tutorial contém as seguintes partes:

-   [Etapa 1: criar um layout de texto.](#step-1-create-a-text-layout)
-   [Etapa 2: definir uma classe derivada da interface IDWriteInlineObject.](#step-2-define-a-class-derived-from-the-idwriteinlineobject-interface)
-   [Etapa 3: implementar a classe de objeto embutido.](#step-3-implement-the-inline-object-class)
    -   [O construtor.](#the-constructor)
    -   [O método Draw.](#the-draw-method)
    -   [O método getmetrics.](#the-getmetrics-method)
    -   [O método GetOverhangMetrics.](#the-getoverhangmetrics-method)
    -   [O método GetBreakConditions.](#the-getbreakconditions-method)
-   [Etapa 4: Crie uma instância da classe InlineImage e adicione-a ao layout de texto.](#step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout)

## <a name="step-1-create-a-text-layout"></a>Etapa 1: criar um layout de texto.

Para começar, você precisará de um aplicativo com um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . Se você já tiver um aplicativo que exibe texto com um layout de texto, pule para a etapa 2.

Para adicionar um layout de texto, você deve fazer o seguinte:

1.  Declare um ponteiro para uma interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) como um membro da classe.
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  No final do método CreateDeviceIndependentResources, crie um objeto de interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chamando o método [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .
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

    

3.  Em seguida, você deve alterar a chamada para o método [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) para [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), conforme mostrado no código a seguir.
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

## <a name="step-2-define-a-class-derived-from-the-idwriteinlineobject-interface"></a>Etapa 2: definir uma classe derivada da interface IDWriteInlineObject.

O suporte para objetos embutidos no [DirectWrite](direct-write-portal.md) é fornecido pela interface [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) . Para usar objetos embutidos, você deve implementar essa interface. Ele manipula o desenho do objeto embutido, bem como fornece métricas e outras informações para o renderizador.

Crie um novo arquivo de cabeçalho e declare uma interface chamada InlineImage, derivada de [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject).

Além de QueryInterface, AddRef e Release herdados de IUnknown, essa classe deve ter os seguintes métodos:

-   [**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw)
-   [**Getmetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics)
-   [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md)
-   [**GetBreakConditions**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getbreakconditions)

## <a name="step-3-implement-the-inline-object-class"></a>Etapa 3: implementar a classe de objeto embutido.

Crie um novo arquivo C++, chamado InlineImage. cpp, para a implementação de classe. Além do método LoadBitmapFromFile e dos métodos herdados da interface IUnknown, a classe InlineImage é composta pelos métodos a seguir.

### <a name="the-constructor"></a>O construtor.


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



O primeiro argumento do construtor é o ID2D1RenderTarget para o qual a imagem embutida será renderizada. Isso é armazenado para uso posterior durante o desenho.

O destino de renderização, IWICImagingFactory e o URI do nome de arquivo são todos passados para o método LoadBitmapFromFile que carrega o bitmap e armazena o tamanho do bitmap (largura e altura) na \_ variável de membro Rect.

### <a name="the-draw-method"></a>O método Draw.

O método [**draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw) é um retorno de chamada que é chamado pelo objeto [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) quando o objeto embutido precisa ser desenhado. O layout de texto não chama esse método diretamente.


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



Nesse caso, o desenho do bitmap é feito usando o método [**ID2D1RenderTarget::D rawbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) ; no entanto, qualquer método de desenho pode ser usado.

### <a name="the-getmetrics-method"></a>O método getmetrics.


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



Para o método [**Getmetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) , armazene a largura, a altura e a linha de base em uma estrutura de [**\_ \_ \_ métricas de objeto embutido DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) . [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chama essa função de retorno de chamada para obter a medida do objeto embutido.

### <a name="the-getoverhangmetrics-method"></a>O método GetOverhangMetrics.


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



Nesse caso, nenhuma folga é necessária, portanto, o método [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md) retorna todos os zeros.

### <a name="the-getbreakconditions-method"></a>O método GetBreakConditions.


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



## <a name="step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout"></a>Etapa 4: Crie uma instância da classe InlineImage e adicione-a ao layout de texto.

Por fim, no método CreateDeviceDependentResources, crie uma instância da classe InlineImage e adicione-a ao layout de texto. Como ele contém uma referência ao [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), que é um recurso dependente de dispositivo, e o [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) é criado usando o destino render, o InlineImage também é dependente de dispositivo e deve ser recriado se o destino de renderização for recriado.


```C++
// Create an InlineObject.
pInlineImage_ = new InlineImage(pRT_, pWICFactory_, L"img1.jpg");

DWRITE_TEXT_RANGE textRange = {14, 1};

pTextLayout_->SetInlineObject(pInlineImage_, textRange);
```



O método [**IDWriteTextLayout:: Setinlineobject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject) usa uma estrutura de intervalo de texto. O objeto se aplica ao intervalo especificado aqui e qualquer texto no intervalo será suprimido. Se o comprimento do intervalo de texto for 0, o objeto não será desenhado.

Neste exemplo, há um asterisco ( \* ) como um espaço reservado na posição onde a imagem será exibida.


```C++
// The string to display.  The '*' character will be suppressed by our image.
wszText_ = L"Inline Object * Example";
cTextLength_ = wcslen(wszText_);
```



Como a classe InlineImage é dependente do [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), você deve liberá-la ao liberar o destino de renderização.


```C++
SafeRelease(&pInlineImage_);
```



 

 