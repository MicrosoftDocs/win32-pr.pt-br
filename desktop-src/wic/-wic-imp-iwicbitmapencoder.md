---
description: Implementando IWICBitmapEncoder
ms.assetid: b671e941-ded6-4bde-bc4d-461f13feade0
title: Implementando IWICBitmapEncoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590dffcf762d22155a89a8143994d9a4d8bcab02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829497"
---
# <a name="implementing-iwicbitmapencoder"></a>Implementando IWICBitmapEncoder

-   [IWICBitmapEncoder](#implementing-iwicbitmapencoder)
    -   [Inicializar](#initialize)
    -   [GetContainerFormat](#getcontainerformat)
    -   [GetEncoderInfo](#getencoderinfo)
    -   [CreateNewFrame](#createnewframe)
    -   [Confirmar](#commit)
    -   [SetPreview](#setpreview)
-   [Tópicos relacionados](#related-topics)

## <a name="iwicbitmapencoder"></a>IWICBitmapEncoder

-   [Inicializar](#initialize)
-   [GetContainerFormat](#getcontainerformat)
-   [GetEncoderInfo](#getencoderinfo)
-   [CreateNewFrame](#createnewframe)
-   [Confirmar](#commit)
-   [SetPreview](#setpreview)

Essa interface é a contraparte para a interface [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e é o ponto de partida para codificar um arquivo de imagem. Assim como **IWICBitmapDecoder** é usado para recuperar propriedades de nível de contêiner e quadros individuais do contêiner de imagem, [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) é usado para definir propriedades em nível de contêiner e serializar quadros de imagem individuais no contêiner. Você implementa essa interface em sua classe de codificador de nível de contêiner.

``` syntax
interface IWICBitmapEncoder : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IStream *pIStream,
              WICBitmapEncoderCacheOption cacheOption );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetEncoderInfo ( IWICBitmapEncoderInfo **pIEncoderInfo );
   HRESULT CreateNewFrame ( IWICBitmapFrameEncode **ppIFrameEncode,
              IPropertyBag2 **ppIEncoderOptions );
   HRESULT Commit ( void );

   // Optional methods
   HRESULT SetPreview ( IWICBitmapSource *pIPreview );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT SetColorContexts ( UINT cCount,
              IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
              **ppIMetadataQueryWriter );
   HRESULT SetPalette ( IWICPalette *pIPalette);
};
```

Conforme discutido na [implementação de IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md), alguns formatos de imagem têm miniaturas globais, contextos de cor ou metadados, enquanto muitos formatos de imagem fornecem esses apenas em uma base por quadro. Portanto, os métodos para configurá-los são opcionais em [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder), mas são necessários em [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). Discutiremos os métodos que são opcionais em **IWICBitmapEncoder** na seção sobre **IWICBitmapFrameEncode**, onde eles são mais comumente implementados.

Se você não oferecer suporte a miniaturas globais, retornará WINCODEC \_ Err \_ CODECNOTHUMBNAIL do método SetThumbnail em [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder). Se você não oferecer suporte a uma paleta de nível de contêiner ou se a imagem que você está codificando não tiver um formato indexado, retornará WINCODEC \_ Err \_ PALETTEUNAVAILABLE do método SetPalette. Para qualquer outro método sem suporte, retorne WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.

### <a name="initialize"></a>Inicializar

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) é o primeiro método invocado em um [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) depois de ter sido instanciado. Um fluxo de imagem é passado para o codificador, e um chamador pode opcionalmente especificar uma opção de cache. No caso do decodificador, o fluxo é somente leitura, mas o fluxo passado para um codificador é um fluxo gravável, no qual o codificador serializará todos os dados de imagem e metadados. As opções de cache no codificador também são diferentes.

``` syntax
enum WICBitmapEncoderCacheOption
{
   WICBitmapEncoderCacheInMemory,
   WICBitmapEncoderCacheTempFile,
   WICBitmapEncoderNoCache
}
```

O aplicativo tem a opção de solicitar que o codificador armazene em cache os dados da imagem na memória, armazená-los em cache em um arquivo temporário ou gravá-los diretamente no arquivo de disco sem cache. Quando solicitado a armazenar em cache os dados em um arquivo temporário, o codificador deve criar um arquivo temporário no disco e gravar diretamente nesse arquivo sem armazenar em cache na memória. Quando o chamador seleciona a opção sem cache, cada quadro deve ser confirmado na ordem antes que o próximo quadro possa ser criado.

### <a name="getcontainerformat"></a>GetContainerFormat

[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat) é implementado da mesma maneira que o método [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) na [implementação de IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).

### <a name="getencoderinfo"></a>GetEncoderInfo

[**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) retorna um objeto [**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo) . Para obter o objeto **IWICBitmapEncoderInfo** , basta passar o GUID do seu codificador para o método [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) em [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)e, em seguida, solicitar a interface **IWICBitmapEncoderInfo** nele.

Consulte o exemplo em [implementando IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) em [GetDecoderInfo](-wic-imp-iwicbitmapdecoder.md).

### <a name="createnewframe"></a>CreateNewFrame

[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) é o equivalente do codificador de [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) em [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder). Esse método retorna um objeto [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) , que é o objeto que realmente serializa os dados da imagem para um quadro específico dentro do contêiner.

Um dos benefícios do Windows Imaging Component (WIC) é que ele fornece uma camada de abstração para aplicativos que permite que eles trabalhem com todos os formatos de imagem da mesma maneira. No entanto, nem todos os formatos de imagem são exatamente iguais. Alguns formatos de imagem têm recursos que outros não têm. Para que os aplicativos possam aproveitar esses recursos exclusivos, é necessário fornecer uma maneira para que o codec os exponha. Essa é a finalidade das opções de codificador. Se o codec oferecer suporte a qualquer opção de codificador, você deverá criar um objeto [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que exponha as opções de codificador para as quais dá suporte e retorná-lo no parâmetro *ppIEncoderOptions* desse método. O chamador pode usar esse objeto IPropertyBag2 para determinar quais opções de codificador o codec dá suporte. Se o chamador quiser especificar valores para qualquer uma das opções de codificador com suporte, ele atribuirá o valor à propriedade relevante no objeto IPropertyBag2 e o passará para o objeto [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) recém-criado em seu método Initialize.

Para instanciar um objeto [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) , primeiro você precisa criar um struct PROPBAG2 para especificar cada opção de codificador que o codificador suporta e seu tipo de dados para cada propriedade. Em seguida, você deve implementar um objeto IPropertyBag2 que impõe os intervalos de valores para cada propriedade na gravação e reconcilia todos os valores conflitantes ou sobrepostos. Para conjuntos simples de opções de codificador não conflitantes, você pode invocar o método [**CreateEncoderPropertyBag**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createencoderpropertybag) , que criará um objeto IPropertyBag2 simples usando as propriedades que você especificar em seu struct PROPBAG2. Você ainda deve impor os intervalos de valores. Para obter opções de codificador mais avançadas ou se precisar reconciliar valores conflitantes, você deve escrever sua própria implementação de IPropertyBag2.


```C++
UINT cuiPropertyCount = 0;
IPropertyBag2* pPropertyBag = NULL;
PROPBAG2* pPropBagOptions;
HRESULT hr;

// Insert code here to initialize piPropertyBag with the 
// supported options for your encoder, and to initialize 
// cuiPropertyCount to the number of encoder option properties
// you are exposing.
...

hr = pComponentFactory->CreateEncoderPropertyBag( 
   pPropBagOptions, cuiPropertyCount, &pPropertyBag);
```



O WIC fornece um pequeno conjunto de opções de codificador canônicos que são usadas por alguns dos formatos de imagem comuns. Todas as opções canônicas de codificador são opcionais e os codecs não são necessários para dar suporte a nenhuma delas. O motivo pelo qual eles são fornecidos como opções canônicas é porque muitos aplicativos expõem a interface do usuário para que os usuários especifiquem essas opções ao salvar um arquivo de imagem em um formato que ofereça suporte a eles. Fornecer uma maneira canônica de especificar essas opções torna mais fácil para os aplicativos se comunicarem com os codificadores de forma consistente. As opções canônicas de codificador são listadas na tabela a seguir.



| Opção de codificador     | VARTYPE  | Intervalo de valores               |
|--------------------|----------|---------------------------|
| Lossless           | BOOL do VT \_ | Verdadeiro/Falso                |
| ImageQuality       | VT \_ R4   | 0,0 a 1,0                   |
| CompressionQuality | VT \_ R4   | 0,0 a 1,0                   |
| BitmapTransform    | \_UI1 VT  | WICBitmapTransformOptions |



 

Se o codec der suporte à codificação sem perdas, você deverá expor a opção de codificador sem perdas como uma maneira de os aplicativos solicitarem que uma imagem seja codificada sem perdas. Se um chamador definir essa propriedade como true, você deverá ignorar a opção ImageQuality e codificar a imagem sem perdas.

A opção ImageQuality permite que um aplicativo especifique o grau de fidelidade com o qual codificar a imagem. Essa opção permite que um usuário faça uma compensação entre qualidade de imagem versus velocidade e/ou tamanho do arquivo. JPEG é um exemplo de formato de imagem que dá suporte a essa compensação. Um valor de 0,0 indica que a fidelidade é de baixa importância e que o codificador deve usar seu algoritmo mais com perda. Um valor de 1,0 indica que a fidelidade é a mais importante e o codificador deve preservar a maior fidelidade possível. (Dependendo do seu codec, isso pode ser sinônimo da opção sem perdas. No entanto, se o codec der suporte à codificação sem perdas e se a opção sem perdas for definida como true, a opção ImageQuality deverá ser ignorada.)

A opção CompressionQuality permite que um aplicativo especifique a eficiência da compactação a ser usada ao codificar a imagem. Um algoritmo muito eficiente pode produzir um arquivo de imagem menor com a mesma qualidade que um algoritmo de compactação menos eficiente, mas pode levar mais tempo para codificar. Essa opção permite que um usuário especifique uma compensação entre o tamanho do arquivo versus a velocidade de codificação, preservando o mesmo nível de qualidade. TIFF é um exemplo de formato de imagem que dá suporte a essa compensação. (Observe que um formato como o JPEG dá suporte a diferentes níveis de compactação, mas uma taxa mais alta de compactação resulta em uma qualidade de imagem inferior. Portanto, um formato de imagem JPEG exporia a opção ImageQuality em vez da opção CompressionQuality.) Um valor de 0,0 para essa opção indica que você deve compactar a imagem o mais rápido possível, sem reduzir a fidelidade, às custas de um tamanho de arquivo maior. Um valor de 1,0 indica que você deve criar o menor tamanho de arquivo possível (no mesmo nível de qualidade), independentemente de quanto tempo pode levar para codificá-lo. Um codec pode dar suporte à opção ImageQuality e à opção CompressionQuality, em que a opção ImageQuality especifica o grau aceitável de perda e a opção CompressionQuality oferece uma compensação de tamanho/velocidade no nível de qualidade especificado.

A opção BitmapTransform fornece uma maneira para o chamador especificar um ângulo de rotação ou uma orientação vertical ou horizontal invertida durante a codificação. A enumeração WICBitmapTransformOptions usada para especificar a transformação solicitada é o mesmo enum usado ao solicitar uma transformação durante a decodificação por meio da interface IWICBitmapSourceTransform.

Observe que os codificadores não estão limitados às opções de codificador canônico. A finalidade das opções de codificador é permitir que os codificadores exponham seus recursos, e não há nenhum limite para os tipos de recursos que você pode expor. Verifique se suas opções de codificador estão bem documentadas. Embora um aplicativo possa usar o recipiente de propriedades que você retorna desse método para descobrir os nomes, os tipos e os intervalos de valores das opções que você dá suporte, a única maneira para eles descobrirem seus significados ou como expô-los na interface do usuário é de sua documentação.

### <a name="commit"></a>Commit

[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) é o método que você chama depois que todos os dados e metadados da imagem forem serializados no fluxo. Você deve usar esse método para serializar os dados da imagem de visualização para o fluxo e quaisquer miniaturas globais, metadados, paletas ou outros itens, se aplicável. Esse método não deve fechar o fluxo de arquivos, pois o aplicativo que abriu o fluxo é esperado fechá-lo.

A seção sobre o método IWICBitmapFrameEncode: Commit tem detalhes sobre como o IWICBitmapEncoderCacheOptions afeta o comportamento desse método.

### <a name="setpreview"></a>SetPreview

[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) é usado para criar uma visualização da imagem. Embora não seja estritamente necessário que todas as imagens tenham uma visualização, é altamente recomendável. Câmeras digitais e scanners modernos geram imagens de alta resolução, que tendem a ser muito grandes e, consequentemente, levam um tempo de processamento significativo para decodificação. As imagens da próxima geração de câmeras serão ainda maiores. É uma boa ideia fornecer uma versão menor, de menor resolução, de uma imagem, normalmente no formato JPEG, que possa ser rapidamente decodificada e exibida "instantaneamente" quando um usuário solicitar. Um aplicativo pode solicitar uma visualização antes de solicitar que a imagem real seja decodificada para fornecer uma experiência melhor para os usuários e mostrá-los uma representação de tamanho de tela da imagem enquanto theyare aguardando a decodificação da imagem real. Embora os codecs devam fornecer visualizações, os codecs que não dão suporte a [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) devem definitivamente fazer isso.

Se você fornecer uma visualização JPEG, não precisará escrever um codificador de JPEG para codificá-lo. Você deve delegar para o codificador JPEG que acompanha a plataforma WIC para codificação de visualizações e miniaturas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Interfaces do codificador](-wic-encoderinterfaces.md)
</dt> <dt>

[Implementando IWICBitmapCodecProgressNotification (codificador)](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
