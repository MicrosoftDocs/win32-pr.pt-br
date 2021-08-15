---
description: Implementando IWICBitmapEncoder
ms.assetid: b671e941-ded6-4bde-bc4d-461f13feade0
title: Implementando IWICBitmapEncoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d02105470f837dba0689b665473c01c42f6cd6497a85424ea6eea3371696f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088008"
---
# <a name="implementing-iwicbitmapencoder"></a>Implementando IWICBitmapEncoder

-   [IWICBitmapEncoder](#implementing-iwicbitmapencoder)
    -   [Inicializar](#initialize)
    -   [Getcontainerformat](#getcontainerformat)
    -   [GetEncoderInfo](#getencoderinfo)
    -   [Createnewframe](#createnewframe)
    -   [Confirmar](#commit)
    -   [SetPreview](#setpreview)
-   [Tópicos relacionados](#related-topics)

## <a name="iwicbitmapencoder"></a>IWICBitmapEncoder

-   [Inicializar](#initialize)
-   [Getcontainerformat](#getcontainerformat)
-   [GetEncoderInfo](#getencoderinfo)
-   [Createnewframe](#createnewframe)
-   [Confirmar](#commit)
-   [SetPreview](#setpreview)

Essa interface é a contraparte da interface [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e é o ponto de partida para codificar um arquivo de imagem. Assim como **IWICBitmapDecoder** é usado para recuperar propriedades no nível do contêiner e quadros individuais do contêiner de imagem, [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) é usado para definir propriedades no nível do contêiner e serializar quadros de imagem individuais no contêiner. Você implementa essa interface em sua classe de codificador no nível do contêiner.

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

Conforme discutido em [Implementando IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md), alguns formatos de imagem têm miniaturas globais, contextos de cor ou metadados, enquanto muitos formatos de imagem fornecem esses formatos apenas por quadro. Portanto, os métodos para defini-los são opcionais em [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder), mas são necessários [**em IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). Discutiremos os métodos opcionais em **IWICBitmapEncoder** na seção **em IWICBitmapFrameEncode**, em que eles são implementados com mais comum.

Se você não tiver suporte para miniaturas globais, retorne WINCODEC \_ ERR \_ CODECNOTHUMBNAIL do método SetThumbnail [**em IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder). Se você não tiver suporte para uma paleta no nível do contêiner ou se a imagem que você está codificando não tiver um formato indexado, retorne WINCODEC ERR PALETTEUNAVAILABLE do método \_ \_ SetPalette. Para qualquer outro método sem suporte, retorne WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION.

### <a name="initialize"></a>Inicializar

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) é o primeiro método invocado em [**um IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) depois que ele é instautado. Um fluxo de imagem é passado para o codificador e um chamador pode, opcionalmente, especificar uma opção de cache. No caso do decodificador, o fluxo é somente leitura, mas o fluxo passado para um codificador é um fluxo que pode ser escrito, no qual o codificador serializará todos os dados e metadados da imagem. As opções de cache no codificador também são diferentes.

``` syntax
enum WICBitmapEncoderCacheOption
{
   WICBitmapEncoderCacheInMemory,
   WICBitmapEncoderCacheTempFile,
   WICBitmapEncoderNoCache
}
```

O aplicativo tem a opção de solicitar ao codificador para armazenar em cache os dados da imagem na memória, armazenar em cache em um arquivo temporário ou gravar diretamente no arquivo de disco sem cache. Quando solicitado a armazenar em cache os dados em um arquivo temporário, o codificador deve criar um arquivo temporário no disco e gravar diretamente nesse arquivo sem armazenar em cache na memória. Quando o chamador seleciona a opção sem cache, cada quadro deve ser confirmado na ordem antes que o próximo quadro possa ser criado.

### <a name="getcontainerformat"></a>Getcontainerformat

[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat) é implementado da mesma maneira que o [método GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) em [Implementando IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).

### <a name="getencoderinfo"></a>GetEncoderInfo

[**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) retorna um [**objeto IWICBitmapEncoderInfo.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo) Para obter o objeto **IWICBitmapEncoderInfo,** basta passar o GUID do codificador para o [**método CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) [**em IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)e, em seguida, solicitar a interface **IWICBitmapEncoderInfo** nele.

Consulte o exemplo em [Implementando IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) em [GetDecoderInfo](-wic-imp-iwicbitmapdecoder.md).

### <a name="createnewframe"></a>Createnewframe

[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) é o equivalente do [**codificador GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) em [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder). Esse método retorna um [**objeto IWICBitmapFrameEncode,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) que é o objeto que realmente serializa os dados de imagem para um quadro específico dentro do contêiner.

Um dos benefícios do WIC (Windows Imaging Component) é que ele fornece uma camada de abstração para aplicativos que permitem que eles trabalhem com todos os formatos de imagem da mesma maneira. No entanto, nem todos os formatos de imagem são exatamente os mesmos. Alguns formatos de imagem têm recursos que outros não têm. Para que os aplicativos sejam capazes de aproveitar esses recursos exclusivos, é necessário fornecer uma maneira para o codec expô-los. Essa é a finalidade das opções do codificador. Se o codec dá suporte a qualquer opção de codificador, você deve criar um objeto [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que expõe as opções de codificador compatíveis e devolvê-lo no *parâmetro ppIEncoderOptions* desse método. O chamador pode usar esse objeto IPropertyBag2 para determinar quais opções de codificador o codec dá suporte. Se o chamador quiser especificar valores para qualquer uma das opções de codificador com suporte, ele atribuirá o valor à propriedade relevante no objeto IPropertyBag2 e o passará para o objeto [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) recém-criado em seu método Initialize.

Para criar uma inciação de um objeto [IPropertyBag2,](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) primeiro você precisa criar um struct PROPBAG2 para especificar cada opção de codificador compatível com o codificador e seu tipo de dados para cada propriedade. Em seguida, você deve implementar um objeto IPropertyBag2 que impõe os intervalos de valor para cada propriedade na gravação e reconcilia quaisquer valores conflitantes ou sobrepostos. Para conjuntos simples de opções de codificador não conflitantes, você pode invocar o método [**CreateEncoderPropertyBag,**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createencoderpropertybag) que criará um objeto IPropertyBag2 simples usando as propriedades especificadas em seu struct PROPBAG2. Você ainda deve impor os intervalos de valor. Para opções de codificador mais avançadas ou se você precisar reconciliar valores conflitantes, deverá escrever sua própria implementação de IPropertyBag2.


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



O WIC fornece um pequeno conjunto de opções de codificador canônico que são usadas por alguns dos formatos de imagem comuns. Todas as opções de codificador canônico são opcionais e codecs não são necessários para dar suporte a nenhuma delas. O motivo pelo qual eles são fornecidos como opções canônicas é porque muitos aplicativos expõem a interface do usuário para que os usuários especifiquem essas opções ao salvar um arquivo de imagem em um formato que dá suporte a eles. Fornecer uma maneira canônica de especificar essas opções facilita que os aplicativos os comuniquem aos codificadores de maneira consistente. As opções do codificador canônico são listadas na tabela a seguir.



| Opção do codificador     | Vartype  | Intervalo de valores               |
|--------------------|----------|---------------------------|
| Lossless           | BOOL da VT \_ | Verdadeiro/Falso                |
| ImageQuality       | VT \_ R4   | 0.0-1.0                   |
| CompressionQuality | VT \_ R4   | 0.0-1.0                   |
| BitmapTransform    | VT \_ UI1  | WICBitmapTransformOptions |



 

Se o codec dá suporte à codificação sem perda, você deve expor a opção de codificador sem perda como uma maneira de os aplicativos solicitarem que uma imagem seja codificada sem perda. Se um chamador define essa propriedade como True, você deve ignorar a opção ImageQuality e codificar a imagem sem perda.

A opção ImageQuality permite que um aplicativo especifique o grau de fidelidade com o qual codificar a imagem. Essa opção permite que um usuário faça uma troca entre a qualidade da imagem versus a velocidade e/ou o tamanho do arquivo. JPEG é um exemplo de um formato de imagem que dá suporte a essa troca. Um valor de 0,0 indica que a fidelidade é de baixa importância e o codificador deve usar seu algoritmo mais perdido. Um valor de 1,0 indica que a fidelidade é a mais importante e o codificador deve preservar a maior fidelidade possível. (Dependendo do codec, isso pode ser sinônimo da opção Sem perda. No entanto, se o codec for compatível com a codificação sem perda e se a opção Sem perda estiver definida como True, a opção ImageQuality deverá ser ignorada.)

A opção CompressionQuality permite que um aplicativo especifique a eficiência da compactação a ser usada ao codificar a imagem. Um algoritmo muito eficiente pode produzir um arquivo de imagem menor com a mesma qualidade que um algoritmo de compactação menos eficiente, mas pode levar mais tempo para codificar. Essa opção permite que um usuário especifique uma troca entre o tamanho do arquivo versus a velocidade da codificação, preservando o mesmo nível de qualidade. TIFF é um exemplo de um formato de imagem que dá suporte a essa troca. (Observe que um formato como JPEG dá suporte a diferentes níveis de compactação, mas uma taxa mais alta de compactação resulta em menor qualidade de imagem. Portanto, um formato de imagem JPEG exporia a opção ImageQuality em vez da opção CompressionQuality.) Um valor de 0,0 para essa opção indica que você deve compactar a imagem o mais rápido possível, sem reduzir a fidelidade, às custas de um tamanho de arquivo maior. Um valor de 1,0 indica que você deve criar o menor tamanho de arquivo possível (no mesmo nível de qualidade), independentemente de quanto tempo pode levar para codá-lo. Um codec pode dar suporte à opção ImageQuality e à opção CompressionQuality, em que a opção ImageQuality especifica o grau aceitável de perda e a opção CompressionQuality oferece uma troca de tamanho/velocidade no nível de qualidade especificado.

A opção BitmapTransform fornece uma maneira para o chamador especificar um ângulo de rotação ou orientação de invasão vertical ou horizontal durante a codificação. A enum WICBitmapTransformOptions usada para especificar a transformação solicitada é a mesma enum usada ao solicitar uma transformação durante a decodificação por meio da interface IWICBitmapSourceTransform.

Observe que os codificadores não estão limitados às opções do codificador canônico. A finalidade das opções do codificador é permitir que os codificadores exponham seus recursos e não há limite para os tipos de recursos que você pode expor. Certifique-se de que as opções do codificador estão bem documentadas. Embora um aplicativo possa usar o pacote de propriedades que você retorna desse método para descobrir os nomes, tipos e intervalos de valor para as opções que você dá suporte, a única maneira de descobrir seus significados ou como expô-los na interface do usuário é na documentação.

### <a name="commit"></a>Commit

[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) é o método que você chama depois que todos os dados de imagem e metadados foram serializados no fluxo. Você deve usar esse método para serializar os dados da imagem de visualização no fluxo e quaisquer miniaturas globais, metadados, paleta ou outros itens, se aplicável. Esse método não deve fechar o fluxo de arquivos, pois espera-se que o aplicativo que abriu o fluxo o feche.

A seção no método IWICBitmapFrameEncode:Commit tem detalhes sobre como o IWICBitmapEncoderCacheOptions afeta o comportamento desse método.

### <a name="setpreview"></a>SetPreview

[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) é usado para criar uma visualização da imagem. Embora não seja estritamente necessário que cada imagem tenha uma versão prévia, é altamente recomendável. Câmeras digitais modernas e scanners geram imagens de resolução muito alta, que tendem a ser muito grandes e, consequentemente, levam um tempo significativo de processamento para decodificar. As imagens da próxima geração de câmeras serão ainda maiores. É uma boa ideia fornecer uma versão de resolução menor e inferior de uma imagem, normalmente no formato JPEG, que pode ser rapidamente decodificada e exibida "instantaneamente" quando um usuário a solicita. Um aplicativo pode solicitar uma visualização antes de solicitar que a imagem real seja decodificada para fornecer uma experiência melhor para os usuários e mostrar a eles uma representação de tamanho de tela da imagem enquanto eles estão aguardando para decodificar a imagem real. Embora os codecs devem fornecer visualizações, os codecs que não dão suporte a [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) devem fazer isso definitivamente.

Se você fornecer uma versão prévia JPEG, não será preciso escrever um codificador JPEG para codiá-lo. Você deve delegar ao codificador JPEG que acompanha a plataforma WIC para codificação de visualizações e miniaturas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

[**Iwicbitmapframeencode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Interfaces do codificador](-wic-encoderinterfaces.md)
</dt> <dt>

[Implementando IWICBitmapCodecProgressNotification (Codificador)](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[Como escrever um codec WIC-Enabled código](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
