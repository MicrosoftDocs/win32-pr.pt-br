---
title: Compactação de bloco
description: Descreve como funciona a compactação de bloco e como usá-la em WIC e Direct2D.
ms.assetid: 52AF86A5-16E8-4AC8-BB67-CC2F1A3635B5
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: e8ee83911cc7be1ab6e611a735a7a5b3a7397c472b78e3192468d2e323ed0c4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331729"
---
# <a name="block-compression"></a>Compactação de bloco

a partir do Windows 8.1, o Direct2D dá suporte a vários formatos de pixel compactados de bloco. além disso, Windows 8.1 contém um novo codec dds (Windows Imaging Component) para habilitar o carregamento e o armazenamento de imagens compactadas em bloco no formato de arquivo DDS. A compactação de bloco é uma técnica para reduzir a quantidade de memória gráfica consumida pelo conteúdo de bitmap. Usando a compactação de bloco, seu aplicativo pode reduzir o consumo de memória e tempos de carregamento para as mesmas imagens de resolução. Ou, seu aplicativo pode usar imagens de resolução mais ou mais altas enquanto ainda estiver consumindo a mesma superfície de memória de GPU.

a compactação de bloco foi usada por aplicativos de Direct3D por um longo tempo e, com Windows 8.1, está disponível para os desenvolvedores de aplicativos mais importantes e Direct2D também.

Este tópico descreve como funciona a compactação de bloco e como usá-la em WIC e Direct2D.

## <a name="about-block-compression"></a>Sobre a compactação de bloco

A [compactação de bloqueio](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression) (BC) refere-se a uma classe de técnicas de compactação para reduzir os tamanhos de textura. O Direct3D 11 dá suporte a até 7 formatos de BC diferentes, dependendo do nível de recurso. no Windows 8.1 Direct2D apresenta suporte para os formatos BC1, BC2 e BC3 que estão disponíveis em todos os níveis de recurso.

### <a name="how-block-compression-works"></a>Como funciona a compactação de bloco

Todos os formatos compactados de bloco usam a mesma técnica básica para reduzir o espaço consumido pelos dados coloridos. Esta seção resume o algoritmo mais simples, BC1. Para obter uma explicação mais detalhada, consulte [Bloquear compactação](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11).

Primeiro, a imagem é dividida em blocos de 4 por 4 pixels. Cada bloco é compactado separadamente.

> [!Note]  
> Isso significa que a largura e a altura de uma imagem devem ser um múltiplo de 4 pixels para que ela seja bloqueada.

 

Esta imagem de exemplo mostra um bloco de pixel 4x4 dentro de uma imagem.

![uma imagem de exemplo mostra um bloco de pixel 4x4 dentro de uma imagem.](images/dds1.png)

Em seguida, dentro de um bloco 4 por 4, duas cores de "referência" são selecionadas e codificadas como valores de 2 16 bits (5 bits vermelho, 6 bits verde, 5 bits azul). A escolha dessas cores afeta significativamente a qualidade da imagem e não é trivial. Duas cores intermediárias são calculadas por interpolação linear entre as duas cores de referência no espaço de cores RGB. Isso produz um total de 4 cores possíveis diferentes; cada cor é atribuída a um valor de índice de dois bits. No entanto, observe que apenas as duas cores do ponto de extremidade precisam ser armazenadas conforme a interpolação é fixa.

Nesta figura, as cores 0 e 3 são selecionadas como cores de "referência" para o bloco, enquanto as cores 1 e 2 são calculadas usando interpolação linear.

![Diagrama que mostra o cálculo de 4 valores de cor para representar o bloco.](images/dds2.png)

Por fim, cada pixel no bloco é mapeado para uma das quatro cores calculadas anteriormente e cada pixel é codificado usando o valor de índice de dois bits.

A quantidade total de dados usados para representar esses 16 pixels é:

`16 bits [to define a reference color] * 2 + 2 bits * 16 [number of pixels]  = 64 bits`

Isso resulta em uma densidade média de 4 bits por pixel. Para comparação, o \_ \_ formato B8G8R8A8 UNORM pixel do formato dxgi comum \_ consome 32 bits por pixel.

Este diagrama mostra que cada pixel é codificado como um índice de 2 bits. O bloco inteiro é codificado em 64 bits.

![Calculando 4 valores de cor para representar o bloco.](images/dds3.png)

Há variações para dar suporte a dados alfa e números variados de canais de cor. BC6H e BC7 usam algoritmos significativamente diferentes para dar suporte ao conteúdo de intervalo dinâmico alto (HDR) e aumentar a qualidade da imagem, respectivamente.

### <a name="directdraw-surface-dds-file-format"></a>Formato de arquivo da superfície do DirectDraw (DDS)

Bloquear dados compactados normalmente são armazenados em arquivos de [superfície do DirectDraw (DDS)](/windows/desktop/direct3ddds/dx-graphics-dds-reference) . Você pode estar familiarizado com arquivos DDS se você for um desenvolvedor de Direct3D. observe que Direct2D dá suporte apenas a determinados recursos de DDS; para obter mais informações, consulte [requisitos de DDS](#dds-requirements).

### <a name="advantages-of-block-compression"></a>Vantagens da compactação de bloco

Os formatos compactados de bloco diferem dos formatos comuns de compactação de imagem do setor, como JPEG, nos formatos de BC com suporte nativo pelas GPUs modernas. Isso significa que você pode carregar diretamente uma imagem compactada de bloco na GPU sem qualquer decodificação ou descompactação. Os formatos de BC consomem de 4 a 8 bits por pixel em média; quando comparado a um bitmap típico descompactado de 32 bits por pixel BGRA, isso resulta na economia de memória de 75% a 87,5%. Além disso, como não há nenhuma etapa de decodificação, o tempo para carregar uma imagem de BC é significativamente reduzido em comparação com formatos como JPEG.

### <a name="when-to-use-block-compression"></a>Quando usar a compactação de bloco

Você deve considerar o uso de imagens compactadas em bloco em seu aplicativo, em vez de outros formatos, como JPEG, se quiser reduzir o consumo de memória de bitmaps ou se quiser reduzir os tempos de decodificação e carregamento.

No entanto, a compactação de bloco não é apropriada para todos os casos e requer algumas compensações. Primeiro, os algoritmos de compactação de bloco estão com perdas. A compactação de bloco funciona bem com conteúdo fotográfico natural, mas pode introduzir artefatos visuais indesejados em imagens com limites nítidos de alto contraste, como capturas de tela geradas por computador. Você deve garantir que seus ativos de imagem compactada em bloco tenham qualidade de imagem aceitável antes de usá-los.

Em segundo lugar, bloquear arquivos DDS compactados geralmente consome mais espaço em disco do que imagens JPEG comparáveis. Isso, por sua vez, aumentará o tamanho do pacote do aplicativo e os requisitos de largura de banda da rede.

## <a name="using-block-compression"></a>Usando compactação de bloco

esta seção explica como gerar e usar o bloqueio de ativos compactados em um aplicativo Direct2D.

### <a name="overview"></a>Visão geral

Bloquear arquivos DDS compactados são um formato otimizado para tempo de execução, o que significa que eles são especificamente otimizados para um bom desempenho no tempo de execução do aplicativo. Recomendamos que você continue a usar a criação de ativos e o pipeline de edição existentes e converta somente em um formato de bloco compactado ao importá-los para seu projeto de aplicativo ou em tempo de compilação.

### <a name="dds-requirements"></a>Requisitos de DDS

O formato de arquivo DDS foi projetado para dar suporte a uma ampla gama de recursos usados no Direct3D. Direct2D usa apenas um subconjunto desses recursos. portanto, ao criar imagens DDS para uso com Direct2D, você deve ter em mente as seguintes restrições:

-   Somente os seguintes valores de [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) são permitidos:
    -   \_Formato dxgi \_ BC1 \_ UNORM
    -   \_Formato dxgi \_ BC2 \_ UNORM
    -   \_Formato dxgi \_ BC3 \_ UNORM
-   Os dados alfa precalculados devem ser usados. Isso inclui arquivos DDS herdados usando formatos que definem explicitamente alfa (DXT1, DXT2, DXT4), bem como arquivos DDS que usam a \_ estrutura do cabeçalho DDS \_ DX10 com os \_ \_ \_ \_ \_ \_ valores precalculados do modo alfa do DDS opaco e DDS.
-   As dimensões X e Y devem ser múltiplos de 4 pixels.
-   As texturas de volume, cubemaps, mipmaps ou de textura não são permitidas. Você só deve usar imagens de origem de quadro único.

### <a name="generating-block-compressed-assets"></a>Gerando ativos compactados de bloco

Há uma variedade de ferramentas de criação de DDS disponíveis para criar ou converter arquivos DDS compactados de bloqueio. observação nem todas as ferramentas dão suporte aos requisitos de uso de arquivos DDS com Direct2D, conforme detalhado na seção anterior.

a partir do Visual Studio 2013, você pode fazer Visual Studio converter ativos visuais existentes, como JPEG e PNG, no formato de bloqueio de DDS correto como uma parte automática do seu processo de compilação. Isso é feito usando a etapa de compilação personalizada da tarefa conteúdo da imagem.

para obter informações sobre como configurar isso para seu projeto, consulte: [como exportar uma textura para uso com aplicativos Direct2D ou Javascipt](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120)).

### <a name="direct2d-apis"></a>Direct2D API

Direct2D é atualizado no Windows 8.1 para dar suporte aos seguintes formatos de pixel:

-   \_Formato dxgi \_ BC1 \_ UNORM
-   \_Formato dxgi \_ BC2 \_ UNORM
-   \_Formato dxgi \_ BC3 \_ UNORM

Para os formatos anteriores, você deve usar alfa-geomultiplicado. Além disso, esses formatos só são válidos para uso como origem, não como um destino. por exemplo, isso significa que você pode criar um Direct2D bitmap usando BC1, mas não um contexto de dispositivo.

os métodos a seguir são atualizados no Windows 8.1 para oferecer suporte aos formatos de BC:

-   [**ID2D1DeviceContext:: IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported)
-   [**ID2D1DeviceContext:: CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))
-   [**ID2D1DeviceContext:: CreateBitmapFromDxgiSurface**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1))
-   [**ID2D1RenderTarget:: CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)
-   [**ID2D1RenderTarget:: CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md)
-   [**ID2D1Bitmap::CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory)
-   [**ID2D1Bitmap::CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)
-   [**ID2D1Bitmap1:: getsurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-getsurface)

Observe que o [**CreateBitmapFromWicBitmap**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md) usa [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) como uma interface; no entanto, no Windows 8.1 o WIC não dá suporte à obtenção de dados compactados de bloqueio de **IWICBitmapSource**, e não há nenhum formato de pixel do wic correspondente ao \_ formato DXGI \_ BC1 \_ UNORM, etc. Em vez disso, **CreateBitmapFromWicBitmap** determina se **IWICBITMAPSOURCE** é um DDS [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) válido e carrega diretamente os dados compactados em bloco. você pode especificar explicitamente o formato de pixel no [**D2D1 \_ BITMAP \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) struct ou permitir que Direct2D determine automaticamente o formato correto.

### <a name="windows-imaging-component-apis"></a>Windows APIs do componente de geração de imagens

o Windows o componente de geração de imagens (WIC) adiciona um novo codec DDS no Windows 8.1. Além disso, ele adiciona novas interfaces que dão suporte ao acesso a dados específicos de DDS, incluindo dados de pixels compactados em bloco:

-   [**IWICDdsDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsdecoder)
-   [**IWICDdsEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsencoder)
-   [**IWICDdsFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode)

### <a name="block-compressed-wic-pixel-formats"></a>Bloquear formatos de pixel WIC compactados

Não há novos formatos de pixel compactados em bloco de WIC no Windows 8.1. Em vez disso, se você obtiver um [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) do decodificador DDS e chamar [**CopyPixels**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels), receberá pixels não compactados padrão, como WICPixelFormat32bppPBGRA. Você pode usar [**IWICDdsFrameDecode:: CopyBlocks**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsframedecode-copyblocks) para obter os dados compactados de blocos brutos na forma de um buffer de memória de um arquivo DDS.

### <a name="multi-frame-dds-access"></a>Acesso de DDS de vários quadros

O formato de arquivo DDS permite que várias imagens relacionadas sejam armazenadas em um único arquivo. Por exemplo, um arquivo DDS pode conter um cubemap, uma textura de volume ou uma matriz de textura, que pode ser mipmapped. No Direct3D, essas várias imagens são expostas como subrecursos. No WIC, várias imagens são expostas como quadros ([**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) e [**IWICBitmapFrameEncode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode)).

O WIC só dá suporte à noção de uma única matriz dimensional de quadros, enquanto o DDS dá suporte a três dimensões independentes (embora somente duas possam ser usadas em um arquivo). O WIC fornece métodos de conveniência para auxiliar no mapeamento entre um subrecurso DDS e um quadro WIC. Para decodificação, [**IWICDdsDecoder:: GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsdecoder-getframe) permite que você especifique o índice de matriz, o nível de MIP e o índice de fatia do subrecurso e retorna o quadro WIC correto.

Para codificação, [**IWICDdsEncoder:: CreateNewFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-createnewframe) computa o índice de matriz resultante, o nível de MIP e o índice de fatia quando você cria um novo quadro. Primeiro, você deve ter chamado [**IWICDdsEncoder:: Parameters**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-setparameters) para definir os parâmetros de arquivo específicos do DDS.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como exportar uma textura para uso com aplicativos Direct2D ou Javascipt](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120))
</dt> <dt>

[Referência para DDS](/windows/desktop/direct3ddds/dx-graphics-dds-reference)
</dt> <dt>

[Compactação de bloco](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)
</dt> </dl>

 

 