---
description: Implementando IWICBitmapDecoder
ms.assetid: 9e316bdd-803a-47af-b004-7675478eb829
title: Implementando IWICBitmapDecoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b31bca377828606fe1beb68d6f1d95d290e01407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011091"
---
# <a name="implementing-iwicbitmapdecoder"></a>Implementando IWICBitmapDecoder

## <a name="iwicbitmapdecoder"></a>IWICBitmapDecoder

Quando um aplicativo solicita um decodificador, o primeiro ponto de interação com o codec é por meio da interface [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) . Essa é a interface de nível de contêiner que fornece acesso às propriedades de nível superior do contêiner e, o mais importante, os quadros que ele contém. Essa é a interface principal em sua classe de decodificador de nível de contêiner.

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

Alguns formatos de imagem têm miniaturas globais, contextos de cor ou metadados, enquanto muitos formatos de imagem só fornecem isso por quadro. Os métodos para acessar esses itens são opcionais em [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder), mas são necessários em [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode). Da mesma forma, alguns codecs não usam formatos de pixel indexados e, portanto, não precisam implementar os métodos [CopyPalette](-wic-imp-iwicbitmapframedecode.md) em nenhuma das interfaces. Para obter mais informações sobre os métodos **IWICBitmapDecoder** opcionais, consulte [implementando IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md), onde eles são mais comumente implementados.

### <a name="querycapability"></a>QueryCapability

[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) é o método usado para arbitragem de codec. (Consulte [descoberta e arbitragem](-wic-howwicworks.md) no tópico [como o componente do Windows Imaging Component funciona](-wic-howwicworks.md) ). Se dois codecs forem capazes de decodificar o mesmo formato de imagem, ou se ocorrer uma colisão de padrão em que dois codecs usem o mesmo padrão de identificação, esse método permitirá que você selecione o codec que pode lidar melhor com qualquer imagem específica.

Ao invocar esse método, o Windows Imaging Component (WIC) passa o fluxo real que contém a imagem. Você deve verificar se é possível decodificar cada quadro dentro da imagem e enumerar os blocos de metadados para declarar com precisão quais recursos esse decodificador tem em relação ao fluxo de arquivo específico passado para ele. Isso é importante para todos os decodificadores, mas particularmente importante para formatos de imagem com base em contêineres TIFF (Tagged Image File Format). O processo de descoberta funciona por padrões correspondentes associados aos decodificadores no registro para padrões no arquivo de imagem real. Declarar seu padrão de identificação no registro garante que seu decodificador sempre será detectado para imagens no seu formato de imagem. No entanto, seu decodificador ainda pode ser detectado para imagens em outros formatos. Por exemplo, todos os contêineres TIFF incluem o padrão TIFF, que é um padrão de identificação válido para o formato de imagem TIFF. Isso significa que, durante a descoberta, pelo menos dois padrões de identificação serão encontrados em arquivos de imagem para qualquer formato de imagem baseado em um contêiner de estilo TIFF. Um será o padrão TIFF e o outro será o padrão de formato de imagem real. Embora menos provável, também pode haver colisões de padrões entre outros formatos de imagem não relacionados. É por isso que a descoberta e a arbitragem são um processo de duas etapas. Sempre verifique se o fluxo de imagem passado para [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) é, na verdade, uma instância válida do seu próprio formato de imagem. Além disso, se o codec decodificar um formato de imagem para o qual você não possui a especificação, sua implementação de **QueryCapability** deverá verificar a presença de qualquer recurso que possa ser válido na especificação de formato de imagem que o codec não implementa. Isso garantirá que os usuários não tenham falhas de decodificação desnecessárias ou obtenham resultados inesperados com seu codec.

Antes de executar qualquer operação na imagem, você deve salvar a posição atual do fluxo, para que possa restaurá-la para sua posição original antes de retornar do método. A enumeração [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) que especifica os recursos é definida da seguinte maneira:

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

Você deve declarar **WICBitmapDecoderCapabilitySameEncoder** somente se o codificador foi aquele que codificou a imagem. Depois de verificar se você pode decodificar cada quadro no contêiner, declare **WICBitmapDecoderCapabilityCanDecodeSomeImages** se você puder decodificar alguns, mas não todos os quadros, **WICBitmapDecoderCapabilityCanDecodeAllImages** se você puder decodificar todos os quadros, ou nenhum deles, se não for possível decodificar nenhum deles. (Essas duas enumerações são mutuamente exclusivas; se você retornar **WICBitmapDecoderCapabilityCanDecodeAllImages**, **WICBitmapDecoderCapabilityCanDecodeSomeImages** será ignorado.) Declare **WICBitmapDecoderCapabilityCanEnumerateMetadata** depois de verificar se você pode enumerar os blocos de metadados no contêiner de imagem. Você não precisa verificar uma miniatura em todos os quadros. Se houver uma miniatura global e você puder decodificá-la, você poderá declarar **WICBitmapDecoderCapabilityCanDecodeThumbnail**. Se não houver uma miniatura global, tente decodificar a miniatura do quadro 0. Se não houver nenhuma miniatura em nenhum desses locais, não declare esse recurso.

Depois de determinar os recursos do decodificador em relação ao fluxo de imagem passado para esse método, execute uma operação OR com o [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) que você verificou que esse decodificador pode executar nessa imagem e retorne o resultado. Lembre-se de restaurar o fluxo para sua posição original antes de retornar.

### <a name="initialize"></a>Inicializar

A [**inicialização**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) é invocada por um aplicativo após a seleção de um decodificador para decodificar uma imagem específica. O fluxo de imagem é passado para o decodificador, e um chamador pode opcionalmente especificar a opção de cache [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) para lidar com os metadados no arquivo.

``` syntax
enum WICDecodeOptions
{
   WICDecodeMetadataCacheOnDemand,
   WICDecodeMetadataCacheOnLoad
}
```

Alguns aplicativos usam metadados mais do que outros. A maioria dos aplicativos não precisa acessar todos os metadados em um arquivo de imagem e solicitará metadados específicos conforme eles precisarem. Outros aplicativos, em vez disso, armazenariam em cache todos os metadados antecipadamente que mantêm o fluxo de arquivos aberto e executam e/s de disco toda vez que precisam acessar metadados. Se o chamador não especificar uma opção de cache de metadados, o comportamento de cache padrão deverá ser o cache sob demanda. Isso significa que nenhum metadado deve ser carregado na memória até que o aplicativo faça uma solicitação específica para esses metadados. Se o aplicativo especificar **WICDecodeMetadataCacheOnLoad**, os metadados deverão ser carregados na memória imediatamente e armazenados em cache. Quando os metadados são armazenados em cache no carregamento, o fluxo de arquivos pode ser liberado depois que os metadados são armazenados em cache.

### <a name="getcontainerformat"></a>GetContainerFormat

Para implementar [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat), basta retornar o GUID do formato de imagem da imagem para a qual o decodificador é instanciado. Esse método também é implementado em [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) e [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).

### <a name="getdecoderinfo"></a>GetDecoderInfo

[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) retorna um objeto [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) . Para obter o objeto **IWICBitmapDecoderInfo** , basta passar o GUID do decodificador para o método [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) em [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)e, em seguida, solicitar a interface **IWICBitmapDecoderInfo** nele, conforme mostrado no exemplo a seguir.


```C++
IWICComponentInfo* pComponentInfo = NULL;
HRESULT hr;
 
hr = m_pImagingFactory->CreateComponentInfo(CLSID_This, &pComponentInfo);

hr = pComponentInfo->QueryInterface(IID_IWICBitmapDecoderInfo, (void**)ppIDecoderInfo);

```



### <a name="getframecount"></a>GetFrameCount

[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) retorna apenas o número de quadros no contêiner. Alguns formatos de contêiner dão suporte a vários quadros e outros dão suporte a apenas um quadro por contêiner.

### <a name="getframe"></a>GetFrame

[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) é um método importante na interface [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) porque o quadro contém os bits de imagem reais, e o objeto decodificador de quadro retornado desse método é o objeto que faz a decodificação real da imagem solicitada. Esse é o outro objeto que você precisa implementar ao escrever um decodificador. Para obter mais informações sobre decodificadores de quadros, consulte [implementando IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).

### <a name="getpreview"></a>GetPreview

[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) retorna uma visualização da imagem. Para obter uma discussão detalhada sobre visualizações, consulte o método [implementando IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) na interface de [implementação IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) .

Se o formato de imagem contiver uma visualização JPEG incorporada, é altamente recomendável que, em vez de gravar um decodificador de JPEG para decodificá-lo, você delegue ao decodificador de JPEG que é fornecido com a plataforma WIC para decodificar visualizações e miniaturas. Para fazer isso, procure o início dos dados da imagem de visualização no fluxo e invoque o método [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) no [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).


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

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Interfaces do decodificador](-wic-decoderinterfaces.md)
</dt> <dt>

[Implementando IWICBitmapCodecProgressNotification (decodificador)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



