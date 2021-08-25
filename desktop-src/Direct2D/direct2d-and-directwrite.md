---
title: renderização de texto com Direct2D e DirectWrite
description: ao contrário de outras APIs, como GDI, GDI+ ou WPF, Direct2D interopera com outra API, DirectWrite, para manipular e renderizar texto. Este tópico descreve os benefícios e a interoperação desses componentes separados.
ms.assetid: 1d5b8deb-34e2-433c-8de3-4ef66fb4e49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd95e7644b5f429d4dd91d2276213d5b7ffb92b058d8e530bfcf47fee77fea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698217"
---
# <a name="text-rendering-with-direct2d-and-directwrite"></a>renderização de texto com Direct2D e DirectWrite

ao contrário de outras APIs, como [GDI](/windows/desktop/gdi/windows-gdi), GDI+ ou WPF, [Direct2D](./direct2d-portal.md) interopera com outra API, [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), para manipular e renderizar texto. Este tópico descreve os benefícios e a interoperação desses componentes separados.

Este tópico inclui as seções a seguir.

-   [Direct2D Habilita a adoção incremental](#direct2d-enables-incremental-adoption)
-   [Serviços de texto versus renderização de texto](#text-services-versus-text-rendering)
-   [Glifos versus texto](#glyphs-versus-text)
-   [DirectWrite e Direct2D](#directwrite-and-direct2d)
    -   [DrawText](#drawtextlayout)
    -   [DrawTextLayout](#drawtextlayout)
    -   [DrawGlyphRun](#drawglyphrun)
-   [Renderização de glifo](#glyph-rendering)
-   [Conclusão](#conclusion)

## <a name="direct2d-enables-incremental-adoption"></a>Direct2D Habilita a adoção incremental

Mover um aplicativo de uma API de gráficos para outra pode ser difícil ou não o que você deseja por vários motivos. Isso pode ocorrer porque você precisa dar suporte a plug-ins que ainda usam as interfaces mais antigas, pois o próprio aplicativo é muito grande para portar para uma nova API em uma versão ou porque alguma parte da API mais recente é desejável, mas a API mais antiga está funcionando bem suficiente para outras partes do aplicativo.

como [Direct2D](./direct2d-portal.md) e [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) são implementados como componentes separados, você pode atualizar seu sistema de gráficos 2d inteiro ou apenas a parte do texto dele. por exemplo, você pode atualizar um aplicativo para usar DirectWrite para texto, mas ainda usar [GDI](/windows/desktop/gdi/windows-gdi) ou GDI+ para renderização.

## <a name="text-services-versus-text-rendering"></a>Serviços de texto versus renderização de texto

À medida que os aplicativos evoluíram, seus requisitos de processamento de texto cresceram cada vez mais complexos. A princípio, o texto geralmente estava confinado à interface do usuário com o layout estático, e o texto foi renderizado em uma caixa bem definida, como um botão. À medida que os aplicativos começaram a estar disponíveis em um número cada vez maior de linguagens, essa abordagem tornou-se mais difícil de sustentar, pois a largura e a altura do texto traduzido podem variar significativamente entre os idiomas. Para adaptar-se, os aplicativos começaram a definir dinamicamente sua interface do usuário para depender do tamanho real renderizado do texto, em vez do contrário.

para ajudar os aplicativos a concluir essa tarefa, [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) fornece a interface [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) . Essa API permite que um aplicativo especifique uma parte do texto com características complexas, como diferentes fontes e tamanhos de fonte, sublinhados, tachados, texto bidirecional, efeitos, reticências e até mesmo caracteres sem glifos incorporados (como um emoticon de bitmap ou um ícone). O aplicativo pode então alterar várias características do texto conforme ele determina iterativamente seu layout de interface do usuário. o [DirectWrite Olá, Mundo exemplo](/samples/browse/?redirectedfrom=MSDN-samples), que é mostrado na ilustração a seguir e no [Tutorial: Introdução com DirectWrite](/windows/desktop/DirectWrite/getting-started-with-directwrite) tópico mostra muitos desses efeitos.

![captura de tela do exemplo "Olá, mundo".](images/dwrite-hello-world.png)

O layout pode posicionar os glifos de maneira ideal com base em suas larguras (como o WPF faz), ou pode ajustar os glifos para as posições de pixel mais próximas (como a [GDI](/windows/desktop/gdi/windows-gdi) faz).

Além de obter medidas de texto, o aplicativo pode clicar em testar várias partes do texto. Por exemplo, talvez você queira saber que um hiperlink no texto é clicado. (Para obter mais informações sobre testes de clique, consulte o tópico [como executar testes de clique em um layout de texto](/windows/desktop/DirectWrite/how-to-perform-hit-testing-on-a-text-layout) .)

A interface de layout de texto é dissociada da API de renderização usada pelo aplicativo, como mostra o diagrama a seguir:

![layout de texto e diagrama de API de gráficos.](images/direct2d-directwrite1.png)

essa separação é possível porque DirectWrite fornece uma [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer)(interface de renderização) que os aplicativos podem implementar para renderizar texto usando qualquer API de gráficos que você desejar. o aplicativo implementou [**IDWriteTextRenderer::D**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) método de retorno de chamada rawglyphrun é chamado pelo DirectWrite ao renderizar um layout de texto. É responsabilidade desse método executar as operações de desenho ou passá-las.

para glifos de desenho, [Direct2D](./direct2d-portal.md) fornece [**ID2D1RenderTarget::D rawglyphrun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) para desenhar em uma superfície de Direct2D e [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) fornece [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) para desenhar em uma superfície GDI que pode ser transferida para uma janela usando GDI. convenientemente, **DrawGlyphRun** em ambos os Direct2D e DirectWrite têm parâmetros exatamente compatíveis para o método [**DrawGlyphRun**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) que o aplicativo implementa no [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer).

após uma separação semelhante, recursos específicos de texto (como enumeração de fontes e gerenciamento, análise de glifo e assim por diante) são tratados por [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) em vez de [Direct2D](./direct2d-portal.md). os objetos DirectWrite são aceitos diretamente pelo Direct2D. para ajudar os aplicativos GDI existentes a aproveitar o DirectWrite, ele fornece a interface do método [**IDWriteGdiInterop**](/windows/desktop/api/dwrite/nn-dwrite-idwritegdiinterop) com métodos para fazer o seguinte:

-   criar uma fonte de [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) de uma fonte lógica [GDI](/windows/desktop/gdi/windows-gdi) ([**CreateFontFromLOGFONT**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)).
-   converter de uma Face de fonte [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) para uma fonte lógica [GDI](/windows/desktop/gdi/windows-gdi) ([**ConvertFontFaceToLOGFONT**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)).
-   recupere a Face de fonte [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) a partir da que está selecionada em um HDC. ([**CreateFontFaceFromHdc**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc))
-   crie um [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) [**bitmap de renderização de destino**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) na memória do sistema ([**CreateBitmapRenderTarget**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget)).

## <a name="glyphs-versus-text"></a>Glifos versus texto

Texto é um conjunto de pontos de código Unicode (caracteres), com vários modificadores estilísticos (fontes, pesos, sublinhados, tachados e assim por diante) que são dispostos em um retângulo. Um glifo, por outro lado, é um índice específico em um arquivo de fonte específico. Um glifo define um conjunto de curvas que pode ser renderizado, mas não tem nenhum significado textual. Há potencialmente um mapeamento muitos para muitos entre glifos e caracteres. Uma sequência de glifos que vêm da mesma face de fonte e que são dispostos em sequência em uma linha de base é chamada de [GlyphRun](/windows/desktop/DirectWrite/glyphs-and-glyph-runs). ambos [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) e [Direct2D](./direct2d-portal.md) chamar suas [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) de API de renderização de glifo mais precisas e têm assinaturas muito semelhantes. O seguinte é de [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) no Direct2D:


```
STDMETHOD_(void, DrawGlyphRun)(
        D2D1_POINT_2F baselineOrigin,
        __in CONST DWRITE_GLYPH_RUN *glyphRun,
        __in ID2D1Brush *foregroundBrush,
        DWRITE_MEASURING_MODE measuringMode = DWRITE_MEASURING_MODE_NATURAL 
        ) PURE;
```



E esse método é de [**IDWriteBitmapRenderTarget**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) no [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal):


```
STDMETHOD(DrawGlyphRun)(
        FLOAT baselineOriginX,
        FLOAT baselineOriginY,
        DWRITE_MEASURING_MODE measuringMode,
        __in DWRITE_GLYPH_RUN const* glyphRun,
        IDWriteRenderingParams* renderingParams,
        COLORREF textColor,
        __out_opt RECT* blackBoxRect = NULL
        ) PURE;
```



a versão [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) mantém a origem da linha de base, o modo de medição e os parâmetros de execução de glifo e inclui parâmetros adicionais.

[DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) também permite que você use um renderizador personalizado para glifos implementando a interface [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) . Essa interface também tem um método **DrawGlyphRun** , como mostra o exemplo de código a seguir.


```
STDMETHOD(DrawGlyphRun)(
        __maybenull void* clientDrawingContext,
        FLOAT baselineOriginX,
        FLOAT baselineOriginY,
        DWRITE_MEASURING_MODE measuringMode,
        __in DWRITE_GLYPH_RUN const* glyphRun,
        __in DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription,
        __maybenull IUnknown* clientDrawingEffect
        ) PURE;
```



Essa versão inclui mais parâmetros que são úteis quando você implementa um [processador de texto personalizado](/windows/desktop/DirectWrite/how-to-implement-a-custom-text-renderer). O parâmetro final é usado para efeitos de desenho personalizados implementados pelo aplicativo. (Para obter mais informações sobre os efeitos de desenho do cliente, consulte [como adicionar efeitos de desenho de cliente a um layout de texto](/windows/desktop/DirectWrite/how-to-add-custom-drawing-efffects-to-a-text-layout).

Cada execução de glifo começa em uma origem e é colocada em uma linha que começa dessa origem. Os glifos são alterados pela transformação do mundo atual e pelas configurações de renderização de texto selecionadas no destino de renderização associado. Essa API é geralmente chamada diretamente apenas por aplicativos que fazem seu próprio layout (por exemplo, um processador de texto) ou por um aplicativo que implementou a interface [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) .

## <a name="directwrite-and-direct2d"></a>DirectWrite e Direct2D

o [Direct2D](./direct2d-portal.md) fornece serviços de renderização de nível de glifo por meio de [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun). No entanto, isso requer que o aplicativo implemente os detalhes de renderização, que basicamente reproduz a funcionalidade da API [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) do GDI por conta própria.

portanto, [Direct2D](./direct2d-portal.md) fornece APIs que aceitam texto em vez de glifos: [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) e [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)). os dois métodos são renderizados para uma superfície de Direct2D. Para renderizar em uma superfície GDI, [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) é fornecido. Mas esse método requer que um renderizador de texto personalizado seja implementado pelo aplicativo. (Para obter mais informações, consulte o tópico [renderizar em uma superfície GDI](/windows/desktop/DirectWrite/render-to-a-gdi-surface) .)

O uso de um aplicativo de texto normalmente começa simples: colocar **OK** ou **Cancelar** em um botão de layout fixo, por exemplo. No entanto, ao longo do tempo, ele se torna mais complexo como internacionalização e outros recursos são adicionados. eventualmente, muitos aplicativos terão que usar os objetos de layout de texto [do DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) e implementar o renderizador de texto.

portanto, o [Direct2D](./direct2d-portal.md) fornece APIs em camadas que permitem que um aplicativo seja iniciado simplesmente e cresça mais sofisticados sem precisar fazer o controle de versão ou abandonar seu código de trabalho. Uma exibição simplificada é mostrada no diagrama a seguir:

![diagrama de aplicativo DirectWrite e Direct2D.](images/direct2d-directwrite2.png)

### <a name="drawtext"></a>DrawText

O [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) é a mais simples das APIs a serem usadas. Ela usa uma cadeia de caracteres Unicode, um pincel de primeiro plano, um único objeto de formato e um retângulo de destino. Ele fará o layout e processará a cadeia de caracteres inteira dentro do retângulo de layout e, opcionalmente, o cortará. Isso é útil quando você coloca uma parte simples do texto em uma parte da interface do usuário de layout fixo.

### <a name="drawtextlayout"></a>DrawTextLayout

Ao criar um objeto [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) , um aplicativo pode começar a medir e organizar o texto e outros elementos da interface do usuário, além de dar suporte a várias fontes, estilos, sublinhados e tachados. [Direct2D](./direct2d-portal.md) fornece a API [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) que aceita esse objeto diretamente e renderiza o texto em um determinado ponto. (A largura e a altura são fornecidas pelo objeto de layout). além de implementar todos os recursos de layout de texto esperados, Direct2D irá interpretar qualquer objeto de efeito como um pincel e aplicar esse pincel ao intervalo selecionado de glifos. Ele também chamará todos os objetos embutidos. Em seguida, um aplicativo pode inserir caracteres sem glifo (ícones) no texto, se desejar. Outra vantagem de usar um objeto de layout de texto é que as posições de glifo são armazenadas em cache. Portanto, um grande lucro de desempenho é possível ao reutilizar o mesmo objeto de layout para várias chamadas de desenho e evitar recalcular as posições de glifo para cada chamada. Esse recurso não está presente para o [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))da GDI.

### <a name="drawglyphrun"></a>DrawGlyphRun

Por fim, o aplicativo pode implementar a própria interface [**IDWriteTextRenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) e chamar [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) e [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f_id2d1brush)) em si ou qualquer outra API de renderização. Toda a interação existente com o objeto de layout de texto permanecerá inalterada.

Para ver um exemplo de como implementar um renderador de texto personalizado, consulte o [tópico Renderizar usando um renderdor de texto](/windows/desktop/DirectWrite/how-to-implement-a-custom-text-renderer) personalizado.

## <a name="glyph-rendering"></a>Renderização de glifo

Adicionar [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) a um aplicativo GDI existente permite que o aplicativo use a API [**IDWriteBitmapRenderTarget**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) para renderizar glifos. O método [**IDWriteBitmapRenderTarget::D rawGlyphRun**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) que o DirectWrite fornece renderizará em cores sólidas para um DC de memória sem a necessidade de APIs adicionais, como Direct2D [.](./direct2d-portal.md)

Isso permite que o aplicativo obtenha recursos avançados de renderização de texto, como o seguinte:

-   O ClearType de sub pixel permite que um aplicativo coloque glifos em posições de sub pixel para permitir a renderização de glifo nítido e o layout de glifo.
-   A suavização de direção Y permite uma renderização mais suave de curvas em glifos maiores.

Um aplicativo que se move [para Direct2D](./direct2d-portal.md) também obterá os seguintes recursos:

-   Aceleração de hardware.
-   A capacidade de preencher texto com um pincel [de](./direct2d-portal.md) Direct2D arbitrário, como gradientes radiais, gradientes lineares e bitmaps.
-   Mais suporte para recortar em camadas e recorte por meio das APIs [**PushAxisAlignedClip,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e [**CreateCompatibleRenderTarget.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget))
-   A capacidade de dar suporte à renderização de texto em Escala de Cinza. Isso preenche corretamente o canal alfa de destino de acordo com a opacidade do pincel de texto e a aninhamento do texto.

Para dar suporte eficiente à aceleração de hardware, [Direct2D](./direct2d-portal.md) uma aproximação ligeiramente diferente da correção gama chamada *correção alfa.* Isso não requer que Direct2D o pixel de cor de destino de renderização ao renderizar texto.

## <a name="conclusion"></a>Conclusão

Este tópico explica as diferenças [](./direct2d-portal.md) e semelhanças entre Direct2D e [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) e as motivações de arquitetura para forneça-las como APIs separadas e cooperativas.

 

 