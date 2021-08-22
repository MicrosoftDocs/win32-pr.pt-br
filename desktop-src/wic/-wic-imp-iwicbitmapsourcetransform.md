---
description: Implementando IWICBitmapSourceTransform
ms.assetid: 6a3e682c-55c6-4728-9d14-5eb0290f3dcc
title: Implementando IWICBitmapSourceTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79caa17fdb874b9cbee73a9a371c4ba454e72c6eb249a6ca7d626fdd9c86aea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711071"
---
# <a name="implementing-iwicbitmapsourcetransform"></a>Implementando IWICBitmapSourceTransform

## <a name="iwicbitmapsourcetransform"></a>IWICBitmapSourceTransform

Embora seja opcional, é altamente recomendável que cada decodificador implemente essa interface em sua classe de decodificação no nível do quadro, pois ela pode fornecer grandes benefícios de desempenho. Quando um aplicativo solicita uma região específica de interesse, tamanho, orientação ou formato de pixel, em vez de apenas decodificar a imagem inteira em resolução completa e, em seguida, aplicar as transformação solicitadas, o WIC (componente de geração de imagens) do Windows chama [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para essa interface no objeto [**IWICBitmapFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) Se o decodificador de quadro oferecer suporte a ele, o WIC chamará o método ou os métodos apropriados para determinar se o decodificador de quadro pode executar a transformação solicitada ou determinar o tamanho ou o formato de pixel mais próximo que o decodificador pode fornecer ao solicitado. Se o decodificador puder executar a transformação ou as transformação solicitadas, o WIC invocará [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) com os parâmetros apropriados. Se o decodificador puder executar algumas, mas nem todas as transformação solicitadas, o WIC solicitará que o decodificador execute os objetos de transformação WIC ([**IWICBitmapScaler,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) [**IWICBitmapClipper,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)e [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) para executar as transformação restantes que não puderam ser executadas pelo decodificador de quadro no resultado da chamada **CopyPixels.** Se o decodificador não dá suporte a [**IWICBitmapSourceTransform,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)o WIC deve usar os objetos de transformação para executar todas as transformaçãos. Normalmente, é muito mais eficiente para o decodificador executar as transformação durante o processo de decodificação do que decodificar toda a imagem e, em seguida, executar as transformaçãos. Isso é especialmente verdadeiro para operações como dimensionamento para um tamanho muito menor ou conversões de formato de pixel.


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
-   [Copypixels](#copypixels)
-   [GetClosestSize](#getclosestsize)
-   [GetClosestPixelFormat](#getclosestpixelformat)

### <a name="doessupporttransform"></a>DoesSupportTransform

[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) pergunta se o decodificador dá suporte à operação de rotação ou invertida solicitada. As [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) que podem ser solicitadas são:


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



### <a name="copypixels"></a>Copypixels

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) executa o trabalho real de decodificação dos bits de imagem, como o método [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) na interface [**IWICBitmapSource,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) mas o método [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) em [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) é muito mais poderoso e pode melhorar significativamente o desempenho do processamento de imagem.

Quando várias operações de transformação são solicitadas, o resultado depende da ordem em que as operações são executadas. Para garantir a previsibilidade e a consistência entre codecs, é importante que todos os codecs executem essas operações na mesma ordem. Essa é a ordem canônica para executar essas operações.

1.  Escala
2.  Crop
3.  Rotate

A conversão de formato de pixel pode ser executada a qualquer momento, pois não tem efeito sobre as outras transformaçãos.

O primeiro parâmetro, *prcSrc,* é usado para especificar a região de interesse para cortar a imagem. Como o dimensionamento é executado antes do recorte por convenção, se a imagem deve ser dimensionada, bem como recortada, a região de interesse deve ser determinada depois que a imagem for dimensionada.

O segundo e o terceiro parâmetros indicam o tamanho para o qual dimensionar a imagem.

O *parâmetro pguidDstFormat* indica o formato de pixel solicitado para a imagem decodificada. Como o WIC já chamou [**GetClosestPixelFormat,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)esse deve ser um formato de pixel que o decodificador indicou que dá suporte.

O *parâmetro dstTransform* indica o ângulo de rotação solicitado e se a imagem deve ser in flip vertical, horizontal ou ambas. Novamente, como o WIC já terá chamado [**DoesSupportTransform,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)a transformação solicitada deve ser aquela à qual o decodificador já indicou que dá suporte. Lembre-se de que a rotação sempre deve ser executada após o dimensionamento e o recorte.

### <a name="getclosestsize"></a>GetClosestSize

[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) recebe dois parâmetros de saída/de saída. O chamador usa os *parâmetros puiWidth* e *puiHeight* para especificar o tamanho no qual o chamador prefere que a imagem seja decodificada. No entanto, um decodificador pode decodificar uma imagem apenas para um tamanho que seja um múltiplo de seu tamanho de DCT, e formatos de imagem diferentes podem ter tamanhos de DCT diferentes. O decodificador deve determinar, com base em seu próprio tamanho de DCT, quanto mais próximo ele puder chegar ao tamanho solicitado e definir *puiWidth* e *puiHeight* para essas dimensões no retorno. Se um tamanho maior for solicitado, mas o codec não dar suporte ao upscaling, o original deverá ser retornado.

### <a name="getclosestpixelformat"></a>GetClosestPixelFormat

[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) é usado para determinar o formato de pixel mais próximo ao formato de pixel solicitado que o decodificador pode fornecer sem perda de dados. É sempre preferível converter em um formato de pixel mais amplo do que um mais estreito, mesmo que aumente o tamanho da imagem, pois ela sempre poderá ser revertida para um formato mais restritivo, se necessário. No entanto, depois que os dados são perdidos, eles não podem ser recuperados.

## <a name="continued-reading"></a>Leitura contínua

Para saber mais sobre como criar um codec habilitado para WIC, consulte [Implementando IWICDevelopRaw](-wic-imp-iwicdevelopraw.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)
</dt> <dt>

[**Iwicmetadatablockreader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Implementando IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[Implementando IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[Como escrever um codec WIC-Enabled código](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
