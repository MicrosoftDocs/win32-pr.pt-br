---
description: Este tópico apresenta o novo esquema XMP (Extensible Metadata Platform) e o sistema de propriedades de fotos do Windows 7. photos. Peoples que habilita a marcação de indivíduos em uma foto digital.
ms.assetid: 557c3e9a-1756-4abb-8465-b12195ecbc91
title: Visão geral de marcação de pessoas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64f2080e51d4d340474e0610fcce9512fc72429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091743"
---
# <a name="people-tagging-overview"></a>Visão geral de marcação de pessoas

Este tópico apresenta o novo esquema XMP (Extensible Metadata Platform) e o sistema de propriedades de fotos do Windows 7 [. photos. Peoples](../properties/props-system-photo-peoplenames.md) que habilita a marcação de indivíduos em uma foto digital. Este tópico também aborda como usar a API do Windows Imaging Component (WIC) para ler e gravar os metadados necessários para a marcação de pessoas.

Este tópico inclui as seções a seguir.

-   [Pré-requisitos](#prerequisites)
-   [Introdução](#introduction)
-   [Marcação de pessoas](#people-tagging-overview)
    -   [Nomes de pessoas](#people-names)
    -   [Retângulos de pessoas](#people-rectangles)
-   [Referência de esquema](#schema-reference)
    -   [Esquema do Microsoft Photo 1,2](#microsoft-photo-12-schema)
    -   [Esquema do Microsoft Photo RegionInfo](#microsoft-photo-regioninfo-schema)
    -   [Esquema de região fotográfica da Microsoft](#microsoft-photo-regioninfo-schema)
    -   [Metadados de exemplo](#sample-metadata)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites"></a>Pré-requisitos

Para entender este tópico, você deve estar familiarizado com as interfaces do decodificador do WIC e seus componentes COM (Component Object Model) relacionados, conforme descrito no [visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md). Também ajuda a ter uma familiaridade geral com metadados de geração de imagens, especialmente XMP.

## <a name="introduction"></a>Introdução

A Microsoft criou um novo esquema XMP para marcar pessoas em uma imagem digital. Esse esquema permite que os aplicativos armazenem os nomes e locais de indivíduos que estão na imagem como metadados dentro da imagem. Além do novo esquema, a nova propriedade de foto [System. Photo. peoplenames](../properties/props-system-photo-peoplenames.md) está disponível no Windows 7. Essa nova propriedade permite que os aplicativos leiam os nomes de indivíduo armazenados nos metadados da imagem. O WIC utiliza esses novos recursos, permitindo que os aplicativos leiam e gravem facilmente os metadados de marcação de pessoas em fotos digitais.

## <a name="people-tagging"></a>Marcação de pessoas

O WIC fornece aos desenvolvedores de aplicativos com componentes COM que lêem dados de imagem, bem como metadados de imagem. Para ler e gravar metadados, como o novo recurso de marcação de pessoas, o WIC fornece as interfaces [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) e [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) . Essas interfaces permitem que os aplicativos usem a [linguagem de consulta de metadados](-wic-codec-metadataquerylanguage.md) para gravar metadados em quadros individuais de uma imagem. A seção a seguir demonstra como ler e gravar os metadados de marcação de pessoas em metadados de uma imagem usando leitores de consulta do WIC e gravadores.

### <a name="people-names"></a>Nomes de pessoas

Parte do recurso de marcação de pessoas é a capacidade de simplesmente obter uma lista dos nomes das pessoas marcadas na imagem. Esta parte do recurso é suportada pelos manipuladores de metadados [System. Photo. People](../properties/props-system-photo-peoplenames.md) e WIC. A interface [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) , em conjunto com a propriedade System. Photo. peoplenames, é usada para ler os nomes das pessoas identificadas em uma imagem e armazenadas nos metadados da imagem.

O exemplo de código a seguir demonstra um leitor de consulta obtido de um quadro de imagem para consultar os metadados de uma imagem em busca de nomes marcados da propriedade [System. Photo. peoplenames](../properties/props-system-photo-peoplenames.md) .


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



A expressão de consulta "System. Photo. Peoplenames" consulta o quadro para a propriedade. Se os metadados de marcação de pessoas existirem e contiverem nomes de pessoas, o valor [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) será definido como VT \_ LPWSTR e o valor dos dados conterá a lista de nomes marcados. Para obter mais informações sobre como ler metadados de imagem, consulte [visão geral da leitura e gravação de metadados de imagem](-wic-codec-readingwritingmetadata.md).

Consultar a marca nomes de pessoas só será útil se a imagem contiver realmente os metadados de marcação de pessoas. Para que isso ocorra, um aplicativo deve primeiro tê-lo gravado. Para gravar os metadados de nomes de pessoas, use um [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) e o caminho XMP explícito dos metadados. O exemplo de código a seguir demonstra como usar um gravador de consulta para gravar um nome no caminho de consulta.


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



Observe a etapa que constrói a estrutura XMP e a define em `MPRI:Regions/{ulong=0}` . Sem essa etapa, o WIC não pode identificar onde colocá-lo `PersonDisplayName` mais tarde. Observe também que o caminho de consulta explícito é usado em vez de [System. Photo. peoplenames](-wic-photoprop-system-photo-peoplenames.md), cuja política de metadados não dá suporte à gravação de metadados.

### <a name="people-rectangles"></a>Retângulos de pessoas

No entanto, os nomes das pessoas são apenas parte do recurso de marcação de pessoas. Além de armazenar nomes de pessoas nos metadados, o esquema também oferece suporte a informações de região que identificam a área específica (um retângulo) que a pessoa é mostrada na imagem.

As informações de retângulo são representadas por quatro valores decimais delimitados por vírgula, como "0,25, 0,25, 0,25, 0,25". Os dois primeiros valores especificam a coordenada superior esquerda; os dois finais especificam a altura e a largura do retângulo. As dimensões da imagem para fins de definição de retângulos de pessoas são normalizadas para 1, o que significa que, no exemplo "0,25, 0,25, 0,25, 0,25", o retângulo começa a 1/4 da distância da parte superior e da 1/4 da distância à esquerda da imagem. A altura e a largura do retângulo são 1/4 do tamanho de suas respectivas dimensões de imagem.

As informações de retângulo que identificam indivíduos são escritas da mesma forma que os nomes das pessoas são escritas, dentro da mesma estrutura. Para gravar os metadados de retângulo, use um [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) e o caminho XMP explícito dos metadados. O exemplo de código a seguir continua o exemplo anterior e adiciona um retângulo representando ' João doe ' aos metadados da imagem. Observe que ele usa o mesmo `{ulong=0}` índice para associar este retângulo a ' João doe '.


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

Os esquemas XMP da Microsoft para marcação de pessoas definem um conjunto de propriedades para marcar indivíduos em fotos digitais.

As seções a seguir fornecem as definições de esquema necessárias para a marcação de pessoas. Sempre que possível, as definições de esquema usam as convenções fornecidas pelas [especificações XMP (Extensible Metadata Platform) da Adobe](https://www.adobe.com/devnet/xmp/). As definições de esquema neste tópico mostram o XML namespace Uniform Resource Identifier (URI) que identifica o esquema e o prefixo de namespace de esquema preferencial, seguido por uma tabela que lista todas as propriedades definidas para o esquema. Cada tabela tem as seguintes colunas:

-   **Property** -o nome da propriedade, incluindo o prefixo de namespace preferencial.

-   **Tipo de valor** -o tipo de valor da propriedade. Os esquemas de suporte à marcação de pessoas usam os tipos de valor XMP sempre que possível, incluindo data e texto. Os tipos de matriz são precedidos pelo tipo de contêiner: `alt` , `bag` ou `seq` .

-   **Categoria** -as propriedades de esquema são internas ou externas:

    -   Os metadados internos devem ser definidos pelo aplicativo.

    -   Os metadados externos devem ser definidos pelo usuário e são independentes do conteúdo do documento.

-   **Descrição** -a descrição da propriedade.

### <a name="microsoft-photo-12-schema"></a>Esquema do Microsoft Photo 1,2

O esquema do Microsoft Photo 1,2 fornece um conjunto de propriedades para regiões de imagem.

-   O URI do namespace do esquema é `https://ns.microsoft.com/photo/1.2/` .
-   O prefixo de namespace de esquema preferencial é `MP` .



| Propriedade      | Tipo de valor | Categoria | Descrição                                                                                                                     |
|---------------|------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| MP: RegionInfo | RegionInfo | Interna | **obrigatório** : armazena a raiz dos metadados de marcação de pessoas. Consulte a seção esquema do Microsoft Photo RegionInfo que segue. |



 

### <a name="microsoft-photo-regioninfo-schema"></a>Esquema do Microsoft Photo RegionInfo

O esquema Microsoft Photo RegionInfo 1,2 fornece um conjunto de propriedades para informações de região.

-   O URI do namespace do esquema é `https://ns.microsoft.com/photo/1.2/t/RegionInfo#` .
-   O prefixo de namespace de esquema preferencial é `MPRI` .



| Propriedade              | Tipo de valor | Categoria | Descrição                                                                                                    |
|-----------------------|------------|----------|----------------------------------------------------------------------------------------------------------------|
| MPRI:DateRegionsValid | Data       | Externo | **opcional** : data em que a última região foi criada.                                                          |
| MPRI: regiões          | Região da bolsa | Externo | **obrigatório** : armazena as regiões de marcação de pessoas. Consulte a seção esquema de região fotográfica da Microsoft que segue. |



 

### <a name="microsoft-photo-region-schema"></a>Esquema de região fotográfica da Microsoft

O esquema da região 1,2 do Microsoft Photo fornece um conjunto de propriedades para regiões de imagem.

-   O URI do namespace do esquema é `https://ns.microsoft.com/photo/1.2/t/Region#` .
-   O prefixo de namespace de esquema preferencial é `MPReg` .



| MPReg: Propriedade          | Tipo de valor | Categoria | Descrição                                                                                                                                                                                                                                                                                                     |
|-------------------------|------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MPReg:PersonDisplayName | Texto       | Externo | **obrigatório** : armazena o nome da pessoa no retângulo fornecido.                                                                                                                                                                                                                                            |
| MPReg: retângulo         | Texto       | Externo | **opcional** : armazena o retângulo que identifica a pessoa na foto. O retângulo é armazenado como quatro valores decimais delimitados por vírgula. Os dois primeiros valores especificam a coordenada superior esquerda; os dois finais especificam a altura e a largura do retângulo. Os valores decimais devem ser normalizados para 1. |
| MPReg:PersonEmailDigest | Texto       | Externo | **opcional** : armazena o hash de mensagem criptografada SHA-1 do endereço de email ao vivo da pessoa.                                                                                                                                                                                                                     |
| MPReg:PersonLiveIdCID   | Texto       | Externo | **opcional** : armazena a representação decimal assinada da CID ao vivo da pessoa, um inteiro de 64 bits que identifica publicamente uma identidade ao vivo.                                                                                                                                                                     |



 

### <a name="sample-metadata"></a>Metadados de exemplo

Veja a seguir uma representação dos metadados XMP para marcação de pessoas.

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

**Conceitua**
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Visão geral dos metadados do WIC](-wic-about-metadata.md)
</dt> <dt>

[Visão geral da leitura e gravação de metadados de imagem](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Visão geral da linguagem de consulta de metadados](-wic-codec-metadataquerylanguage.md)
</dt> </dl>

 

 
