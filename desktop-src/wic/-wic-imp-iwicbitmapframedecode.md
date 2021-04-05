---
description: Implementando IWICBitmapFrameDecode
ms.assetid: 7dc626ad-1158-4b67-8ca7-47b4cf88e278
title: Implementando IWICBitmapFrameDecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 394b5858ec5eee37ef1c7f52b766806c4a0c1a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662756"
---
# <a name="implementing-iwicbitmapframedecode"></a>Implementando IWICBitmapFrameDecode

## <a name="iwicbitmapframedecode"></a>IWICBitmapFrameDecode

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) é a interface de nível de quadro que fornece acesso aos bits de imagem reais. Você implementa essa interface em sua classe de decodificação de nível de quadro. Como ele é derivado de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource), sua implementação de **IWICBitmapFrameDecode** incluirá uma implementação dos métodos **IWICBitmapSource** . Os métodos adicionais em **IWICBitmapFrameDecode** fornecem acesso à miniatura de nível de quadro, qualquer contextos de cor para a imagem e o leitor de consulta de metadados para o quadro.

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
-   [GetSize, GetPixelFormat e Resolution](#getsize-getpixelformat-and-getresolution)
-   [CopyPixels](#copypixels)
-   [CopyPalette](#copypalette)

### <a name="getthumbnail"></a>GetThumbnail

[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) retorna a miniatura do quadro atual. Por motivos de desempenho, as miniaturas são geralmente codificadas em um formato JPEG. Assim como acontece com a visualização do decodificador, não é necessário ou recomendado fornecer seu próprio decodificador de JPEG para miniaturas. Em vez disso, você deve delegar ao decodificador de JPEG fornecido pelo Windows Imaging Component (WIC).

Para obter mais informações sobre miniaturas, consulte o método [SetThumbnail](-wic-imp-iwicbitmapframeencode.md) sobre [implementação de IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md).

### <a name="getcolorcontexts"></a>GetColorContexts

[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) retorna os contextos de cor válidos (também conhecidos como perfis de cor) associados à imagem neste quadro. Na maioria dos casos, isso só será um, mas pode haver casos em que há dois ou, raramente, mais. O chamador passará um ou mais objetos [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) , definindo o parâmetro *conta* para indicar quantos eles estão passando. Esse método popula os objetos **IWICColorContext** com os dados de contexto de cor reais para os perfis de cor associados à imagem. Defina o parâmetro *pcActualCount* como o número real de contextos de cor associados à imagem, mesmo que isso seja maior que o número que você pode retornar. (No caso em que mais contextos de cor estão disponíveis do que o número de objetos **IWICColorContext** passados pelo chamador, isso informa ao chamador que há um ou mais outros disponíveis.)

### <a name="getmetadataqueryreader"></a>GetMetadataQueryReader

[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) retorna um [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) que pode ser usado por um aplicativo para recuperar metadados do quadro da imagem. Essa interface é implementada por um manipulador de metadados e permite que um aplicativo consulte Propriedades de metadados específicas que pertencem a um formato de metadados específico. Para obter mais informações, consulte [implementando o IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md).

Para criar uma instância de um [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), chame [**CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) no [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory).


```C++
IWICMetadataQueryReader* pQueryReader = NULL;
HRESULT hr;

hr = m_pComponentFactory->CreateQueryReaderFromBlockReader( 
  static_cast<IWICMetadataBlockWriter*>(this),
  &pQueryReader);
```



### <a name="getsize-getpixelformat-and-getresolution"></a>GetSize, GetPixelFormat e Resolution

[**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize), [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)e [**Resolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) são auto-explicativos e retornam as propriedades solicitadas da imagem.

### <a name="copypixels"></a>CopyPixels

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) é o método chamado por um aplicativo quando ele deseja criar um bitmap na memória que pode ser renderizado para a exibição ou impressora. Esse é o método que faz a decodificação real dos bits de imagem. Os parâmetros são um retângulo, que representa a região de interesse na imagem de origem a ser copiada na memória; o stride, que especifica o número de bytes em uma linha de digitalização; o tamanho do buffer na memória que foi alocado pelo aplicativo; e um ponteiro para o buffer no qual os bits de imagem solicitados devem ser copiados. (Para evitar que estouros de buffer em potencial introduzam vulnerabilidades de segurança, certifique-se de copiar apenas a quantidade de dados de imagem no buffer que o parâmetro *cbBufferSize* especifica.)

### <a name="copypalette"></a>CopyPalette

Somente os codecs que têm formatos de pixel indexados devem implementar o método [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) . Se uma imagem usar um formato indexado, use esse método para retornar a paleta de cores usadas na imagem. Se o seu codec não tiver um formato indexado, retornará WINCODEC \_ Err \_ PALETTEUNAVAILABLE.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Implementando IWICBitmapSource](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[Implementando o IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



