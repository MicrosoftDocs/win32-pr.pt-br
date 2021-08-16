---
title: Visão geral de API do Direct2D
description: Fornece uma visão geral do modelo Direct2D objeto.
ms.assetid: b1362ef6-40fc-4fa5-ba5b-22c622c39f04
keywords:
- Direct2D, sobre
- Direct2D, arquivos de header
- Direct2D,modelo de objeto
- Direct2D,interfaces
- Interface ID2D1Factory
- Direct2D, renderizar destinos
- destinos de renderização, sobre
- Direct2D, comandos de desenho
- renderizar destinos, comandos de desenho
- Direct2D, tratamento de erro
- renderizar destinos, tratamento de erros
- tratamento de erros
- pincéis
- renderizar destinos, pincéis
- geometries
- Direct2D, geometrias
- bitmaps para Direct2D
- Direct2D,bitmaps
- Primitives
- Direct2D,primitivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f318e3542d54ee92817193ef6b749a3ba1cf4678407ca7a12f28c6c187ae86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074990"
---
# <a name="direct2d-api-overview"></a>Visão geral de API do Direct2D

Direct2D fornece uma API, semelhante ao Direct3D, para uso com C ou C++. A API expõe uma variedade de funcionalidades relacionadas ao desenho:

-   Renderizar destinos para exibição e renderização fora da tela usando Direct2D, Direct3D ou GDI.
-   Objetos para gerenciar o estado de desenho, como transformaçãos de espaço de coordenadas e modos de aninhamento.
-   Representações para dados geométricos e funções para processamento de geometria.
-   Funcionalidade de renderização para bitmaps, geometrias e texto.
-   Provisionamentos para usar conteúdo gráfico criado usando GDI ou Direct3D.

Este tópico fornece uma visão geral dos objetos que compõe a API Direct2D dados. Ele contém as seções a seguir:

-   [Direct2D Arquivos de header](#direct2d-header-files)
-   [Direct2D Interfaces](#direct2d-interfaces)
-   [A interface ID2D1Factory](#the-id2d1factory-interface)
-   [Destinos de renderização](#render-targets)
    -   [Renderizar recursos de destino](#render-target-features)
    -   [Renderizar recursos de destino](#render-target-resources)
    -   [Comandos de desenho](#drawing-commands)
    -   [Tratamento de erro](#error-handling)
-   [Desenhando recursos](#drawing-resources)
    -   [Pincéis](#brushes)
    -   [Geometrias](#geometries)
    -   [Bitmaps](#bitmaps)
-   [Desenhando texto](#drawing-text)
-   [Direct2D Primitives](#direct2d-primitives)
-   [Tópicos relacionados](#related-topics)

## <a name="direct2d-header-files"></a>Direct2D Arquivos de header

A API Direct2D é definida pelos arquivos de header a seguir.

| Arquivo de cabeçalho         | Descrição                                                                                                                  |
|---------------------|------------------------------------------------------------------------------------------------------------------------------|
| d2d1.h              | Define as versões C e C++ da API Direct2D primária.                                                                      |
| d2d1helper.h        | Define funções, classes e estruturas auxiliares do C++.                                                                       |
| d2dbasetypes.h      | Define primitivos de desenho para Direct2D, como pontos e retângulos. Esse header está incluído com d2d1.h.                 |
| d2derr.h            | Define os códigos de erro para Direct2D. Esse header está incluído com d2d1.h.                                                   |
| d2d1 \_ 1.h           | Define as versões C e C++ da API Direct2D principal para Windows 8 e posteriores.                                              |
| d2d1 \_ 1helper.h     | Define funções auxiliares, classes e estruturas do C++ para Windows 8 e posteriores.                                               |
| d2d1effects.h       | Define as versões C e C++ da parte de efeitos da imagem da API Direct2D para Windows 8 e posterior.                            |
| d2d1effecthelpers.h | Define funções auxiliares, classes e estruturas do C++ da parte dos efeitos da imagem da API Direct2D para Windows 8 e posterior. |



 

Para usar Direct2D, seu aplicativo deve incluir o arquivo de header d2d1.h.

Para compilar um Direct2D, adicione d2d1.lib à lista de bibliotecas. Você pode encontrar d2d1.h e d2d1.lib [no Windows SDK (Software Development Kit) para Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).

As seções a seguir descrevem algumas das interfaces comuns fornecidas pela API Direct2D.

## <a name="direct2d-interfaces"></a>Direct2D Interfaces

Na raiz da API Direct2D estão as interfaces [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) e [**ID2D1Resource.**](/windows/win32/api/d2d1/nn-d2d1-id2d1resource) Um **objeto ID2D1Factory** cria **objetos ID2D1Resource** e serve como o ponto de partida para usar Direct2D. Todos os Direct2D objetos herdados da interface **ID2D1Resource.** Há dois tipos de recursos Direct2D: recursos independentes de dispositivo e recursos dependentes do dispositivo.

-   Recursos independentes de dispositivo não estão associados a um dispositivo de renderização específico e podem persistir durante a vida útil de um aplicativo.
-   Os recursos dependentes do dispositivo são associados a um dispositivo de renderização específico e deixarão de funcionar se esse dispositivo for removido.

(Para obter mais informações sobre recursos e compartilhamento de recursos, consulte Visão [geral de recursos](resources-and-resource-domains.md).)

## <a name="the-id2d1factory-interface"></a>A interface ID2D1Factory

A [**interface ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) é o ponto de partida para usar Direct2D. Você usa um **ID2D1Factory para** insinciar Direct2D recursos. Para criar um ID2D1Factory, use um dos [**métodos CreateFactory.**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory)

Uma fábrica define um conjunto de métodos Create *Resource* que podem produzir os seguintes recursos de desenho:

-   Destinos de renderização são objetos que renderizar comandos de desenho.
-   Os blocos de estado de desenho são objetos que armazenam informações de estado de desenho, como a transformação atual e o modo de aninhamento.
-   Geometrias são objetos que representam formas simples e potencialmente complexas.

Um dos objetos mais úteis que uma fábrica pode criar é [**o ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), descrito na seção a seguir.

## <a name="render-targets"></a>Destinos de renderização

Um destino de renderização é um recurso que herda da interface [**ID2D1RenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) Um destino de renderização cria recursos para desenho e executa operações de desenho. Há vários tipos de destinos de renderização que podem ser usados para renderizar gráficos das seguintes maneiras:

-   [**Objetos ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) renderizam conteúdo em uma janela.
-   [**Objetos ID2D1DCRenderTarget renderizar**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) em um contexto de dispositivo GDI.
-   Objetos de destino de renderização de bitmap renderizar conteúdo para um bitmap fora da tela.
-   Os objetos de destino de renderização do DXGI são rendertados em uma superfície DXGI para uso com o Direct3D.

Como um destino de renderização está associado a um dispositivo de renderização específico, ele é um recurso dependente do dispositivo e deixará de funcionar se o dispositivo for removido.

### <a name="render-target-features"></a>Renderizar recursos de destino

Você pode especificar se um destino de renderização deve usar a aceleração de hardware e se a exibição remota deve ser processada pelo computador local ou remoto. Os destinos de renderização podem ser configurados para renderização com alias ou AntiAlias. Para a renderização de cenas com um grande número de primitivos, um desenvolvedor também pode renderizar gráficos 2D no modo com alias e usar a suavização de vários exemplos do D3D para obter maior escalabilidade.

Os destinos de renderização também podem agrupar operações de desenho em camadas que são representadas pela interface [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) . As camadas são úteis para coletar operações de desenho a serem compostas ao renderizar um quadro. Para alguns cenários, isso pode ser uma alternativa útil para renderizar para um destino de renderização de bitmap e, em seguida, reutilizar o conteúdo do bitmap, já que os custos de alocação para a disposição em camadas são menores do que para um [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).

Os destinos de renderização podem criar novos destinos de renderização que são compatíveis com eles próprios, o que é útil para o processamento fora da tela intermediário enquanto retém as várias propriedades de destino de renderização que foram definidas no original.

também é possível renderizar usando GDI em um Direct2D de destino de renderização chamando [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) em um destino de renderização para [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), que tem os métodos [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) e [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) que podem ser usados para recuperar um contexto de dispositivo GDI. A renderização por meio de GDI só será possível se o destino de renderização tiver sido criado com o sinalizador de [**\_ uso de \_ destino \_ \_ \_ compatível com GDI do d2d1 render**](/windows/win32/api/d2d1/ne-d2d1-d2d1_render_target_usage) . isso é útil para aplicativos que são renderizados principalmente com Direct2D, mas têm um modelo de extensibilidade ou outro conteúdo herdado que requer a capacidade de renderizar com o GDI. para obter mais informações, consulte a [visão geral de interoperabilidade Direct2D e GDI](direct2d-and-gdi-interoperation-overview.md).

### <a name="render-target-resources"></a>Renderizar recursos de destino

Como uma fábrica, um destino de renderização pode criar recursos de desenho. Todos os recursos criados por um destino de renderização são recursos dependentes do dispositivo (assim como o destino de renderização). Um destino de renderização pode criar os seguintes tipos de recursos:

-   Bitmaps
-   Pincéis
-   Camadas
-   Malhas

### <a name="drawing-commands"></a>Comandos de desenho

Para renderizar o conteúdo, use os métodos de desenho de destino de renderização. Antes de começar a desenhar, chame o método [**ID2D1RenderTarget:: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) . Depois de terminar o desenho, chame o método [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Entre essas chamadas, você usa métodos Draw e Fill para renderizar recursos de desenho. A maioria dos métodos Draw e Fill pega uma forma (uma primitiva ou uma geometry) e um pincel para preencher ou estruturar a forma.

Os destinos de renderização também fornecem métodos para recorte, aplicação de máscaras de opacidade e transformação do espaço de coordenadas.

Direct2D usa um sistema de coordenadas à esquerda: valores positivos do eixo x passam para os valores do eixo y direito e positivo prosseguem para baixo.

### <a name="error-handling"></a>Tratamento de erros

Processar comandos de desenho de destino não indique se a operação solicitada foi bem-sucedida. Para descobrir se houve erros de desenho, chame o método de [**liberação**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) de destino render ou o método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) para obter um **HRESULT**.

## <a name="drawing-resources"></a>Recursos de desenho

As seções a seguir descrevem alguns dos recursos que podem ser criados pelo destino de renderização e pelas interfaces de fábrica.

### <a name="brushes"></a>Pincéis

Um pincel, representado pela interface [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) , é um recurso dependente de dispositivo, criado por um destino de renderização, que pinta uma área com sua saída. Pincéis diferentes têm tipos diferentes de saída. Alguns pincéis pintam uma área com uma cor sólida, outras com um gradiente ou uma imagem. Direct2D fornece quatro tipos de pincéis:

-   [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) pinta uma área com uma cor sólida.
-   [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) pinta uma área com um gradiente linear que mistura duas ou mais cores em uma linha, o eixo gradiente.
-   [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) pinta uma área com um gradiente radial que mistura duas ou mais cores em uma elipse.
-   [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) pinta uma área com um bitmap.

Para criar um pincel, use um dos métodos de pincel [**ID2D1RenderTarget::**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)Create *<Type>* , como [**CreateRadialGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)). Os pincéis podem ser usados com métodos de desenho e preenchimento de destino de renderização, para pintar um traço de forma ou estrutura de tópicos ou como uma máscara de opacidade.

Para obter mais informações sobre pincéis, consulte a [visão geral de pincéis](direct2d-brushes-overview.md).

### <a name="geometries"></a>Geometrias

além dos primitivos básicos de desenho, como pontos, retângulos e reticências, Direct2D fornece a interface [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) para descrever formas simples e complexas. As interfaces que herdam de **ID2D1Geometry** definem diferentes tipos de formas, como [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) para representar retângulos, [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) para representar retângulos arredondados e [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) para representar reticências.

Formas mais complexas podem ser criadas usando a interface [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) para especificar uma série de figuras compostas por linhas, curvas e arcos. O **ID2D1GeometrySink** é passado para o método Open de um [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) para gerar uma geometria complexa. [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) também pode ser usado com a API DirectWrite para extrair contornos de caminho de texto formatado para renderização artística.

As interfaces de geometria fornecem métodos para manipular formas ampliando ou simplificando geometrias existentes ou gerando a interseção ou União de várias geometrias. Eles também fornecem métodos para determinar se as geometrias estão se interseccionando ou se sobrepondo, recuperando informações associadas, computando a área ou o comprimento de uma geometria e interpolando os locais ao longo de uma geometria. Direct2D também fornece a capacidade de criar uma malha de triângulos que é mosaico de uma geometria.

Para criar uma geometria, use um dos métodos de geometria [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory):: Create *<Type>* , como [**createpathgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry). Uma geometria é um recurso independente de dispositivo.

Para renderizar uma geometria, você usa os métodos [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) e [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) de um destino de renderização.

Para obter mais informações sobre geometrias, consulte a [visão geral de geometrias](direct2d-geometries-overview.md).

### <a name="bitmaps"></a>Bitmaps

Direct2D não fornece métodos para carregar ou armazenar bitmaps; em vez disso, ele permite que você crie bitmaps usando o [Windows o componente de geração de imagens (WIC)](../wic/-wic-about-windows-imaging-codec.md). Os recursos de bitmap podem ser carregados usando o WIC e, em seguida, usados para criar um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) por meio do método [**ID2D1RenderTarget:: CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties_id2d1bitmap)) .

Os bitmaps também podem ser criados a partir de dados na memória que foram configurados por outros meios. Depois que um bitmap tiver sido criado, ele poderá ser desenhado pelo método [**DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) de destino render ou por um pincel de bitmap.

como a criação de recursos de bitmap em destinos de renderização de hardware geralmente é uma operação cara, Direct2D pode atualizar o conteúdo de um bitmap (ou parte do bitmap) usando os métodos [**CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap), [**CopyFromRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget)e [**CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory) . Usar esses métodos pode potencialmente salvar os custos associados a alocações de textura de GPU adicionais.

## <a name="drawing-text"></a>Texto de desenho

Direct2D foi projetado para trabalhar com as operações de texto da nova API de texto, DirectWrite. para tornar o uso da API DirectWrite mais simples, os destinos de renderização fornecem três métodos para processar DirectWrite recursos de texto: [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)e [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun). como Direct2D usa a GPU para o processo de renderização de texto ClearType, o Direct2D fornece menor uso de CPU do que o GDI para operações de texto e melhor escalabilidade, pois mais capacidade de processamento de GPU está disponível.

O [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) foi projetado para os cenários mais simples envolvendo a renderização de uma cadeia de caracteres de texto Unicode com formatação mínima. Layout mais complexo e flexibilidade tipográfica são fornecidos por meio do método [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , que usa um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) para especificar o conteúdo e a formatação a serem renderizados. O **IDWriteTextLayout** permite que você especifique a formatação individual para subcadeias de texto e outras opções de tipografia avançadas.

Para cenários em que o controle preciso do layout em nível de glifo é necessário, o método [**ID2D1RenderTarget::D rawglyphrun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) pode ser usado em conjunto com as facilidades de medida fornecidas pelo [DirectWrite](../directwrite/direct-write-portal.md).

para usar a API de DirectWrite, inclua o cabeçalho dwrite. h. como Direct2D, DirectWrite usa uma fábrica, [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) para criar objetos de texto. use a função [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) para criar uma fábrica e, em seguida, use seus métodos create para criar DirectWrite recursos (como [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))).

para obter mais informações sobre DirectWrite, consulte o tópico [introdução DirectWrite](../directwrite/introducing-directwrite.md) .

## <a name="direct2d-primitives"></a>Direct2D Primitivos

Direct2D define um conjunto de primitivos que são semelhantes aos fornecidos por outras APIs de desenho. Ele fornece uma estrutura de cores, uma estrutura de matriz para executar transformações e versões de ponto flutuante e inteiro de pontos, retângulos, elipses e estruturas de tamanho. Normalmente, você usa as versões de ponto flutuante dessas estruturas.

você não usa uma fábrica ou um destino de renderização para instanciar Direct2D primitivos. Você pode criá-los diretamente ou usar os métodos auxiliares definidos em d2d1helper. h para criá-los.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Direct2D Referência](reference.md)
</dt> <dt>

[DirectWrite Exemplo de Olá, Mundo](/samples/browse/?redirectedfrom=MSDN-samples)
</dt> <dt>

[Introdução ao DirectWrite](../directwrite/introducing-directwrite.md)
</dt> <dt>

[Visão geral de recursos](resources-and-resource-domains.md)
</dt> <dt>

[Windows Imaging Component (WIC)](../wic/-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 