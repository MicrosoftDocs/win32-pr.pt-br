---
title: Visão geral de API do Direct2D
description: fornece uma visão geral do modelo de objeto Direct2D.
ms.assetid: b1362ef6-40fc-4fa5-ba5b-22c622c39f04
keywords:
- Direct2D, sobre
- Direct2D, arquivos de cabeçalho
- Direct2D, modelo de objeto
- Direct2D, interfaces
- Interface ID2D1Factory
- Direct2D, processar destinos
- processar destinos, sobre
- Direct2D, comandos de desenho
- processar destinos, comandos de desenho
- Direct2D, tratamento de erro
- processar destinos, tratamento de erros
- tratamento de erros
- pincéis
- renderizar destinos, pincéis
- geometries
- Direct2D, geometrias
- bitmaps para Direct2D
- Direct2D, bitmaps
- primitivos
- Direct2Ds, primitivos
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

-   renderize destinos para exibição e renderização fora da tela usando Direct2D, Direct3D ou GDI.
-   Objetos para gerenciar o estado de desenho, como transformações de espaço de coordenadas e modos de suavização.
-   Representações para dados geométricos e funções para processamento de geometria.
-   Funcionalidade de renderização para bitmaps, geometrias e texto.
-   Provisiona para o uso de conteúdo gráfico criado usando GDI ou Direct3D.

este tópico fornece uma visão geral dos objetos que compõem a API do Direct2D. Ele contém as seções a seguir:

-   [Direct2D Arquivos de cabeçalho](#direct2d-header-files)
-   [Direct2D Interface](#direct2d-interfaces)
-   [A interface ID2D1Factory](#the-id2d1factory-interface)
-   [Destinos de renderização](#render-targets)
    -   [Recursos de destino de renderização](#render-target-features)
    -   [Renderizar recursos de destino](#render-target-resources)
    -   [Comandos de desenho](#drawing-commands)
    -   [Tratamento de erro](#error-handling)
-   [Recursos de desenho](#drawing-resources)
    -   [Pincéis](#brushes)
    -   [Geometrias](#geometries)
    -   [Bitmaps](#bitmaps)
-   [Texto de desenho](#drawing-text)
-   [Direct2D Primitivos](#direct2d-primitives)
-   [Tópicos relacionados](#related-topics)

## <a name="direct2d-header-files"></a>Direct2D Arquivos de cabeçalho

a API Direct2D é definida pelos seguintes arquivos de cabeçalho.

| Arquivo de cabeçalho         | Descrição                                                                                                                  |
|---------------------|------------------------------------------------------------------------------------------------------------------------------|
| d2d1. h              | define as versões C e C++ da API de Direct2D primária.                                                                      |
| d2d1helper. h        | Define as funções, classes e estruturas do auxiliar do C++.                                                                       |
| d2dbasetypes. h      | define primitivas de desenho para Direct2D, como pontos e retângulos. Esse cabeçalho é incluído com d2d1. h.                 |
| d2derr. h            | Define os códigos de erro para Direct2D. Esse cabeçalho é incluído com d2d1. h.                                                   |
| d2d1 \_ 1. h           | define as versões C e C++ da API de Direct2D primária para Windows 8 e posterior.                                              |
| d2d1 \_ 1helper. h     | define as funções, classes e estruturas do auxiliar do C++ para Windows 8 e posterior.                                               |
| d2d1effects. h       | define as versões C e C++ da parte de efeitos da imagem da API Direct2D para Windows 8 e posterior.                            |
| d2d1effecthelpers. h | define as funções, classes e estruturas do auxiliar do C++ da parte de efeitos da imagem da API de Direct2D para Windows 8 e posterior. |



 

para usar Direct2D, seu aplicativo deve incluir o arquivo de cabeçalho d2d1. h.

para compilar um aplicativo Direct2D, adicione d2d1. lib à lista de bibliotecas. você pode encontrar d2d1. h e d2d1. lib em [Windows Software Development Kit (SDK) para Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).

as seções a seguir descrevem algumas das interfaces comuns fornecidas pela API de Direct2D.

## <a name="direct2d-interfaces"></a>Direct2D Interface

na raiz da API de Direct2D estão as interfaces [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) e [**ID2D1Resource**](/windows/win32/api/d2d1/nn-d2d1-id2d1resource) . Um objeto **ID2D1Factory** cria objetos **ID2D1Resource** e serve como o ponto de partida para usar Direct2D. todos os outros objetos Direct2D herdam da interface **ID2D1Resource** . há dois tipos de recursos de Direct2D: recursos independentes de dispositivo e recursos dependentes de dispositivo.

-   Os recursos independentes de dispositivo não são associados a um determinado dispositivo de renderização e podem persistir durante o ciclo de vida de um aplicativo.
-   Os recursos dependentes do dispositivo são associados a um determinado dispositivo de renderização e deixam de funcionar se o dispositivo for removido.

(Para obter mais informações sobre recursos e compartilhamento de recursos, consulte a [visão geral de recursos](resources-and-resource-domains.md).)

## <a name="the-id2d1factory-interface"></a>A interface ID2D1Factory

A interface [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) é o ponto de partida para usar Direct2D. você usa um **ID2D1Factory** para instanciar Direct2D recursos. Para criar um ID2D1Factory, use um dos métodos [**CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) .

Uma fábrica define um conjunto de métodos Create *Resource* que podem produzir os seguintes recursos de desenho:

-   Os destinos de renderização são objetos que renderizam comandos de desenho.
-   Os blocos de estado de desenho são objetos que armazenam informações de estado de desenho, como o modo de transformação e de anti-aliasing atual.
-   As geometrias são objetos que representam formas simples e potencialmente complexas.

Um dos objetos mais úteis que uma fábrica pode criar é o [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), descrito na seção a seguir.

## <a name="render-targets"></a>Destinos de renderização

Um destino de renderização é um recurso que herda da interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) . Um destino de renderização cria recursos para desenhar e executar operações de desenho. Há vários tipos de destinos de renderização que podem ser usados para renderizar elementos gráficos das seguintes maneiras:

-   Os objetos [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) renderizam o conteúdo em uma janela.
-   Os objetos [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) são renderizados em um contexto de dispositivo GDI.
-   Os objetos de destino de renderização de bitmap renderizam conteúdo para um bitmap fora da tela.
-   Os objetos de destino de renderização DXGI são renderizados em uma superfície DXGI para uso com o Direct3D.

Como um destino de renderização é associado a um dispositivo de renderização específico, ele é um recurso dependente de dispositivo e deixa de funcionar se o dispositivo for removido.

### <a name="render-target-features"></a>Recursos de destino de renderização

Você pode especificar se um destino de renderização deve usar a aceleração de hardware e se a exibição remota deve ser renderizada pelo computador local ou remoto. Os destinos de renderização podem ser definidos para renderização suavizada ou com alias. Para renderizar cenas com um grande número de primitivos, um desenvolvedor também pode renderizar elementos gráficos 2D no modo com alias e usar a suavização multisample D3D para obter maior escalabilidade.

Destinos de renderização também podem agrupar operações de desenho em camadas representadas pela interface [**ID2D1Layer.**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) As camadas são úteis para coletar operações de desenho a serem compostas juntas ao renderizar um quadro. Para alguns cenários, isso pode ser uma alternativa útil para renderizar para um destino de renderização de bitmap e, em seguida, reutilizar o conteúdo do bitmap, pois os custos de alocação para o layering são menores do que para um [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).

Destinos de renderização podem criar novos destinos de renderização compatíveis com eles mesmos, o que é útil para renderização intermediária fora da tela, mantendo as várias propriedades de destino de renderização que foram definidas no original.

Também é possível renderizar usando GDI em um destino de renderização do Direct2D chamando [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) em um destino de renderização para [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), que tem [**métodos GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) e [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) que podem ser usados para recuperar um contexto de dispositivo GDI. A renderização por meio de GDI só será possível se o destino de renderização tiver sido criado com o sinalizador [**D2D1 \_ RENDER TARGET USAGE \_ \_ \_ GDI \_ COMPATIBLE**](/windows/win32/api/d2d1/ne-d2d1-d2d1_render_target_usage) definido. Isso é útil para aplicativos que renderizam principalmente com Direct2D mas têm um modelo de extensibilidade ou outro conteúdo herdado que exige a capacidade de renderizar com GDI. Para obter mais informações, consulte a [Visão geral Direct2D interoperabilidade de GDI e do Direct2D GDI.](direct2d-and-gdi-interoperation-overview.md)

### <a name="render-target-resources"></a>Renderizar recursos de destino

Como uma fábrica, um destino de renderização pode criar recursos de desenho. Todos os recursos criados por um destino de renderização são recursos dependentes do dispositivo (assim como o destino de renderização). Um destino de renderização pode criar os seguintes tipos de recursos:

-   Bitmaps
-   Pincéis
-   Camadas
-   Malhas

### <a name="drawing-commands"></a>Comandos de desenho

Para renderizar o conteúdo, use os métodos de desenho de destino de renderização. Antes de começar a desenhar, chame o [**método ID2D1RenderTarget::BeginDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) Depois de terminar de desenhar, chame o [**método ID2D1RenderTarget::EndDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) Entre essas chamadas, você usa os métodos Draw e Fill para renderizar recursos de desenho. A maioria dos métodos Draw e Fill tem uma forma (um primitivo ou uma geometria) e um pincel para preencher ou delinear a forma.

Destinos de renderização também fornecem métodos para recorte, aplicação de máscaras de opacidade e transformação do espaço de coordenadas.

Direct2D usa um sistema de coordenadas à esquerda: os valores positivos do eixo x vão para a direita e os valores positivos do eixo y prossestram para baixo.

### <a name="error-handling"></a>Tratamento de erros

Renderizar comandos de desenho de destino não indicam se a operação solicitada foi bem-sucedida. Para descobrir se houve erros de desenho, chame o método [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) de destino de renderização ou [**o método EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) para obter um **HRESULT.**

## <a name="drawing-resources"></a>Desenhando recursos

As seções a seguir descrevem alguns dos recursos que podem ser criados pelas interfaces de destino de renderização e de fábrica.

### <a name="brushes"></a>Pincéis

Um pincel, representado pela interface [**ID2D1Brush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) é um recurso dependente do dispositivo, criado por um destino de renderização, que pinta uma área com sua saída. Pincéis diferentes têm tipos diferentes de saída. Alguns pincéis pintam uma área com uma cor sólida, outros com um gradiente ou uma imagem. Direct2D fornece quatro tipos de pincéis:

-   [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) pinta uma área com uma cor sólida.
-   [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) pinta uma área com um gradiente linear que combina duas ou mais cores em uma linha, o eixo de gradiente.
-   [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) pinta uma área com um gradiente radial que combina duas ou mais cores em torno de uma elipse.
-   [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) pinta uma área com um bitmap.

Para criar um pincel, use um dos métodos [**ID2D1RenderTarget::**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)Create Brush, como *<Type>* [**CreateRadialGradientBrush.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) Os pincéis podem ser usados com um destino de renderização dos métodos Draw e Fill, para pintar um traço de forma ou contorno ou como uma máscara de opacidade.

Para obter mais informações sobre pincéis, consulte Visão [geral de pincéis.](direct2d-brushes-overview.md)

### <a name="geometries"></a>Geometrias

Além dos primitivos de desenho básicos, como pontos, retângulos e reellipses, o Direct2D fornece a interface [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) para descrever formas simples e complexas. Interfaces herdadas de **ID2D1Geometry** definem diferentes tipos de formas, como [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) para representar retângulos, [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) para representar retângulos arredondados e [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) para representar re elipses.

Formas mais complexas podem ser criadas usando a interface [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) para especificar uma série de figuras compostas por linhas, curvas e arcos. O **ID2D1GeometrySink** é passado para o método Open de [**um ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) para gerar uma geometria complexa. [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) também pode ser usado com a API do DirectWrite para extrair contornos de caminho de texto formatado para renderização de renderização de renderização.

As interfaces de geometria fornecem métodos para manipular formas ampliando ou simplificando geometrias existentes ou gerando a interseção ou a união de várias geometrias. Eles também fornecem métodos para determinar se as geometrias estão intersecções ou sobrepostas, recuperando informações de limites, computando a área ou o comprimento de uma geometria e interpolando locais ao longo de uma geometria. Direct2D também fornece a capacidade de criar uma malha de triângulos que é mosaico de uma geometria.

Para criar uma geometria, use um dos métodos [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)::Create *<Type>* Geometry, como [**CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry). Uma geometria é um recurso independente de dispositivo.

Para renderizar uma geometria, use os [**métodos DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) e [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) de um destino de renderização.

Para obter mais informações sobre geometrias, consulte a Visão [geral de geometrias.](direct2d-geometries-overview.md)

### <a name="bitmaps"></a>Bitmaps

Direct2D não fornece métodos para carregar ou armazenar bitmaps; em vez disso, ele permite que você crie bitmaps [usando o WIC (Windows Imaging Component).](../wic/-wic-about-windows-imaging-codec.md) Os recursos de bitmap podem ser carregados usando o WIC e usados para criar [**um ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) por meio do método [**ID2D1RenderTarget::CreateBitmapFromWicBitmap.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties_id2d1bitmap))

Os bitmaps também podem ser criados a partir de dados na memória que foram definidos por outros meios. Depois que um bitmap tiver sido criado, ele poderá ser desenhado pelo método [**DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) de destino de renderização ou com um pincel de bitmap.

Como a criação de recursos de bitmap em destinos de renderização de hardware geralmente é uma operação cara, o Direct2D pode atualizar o conteúdo de um bitmap (ou parte do bitmap) usando os métodos [**CopyFromBitmap,**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap) [**CopyFromRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget)e [**CopyFromMemory.**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory) O uso desses métodos pode potencialmente economizar os custos associados a alocações de textura de GPU adicionais.

## <a name="drawing-text"></a>Desenhando texto

Direct2D foi projetado para trabalhar com as operações de texto da nova API de texto, DirectWrite. Para simplificar o uso da API DirectWrite, os destinos de renderização fornecem três métodos para renderizar DirectWrite de texto: [**DrawText,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)e [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun). Como Direct2D usa a GPU para o processo de renderização de texto ClearType, o Direct2D fornece menor uso de CPU do que o GDI para operações de texto e melhor escalabilidade à medida que mais potência de processamento de GPU está disponível.

O [**ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) foi projetado para os cenários mais simples que envolvem renderizar uma cadeia de caracteres de texto Unicode com formatação mínima. O layout mais complexo e a flexibilidade tipográfica são fornecidos por meio do método [**ID2D1RenderTarget::D rawTextLayout,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) que usa um [**objeto IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) para especificar o conteúdo e a formatação a serem renderizados. **IDWriteTextLayout** permite que você especifique a formatação individual para substrings de texto e outras opções de tipografia avançadas.

Para cenários em que o controle preciso do layout no nível do glifo é necessário, o método [**ID2D1RenderTarget::D rawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) pode ser usado em conjunto com os recursos de medição fornecidos [pelo DirectWrite](../directwrite/direct-write-portal.md).

Para usar a API DirectWrite, inclua o header dwrite.h. Como Direct2D, DirectWrite usa uma fábrica, [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) para criar objetos de texto. Use a [**função DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) para criar uma fábrica e, em seguida, use seus métodos Create para criar DirectWrite recursos (como [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))).

Para obter mais informações sobre DirectWrite, consulte o [tópico Introducing DirectWrite.](../directwrite/introducing-directwrite.md)

## <a name="direct2d-primitives"></a>Direct2D Primitives

Direct2D define um conjunto de primitivos que são semelhantes aos fornecidos por outras APIs de desenho. Ele fornece uma estrutura de cores, uma estrutura de matriz para executar transformações e versões de ponto flutuante e inteiro de pontos, retângulos, reellipses e estruturas de tamanho. Normalmente, você usa as versões de ponto flutuante dessas estruturas.

Você não usa uma fábrica ou um destino de renderização para insinciar Direct2D primitivos. Você pode criar diretamente ou usar os métodos auxiliares definidos em d2d1helper.h para criar esses métodos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Direct2D Referência](reference.md)
</dt> <dt>

[DirectWrite Olá, Mundo exemplo](/samples/browse/?redirectedfrom=MSDN-samples)
</dt> <dt>

[Introdução DirectWrite](../directwrite/introducing-directwrite.md)
</dt> <dt>

[Visão geral de recursos](resources-and-resource-domains.md)
</dt> <dt>

[Windows Imaging Component (WIC)](../wic/-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 