---
title: Como adicionar efeitos de desenho do cliente a um layout de texto
description: Fornece um breve tutorial sobre como adicionar efeitos de desenho do cliente a um aplicativo DirectWrite que exibe texto usando a interface IDWriteTextLayout e um renderador de texto personalizado.
ms.assetid: b66ff814-2113-48b0-8913-3d30a5d20077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bae98813d8f8aa8fc8a7df0a1a53d11a0329c93abb22a7f60d60754b8edc91f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071701"
---
# <a name="how-to-add-client-drawing-effects-to-a-text-layout"></a>Como adicionar efeitos de desenho do cliente a um layout de texto

Fornece um breve tutorial sobre como adicionar efeitos de desenho do cliente a um [aplicativo DirectWrite](direct-write-portal.md) que exibe texto usando a interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) e um renderador de texto personalizado.

O produto final deste tutorial é um aplicativo que exibe texto que tem intervalos de texto com um efeito de desenho de cores diferente em cada um, conforme mostrado na captura de tela a seguir.

![captura de tela do "exemplo de efeito de desenho do cliente!" em cores diferentes](images/drawingeffects.png)

> [!Note]  
> Este tutorial deve ser um exemplo simplificado de como criar efeitos de desenho de cliente personalizados, não um exemplo de um método simples para desenhar texto de cor. Consulte a página de referência [**IDWriteTextLayout::SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) para obter mais informações.

 

Este tutorial contém as seguintes partes:

-   [Etapa 1: Criar um layout de texto](#step-1-create-a-text-layout)
-   [Etapa 2: Implementar uma classe de efeito de desenho personalizada](#step-2-implement-a-custom-drawing-effect-class)
-   [Etapa 3: Implementar uma classe de renderização de texto personalizado](#step-3-implement-a-custom-text-renderer-class)
    -   [O construtor](#the-constructor)
    -   [O método DrawGlyphRun](#the-drawglyphrun-method)
    -   [O destruidor](#the-destructor)
-   [Etapa 4: Criar o renderdor de texto](#step-4-create-the-text-renderer)
-   [Etapa 5: Insinciar os objetos de efeito de desenho de cor](#step-5-instantiate-the-color-drawing-effect-objects)
-   [Etapa 6: Definir o efeito de desenho para intervalos de texto específicos](#step-6-set-the-drawing-effect-for-specific-text-ranges)
-   [Etapa 7: desenhar o layout de texto usando o renderdor personalizado](#step-7-draw-the-text-layout-using-the-custom-renderer)
-   [Etapa 8: Limpar](#step-8-clean-up)

## <a name="step-1-create-a-text-layout"></a>Etapa 1: Criar um layout de texto

Para começar, você precisará de um aplicativo com um [**objeto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) Se você já tiver um aplicativo que exibe texto com um layout de texto ou estiver usando o Código de Exemplo DrawingEffect Personalizado, pule para a Etapa 2.

Para adicionar um layout de texto, você deve fazer o seguinte:

1.  Declare um ponteiro para uma interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) como um membro da classe .
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  No final do método **CreateDeviceIndependentResources,** crie um objeto de interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chamando o [**método CreateTextLayout.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)
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

    

3.  Por fim, lembre-se de liberar o layout de texto no destruidor.
    ```C++
    SafeRelease(&pTextLayout_);
    ```

    

## <a name="step-2-implement-a-custom-drawing-effect-class"></a>Etapa 2: Implementar uma classe de efeito de desenho personalizada

Além dos métodos herdados de IUnknown, uma interface de efeito de desenho de cliente personalizada não tem requisitos sobre o que ela deve implementar. Nesse caso, a classe **ColorDrawingEffect** simplesmente mantém um valor [**D2D1 \_ COLOR \_ F**](../direct2d/d2d1-color-f.md) e declara métodos para obter e definir esse valor, bem como um construtor que pode definir a cor inicialmente.

Depois que um efeito de desenho do cliente é aplicado a um intervalo de texto em um objeto [**IDWriteTextLayout,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) o efeito de desenho é passado para o método [**IDWriteTextRenderer::D rawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) de qualquer run de glifo que deve ser renderizado. Os métodos do efeito de desenho ficam disponíveis para o renderdor de texto.

Um efeito de desenho de cliente pode ser tão complexo quanto você deseja torná-lo, carregando mais informações do que neste exemplo, bem como fornecendo métodos para alterar glifos, criar objetos a serem usados para desenho e assim por diante.

## <a name="step-3-implement-a-custom-text-renderer-class"></a>Etapa 3: Implementar uma classe de renderização de texto personalizado

Para aproveitar um efeito de desenho do cliente, você deve implementar um renderador de texto personalizado. Esse renderador de texto aplicará o efeito de desenho passado a ele pelo método [**IDWriteTextLayout::D raw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) à run de glifo que está sendo desenhada.

### <a name="the-constructor"></a>O construtor

O construtor do renderador de texto personalizado armazena o objeto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) que será usado para criar objetos [Direct2D](../direct2d/direct2d-portal.md) e o destino de renderização Direct2D para o que o texto será desenhado.


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



### <a name="the-drawglyphrun-method"></a>O método DrawGlyphRun

Uma run de glifo é um conjunto de glifos que compartilham o mesmo formato, incluindo o efeito de desenho do cliente. O [**método DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) cuida da renderização de texto para uma run de glifo especificada.

Primeiro, crie [**um ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) e um [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)e, em seguida, recupere o contorno de executar glifo usando [**IDWriteFontFace::GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline). Em seguida, transforme a origem [da](../direct2d/direct2d-portal.md) geometria usando o método [**Direct2D ID2D1Factory::CreateTransformedGeometry,**](../direct2d/id2d1factory-createtransformedgeometry.md) conforme mostrado no código a seguir.


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



Em seguida, declare um [Direct2D](../direct2d/direct2d-portal.md) de pincel sólido.


```C++
ID2D1SolidColorBrush* pBrush = NULL;
```



Se o *parâmetro clientDrawingEffect* não for NULL, consulte o objeto para a interface **ColorDrawingEffect.** Isso funcionará porque você definirá essa classe como o efeito de desenho do cliente nos intervalos de texto do objeto de layout de texto.

Depois de ter um ponteiro para a interface **ColorDrawingEffect,** você pode recuperar o valor [**D2D1 \_ COLOR \_ F**](../direct2d/d2d1-color-f.md) que ele armazena usando o **método GetColor.** Em seguida, use **a \_ COR \_ F D2D1** para criar [**um ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) nessa cor.

Se o *parâmetro clientDrawingEffect* for **NULL,** basta criar um [**ID2D1SolidColorBrush preto.**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)


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



Por fim, desenhe a geometria do contorno e preencha-a usando o pincel de cor sólida que você acabou de criar.


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



### <a name="the-destructor"></a>O destruidor

Não se esqueça de liberar a fábrica [Direct2D](../direct2d/direct2d-portal.md) e renderizar o destino no destruidor.


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
}
```



## <a name="step-4-create-the-text-renderer"></a>Etapa 4: Criar o renderdor de texto

Nos recursos **CreateDeviceDependent,** crie o objeto de renderização de texto personalizado. Ele depende do dispositivo porque usa o **ID2D1RenderTarget**, que é dependente do próprio dispositivo.


```C++
// Create the text renderer
pTextRenderer_ = new CustomTextRenderer(
                        pD2DFactory_,
                        pRT_
                        );
```



## <a name="step-5-instantiate-the-color-drawing-effect-objects"></a>Etapa 5: Insinciar os objetos de efeito de desenho de cor

Insinue **objetos ColorDrawingEffect** em vermelho, verde e azul.


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



## <a name="step-6-set-the-drawing-effect-for-specific-text-ranges"></a>Etapa 6: Definir o efeito de desenho para intervalos de texto específicos

Definir o efeito de desenho para intervalos específicos de texto usando o [**método IDWriteTextLayou::SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) e um struct [**DWRITE \_ TEXT \_ RANGE.**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range)


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



## <a name="step-7-draw-the-text-layout-using-the-custom-renderer"></a>Etapa 7: desenhar o layout de texto usando o renderdor personalizado

Você deve chamar o método [**IDWriteTextLayout::D raw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) em vez dos métodos [**ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) ou [**ID2D1RenderTarget::D rawTextLayout.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



## <a name="step-8-clean-up"></a>Etapa 8: Limpar

No destruidor DemoApp, libere o renderdor de texto personalizado.


```C++
SafeRelease(&pTextRenderer_);
```



Depois disso, adicione código para liberar as classes de efeito de desenho do cliente.


```C++
SafeRelease(&redDrawingEffect_);
SafeRelease(&blueDrawingEffect_);
SafeRelease(&greenDrawingEffect_);
```



 

 