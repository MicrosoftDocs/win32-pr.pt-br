---
description: Este tópico apresenta o suporte a metadados de imagens fornecido pelo Windows Imaging Component (WIC).
ms.assetid: 35727810-3c4c-4c11-a4a2-3ae2cf3b8142
title: Visão geral dos metadados do WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f00e3a77eb74a3fb4a00db05ef9e00028f02ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551280"
---
# <a name="wic-metadata-overview"></a>Visão geral dos metadados do WIC

Este tópico apresenta o suporte a metadados de imagens fornecido pelo Windows Imaging Component (WIC). Ele fornece uma introdução à leitura e gravação de metadados de imagem, à linguagem de consulta de metadados e à extensibilidade do manipulador de metadados.

Metadados de imagem são dados inseridos dentro de um arquivo de imagem que fornece informações adicionais sobre a imagem, como o dispositivo usado para capturar a imagem ou as dimensões da imagem. Embora esteja contido no próprio arquivo de imagem, esses metadados não fazem parte dos dados de renderização. O WIC fornece interfaces que permitem que você leia e grave esses metadados para vários formatos de metadados comuns, incluindo XMP (Extensible Metadata Platform), EXIF (arquivo de imagem intercambiável) e dados textuais de png (texto).

Este tópico inclui as seções a seguir.

-   [Pré-requisitos](#prerequisites)
-   [Introdução](#introduction)
-   [Lendo metadados de imagem](#reading-image-metadata)
-   [Gravando metadados de imagem](#writing-image-metadata)
-   [Extensibilidade de metadados](#metadata-extensibility)
-   [Formatos de metadados com suporte](#supported-metadata-formats)
-   [Resumo do componente de metadados](#metadata-component-summary)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites"></a>Pré-requisitos

Para entender este tópico, você deve estar familiarizado com as interfaces do codificador e do codificador do WIC e seus componentes COM (Component Object Model) relacionados, conforme descrito na [visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md). Também ajuda a ter uma familiaridade geral com alguns dos formatos de metadados de geração de imagens usados hoje em dia.

## <a name="introduction"></a>Introdução

Metadados fornecem informações estendidas sobre uma imagem. Essas informações podem ser usadas de várias maneiras. Uma imagem pode conter metadados como uma descrição, classificação, marcas de categoria e informações de direitos autorais. O acesso aos metadados facilita a execução de tarefas como o gerenciamento de ativos, o local do arquivo ou a determinação de informações de direitos autorais. Por exemplo, a Galeria de fotos do Windows no Windows Vista permite que você adicione descrições e marcas de categoria a imagens. Isso permite uma melhor descoberta de imagens e uma maneira conveniente de categorizar imagens. Usando as APIs do WIC e os formatos de metadados comuns, os aplicativos podem facilmente escrever ou ler esse tipo de metadados de ou para imagens.

O diagrama a seguir ilustra o conteúdo de um arquivo JPEG que inclui blocos de metadados incorporados e itens de metadados.

![imagem JPEG com metadados de classificação](graphics/jpeg.png)

Nesta imagem de exemplo, os metadados são inseridos no arquivo de imagem dentro de um quadro de imagem. O formato JPEG não dá suporte a vários quadros de imagem, portanto, os metadados são anexados conceitualmente a esse único quadro. Formatos que dão suporte a vários quadros, como TIFF, podem ter metadados anexados a cada quadro de imagem, como mostra este diagrama. Embora não seja comum hoje e não tenha suporte dos codecs de imagem nativa, alguns formatos de imagem também podem oferecer suporte a metadados fora de um quadro de imagem. O WIC é flexível o suficiente para lidar com metadados de nível de quadro e metadados fora do quadro individual de uma imagem.

## <a name="reading-image-metadata"></a>Lendo metadados de imagem

As APIs do WIC fornecem componentes COM que tornam mais fácil para os aplicativos ler e gravar metadados de imagem.

A maneira principal de ler metadados é usar um [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)(leitor de consulta de metadados) para acessar itens de metadados específicos. O componente leitor de consulta de metadados é implementado pelo codec e pode ser acessado no nível do decodificador ou por meio de quadros de imagem individuais, que é o método mais comum. O código a seguir demonstra como acessar um leitor de consulta para um quadro individual usando o método **GetMetadataQueryReader** do leitor de consulta.


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



Um leitor de consulta fornece métodos para obter informações sobre metadados específicos e um meio de especificar um item de metadados a ser recuperado. O código a seguir usa uma expressão de consulta para solicitar um item de metadados específico dentro do bloco de IFD (diretório de arquivos de imagem aninhada) do App1. Isso é feito usando o método **GetMetadataByName** do leitor de consulta. O código a seguir demonstra como usar o leitor de consultas para obter o valor de classificação MicrosoftPhoto.


```
PROPVARIANT value;
PropVariantInit(&value);

LPCWSTR pwzRatingQuery = L"/app1/ifd/{ushort=18249}";

if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(pwzRatingQuery, &value);
}
```



A variável pwzRatingQuery no exemplo anterior é a cadeia de caracteres de consulta para acessar a classificação MicrosoftPhoto do item de metadados. Essa cadeia de caracteres é criada usando a linguagem de consulta de metadados. Para criar essa cadeia de caracteres, é necessário ter conhecimento do formato de metadados e da linguagem de consulta de metadados para recuperar itens de metadados individuais. Para obter mais informações sobre a linguagem de consulta de metadados, consulte [visão geral da linguagem de consulta de metadados](-wic-codec-metadataquerylanguage.md).

Nos bastidores, um leitor de consulta usa um leitor de metadados ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) para acessar os metadados descritos pela expressão de consulta. Além de usar um leitor de consulta, você também pode acessar um leitor de metadados diretamente para ler os metadados. Você pode obter um leitor de metadados do decodificador ou quadros individuais consultando uma interface [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)(leitor de bloco).

## <a name="writing-image-metadata"></a>Gravando metadados de imagem

O processo de gravação de metadados é semelhante ao modo como é lido, exceto pelo fato de que um [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)(gravador de consulta de metadados) é usado. A interface do gravador de consulta é implementada pelo codificador de imagem e, como no leitor de consulta, os metadados são acessados no codificador e em quadros individuais (dependendo do suporte ao formato de imagem).

O código a seguir demonstra como obter um gravador de consulta de um quadro de codificador e remover o valor de classificação que foi lido anteriormente.


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



Outra maneira de gravar metadados é por meio de atualizações rápidas de metadados. A codificação rápida de metadados é uma maneira de gravar metadados de imagem sem a necessidade de codificar novamente um arquivo de imagem. Isso é feito com a gravação de novas informações de metadados em uma região preenchida do formato de metadados. O [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)(codificador de metadados rápidos) é obtido da fábrica de componentes, com base no decodificador de imagem. O codificador de metadados rápido Obtém um gravador de consulta que é usado para gravar os metadados. Por fim, o codificador rápido confirma a alteração.

O código a seguir demonstra como obter um codificador de metadados rápido e usá-lo para gravar o valor de MicrosoftRating.


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



Nem todos os formatos de metadados dão suporte a metadados rápidos. Para ver quais formatos com suporte nativo dão suporte à codificação de metadados rápida, consulte a tabela na seção [formatos de metadados com suporte](#supported-metadata-formats) mais adiante neste documento.

Nos bastidores, um gravador de consulta usa um gravador de metadados ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) para gravar os metadados descritos pela expressão de consulta. Além de usar um leitor de consulta, você também pode acessar um gravador de metadados diretamente para gravar metadados. Você pode obter um gravador de metadados do decodificador ou quadros individuais usando a consulta para uma interface de gravador de bloco ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).

## <a name="metadata-extensibility"></a>Extensibilidade de metadados

Conforme mencionado anteriormente, o WIC fornece vários manipuladores de metadados para ler e gravar metadados para formatos de metadados comuns. No entanto, há alguns formatos de metadados que não têm suporte nativo. Portanto, o WIC fornece APIs para criar manipuladores de metadados adicionais que podem estender o suporte de metadados para outros formatos.

Para oferecer suporte total a outros formatos de metadados, dois tipos de manipuladores devem ser desenvolvidos — um leitor de metadados para ler metadados e um gravador de metadados para gravar metadados. Embora esses dois manipuladores sejam geralmente implementados em pares para um formato específico, isso não é um requisito. Pode haver alguns casos em que apenas a capacidade de leitura ou apenas a capacidade de gravação é necessária.

Para obter mais informações sobre a extensibilidade de metadados usando as APIs do WIC, consulte [visão geral da extensibilidade de metadados](-wic-codec-metadatahandlers.md).

## <a name="supported-metadata-formats"></a>Formatos de metadados com suporte

O WIC fornece suporte para vários formatos de metadados comuns. A tabela a seguir lista os formatos de metadados com suporte, suas versões, os formatos de imagem que oferecem suporte ao formato de metadados e se o formato de metadados oferece suporte à codificação de metadados rápida. Para obter mais informações sobre a codificação rápida de metadados, consulte a seção [gravando metadados de imagem](#writing-image-metadata) anteriormente neste documento.



| Formatos de metadados com suporte | Versão de especificação de metadados | Suporte ao formato de imagem | Dá suporte à codificação de metadados rápida |
|----------------------------|--------------------------------|----------------------|---------------------------------|
| App0                       | JFIF 1, 2                      | JPEG                 | No                              |
| Aplicativo1                       | JFIF 1, 2                      | JPEG, TIFF           | No                              |
| App13                      | Unknown                        | JPEG, TIFF           | No                              |
| IFD                        | TIFF 6,0                       | JPEG, TIFF           | Yes                             |
| IRB                        | Unknown                        | JPEG, TIFF           | No                              |
| Exif                       | EXIF 2,2                       | JPEG, TIFF           | Yes                             |
| XMP                        | XMP 1,0 (setembro de 2005)            | JPEG, TIFF           | Yes                             |
| GPS                        | EXIF 2,2                       | JPEG, TIFF           | Yes                             |
| IPTC                       | IPTC 4,0                       | JPEG, TIFF           | Yes                             |
| Texto                       | PNG 1,2                        | PNG                  | No                              |



 

> [!Note]  
> O IPTC só dá suporte a FME se os blocos crescerem em tamanho, pois o IPTC não oferece suporte a preenchimento.

 

## <a name="metadata-component-summary"></a>Resumo do componente de metadados

A tabela a seguir descreve as interfaces WIC que dão suporte a metadados e seus componentes correspondentes. Esses componentes fornecem o acesso aos metadados de uma imagem. Para obter mais informações sobre esses componentes, consulte [visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md). 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Componente</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Decodificador de bitmap (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>)</td>
<td><ul>
<li>Lê um fluxo de imagem e produz uma fonte de bitmap utilizável. Associado a um formato de contêiner, como TIFF (Tagged Image File Format) ou JPEG (grupo de especialistas fotográfico) conjunta.</li>
<li>Implementa uma interface <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> para enumerar todos os blocos de metadados no fluxo de dados do decodificador que não estão dentro de um quadro.</li>
<li>Expõe um leitor de consulta para ler os metadados associados à imagem que não está dentro de um quadro.</li>
</ul></td>
</tr>
<tr class="even">
<td>Decodificação de quadros de bitmap (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>)</td>
<td><ul>
<li>Acessa quadros individuais do fluxo de imagem mantido pelo decodificador.</li>
<li>Implementa uma interface <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> para enumerar todos os blocos de metadados no fluxo de dados do quadro.</li>
<li>Expõe um leitor de consulta para ler os metadados associados ao quadro, usando expressões de consulta.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Codificador de bitmap (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>)</td>
<td><ul>
<li>Grava uma origem de bitmap em um fluxo de imagem. Associado a um formato de contêiner como TIFF ou JPEG.</li>
<li>Implementa uma interface <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> para criar uma lista de blocos de metadados para gravar no fluxo de dados do codificador.</li>
<li>Expõe um gravador de consulta para gravar os metadados associados à imagem, usando expressões de consulta.</li>
</ul></td>
</tr>
<tr class="even">
<td>Bitma frame Encode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>)</td>
<td><ul>
<li>Cria um quadro que será codificado no fluxo mantido pelo codificador.</li>
<li>Implementa uma interface <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> para criar uma lista de blocos de metadados para gravar no fluxo de dados do quadro.</li>
<li>Expõe um gravador de consulta para gravar os metadados associados ao quadro, usando expressões de consulta.</li>
</ul></td>
</tr>
</tbody>
</table>



 

A tabela a seguir descreve os componentes de metadados do WIC. Esses componentes permitem que você leia e grave os metadados em uma imagem exposta pelos componentes listados na tabela anterior. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Componente</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Leitor de consulta de metadados (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>)</td>
<td><ul>
<li>Usa uma cadeia de caracteres de consulta e navega pela hierarquia de metadados subjacente para obter metadados.</li>
</ul></td>
</tr>
<tr class="even">
<td>Gravador de consulta de metadados (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>)</td>
<td><ul>
<li>Usa uma cadeia de caracteres de consulta e navega pela hierarquia de metadados subjacente para obter, definir e remover metadados.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Iniwicmetadatablockreader (leitor<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong></strong></a>de bloco de metadados)</td>
<td><ul>
<li>Gerencia uma coleção somente leitura de objetos <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> na parte superior da hierarquia de metadados e habilita a enumeração de todos os blocos de metadados.</li>
<li>Implementado por um decodificador de bitmap e um quadro de bitmap decodificado.</li>
<li>Implementados por desenvolvedores de componentes de terceiros para codecs personalizados.</li>
</ul></td>
</tr>
<tr class="even">
<td>Gravador de bloco de metadados (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>)</td>
<td><ul>
<li>Gerencia uma coleção de leitura e gravação de objetos <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a> na parte superior da hierarquia de metadados.</li>
<li>Implementado por um codificador de bitmap e uma codificação de quadro de bitmap.</li>
<li>Implementados por desenvolvedores de componentes de terceiros para codecs personalizados.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Leitor de metadados (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>)</td>
<td><ul>
<li>Analisa um fluxo de metadados e gerencia uma coleção somente leitura dos itens de metadados. Associado a um formato de metadados como EXIF, IFD e XMP.</li>
<li>Atua como um dicionário, retornando um valor quando um par de formato e ID é fornecido.</li>
<li>Implementado por desenvolvedores de componentes de terceiros para tipos de metadados personalizados.</li>
</ul></td>
</tr>
<tr class="even">
<td>Gravador de metadados (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>)</td>
<td><ul>
<li>Analisa e serializa um fluxo de metadados e gerencia uma coleção de leitura/gravação de itens de metadados.</li>
<li>Implementado por desenvolvedores de componentes de terceiros para tipos de metadados personalizados.</li>
</ul></td>
</tr>
<tr class="odd">
<td>IWICFastMetadataEncoder do codificador de metadados rápidos<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong></strong></a></td>
<td><ul>
<li>Expõe a semântica para gravar em uma hierarquia de metadados que atualizará os metadados no local sem codificar novamente a imagem.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Visão geral da linguagem de consulta de metadados](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Visão geral da leitura e gravação de metadados de imagem](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Visão geral da extensibilidade de metadados](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Como: codificar novamente uma imagem JPEG com metadados](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



