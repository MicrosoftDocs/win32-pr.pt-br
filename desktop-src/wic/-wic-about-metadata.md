---
description: Este tópico apresenta o suporte a metadados de imagens fornecido pelo WIC (Windows de imagens de imagem).
ms.assetid: 35727810-3c4c-4c11-a4a2-3ae2cf3b8142
title: Visão geral dos metadados do WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f5031759dd73861a97aace623b35f229b75952
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472022"
---
# <a name="wic-metadata-overview"></a>Visão geral dos metadados do WIC

Este tópico apresenta o suporte a metadados de imagens fornecido pelo WIC (Windows de imagens de imagem). Ele fornece uma introdução à leitura e à escrita de metadados de imagem, à linguagem de consulta de metadados e à extensibilidade do manipulador de metadados.

Os metadados de imagem são dados inseridos dentro de um arquivo de imagem que fornece informações adicionais sobre a imagem, como o dispositivo usado para capturar a imagem ou as dimensões da imagem. Embora ele seja contido no próprio arquivo de imagem, esses metadados não fazem parte dos dados de renderização. O WIC fornece interfaces que permitem que você leia e escreva esses metadados para vários formatos de metadados comuns, incluindo XMP (Extensible Metadata Platform), EXIF (Exchangeable Image File) e TEXt (Png Textual Data).

Este tópico inclui as seções a seguir.

-   [Pré-requisitos](#prerequisites)
-   [Introdução](#introduction)
-   [Lendo metadados de imagem](#reading-image-metadata)
-   [Escrevendo metadados de imagem](#writing-image-metadata)
-   [Extensibilidade de metadados](#metadata-extensibility)
-   [Formatos de metadados com suporte](#supported-metadata-formats)
-   [Resumo do componente de metadados](#metadata-component-summary)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites"></a>Pré-requisitos

Para entender este tópico, você deve estar familiarizado com as interfaces do codificador e do decodificador do WIC e seus componentes Component Object Model (COM) relacionados, conforme descrito na Visão geral do componente Windows [Imaging](-wic-about-windows-imaging-codec.md). Ele também ajuda a ter uma familiaridade geral com alguns dos formatos de metadados de imagens em uso atualmente.

## <a name="introduction"></a>Introdução

Os metadados fornece informações estendidas sobre uma imagem. Essas informações podem ser usadas de várias maneiras. Uma imagem pode conter metadados como uma descrição, classificação, marcas de categoria e informações de direitos autorais. O acesso aos metadados facilita a execução de tarefas como gerenciamento de ativos, local do arquivo ou determinação de informações de direitos autorais. Por exemplo, o Windows Galeria de Fotos no Windows Vista permite que você adicione descrições e marcas de categoria a imagens. Isso permite uma melhor descoberta de imagens e uma maneira conveniente de categorizar imagens. Usando as APIs do WIC e formatos de metadados comuns, os aplicativos podem facilmente gravar ou ler esse tipo de metadados de ou para imagens.

O diagrama a seguir ilustra o conteúdo de um arquivo JPEG que inclui blocos de metadados inseridos e itens de metadados.

![imagem jpeg com metadados de classificação](graphics/jpeg.png)

Nesta imagem de exemplo, os metadados são inseridos no arquivo de imagem dentro de um quadro de imagem. O formato JPEG não dá suporte a vários quadros de imagem, portanto, os metadados são conceitualmente anexados a esse único quadro. Formatos que suportam vários quadros, como TIFF, podem ter metadados anexados a cada quadro de imagem, como mostra este diagrama. Embora não seja comum atualmente e não tenha suporte dos codecs de imagem nativa, alguns formatos de imagem também podem dar suporte a metadados fora de um quadro de imagem. O WIC é flexível o suficiente para lidar com metadados no nível do quadro e metadados fora do quadro individual de uma imagem.

## <a name="reading-image-metadata"></a>Lendo metadados de imagem

As APIs do WIC fornecem componentes COM que facilitam para os aplicativos ler e gravar metadados de imagem.

A principal maneira de ler metadados é usar um leitor de consulta de metadados ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) para acessar itens de metadados específicos. O componente de leitor de consulta de metadados é implementado pelo codec e pode ser acessado no nível do decodificador ou por meio de quadros de imagem individuais, que é o método mais comum. O código a seguir demonstra como acessar um leitor de consulta para um quadro individual usando o método **GetMetadataQueryReader** do leitor de consulta.


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



Um leitor de consulta fornece métodos para obter informações sobre metadados específicos e um meio de especificar um item de metadados a ser recuperado. O código a seguir usa uma expressão de consulta para solicitar um item de metadados específico dentro do bloco IFD (diretório de arquivos de imagem aninhado) app1. Isso é feito usando o método **GetMetadataByName** do leitor de consulta. O código a seguir demonstra como usar o leitor de consulta para obter o valor de classificação MicrosoftPhoto.


```
PROPVARIANT value;
PropVariantInit(&value);

LPCWSTR pwzRatingQuery = L"/app1/ifd/{ushort=18249}";

if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(pwzRatingQuery, &value);
}
```



A variável pwzRatingQuery no exemplo anterior é a cadeia de caracteres de consulta para acessar o item de metadados MicrosoftPhoto rating. Essa cadeia de caracteres é criada usando a linguagem de consulta de metadados. Para criar essa cadeia de caracteres, o conhecimento do formato de metadados e da linguagem de consulta de metadados é necessário para recuperar itens de metadados individuais. Para obter mais informações sobre a linguagem de consulta de metadados, consulte Visão geral da linguagem [de consulta de metadados](-wic-codec-metadataquerylanguage.md).

Nos bastidores, um leitor de consulta usa um leitor de metadados ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) para acessar os metadados descritos pela expressão de consulta. Além de usar um leitor de consulta, você também pode acessar um leitor de metadados diretamente para ler metadados. Você pode obter um leitor de metadados do decodificador ou quadros individuais consultando uma interface de leitor de bloco ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)).

## <a name="writing-image-metadata"></a>Escrevendo metadados de imagem

O processo de escrita de metadados é semelhante à maneira como eles são lidos, exceto pelo fato de um autor de consulta de metadados ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) ser usado. A interface do codificador de consulta é implementada pelo codificador de imagem e, assim como no leitor de consulta, os metadados são acessados no codificador e em quadros individuais (dependendo do suporte ao formato de imagem).

O código a seguir demonstra como obter um autor de consulta de um quadro do codificador e remover o valor de classificação que foi lido anteriormente.


```
// Get the frame's query writer
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/app1/ifd/{ushort=18249}");
}
```



Outra maneira de gravar metadados é por meio de atualizações rápidas de metadados. A codificação rápida de metadados é uma maneira de gravar metadados de imagem sem precisar codificar um arquivo de imagem. Isso é feito escrevendo novas informações de metadados em uma região de preenchimento do formato de metadados. O codificador de metadados rápido ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) é obtido da fábrica de componentes, com base no decodificador de imagem. Em seguida, o codificador de metadados rápido obtém um autor de consulta usado para gravar os metadados. Por fim, o codificador rápido confirma a alteração.

O código a seguir demonstra como obter um codificador de metadados rápido e usá-lo para gravar o valor microsoftRating.


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode,
        &pFME);

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



Nem todos os formatos de metadados são suportados por metadados rápidos. Para ver quais formatos com suporte nativo são suportados para codificação rápida de metadados, consulte a tabela na seção [Formatos](#supported-metadata-formats) de metadados com suporte mais adiante neste documento.

Nos bastidores, um autor de consulta usa um autor de metadados ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) para gravar os metadados descritos pela expressão de consulta. Além de usar um leitor de consulta, você também pode acessar um gravação de metadados diretamente para gravar metadados. Você pode obter um autor de metadados do decodificador ou quadros individuais usando a consulta para uma interface de bloqueador ([**IWICMetadataBlockWriter).**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)

## <a name="metadata-extensibility"></a>Extensibilidade de metadados

Conforme mencionado anteriormente, o WIC fornece vários manipuladores de metadados para ler e gravar metadados para formatos de metadados comuns. No entanto, há alguns formatos de metadados que não têm suporte nativo. Portanto, o WIC fornece APIs para criar manipuladores de metadados adicionais que podem estender o suporte a metadados para outros formatos.

Para dar suporte total a outros formatos de metadados, dois tipos de manipuladores devem ser desenvolvidos – um leitor de metadados para ler metadados e um gravação de metadados para gravar metadados. Embora esses dois manipuladores geralmente sejam implementados em pares para um formato específico, isso não é um requisito. Pode haver alguns casos em que apenas a capacidade de leitura ou apenas a capacidade de gravação é necessária.

Para obter mais informações sobre extensibilidade de metadados usando as APIs do WIC, consulte a Visão [geral de extensibilidade de metadados](-wic-codec-metadatahandlers.md).

## <a name="supported-metadata-formats"></a>Formatos de metadados com suporte

O WIC dá suporte a vários formatos de metadados comuns. A tabela a seguir lista os formatos de metadados com suporte, suas versões, os formatos de imagem que suportam o formato de metadados e se o formato de metadados dá suporte à codificação rápida de metadados. Para obter mais informações sobre codificação rápida de metadados, consulte a seção [Escrevendo](#writing-image-metadata) metadados de imagem anteriormente neste documento.



| Formatos de metadados com suporte | Versão da especificação de metadados | Suporte ao formato de imagem | Dá suporte à codificação de metadados rápida |
|----------------------------|--------------------------------|----------------------|---------------------------------|
| App0                       | JFIF 1.02                      | JPEG                 | Não                              |
| Aplicativo1                       | JFIF 1.02                      | JPEG, TIFF           | Não                              |
| App13                      | Unknown                        | JPEG, TIFF           | Não                              |
| IFD                        | TIFF 6.0                       | JPEG, TIFF           | Sim                             |
| IRB                        | Unknown                        | JPEG, TIFF           | Não                              |
| Exif                       | EXIF 2,2                       | JPEG, TIFF           | Sim                             |
| XMP                        | XMP 1,0 (setembro de 2005)            | JPEG, TIFF           | Sim                             |
| GPS                        | EXIF 2,2                       | JPEG, TIFF           | Sim                             |
| IPTC                       | IPTC 4,0                       | JPEG, TIFF           | Sim                             |
| Texto                       | PNG 1,2                        | PNG                  | Não                              |



 

> [!Note]  
> O IPTC só dá suporte a FME se os blocos crescerem em tamanho, pois o IPTC não oferece suporte a preenchimento.

 

## <a name="metadata-component-summary"></a>Resumo do componente de metadados

A tabela a seguir descreve as interfaces WIC que dão suporte a metadados e seus componentes correspondentes. Esses componentes fornecem o acesso aos metadados de uma imagem. para obter mais informações sobre esses componentes, consulte a [visão geral do componente de Windows Imaging](-wic-about-windows-imaging-codec.md). 


| Componente | Descrição | 
|-----------|-------------|
| Decodificador de bitmap (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>) | <ul><li>Lê um fluxo de imagem e produz uma fonte de bitmap utilizável. Associado a um formato de contêiner, como TIFF (Tagged Image File Format) ou JPEG (grupo de especialistas fotográfico) conjunta.</li><li>Implementa uma interface <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> para enumerar todos os blocos de metadados no fluxo de dados do decodificador que não estão dentro de um quadro.</li><li>Expõe um leitor de consulta para ler os metadados associados à imagem que não está dentro de um quadro.</li></ul> | 
| Decodificação de quadros de bitmap (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>) | <ul><li>Acessa quadros individuais do fluxo de imagem mantido pelo decodificador.</li><li>Implementa uma interface <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> para enumerar todos os blocos de metadados no fluxo de dados do quadro.</li><li>Expõe um leitor de consulta para ler os metadados associados ao quadro, usando expressões de consulta.</li></ul> | 
| Codificador de bitmap (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>) | <ul><li>Grava uma origem de bitmap em um fluxo de imagem. Associado a um formato de contêiner como TIFF ou JPEG.</li><li>Implementa uma interface <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> para criar uma lista de blocos de metadados para gravar no fluxo de dados do codificador.</li><li>Expõe um gravador de consulta para gravar os metadados associados à imagem, usando expressões de consulta.</li></ul> | 
| Bitma frame Encode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>) | <ul><li>Cria um quadro que será codificado no fluxo mantido pelo codificador.</li><li>Implementa uma interface <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> para criar uma lista de blocos de metadados para gravar no fluxo de dados do quadro.</li><li>Expõe um gravador de consulta para gravar os metadados associados ao quadro, usando expressões de consulta.</li></ul> | 




 

A tabela a seguir descreve os componentes de metadados do WIC. Esses componentes permitem que você leia e grave os metadados em uma imagem exposta pelos componentes listados na tabela anterior. 


| Componente | Descrição | 
|-----------|-------------|
| Leitor de consulta de metadados (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>) | <ul><li>Usa uma cadeia de caracteres de consulta e navega pela hierarquia de metadados subjacente para obter metadados.</li></ul> | 
| Gravador de consulta de metadados (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>) | <ul><li>Usa uma cadeia de caracteres de consulta e navega pela hierarquia de metadados subjacente para obter, definir e remover metadados.</li></ul> | 
| Iniwicmetadatablockreader (leitor<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong></strong></a>de bloco de metadados) | <ul><li>Gerencia uma coleção somente leitura de objetos <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> na parte superior da hierarquia de metadados e habilita a enumeração de todos os blocos de metadados.</li><li>Implementado por um decodificador de bitmap e um quadro de bitmap decodificado.</li><li>Implementados por desenvolvedores de componentes de terceiros para codecs personalizados.</li></ul> | 
| Gravador de bloco de metadados (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>) | <ul><li>Gerencia uma coleção de leitura e gravação de objetos <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a> na parte superior da hierarquia de metadados.</li><li>Implementado por um codificador de bitmap e uma codificação de quadro de bitmap.</li><li>Implementados por desenvolvedores de componentes de terceiros para codecs personalizados.</li></ul> | 
| Leitor de metadados (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>) | <ul><li>Analisa um fluxo de metadados e gerencia uma coleção somente leitura dos itens de metadados. Associado a um formato de metadados como EXIF, IFD e XMP.</li><li>Atua como um dicionário, retornando um valor quando um par de formato e ID é fornecido.</li><li>Implementado por desenvolvedores de componentes de terceiros para tipos de metadados personalizados.</li></ul> | 
| Gravador de metadados (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>) | <ul><li>Analisa e serializa um fluxo de metadados e gerencia uma coleção de leitura/gravação de itens de metadados.</li><li>Implementado por desenvolvedores de componentes de terceiros para tipos de metadados personalizados.</li></ul> | 
| IWICFastMetadataEncoder do codificador de metadados rápidos<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong></strong></a> | <ul><li>Expõe a semântica para gravar em uma hierarquia de metadados que atualizará os metadados no local sem codificar novamente a imagem.</li></ul> | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Windows Visão geral do componente de geração de imagens](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Visão geral da linguagem de consulta de metadados](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Visão geral da leitura e gravação de metadados de imagem](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Visão geral da extensibilidade de metadados](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Como: codificar novamente uma imagem JPEG com metadados](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



