---
title: O que há de novo no Direct2D
description: Aqui estão algumas das novas adições a Direct2D.
ms.assetid: BA459FF0-9457-4652-A97C-BD4EC57EC8E2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 595a0833e88948585622d79907c81a1465e3fa7b11d1ebc8d6bbd697312509bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430466"
---
# <a name="whats-new-in-direct2d"></a>O que há de novo no Direct2D

Aqui estão algumas das novas adições a Direct2D.

## <a name="whats-new-for-windows-10-creators-update"></a>o que há de novo para Atualização do Windows 10 para Criadores

os seguintes recursos e APIs foram adicionados ou atualizados para Atualização do Windows 10 para Criadores.

### <a name="support-for-svg-image-rendering"></a>Suporte para renderização de imagem SVG

a partir do Atualização do Windows 10 para Criadores, o Direct2D fornece suporte para análise e desenho de imagens SVG, permitindo que os desenvolvedores processem ativos produzidos em suas ferramentas de arte de vetor favoritas sem convertê-los primeiro em imagens rasterizadas. use esse recurso para melhorar a superfície do disco e o comportamento de dimensionamento de seu iconografia no aplicativo e use as novas APIs do modelo de objeto SVG do Direct2D para fazer alterações programáticas no SVG do seu aplicativo. observe que Direct2D dá suporte apenas a um subconjunto limitado de SVG adequado para imagens e não oferece suporte a todos os recursos de desenho SVG. Se você precisar de compatibilidade de SVG de nível de navegador ou de recursos orientados pela Web do SVG, considere usar o [controle WebView XAML](/uwp/api/Windows.UI.Xaml.Controls.WebView) em vez disso. Para obter mais informações, consulte estes tópicos:

-   [Direct2D Exemplo de renderização de imagem SVG](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DSvgImage)
-   [Suporte a SVG](svg-support.md)
-   Método [**ID2D1DeviceContext5:: CreateSvgDocument**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createsvgdocument)
-   [**ID2D1DeviceContext5: método rawsvgdocument de:D**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-drawsvgdocument)
-   Interface [**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)

### <a name="improved-support-for-color-management"></a>Suporte aprimorado para gerenciamento de cores

a partir do Atualização do Windows 10 para Criadores, o Direct2D fornece recursos aprimorados de gerenciamento de cores. os desenvolvedores não precisam mais de um perfil ICC para usar o efeito de gerenciamento de cores do Direct2D; Agora eles podem usar espaços de cores DXGI ou construir sua própria definição de espaço de cores parametrizado. Para obter mais informações, consulte estes tópicos:

-   [Efeito de gerenciamento de cores](color-management.md)
-   [**ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace)
-   [**ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile_id2d1colorcontext1))

## <a name="whats-new-for-windows-10-anniversary-update"></a>o que há de novo para Windows 10 atualização de aniversário

os seguintes recursos e APIs foram adicionados ou atualizados para Windows 10 atualização de aniversário.

### <a name="improved-support-for-color-fonts"></a>Suporte aprimorado para fontes coloridas

a partir da atualização Windows 10 aniversário, Direct2D agora dá suporte à renderização de uma variedade maior de formatos de fonte de cor, permitindo que os desenvolvedores usem mais tipos de fontes em seus aplicativos com Direct2D do que nunca. Isso inclui suporte para:

-   A tabela OpenType ' COLR ', que habilita o conteúdo de vetor compacto em fontes. (Com suporte desde Windows 8.1.)
-   A tabela OpenType ' SVG ', que habilita o conteúdo SVG em fontes.
-   A tabela OpenType ' CBDT ', que permite o conteúdo de bitmap em cores em fontes.
-   A tabela OpenType ' sbix ', que permite o conteúdo de bitmap em cores em fontes.

o Direct2D dá suporte a esses formatos de fonte de cor automaticamente quando as [**\_ opções de texto de desenho D2D1 \_ \_ \_ habilitam \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_draw_text_options) o sinalizador de fonte de cor está habilitado. Para obter mais informações, consulte estes tópicos:

-   [Fontes de cores](/windows/desktop/DirectWrite/color-fonts)
-   [exemplo de glifo de cor DirectWrite](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)

### <a name="new-image-effects"></a>Novos efeitos de imagem

a partir da atualização Windows 10 aniversário, Direct2D inclui os efeitos AlphaMask, fading cruzado, opacidade e tonalidade. Essa funcionalidade estava disponível anteriormente de configurações específicas de efeitos Composite, ArithmeticComposite e ColorMatrix, mas os novos efeitos internos facilitam a tarefa de realizar essas operações comuns.

## <a name="whats-new-for-windows-10"></a>O que há de novo para Windows 10

Os seguintes recursos e APIs foram adicionados ou atualizados para Windows 10.

### <a name="sprite-batches"></a>Lotes de Sprite

a partir do Windows 10, o Direct2D fornece suporte para criar e renderizar lotes sprite. Em comparação com o método [**DrawImage**](id2d1devicecontext-drawimage-overload.md) de uso geral, os lotes Sprite incorrem muito menos a sobrecarga de CPU por imagem. Isso os torna ideais para cenários que envolvem centenas ou milhares de imagens simultâneas, como sprites de jogos ou sistemas de partículas. Para obter mais informações, consulte estes tópicos:

-   Método [**ID2D1DeviceContext3:: CreateSpriteBatch**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-createspritebatch)
-   [**ID2D1DeviceContext3:**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-drawspritebatch(id2d1spritebatch_id2d1bitmap_d2d1_bitmap_interpolation_mode_d2d1_sprite_options)) métodos de rawspritebatch de:D
-   Interface [**ID2D1SpriteBatch**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1spritebatch)

### <a name="gradient-meshes"></a>Malhas de gradiente

a partir do Windows 10, o Direct2D fornece um novo primitivo para malhas de gradiente. As malhas de gradiente são frequentemente usadas por Illustrators profissionais em software de design gráfico e permitem que os artistas processem formas multicoloridas complexas (mesmo foto-realística) com todos os benefícios de memória e escalabilidade de vetores. Para obter mais informações, consulte os seguintes tópicos:

-   [Amostra de malha de gradiente do Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DGradientMesh)
-   [**D2d1 \_ Estrutura \_ do \_ patch da malha de gradiente**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch)
-   [**ID2D1DeviceContext2: método rawgradientmesh de:D**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawgradientmesh)

### <a name="improved-image-loading-apis"></a>APIs de carregamento de imagem aprimoradas

a partir do Windows 10, o Direct2D oferece uma nova API para carregar imagens, ID2D1ImageSource. A origem da imagem melhora as APIs de carregamento de imagem existentes, incluindo CreateBitmapFromWicBitmap, o efeito de origem de bitmap e o efeito de YCbCr. a origem da imagem de Direct2D combina os recursos dessas APIs com suporte para imagens arbitrariamente grandes, fácil integração com impressão e efeitos e várias otimizações, incluindo jpeg YCbCr e jpeg indexado. Para saber mais, consulte esses tópicos:

-   [Direct2D Exemplo de SDK de ajuste de foto](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)
-   [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource)
-   [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)
-   [IWICJpegFrameDecode:: setindexing](/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-setindexing)

### <a name="improved-support-for-ink-rendering"></a>Suporte aprimorado para renderização de tinta

a partir do Windows 10, o Direct2D fornece um novo primitivo para representar traços de tinta. Direct2D traços de tinta são definidos por curvas de bézier, dão suporte a diferentes formas de nib e transformações e podem ter espessuras fixas ou variáveis. o suporte interno do Direct2D para traços de tinta permite que os aplicativos processem com facilidade uma tinta mais rápida e mais bonita do que as abordagens anteriores, que normalmente exigem que os aplicativos gerenciem a tinta em si, como uma série de reticências e quadrilaterals. Para obter mais informações, consulte estes tópicos:

-   [**Interface ID2D1Ink**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1ink)
-   [**ID2D1DeviceContext2: método rawInk de:D**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawink)
-   [**Interface ID2D1InkStyle**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1inkstyle)

### <a name="effect-shader-linking"></a>Vinculação de sombreador de efeito

Direct2D efeitos são implementados usando HLSL pixel, vértice e/ou sombreadores de computação. a partir do Windows 10, o Direct2D agora analisa automaticamente grafos de efeito para oportunidades de combinar e executar sombreadores individuais juntos. Isso pode fornecer um aumento significativo na taxa de transferência de efeito. Os consumidores de efeitos internos não precisam fazer nada para se beneficiar da vinculação de sombreador de efeito, mas os desenvolvedores que criam seus próprios efeitos personalizados devem seguir as práticas recomendadas atualizadas para aproveitar a vinculação de sombreador de efeito. Para obter mais informações, consulte estes tópicos:

-   [Vinculação de Sombreador de Efeito](effect-shader-linking.md)
-   [Direct2D Auxiliares de HLSL](hlsl-helpers.md)
-   [Direct2D exemplo de SDK de efeitos personalizados](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)

A vinculação de sombreador de efeito foi projetada para não afetar a saída Visual de efeitos. No entanto, isso nem sempre é possível devido ao comportamento específico em relação à precisão do efeito e ao recorte numérico. Para obter mais informações sobre como controlar esses comportamentos, consulte:

-   [Controlando a precisão e recorte numérico em grafos de efeito](precision-and-clipping-in-effect-graphs.md)

### <a name="new-built-in-effects"></a>Novos efeitos internos

a partir do Windows 10, o Direct2D inclui um conjunto avançado de novos efeitos internos que abordam as principais solicitações do desenvolvedor e permitem novos tipos de cenários visuais. Os novos efeitos são:

### <a name="color"></a>Cor:

-   [Efeito de RGB em matiz](rgb-to-hue-effect.md)
-   [Efeito de matiz para RGB](hue-to-rgb-effect.md)
-   [efeito de tabela de pesquisa 3D](3d-lookup-table-effect.md)

### <a name="photo"></a>Gráfico

-   [Efeito de contraste](contrast-effect.md)
-   [Efeito de exposição](exposure-effect.md)
-   [Efeito de escala de cinza](grayscale-effect.md)
-   [Efeito de realces e sombras](highlights-and-shadows-effect.md)
-   [Efeito Invert](invert-effect.md)
-   [Efeito sepia](sepia-effect.md)
-   [Efeito de ajuste](sharpen-effect.md)
-   [Efeito de ressarção](straighten-effect.md)
-   [Temperatura e efeito de tonalidade](temperature-and-tint-effect.md)
-   [Efeito Vigette](vignette-effect.md)

### <a name="filter"></a>Filtro:

-   [Efeito de detecção de borda](edge-detection-effect.md)

### <a name="stylize"></a>Stylize:

-   [Efeito emboss](emboss-effect.md)
-   [Efeito de cartaz](posterize-effect.md)

### <a name="transparency"></a>Transparência:

-   [Efeito Chroma-key](chromakey-effect.md)

As reações, saturação, contraste, realçamentos e sombras e efeitos de temperatura e tonalidade são demonstrados no [exemplo Direct2D SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)de Ajuste de Foto.

## <a name="whats-new-for-windows-81"></a>Novidades do Windows 8.1

Os seguintes recursos e APIs foram adicionados ou atualizados para Windows 8.1.

A partir Windows 8.1, Direct2D é criado com base no Direct3D 11.2.

### <a name="geometry-realizations"></a>Realizaçãos de geometria

Começando no Windows 8.1, Direct2D oferece realização de geometria. As realizaçãos de geometria permitem que os aplicativos melhorem o desempenho de renderização de geometria em determinadas situações, sem algumas das desvantagens do rasterização da geometria para um bitmap. Para obter mais informações, consulte estes tópicos:

-   [**Interface ID2D1Device1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1device1)
-   [**Método ID2D1DeviceContext1::D rawGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization)

### <a name="support-for-jpeg-ycbcr-images"></a>Suporte para imagens JPEG YCbCr

Começando no Windows 8.1, Direct2D dá suporte para renderizar dados de imagem no formato JPEG Y'CbCr. Os aplicativos podem renderizar o conteúdo JPEG em sua representação nativa do Y'CbCr em vez de descompactar para BGRA. Isso pode reduzir significativamente o consumo de memória de gráficos e o tempo de criação de recursos. Para obter mais informações, consulte estes tópicos:

-   Direct2D efeito [YCbCr](ycbcr-effect.md)
-   Interface [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)

### <a name="support-for-block-compressed-formats-dds-files"></a>Suporte para formatos compactados em bloco (arquivos DDS)

A partir do Windows 8.1, o Direct2D oferece suporte para bitmaps que contêm dados de pixel BC1 UNORM de FORMATO \_ \_ \_ DXGI, FORMATO DXGI \_ \_ BC2 \_ UNORM e FORMATO DXGI \_ \_ BC3 \_ UNORM. Os aplicativos podem substituir seus ativos de imagem por imagens DDS compactadas em bloco. Isso pode reduzir significativamente o consumo de memória de gráficos e o tempo de criação de recursos. Para obter mais informações, consulte estes tópicos:

-   [**Método ID2D1DeviceContext::CreateBitmapFromWicBitmap**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md)
-   Interface [**IWICDdsFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode)

### <a name="rendering-priority"></a>Prioridade de renderização

A partir do Windows 8.1, Direct2D dá suporte à prioridade de renderização por dispositivo. Esse novo recurso permite que os aplicativos alternem um dispositivo entre a prioridade de renderização normal (o padrão) e a baixa prioridade de renderização (na qual o dispositivo não bloqueará outras tarefas de renderização no sistema). É recomendável que os aplicativos usem baixa prioridade de renderização para tarefas que não são críticas para a capacidade de resposta do usuário, como pré-renderização de conteúdo, renderização enquanto minimizadas e outras operações que normalmente são executadas em segundo plano. Para obter mais informações, consulte estes tópicos:

-   [**Método ID2D1Device1::SetRenderingPriority**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1device1-setrenderingpriority)
-   [**D2D1 \_ Enumeração \_ RENDERING PRIORITY**](/windows/desktop/api/D2D1_2/ne-d2d1_2-d2d1_rendering_priority)

## <a name="whats-new-for-windows-8"></a>Novidades da Windows 8

Os seguintes recursos e APIs foram adicionados ou atualizados para Windows 8.

As novas Direct2D interfaces do Windows 7 têm suporte com a Atualização de Plataforma [para Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7) instalada.

A semântica do Direct2D para dispositivos e contextos de dispositivo foi atualizada para se parecer mais com a semântica usada pelo Direct3D e para fornecer uma operação concisa em aplicativos da Windows Store. Consulte [Dispositivos e contextos de dispositivo](devices-and-device-contexts.md) para obter mais informações.

APIs relacionadas selecionadas:

-   [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)
-   [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)

A API da lista de comandos permite que você compartilhe o caminho de renderização para na renderização e impressão da tela. Ele também permite que você use primitivos para criar um pincel de imagem para preencher primitivos.

APIs relacionadas selecionadas:

-   [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)
-   [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)
-   [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush)

[Direct2D efeitos é](effects-overview.md) um conjunto de APIs, novos Windows 8, para aplicar efeitos de alta qualidade a imagens. Ele também inclui APIs que permitem que você faça seus próprios efeitos personalizados.

APIs relacionadas selecionadas:

-   [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
-   [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl)
-   [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext)

Começando com Windows 8, Direct2D inclui APIs adicionais para a criação de aplicativos multithread. Consulte [Multithreaded Direct2D Apps](multi-threaded-direct2d-apps.md) para obter mais informações.

APIs relacionadas selecionadas:

-   [**ID2D1MultiThread**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1multithread)
-   [**D2D1 \_ FACTORY \_ TYPE \_ MULTI \_ THREADED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type)

 

 