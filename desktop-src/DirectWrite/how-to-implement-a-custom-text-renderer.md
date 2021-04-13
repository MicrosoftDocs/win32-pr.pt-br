---
title: Renderizar usando um renderizador de texto personalizado
description: Um layout de texto DirectWrite \ 160; pode ser desenhado por um renderizador de texto personalizado derivado de IDWriteTextRenderer.
ms.assetid: a5b09733-24b2-408e-a1f9-cf7ad20c5c63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17cda56fc5cc38a62e48a2f62066edfec2327e9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366298"
---
# <a name="render-using-a-custom-text-renderer"></a>Renderizar usando um renderizador de texto personalizado

Um [](direct-write-portal.md) [**layout de texto**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) DirectWrite pode ser desenhado por um renderizador de texto personalizado derivado de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer). Um processador personalizado é necessário para aproveitar alguns recursos avançados do DirectWrite, como renderização em um bitmap ou superfície GDI, objetos embutidos e efeitos de desenho de cliente. Este tutorial descreve os métodos de **IDWriteTextRenderer** e fornece uma implementação de exemplo que usa [Direct2D](../direct2d/direct2d-portal.md) para renderizar texto com um preenchimento de bitmap.

Este tutorial contém as seguintes partes:

-   [O Construtor](#the-constructor)
-   [DrawGlyphRun()](#drawglyphrun)
-   [DrawUnderline () e DrawStrikethrough ()](#drawunderline-and-drawstrikethrough)
-   [Encaixe de pixels, pixels por DIP e transformação](#pixel-snapping-pixels-per-dip-and-transform)
    -   [IsPixelSnappingDisabled()](#ispixelsnappingdisabled)
    -   [GetCurrentTransform()](#getcurrenttransform)
    -   [GetPixelsPerDip()](#getpixelsperdip)
-   [DrawInlineObject()](#drawinlineobject)
-   [O destruidor](#the-destructor)
-   [Usando o renderizador de texto personalizado](#using-the-custom-text-renderer)

Seu renderizador de texto personalizado deve implementar os métodos herdados de IUnknown, além dos métodos listados na página de referência do [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) e abaixo.

Para obter o código-fonte completo do renderizador de texto personalizado, consulte os arquivos CustomTextRenderer. cpp e CustomTextRenderer. h do [exemplo de Olá, mundo de DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples).

## <a name="the-constructor"></a>O Construtor

Seu renderizador de texto personalizado precisará de um construtor. Este exemplo usa pincéis sólidos e de [Direct2D](../direct2d/direct2d-portal.md) de bitmap para renderizar o texto.

Por isso, o construtor usa os parâmetros encontrados na tabela abaixo com descrições.



| Parâmetro       | Descrição                                                                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *pD2DFactory*   | Um ponteiro para um objeto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) que será usado para criar qualquer recurso do Direct2D que seja necessário.                                                                                                        |
| *pRT*           | Um ponteiro para o objeto [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) para o qual o texto será renderizado. |
| *pOutlineBrush* | Um ponteiro para o [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) que será usado para desenhar o contorno do texto                                                                                                                     |
| *pFillBrush*    | Um ponteiro para o [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) que será usado para preencher o texto.                                                                                                                                      |



 

Eles serão armazenados pelo construtor, conforme mostrado no código a seguir.


```C++
CustomTextRenderer::CustomTextRenderer(
    ID2D1Factory* pD2DFactory, 
    ID2D1HwndRenderTarget* pRT, 
    ID2D1SolidColorBrush* pOutlineBrush, 
    ID2D1BitmapBrush* pFillBrush
    )
:
cRefCount_(0), 
pD2DFactory_(pD2DFactory), 
pRT_(pRT), 
pOutlineBrush_(pOutlineBrush), 
pFillBrush_(pFillBrush)
{
    pD2DFactory_->AddRef();
    pRT_->AddRef();
    pOutlineBrush_->AddRef();
    pFillBrush_->AddRef();
}
```



## <a name="drawglyphrun"></a>DrawGlyphRun()

O método [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) é o principal método de retorno de chamada do processador de texto. É passada uma execução de glifos a serem renderizados, além de informações como a origem da linha de base e o modo de medição. Ele também passa um objeto de efeito de desenho de cliente para ser aplicado à execução de glifo. Para obter mais informações, consulte o tópico [como adicionar efeitos de desenho de cliente a um layout de texto](how-to-add-custom-drawing-efffects-to-a-text-layout.md) .

Essa implementação de processador de texto renderiza as execuções de glifos convertendo-as em geometrias de [Direct2D](rendering-by-using-direct2d.md) e, em seguida, desenhando e preenchendo as geometria Isso consiste nas etapas a seguir.

1.  Crie um objeto [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) e, em seguida, recupere o objeto [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) usando o método [**ID2D1PathGeometry:: Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) .

    ```C++
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
    ```

    

2.  A [**\_ \_ execução de glifo DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) que é passada para [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) contém um objeto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) , chamado *fontface*, que representa a face da fonte para toda a execução do glifo. Coloque o contorno do glifo executado no coletor de geometria usando o método [**IDWriteFontFace:: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) , conforme mostrado no código a seguir.

    ```C++
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
    ```

    

3.  Depois de preencher o coletor de geometria, feche-o.

    ```C++
    // Close the geometry sink
    if (SUCCEEDED(hr))
    {
        hr = pSink->Close();
    }
    ```

    

4.  A origem da execução de glifo deve ser traduzida para que seja renderizada da origem de linha de base correta, conforme mostrado no código a seguir.

    ```C++
    // Initialize a matrix to translate the origin of the glyph run.
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );
    ```

    

    *BaselineOriginX* e *baselineOriginY* são passados como parâmetros para o método de retorno de chamada [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) .

5.  Crie a geometria transformada usando o método [**ID2D1Factory:: CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) e passando a geometria do caminho e a matriz de conversão.

    ```C++
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

    

6.  Por fim, desenhe o contorno da geometria transformada e preencha-a usando os métodos [**ID2D1RenderTarget::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) e [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) e os pincéis de [Direct2D](../direct2d/direct2d-portal.md) armazenados como variáveis de membro.

    ```C++
        // Draw the outline of the glyph run
        pRT_->DrawGeometry(
            pTransformedGeometry,
            pOutlineBrush_
            );

        // Fill in the glyph run
        pRT_->FillGeometry(
            pTransformedGeometry,
            pFillBrush_
            );
    ```

    

7.  Agora que você terminou de desenhar, não se esqueça de limpar os objetos que foram criados nesse método.

    ```C++
    SafeRelease(&pPathGeometry);
    SafeRelease(&pSink);
    SafeRelease(&pTransformedGeometry);
    ```

    

## <a name="drawunderline-and-drawstrikethrough"></a>DrawUnderline () e DrawStrikethrough ()

[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) também tem retornos de chamada para desenhar o sublinhado e tachado. Este exemplo desenha um retângulo simples para um sublinhado ou tachado, mas outras formas podem ser desenhadas.

Desenhar um sublinhado usando [Direct2D](../direct2d/direct2d-portal.md) consiste nas etapas a seguir.

1.  Primeiro, crie uma estrutura [**d2d1 \_ Rect \_ F**](../direct2d/d2d1-rect-f.md) do tamanho e da forma do sublinhado. A [**estrutura \_ sublinhada DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) que é passada para o método de retorno de chamada [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) fornece o deslocamento, a largura e a espessura do sublinhado.

    ```C++
    D2D1_RECT_F rect = D2D1::RectF(
        0,
        underline->offset,
        underline->width,
        underline->offset + underline->thickness
        );
    ```

    

2.  Em seguida, crie um objeto [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) usando o método [**ID2D1Factory:: CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)) e a estrutura [**\_ \_ F Rect**](../direct2d/d2d1-rect-f.md) inicializada d2d1.

    ```C++
    ID2D1RectangleGeometry* pRectangleGeometry = NULL;
    hr = pD2DFactory_->CreateRectangleGeometry(
            &rect, 
            &pRectangleGeometry
            );
    ```

    

3.  Assim como acontece com a execução de glifos, a origem da geometria de sublinhado deve ser traduzida, com base nos valores de origem da linha de base, usando o método [**CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) .

    ```C++
    // Initialize a matrix to translate the origin of the underline
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );

    ID2D1TransformedGeometry* pTransformedGeometry = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pD2DFactory_->CreateTransformedGeometry(
            pRectangleGeometry,
            &matrix,
            &pTransformedGeometry
            );
    }
    ```

    

4.  Por fim, desenhe o contorno da geometria transformada e preencha-a usando os métodos [**ID2D1RenderTarget::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) e [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) e os pincéis de [Direct2D](../direct2d/direct2d-portal.md) armazenados como variáveis de membro.

    ```C++
        // Draw the outline of the glyph run
        pRT_->DrawGeometry(
            pTransformedGeometry,
            pOutlineBrush_
            );

        // Fill in the glyph run
        pRT_->FillGeometry(
            pTransformedGeometry,
            pFillBrush_
            );
    ```

    

5.  Agora que você terminou de desenhar, não se esqueça de limpar os objetos que foram criados nesse método.

    ```C++
    SafeRelease(&pRectangleGeometry);
    SafeRelease(&pTransformedGeometry);
    ```

    

O processo para desenhar um tachado é o mesmo. No entanto, o tachado terá um deslocamento diferente e provavelmente uma largura e uma espessura diferentes.

## <a name="pixel-snapping-pixels-per-dip-and-transform"></a>Encaixe de pixels, pixels por DIP e transformação

### <a name="ispixelsnappingdisabled"></a>IsPixelSnappingDisabled()

Esse método é chamado para determinar se o ajuste de pixel está desabilitado. O padrão recomendado é **false**, que é a saída deste exemplo.


```C++
*isDisabled = FALSE;
```



### <a name="getcurrenttransform"></a>GetCurrentTransform()

Este exemplo é renderizado para um destino de renderização Direct2D, portanto, encaminhe a transformação do destino render usando [**ID2D1RenderTarget:: GetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform).


```C++
//forward the render target's transform
pRT_->GetTransform(reinterpret_cast<D2D1_MATRIX_3X2_F*>(transform));
```



### <a name="getpixelsperdip"></a>GetPixelsPerDip()

Esse método é chamado para obter o número de pixels por DIP (pixel independente de dispositivo).


```C++
float x, yUnused;

pRT_->GetDpi(&x, &yUnused);
*pixelsPerDip = x / 96;
```



## <a name="drawinlineobject"></a>DrawInlineObject()

Um processador de texto personalizado também tem um retorno de chamada para desenhar objetos embutidos. Neste exemplo, [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) retorna E \_ NOTIMPL. Uma explicação de como desenhar objetos embutidos está além do escopo deste tutorial. Para obter mais informações, consulte o tópico [como adicionar objetos embutidos a um layout de texto](how-to-add-inline-objects-to-a-text-layout.md) .

## <a name="the-destructor"></a>O destruidor

É importante liberar todos os ponteiros que foram usados pela classe de processador de texto personalizado.


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
    SafeRelease(&pOutlineBrush_);
    SafeRelease(&pFillBrush_);
}
```



## <a name="using-the-custom-text-renderer"></a>Usando o renderizador de texto personalizado

Você renderiza com o renderizador personalizado usando o método [**bruto IDWriteTextLayout::D**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , que usa uma interface de retorno de chamada derivada de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) como um argumento, conforme mostrado no código a seguir.


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



O método [**RAW IDWriteTextLayout::D**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) chama os métodos do retorno de chamada do processador personalizado fornecido por você. Os métodos [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)e [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) descritos acima executam as funções de desenho.

 

 