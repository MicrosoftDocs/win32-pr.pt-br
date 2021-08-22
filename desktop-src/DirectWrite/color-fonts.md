---
title: Fontes de cores
description: Este tópico descreve fontes de cores, seu suporte DirectWrite e Direct2D e como usá-las em seu aplicativo.
ms.assetid: 74e096c4-9d1c-8854-e9ee-f8b11ac1c71a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5c0154e528ab8471d40f4771db5479ca9233320177386adbbd849162dbcd598
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329516"
---
# <a name="color-fonts"></a>Fontes de cores

Este tópico descreve fontes de cores, seu suporte DirectWrite e Direct2D e como usá-las em seu aplicativo.

Este documento contém as seguintes partes:

-   [O que são fontes de cores?](#what-are-color-fonts)
-   [Por que usar fontes de cores?](#why-use-color-fonts)
-   [A quais tipos de fontes de cores Windows suporte?](#what-kinds-of-color-fonts-does-windows-support)
-   [Usando fontes de cores](#using-color-fonts)
    -   [Usando fontes de cores em um aplicativo XAML](#using-color-fonts-in-a-xaml-app)
    -   [Usando fontes de cores em Microsoft Edge](#using-color-fonts-in-microsoft-edge)
    -   [Usando fontes de cores com DirectWrite e Direct2D](#using-color-fonts-with-directwrite-and-direct2d)
    -   [Usando fontes de cores com Win2D](#using-color-fonts-with-win2d)
-   [Tópicos relacionados](#related-topics)

## <a name="what-are-color-fonts"></a>O que são fontes de cores?

Fontes de cores, também conhecidas como fontes multicolorida ou fontes chromatic, são uma tecnologia de fonte que permite que os designers de fonte usem várias cores em cada glifo. As fontes de cores habilitam cenários de texto multicolorido em aplicativos e sites com menos código e suporte ao sistema operacional mais robusto do que as técnicas ad hoc implementadas acima do sistema de renderização de texto.

As fontes com as que você provavelmente está mais familiarizado não são fontes de cores. Essas fontes definem apenas a forma dos glifos que elas contêm, seja com contornos de vetor ou bitmaps monocromáticos. No momento do desenho, um renderador de texto preenche a forma de glifo usando uma única cor (a cor da fonte ) especificada pelo aplicativo ou documento que está sendo renderizado. As fontes de cores, por outro lado, contêm informações de cor além das informações de forma. Algumas abordagens permitem que os designers de fonte ofereçam várias paletas de cores, dando flexibilidade de flexibilidade de flexibilidade da fonte de cores.

O exemplo a seguir mostra um glifo da fonte Segoe UI de cores do Emoji. O glifo é renderizado em monocromático à esquerda e em cores à direita.

![Mostra glifos lado a lado, o glifo esquerdo renderizado em monocromático, a direita na fonte de cor do Emoji do Segoe U I.](images/color-font-cat.png)

As fontes de cores normalmente incluem informações de fallback para plataformas que não têm suporte para fontes de cores ou para cenários em que a funcionalidade de cor foi desabilitada. Nessas plataformas, as fontes de cores são renderizadas como fontes monocromáticas regulares.

## <a name="why-use-color-fonts"></a>Por que usar fontes de cores?

Historicamente, designers e desenvolvedores usaram uma variedade de técnicas para obter texto multicolorido. Por exemplo, os sites geralmente usam imagens de raster em vez de texto para exibir os headers rich. Essa abordagem permite flexibilidade abrangente, mas os gráficos de raster não são dimensionados bem para todos os tamanhos de exibição, nem fornecem os mesmos recursos de acessibilidade que o texto real. Outra técnica comum é sobrepor várias fontes monocromáticas em cores de fonte diferentes, mas isso normalmente requer código de layout extra para gerenciar.

As fontes de cores oferecem uma maneira de obter esses efeitos visuais com toda a simplicidade e a funcionalidade de fontes regulares. O texto renderizado em uma fonte de cor é o mesmo que outro texto: ele pode ser copiado e copiado, pode ser analisado por ferramentas de acessibilidade e assim por diante.

## <a name="what-kinds-of-color-fonts-does-windows-support"></a>A quais tipos de fontes de cores Windows suporte?

A [especificação OpenType](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) define várias maneiras de inserir informações de cor em uma fonte. A partir Windows 10 Atualização de Aniversário, DirectWrite e Direct2D (e as estruturas Windows criadas neles) são suportadas por todas essas abordagens. Eles são resumidos na tabela abaixo:



| Técnica                                                                                                                        | Descrição                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [COLR](/typography/opentype/spec/colr) / [Tabelas CPAL](/typography/opentype/spec/cpal) | Usa camadas de vetores coloridos, cujas formas são definidas da mesma maneira que contornos de glifo de cor única. **Observação:** Suporte a partir do Windows 8.1. <br/>                                                                                                                                                 |
| [Tabela SVG](/typography/opentype/spec/svg)                                                                 | Usa imagens de vetor feitas no formato Gráficos vetoriais escalonáveis. **Observação:** A partir Windows 10 De aniversário, DirectWrite dá suporte a um subconjunto da especificação SVG completa. Nem todo o conteúdo SVG é garantido para renderizar em uma fonte SVG OpenType. Confira [Suporte a SVG](../direct2d/svg-support.md) para obter mais detalhes. <br/> |
| [CBDT](/typography/opentype/spec/cbdt) / [Tabelas CBLC](/typography/opentype/spec/cblc) | Usa imagens de bitmap de cores inseridas.                                                                                                                                                                                                                                                                                |
| [tabela sbix](/typography/opentype/spec/sbix)                                                               | Usa imagens de bitmap de cores inseridas.                                                                                                                                                                                                                                                                                |



 

## <a name="using-color-fonts"></a>Usando fontes de cores

Da perspectiva do usuário, as fontes de cores são apenas fontes . Por exemplo, eles geralmente podem ser instalados e desinstalados do sistema da mesma maneira que fontes monocromáticas e são renderizados como texto regular e selecionável.

Da perspectiva do desenvolvedor também, as fontes de cores geralmente são usadas da mesma maneira que as fontes monocromáticas. Nas estruturas XAML e Microsoft Edge, você pode estilizar seu texto com fontes de cores da mesma forma que fontes regulares e, por padrão, seu texto será renderizado em cores. No entanto, se seu aplicativo chamar diretamente Direct2D APIs (ou APIs win2D) para renderizar texto, ele deverá solicitar explicitamente a renderização da fonte de cores.

### <a name="using-color-fonts-in-a-xaml-app"></a>Usando fontes de cores em um aplicativo XAML

Os elementos de texto da plataforma XAML (como [TextBlock,](/uwp/api/windows.ui.xaml.controls.textblock) [TextBox,](/uwp/api/windows.ui.xaml.controls.textbox) [RichEditBox,](/uwp/api/windows.ui.xaml.controls.richeditbox) [Glifos](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396)e [FontIcon)](/uwp/api/windows.ui.xaml.controls.fonticon)são suportados por padrão por fontes de cores. Basta estilizado o texto com uma fonte de cor e qualquer glifo de cor será renderizado em cores. O exemplo de código a seguir mostra uma maneira de estilar um TextBlock com uma fonte de cor empacotada com seu aplicativo. A mesma técnica se aplica a fontes regulares.


```XML
<TextBlock FontFamily="Assets/TMyColorFont.otf#MyFontFamilyName">Here is some text.</TextBlock>
```



Se você nunca quiser que o elemento de texto XAML renderizar texto multicolorido, defina sua propriedade [IsColorFontEnabledProperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) como false.

### <a name="using-color-fonts-in-microsoft-edge"></a>Usando fontes de cores em Microsoft Edge

As fontes de cores são renderizadas por padrão em sites e aplicativos Web em execução Microsoft Edge, incluindo o controle [WebView](/uwp/api/windows.ui.xaml.controls.webview) XAML. Basta usar HTML e CSS para estilizado seu texto com uma fonte de cor e qualquer glifo de cor será renderizado em cores.

### <a name="using-color-fonts-with-directwrite-and-direct2d"></a>Usando fontes de cores com DirectWrite e Direct2D

Seu aplicativo pode usar Direct2D métodos de desenho de texto de nível superior [**(DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) e [**DrawTextLayout)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)ou pode usar técnicas de nível inferior para desenhar as executações de glifo diretamente. Em ambos os casos, seu aplicativo requer alterações de código para manipular glifos de cor corretamente. Se seu aplicativo usar Direct2D APIs **DrawText** e **DrawTextLayout,** observe que elas não renderizarão glifos de cor por padrão. Isso é para evitar alterações inesperadas de comportamento em aplicativos de renderização de texto que foram projetados antes do suporte à fonte de cores.

Para optar pela renderização de glifo de cor, passe o sinalizador OPÇÕES DE TEXTO [**DE DESENHO D2D1 HABILITAR \_ FONTE \_ \_ \_ \_ \_ DE**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) COR para o método de desenho. O exemplo de código a seguir mostra como chamar Direct2D método DrawText para renderizar uma cadeia de caracteres em uma fonte de cor:


```C++
// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_defaultFillBrush. 
m_deviceContext->DrawText( 
    m_string->Data(), 
    m_string->Length(), 
    m_textFormat.Get(), 
    m_layoutRect, 
    m_defaultFillBrush.Get(), 
    D2D1_DRAW_TEXT_OPTIONS_ENABLE_COLOR_FONT 
    );  
    
```



Se seu aplicativo usar APIs de nível inferior para lidar com glifos executados diretamente, ele continuará a funcionar na presença de fontes de cores, mas não poderá desenhar glifos de cor sem lógica adicional.

Para lidar corretamente com glifos de cor, seu aplicativo deve:

1.  Passe as informações de run de glifo para [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), juntamente com um parâmetro [**DWRITE \_ LYPH \_ IMAGE \_ FORMATS**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) que indica quais tipos de glifo de cor o aplicativo está preparado para manipular. Se algum glifo de cor estiver presente (com base na fonte e nos FORMATOS de IMAGEM de **GLIFO de DWRITE \_ \_ \_ solicitados),** o DirectWrite dividirá o glifo primário em sequências de glifo de cor individuais que podem ser acessadas por meio do objeto [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) retornado na Etapa 4.
2.  Verifique o HRESULT retornado por [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) para determinar se foram detectadas quaisquer glifos de cor. Um **HRESULT** de **DWRITE \_ E \_ NOCOLOR** indica que não há nenhuma run de glifo de cor aplicável.
3.  Se [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) não relatou nenhuma sequência de glifo de cor (retornando **DWRITE \_ E \_ NOCOLOR),** toda a sequência de glifos será tratada como monocromática e seu aplicativo deverá desenhá-la conforme desejado (por exemplo, usando [**ID2D1DeviceContext::D rawGlyphRun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).
4.  Se [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) relatar a presença de glifo de cor executado, seu aplicativo deverá ignorar a sequência de glifo primário e, em vez disso, usar as run(s) de glifo de cor retornadas por TranslateColorGlyphRun. Para fazer isso, itere pelo objeto [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) retornado, recuperando cada glifo de cor e desenhando-o conforme apropriado para seu formato de imagem de glifo (por exemplo, você pode usar [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) e [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) para desenhar glifos de bitmap de cor e glifos SVG, respectivamente).

O exemplo de código a seguir mostra a estrutura geral deste procedimento:


```C++
// An example code snippet demonstrating how to use TranslateColorGlyphRun 
// to handle different kinds of color glyphs. This code does not make any 
// actual drawing calls. 
HRESULT DrawGlyphRun( 
    FLOAT baselineOriginX, 
    FLOAT baselineOriginY, 
    DWRITE_MEASURING_MODE measuringMode, 
    _In_ DWRITE_GLYPH_RUN const* glyphRun, 
    _In_ DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription, 
) 
{ 
    // Specify the color glyph formats your app supports. In this example, 
    // the app requests only glyphs defined with PNG or SVG. 
    DWRITE_GLYPH_IMAGE_FORMATS requestedFormats = 
        DWRITE_GLYPH_IMAGE_FORMATS_PNG | DWRITE_GLYPH_IMAGE_FORMATS_SVG; 

    ComPtr<IDWriteColorGlyphRunEnumerator1> glyphRunEnumerator; 
    HRESULT hr = m_dwriteFactory->TranslateColorGlyphRun( 
        D2D1::Point2F(baselineOriginX, baselineOriginY), 
        glyphRun, 
        glyphRunDescription, 
        requestedFormats, // the glyph formats supported by this renderer 
        measuringMode, 
        nullptr, 
        0, 
        &glyphRunEnumerator // on return, may contain color glyph runs 
        ); 

    if (hr == DWRITE_E_NOCOLOR) 
    { 
        // The glyph run has no color glyphs. Draw it as a monochrome glyph 
        // run, for example using the DrawGlyphRun method on a Direct2D 
        // device context. 
    } 
    else 
    { 
        // The glyph run has one or more color glyphs. 
        DX::ThrowIfFailed(hr); 

        // Iterate through the color glyph runs and draw them. 
        for (;;) 
        { 
            BOOL haveRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->MoveNext(&haveRun)); 
            if (!haveRun) 
            { 
                break; 
            } 

            // Retrieve the color glyph run. 
            DWRITE_COLOR_GLYPH_RUN1 const* colorRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->GetCurrentRun(&colorRun)); 

            // Draw the color glyph run depending on its format. 
            switch (colorRun->glyphImageFormat) 
            { 
            case DWRITE_GLYPH_IMAGE_FORMATS_PNG: 
                // Draw the PNG glyph, for example with 
                // ID2D1DeviceContext4::DrawColorBitmapGlyphRun. 
                break; 

            case DWRITE_GLYPH_IMAGE_FORMATS_SVG: 
                // Draw the SVG glyph, for example with 
                // ID2D1DeviceContext4::DrawSvgGlyphRun. 
                break; 

                // ...etc. 
            } 
        } 
    } 

    return hr; 
} 
```



### <a name="using-color-fonts-with-win2d"></a>Usando fontes de cores com Win2D

Semelhante ao Direct2D, as APIs de desenho de texto do Win2D não renderizarão glifos de cor por padrão. Para optar pela renderização de glifo de cor, de definir o sinalizador de opções [EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) no objeto de formato de texto que seu aplicativo passa para o método de desenho de texto. O exemplo de código a seguir mostra como renderizar uma cadeia de caracteres em uma fonte de cor usando Win2D:


```C++
// The text format that will be used to draw the text. (Declared elsewhere 
// and initialized elsewhere by the app to point to a color font.) 
CanvasTextFormat m_textFormat; 

// Set the EnableColorFont option. 
m_textFormat.Options = CanvasDrawTextOptions.EnableColorFont; 

// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_color. 
args.DrawingSession.DrawText( 
    m_string, 
    m_point, 
    m_color, 
    m_textFormat 
    ); 
```

## <a name="related-topics"></a>Tópicos relacionados

[DirectWrite exemplo de glifo colorido](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)


[**Interface IDWriteFontFace4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4)


[**Método IDWriteFactory4::TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)


[**Método ID2D1DeviceContext4::D rawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md)


 

