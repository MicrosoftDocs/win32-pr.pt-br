---
description: Este tópico apresenta o novo esquema XMP (Extensible Metadata Platform) e a propriedade de foto System.Photo.PeopleNames do Windows 7 que permite a marcação de indivíduos em uma foto digital.
ms.assetid: 557c3e9a-1756-4abb-8465-b12195ecbc91
title: Visão geral de marcação de pessoas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a262acd70474f75689e99a3bcd1087cd0117ae3602b78a90357aa932fdd7fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205696"
---
# <a name="people-tagging-overview"></a>Visão geral de marcação de pessoas

Este tópico apresenta o novo esquema XMP (Extensible Metadata Platform) e a propriedade de foto [system.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) do Windows 7 que permite a marcação de indivíduos em uma foto digital. Este tópico também discute como usar a API do WIC (componente Windows imagem) para ler e gravar os metadados necessários para marcação de pessoas.

Este tópico inclui as seções a seguir.

-   [Pré-requisitos](#prerequisites)
-   [Introdução](#introduction)
-   [Marcação de pessoas](#people-tagging-overview)
    -   [Nomes de pessoas](#people-names)
    -   [Retângulos de pessoas](#people-rectangles)
-   [Referência de esquema](#schema-reference)
    -   [Esquema do Microsoft Photo 1.2](#microsoft-photo-12-schema)
    -   [Esquema RegionInfo do Microsoft Photo](#microsoft-photo-regioninfo-schema)
    -   [Esquema de região de foto da Microsoft](#microsoft-photo-regioninfo-schema)
    -   [Metadados de exemplo](#sample-metadata)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites"></a>Pré-requisitos

Para entender este tópico, você deve estar familiarizado com as interfaces do decodificador WIC e seus componentes Component Object Model (COM) relacionados, conforme descrito na Visão geral do componente [Windows Imaging.](-wic-about-windows-imaging-codec.md) Ele também ajuda a ter uma familiaridade geral com metadados de imagens, especialmente XMP.

## <a name="introduction"></a>Introdução

A Microsoft criou um novo esquema XMP para marcar pessoas em uma imagem digital. Esse esquema permite que os aplicativos armazenem os nomes e locais de indivíduos que estão na imagem como metadados na imagem. Além do novo esquema, a nova propriedade de foto [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) está disponível no Windows 7. Essa nova propriedade permite que os aplicativos leiam os nomes do indivíduo armazenados nos metadados da imagem. O WIC utiliza esses novos recursos permitindo que os aplicativos leiam e escrevam facilmente metadados de marcação de pessoas em fotos digitais.

## <a name="people-tagging"></a>Marcação de pessoas

O WIC fornece aos desenvolvedores de aplicativos componentes COM que leem dados de imagem, bem como metadados de imagem. Para ler e escrever metadados, como o novo recurso de marcação de pessoas, o WIC fornece as interfaces [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) e [**IWICMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) Essas interfaces permitem que os aplicativos usem a linguagem de consulta [de](-wic-codec-metadataquerylanguage.md) metadados para gravar metadados nos quadros individuais de uma imagem. A seção a seguir demonstra como ler e gravar os metadados de marcação de pessoas nos metadados de uma imagem usando leitores e autores de consultas WIC.

### <a name="people-names"></a>Nomes de pessoas

Parte do recurso de marcação de pessoas é a capacidade de simplesmente obter uma lista dos nomes das pessoas marcadas dentro da imagem. Essa parte do recurso é suportada pelos manipuladores de metadados [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) e WIC. A interface [**IWICMetadataQueryReader,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) em conjunto com a propriedade System.Photo.PeopleNames, é usada para ler os nomes de pessoas identificadas em uma imagem e armazenadas nos metadados da imagem.

O exemplo de código a seguir demonstra um leitor de consulta obtido de um quadro de imagem para consultar os metadados de uma imagem para nomes marcados da propriedade [System.Photo.PeopleNames.](../properties/props-system-photo-peoplenames.md)


```C++
// Not shown: image decoding, retrieving an image frame. 
...
PROPVARIANT value;
IWICMetadataQueryReader *pQueryReader = NULL;
...
// Get the query reader.
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

// Query for the System.Photo.PeopleNames property.
if (SUCCEEDED(hr))
{
    // Get the property metadata by property name.
    hr = pQueryReader->GetMetadataByName(L"System.Photo.PeopleNames", &value);
}
```



A expressão de consulta "System.Photo.PeopleNames" consulta o quadro para a propriedade . Se os metadados de marcação de pessoas existirem e contiver nomes de pessoas, o valor [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) será definido como VT LPWSTR e o valor dos dados conterá a lista de nomes \_ marcados. Para obter mais informações sobre como ler metadados de imagem, consulte [Visão geral de leitura e escrita de metadados de imagem.](-wic-codec-readingwritingmetadata.md)

Consultar a marca de nomes de pessoas só será útil se a imagem realmente contiver os metadados de marcação de pessoas. Para que isso ocorra, um aplicativo deve primeiro tê-lo gravado. Para escrever os nomes de pessoas de metadados, use [**um IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) e o caminho XMP explícito dos metadados. O exemplo de código a seguir demonstra o uso de um autor de consulta para gravar um nome no caminho da consulta.


```C++
// Not shown: image encoding, retrieving/creating the image frame,
// creating the IWICImagingFactory 
...
IWICImagingFactory *pFactory = NULL;
IWICMetadataQueryWriter *pQueryWriter = NULL;
...
// Get the query writer from the image frame.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pQueryWriter);
}

// A query writer specifically for this person's XMP struct
IWICMetadataQueryWriter *pXMPStructQueryWriter = NULL;

// Create a query writer specifically for an XMP Struct
hr = pFactory->CreateQueryWriter(
    GUID_MetadataFormatXMPStruct,
    NULL,
    &pXMPStructQueryWriter
    );

// Create a variant representing the structure created above
PROPVARIANT xmpStruct;
PropVariantInit(&xmpStruct);

// VT_UNKNOWN indicates that we're setting a COM object, in this case a XMPStruct
// which will hold the name and rectangle
xmpStruct.vt = VT_UNKNOWN; 
xmpStruct.punkVal = pXMPStructQueryWriter;

if(SUCCEEDED(hr))
{
    // WIC will automatically create the xmp base, the RegionInfo struct, and the Regions
    // bag (an unordered array) but structs within that bag need to be explicitly created.
    // The {ulong=0} in the query means to insert the new struct at the start of the bag,
    // {} could also be used to insert at the end of the bag.
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions/{ulong=0}",
        &xmpStruct
        );
}

// Set up the PROPVARIANT with the name information
PROPVARIANT personName;
PropVariantInit(&personName);
personName.vt = VT_LPWSTR;
personName.pwszVal = L"John Doe";

if(SUCCEEDED(hr))
{
    // Set the name metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:PersonDisplayName",
        &personName
        );  
}
```



Observe a etapa que constrói a estrutura XMP e a configura em `MPRI:Regions/{ulong=0}` . Sem essa etapa, o WIC não pode identificar onde colocar o `PersonDisplayName` posteriormente. Observe também que o caminho de consulta explícito é usado em vez de [System.Photo.PeopleNames,](-wic-photoprop-system-photo-peoplenames.md)cuja política de metadados não dá suporte à escrita de metadados.

### <a name="people-rectangles"></a>Retângulos de pessoas

No entanto, os nomes das pessoas fazem parte apenas do recurso de marcação de pessoas. Além de armazenar nomes de pessoas nos metadados, o esquema também dá suporte a informações de região que identificam a área específica (um retângulo) que a pessoa é mostrada na imagem.

As informações do retângulo são representadas por quatro valores decimais delimitados por vírgula, como "0,25, 0,25, 0,25, 0,25". Os dois primeiros valores especificam a coordenada superior esquerda; os dois finais especificam a altura e a largura do retângulo. As dimensões da imagem para fins de definição de retângulos de pessoas são normalizadas para 1, o que significa que, no exemplo "0,25, 0,25, 0,25, 0,25", o retângulo inicia 1/4 da distância da parte superior e 1/4 da distância da esquerda da imagem. A altura e a largura do retângulo são 1/4 do tamanho de suas respectivas dimensões de imagem.

As informações de retângulo que identificam indivíduos são escritas da mesma maneira que os nomes das pessoas são gravados, dentro da mesma estrutura. Para gravar os metadados do retângulo, use [**um IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) e o caminho XMP explícito dos metadados. O exemplo de código a seguir continua o exemplo anterior e adiciona um retângulo que representa 'John Doe' aos metadados da imagem. Observe que ele usa o mesmo `{ulong=0}` índice para associar esse retângulo a 'John Doe'.


```C++
// Set up the PROPVARIANT with the rectangle information
PROPVARIANT rectangle;
PropVariantInit(&rectangle);
rectangle.vt = VT_LPWSTR;
rectangle.pwszVal = L"0.0,0.0,0.25,0.25";

if(SUCCEEDED(hr))
{
    // Set the rectangle metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:Rectangle",
        &rectangle
        );
}
```



## <a name="schema-reference"></a>Referência de esquema

Os esquemas do Microsoft XMP para marcação de pessoas definem um conjunto de propriedades para marcar indivíduos em fotos digitais.

As seções a seguir fornecem as definições de esquema necessárias para a marcação de pessoas. Sempre que possível, as definições de esquema usam as convenções fornecidas pelas especificações [XMP (Extensible Metadata Platform) da Adobe.](https://www.adobe.com/devnet/xmp/) As definições de esquema neste tópico mostram o namespace xml Uniform Resource Identifier (URI) que identifica o esquema e o prefixo de namespace de esquema preferencial, seguido por uma tabela que lista todas as propriedades definidas para o esquema. Cada tabela tem as seguintes colunas:

-   **Propriedade** – o nome da propriedade, incluindo o prefixo de namespace preferencial.

-   **Tipo de** valor – o tipo de valor da propriedade. Os esquemas de suporte à marcação de pessoas usam os tipos de valor XMP sempre que possível, incluindo Data e Texto. Os tipos de matriz são precedidas pelo tipo de contêiner: `alt` `bag` , ou `seq` .

-   **Categoria** – As propriedades do esquema são internas ou externas:

    -   Os metadados internos devem ser definidos pelo aplicativo.

    -   Os metadados externos devem ser definidos pelo usuário e são independentes do conteúdo do documento.

-   **Descrição** – a descrição da propriedade.

### <a name="microsoft-photo-12-schema"></a>Esquema do Microsoft Photo 1.2

O esquema do Microsoft Photo 1.2 fornece um conjunto de propriedades para regiões de imagem.

-   O URI do namespace do esquema é `https://ns.microsoft.com/photo/1.2/` .
-   O prefixo de namespace de esquema preferencial é `MP` .



| Propriedade      | Tipo de valor | Categoria | Descrição                                                                                                                     |
|---------------|------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| MP:RegionInfo | Regioninfo | Interna | **required:** armazena a raiz dos metadados de marcação de pessoas. Consulte a seção Esquema Do Microsoft Photo RegionInfo a seguir. |



 

### <a name="microsoft-photo-regioninfo-schema"></a>Esquema RegionInfo do Microsoft Photo

O esquema RegionInfo 1.2 do Microsoft Photo fornece um conjunto de propriedades para informações de região.

-   O URI do namespace do esquema é `https://ns.microsoft.com/photo/1.2/t/RegionInfo#` .
-   O prefixo de namespace de esquema preferencial é `MPRI` .



| Propriedade              | Tipo de valor | Categoria | Descrição                                                                                                    |
|-----------------------|------------|----------|----------------------------------------------------------------------------------------------------------------|
| MPRI:DateRegionsValid | Data       | Externo | **opcional:** data em que a última região foi criada.                                                          |
| MPRI:Regions          | região do bag | Externo | **obrigatório:** armazena as regiões de marcação de pessoas. Consulte a seção Esquema de Região de Foto da Microsoft a seguir. |



 

### <a name="microsoft-photo-region-schema"></a>Esquema de região de foto da Microsoft

O esquema Microsoft Photo Region 1.2 fornece um conjunto de propriedades para regiões de imagem.

-   O URI do namespace do esquema é `https://ns.microsoft.com/photo/1.2/t/Region#` .
-   O prefixo de namespace de esquema preferencial é `MPReg` .



| MPReg:Property          | Tipo de valor | Categoria | Descrição                                                                                                                                                                                                                                                                                                     |
|-------------------------|------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MPReg:PersonDisplayName | Texto       | Externo | **required** : armazena o nome da pessoa no retângulo determinado.                                                                                                                                                                                                                                            |
| MPReg:Rectangle         | Texto       | Externo | **opcional:** armazena o retângulo que identifica a pessoa dentro da foto. O retângulo é armazenado como quatro valores decimais delimitados por vírgulas. Os dois primeiros valores especificam a coordenada superior esquerda; os dois finais especificam a altura e a largura do retângulo. Os valores decimais devem ser normalizados para 1. |
| MPReg:PersonEmailDigest | Texto       | Externo | **opcional:** armazena o hash de mensagem criptografada SHA-1 do endereço de email ao vivo da pessoa.                                                                                                                                                                                                                     |
| MPReg:PersonLiveIdCID   | Texto       | Externo | **opcional** : armazena a representação decimal assinada do CID ao vivo da pessoa, um inteiro de 64 bits que identifica publicamente uma identidade ao vivo.                                                                                                                                                                     |



 

### <a name="sample-metadata"></a>Metadados de exemplo

A seguir está uma representação dos metadados XMP para marcação de pessoas.

``` syntax
<rdf:Description rdf:about="" xmlns:MP="https://ns.microsoft.com/photo/1.2/">
<MP:RegionInfo> 
<rdf:Description xmlns:MPRI="https://ns.microsoft.com/photo/1.2/t/RegionInfo#">
   <MPRI:Regions> 
       <rdf:Bag> 
          <rdf:li> 
       <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#"> 
           <MPReg:Rectangle>0.790650, 0.441734, 0.209350, 0.279133
           </MPReg:Rectangle>
           <MPReg:PersonDisplayName>John Doe</MPReg:PersonDisplayName> 
           <MPReg:PersonEmailDigest>2FD4E1C67A2D28FCED849EE1BB76E7391B93EB13</MPReg:PersonEmailDigest> 
           <MPReg:PersonLiveIdCID>1234567890123456789</MPReg:PersonLiveIdCID> 
       </rdf:Description> 
         </rdf:li> 
         <rdf:li>
             <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#">
                  <MPReg:Rectangle>0.222656, 0.302083, 0.378906, 0.505208</MPReg:Rectangle> 
                  <MPReg:PersonDisplayName>Jane Doe</MPReg:PersonDisplayName> 
              </rdf:Description> 
         </rdf:li> 
<!-- Addition Regions --> ... 
<rdf:li>...
</rdf:li> 
</rdf:Bag> 
</MPRI:Regions> </rdf:Description> </MP:RegionInfo> </rdf:Description>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Visão geral dos metadados do WIC](-wic-about-metadata.md)
</dt> <dt>

[Visão geral da leitura e da escrita de metadados de imagem](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Visão geral da linguagem de consulta de metadados](-wic-codec-metadataquerylanguage.md)
</dt> </dl>

 

 
