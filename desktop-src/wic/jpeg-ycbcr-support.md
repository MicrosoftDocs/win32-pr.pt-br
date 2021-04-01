---
description: A partir do Windows 8.1, o codec JPEG do Windows Imaging Component (WIC) dá suporte à leitura e gravação de dados de imagem em seu formato YCbCr nativo.
ms.assetid: 50B89A96-72E8-4771-9109-207F4CDD06CB
title: Suporte a JPEG YCbCr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a8f05fe55e724a12513f24fc7401d277ebf097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921797"
---
# <a name="jpeg-ycbcr-support"></a>Suporte a JPEG YCbCr

A partir do Windows 8.1, o codec JPEG do [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) dá suporte à leitura e gravação de dados de imagem em seu formulário YC<sub>b</sub>C<sub>r</sub> nativo. O suporte do WIC YC<sub>b</sub>c<sub>r</sub> pode ser usado em conjunto com [Direct2D](../direct2d/direct2d-portal.md) para renderizar dados do YC<sub>b</sub>C<sub>r</sub> pixel com um efeito de imagem. Além disso, o codec JPEG WIC pode consumir dados YC<sub>b</sub>C<sub>r</sub> pixel produzidos por determinados drivers de câmera por meio de Media Foundation.

Os dados YC<sub>b</sub>C<sub>r</sub> pixel consumem significativamente menos memória do que os formatos de pixel BGRA padrão. Além disso, o acesso<sub>aos dados da</sub> YC<sub>b</sub>C permite descarregar alguns estágios do pipeline de decodificação/codificação JPEG em Direct2D que é acelerado por GPU. Usando o YC<sub>b</sub>C<sub>r</sub>, seu aplicativo pode reduzir o consumo de memória JPEG e tempos de carregamento para as mesmas imagens de tamanho e qualidade. Ou, seu aplicativo pode usar imagens JPEG mais de resolução mais alta sem sofrer penalidades de desempenho.

Este tópico descreve como os dados YC<sub>b</sub>C<sub>r</sub> funcionam e como usá-los no WIC e no Direct2D.

-   [Sobre dados JPEG YC<sub>b</sub>C<sub>r</sub>](#about-jpeg-ycbcr-data)
    -   [Modelo de cor do YC<sub>b</sub>C<sub>r</sub>](#ycbcr-color-model)
    -   [Layouts do planar versus de memória intercalada](#planar-versus-interleaved-memory-layouts)
    -   [Subamostragem croma](#chroma-subsampling)
    -   [Uso de JPEG de YC<sub>b</sub>C<sub>r</sub>](#jpeg-usage-of-ycbcr)
-   [Usando dados JPEG YC<sub>b</sub>C<sub>r</sub>](#using-jpeg-ycbcr-data)
    -   [Usando imagens YC<sub>b</sub>C<sub>r</sub> JPEG](#using-ycbcr-jpeg-images)
    -   [APIs do Windows Imaging Component](#windows-imaging-component-apis)
    -   [APIs do Direct2D](#direct2d-apis)
    -   [Determinando se há suporte para a configuração YC<sub>b</sub>C<sub>r</sub>](#determining-if-the-ycbcr-configuration-is-supported)
    -   [Decodificando dados de YC<sub>b</sub>C<sub>r</sub> pixel](#decoding-ycbcr-pixel-data)
    -   [Transformando dados de pixel YC<sub>b</sub>C<sub>r</sub>](#transforming-ycbcr-pixel-data)
    -   [Codificando dados de YC<sub>b</sub>C<sub>r</sub> pixel](#encoding-ycbcr-pixel-data)
    -   [Decodificando dados do YC<sub>b</sub>C<sub>r</sub> pixel no Windows 10](#decoding-ycbcr-pixel-data-in-windows-10)
-   [Tópicos relacionados](#related-topics)

## <a name="about-jpeg-ycsubbsubcsubrsub-data"></a>Sobre dados JPEG YC<sub>b</sub>C<sub>r</sub>

Esta seção explica alguns dos principais conceitos necessários para entender como o suporte a YC<sub>b</sub>C<sub>r</sub> no WIC funciona e seus principais benefícios.

### <a name="ycsubbsubcsubrsub-color-model"></a>Modelo de cor do YC<sub>b</sub>C<sub>r</sub>

O WIC no Windows 8 e versões anteriores oferecem suporte a quatro [modelos de cores](-wic-codec-native-pixel-formats.md)diferentes, o mais comum deles é o RGB/BGR. Esse modelo de cores define os dados de cores usando componentes vermelhos, verdes e azuis; um quarto componente alfa também pode ser usado.

Aqui está uma imagem decomposta em seus componentes vermelho, verde e azul.

![uma imagem decomposta em seus componentes vermelho, verde e azul.](graphics/ycbcr1.png)

O YC<sub>b</sub>C<sub>r</sub> é um modelo de cores alternativo que define os dados de cores usando um componente de luminância (Y) e dois componentes crominância (c<sub>b</sub> e c<sub>r</sub>). Ele é comumente usado em cenários de vídeo e geração de imagens digitais. O termo YC<sub>b</sub>C<sub>r</sub> geralmente é usado de forma intercambiável com YUV, embora os dois sejam tecnicamente distintos.

Há várias variações de YC<sub>b</sub>C<sub>r</sub> que diferem em espaço de cores e definições de intervalo dinâmico – o WIC dá suporte especificamente a dados JPEG JFIF YC<sub>b</sub>C<sub>r</sub> . Para obter mais informações, consulte a [especificação JPEG ITU-T81](https://www.w3.org/Graphics/JPEG/itu-t81.pdf).

Aqui está uma imagem decomposta em seus componentes Y, C<sub>b</sub>e c<sub>r</sub> .

![uma imagem decomposta em seus componentes y, CB e CR.](graphics/ycbcr2.png)

### <a name="planar-versus-interleaved-memory-layouts"></a>Layouts do planar versus de memória intercalada

Esta seção descreve algumas diferenças entre acessar e armazenar dados de pixel RGB na memória versus dados de YC<sub>b</sub>C<sub>r</sub> .

Os dados de pixel RGB normalmente são armazenados usando um layout de memória intercalada. Isso significa que os dados de um único componente de cor são intercalados entre os pixels e cada pixel é armazenado de forma contígua na memória.

Aqui está uma figura mostrando dados de pixels RGBA armazenados em um layout de memória intercalada.

![uma figura que mostra dados de pixel RGBA armazenados em um layout de memória intercalada.](graphics/ycbcr3.png)

Os dados YC<sub>b</sub>C<sub>r</sub> normalmente são armazenados usando um layout de memória do planar. Isso significa que cada componente de cor é armazenado separadamente em seu próprio plano contíguo, para um total de três planos. Em outra configuração comum, os componentes C<sub>b</sub> e c<sub>r</sub> são intercalados e armazenados juntos, enquanto o componente Y permanece em seu próprio plano, para um total de dois planos.

Veja a seguir uma figura que mostra dados de pixels de x<sub>b</sub>c<sub>r</sub> e intercalados, um layout comum de memória YC<sub>b</sub>c<sub>r</sub> .

![uma figura que mostra dados de pixel CbCr e intercalados do planar, um layout de memória YCbCr comum.](graphics/ycbcr4.png)

Tanto no WIC quanto no Direct2D, cada plano de cores é tratado como seu próprio objeto distinto (um [IWICBitmapSource](-wic-imp-iwicbitmapsource.md) ou [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)) e, coletivamente, esses planos formam os dados de backup de uma imagem do YC <sub>b</sub>C <sub>r</sub> .

Embora o WIC dê suporte ao acesso a dados de YC<sub>b</sub>C<sub>r</sub> nas configurações de 2 e 3 planos, o Direct2D dá suporte apenas ao primeiro (s e c<sub>b</sub><sub>r</sub>). Portanto, ao usar o WIC e o Direct2D juntos, você sempre deve usar a configuração de 2 planos YC<sub>b</sub>C<sub>r</sub> .

### <a name="chroma-subsampling"></a>Subamostragem croma

O modelo de cor YC<sub>b</sub>C<sub>r</sub> é adequado para cenários de geração de imagens digitais, pois pode tirar proveito de determinados aspectos do sistema visual humano. Em particular, os seres humanos são mais sensíveis a alterações na luminância (brilho) de uma imagem e menos sensíveis ao crominância (cor). Ao dividir os dados de cor em componentes de luminância e crominância separados, podemos compactar seletivamente apenas os componentes do crominância para obter economia de espaço com uma perda mínima de qualidade.

Uma técnica para fazer isso é chamada de subamostragem croma. Os planos C<sub>b</sub> e c<sub>r</sub> são subamostrados (downscaled) em uma ou ambas as dimensões horizontal e vertical. Por motivos históricos, cada modo de subamostragem croma é comumente referido usando uma proporção de três partes J:a: b.



| Modo de subamostragem | Diminuir horizontal | Diminuir vertical | Bits por pixel\* |
|------------------|----------------------|--------------------|------------------|
| 4:4:4            | 1x                   | 1x                 | 24               |
| 4:2:2            | 2                   | 1x                 | 16               |
| 4:4:0            | 1x                   | 2                 | 16               |
| 4:2:0            | 2                   | 2                 | 12               |



 

\* Inclui dados Y.

Na tabela acima, se você usar YC<sub>b</sub>C<sub>r</sub> para armazenar dados de imagem descompactados, poderá obter uma economia de memória de 25% a 62,5% versus 32 bits por pixel RGBA de dados, dependendo de qual modo de subamostragem croma é usado.

### <a name="jpeg-usage-of-ycsubbsubcsubrsub"></a>Uso de JPEG de YC<sub>b</sub>C<sub>r</sub>

Em um alto nível, o pipeline de descompactação JPEG consiste nos seguintes estágios:

1.  Executar a descompactação de entropia (por exemplo, Huffman)
2.  Executar desquantificação
3.  Executar transformação de cosseno discreto inverso
4.  Executar croma upamostragem em dados C<sub>b</sub>c<sub>r</sub>
5.  Converter dados YC<sub>b</sub>C<sub>r</sub> em RGBA (se necessário)

Fazendo com que o codec JPEG produza dados YC<sub>b</sub>C<sub>r</sub> , podemos evitar as duas etapas finais do processo de decodificação ou adie-las para a GPU. Além das economias de memória listadas na seção anterior, isso reduz significativamente o tempo geral necessário para decodificar a imagem. A mesma economia se aplicam ao codificar dados de YC<sub>b</sub>C<sub>r</sub> .

## <a name="using-jpeg-ycsubbsubcsubrsub-data"></a>Usando dados JPEG YC<sub>b</sub>C<sub>r</sub>

Esta seção explica como usar o WIC e o Direct2D para operar em dados do YC<sub>b</sub>C<sub>r</sub> .

Para ver as diretrizes deste documento usadas na prática, consulte o [exemplo de otimizações do JPEG YCbCr no Direct2D e o WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample) , que demonstra todas as etapas necessárias para decodificar e renderizar o conteúdo do YC<sub>b</sub>C<sub>r</sub> em um aplicativo Direct2D.

### <a name="using-ycsubbsubcsubrsub-jpeg-images"></a>Usando imagens YC<sub>b</sub>C<sub>r</sub> JPEG

A grande maioria das imagens JPEG é armazenada como YC<sub>b</sub>C<sub>r</sub>. Alguns JPEGs contêm dados CMYK ou tons de cinza e não usam YC<sub>b</sub>C<sub>r</sub>. Isso significa que você normalmente, mas nem sempre, pode usar diretamente conteúdo JPEG pré-existente sem nenhuma modificação.

O WIC e o Direct2D não dão suporte a todas as configurações de YC<sub>b</sub>c<sub>r</sub> possíveis e o suporte a YC<sub>b</sub>c<sub>r</sub> no Direct2D depende do driver e hardware de gráficos subjacentes. Por isso, um pipeline de geração de imagens de uso geral precisa ser robusto para imagens que não usam YC<sub>b</sub>C<sub>r</sub> (incluindo outros formatos de imagem comuns, como png ou bmp), ou para casos em que o suporte a C<sub>r</sub> do YC<sub>b</sub>não está disponível. Recomendamos que você mantenha seu pipeline de imagens baseado em BGRA existente e habilite o YC<sub>b</sub>C<sub>r</sub> como uma otimização de desempenho, quando disponível.

### <a name="windows-imaging-component-apis"></a>APIs do Windows Imaging Component

O WIC no Windows 8.1 adiciona três novas interfaces para fornecer acesso aos dados JPEG YC<sub>b</sub>C<sub>r</sub> .

### <a name="iwicplanarbitmapsourcetransform"></a>IWICPlanarBitmapSourceTransform

[**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) é análogo a [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), exceto pelo fato de que ele produz pixels em uma configuração de planar, incluindo dados de YC <sub>b</sub>C <sub>r</sub> . Você pode obter essa interface chamando QueryInterface em uma implementação de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) que dá suporte ao acesso planar. Isso inclui a implementação do codec JPEG de [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) , bem como [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)e [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform).

### <a name="iwicplanarbitmapframeencode"></a>IWICPlanarBitmapFrameEncode

O [**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) fornece a capacidade de codificar dados de pixel planar, incluindo dados do YC <sub>b</sub>C <sub>r</sub> . Você pode obter essa interface chamando QueryInterface na implementação do codec JPEG do [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).

### <a name="iwicplanarformatconverter"></a>IWICPlanarFormatConverter

[**IWICPlanarFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) permite que o [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) consuma dados de pixel planar, incluindo YC <sub>b</sub>C <sub>r</sub>, e converta-o em um formato de pixel intercalado. Ele não expõe a capacidade de converter dados de pixel intercalados em um formato planar. Você pode obter essa interface chamando QueryInterface na implementação fornecida pelo Windows do **IWICFormatConverter**.

### <a name="direct2d-apis"></a>APIs do Direct2D

Direct2D em Windows 8.1 dá suporte a dados de pixel do YC<sub>b</sub>c<sub>r</sub> com o novo efeito de imagem do YC<sub>b</sub>c<sub>r</sub> . Esse efeito fornece a capacidade de renderizar dados de YC<sub>b</sub>C<sub>r</sub> . O efeito usa como entrada duas interfaces [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) : uma contendo dados Y planar no formato \_ UNORM de R8 de formato dxgi \_ \_ e uma contendo dados intercalados de CbCr no formato \_ dxgi \_ R8G8 \_ UNORM. Normalmente, você usa esse efeito no lugar do **ID2D1Bitmap** que teria contido nos dados do BGRA pixel.

O efeito de imagem YC<sub>b</sub>c<sub>r</sub> deve ser usado em conjunto com as APIs do WIC YC<sub>b</sub>c<sub>r</sub> que fornecem os dados de YC<sub>b</sub>c<sub>r</sub> . Isso efetivamente atua para descarregar parte do trabalho de decodificação da CPU para a GPU, onde ela pode ser processada muito mais rapidamente e em paralelo.

### <a name="determining-if-the-ycsubbsubcsubrsub-configuration-is-supported"></a>Determinando se há suporte para a configuração YC<sub>b</sub>C<sub>r</sub>

Conforme observado anteriormente, seu aplicativo deve ser robusto para casos em que o suporte a YC<sub>b</sub>C<sub>r</sub> não está disponível. Esta seção aborda as condições que seu aplicativo deve verificar. Se qualquer uma das verificações a seguir falhar, seu aplicativo deverá retornar a um pipeline padrão baseado em BGRA.

### <a name="does-the-wic-component-support-ycsubbsubcsubrsub-data-access"></a>O componente do WIC dá suporte ao acesso a dados do YC<sub>b</sub>C<sub>r</sub> ?

Somente o codec JPEG fornecido pelo Windows e determinadas transformações de WIC dão suporte ao acesso a dados YC<sub>b</sub>C<sub>r</sub> . Para obter uma lista completa, consulte a seção [Windows Imaging Component APIs](#windows-imaging-component-apis) .

Para obter uma das interfaces planar YC<sub>b</sub>C<sub>r</sub> , chame QueryInterface na interface original. Isso falhará se o componente não oferecer suporte ao acesso a dados YC<sub>b</sub>C<sub>r</sub> .

### <a name="is-the-requested-wic-transform-supported-for-ycsubbsubcsubrsub"></a>A transformação de WIC solicitada tem suporte para o YC<sub>b</sub>C<sub>r</sub>?

Depois de obter um [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform), você deve primeiro chamar [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform). Esse método usa como parâmetros de entrada o conjunto completo de transformações que você deseja aplicar<sub>aos dados planar</sub> YC<sub>b</sub>C e retorna um valor booleano que indica suporte, bem como as dimensões mais próximas para o tamanho solicitado que pode ser retornado. Você deve verificar todos os três valores antes de acessar os dados de pixel com [**IWICPlanarBitmapSourceTransform:: CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels).

Esse padrão é semelhante a como o [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) é usado.

### <a name="does-the-graphics-driver-support-the-features-necessary-to-use-ycsubbsubcsubrsub-with-direct2d"></a>O driver de gráficos dá suporte aos recursos necessários para usar o YC<sub>b</sub>C<sub>r</sub> com Direct2D?

Essa verificação só será necessária se você estiver usando o efeito Direct2D YC<sub>b</sub>c<sub>r</sub> para renderizar o conteúdo do YC<sub>b</sub>c<sub>r</sub> . O Direct2D armazena dados de YC<sub>b</sub>C<sub>r</sub> usando os formatos de de \_ R8 de formato dxgi \_ \_ UNORM e dxgi \_ \_ R8G8 \_ UNORM de pixel, que não estão disponíveis em todos os drivers gráficos.

Antes de usar o efeito de imagem YC <sub>b</sub>C <sub>r</sub> , você deve chamar [**ID2D1DeviceContext:: IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) para garantir que os dois formatos tenham suporte do driver.

### <a name="sample-code"></a>Código de exemplo

Veja abaixo um exemplo de código que demonstra as verificações recomendadas. Este exemplo foi tirado das [otimizações JPEG YCbCr no exemplo de Direct2D e WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample).


```C++
bool DirectXSampleRenderer::DoesWicSupportRequestedYCbCr()
{
    ComPtr<IWICPlanarBitmapSourceTransform> wicPlanarSource;
    HRESULT hr = m_wicScaler.As(&wicPlanarSource);
    if (SUCCEEDED(hr))
    {
        BOOL isTransformSupported;
        uint32 supportedWidth = m_cachedBitmapPixelWidth;
        uint32 supportedHeight = m_cachedBitmapPixelHeight;
        DX::ThrowIfFailed(
            wicPlanarSource->DoesSupportTransform(
                &supportedWidth,
                &supportedHeight,
                WICBitmapTransformRotate0,
                WICPlanarOptionsDefault,
                SampleConstants::WicYCbCrFormats,
                m_planeDescriptions,
                SampleConstants::NumPlanes,
                &isTransformSupported
                )
            );

        // The returned width and height may be larger if IWICPlanarBitmapSourceTransform does not
        // exactly support what is requested.
        if ((isTransformSupported == TRUE) &&
            (supportedWidth == m_cachedBitmapPixelWidth) &&
            (supportedHeight == m_cachedBitmapPixelHeight))
        {
            return true;
        }
    }

    return false;
}

bool DirectXSampleRenderer::DoesDriverSupportYCbCr()
{
    auto d2dContext = m_deviceResources->GetD2DDeviceContext();

    return (d2dContext->IsDxgiFormatSupported(DXGI_FORMAT_R8_UNORM)) &&
        (d2dContext->IsDxgiFormatSupported(DXGI_FORMAT_R8G8_UNORM));
}
```



### <a name="decoding-ycsubbsubcsubrsub-pixel-data"></a>Decodificando dados de YC<sub>b</sub>C<sub>r</sub> pixel

Se você quiser obter dados de YC <sub>b</sub>C <sub>r</sub> pixel, deverá chamar [**IWICPlanarBitmapSourceTransform:: CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels). Esse método copia dados de pixel em uma matriz de estruturas [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) preenchidas, uma para cada plano de dados desejado (por exemplo, Y e c <sub>b</sub><sub>r</sub>). Um **WICBitmapPlane** contém informações sobre os dados de pixel e aponta para o buffer de memória que receberá os dados.

Se você quiser usar os dados do YC <sub>b</sub>C <sub>r</sub> pixel com outras APIs do WIC, você deve criar um [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)configurado adequadamente, chamar [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) para obter o buffer de memória subjacente e associar o buffer ao [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) usado para receber os dados do YC <sub>b</sub>C <sub>r</sub> pixel. Em seguida, você pode usar o [IWICBitmap](-wic-imp-iwicbitmapdecoder.md) normalmente.

Por fim, se você quiser renderizar os dados YC <sub>b</sub>C <sub>r</sub> em Direct2D, deverá criar um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) de cada [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) e usá-los como fonte para o efeito de imagem do YC <sub>b</sub>C <sub>r</sub> . O WIC permite que você solicite várias configurações de planar. Ao interoperar com o Direct2D, você deve solicitar dois planos, um usando \_ o GUID WICPixelFormat8bppY e o outro usando o GUID \_ WICPixelFormat16bppCbCr, pois essa é a configuração esperada por Direct2D.

### <a name="code-sample"></a>Exemplo de código

Veja abaixo um exemplo de código que demonstra as etapas para decodificar e renderizar dados YC<sub>b</sub>C<sub>r</sub> em Direct2D. Este exemplo foi tirado das [otimizações JPEG YCbCr no exemplo de Direct2D e WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample).


```C++
void DirectXSampleRenderer::CreateYCbCrDeviceResources()
{
    auto wicFactory = m_deviceResources->GetWicImagingFactory();
    auto d2dContext = m_deviceResources->GetD2DDeviceContext();

    ComPtr<IWICPlanarBitmapSourceTransform> wicPlanarSource;
    DX::ThrowIfFailed(
        m_wicScaler.As(&wicPlanarSource)
        );

    ComPtr<IWICBitmap> bitmaps[SampleConstants::NumPlanes];
    ComPtr<IWICBitmapLock> locks[SampleConstants::NumPlanes];
    WICBitmapPlane planes[SampleConstants::NumPlanes];

    for (uint32 i = 0; i < SampleConstants::NumPlanes; i++)
    {
        DX::ThrowIfFailed(
            wicFactory->CreateBitmap(
                m_planeDescriptions[i].Width,
                m_planeDescriptions[i].Height,
                m_planeDescriptions[i].Format,
                WICBitmapCacheOnLoad,
                &bitmaps[i]
                )
            );

        LockBitmap(bitmaps[i].Get(), WICBitmapLockWrite, nullptr, &locks[i], &planes[i]);
    }

    DX::ThrowIfFailed(
        wicPlanarSource->CopyPixels(
            nullptr, // Copy the entire source region.
            m_cachedBitmapPixelWidth,
            m_cachedBitmapPixelHeight,
            WICBitmapTransformRotate0,
            WICPlanarOptionsDefault,
            planes,
            SampleConstants::NumPlanes
            )
        );

    DX::ThrowIfFailed(d2dContext->CreateEffect(CLSID_D2D1YCbCr, &m_d2dYCbCrEffect));

    ComPtr<ID2D1Bitmap1> d2dBitmaps[SampleConstants::NumPlanes];
    for (uint32 i = 0; i < SampleConstants::NumPlanes; i++)
    {
        // IWICBitmapLock must be released before using the IWICBitmap.
        locks[i] = nullptr;

        // First ID2D1Bitmap1 is DXGI_FORMAT_R8 (Y), second is DXGI_FORMAT_R8G8 (CbCr).
        DX::ThrowIfFailed(d2dContext->CreateBitmapFromWicBitmap(bitmaps[i].Get(), &d2dBitmaps[i]));
        m_d2dYCbCrEffect->SetInput(i, d2dBitmaps[i].Get());
    }
}

void DirectXSampleRenderer::LockBitmap(
    _In_ IWICBitmap *pBitmap,
    DWORD bitmapLockFlags,
    _In_opt_ const WICRect *prcSource,
    _Outptr_ IWICBitmapLock **ppBitmapLock,
    _Out_ WICBitmapPlane *pPlane
    )
{
    // ComPtr guarantees the IWICBitmapLock is released if an exception is thrown.
    ComPtr<IWICBitmapLock> lock;
    DX::ThrowIfFailed(pBitmap->Lock(prcSource, bitmapLockFlags, &lock));
    DX::ThrowIfFailed(lock->GetStride(&pPlane->cbStride));
    DX::ThrowIfFailed(lock->GetDataPointer(&pPlane->cbBufferSize, &pPlane->pbBuffer));
    DX::ThrowIfFailed(lock->GetPixelFormat(&pPlane->Format));
    *ppBitmapLock = lock.Detach();
}
```



### <a name="transforming-ycsubbsubcsubrsub-pixel-data"></a>Transformando dados de pixel YC<sub>b</sub>C<sub>r</sub>

A transformação de dados YC <sub>b</sub>C <sub>r</sub> é quase idêntica à decodificação, pois ambos envolvem [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform). A única diferença é o objeto WIC do qual você obteve a interface. O dimensionador fornecido pelo Windows, o flip rotação e a transformação de cor dão suporte ao acesso de YC<sub>b</sub>C<sub>r</sub> .

### <a name="chaining-transforms-together"></a>Encadeamento de transformações em conjunto

O WIC dá suporte à noção de encadear várias transformações. Por exemplo, você pode criar o seguinte pipeline de WIC:

![um diagrama de um pipeline de WIC começando com um decodificador JPEG.](graphics/ycbcr5.png)

Em seguida, você pode chamar QueryInterface no [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) para obter [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform). A transformação de cor pode se comunicar com as transformações anteriores e pode expor os recursos agregados de cada estágio no pipeline. O WIC garante que os dados YC<sub>b</sub>C<sub>r</sub> sejam preservados por todo o processo. Esse encadeamento só funciona ao usar componentes que dão suporte ao acesso a YC<sub>b</sub>C<sub>r</sub> .

### <a name="jpeg-codec-optimizations"></a>Otimizações de codec JPEG

Semelhante à implementação de decodificação de quadros JPEG de [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), a implementação de decodificação de quadros JPEG do [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) dá suporte ao dimensionamento e à rotação de domínio JPEG DCT nativo. Você pode solicitar uma potência de dois diminuir ou uma rotação diretamente do decodificador JPEG. Isso normalmente resulta em maior qualidade e desempenho do que o uso de transformações discretas.

Além disso, quando você encadea uma ou mais transformações de WIC após o decodificador JPEG, ela pode aproveitar a escala e a rotação de JPEG nativa para atender à operação de agregação solicitada.

### <a name="format-conversions"></a>Conversões de formato

Use [**IWICPlanarFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) para converter dados de pixel planar YC <sub>b</sub>C <sub>r</sub> em um formato de pixel intercalado, como GUID \_ WICPixelFormat32bppPBGRA. O WIC no Windows 8.1 não fornece a capacidade de converter em um formato planar YC<sub>b</sub>C<sub>r</sub> pixel.

### <a name="encoding-ycsubbsubcsubrsub-pixel-data"></a>Codificando dados de YC<sub>b</sub>C<sub>r</sub> pixel

Use [**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) para codificar os dados do YC <sub>b</sub>C <sub>r</sub> pixel para o codificador JPEG. A codificação YC <sub>b</sub>C <sub>r</sub> data **IWICPlanarBitmapFrameEncode** é semelhante, mas não é idêntica à codificação de dados intercalados usando [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). A interface planar só expõe a capacidade de gravar dados de imagem de quadro planar, e você deve continuar usando a interface de codificação de quadros para definir metadados ou uma miniatura e para confirmar no final da operação.

Para o caso típico, você deve seguir estas etapas:

1.  Obtenha o [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) como normal. Se você quiser configurar a subamostragem croma, defina a opção de codificador [**JpegYCrCbSubsampling**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) ao criar o quadro.
2.  Se você precisar definir metadados ou uma miniatura, faça isso usando [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) como normal.
3.  QueryInterface para o [**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode).
4.  Defina os dados do YC <sub>b</sub>C <sub>r</sub> pixel usando [**IWICPlanarBitmapFrameEncode:: WriteName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writesource) ou [**IWICPlanarBitmapFrameEncode:: WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writepixels). Ao contrário de suas contrapartes de [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) , você fornece esses métodos com uma matriz de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) ou [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) que contêm os planos de pixels de YC <sub>b</sub>C <sub>r</sub> .
5.  Quando tiver terminado, chame [**IWICBitmapFrameEncode:: Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).

### <a name="decoding-ycsubbsubcsubrsub-pixel-data-in-windows-10"></a>Decodificando dados do YC<sub>b</sub>C<sub>r</sub> pixel no Windows 10

A partir do Windows 10 Build 1507, o Direct2D fornece o [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic), uma maneira mais simples de DEcodificar jpegs em Direct2D ao mesmo tempo em que aproveita as otimizações de YC <sub>b</sub>C <sub>r</sub> . O **ID2D1ImageSourceFromWic** executa automaticamente todas as verificações de funcionalidade do YC <sub>b</sub>C <sub>r</sub> necessárias para você; Ele usa o codepath otimizado quando possível e usa um fallback de outra forma. Ele também permite novas otimizações, como armazenar somente as subregiãos de cache da imagem que são necessárias por vez.

Para obter mais informações sobre como usar o [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic), consulte o [exemplo](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)de SDK de ajuste de foto do Direct2D.

## <a name="related-topics"></a>Tópicos relacionados

* [Otimizações de YCbCr JPEG no exemplo de Direct2D e WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample)
