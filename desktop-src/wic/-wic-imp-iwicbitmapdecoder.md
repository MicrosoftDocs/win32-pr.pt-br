---
description: Implementando IWICBitmapDecoder
ms.assetid: 9e316bdd-803a-47af-b004-7675478eb829
title: Implementando IWICBitmapDecoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0088b756a7a30134224e32fa67ee891f2c48339f9af70447cb760915ad420619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711143"
---
# <a name="implementing-iwicbitmapdecoder"></a>Implementando IWICBitmapDecoder

## <a name="iwicbitmapdecoder"></a>Iwicbitmapdecoder

Quando um aplicativo solicita um decodificador, o primeiro ponto de interação com o codec é por meio da interface [**IWICBitmapDecoder.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) Essa é a interface de nível de contêiner que fornece acesso às propriedades de nível superior do contêiner e, mais importante, aos quadros que ele contém. Essa é a interface primária em sua classe de decodificador no nível do contêiner.

``` syntax
interface IWICBitmapDecoder : IUnknown
{
// Required methods
   HRESULT QueryCapability (IStream *pIStream, 
      DWORD *pdwCapabilities );
   HRESULT Initialize ( IStream *pIStream,
      WICDecodeOptions cacheOptions );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetDecoderInfo ( IWICBitmapDecoderInfo **pIDecoderInfo );
   HRESULT GetFrameCount ( UINT *pCount );
   HRESULT GetFrame ( UINT index, 
      IWICBitmapFrameDecode **ppIBitmapFrame );

// Optional methods
   HRESULT GetPreview ( IWICBitmapSource **ppIPreview );
   HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
   HRESULT GetColorContexts ( UINT cCount, 
      IWICColorContext **ppIColorContexts, 
      UINT *pcActualCount );
   HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader);
   HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

Alguns formatos de imagem têm miniaturas globais, contextos de cores ou metadados, enquanto muitos formatos de imagem fornecem esses formatos apenas por quadro. Os métodos para acessar esses itens são opcionais em [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder), mas são necessários em [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode). Da mesma forma, alguns codecs não usam formatos de pixel indexados e, portanto, não precisam implementar os métodos [CopyPalette](-wic-imp-iwicbitmapframedecode.md) em nenhuma das interfaces. Para obter mais informações sobre os métodos **IWICBitmapDecoder** opcionais, consulte [Implementando IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md), em que eles são implementados mais comumente.

### <a name="querycapability"></a>QueryCapability

[**QueryCapability é**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) o método usado para a mediação de codec. (Consulte [Discovery and Arbitration](-wic-howwicworks.md) no tópico How The Windows [Imaging Component Works).](-wic-howwicworks.md) Se dois codecs puderem decodificar o mesmo formato de imagem ou se ocorrer uma colisão de padrões em que dois codecs usam o mesmo padrão de identificação, esse método permitirá que você selecione o codec que pode lidar melhor com qualquer imagem específica.

Ao invocar esse método, Windows WIC (Componente de Imagens) passa o fluxo real que contém a imagem. Você deve verificar se é possível decodificar cada quadro dentro da imagem e enumerar por meio dos blocos de metadados, para declarar com precisão quais recursos esse decodificador tem em relação ao fluxo de arquivos específico passado para ele. Isso é importante para todos os decodificadores, mas particularmente importante para formatos de imagem com base em contêineres TIFF (Formato de Arquivo de Imagem Marcada). O processo de descoberta funciona correspondendo padrões associados a decodificadores no Registro para padrões no arquivo de imagem real. Declarar seu padrão de identificação no Registro garante que o decodificador sempre será detectado para imagens no formato de imagem. No entanto, o decodificador ainda pode ser detectado para imagens em outros formatos. Por exemplo, todos os contêineres TIFF incluem o padrão TIFF, que é um padrão de identificação válido para o formato de imagem TIFF. Isso significa que, durante a descoberta, pelo menos dois padrões de identificação serão encontrados em arquivos de imagem para qualquer formato de imagem baseado em um contêiner no estilo TIFF. Um será o padrão TIFF e o outro será o padrão de formato de imagem real. Embora seja menos provável, também pode haver colisões de padrões entre outros formatos de imagem não relacionados. É por isso que a descoberta e a mediação são um processo de duas fases. Sempre verifique se o fluxo de imagem passado para [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) é, na verdade, uma instância válida do seu próprio formato de imagem. Além disso, se o codec decodificar um formato de imagem para o qual você não possui a especificação, a implementação **de QueryCapability** deverá verificar a presença de qualquer recurso que possa ser válido na especificação de formato de imagem que seu codec não implementa. Isso garantirá que os usuários não experimentem falhas desnecessárias de decodificação nem recebam resultados inesperados com seu codec.

Antes de executar qualquer operação na imagem, você deve salvar a posição atual do fluxo, para que possa restaurá-la para sua posição original antes de retornar do método . A [**enumeração WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) que especifica os recursos é definida da seguinte forma:

``` syntax
enum WICBitmapDecoderCapabilities
{   
   WICBitmapDecoderCapabilitySameEncoder,
   WICBitmapDecoderCapabilityCanDecodeAllImages,
   WICBitmapDecoderCapabilityCanDecodeSomeImages,
   WICBitmapDecoderCapabilityCanEnumerateMetadata,
   WICBitmapDecoderCapabilityCanDecodeThumbnail
}
```

Você deverá declarar **WICBitmapDecoderCapabilitySameEncoder** somente se o codificador tiver codificado a imagem. Depois de verificar se é possível decodificar cada quadro no contêiner, declare **WICBitmapDecoderCapabilityCanDecodeSomeImages** se puder decodificar alguns, mas não todos os quadros, **WICBitmapDecoderCapabilityCanDecodeAllImages** se você puder decodificar todos os quadros ou nenhum se não puder decodificar nenhum deles. (Essas duas enums são mutuamente exclusivas; se você retornar **WICBitmapDecoderCapabilityCanDecodeAllImages**, **WICBitmapDecoderCapabilityCanDecodeSomeImages** será ignorado.) Declare **WICBitmapDecoderCapabilityCanEnumerateMetadata** depois de verificar se você pode enumerar por meio dos blocos de metadados no contêiner de imagem. Você não precisa verificar se há uma miniatura em cada quadro. Se houver uma miniatura global e você puder decodificá-la, poderá declarar **WICBitmapDecoderCapabilityCanDecodeThumbnail**. Se não houver nenhuma miniatura global, tente decodificar a miniatura do Quadro 0. Se não houver miniatura em nenhum desses locais, não declare essa funcionalidade.

Depois de determinar os recursos do decodificador em relação ao fluxo de imagem passado para esse método, execute uma operação OR com [**o WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) que você verificou que esse decodificador pode executar nessa imagem e retornar o resultado. Lembre-se de restaurar o fluxo para sua posição original antes de retornar.

### <a name="initialize"></a>Inicializar

[**Inicializar**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) é invocado por um aplicativo depois que um decodificador foi selecionado para decodificar uma imagem específica. O fluxo de imagem é passado para o decodificador e um chamador pode, opcionalmente, especificar a opção de cache [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) para lidar com os metadados no arquivo.

``` syntax
enum WICDecodeOptions
{
   WICDecodeMetadataCacheOnDemand,
   WICDecodeMetadataCacheOnLoad
}
```

Alguns aplicativos usam metadados mais do que outros. A maioria dos aplicativos não precisa acessar todos os metadados em um arquivo de imagem e solicitará metadados específicos conforme necessário. Outros aplicativos preferem armazenar em cache todos os metadados antes de manter o fluxo de arquivos aberto e executar E/S de disco sempre que eles precisam acessar metadados. Se o chamador não especificar uma opção de cache de metadados, o comportamento de cache padrão deverá ser o cache sob demanda. Isso significa que nenhum metadado deve ser carregado na memória até que o aplicativo faça uma solicitação específica para os metadados. Se o aplicativo especificar **WICDecodeMetadataCacheOnLoad,** os metadados deverão ser carregados na memória imediatamente e armazenados em cache. Quando os metadados são armazenados em cache na carga, o fluxo de arquivos pode ser liberado depois que os metadados são armazenados em cache.

### <a name="getcontainerformat"></a>Getcontainerformat

Para implementar [**GetContainerFormat,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)basta retornar o GUID do formato de imagem da imagem para o qual o decodificador é instautado. Esse método também é implementado [**em IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) e [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).

### <a name="getdecoderinfo"></a>GetDecoderInfo

[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) retorna um [**objeto IWICBitmapDecoderInfo.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) Para obter o objeto **IWICBitmapDecoderInfo,** basta passar o GUID do decodificador para o método [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) em [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)e, em seguida, solicitar a interface **IWICBitmapDecoderInfo,** conforme mostrado no exemplo a seguir.


```C++
IWICComponentInfo* pComponentInfo = NULL;
HRESULT hr;
 
hr = m_pImagingFactory->CreateComponentInfo(CLSID_This, &pComponentInfo);

hr = pComponentInfo->QueryInterface(IID_IWICBitmapDecoderInfo, (void**)ppIDecoderInfo);

```



### <a name="getframecount"></a>GetFrameCount

[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) apenas retorna o número de quadros no contêiner. Alguns formatos de contêiner suportam vários quadros e outros suportam apenas um quadro por contêiner.

### <a name="getframe"></a>Getframe

[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) é um método importante na interface [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) porque o quadro contém os bits de imagem reais e o objeto de decodificador de quadro retornado desse método é o objeto que faz a decodificação real da imagem solicitada. Esse é o outro objeto que você precisa implementar ao escrever um decodificador. Para obter mais informações sobre decodificadores de quadro, consulte [Implementando IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).

### <a name="getpreview"></a>GetPreview

[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) retorna uma visualização da imagem. Para ver uma discussão detalhada sobre previews, consulte Implementando o método [IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) na interface [Implementando IWICBitmapEncoder.](-wic-imp-iwicbitmapencoder.md)

Se o formato de imagem contiver uma visualização JPEG inserida, é fortemente recomendável que, em vez de escrever um decodificador JPEG para decodificá-lo, você delegue ao decodificador JPEG que acompanha a plataforma WIC para decodificar visualizações e miniaturas. Para fazer isso, procure até o início dos dados de imagem de visualização no fluxo e invoque o método [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) no [**IWICImagingFactory.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)


```C++
IWICBitmapDecoder* pPreviewDecoder = NULL;
IWICBitmapFrameDecode* pPreviewFrame = NULL;
IWICBitmapSource* pPreview = NULL;
HRESULT hr;

hr = m_pImagingFactory->CreateDecoderFromStream(
                               m_pStream, NULL, 
                               WICDecodeMetadataCacheOnDemand, &pPreviewDecoder);
hr = pPreviewDecoder->GetFrame(0, pPreviewFrame);
hr = pPreviewFrame->QueryInterface(IID_IWICBitmapSource, (void**)&pPreview);

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**Iwicbitmapdecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**Iwicbitmapframedecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Interfaces do decodificador](-wic-decoderinterfaces.md)
</dt> <dt>

[Implementando IWICBitmapCodecProgressNotification (Decoder)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[Como escrever um codec WIC-Enabled código](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



