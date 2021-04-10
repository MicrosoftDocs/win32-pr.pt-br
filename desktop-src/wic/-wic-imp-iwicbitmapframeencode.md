---
description: Implementando IWICBitmapFrameEncode
ms.assetid: 509fa49c-c90d-4270-a338-6ce638ccd89a
title: Implementando IWICBitmapFrameEncode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d2a5ea0412ea4a45ea329618d00443c1755391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170872"
---
# <a name="implementing-iwicbitmapframeencode"></a>Implementando IWICBitmapFrameEncode

## <a name="iwicbitmapframeencode"></a>IWICBitmapFrameEncode

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) é o equivalente do codificador à interface [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) . Você pode implementar essa interface em sua classe de codificação de nível de quadro, que é a classe que faz a codificação real dos bits de imagem para cada quadro.


```C++
interface IWICBitmapFrameEncode : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IPropertyBag2 *pIEncoderOptions );
   HRESULT SetSize ( UINT width,
               UINT height );
   HRESULT SetResolution ( double dpiX,
               double dpiY );
   HRESULT SetPixelFormat (WICPixelFormatGUID *pPixelFormat);
   HRESULT SetColorContexts ( UINT cCount,
               IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
               **ppIMetadataQueryWriter );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT WritePixels ( UINT lineCount,
               UINT cbStride,
               UINT cbBufferSize,
               BYTE *pbPixels );
   HRESULT WriteSource ( IWICBitmapSource *pIWICBitmapSource,
               WICRect *prc );
   HRESULT Commit ( void );

// Optional method
   HRESULT SetPalette ( IWICPalette *pIPalette );
};
```



-   [Inicializar](#initialize)
-   [SetSize e Resolution](#setsize-and-setresolution)
-   [SetPixelFormat](#setpixelformat)
-   [SetColorContexts](#setcolorcontexts)
-   [GetMetadataQueryWriter](#getmetadataquerywriter)
-   [SetThumbnail](#setthumbnail)
-   [WritePixels](#writepixels)
-   [Gravação](#writesource)
-   [Confirmar](#commit)
-   [SetPalette](#setpalette)

### <a name="initialize"></a>Inicializar

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) é o primeiro método invocado em um objeto [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) depois de ter sido instanciado. Esse método tem um parâmetro, que pode ser definido como **nulo**. Esse parâmetro representa as opções de codificador e é a mesma instância de [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que você criou no método [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) no decodificador de nível de contêiner e passado de volta para o chamador no parâmetro pIEncoderOptions desse método. Nesse momento, você preencheu o struct IPropertyBag2 com propriedades que representam as opções de codificação com suporte no seu codificador de nível de quadro. O chamador agora forneceu valores para essas propriedades para indicar determinados parâmetros de opção de codificação e está passando o mesmo objeto de volta para você inicializar o objeto **IWICBitmapFrameEncode** . Você deve aplicar as opções especificadas ao codificar os bits de imagem.

### <a name="setsize-and-setresolution"></a>SetSize e Resolution

[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) e [**Resolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) são auto-explicativos. O chamador usa esses métodos para especificar o tamanho e a resolução da imagem codificada.

### <a name="setpixelformat"></a>SetPixelFormat

[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) é usado para solicitar um formato de pixel no qual codificar a imagem. Se não houver suporte para o formato de pixel solicitado, você deverá retornar o GUID do formato de pixel mais próximo com suporte em *pPixelFormat*, que é um parâmetro in/out.

### <a name="setcolorcontexts"></a>SetColorContexts

[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) é usado para especificar um ou mais contextos de cor válidos (também conhecidos como perfis de cor) para esta imagem. É importante especificar os contextos de cor, de modo que um aplicativo que decodifique a imagem posteriormente possa converter do perfil de cor de origem para o perfil de destino do dispositivo que está sendo usado para exibir ou imprimir a imagem. Sem um perfil de cor, não é possível obter cores consistentes em diferentes dispositivos. Isso pode ser frustrante para os usuários finais quando suas fotos parecem diferentes em monitores diferentes e não conseguem fazer as cópias coincidirem com o que vêem na tela.

### <a name="getmetadataquerywriter"></a>GetMetadataQueryWriter

[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) retorna um [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) que pode ser usado por um aplicativo para inserir ou editar propriedades de metadados específicas em um bloco de metadados no quadro da imagem.

Você pode criar uma instância de um [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) do [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) de várias maneiras. Você pode criá-lo de seu [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter), da mesma forma que [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) foi criado a partir de um [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) no método [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) na interface [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .


```C++
IWICMetadataQueryWriter* piMetadataQueryWriter = NULL;
HRESULT hr;

hr = m_piComponentFactory->CreateQueryWriterFromBlockWriter( 
      static_cast<IWICMetadataBlockWriter*>(this), 
      &piMetadataQueryWriter);

```



Você também pode criá-lo de um [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)existente, como aquele obtido usando o método anterior.


```C++
hr = m_piComponentFactory->CreateQueryWriterFromReader( 
      piMetadataQueryReader, pguidVendor, &piMetadataQueryWriter);
```



O parâmetro *pguidVendor* permite que você especifique um fornecedor específico para o gravador de consulta usar ao instanciar um gravador de metadados. Por exemplo, se você fornecer seus próprios gravadores de metadados, talvez queira especificar seu próprio GUID de fornecedor. Você pode passar **NULL** para esse parâmetro se não tiver uma preferência.

### <a name="setthumbnail"></a>SetThumbnail

[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) é usado para fornecer uma miniatura. Todas as imagens devem fornecer uma miniatura globalmente, em cada quadro ou em ambas. Os métodos **GetThumbnail** e **SetThumbnail** são opcionais no nível do contêiner, mas, se um codec retornar WINCODEC \_ Err \_ CODECNOTHUMBNAIL do método [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) , o Windows Imaging Component (WIC) invocará o método [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) para o quadro 0. Se nenhuma miniatura for encontrada em qualquer lugar, o WIC deverá decodificar a imagem completa e dimensioná-la para o tamanho da miniatura, o que pode incorrer em uma grande penalidade de desempenho para imagens maiores.

A miniatura deve ter um tamanho e uma resolução que tornem a decodificação e a exibição rápidas. Por esse motivo, as miniaturas são imagens JPEG mais comuns. Observe que, se você usar JPEG para suas miniaturas, não precisará escrever um codificador de JPEG para codificá-las ou um decodificador de JPEG para decodificá-las. Você sempre deve delegar ao codec JPEG fornecido com a plataforma WIC para codificação e decodificação de miniaturas.

### <a name="writepixels"></a>WritePixels

[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) é o método usado para passar linhas de verificação de um bitmap na memória para codificação. O método será chamado repetidamente até que todas as linhas de verificação tenham sido passadas. O parâmetro *LineCount* indica quantas linhas de verificação devem ser gravadas nesta chamada. O parâmetro *cbStride* indica o número de bytes por linha de varredura. *cbBufferSize* indica o tamanho do buffer passado no parâmetro pbPixels, que contém os bits de imagem reais a serem codificados. Se a altura combinada das linhas de verificação das chamadas cumulativas for maior que a altura especificada no método [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) , retornará WINCODEC \_ Err \_ TOOMANYSCANLINES.

Quando [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) for **WICBitmapEncoderCacheInMemory**, as linhas de verificação deverão ser armazenadas em cache na memória até que todas as linhas de verificação tenham sido passadas. Se a opção de cache do codificador for **WICBitmapEncoderCacheTempFile**, as linhas de verificação deverão ser armazenadas em cache em um arquivo temporário, criado durante a inicialização do objeto. Em qualquer um desses casos, a imagem não deve ser codificada até que o chamador chame [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit). No caso em que a opção de cache é **WICBitmapEncoderNoCache**, o codificador deve codificar as linhas de varredura conforme elas são recebidas, se possível. (Em alguns formatos, isso não é possível e as linhas de verificação devem ser armazenadas em cache até que a confirmação seja chamada.)

A maioria dos codecs brutos não implementará [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), pois eles não dão suporte à alteração dos bits de imagem no arquivo bruto. No entanto, os codecs brutos ainda devem implementar **WritePixels**, porque quando os metadados são adicionados, ele pode aumentar o tamanho do arquivo, exigindo que o arquivo seja regravado no disco. Nesse caso, é necessário ser capaz de copiar os bits de imagem existentes, que é o que o método **WritePixels** faz.

### <a name="writesource"></a>Gravação

O [**writeprovider**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) é usado para codificar um objeto [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) . O primeiro parâmetro é um ponteiro para um objeto **IWICBitmapSource** . O segundo parâmetro é um WICRect que especifica a região de interesse a ser codificada. Esse método pode ser chamado várias vezes em sucessão, desde que a largura de cada retângulo tenha a mesma largura da imagem final a ser codificada. Se a largura do retângulo passado no parâmetro prc for diferente da largura especificada no método setSize, retornará WINCODEC \_ Err \_ SOURCERECTDOESNOTMATCHDIMENSIONS. Se a altura combinada das linhas de verificação das chamadas cumulativas for maior que a altura especificada no método setSize, retornará WINCODEC \_ Err \_ TOOMANYSCANLINES.

As opções de cache funcionam da mesma maneira com esse método, como com o método [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) descrito anteriormente.

### <a name="commit"></a>Commit

[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) é o método que serializa os bits de imagem codificada para o fluxo de arquivos e faz a iteração por todos os gravadores de metadados para o quadro que os solicita para serializar seus metadados para o fluxo. No caso em que a opção de cache do codificador é WICBitmapEncoderCacheInMemory ou WICBitmapEncoderCacheTempFile, esse método também é responsável por codificar a imagem e, quando a opção cache é WICBitmapEncoderCacheTempFile, o método **Commit** também deve excluir o arquivo temporário usado para armazenar em cache os dados da imagem antes da codificação.

Esse método é sempre invocado depois que todas as linhas de verificação ou retângulos que compõem a imagem foram passados usando o método [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) ou [**writery**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) . O tamanho do retângulo final que é composto por meio das chamadas acumuladas para WritePixels ou WriteName deve ter o mesmo tamanho que foi especificado no método setSize. Se o tamanho não corresponder ao tamanho esperado, esse método deverá retornar WINCODECERROR \_ UNEXPECTEDSIZE.

Para iterar os gravadores de metadados e informar a cada gravador de metadados para serializar seus metadados, acesse o fluxo, invoque GetWriterByIndex para iterar pelos gravadores para cada bloco e invoque IWICPersistStream. Save em cada gravador de metadados.


```C++
IWICMetadataWriter* piMetadataWRiter = NULL;
IWICPersistStream* piPersistStream = NULL;
HRESULT hr;

for (UINT x=0; x < m_blockCount; x++) 
{
    hr = GetWriterByIndex(x, & piMetadataWriter);
hr = piMetadataWriter->QueryInterface(
IID_IWICPersistStream,(void**)&piPersistStream);

hr = piPersistStream->Save(m_piStream, 
WICPersistOptions.WicPersistOptionDefault, 
true);
...
}
```



### <a name="setpalette"></a>SetPalette

Somente os codecs que têm formatos indexados precisam implementar o método [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) . Se uma imagem usar um formato indexado, use esse método para especificar a paleta de cores usadas na imagem. Se o seu codec não tiver um formato indexado, retorne WINCODEC \_ Err \_ PALETTEUNAVAILABLE a partir desse método.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Implementando IWICBitmapCodecProgressNotification (codificador)](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[Implementando IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
