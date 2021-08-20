---
description: Implementando IWICBitmapFrameDecode
ms.assetid: 7dc626ad-1158-4b67-8ca7-47b4cf88e278
title: Implementando IWICBitmapFrameDecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b49e3636f5d81202b1060d868ecb40bb99d095dd9f26b6afd0d40c5f5fd0d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205760"
---
# <a name="implementing-iwicbitmapframedecode"></a>Implementando IWICBitmapFrameDecode

## <a name="iwicbitmapframedecode"></a>Iwicbitmapframedecode

[**IWICBitmapFrameDecode é**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) a interface no nível do quadro que fornece acesso aos bits de imagem reais. Você implementa essa interface em sua classe de decodificação no nível do quadro. Como ele é derivado de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource), sua implementação de **IWICBitmapFrameDecode** incluirá uma implementação dos métodos **IWICBitmapSource.** Os métodos adicionais em **IWICBitmapFrameDecode** fornecem acesso à miniatura no nível do quadro, a qualquer contexto de cor para a imagem e ao leitor de consulta de metadados para o quadro.

``` syntax
interface IWICBitmapFrameDecode : IWICBitmapSource
{
// Required methods
HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
HRESULT GetColorContexts ( UINT cCount, 
IWICColorContext **ppIColorContexts, UINT *pcActualCount );
HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader );

// Methods inherited from IWICBitmapSource
HRESULT GetSize ( UINT *puiWidth, UINT *puiHeight );
HRESULT GetPixelFormat ( WICPixelFormatGUID *pPixelFormat );
HRESULT GetResolution ( double *pDpiX, double *pDpiY );
HRESULT CopyPixels ( const WICRect *prc, 
   UINT cbStride,
   UINT cbBufferSize, 
   BYTE *pbBuffer );
// Optional method
HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

-   [GetThumbnail](#getthumbnail)
-   [GetColorContexts](#getcolorcontexts)
-   [GetMetadataQueryReader](#getmetadataqueryreader)
-   [GetSize, GetPixelFormat e GetResolution](#getsize-getpixelformat-and-getresolution)
-   [Copypixels](#copypixels)
-   [CopyPalette](#copypalette)

### <a name="getthumbnail"></a>GetThumbnail

[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) retorna a miniatura do quadro atual. Por motivos de desempenho, as miniaturas são codificadas com mais comum em um formato JPEG. Assim como com a Versão Prévia no decodificador, não é necessário ou recomendado fornecer seu próprio decodificador JPEG para miniaturas. Em vez disso, você deve delegar ao decodificador JPEG fornecido Windows WIC (Componente de Imagens de Imagem).

Para obter mais informações sobre miniaturas, consulte o [método SetThumbnail](-wic-imp-iwicbitmapframeencode.md) em [Implementando IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md).

### <a name="getcolorcontexts"></a>GetColorContexts

[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) retorna os contextos de cor válidos (também conhecidos como perfis de cor) associados à imagem nesse quadro. Na maioria dos casos, isso será apenas um, mas pode haver casos em que há dois ou, raramente, mais. O chamador passará um ou mais objetos [**IWICColorContext,**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) definindo o parâmetro *cCount* para indicar quantos eles estão passando. Esse método popula os objetos **IWICColorContext** com os dados de contexto de cor reais para os perfis de cor associados à imagem. De definir *o parâmetro pcActualCount* para o número real de contextos de cor associados à imagem, mesmo que isso seja maior que o número que você pode retornar. (No caso em que mais contextos de cor estão disponíveis do que o número de objetos **IWICColorContext** passados pelo chamador, isso informa ao chamador que há um ou mais outros disponíveis.)

### <a name="getmetadataqueryreader"></a>GetMetadataQueryReader

[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) retorna [**um IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) que um aplicativo pode usar para recuperar metadados do quadro de imagem. Essa interface é implementada por um manipulador de metadados e permite que um aplicativo consulte propriedades de metadados específicas que pertencem a um formato de metadados específico. Para obter mais informações, [consulte Implementando IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md).

Para iniciá-lo em [**um IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), chame [**CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) no [**IWICComponentFactory.**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)


```C++
IWICMetadataQueryReader* pQueryReader = NULL;
HRESULT hr;

hr = m_pComponentFactory->CreateQueryReaderFromBlockReader( 
  static_cast<IWICMetadataBlockWriter*>(this),
  &pQueryReader);
```



### <a name="getsize-getpixelformat-and-getresolution"></a>GetSize, GetPixelFormat e GetResolution

[**GetSize,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)e [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) são autoexplicativos e retornam as propriedades solicitadas da imagem.

### <a name="copypixels"></a>Copypixels

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) é o método que um aplicativo chama quando deseja criar um bitmap na memória que pode ser renderizado para a exibição ou impressora. Esse é o método que faz a decodificação real dos bits de imagem. Os parâmetros são um retângulo, que representa a região de interesse na imagem de origem a ser copiada na memória; o stride, que especifica o número de bytes em uma linha de verificação; o tamanho do buffer na memória que foi alocado pelo aplicativo; e um ponteiro para o buffer no qual os bits de imagem solicitados devem ser copiados. (Para impedir que possíveis estouros de buffer introduzam vulnerabilidades de segurança, copie apenas a quantidade de dados de imagem no buffer que o parâmetro *cbBufferSize* especificar.)

### <a name="copypalette"></a>CopyPalette

Somente codecs que têm formatos de pixel indexados devem implementar o [**método CopyPalette.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) Se uma imagem usar um formato indexado, use esse método para retornar a paleta de cores usada na imagem. Se o codec não tiver um formato indexado, retorne WINCODEC \_ ERR \_ PALETTEUNAVAILABLE.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**Iwicbitmapsource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[**Iwicbitmapdecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**Iwicbitmapframedecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Implementando IWICBitmapSource](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[Implementando IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[Como escrever um codec WIC-Enabled código](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



