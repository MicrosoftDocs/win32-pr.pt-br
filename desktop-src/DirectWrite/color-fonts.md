---
title: Fontes de cores
description: Este tópico descreve as fontes de cor, seu suporte no DirectWrite e Direct2D e como usá-las em seu aplicativo.
ms.assetid: 74e096c4-9d1c-8854-e9ee-f8b11ac1c71a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6774089cc1f0bed1349edc940c6a1ae715d052c7
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "104552983"
---
# <a name="color-fonts"></a>Fontes de cores

Este tópico descreve as fontes de cor, seu suporte no DirectWrite e Direct2D e como usá-las em seu aplicativo.

Este documento contém as seguintes partes:

-   [O que são fontes coloridas?](#what-are-color-fonts)
-   [Por que usar fontes de cores?](#why-use-color-fonts)
-   [A quais tipos de fontes de cores o Windows dá suporte?](#what-kinds-of-color-fonts-does-windows-support)
-   [Usando fontes de cores](#using-color-fonts)
    -   [Usando fontes de cores em um aplicativo XAML](#using-color-fonts-in-a-xaml-app)
    -   [Usando fontes de cores no Microsoft Edge](#using-color-fonts-in-microsoft-edge)
    -   [Usando fontes de cores com DirectWrite e Direct2D](#using-color-fonts-with-directwrite-and-direct2d)
    -   [Usando fontes de cores com Win2D](#using-color-fonts-with-win2d)
-   [Tópicos relacionados](#related-topics)

## <a name="what-are-color-fonts"></a>O que são fontes coloridas?

Fontes de cores, também conhecidas como fontes com várias cores ou fontes de desvio, são uma tecnologia de fonte que permite que os designers de fontes usem diversas cores dentro de cada glifo. Fontes de cores permitem cenários de texto multicolorido em aplicativos e sites com menos código e suporte a sistemas operacionais mais robustos do que as técnicas ad hoc implementadas acima do sistema de renderização de texto.

As fontes às quais você provavelmente está mais familiarizado não são fontes de cores. Essas fontes definem apenas a forma dos glifos que elas contêm, com contornos vetoriais ou bitmaps monocromáticas. No momento do desenho, um processador de texto preenche a forma de glifo usando uma única cor (a cor da fonte) especificada pelo aplicativo ou documento que está sendo renderizado. As fontes de cores, por outro lado, contêm informações de cores além das informações de forma. Algumas abordagens permitem que os designers de fontes ofereçam várias paletas de cores, dando a fonte de cor a flexibilidade artística.

O exemplo a seguir mostra um glifo da fonte de cor do Segoe UI Emoji. O glifo é renderizado no monocromático à esquerda e colorido à direita.

![Mostra glifos lado a lado, o glifo esquerdo renderizado em monocromático, o direito na fonte de cores Segoe U de Emoji.](images/color-font-cat.png)

As fontes de cores normalmente incluem informações de fallback para plataformas que não dão suporte a fontes de cores ou para cenários em que a funcionalidade de cores foi desabilitada. Nessas plataformas, as fontes de cores são renderizadas como fontes monodesvios regulares.

## <a name="why-use-color-fonts"></a>Por que usar fontes de cores?

Historicamente, designers e desenvolvedores usaram uma variedade de técnicas para obter texto multicolorido. Por exemplo, os sites geralmente usam imagens rasterizadas em vez de texto para exibir cabeçalhos ricos. Essa abordagem habilita a flexibilidade artística, mas os gráficos rasterizados não são bem dimensionados para todos os tamanhos de exibição, nem fornecem os mesmos recursos de acessibilidade que o texto real. Outra técnica comum é sobreposição de várias fontes monocromáticas em diferentes cores de fonte, mas isso normalmente requer um código de layout extra para gerenciar.

Fontes de cores oferecem uma maneira de atingir esses efeitos visuais com toda a simplicidade e funcionalidade de fontes regulares. O texto renderizado em uma fonte de cor é igual a outro texto: pode ser copiado e colado, pode ser analisado por ferramentas de acessibilidade e assim por diante.

## <a name="what-kinds-of-color-fonts-does-windows-support"></a>A quais tipos de fontes de cores o Windows dá suporte?

A [especificação OpenType](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) define várias maneiras de inserir informações de cor em uma fonte. A partir da atualização de aniversário do Windows 10, DirectWrite e Direct2D (e as estruturas do Windows criadas neles) dão suporte a todas essas abordagens. Eles são resumidos na tabela abaixo:



| Técnica                                                                                                                        | Descrição                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [COLR](/typography/opentype/spec/colr) / Tabelas [Cpal](/typography/opentype/spec/cpal) | Usa camadas de vetores coloridos, cujas formas são definidas da mesma maneira que os contornos de glifo de cor única. **Observação:** Com suporte a partir do Windows 8.1. <br/>                                                                                                                                                 |
| Tabela [SVG](/typography/opentype/spec/svg)                                                                 | Usa imagens vetoriais criadas no formato gráfico de vetor escalonável. **Observação:** A partir da atualização de aniversário do Windows 10, o DirectWrite dá suporte a um subconjunto da especificação SVG completa. Nem todo conteúdo SVG é garantido para renderizar em uma fonte de SVG OpenType. Consulte [suporte a SVG](../direct2d/svg-support.md) para obter mais detalhes. <br/> |
| [CBDT](/typography/opentype/spec/cbdt) / Tabelas [CBLC](/typography/opentype/spec/cblc) | Usa imagens de bitmap de cores inseridas.                                                                                                                                                                                                                                                                                |
| tabela [sbix](/typography/opentype/spec/sbix)                                                               | Usa imagens de bitmap de cores inseridas.                                                                                                                                                                                                                                                                                |



 

## <a name="using-color-fonts"></a>Usando fontes de cores

Da perspectiva do usuário, as fontes de cor são apenas fontes. Por exemplo, eles normalmente podem ser instalados e desinstalados do sistema da mesma forma que as fontes monocromáticas e são renderizados como texto comum e selecionável.

Da perspectiva do Developer s também, as fontes de cores geralmente são usadas da mesma maneira que as fontes monocromáticas. Nas estruturas XAML e Microsoft Edge, você pode estilizar o texto com fontes de cores da mesma maneira que as fontes regulares e, por padrão, o texto será renderizado em cores. No entanto, se seu aplicativo chama diretamente APIs Direct2D (ou APIs Win2D) para renderizar o texto, ele deve solicitar explicitamente a renderização de fonte de cor.

### <a name="using-color-fonts-in-a-xaml-app"></a>Usando fontes de cores em um aplicativo XAML

Os elementos de texto da plataforma XAML (como [TextBlock](/uwp/api/windows.ui.xaml.controls.textblock), [TextBox](/uwp/api/windows.ui.xaml.controls.textbox), [RichEditBox](/uwp/api/windows.ui.xaml.controls.richeditbox), [Glyphs](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396)e [FontIcon](/uwp/api/windows.ui.xaml.controls.fonticon)) dão suporte a fontes de cores por padrão. Basta estilizar o texto com uma fonte de cor e todos os glifos de cor serão renderizados em cores. O exemplo de código a seguir mostra uma maneira de estilizar um TextBlock com uma fonte de cor empacotada com seu aplicativo. A mesma técnica se aplica a fontes regulares.


```XML
<TextBlock FontFamily="Assets/TMyColorFont.otf#MyFontFamilyName">Here is some text.</TextBlock>
```



Se você nunca quiser que seu elemento de texto XAML processe texto multicolorido, defina sua propriedade [IsColorFontEnabledProperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) como false.

### <a name="using-color-fonts-in-microsoft-edge"></a>Usando fontes de cores no Microsoft Edge

As fontes de cores são renderizadas por padrão em sites e aplicativos Web em execução no Microsoft Edge, incluindo o controle [WebView](/uwp/api/windows.ui.xaml.controls.webview) XAML. Basta usar HTML e CSS para estilizar o texto com uma fonte de cor e todos os glifos de cor serão renderizados em cores.

### <a name="using-color-fonts-with-directwrite-and-direct2d"></a>Usando fontes de cores com DirectWrite e Direct2D

Seu aplicativo pode usar os métodos de desenho de texto de nível superior do Direct2D ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) e [**DrawTextLayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)) ou pode usar técnicas de nível inferior para desenhar diretamente os glifos. Em ambos os casos, seu aplicativo requer alterações de código para manipular os glifos de cor corretamente. Se seu aplicativo usar Direct2D de **DrawText** e APIs **DrawTextLayout** , observe que eles não renderizam glifos de cor por padrão. Isso é para evitar alterações de comportamento inesperadas em aplicativos de renderização de texto que foram criados antes do suporte à fonte de cores.

Para aceitar a renderização de glifo de cor, passe o sinalizador [**Opções de texto de desenho d2d1 habilitar opções de \_ \_ \_ \_ \_ \_ fonte de cor**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) para o método de desenho. O exemplo de código a seguir mostra como chamar o método DrawText Direct2D s para renderizar uma cadeia de caracteres em uma fonte de cor:


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



Se seu aplicativo usa APIs de nível inferior para manipular as execuções de glifos diretamente, ele continuará a funcionar na presença de fontes de cores, mas não poderá desenhar glifos de cor sem lógica adicional.

Para lidar corretamente com os glifos de cor, seu aplicativo deve:

1.  Passe as informações de execução de glifo para [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), juntamente com um parâmetro de [**formatos de \_ \_ imagem \_ de glifo DWRITE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) que indica que tipo (s) de glifo de cor o aplicativo está preparado para lidar. Se quaisquer glifos de cor estiverem presentes (com base na fonte e nos **\_ formatos de \_ imagem \_ de glifo DWRITE** solicitados), DirectWrite dividirá a execução do glifo primário em execuções de glifos de cores individuais que podem ser acessadas por meio do objeto [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) retornado na etapa 4.
2.  Verifique o HRESULT retornado por [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) para determinar se as execuções de glifo de cor foram detectadas. Um **HRESULT** de **DWRITE \_ E \_ nocolor** indica nenhuma execução de glifo de cor aplicável.
3.  Se [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) não reportou nenhuma execução de glifo de cor (retornando **DWRITE \_ E \_ nocolor**), a execução de glifo inteira será tratada como monodesvio e seu aplicativo deverá desenhá-lo conforme desejado (por exemplo, usando [**ID2D1DeviceContext::D rawglyphrun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).
4.  Se [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) reportar a presença de execuções de glifo de cor, seu aplicativo deverá ignorar a execução de glifo primário e, em vez disso, usar as execuções de glifo de cor retornadas por TranslateColorGlyphRun. Para fazer isso, itere o objeto [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) retornado, recuperando cada execução de glifo de cor e desenhando-o conforme apropriado para seu formato de imagem de glifo (por exemplo, você pode usar [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) e [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) para desenhar glifos de bitmap de cor e glifos SVG, respectivamente).

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

Semelhante ao Direct2D, as APIs de desenho de texto do Win2D não renderizam glifos de cores por padrão. Para aceitar a renderização de glifo de cor, defina o sinalizador de opções [EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) no objeto de formato de texto que seu aplicativo passa para o método de desenho de texto. O exemplo de código a seguir mostra como renderizar uma cadeia de caracteres em uma fonte de cor usando Win2D:


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

[Exemplo de glifo colorido DirectWrite](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)


[**Interface IDWriteFontFace4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4)


[**Método IDWriteFactory4:: TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)


[**ID2D1DeviceContext4: método rawText de:D**](../direct2d/id2d1devicecontext4-drawtext-overload.md)


 

