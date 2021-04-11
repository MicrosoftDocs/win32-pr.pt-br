---
description: Este tópico apresenta os requisitos para a criação de manipuladores de metadados personalizados para o Windows Imaging Component (WIC), incluindo leitores de metadados e gravadores.
ms.assetid: 08f1872b-6e4d-44ee-abc7-48685e435acc
title: Visão geral da extensibilidade de metadados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6576585f7f35628432504086695dd6c64091d3b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170307"
---
# <a name="metadata-extensibility-overview"></a>Visão geral da extensibilidade de metadados

Este tópico apresenta os requisitos para a criação de manipuladores de metadados personalizados para o Windows Imaging Component (WIC), incluindo leitores de metadados e gravadores. Ele também aborda os requisitos para estender a descoberta de componentes de tempo de execução do WIC para incluir manipuladores de metadados personalizados.

Este tópico inclui as seções a seguir.

-   [Pré-requisitos](#prerequisites)
-   [Introdução](#introduction)
-   [Criando um leitor de metadados](#creating-a-metadata-reader)
    -   [Interface IWICMetadataReader](#iwicmetadatareader-interface)
    -   [Interface IWICPersistStream](#iwicpersiststream-interface)
    -   [Interface IWICStreamProvider](#iwicstreamprovider-interface)
-   [Criando um gravador de metadados](#creating-a-metadata-writer)
    -   [Interface IWICMetadataWriter](#iwicmetadatawriter-interface)
    -   [Interface IWICPersistStream](#iwicpersiststream-interface)
    -   [Interface IWICStreamProvider](#iwicstreamprovider-interface)
-   [Instalando e registrando um manipulador de metadados](#installing-and-registering-a-metadata-handler)
    -   [Chaves do registro do manipulador de metadados](#metadata-handler-registry-keys)
    -   [Leitores de metadados](#metadata-readers)
    -   [Gravadores de metadados](#metadata-writers)
    -   [Assinando um manipulador de metadados](#signing-a-metadata-handler)
-   [Considerações especiais](#special-considerations)
    -   [PROPVARIANTS](#propvariants)
    -   [Manipuladores 8BIM](#8bim-handlers)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites"></a>Pré-requisitos

Para entender este tópico, você deve ter uma compreensão aprofundada do WIC, de seus componentes e de metadados para imagens. Para obter mais informações sobre metadados do WIC, consulte a [visão geral dos metadados do WIC](-wic-about-metadata.md). Para obter mais informações sobre os componentes do WIC, consulte [visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md).

## <a name="introduction"></a>Introdução

Conforme discutido na [visão geral dos metadados do WIC](-wic-about-metadata.md), geralmente há vários blocos de metadados em uma imagem, cada um expondo diferentes tipos de informações em diferentes formatos de metadados. Para interagir com um formato de metadados inserido em uma imagem, um aplicativo deve usar um manipulador de metadados apropriado. O WIC fornece vários manipuladores de metadados (leitores de metadados e gravadores) que permitem que você leia e grave tipos específicos de metadados, como EXIF ou XMP.

Além dos manipuladores nativos fornecidos, o WIC fornece APIs que permitem criar novos manipuladores de metadados que participam da descoberta de componente em tempo de execução do WIC. Isso permite que os aplicativos que usam o WIC leiam e gravem seus formatos de metadados personalizados.

As etapas a seguir permitem que seus manipuladores de metadados participem da descoberta de metadados de tempo de execução do WIC.

-   Implemente uma classe de manipulador de leitor de metadados ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) que expõe as interfaces WIC necessárias para ler seu formato de metadados personalizado. Isso permite que os aplicativos baseados em WIC leiam o formato de metadados da mesma maneira que lêem formatos de metadados nativos.
-   Implemente uma classe de manipulador de gravador de metadados ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) que expõe as interfaces WIC necessárias para codificar seu formato de metadados personalizado. Isso permite que aplicativos baseados em WIC serializem seu formato de metadados em formatos de imagem com suporte.
-   Assine digitalmente e registre seus manipuladores de metadados. Isso permite que os manipuladores de metadados sejam descobertos em tempo de execução, combinando o padrão de identificação no registro com o padrão inserido no arquivo de imagem.

## <a name="creating-a-metadata-reader"></a>Criando um leitor de metadados

O principal acesso aos blocos de metadados em um codec é por meio da interface [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) implementada por cada codec do WIC. Essa interface enumera cada um dos blocos de metadados inseridos em um formato de imagem para que o manipulador de metadados apropriado possa ser descoberto e instanciado para cada bloco. Os blocos de metadados que não são reconhecidos pelo WIC são considerados desconhecidos e definidos como o CLSID WICUnknownMetadataReader do GUID \_ . Para que seu formato de metadados seja reconhecido pelo WIC, você deve criar uma classe que implemente três interfaces: [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)e [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).

> [!Note]  
> Se o formato de metadados tiver restrições que processem alguns métodos das interfaces necessárias inadequadas, esses métodos devem retornar WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.

 

### <a name="iwicmetadatareader-interface"></a>Interface IWICMetadataReader

A interface [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) deve ser implementada ao criar um leitor de metadados. Essa interface fornece acesso ao sob a lista de itens de metadados dentro do fluxo de dados de um formato de metadados.

O código a seguir mostra a definição da interface do leitor de metadados, conforme definido no arquivo wincodecsdk. idl.

``` syntax
interface IWICMetadataReader : IUnknown
{
    HRESULT GetMetadataFormat(
        [out] GUID *pguidMetadataFormat
        );

    HRESULT GetMetadataHandlerInfo(
        [out] IWICMetadataHandlerInfo **ppIHandler
        );

    HRESULT GetCount(
        [out] UINT *pcCount
        );

    HRESULT GetValueByIndex(
        [in] UINT nIndex,
        [in, out, unique] PROPVARIANT *pvarSchema,
        [in, out, unique] PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetEnumerator(
        [out] IWICEnumMetadataItem **ppIEnumMetadata
        );
};
```

O método **GetMetadataFormat** retorna o GUID do seu formato de metadados.

O método **GetMetadataHandlerInfo** retorna uma interface [**IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) que fornece informações sobre o manipulador de metadados. Isso inclui informações como quais formatos de imagem dão suporte ao formato de metadados e se o leitor de metadados requer acesso ao fluxo de metadados completo.

O método **GetCount** retorna o número de itens de metadados individuais (incluindo blocos de metadados inseridos) encontrados no fluxo de metadados.

O método **GetValueByIndex** retorna um item de metadados por um valor de índice. Esse método permite que os aplicativos executem um loop em cada item de metadados em um bloco de metadados. O código a seguir demonstra como um aplicativo pode usar esse método para recuperar cada item de metadados em um bloco de metadados.


```C++
PROPVARIANT readerValue;
IWICMetadataBlockReader *blockReader = NULL;
IWICMetadataReader *reader = NULL;

PropVariantInit(&readerValue);

hr = pFrameDecode->QueryInterface(IID_IWICMetadataBlockReader, (void**)&blockReader);

if (SUCCEEDED(hr))
{
    // Retrieve the third block in the image. This is image specific and
    // ideally you should call this by retrieving the reader count
    // first.
    hr = blockReader->GetReaderByIndex(2, &reader);
}

if (SUCCEEDED(hr))
{
    UINT numValues = 0;

    hr = reader->GetCount(&numValues);

    // Loop through each item and retrieve by index
    for (UINT i = 0; SUCCEEDED(hr) && i < numValues; i++)
    {
        PROPVARIANT id, value;

        PropVariantInit(&id);
        PropVariantInit(&value);

        hr = reader->GetValueByIndex(i, NULL, &id, &value);

        if (SUCCEEDED(hr))
        {
            // Do something with the metadata item.
            //...
        }
        PropVariantClear(&id);
        PropVariantClear(&value);
    }               
}
```



O método **GetValue** recupera um item de metadados específico por esquema e/ou ID. Esse método é semelhante ao método **GetValueByIndex** , exceto que ele recupera um item de metadados que tem um esquema ou ID específico.

O método **GetEnumerator** retorna um enumerador de cada item de metadados no bloco de metadados. Isso permite que os aplicativos usem um enumerador para navegar no formato de metadados.

Se o formato de metadados não tiver uma noção de esquemas para itens de metadados, o método GetValue... os métodos devem ignorar essa propriedade. No entanto, se o formato der suporte à nomenclatura de esquema, você deverá prever um valor **nulo** .

Se um item de metadados for um bloco de metadados inserido, crie um manipulador de metadados do Subfluxo do conteúdo inserido e retorne o novo manipulador de metadados. Se não houver nenhum leitor de metadados disponível para o bloco aninhado, crie uma instância e retorne um leitor de metadados desconhecido. Para criar um novo leitor de metadados para o bloco inserido, chame os métodos **CreateMetadataReaderFromContainer** ou **CreateMetadataReader** da fábrica de componentes ou chame a função [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) .

Se o fluxo de metadados contiver conteúdo big endian, o leitor de metadados será responsável por trocar os valores de dados que ele processa. Também é responsável por informar quaisquer leitores de metadados aninhados que estejam trabalhando com o fluxo de dados big-endian. No entanto, todos os valores devem ser retornados no formato little-endian.

Implemente o suporte para navegação de namespace ao dar suporte a consultas em que a ID do item de metadados é um `VT_CLSID` (um GUID) correspondente a um formato de metadados. Se um leitor de metadados aninhado para esse formato for identificado durante a análise, ele deverá ser retornado. Isso permite que os aplicativos usem um leitor de consulta de metadados para pesquisar o formato de metadados.

Ao obter um item de metadados por ID, você deve usar a [função PropVariantChangeType](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) para forçar a ID para o tipo esperado. Por exemplo, o leitor IFD forçará uma ID a digitar `VT_UI2` para coincidir com o tipo de dados de uma ID de etiqueta IFD ushort. O tipo de entrada e o tipo esperado devem ser [PROPVARIANTdos](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) para fazer isso. Isso não é necessário, mas fazer essa coerção simplifica o código que chama o leitor para consultar itens de metadados.

### <a name="iwicpersiststream-interface"></a>Interface IWICPersistStream

A interface [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) herda de **IPersistStream** e fornece métodos adicionais para salvar e carregar objetos usando a enumeração [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .

O código a seguir mostra a definição da interface [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) , conforme definido no arquivo wincodecsdk. idl.

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

O método **LoadEx** fornece o leitor de metadados com um fluxo de dados que contém o seu bloco de metadados. Seu leitor analisa esse fluxo para acessar os itens de metadados subjacentes. O leitor de metadados é inicializado com um subfluxo que está posicionado no início do conteúdo de metadados brutos. Se o leitor não exigir o fluxo completo, o Subfluxo será limitado no intervalo para apenas o conteúdo do bloco de metadados; caso contrário, o fluxo de metadados completo é fornecido com a posição definida no início do seu bloco de metadados.

O método **SaveEx** é usado pelos gravadores de metadados para serializar o bloco de metadados. Quando **SaveEx** é usado em um leitor de metadados, ele deve retornar WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.

### <a name="iwicstreamprovider-interface"></a>Interface IWICStreamProvider

A interface [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) permite que o leitor de metadados forneça referências ao seu fluxo de conteúdo, forneça informações sobre o fluxo e atualize as versões em cache do fluxo.

O código a seguir mostra a definição da interface [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) , conforme definido no arquivo wincodecsdk. idl.

``` syntax
interface IWICStreamProvider : IUnknown
{
    HRESULT GetStream(
        [out] IStream **ppIStream
        );

    HRESULT GetPersistOptions(
        [out] DWORD *pdwPersistOptions
        );

    HRESULT GetPreferredVendorGUID(
        [out] GUID *pguidPreferredVendor
        );

    HRESULT RefreshStream(
        );
};
```

O método **GetStream** recupera uma referência para o fluxo de metadados. O fluxo retornado deve ter o ponteiro de fluxo redefinido para a posição inicial. Se o formato de metadados exigir acesso total ao fluxo, a posição inicial deverá ser o início do seu bloco de metadados.

O método **persisteoptions** retorna as opções atuais do fluxo da enumeração [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .

O método **GetPreferredVendorGUID** retorna o GUID do fornecedor do leitor de metadados.

O método **RefreshStream** atualiza o fluxo de metadados. Esse método deve chamar **LoadEx** com um fluxo **nulo** para todos os blocos de metadados aninhados. Isso é necessário porque os blocos de metadados aninhados e seus itens podem não existir mais, devido à edição in-loco.

## <a name="creating-a-metadata-writer"></a>Criando um gravador de metadados

Um gravador de metadados é um tipo de manipulador de metadados que fornece uma maneira de serializar um bloco de metadados para um quadro de imagem ou fora de um quadro individual se o formato de imagem der suporte a ele. O principal acesso aos gravadores de metadados dentro de um codec é por meio da interface [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) que cada codificador de WIC implementa. Essa interface permite que os aplicativos enumerem cada um dos blocos de metadados inseridos em uma imagem para que o gravador de metadados apropriado possa ser descoberto e instanciado para cada bloco de metadados. Os blocos de metadados que não têm um gravador de metadados correspondente são considerados desconhecidos e são definidos como o CLSID WICUnknownMetadataReader do GUID \_ . Para permitir que os aplicativos habilitados para WIC serializem e gravem seu formato de metadados, você deve criar uma classe que implemente as seguintes interfaces: [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter), [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)e [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).

> [!Note]  
> Se o formato de metadados tiver restrições que processem alguns métodos das interfaces necessárias inadequadas, esses métodos devem retornar WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.

 

### <a name="iwicmetadatawriter-interface"></a>Interface IWICMetadataWriter

A interface [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) deve ser implementada pelo seu gravador de metadados. Além disso, como **IWICMetadataWriter** é herdado de [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), você também deve implementar todos os métodos de **IWICMetadataReader**. Como ambos os tipos de manipulador exigem a mesma herança de interface, talvez você queira criar uma única classe que forneça a funcionalidade de leitura e gravação.

O código a seguir mostra a definição da interface do gravador de metadados, conforme definido no arquivo wincodecsdk. idl.

``` syntax
interface IWICMetadataWriter : IWICMetadataReader
{
    HRESULT SetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT SetValueByIndex(
        [in] UINT nIndex,
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT RemoveValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId
        );

    HRESULT RemoveValueByIndex(
        [in] UINT nIndex
        );
};
```

O método **SetValue** grava o item de metadados especificado para o fluxo de metadados.

O método **SetValueByIndex** grava o item de metadados especificado no índice especificado no fluxo de metadados. O índice não se refere à ID, mas à posição do item dentro do bloco de metadados.

O método **removervalue** remove o item de metadados especificado do fluxo de metadados.

O método **RemoveValueByIndex** remove o item de metadados no índice especificado do fluxo de metadados. Depois de remover um item, espera-se que os itens de metadados restantes ocupem o índice vagado se o índice não for o último índice. Também é esperado que a contagem seja alterada depois que o item for removido.

É responsabilidade do gravador de metadados converter os itens [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) na estrutura subjacente exigida pelo seu formato. No entanto, diferentemente do leitor de metadados, os tipos VARIAntes não devem ser normalmente impostos para tipos diferentes, pois o chamador está especificamente indicando qual tipo de dados usar.

O gravador de metadados deve confirmar todos os itens de metadados para o fluxo de imagem, incluindo valores ocultos ou não reconhecidos. Isso inclui blocos de metadados aninhados desconhecidos. No entanto, é responsabilidade do codificador definir quaisquer itens de metadados críticos antes de iniciar a operação de salvamento.

Se o fluxo de metadados contiver conteúdo big endian, o gravador de metadados será responsável por trocar os valores de dados que ele processa. Também é responsável por informar quaisquer gravadores de metadados aninhados que estejam trabalhando com um fluxo de dados big endian quando eles salvarem.

Implemente o suporte para a criação e remoção de namespace ao dar suporte a operações set e remove em itens de metadados com um tipo de `VT_CLSID` (um GUID) correspondente a um formato de metadados. O gravador de metadados chama a função [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) para inserir corretamente o conteúdo do gravador de metadados aninhado no gravador de metadados pai.

Se o formato de metadados oferecer suporte à codificação in-loco, você será responsável por gerenciar o preenchimento necessário. Para obter mais informações sobre codificação in-loco, consulte [visão geral dos metadados do WIC](-wic-about-metadata.md) e [visão geral da leitura e gravação de metadados de imagem](-wic-codec-readingwritingmetadata.md).

### <a name="iwicpersiststream-interface"></a>Interface IWICPersistStream

A interface [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) herda de **IPersistStream** e fornece métodos adicionais para salvar e carregar objetos usando a enumeração [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .

O código a seguir mostra a definição da interface [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) , conforme definido no arquivo wincodecsdk. idl.

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

O método **LoadEx** fornece o manipulador de metadados com um fluxo de dados que contém o bloco de metadados.

O método **SaveEx** serializa os metadados em um fluxo. Se o fluxo fornecido for o mesmo que o fluxo de inicialização, você deverá executar a codificação in-loco. Se houver suporte para codificação in-loco, esse método deverá retornar WINCODEC \_ Err \_ TOOMUCHMETADATA quando não houver preenchimento suficiente para executar a codificação in-loco. Se não houver suporte para codificação in-loco, esse método deverá retornar WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.

O método **IPersistStream:: GetSizeMax** deve ser implementado e deve retornar o tamanho exato do conteúdo de metadados que seria gravado na gravação subsequente.

O método **IPersistStream:: IsDirty** deve ser implementado se o gravador de metadados for inicializado por meio de um fluxo, para que uma imagem possa determinar de forma confiável se seu conteúdo foi alterado.

Se o formato de metadados oferecer suporte a blocos de metadados aninhados, o gravador de metadados deverá delegar aos gravadores de metadados aninhados a serialização de seu conteúdo ao salvar em um fluxo.

### <a name="iwicstreamprovider-interface"></a>Interface IWICStreamProvider

A implementação da interface [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) para um gravador de metadados é a mesma que a de um leitor de metadados. Para obter mais informações, consulte a seção criando um leitor de metadados neste documento.

## <a name="installing-and-registering-a-metadata-handler"></a>Instalando e registrando um manipulador de metadados

Para instalar um manipulador de metadados, você deve fornecer o assembly do manipulador e registrá-lo no registro do sistema. Você pode decidir como e quando as chaves do registro são populadas.

> [!Note]  
> Para facilitar a leitura, os GUIDs hexadecimais reais não são mostrados nas chaves do registro mostradas nas seções a seguir deste documento. Para localizar o valor hexadecimal para um nome amigável especificado, consulte os arquivos wincodec. idl e wincodecsdk. idl.

 

### <a name="metadata-handler-registry-keys"></a>Chaves do registro do manipulador de metadados

Cada manipulador de metadados é identificado por um CLSID exclusivo, e cada manipulador é necessário para registrar seu CLSID sob o GUID de ID de categoria do manipulador de metadados. A ID de categoria do tipo de manipulador é definida em wincodec. idl; o nome da ID da categoria para leitores é CATID \_ WICMetadataReader e o nome da ID de categoria para gravadores é CATID \_ WICMetadataWriter.

Cada manipulador de metadados é identificado por um CLSID exclusivo, e cada manipulador é necessário para registrar seu CLSID sob o GUID de ID de categoria do manipulador de metadados. A ID de categoria do tipo de manipulador é definida em wincodec. idl; o nome da ID da categoria para leitores é CATID \_ WICMetadataReader e o nome da ID de categoria para gravadores é CATID \_ WICMetadataWriter.

> [!Note]  
> Nas listagens de chave do registro a seguir, {Reader CLSID} refere-se ao CLSID exclusivo que você fornece para o leitor de metadados. {Writer CLSID} refere-se ao CLSID exclusivo que você fornece para o seu gravador de metadados. {Handler CLSID} refere-se ao CLSID do leitor, ao CLSID do gravador ou a ambos, dependendo de quais manipuladores você está fornecendo. {GUID de contêiner} refere-se ao objeto de contêiner (formato de imagem ou formato de metadados) que pode conter o bloco de metadados.

 

As chaves do registro a seguir registram seu manipulador de metadados com os outros manipuladores de metadados disponíveis:

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CATID_WICMetadataReaders}\Instance\{Reader CLSID}]
CLSID={Reader CLSID}
Friendly Name="Reader Name"

[HKEY_CLASSES_ROOT\CLSID\{CATID_ WICMetadataWriters}\Instance\{Writer CLSID}]
CLSID={Writer CLSID}
Friendly Name="Writer Name"
```

Além de registrar seus manipuladores em suas respectivas categorias, você também deve registrar chaves adicionais que fornecem informações específicas para o manipulador. Leitores e gravadores compartilham requisitos de chave de registro semelhantes. A sintaxe a seguir mostra como registrar um manipulador. O manipulador de leitor e o manipulador de gravador devem ser registrados dessa forma, usando seus respectivos CLSIDs:

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CLSID}]
"Vendor"={VendorGUID}
"Date"="yyyy-mm-dd"
"Version"="Major.Minor.Build.Number"
"SpecVersion"="Major.Minor.Build.Number"
"MetadataFormat"={MetadataFormatGUID}
"RequiresFullStream"=dword:1|0
"SupportsPadding"= dword:1|0
"FixedSize"=0

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\InProcServer32]
@="drive:\path\yourdll.dll"
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\{LCID}]
Author="Author's Name"
Description = " Metadata Description"
DeviceManufacturer ="Manufacturer Name"
DeviceModels="Device,Device"
FriendlyName="Friendly Name"
```

### <a name="metadata-readers"></a>Leitores de metadados

O registro do leitor de metadados também inclui chaves que descrevem como o leitor pode ser inserido em um formato de contêiner. Um formato de contêiner pode ser um formato de imagem como TIFF ou JPEG; Ele também pode ser outro formato de metadados, como um bloco de metadados IFD. Os formatos de contêiner de imagem com suporte nativo são listados em wincodec. idl; cada formato de contêiner de imagem é definido como um GUID com um nome que começa com GUID \_ containerFormat. Os formatos de contêiner de metadados com suporte nativo são listados em wincodecsdk. idl; cada formato de contêiner de metadados é definido como um GUID com um nome que começa com GUID \_ MetadataFormat.

As chaves a seguir registram um contêiner ao qual o leitor de metadados dá suporte e os dados necessários para a leitura desse contêiner. Cada contêiner com suporte do leitor deve ser registrado dessa maneira.

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Reader CLSID}\Containers\{Container GUID}\0]
"Position"=dword:00000000
"Pattern"=hex:ff,ff,ff,...
"Mask"=hex:ff,ff,ff,...
"DataOffset"=dword:00000006
```

A chave de padrão descreve o padrão binário que é usado para corresponder o bloco de metadados ao leitor. Ao definir um padrão para o leitor de metadados, ele deve ser confiável o suficiente para que uma correspondência positiva signifique que o leitor de metadados possa entender os metadados no bloco de metadados que está sendo processado.

A chave dataOffset descreve o deslocamento fixo dos metadados do cabeçalho de bloco. Essa chave é opcional e, se não for especificada, significa que os metadados reais não podem ser localizados usando um deslocamento fixo do cabeçalho de bloco.

### <a name="metadata-writers"></a>Gravadores de metadados

O registro do gravador de metadados também inclui chaves que descrevem como gravar o cabeçalho que precede o conteúdo de metadados inserido em um formato de contêiner. Assim como no leitor, um formato de contêiner pode ser um formato de imagem ou outro bloco de metadados.

As chaves a seguir registram um contêiner ao qual o gravador de metadados dá suporte e os dados necessários para gravar o cabeçalho e os metadados. Cada contêiner com suporte do gravador deve ser registrado dessa maneira.

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Writer CLSID}\Containers\{Container GUID}]
"WritePosition"=dword:00000000
"WriteHeader"=hex:ff,ff,ff,...
"WriteOffset"=dword:00000000
```

A chave WriteHeader descreve o padrão binário do cabeçalho do bloco de metadados a ser gravado. Esse padrão binário coincide com a chave de padrão de leitor do formato de metadados.

A chave WriteOffset descreve o deslocamento fixo do cabeçalho de bloco no qual os metadados devem ser gravados. Essa chave é opcional e, se não for especificada, significa que os metadados reais não devem ser gravados com o cabeçalho.

### <a name="signing-a-metadata-handler"></a>Assinando um manipulador de metadados

Todos os manipuladores de metadados devem ser assinados digitalmente para participar do processo de descoberta do WIC. O WIC não carregará nenhum manipulador que não esteja assinado por uma autoridade de certificação confiável. Para obter mais informações sobre a assinatura digital, consulte [introdução à assinatura de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).

## <a name="special-considerations"></a>Considerações especiais

As seções a seguir incluem informações adicionais que você deve considerar ao criar seus próprios manipuladores de metadados.

### <a name="propvariants"></a>PROPVARIANTS

O WIC usa um [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) para representar um item de metadados para leitura e gravação. Um PROPVARIANT fornece um tipo de dados e um valor de dados para um item de metadados usado em um formato de metadados. Como o gravador de um manipulador de metadados, você tem muita flexibilidade em como os dados são armazenados no formato de metadados e como os dados são representados em um bloco de metadados. A tabela a seguir fornece diretrizes para ajudá-lo a decidir sobre o tipo de PROPVARIANT apropriado a ser usado em situações diferentes.



| O tipo de metadados é...          | Usar tipo PROPVARIANT      | Propriedade PROPVARIANT                                                                                                                                                                                                                                                           |
|------------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vazio ou não existente.       | VT \_ vazio                 | Não aplicável.                                                                                                                                                                                                                                                                |
| Indefinido.                   | \_blob VT                  | Use a propriedade blob para definir o tamanho e o ponteiro para o objeto de BLOB alocado usando CoTaskMemAlloc.                                                                                                                                                                           |
| Um bloco de metadados.            | VT \_ desconhecido               | Esse tipo usa a propriedade punkVal.                                                                                                                                                                                                                                           |
| Uma matriz de tipos.           | \_Vetor VT \| VT \_ {Type}  | Use a propriedade CA {Type} para definir a contagem e o ponteiro para a matriz alocada usando CoTaskMemAlloc.                                                                                                                                                                            |
| Uma matriz de blocos de metadados. | \_variante de vetor \| VT \_ VT | Use a propriedade capropvar para definir a matriz de variantes.                                                                                                                                                                                                                       |
| Um valor racional assinado.     | VT \_ i8                    | Use a propriedade hVal para definir o valor. Defina a palavra alta para o denominador e a palavra inferior para o numerador.                                                                                                                                                                |
| Um valor racional.            | \_UI8 VT                   | Use a propriedade uhVal para definir o valor. Defina HighPart para o denominador e o LowPart para o numerador. Observe que o LowPart é um int não assinado. O numerador deve ser convertido de um int não assinado para um int para garantir que o bit de sinal seja preservado, se presente. |



 

Para evitar redundância na representação de itens de matriz, não use matrizes seguras; Use apenas matrizes simples. Isso reduz o trabalho que um aplicativo precisa executar ao interpretar os tipos de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Evite usar `VT_BYREF` e armazenar valores embutidos sempre que possível. `VT_BYREF` é ineficiente para tipos pequenos (comuns para itens de metadados) e não fornece informações de tamanho.

Antes de usar um [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), sempre chame **PropVariantInit** para inicializar o valor. Quando tiver terminado com o PROPVARIANT, sempre chame **PropVariantClear** para liberar qualquer memória alocada para a variável.

### <a name="8bim-handlers"></a>Manipuladores 8BIM

Ao gravar um manipulador de metadados para um bloco de metadados 8BIM, você deve usar uma assinatura que encapsula a assinatura 8BIM e a ID. Por exemplo, o leitor de metadados 8BIMIPTC nativo fornece as seguintes informações de registro para descoberta de leitor:

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{0010668C-0801-4DA6-A4A4-826522B6D28F}\Containers\{16100D66-8570-4BB9-B92D-FDA4B23ECE67}\0]
"Position"=dword:00000000
"Pattern"=hex:38,42,49,4d,04,04
"Mask"=hex:ff,ff,ff,ff,ff,ff
"DataOffset"=dword:00000006
```

O leitor do 8BIMIPTC tem um padrão registrado de 0x38, 0x42, 0x49, 0x4D, 0x04, 0x04. Os primeiros quatro bytes (0x38, 0x42, 0x49, 0x4D) são a assinatura 8BIM e os últimos dois bytes (0x04, 0x04) são a ID do registro IPTC.

Portanto, para escrever um leitor de metadados 8BIM para obter informações de resolução, você precisaria de um padrão registrado de 0x38, 0x42, 0x49, 0x4D, 0x03, 0xED. Novamente, os primeiros quatro bytes (0x38, 0x42, 0x49, 0x4D) são a assinatura 8BIM. Os últimos dois bytes (0x03, 0xED), no entanto, são a ID de informações de resolução, conforme definido pelo formato PSD.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Visão geral dos metadados do WIC](-wic-about-metadata.md)
</dt> <dt>

[Visão geral da linguagem de consulta de metadados](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Visão geral da leitura e gravação de metadados de imagem](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Como: codificar novamente uma imagem JPEG com metadados](-wic-codec-jpegmetadataencoding.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
