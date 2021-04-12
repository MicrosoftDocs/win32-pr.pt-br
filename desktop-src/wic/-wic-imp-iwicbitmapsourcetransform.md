---
description: Implementando IWICBitmapSourceTransform
ms.assetid: 6a3e682c-55c6-4728-9d14-5eb0290f3dcc
title: Implementando IWICBitmapSourceTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0809e1e56fe3c05c8803bb70106c4a24a466eafe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297086"
---
# <a name="implementing-iwicbitmapsourcetransform"></a>Implementando IWICBitmapSourceTransform

## <a name="iwicbitmapsourcetransform"></a>IWICBitmapSourceTransform

Embora opcional, é altamente recomendável que cada decodificador Implemente essa interface em sua classe de decodificação de nível de quadro, pois pode fornecer grandes benefícios de desempenho. Quando um aplicativo solicita uma região específica de interesse, tamanho, orientação ou formato de pixel, em vez de apenas decodificar a imagem inteira em resolução completa e, em seguida, aplicar as transformações solicitadas, o Windows Imaging Component (WIC) chama [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para essa interface no objeto [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) . Se o decodificador de quadro oferecer suporte a ele, o WIC chamará o método ou métodos apropriados para determinar se o decodificador de quadro pode executar a transformação solicitada ou determinar o tamanho ou o formato de pixel mais próximo que o decodificador pode fornecer para o solicitado. Se o decodificador puder executar a transformação ou transformações solicitadas, o WIC invocará [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) com os parâmetros apropriados. Se o decodificador puder executar algumas, mas não todas as transformações solicitadas, o WIC solicitará que o decodificador execute os que ele pode e use os objetos de transformação do WIC ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)e [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) para executar as transformações restantes que não puderam ser executadas pelo decodificador de quadro no resultado da chamada **CopyPixels** . Se o decodificador não oferecer suporte a [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), o WIC deverá usar os objetos de transformação para executar todas as transformações. Normalmente, é muito mais eficiente para o decodificador executar transformações durante o processo de decodificação do que decodificar a imagem inteira e, em seguida, executar as transformações. Isso é especialmente verdadeiro para operações como dimensionar para um tamanho muito menor ou conversões de formato de pixel.


```C++
interface IWICBitmapSourceTransform : IUnknown
{
   // Required methods
   HRESULT DoesSupportTransform ( WICTransformOptions dstTransform,
              BOOL *pfIsSupported);
   HRESULT CopyPixels ( WICRect *prcSrc, 
      UINT uiWidth, 
      UINT uiHeight,
      WICPixelFormatGUID * pguidDstFormat,
      WICBitmapTransformOptions dstTransform, 
      UINT nStride, 
      UINT cbBufferSize, 
      BYTE *pbBuffer );

   // Optional methods
   HRESULT GetClosestSize ( UINT *puiWidth,
              UINT *puiHeight);
   HRESULT GetClosestPixelFormat ( WICPixelFormatGUID *pguidDstFormat);
}
```



-   [DoesSupportTransform](#doessupporttransform)
-   [CopyPixels](#copypixels)
-   [GetClosestSize](#getclosestsize)
-   [GetClosestPixelFormat](#getclosestpixelformat)

### <a name="doessupporttransform"></a>DoesSupportTransform

[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) pergunta se o decodificador dá suporte à operação de rotação ou inversão solicitada. Os [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) que podem ser solicitados são:


```C++
enum WICBitmapTransformOptions
{   
   WICBitmapTransformRotate0,
   WICBitmapTransformRotate90,
   WICBitmapTransformRotate180,
   WICBitmapTransformRotate270,
   WICBitmapTransformFlipHorizontal,
   WICBitmapTransformFlipVertical
}
```



### <a name="copypixels"></a>CopyPixels

O [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) executa o trabalho real de decodificação dos bits de imagem, como o método [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) na interface [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , mas o método [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) em [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) é muito mais poderoso e pode melhorar significativamente o desempenho do processamento de imagens.

Quando várias operações de transformação são solicitadas, o resultado depende da ordem em que as operações são executadas. Para garantir a previsibilidade e a consistência entre codecs, é importante que todos os codecs executem essas operações na mesma ordem. Essa é a ordem canônica para executar essas operações.

1.  Escala
2.  Crop
3.  Rotate

A conversão de formato de pixel pode ser executada a qualquer momento, porque ela não tem nenhum efeito nas outras transformações.

O primeiro parâmetro, *prcSrc*, é usado para especificar a região de interesse para recortar a imagem. Como o dimensionamento é executado antes do recorte por convenção, se a imagem for dimensionada e recortada, a região de interesse deverá ser determinada depois que a imagem for dimensionada.

O segundo e o terceiro parâmetros indicam o tamanho para o qual dimensionar a imagem.

O parâmetro *pguidDstFormat* indica o formato de pixel solicitado para a imagem decodificada. Como o WIC já chamou [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat), ele deve ser um formato de pixel que o decodificador indicou que ele suporta.

O parâmetro *dstTransform* indica o ângulo de rotação solicitado e se deve virar a imagem verticalmente, horizontalmente ou ambas. Novamente, como o WIC já terá chamado [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform), a transformação solicitada deve ser aquela que o decodificador já indicou que ele suporta. Lembre-se de que a rotação sempre deve ser executada após o dimensionamento e o recorte.

### <a name="getclosestsize"></a>GetClosestSize

[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) usa dois parâmetros de entrada/saída. O chamador usa os parâmetros *puiWidth* e *puiHeight* para especificar o tamanho no qual o chamador prefere a imagem a ser decodificada. No entanto, um decodificador pode decodificar uma imagem apenas para um tamanho que seja um múltiplo de seu tamanho de DCT, e diferentes formatos de imagem podem ter tamanhos de DCT diferentes. O decodificador deve determinar, com base em seu próprio tamanho de DCT, o mais próximo que pode chegar ao tamanho solicitado e definir o *puiWidth* e *puiHeight* para essas dimensões no retorno. Se um tamanho maior for solicitado, mas o codec não der suporte ao upsizing, o original deverá ser retornado.

### <a name="getclosestpixelformat"></a>GetClosestPixelFormat

[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) é usado para determinar o formato de pixel mais próximo ao formato de pixel solicitado que o decodificador pode fornecer sem perda de dados. É sempre preferível converter para um formato de pixel mais largo do que um mais estreito, mesmo que ele aumente o tamanho da imagem, pois ela sempre poderá ser reconverteda para um formato mais restritivo, se necessário. No entanto, depois que os dados forem perdidos, eles não poderão ser recuperados.

## <a name="continued-reading"></a>Leitura continuada

Para saber mais sobre como criar um codec habilitado para WIC, consulte [implementando IWICDevelopRaw](-wic-imp-iwicdevelopraw.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)
</dt> <dt>

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Implementando o IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[Implementando IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
