---
description: este tópico fornece uma visão geral de como você pode usar as APIs do componente de Windows Imaging (WIC) para ler e gravar metadados inseridos em arquivos de imagem.
ms.assetid: b1e0b936-a13a-42dd-8470-957ba1d90423
title: Visão geral da leitura e gravação de metadados de imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 191ffbe919e09acb153505fd3b43b50453b67708259206bffe66a0322d485a1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088128"
---
# <a name="overview-of-reading-and-writing-image-metadata"></a>Visão geral da leitura e gravação de metadados de imagem

este tópico fornece uma visão geral de como você pode usar as APIs do componente de Windows Imaging (WIC) para ler e gravar metadados inseridos em arquivos de imagem.

Este tópico inclui as seções a seguir.

-   [Pré-requisitos](#prerequisites)
-   [Introdução](#introduction)
-   [Lendo Metadadata usando um leitor de consulta](#reading-metadadata-using-a-query-reader)
    -   [Obtendo um leitor de consulta](#obtaining-a-query-reader)
    -   [Lendo metadados](#reading-metadata)
    -   [Métodos adicionais de leitura de consulta](#additional-query-reader-methods)
-   [Gravando metadados usando um gravador de consulta](#writing-metadata-using-a-query-writer)
    -   [Obtendo um gravador de consulta](#obtaining-a-query-writer)
    -   [Adicionando metadados](#adding-metadata)
    -   [Removendo metadados](#removing-metadata)
    -   [Copiando metadados para nova codificação](#copying-metadata-for-re-encoding)
-   [Codificação rápida de metadados](#fast-metadata-encoding)
    -   [Adicionando preenchimento a blocos de metadados](#adding-padding-to-metadata-blocks)
    -   [Obtendo um codificador de metadados rápido](#obtaining-a-fast-metadata-encoder)
    -   [Usando o codificador de metadados rápido](#using-the-fast-metadata-encoder)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites"></a>Pré-requisitos

Para entender este tópico, você deve estar familiarizado com o sistema de metadados do WIC, conforme descrito na [visão geral dos metadados do WIC](-wic-about-metadata.md). Você também deve estar familiarizado com a linguagem de consulta usada para ler e gravar metadados, conforme descrito em [visão geral da linguagem de consulta de metadados](-wic-codec-metadataquerylanguage.md).

## <a name="introduction"></a>Introdução

O WIC fornece aos desenvolvedores de aplicativos componentes de Component Object Model (COM) para ler e gravar metadados inseridos em arquivos de imagem. Há duas maneiras de ler e gravar metadados:

-   Usando um leitor de consulta/gravador e uma expressão de consulta para consultar blocos de metadados para blocos aninhados ou metadados específicos em um bloco.
-   Usar um manipulador de metadados (um leitor de metadados ou um gravador de metadados) para acessar os blocos de metadados aninhados ou metadados específicos nos blocos de metadados.

O mais fácil é usar um leitor de consulta/gravador e uma expressão de consulta para acessar os metadados. Um leitor de consulta ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) é usado para ler metadados enquanto um gravador de consulta ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) é usado para gravar metadados. Ambos usam uma expressão de consulta para ler ou gravar os metadados desejados. Nos bastidores, um leitor de consulta (e gravador) usa um manipulador de metadados para acessar os metadados descritos pela expressão de consulta.

O método mais avançado é acessar diretamente os manipuladores de metadados. Um manipulador de metadados é obtido dos quadros individuais usando um leitor de bloco ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) ou um gravador de bloco ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)). Os dois tipos de manipuladores de metadados disponíveis são o leitor de metadados ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) e o gravador de metadados ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).

O diagrama a seguir do conteúdo de um arquivo de imagem JPEG é usado em todos os exemplos neste tópico. A imagem representada por este diagrama foi criada usando Microsoft Paint; os metadados de classificação foram adicionados usando o recurso galeria de fotos do Windows Vista.

![ilustração de imagem JPEG com metadados de classificação](graphics/jpeg.png)

## <a name="reading-metadadata-using-a-query-reader"></a>Lendo Metadadata usando um leitor de consulta

A maneira mais fácil de ler metadados é usar a interface do leitor de consulta, [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader). O leitor de consulta permite que você leia blocos de metadados e itens dentro de blocos de metadados usando uma expressão de consulta.

Há três maneiras de obter um leitor de consulta: por meio de um decodificador de bitmap ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)), por meio de seus quadros individuais ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) ou por meio de um gravador de consulta ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).

### <a name="obtaining-a-query-reader"></a>Obtendo um leitor de consulta

O código de exemplo a seguir mostra como obter um decodificador de bitmap do alocador de imagens e recuperar um quadro de bitmap individual. Esse código também executa o trabalho de configuração necessário para obter um leitor de consulta de um quadro decodificado.


```
IWICImagingFactory *pFactory = NULL;
IWICBitmapDecoder *pDecoder = NULL;
IWICBitmapFrameDecode *pFrameDecode = NULL;
IWICMetadataQueryReader *pQueryReader = NULL;
IWICMetadataQueryReader *pEmbedReader = NULL;
PROPVARIANT value;

// Initialize COM
CoInitialize(NULL);

// Initialize PROPVARIANT
PropVariantInit(&value);

//Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_IWICImagingFactory,
    (LPVOID*)&pFactory);

// Create the decoder
if (SUCCEEDED(hr))
{
    hr = pFactory->CreateDecoderFromFilename(
        L"test.jpg",
        NULL,
        GENERIC_READ,
        WICDecodeMetadataCacheOnDemand,
        &pDecoder);
}

// Get a single frame from the image
if (SUCCEEDED(hr))
{
    hr = pDecoder->GetFrame(
         0,  //JPEG has only one frame.
         &pFrameDecode); 
}
```



O decodificador de bitmap para o arquivo de test.jpg é obtido usando o método **CreateDecoderFromFilename** da fábrica de imagens. Nesse método, o quarto parâmetro é definido como o valor WICDecodeMetadataCacheOnDemand da enumeração [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) . Isso informa ao decodificador para armazenar em cache os metadados quando os metadados são necessários; seja obtendo um leitor de consulta ou o leitor de metadados subjacente. O uso dessa opção permite que você retenha o fluxo para os metadados necessários para a codificação de metadados rápida e permite a decodificação sem perdas da imagem JPEG. Como alternativa, você pode usar o outro valor **WICDecodeOptions** , WICDecodeMetadataCacheOnLoad, que armazena em cache os metadados da imagem inserida assim que a imagem é carregada.

Para obter o leitor de consulta do quadro, faça uma chamada simples para o método **GetMetadataQueryReader** do quadro. O código a seguir demonstra essa chamada.


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



Da mesma forma, um leitor de consulta também pode ser obtido no nível do decodificador. Uma chamada simples para o método **GetMetadataQueryReader** do decodificador Obtém o leitor de consulta do decodificador. O leitor de consulta de um decodificador, diferente do leitor de consulta de um quadro, lê os metadados de uma imagem que está fora dos quadros individuais. No entanto, esse cenário não é comum e os formatos de imagem nativa não oferecem suporte a esse recurso. Os CODECs de imagem nativa fornecidos pelos metadados de leitura e gravação do WIC no nível do quadro, mesmo para formatos de quadro único, como JPEG.

### <a name="reading-metadata"></a>Lendo metadados

Antes de prosseguir para realmente ler os metadados, examine o diagrama a seguir de um arquivo JPEG que inclui blocos de metadados incorporados e dados reais a serem recuperados. Este diagrama fornece textos explicativos para blocos de metadados específicos e itens dentro da imagem, fornecendo a expressão de consulta de metadados para cada bloco ou item.

![ilustração de imagem JPEG com textos explicativos de metadados](graphics/jpegwithcallouts.png)

Para consultar blocos de metadados inseridos ou itens específicos por nome, chame o método **GetMetadataByName** . Esse método usa uma expressão de consulta e um [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) no qual o item de metadados é retornado. O código a seguir consulta um bloco de metadados aninhado e converte o componente [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) fornecido pelo valor PROPVARIANT em um leitor de consulta, se encontrado.


```
if (SUCCEEDED(hr))
{
    // Get the nested IFD reader
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd", &value);
    if (value.vt == VT_UNKNOWN)
    {
        hr = value.punkVal->QueryInterface(IID_IWICMetadataQueryReader, (void **)&pEmbedReader);
    }
    PropVariantClear(&value); // Clear value for new query
}
```



A expressão de consulta "/app1/IFD" está consultando o bloco IFD aninhado no bloco App1. O arquivo de imagem JPEG contém o bloco de metadados aninhado IFD, portanto, o [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) é retornado com um tipo de variável (VT) de `VT_UNKNOWN` e um ponteiro para uma interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) (punkVal). Em seguida, você consulta a interface IUnknown para um leitor de consulta.

O código a seguir demonstra uma nova consulta com base no novo leitor de consulta relativo ao bloco de IFD aninhado.


```
if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetMetadataByName(L"/{ushort=18249}", &value);
    PropVariantClear(&value); // Clear value for new query
}
```



A expressão de consulta "/{UShort = 18249}" consulta o bloco IFD para a classificação MicrosoftPhoto inserida na marca 18249. O valor de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) agora conterá um tipo de valor de `VT_UI2` e um valor de dados de 50.

No entanto, não é necessário obter um bloco aninhado antes de consultar valores de dados específicos. Por exemplo, em vez de consultar a IFD aninhada e, em seguida, para a classificação MicrosoftPhoto, você pode usar o bloco de metadados raiz e a consulta mostrada no código a seguir para obter as mesmas informações.


```
if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);
    PropVariantClear(&value);
}
```



Além de consultar itens de metadados específicos em um bloco de metadados, você também pode enumerar todos os itens de metadados em um bloco de metadados (não incluindo itens de metadados em blocos de metadados aninhados). Para enumerar os itens de metadados no bloco atual, o método **Getenumeration** do leitor de consulta é usado. Esse método obtém uma interface **IEnumString** populada com os itens de metadados no bloco atual. Por exemplo, o código a seguir enumera a classificação XMP e a classificação MicrosoftPhoto para o bloco de IFD aninhado que foi obtido anteriormente.


```
IEnumString *metadataItems = NULL;

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetEnumerator(&metadataItems);
}
```



Para obter mais informações sobre como identificar marcas apropriadas para vários formatos de imagem e formatos de metadados, consulte [consultas de metadados de formato de imagem nativa](-wic-native-image-format-metadata-queries.md).

### <a name="additional-query-reader-methods"></a>Métodos adicionais de leitura de consulta

Além de ler metadados, você também pode obter informações adicionais sobre o leitor de consulta e obter metadados por meio de outros meios. O leitor de consulta fornece dois métodos que fornecem informações sobre o leitor de consulta, **GetContainerFormat** e **getLocation**.

Com o leitor de consulta incorporado, você pode usar **GetContainerFormat** para determinar o tipo de bloco de metadados e pode chamar **getLocation** para obter o caminho relativo ao bloco de metadados raiz. O código a seguir consulta o leitor de consulta inserido para sua localização.


```
// Determine the metadata block format

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetContainerFormat(&containerGUID);
}

// Determine the query reader's location
if (SUCCEEDED(hr))
{
    UINT length;
    WCHAR readerNamespace[100];
    hr = pEmbedReader->GetLocation(100, readerNamespace, &length);
}
```



A chamada para **GetContainerFormat** para o leitor de consulta inserida retorna o GUID do formato de metadados IFD. A chamada para **getLocation** retorna um namespace de "/app1/IFD"; fornecendo o caminho relativo do qual as consultas subsequentes para o novo leitor de consulta serão executadas. É claro que o código anterior não é muito útil, mas demonstra como usar o método **getLocation** para localizar blocos de metadados aninhados.

## <a name="writing-metadata-using-a-query-writer"></a>Gravando metadados usando um gravador de consulta

> [!Note]  
> Alguns dos exemplos de código fornecidos nesta seção não são mostrados no contexto das etapas reais necessárias para gravar metadados. Para exibir os exemplos de código no contexto de um exemplo de trabalho, consulte o tutorial como: codificar novamente uma imagem com metadados.

 

O componente principal para gravar metadados é o gravador de consulta ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)). O gravador de consulta permite que você defina e remova os blocos de metadados e os itens em um bloco de metadados.

Assim como o leitor de consultas, há três maneiras de obter um gravador de consulta: por meio de um codificador de bitmap ([**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)), por meio de seus quadros individuais ([**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)) ou por meio de um [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)(codificador de metadados rápido).

### <a name="obtaining-a-query-writer"></a>Obtendo um gravador de consulta

O gravador de consulta mais comum é para um quadro individual de um bitmap. Esse gravador de consulta define e remove os itens e os blocos de metadados de um quadro de imagem. Para obter o gravador de consulta de um quadro de imagem, chame o método **GetMetadataQueryWriter** do quadro. O código a seguir demonstra a chamada de método simples para obter o gravador de consulta de um quadro.


```
IWICMetadataQueryWriter &pFrameQWriter = NULL;

//Obtain a query writer from the frame.
hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
```



Da mesma forma, um gravador de consulta também pode ser obtido para o nível do codificador. Uma chamada simples para o método **GetMetadataQueryWriter** do codificador Obtém o gravador de consulta do codificador. O gravador de consulta de um codificador, diferente do gravador de consulta de um quadro, grava metadados para uma imagem fora do quadro individual. No entanto, esse cenário não é comum e os formatos de imagem nativa não suportam essa funcionalidade. Os codecs de imagem nativa fornecidos pelo WIC leem e escrevem metadados no nível do quadro, mesmo para formatos de quadro único, como JPEG.

Você também pode obter um autor de consulta diretamente da fábrica de imagens ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)). Há dois métodos de fábrica de imagens que retornam um autor de consulta: **CreateQueryWriter** e **CreateQueryWriterFromReader**.

**CreateQueryWriter** cria um autor de consulta para o formato de metadados e o fornecedor especificados. Esse autor de consulta permite que você escreva metadados para um formato de metadados específico e adicione-os à imagem. O código a seguir demonstra uma **chamada CreateQueryWriter** para criar um autor de consulta XMP.


```
IWICMetadataQueryWriter *pXMPWriter = NULL;

// Create XMP block
GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriter(
        GUID_MetadataFormatXMP,
        &vendor,
        &pXMPWriter);
```



Neste exemplo, o nome amigável `GUID_MetadataFormatXMP` é usado como o parâmetro *guidMetadataFormat.* Ele representa o GUID de formato de metadados XMP e o fornecedor representa o manipulador criado pela Microsoft. Como alternativa, **NULL** pode ser passado como o *parâmetro pguidVendor* com os mesmos resultados se nenhum outro manipulador XMP existir. Se um manipulador XMP personalizado for instalado junto com o manipulador XMP nativo, passar **NULL** para o fornecedor fará com que o autor da consulta com o GUID mais baixo seja retornado.

**CreateQueryWriterFromReader** é semelhante ao método **CreateQueryWriter,** exceto que ele pré-popula o novo autor de consultas com os dados fornecidos pelo leitor de consulta. Isso é útil para codificar uma imagem enquanto mantém os metadados existentes ou para remover metadados indesejados. O código a seguir demonstra uma **chamada CreateQueryWriterFromReader.**


```
hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

// Copy metadata using query readers
if(SUCCEEDED(hr) && pFrameQReader)
{
    IWICMetadataQueryWriter *pNewWriter = NULL;

    GUID vendor = GUID_VendorMicrosoft;
    hr = pFactory->CreateQueryWriterFromReader(
        pFrameQReader,
        &vendor,
        &pNewWriter);
```



### <a name="adding-metadata"></a>Adicionando metadados

Depois de obter um autor de consulta, você pode usá-lo para adicionar blocos de metadados e itens. Para gravar metadados, use o método **SetMetadataByName** do autor da consulta. **SetMetadataByName** aceita dois parâmetros: uma expressão de consulta (*wzName*) e um ponteiro para [um PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarValue*). A expressão de consulta define o bloco ou item a ser definido enquanto PROPVARIANT fornece o valor de dados real a ser definido.

O exemplo a seguir demonstra como adicionar um título usando o autor da consulta XMP obtido anteriormente usando o **método CreateQueryWriter.**


```
// Write metadata to the XMP writer
if (SUCCEEDED(hr))
{
    PROPVARIANT value;
    PropVariantInit(&value);

    value.vt = VT_LPWSTR;
    value.pwszVal = L"Metadata Test Image.";
   
    hr = pXMPWriter->SetMetadataByName(L"/dc:title", &value);

    PropVariantClear(&value);
}
```



Neste exemplo, o tipo de value (vt) é definido como , indicando que uma cadeia de caracteres `VT_LPWSTR` será usada como o valor de dados. Como *o tipo* do valor é uma cadeia de *caracteres, pwszVal* é usado para definir o título a ser usado. **SetMetadataByName** é chamado usando a expressão de consulta "/dc:title" e o [recém-definido PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant). A expressão de consulta usada indica que a propriedade title no esquema da câmera digital (dc) deve ser definida. Observe que a expressão não é "/xmp/dc:title"; isso porque o autor da consulta já é específico do XMP e não contém um bloco XMP inserido, que "/xmp/dc:title" sugeriria.

Até esse ponto, você não adicionou nenhum metadado a um quadro de imagem. Você simplesmente preencheu um autor de consultas com dados. Para adicionar a um quadro um bloco de metadados representado pelo autor da consulta, chame novamente **SetMetadataByName** usando o autor da consulta como o [valor de PROPVARIANT.](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) Isso efetivamente copia os metadados no autor da consulta para o quadro de imagem. O código a seguir demonstra como adicionar os metadados no autor da consulta XMP obtidos anteriormente ao bloco de metadados raiz de um quadro.


```
// Get the frame's query writer and write the XMP query writer to it
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);

    // Copy the metadata in the XMP query writer to the frame
    if (SUCCEEDED(hr))
    {
        PROPVARIANT value;

        PropVariantInit(&value);
        value.vt = VT_UNKNOWN;
        value.punkVal = pXMPWriter;
        value.punkVal->AddRef();

        hr = pFrameQWriter->SetMetadataByName(L"/", &value);

        PropVariantClear(&value);
    }
}
```



Neste exemplo, um tipo de valor (vt) de `VT_UNKOWN` é usado, indicando um tipo de valor de interface COM. O autor da consulta XMP (piXMPWriter) é usado como o valor de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), adicionando uma referência a ele usando o método AddRef. Por fim, o autor da consulta XMP é definido chamando o método **SetMetadataByName** do quadro e passando a expressão de consulta "/", indicando o bloco raiz e o PROPVARIANT recém-definido.

> [!Note]  
> Se o quadro já contiver o bloco de metadados que você está tentando adicionar, os metadados que você está adicionando serão adicionados e os metadados existentes serão substituídos.

 

### <a name="removing-metadata"></a>Removendo metadados

Um autor de consulta também permite remover metadados chamando o **método RemoveMetadataByName.** **RemoveMetadataByName** pega uma expressão de consulta e remove o bloco ou item de metadados, se ele existir. O código a seguir demonstra como remover o título que foi adicionado anteriormente.


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp/dc:title");
}
```



O código a seguir demonstra como remover todo o bloco de metadados XMP.


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp");
}
```



### <a name="copying-metadata-for-re-encoding"></a>Copiando metadados para codificação

> [!Note]  
> O código nesta seção é válido somente quando os formatos de imagem de origem e de destino são os mesmos. Você não pode copiar todos os metadados de uma imagem em uma única operação ao codificar para um formato de imagem diferente.

 

Para preservar metadados ao codificar uma imagem no mesmo formato de imagem, há métodos disponíveis para copiar todos os metadados em uma única operação. Cada uma dessas operações segue um padrão semelhante; cada define os metadados do quadro decodificado diretamente no novo quadro que está sendo codificado.

O método preferencial para copiar metadados é inicializar o bloqueador do novo quadro com o leitor de bloco do quadro decodificado. O código a seguir demonstra esse método.


```
if (SUCCEEDED(hr) && formatsEqual)
{
    // Copy metadata using metadata block reader/writer
    if (SUCCEEDED(hr))
    {
        pFrameDecode->QueryInterface(
            IID_IWICMetadataBlockReader,
            (void**)&pBlockReader);
    }
    if (SUCCEEDED(hr))
    {
        pFrameEncode->QueryInterface(
            IID_IWICMetadataBlockWriter,
            (void**)&pBlockWriter);
    }
    if (SUCCEEDED(hr))
    {
        pBlockWriter->InitializeFromBlockReader(pBlockReader);
    }
}
```



Neste exemplo, o leitor de bloco e o bloqueador são obtidos do quadro de origem e do quadro de destino, respectivamente. O bloqueador de blocos é inicializado do leitor de bloco. Isso inicializa o leitor de bloco com os metadados pré-populados do leitor de bloco.

Outro método para copiar metadados é gravar o bloco de metadados referenciado pelo leitor de consulta usando o autor da consulta do codificador. O código a seguir demonstra esse método.


```
if (SUCCEEDED(hr) && formatsEqual)
{
    hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

    // Copy metadata using query readers
    if(SUCCEEDED(hr))
    {
        hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
        if (SUCCEEDED(hr))
        {
            PropVariantClear(&value);
            value.vt=VT_UNKNOWN;
            value.punkVal=pFrameQReader;
            value.punkVal->AddRef();
            hr = pFrameQWriter->SetMetadataByName(L"/", &value);
            PropVariantClear(&value);
        }
    }
}
```



Aqui, um leitor de consulta é obtido do quadro decodificado e, em seguida, usado como o valor da propriedade [do PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) com um tipo de valor definido como VT \_ UNKNOWN. O autor da consulta para o codificador é obtido e a expressão de consulta "/" é usada para definir os metadados no caminho de navegação raiz. Você também pode usar esse método ao definir blocos de metadados aninhados, ajustando a expressão de consulta para o local desejado.

Da mesma forma, você pode criar um autor de consulta com base no leitor de consulta do quadro decodificado usando o método **CreateQueryWriterFromReader** da fábrica de imagens. O autor da consulta criado nesta operação será pré-populado com os metadados do leitor de consulta e poderá ser definido no quadro. O código a seguir demonstra a **operação de cópia CreateQueryWriterFromReader.**


```
IWICMetadataQueryWriter *pNewWriter = NULL;

GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriterFromReader(
    pFrameQReader,
    &vendor,
    &pNewWriter);

if (SUCCEEDED(hr))
{
    // Get the frame's query writer
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

// Set the query writer to the frame.
if (SUCCEEDED(hr))
{
    PROPVARIANT value;

    PropVariantInit(&value);
    value.vt = VT_UNKNOWN;
    value.punkVal = pNewWriter;
    value.punkVal->AddRef();
    hr = pFrameQWriter->SetMetadataByName(L"/",&value);
}
```



Esse método usa um autor de consulta separado criado com base nos dados do leitor de consulta. Em seguida, esse novo autor de consulta é definido no quadro.

Novamente, essas operações para copiar metadados só funcionam quando as imagens de origem e de destino têm o mesmo formato. Isso porque formatos de imagem diferentes armazenam os blocos de metadados em locais diferentes. Por exemplo, JPEG e TIFF são suportados por blocos de metadados XMP. Em imagens JPEG, o bloco XMP está no bloco de metadados raiz, conforme ilustrado na Visão geral de [metadados do WIC.](-wic-about-metadata.md) No entanto, em uma imagem TIFF, o bloco XMP é aninhado em um bloco IFD raiz. O diagrama a seguir ilustra as diferenças entre uma imagem JPEG e uma imagem TIFF com os mesmos metadados de classificação.

![Comparação jpeg e tiff.](graphics/jpgvstiff.png)

## <a name="fast-metadata-encoding"></a>Codificação rápida de metadados

Nem sempre é necessário codificar uma imagem para gravar novos metadados nele. Os metadados também podem ser gravados usando um codificador de metadados rápido. Um codificador de metadados rápido pode gravar uma quantidade limitada de metadados em uma imagem sem codificar a imagem. Isso é feito escrevendo os novos metadados no preenchimento vazio fornecido por alguns formatos de metadados. Os formatos de metadados nativos que suportam o preenchimento de metadados são Exif, IFD, GPS e XMP.

### <a name="adding-padding-to-metadata-blocks"></a>Adicionando preenchimento a blocos de metadados

Antes de executar a codificação de metadados rápida, deve haver espaço dentro do bloco de metadados para gravar mais metadados. Se não houver espaço suficiente no preenchimento existente para gravar os novos metadados, a codificação rápida de metadados falhará. Para adicionar preenchimento de metadados a uma imagem, a imagem deve ser codificada de forma nova. Você pode adicionar o preenchimento da mesma maneira que adicionaria qualquer outro item de metadados, usando uma expressão de consulta, se o bloco de metadados que você estiver padding dá suporte a ele. O exemplo a seguir demonstra como adicionar preenchimento a um bloco IFD inserido em um bloco App1.


```
if (SUCCEEDED(hr))
{
    // Add metadata padding
    PROPVARIANT padding;

    PropVariantInit(&padding);
    padding.vt = VT_UI4;
    padding.uiVal = 4096; // 4KB

    hr = pFrameQWriter->SetMetadataByName(L"/app1/ifd/PaddingSchema:padding", &padding);

    PropVariantClear(&padding);
}
```



Para adicionar preenchimento, crie um PROPVARIANT do tipo VT UI4 e um valor correspondente ao número de \_ bytes de preenchimento a adicionar. Um valor típico é 4096 bytes. As consultas de metadados para JPEG, TIFF e JPEG-XR estão nesta tabela.



| Formato de metadados | Consulta de metadados JPEG                  | Consulta de metadados TIFF, JPEG-XR    |
|-----------------|--------------------------------------|---------------------------------|
| IFD             | /app1/ifd/PaddingSchema:Padding      | /ifd/PaddingSchema:Padding      |
| Exif            | /app1/ifd/exif/PaddingSchema:Padding | /ifd/exif/PaddingSchema:Padding |
| Xmp             | /xmp/PaddingSchema:Padding           | /ifd/xmp/PaddingSchema:Padding  |
| GPS             | /app1/ifd/gps/PaddingSchema:Padding  | /ifd/gps/PaddingSchema:Padding  |



 

### <a name="obtaining-a-fast-metadata-encoder"></a>Obtendo um codificador de metadados rápido

Quando você tem uma imagem com preenchimento de metadados, um codificador de metadados rápido pode ser obtido usando os métodos de fábrica de imagens **CreateFastMetadataEncoderFromDecoder** e **CreateFastMetadataEncoderFromFrameDecode**.

Como o nome indica, **CreateFastMetadataEncoderFromDecoder** cria um codificador de metadados rápido para metadados no nível do decodificador. Os formatos de imagem nativa fornecidos pelo WIC não são suportados por metadados no nível do decodificador, mas esse método é fornecido caso esse formato de imagem seja desenvolvido no futuro.

O cenário mais comum é obter um codificador de metadados rápido de um quadro de imagem usando **CreateFastMetadataEncoderFromFrameDecode**. O código a seguir obtém o codificador de metadados rápidos de um quadro decodificado e altera o valor de classificação no bloco App1.


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode, 
        &pFME);
}
```



### <a name="using-the-fast-metadata-encoder"></a>Usando o Codificador de Metadados Rápidos

No codificador de metadados rápido, você pode obter um autor de consulta. Isso permite que você escreva metadados usando uma expressão de consulta conforme demonstrado anteriormente. Depois que os metadados foram definidos no autor da consulta, commit o codificador de metadados rápido para finalizar a atualização de metadados. O código a seguir demonstra a configuração e a confirmação das alterações de metadados


```
    if (SUCCEEDED(hr))
    {
        hr = pFME->GetMetadataQueryWriter(&pFMEQW);
    }

    if (SUCCEEDED(hr))
    {
        // Add additional metadata
        PROPVARIANT value;

        PropVariantInit(&value);

        value.vt = VT_UI4;
        value.uiVal = 99;
        hr = pFMEQW->SetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);

        PropVariantClear(&value);
    }

    if (SUCCEEDED(hr))
    {
        hr = pFME->Commit();
    }
}
```



Se **a** confirmação falhar por algum motivo, você precisará codificar a imagem de novo para garantir que os novos metadados são adicionados à imagem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Visão geral dos metadados do WIC](-wic-about-metadata.md)
</dt> <dt>

[Visão geral da linguagem de consulta de metadados](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Visão geral da extensibilidade de metadados](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Como codificar uma imagem JPEG com metadados](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 
