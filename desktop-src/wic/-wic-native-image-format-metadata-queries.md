---
description: Este tópico fornece uma visão geral das consultas de linguagem de consulta de metadados para leitura e gravação de metadados com suporte pelas imagens GIF, PNG, TIFF e JPEG.
ms.assetid: a6ab1708-dd82-4960-b908-f1daef7374ef
title: Consultas de metadados de formato de imagem nativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be5e9c0f853e4c5e48fb5eb41f2d2ab27b4f4d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751744"
---
# <a name="native-image-format-metadata-queries"></a>Consultas de metadados de formato de imagem nativa

Este tópico fornece uma visão geral das consultas de [linguagem de consulta de metadados](-wic-codec-metadataquerylanguage.md) para leitura e gravação de metadados com suporte pelas imagens gif, png, TIFF e JPEG. Ele inclui metadados específicos de cada formato de imagem, bem como metadados com suporte em vários formatos.

Este tópico inclui as seções a seguir.

-   [Pré-requisitos](#prerequisites)
-   [Expressão de política de metadados de foto](#photo-metadata-policy-expression)
-   [Metadados específicos de formato de arquivo](#file-format-specific-metadata)
    -   [Metadados GIF](#gif-metadata)
    -   [Metadados PNG](#png-metadata)
    -   [Metadados TIFF](#tiff-metadata)
    -   [Metadados JPEG](#jpeg-metadata)
-   [Metadados independentes de formato de arquivo](#file-format-independent-metadata)
    -   [Metadados de IFD](#ifd-metadata)
    -   [Metadados EXIF](#exif-metadata)
    -   [Metadados de GPS](#gps-metadata)
    -   [Metadados XMP](#xmp-metadata)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites"></a>Pré-requisitos

Para entender este tópico, você deve estar familiarizado com o sistema de metadados do Windows Imaging Component (WIC), conforme descrito na [visão geral dos metadados do WIC](-wic-about-metadata.md). Você também deve estar familiarizado com a linguagem de consulta usada para ler e gravar metadados, conforme descrito em [visão geral da linguagem de consulta de metadados](-wic-codec-metadataquerylanguage.md).

## <a name="photo-metadata-policy-expression"></a>Expressão de política de metadados de foto

Além de oferecer suporte à linguagem de consulta de metadados, o [WIC](-wic-api.md) também aceita nomes de propriedade canônica do [sistema de propriedades do Windows](../properties/windows-properties-system.md). O WIC dá suporte a um subconjunto do namespace de Propriedade do Windows que é relevante para formatos de imagem, conforme descrito em [políticas de metadados de fotos](photo-metadata-policies.md). Uma propriedade do Windows que é usada como uma consulta de metadados do WIC é chamada de expressão de política de metadados de foto.

Por exemplo, a expressão de política de metadados de foto para o sinalizador de orientação EXIF é:

-   [System. Photo. Orientation](-wic-photoprop-system-photo-orientation.md)

Em geral, as expressões de política são recomendadas em relação a consultas de metadados nativas para itens de metadados de imagem comuns que são cobertos pelo namespace de Propriedade do Windows. A linguagem de consulta de metadados é mais adequada para casos em que o acesso de baixo nível a itens de metadados de imagem específicos é necessário, ou para itens de metadados personalizados ou avançados que não são suportados pelo sistema de propriedades do Windows. Para obter mais informações, consulte [expressões de política de metadados de fotos](-wic-codec-metadataquerylanguage.md).

## <a name="file-format-specific-metadata"></a>Metadados específicos de formato de arquivo

As seções a seguir contêm tabelas que listam as consultas de metadados disponíveis para cada tipo de arquivo de imagem. Cada tabela tem as seguintes colunas:

-   **Caminho** -o caminho de consulta usado para recuperar o item de metadados.
-   **Nome** -o nome do item de metadados.
-   **Tipo** – o tipo do item de metadados recuperado do caminho de consulta. Os metadados recuperados pelo [WIC](-wic-api.md) são retornados na forma de PROPVARIANT, que relata o tipo de dados usando a enumeração VarType. on.

Os caminhos de consulta são usados pela API de metadados do WIC para acessar os metadados inseridos de uma imagem. O código de exemplo a seguir demonstra como usar um [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) para consultar o bloco de metadados IFD de JPEG.


```
// Not shown: image decoding 
IWICMetadataQueryReader *pQueryReader = NULL;
IWICMetadataQueryReader *pIFDReader = NULL;

// Get the query reader.
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

if (SUCCEEDED(hr))
{
    // Get the nested IFD reader.
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd", &value);
    if (value.vt == VT_UNKNOWN)
    {
        hr = value.punkVal->QueryInterface(IID_IWICMetadataQueryReader, (void **)&pIFDReader);
    }
    PropVariantClear(&value); // Clear value for new query.
}
```



### <a name="gif-metadata"></a>Metadados GIF

O formato de imagem Graphics Interchange Format (GIF) dá suporte a metadados globais e de nível de quadro. As duas seções a seguir fornecem os caminhos de consulta de metadados disponíveis para os metadados globais e de nível de quadro do GIF.

> [!Note]  
> Para obter uma lista completa de metadados GIF juntamente com informações mais detalhadas, consulte o [padrão gif](https://www.w3.org/Graphics/GIF/spec-gif89a.txt) no site do W3C.

 

### <a name="global-metadata"></a>Metadados globais

A tabela a seguir fornece os caminhos de consulta de metadados disponíveis que podem ser usados para acessar metadados GIF globais.



| Caminho                                               | Nome                       | Tipo                                |
|----------------------------------------------------|----------------------------|-------------------------------------|
| /commentext ou/ \[ \* \] commentext onde \* = 0 a N | Extensão de comentário          | VT \_ desconhecido-um leitor de consulta/gravador |
| /commentext/TextEntry                              |                            | a VT \_ LPSTR                           |
| /logscrdesc                                        | Descrição da tela lógica | VT \_ desconhecido-um leitor de consulta/gravador |
| /logscrdesc/Signature                              |                            | \_Vetor VT UI1 \| VT \_               |
| /logscrdesc/Width                                  |                            | \_UI2 VT                             |
| /logscrdesc/Height                                 |                            | \_UI2 VT                             |
| /logscrdesc/GlobalColorTableFlag                   |                            | BOOL do VT \_                            |
| /logscrdesc/ColorResolution                        |                            | \_UI1 VT                             |
| /logscrdesc/SortFlag                               |                            | BOOL do VT \_                            |
| /logscrdesc/GlobalColorTableSize                   |                            | \_UI1 VT                             |
| /logscrdesc/BackgroundColorIndex                   |                            | \_UI1 VT                             |
| /logscrdesc/PixelAspectRatio                       |                            | \_UI1 VT                             |
| /appext ou/ \[ \* \] appext onde \* = 0 a N         | Extensão do aplicativo      | VT \_ desconhecido-um leitor de consulta/gravador |
| /appext/Application                                |                            | \_Vetor VT UI1 \| VT \_               |
| /appext/Data                                       |                            | \_Vetor VT UI1 \| VT \_               |



 

### <a name="frame-metadata"></a>Metadados do quadro

A tabela a seguir fornece os caminhos de consulta de metadados disponíveis que podem ser usados para acessar os metadados GIF de nível de quadro.



| Caminho                            | Nome                      | Tipo                              |
|---------------------------------|---------------------------|-----------------------------------|
| /grctlext                       | Extensão de controle gráfico | VT \_ desconhecido – leitor de consulta/gravador |
| /grctlext/Disposal              |                           | \_UI1 VT                           |
| /grctlext/UserInputFlag         |                           | BOOL do VT \_                          |
| /grctlext/TransparencyFlag      |                           | BOOL do VT \_                          |
| /grctlext/Delay                 |                           | \_UI2 VT                           |
| /grctlext/TransparentColorIndex |                           | \_UI1 VT                           |
| /imgdesc                        | Descritor de imagem          | VT \_ desconhecido – leitor de consulta/gravador |
| /imgdesc/Left                   |                           | \_UI2 VT                           |
| /imgdesc/Top                    |                           | \_UI2 VT                           |
| /imgdesc/Width                  |                           | \_UI2 VT                           |
| /imgdesc/Height                 |                           | \_UI2 VT                           |
| /imgdesc/LocalColorTableFlag    |                           | BOOL do VT \_                          |
| /imgdesc/InterlaceFlag          |                           | BOOL do VT \_                          |
| /imgdesc/SortFlag               |                           | BOOL do VT \_                          |
| /imgdesc/LocalColorTableSize    |                           | \_UI1 VT                           |



 

### <a name="png-metadata"></a>Metadados PNG

O formato de imagem PNG (Portable Network Graphics) oferece suporte a metadados em nível de quadro.

> [!Note]  
> Para obter uma lista completa de metadados PNG juntamente com informações mais detalhadas, consulte o [padrão png](https://www.w3.org/TR/PNG/) no site do W3C.

 

### <a name="frame-metadata"></a>Metadados do quadro

A tabela a seguir fornece os caminhos de consulta de metadados disponíveis que podem ser usados para acessar os metadados de PNG no nível de quadro.



| Caminho                                                   | Nome             | Tipo                                      |
|--------------------------------------------------------|------------------|-------------------------------------------|
| /text ou/ \[ \* \] texto onde \* = 0 a N                 | Bloco de texto       | VT \_ desconhecido-leitor de consulta de texto/gravador    |
| /tEXt/{str = \* } Where \* = identificação de palavra-chave para texto |                  | a VT \_ LPSTR                                 |
| /gAMA                                                  | Parte gama       | VT \_ desconhecido – leitor de consulta do gama/gravador    |
| /gAMA/ImageGamma                                       |                  | \_UI4 VT                                   |
| /iTXt ou/ \[ \* \] iTXt onde \* = 0 a N                 | Parte IText      | VT \_ desconhecido – leitor de consulta do iTXt/gravador    |
| /iTXt/Keyword                                          |                  | a VT \_ LPSTR                                 |
| /iTXt/CompressionFlag                                  |                  | \_UI1 VT                                   |
| /iTXt/LanguageTag                                      |                  | LPSTR                                     |
| /iTXt/TranslatedKeyword                                |                  | LPWSTR                                    |
| /iTXt/TextEntry                                        |                  | LPWSTR                                    |
| /cHRM                                                  | Parte HRM        | VT \_ desconhecido – leitor de consulta do cHRM/gravador    |
| /cHRM/WhitePointX                                      |                  | \_UI4 VT                                   |
| /cHRM/WhitePointY                                      |                  | \_UI4 VT                                   |
| /cHRM/RedX                                             |                  | \_UI4 VT                                   |
| /cHRM/RedY                                             |                  | \_UI4 VT                                   |
| /cHRM/GreenX                                           |                  | \_UI4 VT                                   |
| /cHRM/GreenY                                           |                  | \_UI4 VT                                   |
| /cHRM/BlueX                                            |                  | \_UI4 VT                                   |
| /cHRM/BlueY                                            |                  | \_UI4 VT                                   |
| /sRGB                                                  | sRGB       | VT \_ desconhecido-leitor de consulta do sRGB/gravador    |
| /sRGB/RenderingIntent                                  |                  | \_UI1 VT                                   |
| /tIME                                                  | Bloco de tempo       | \_Leitor/gravador de consultas de tempo desconhecido VT    |
| /tIME/Year                                             |                  | \_UI2 VT                                   |
| /tIME/Month                                            |                  | \_UI1 VT                                   |
| /tIME/Day                                              |                  | \_UI1 VT                                   |
| /tIME/Hour                                             |                  | \_UI1 VT                                   |
| /tIME/Minute                                           |                  | \_UI1 VT                                   |
| /tIME/Second                                           |                  | \_UI1 VT                                   |
| /bKGD                                                  | Parte em segundo plano | VT \_ desconhecido – leitor de consulta do bKGB/gravador    |
| /bKGD/BackgroundColor                                  |                  | VT \_ UI1, VT \_ UI2 ou VT \_ UI2 \| VT \_ vector |
| /hIST                                                  | Parte sua       | VT \_ desconhecido – leitor de consulta do sua/gravador    |
| /hIST/Frequencies                                      |                  | \_UI2 de vetor \| VT \_ VT                     |
| /iCCP                                                  | Parte iCCP       | VT \_ desconhecido – leitor de consulta do iCCP/gravador    |
| /iCCP/ProfileName                                      |                  | a VT \_ LPSTR                                 |
| /iCCP/ProfileData                                      |                  | \_UI1 de vetor \| VT \_ VT                     |



 

### <a name="tiff-metadata"></a>Metadados TIFF

O formato de imagem TIFF (Tagged Image File Format) dá suporte a metadados em nível de quadro.

> [!Note]  
> Para obter uma lista completa de metadados TIFF juntamente com informações mais detalhadas, consulte [o padrão TIFF](https://www.adobe.io/content/dam/udp/en/open/standards/tiff/TIFF6.pdf).

 

### <a name="frame-metadata"></a>Metadados do quadro

A tabela a seguir fornece os caminhos de consulta de metadados disponíveis que podem ser usados para acessar metadados TIFF no nível de quadro.



| Caminho                                          | Nome            | Tipo                                |
|-----------------------------------------------|-----------------|-------------------------------------|
| /ifd                                          | 0 IFD           | VT \_ desconhecido-um leitor de consulta/gravador |
| /IFD/{UShort = \* } onde \* = 0 a 65535        | Entrada de IFD por ID | Variável                            |
| /IFD/Thumb ou/IFD/{UShort = 330}               | IFD de miniatura   | VT \_ desconhecido-um leitor de consulta/gravador |
| /IFD/XMP ou/IFD/{UShort = 700}                 | XMP             | VT \_ desconhecido-um leitor de consulta/gravador |
| /IFD/EXIF ou/IFD/{UShort = 34665}              | EXIF            | VT \_ desconhecido-um leitor de consulta/gravador |
| /IFD/GPS ou/IFD/{UShort = 34853}               | GPS             | VT \_ desconhecido-um leitor de consulta/gravador |
| /IFD/EXIF/Interop ou/IFD/EXIF/{UShort = 40965} | Interoperabilidade         | VT \_ desconhecido-um leitor de consulta/gravador |
| /IFD/IPTC ou/IFD/{UShort = 33723}              | IPTC            | VT \_ desconhecido-um leitor de consulta/gravador |
| /IFD/IPTC/{Str = \* } onde \* = palavra-chave IPTC    | Entrada IPTC      | Variável                            |
| /ifd/irb/8bimiptc/iptc                        | IPTC            | VT \_ desconhecido-um leitor de consulta/gravador |
| /IFD/IRB/8bimiptc/IPTC/{Str = \* }               | Entrada IPTC      | Variável                            |



 

### <a name="jpeg-metadata"></a>Metadados JPEG

O formato de imagem JPEG oferece suporte a metadados em nível de quadro.

> [!Note]  
> Para obter uma lista completa de metadados JPEG juntamente com informações mais detalhadas, consulte o [padrão JPEG do EXIF](http://www.cipa.jp/std/documents/e/DC-008-2010_E.pdf).

 

### <a name="frame-metadata"></a>Metadados do quadro

A tabela a seguir fornece os caminhos de consulta de metadados disponíveis que podem ser usados para acessar metadados JPEG no nível de quadro.



| Caminho                                                               | Nome                 | Tipo                                          |
|--------------------------------------------------------------------|----------------------|-----------------------------------------------|
| /app0                                                              | App0                 | VT \_ desconhecido – leitor de consulta do App0/gravador        |
| /app0/{UShort = 0}                                                   | Versão              | \_UI2 VT                                       |
| /app0/{UShort = 1}                                                   | Unidades                | \_UI1 VT                                       |
| /app0/{UShort = 2}                                                   | DpiX                 | \_UI2 VT                                       |
| /app0/{UShort = 3}                                                   | DpiY                 | \_UI2 VT                                       |
| /app0/{UShort = 4}                                                   | Xthumbnail           | \_UI1 VT                                       |
| /app0/{UShort = 5}                                                   | Ythumbnail           | \_UI1 VT                                       |
| /app0/{UShort = 6}                                                   | ThumbnailData        | \_blob VT                                      |
| /App1                                                              | Aplicativo1                 | VT \_ desconhecido – App1 leitor/gravador de consulta        |
| /App1/IFD ou/App1/{UShort = 0}                                     | 0 IFD                | VT \_ desconhecido – leitor de consulta de IFD/gravador         |
| /App1/IFD/EXIF ou/App1/IFD/{UShort = 34665}                         | IFD DE EXIF             | VT \_ desconhecido – leitor de consulta do EXIF/gravador        |
| /App1/Thumb ou/App1/{UShort = 1}                                   | IFD de miniatura        | VT \_ desconhecido – leitor de consulta do SubIFD/gravador      |
| /app13                                                             | App13                | VT \_ desconhecido – leitor de consulta do App13/gravador       |
| /app13/IRB ou/app13/{UShort = 0}                                    | IRB                  | VT \_ desconhecido-leitor de consulta do IRB/gravador         |
| /app13/IRB/{ULONGLONG = \* } onde \* = identificador IRB (consulte a especificação IRB) | Entrada IRB            | VT \_ desconhecido-leitor/gravador de consultas desconhecido     |
| /app13/IRB/{ULONGLONG = \* }/{}                                       | Conteúdo da entrada IRB   | \_blob VT                                      |
| /app13/IRB/8bimiptc ou/app13/IRB/{ULONGLONG = 61857348781060}       | 8BIMIPTC             | VT \_ desconhecido – leitor de consulta do 8BIMIPTC/gravador    |
| /app13/irb/8bimiptc/iptc                                           | IPTC                 | VT \_ desconhecido – leitor/gravador de consulta IPTC        |
| /app13/IRB/8bimiptc/IPTC/{Str = \* }                                  | Entrada IPTC           | Variável                                      |
| /app13/irb/8bimResInfo ou/app13/IRB/{ULONGLONG = 61857348781037}    | Informações de resolução de 8BIM | VT \_ desconhecido – leitor de consulta/gravador             |
| /app13/irb/8bimResInfo/PString                                     |                      | a VT \_ LPSTR                                     |
| /app13/irb/8bimResInfo/HResolution                                 |                      | \_UI4 VT                                       |
| /app13/irb/8bimResInfo/VResolution                                 |                      | \_UI4 VT                                       |
| /app13/irb/8bimResInfo/WidthUnit                                   |                      | \_UI2 VT                                       |
| /app13/irb/8bimResInfo/HeightUnit                                  |                      | \_UI2 VT                                       |
| /app13/irb/8bimResInfo/HResolutionUnit                             |                      | \_UI2 VT                                       |
| /app13/irb/8bimResInfo/VResolutionUnit                             |                      | \_UI2 VT                                       |
| /com                                                               | Comentário JPEG         | VT \_ desconhecido-leitor de consulta de comentário/gravador     |
| /com/TextEntry                                                     |                      | LPSTR                                         |
| /luminance                                                         | Luminância            | VT \_ desconhecido-leitor de consulta de luminância/gravador   |
| /luminance/TableEntry                                              |                      | \_Vetor VT UI1 \| VT \_                         |
| /chrominance                                                       | Crominância          | VT \_ desconhecido – leitor de consulta do crominância/gravador |
| /chrominance/TableEntry                                            |                      | \_Vetor VT UI1 \| VT \_                         |
| /xmp                                                               | XMP                  | VT \_ desconhecido – leitor de consulta XMP/gravador         |



 

## <a name="file-format-independent-metadata"></a>Metadados independentes de formato de arquivo

As seções a seguir contêm informações relacionadas a formatos de metadados com suporte em vários formatos de imagem. Cada tabela tem as seguintes colunas:

-   **Caminho relativo** -o caminho de consulta usado para recuperar o item de metadados em relação ao bloco de metadados.
-   **Nome** -o nome do item de metadados.
-   **Tipo** – o tipo do item de metadados recuperado do caminho de consulta. Os metadados recuperados pelo [WIC](-wic-api.md) são retornados na forma de PROPVARIANT, que relata o tipo de dados usando a enumeração VarType.

> [!Note]  
> As tabelas aqui fornecem apenas o caminho relativo para acessar um item de metadados dentro do formato de metadados específico. Para obter a consulta de metadados totalmente qualificada, acrescente esse caminho relativo à consulta de bloco de metadados para o formato de metadados específico.

 

Por exemplo, para acessar o sinalizador de [orientação](-wic-photoprop-system-photo-orientation.md) em um arquivo JPEG, use a seguinte expressão:

-   /App1/IFD/{UShort = 274}

Em um arquivo TIFF, use a seguinte expressão:

-   /IFD/{UShort = 274}

Neste exemplo, observe que diferentes formatos de imagem podem armazenar um determinado bloco de metadados de forma diferente e, portanto, a consulta de metadados totalmente qualificada para acessar um determinado item de metadados pode ser específica ao formato de imagem. Consulte cada tabela de formato para localizar a consulta de metadados apropriada para acessar um determinado bloco de metadados.

### <a name="ifd-metadata"></a>Metadados de IFD

Uma IFD, ou um diretório de arquivos de imagem, é uma estrutura de dados definida no padrão TIFF que pode conter metadados de imagem. Ele identifica cada item de metadados usando uma marca do tipo ushort. JPEG, TIFF e JPEG-XR dão suporte a metadados de IFD. Formatos de terceiros, como alguns formatos brutos de câmera, também podem dar suporte a metadados IFD.

A tabela aqui fornece caminhos de consulta de metadados relativos para acessar alguns itens de metadados IFD usados com frequência. A estrutura de dados IFD permite a extensibilidade de terceiros e essa tabela não é uma lista exaustiva. Consulte o padrão TIFF para obter mais informações.

> [!Note]  
> Embora o JPEG e outros formatos ofereçam suporte à estrutura de dados IFD, eles não podem usar todos os itens de metadados que ele define. Consulte o padrão de cada formato para obter mais informações.

 

> [!Note]  
> Alguns itens de metadados na tabela aqui exigem interpretação ou informações adicionais para uso adequado, consulte o padrão TIFF. Por exemplo, o item de metadados [PhotometricInterpretation](-wic-photoprop-system-photo-photometricinterpretation.md) retorna um PROPVARIANT do tipo VT \_ UI2. No entanto, de acordo com o padrão TIFF, ele é interpretado como uma enumeração. Consulte o padrão TIFF para obter mais informações.

 



| Caminho relativo   | Nome                      | Tipo                                           |
|-----------------|---------------------------|------------------------------------------------|
| /{ushort = 256}   | ImageWidth                | VT \_ UI2 ou VT \_ UI4                             |
| /{ushort = 257}   | ImageLength               | VT \_ UI2 ou VT \_ UI4                             |
| /{ushort = 258}   | BitsPerSample             | \_UI2 VT                                        |
| /{ushort = 259}   | Compactação               | \_UI2 VT                                        |
| /{ushort = 262}   | PhotometricInterpretation | \_UI2 VT                                        |
| /{ushort = 274}   | Orientation               | \_UI2 VT                                        |
| /{ushort = 277}   | SamplesPerPixel           | \_UI2 VT                                        |
| /{ushort = 284}   | PlanarConfiguration       | \_UI2 VT                                        |
| /{ushort = 530}   | YCbCrSubSampling          | \_UI2 de vetor \| VT \_ VT                          |
| /{ushort = 531}   | YCbCrPositioning          | \_UI2 VT                                        |
| /{ushort = 282}   | XResolution               | \_UI8 VT                                        |
| /{ushort = 283}   | YResolution               | \_UI8 VT                                        |
| /{ushort = 296}   | ResolutionUnit            | \_UI2 VT                                        |
| /{ushort = 306}   | Datetime                  | a VT \_ LPSTR                                      |
| /{ushort = 270}   | ImageDescription          | a VT \_ LPSTR                                      |
| /{ushort = 271}   | Faça                      | a VT \_ LPSTR                                      |
| /{ushort = 272}   | Modelar                     | a VT \_ LPSTR                                      |
| /{ushort = 305}   | Software                  | a VT \_ LPSTR                                      |
| /{ushort = 315}   | Autor                    | a VT \_ LPSTR                                      |
| /{ushort = 33432} | Direitos autorais                 | a VT \_ LPSTR                                      |
| /{ushort = 338}   | ExtraSamples              | \_UI2 VT                                        |
| /{ushort = 254}   | NewSubfileType            | \_UI4 VT                                        |
| /{ushort = 278}   | RowsPerStrip              | VT \_ UI2 ou VT \_ UI4                             |
| /{ushort = 279}   | StripByteCounts           | Vetor VT VT \_ \| \_ UI2 ou VT \_ vector \| VT \_ UI4 |
| /{ushort = 273}   | StripOffsets              | Vetor VT VT \_ \| \_ UI2 ou VT \_ vector \| VT \_ UI4 |



 

### <a name="exif-metadata"></a>Metadados EXIF

Os metadados EXIF são definidos como parte da especificação JPEG do EXIF. Os metadados EXIF baseiam-se na estrutura de dados IFD, conforme definido no padrão TIFF, e fornece atributos adicionais, como informações sobre os dispositivos e atributos fotográficos usados para criar a imagem. Ele identifica cada item de metadados usando uma marca do tipo ushort. JPEG, TIFF e JPEG-XR dão suporte a metadados EXIF. Formatos de terceiros, como alguns formatos brutos de câmera, também podem dar suporte a metadados EXIF.

A tabela a seguir fornece caminhos de consulta de metadados relativos para acessar alguns itens de metadados EXIF usados com frequência. A estrutura de dados EXIF permite a extensibilidade de terceiros e essa tabela não é uma lista completa; consulte o padrão EXIF para obter mais informações.

> [!Note]  
> Muitos itens de metadados EXIF são definidos no padrão EXIF como o tipo "RATIONAL" ou "SRATIONAL". Um "racional" consiste em um numerador e um denominador, ambos os quais são inteiros de 32 bits sem sinal. O numerador está contido nos bits de 32 altos e o denominador nos bits inferiores de 32. No [WIC](-wic-api.md), eles são retornados como PROPVARIANT com um tipo de VT \_ UI8 ou VT \_ i8, respectivamente; o valor real é armazenado como um \_ número inteiro ULARGE ou \_ inteiro grande, respectivamente. Para acessar o numerador e o denominador, leia os membros HighPart e LowPart do \_ número inteiro ULARGE ou \_ valor inteiro grande.

 

> [!Note]  
> Determinados itens de metadados na tabela abaixo exigem interpretação ou informações adicionais para uso adequado. Por exemplo, o item de metadados [colorspace](-wic-photoprop-system-image-colorspace.md) retorna um PROPVARIANT do tipo VT \_ UI2. No entanto, de acordo com o padrão EXIF, ele é interpretado como uma enumeração. Consulte o padrão EXIF para obter mais informações.

 



| Caminho relativo   | Nome                      | Tipo                  |
|-----------------|---------------------------|-----------------------|
| /{ushort = 36864} | ExifVersion               | \_blob VT              |
| /{ushort = 40960} | FlashpixVersion           | \_blob VT              |
| /{ushort = 40961} | ColorSpace                | \_UI2 VT               |
| /{ushort = 40962} | PixelXDimension           | VT \_ UI2 ou VT \_ UI4    |
| /{ushort = 40963} | PixelYDimension           | VT \_ UI2 ou VT \_ UI4    |
| /{ushort = 37500} | MakerNote                 | \_blob VT              |
| /{ushort = 37510} | UserComment               | LPWStr do VT \_            |
| /{ushort = 36867} | DateTimeOriginal          | a VT \_ LPSTR             |
| /{ushort = 36868} | DateTimeDigitized         | a VT \_ LPSTR             |
| /{ushort = 42016} | ImageUniqueID             | a VT \_ LPSTR             |
| /{ushort = 42032} | CameraOwnerName           | a VT \_ LPSTR             |
| /{ushort = 42033} | BodySerialNumber          | a VT \_ LPSTR             |
| /{ushort = 42034} | LensSpecification         | \_UI8 de vetor \| VT \_ VT |
| /{ushort = 42035} | LensMake                  | a VT \_ LPSTR             |
| /{ushort = 42036} | LensModel                 | a VT \_ LPSTR             |
| /{ushort = 42037} | LensSerialNumber          | a VT \_ LPSTR             |
| /{ushort = 33434} | Exposiçãotime              | \_UI8 VT               |
| /{ushort = 33437} | FNumber                   | \_UI8 VT               |
| /{ushort = 34850} | ExposureProgram           | \_UI2 VT               |
| /{ushort = 34852} | SpectralSensitivity       | a VT \_ LPSTR             |
| /{ushort = 34855} | PhotographicSensitivity   | \_UI2 de vetor \| VT \_ VT |
| /{ushort = 34856} | OECF                      | \_blob VT              |
| /{ushort = 34864} | Sensibilidade           | \_UI2 VT               |
| /{ushort = 34865} | StandardOutputSensitivity | \_UI4 VT               |
| /{ushort = 34866} | RecommendedExposureIndex  | \_UI4 VT               |
| /{ushort = 34867} | ISOSpeed                  | \_UI4 VT               |
| /{ushort = 34868} | ISOSpeedLatitudeyyy       | \_UI4 VT               |
| /{ushort = 34869} | ISOSpeedLatitudezzz       | \_UI4 VT               |
| /{ushort = 37377} | ShutterSpeedValue         | VT \_ i8                |
| /{ushort = 37378} | Aberturavalue             | \_UI8 VT               |
| /{ushort = 37379} | Brilhovalue           | VT \_ i8                |
| /{ushort = 37380} | ExposureBiasValue         | VT \_ i8                |
| /{ushort = 37381} | MaxApertureValue          | \_UI8 VT               |
| /{ushort = 37382} | SubjectDistance           | \_UI8 VT               |
| /{ushort = 37383} | MeteringMode              | \_UI2 VT               |
| /{ushort = 37384} | Claridade               | \_UI2 VT               |
| /{ushort = 37385} | Flash                     | \_UI2 VT               |
| /{ushort = 37386} | FocalLength               | \_UI8 VT               |
| /{ushort = 37396} | SubjectArea               | \_UI2 de vetor \| VT \_ VT |
| /{ushort = 41483} | FlashEnergy               | \_UI8 VT               |
| /{ushort = 41484} | SpatialFrequencyResponse  | \_blob VT              |
| /{ushort = 41486} | FocalPlaneXResolution     | \_UI8 VT               |
| /{ushort = 41487} | FocalPlaneYResolution     | \_UI8 VT               |
| /{ushort = 41488} | FocalPlaneResolutionUnit  | \_UI2 VT               |
| /{ushort = 41492} | SubjectLocation           | \_UI2 de vetor \| VT \_ VT |
| /{ushort = 41493} | ExposureIndex             | \_UI8 VT               |
| /{ushort = 41495} | SensingMethod             | \_UI2 VT               |
| /{ushort = 41728} | FileSource                | \_blob VT              |
| /{ushort = 41729} | Scenetype                 | \_blob VT              |
| /{ushort = 41730} | CFAPattern                | \_blob VT              |
| /{ushort = 41985} | CustomRendered            | \_UI2 VT               |
| /{ushort = 41986} | Exposiçãomode              | \_UI2 VT               |
| /{ushort = 41987} | WhiteBalance              | \_UI2 VT               |
| /{ushort = 41988} | DigitalZoomRatio          | \_UI8 VT               |
| /{ushort = 41989} | FocalLengthIn35mmFilm     | \_UI2 VT               |
| /{ushort = 41990} | SceneCaptureType          | \_UI2 VT               |
| /{ushort = 41991} | GainControl               | \_UI8 VT               |
| /{ushort = 41992} | Contraste                  | \_UI2 VT               |
| /{ushort = 41993} | Saturação                | \_UI2 VT               |
| /{ushort = 41994} | Nitidez                 | \_UI2 VT               |
| /{ushort = 41995} | DeviceSettingDescription  | \_blob VT              |
| /{ushort = 41996} | SubjectDistanceRange      | \_UI2 VT               |



 

### <a name="gps-metadata"></a>Metadados de GPS

Os metadados do GPS contêm informações de geolocalização e são definidos como parte da especificação JPEG do EXIF. Ele identifica cada item de metadados usando uma marca do tipo ushort. JPEG, TIFF e JPEG-XR dão suporte a metadados de GPS; formatos de terceiros, como alguns formatos brutos de câmera, também podem dar suporte a metadados GPS.

A tabela a seguir fornece caminhos de consulta de metadados relativos para acessar alguns itens de metadados GPS usados com frequência. Esta tabela não é uma lista completa; consulte o padrão EXIF para obter mais informações.

> [!Note]  
> Muitos itens de metadados GPS são definidos no padrão EXIF como o tipo "RATIONAL". Um "racional" consiste em um numerador e um denominador, ambos os quais são inteiros de 32 bits sem sinal. O numerador está contido nos bits de 32 altos e o denominador nos bits inferiores de 32. No [WIC](-wic-api.md), eles são retornados como PROPVARIANT com um tipo de VT \_ UI8. O valor real é armazenado como um \_ número inteiro ULARGE. Para acessar o numerador e o denominador, leia os membros HighPart e LowPart do \_ valor inteiro ULARGE.

 

> [!Note]  
> Alguns itens de metadados na tabela aqui exigem interpretação ou informações adicionais para uso adequado. Por exemplo, o item de metadados GPSLatitudeRef retorna um PROPVARIANT do tipo VT \_ LPSTR. De acordo com o padrão EXIF, essa cadeia de caracteres é "N" ou "S", representando o norte ou o Latitude. Consulte o padrão EXIF para obter mais informações.

 



| Caminho relativo | Nome            | Tipo                                          |
|---------------|-----------------|-----------------------------------------------|
| {ushort = 0}    | GPSVersionID    | \_UI1 de vetor \| VT \_ VT                         |
| {ushort = 1}    | GPSLatitudeRef  | a VT \_ LPSTR                                     |
| {ushort = 2}    | GPSLatitude     | \_UI8 de vetor \| VT \_ VT                         |
| {ushort = 3}    | GPSLongitudeRef | a VT \_ LPSTR                                     |
| {ushort = 4}    | GPSLongitude    | {ushort = 4} GPSLongitude VT \_ vector \| \_ UI8 |
| {ushort = 5}    | GPSAltitudeRef  | \_UI1 VT                                       |
| {ushort = 6}    | GPSAltitude     | \_UI8 VT                                       |
| {ushort = 7}    | GPSTimeStamp    | \_UI8 de vetor \| VT \_ VT                         |
| {ushort = 8}    | GPSSatellites   | a VT \_ LPSTR                                     |
| {ushort = 9}    | GPSStatus       | a VT \_ LPSTR                                     |
| {ushort = 10}   | GPSMeasureMode  | a VT \_ LPSTR                                     |
| {ushort = 11}   | GPSDOP          | \_UI8 VT                                       |
| {ushort = 12}   | GPSSpeedRef     | a VT \_ LPSTR                                     |
| {ushort = 13}   | GPSSpeed        | \_UI8 VT                                       |
| {ushort = 14}   | GPSTrackRef     | a VT \_ LPSTR                                     |
| {ushort = 15}   | GPSTrack        | \_UI8 VT                                       |



 

### <a name="xmp-metadata"></a>Metadados XMP

O XMP é um padrão de metadados extensível baseado em XML. Os itens de metadados podem ser hierárquicos e conter estruturas de dados complexas. JPEG, TIFF e JPEG-XR dão suporte a metadados XMP. Formatos de terceiros, como alguns formatos brutos de câmera, também podem dar suporte a metadados XMP.

O padrão XMP pode ser obtido em: <https://www.adobe.com/devnet/xmp.html> .

XMP e permite que entidades de terceiros publiquem seus próprios esquemas, ou namespaces, que permitem definir novos itens de metadados sem a necessidade de modificar o padrão XMP. Um esquema XMP é identificado exclusivamente por uma URL, mas o [WIC](-wic-api.md) fornece um conjunto de identificadores amigáveis para esquemas bem conhecidos.

Os itens de metadados XMP são identificados por um nome de cadeia de caracteres, bem como um identificador de esquema. Como prática recomendada, cada consulta de metadados XMP deve especificar o esquema e o nome. Se o identificador de esquema estiver ausente, o JPEG tentará corresponder o nome dos metadados em todos os namespaces presentes no pacote de metadados XMP.

Por exemplo, para obter a propriedade de classificação conforme definido pelo esquema XMP em uma imagem JPEG, use a seguinte consulta:

-   /XMP/{WSTR =https://ns.adobe.com/xap/1.0/}:Rating

A primeira parte, "/XMP", recupera o leitor/gravador de metadados XMP para a imagem. " https://ns.adobe.com/xap/1.0/ " é a URL do esquema XMP, conforme definido no padrão XMP. A URL é colocada em uma expressão de dados para permitir o uso de caracteres como uma barra (/). Finalmente, "rating" é o nome do item de metadados real, conforme definido pelo esquema XMP, e é separado do identificador de esquema por dois-pontos (:).

Neste exemplo, o WIC fornece um identificador amigável para o esquema XMP, que pode ser usado no lugar da URL completa. Assim, a consulta anterior pode ser reescrita como:

-   /XMP/XMP: classificação

O [WIC](-wic-api.md) fornece prefixos de esquema amigáveis para os seguintes esquemas usados com frequência:



| Prefixo do esquema  | URL do esquema                                        | Link para Standard                                         |
|----------------|---------------------------------------------------|----------------------------------------------------------|
| RDF            | https://www.w3.org/1999/02/22-rdf-syntax-ns\#      | <https://www.w3.org/TR/REC-rdf-syntax/>                   |
| dc             | https://purl.org/dc/elements/1.1/                  | <https://www.adobe.com/devnet/xmp.html>                   |
| XMP            | https://ns.adobe.com/xap/1.0/                      | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpidq         | https://ns.adobe.com/xmp/Identifier/qual/1.0/      | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpRights      | https://ns.adobe.com/xap/1.0/rights/               | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpMM          | https://ns.adobe.com/xap/1.0/mm/                   | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpBJ          | https://ns.adobe.com/xap/1.0/bj/                   | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpTPg         | https://ns.adobe.com/xap/1.0/t/pg/                 | <https://www.adobe.com/devnet/xmp.html>                   |
| pdf            | https://ns.adobe.com/pdf/1.3/                      | <https://www.adobe.com/devnet/xmp.html>                   |
| Photoshop      | https://ns.adobe.com/photoshop/1.0/                | <https://www.adobe.com/devnet/xmp.html>                   |
| tiff           | https://ns.adobe.com/tiff/1.0/                     | <https://www.adobe.com/devnet/xmp.html>                   |
| EXIF           | https://ns.adobe.com/exif/1.0/                     | <https://www.adobe.com/devnet/xmp.html>                   |
| stDim          | https://ns.adobe.com/xap/1.0/sType/Dimensions\#    | <https://www.adobe.com/devnet/xmp.html>                   |
| xapGImg        | https://ns.adobe.com/xap/1.0/g/img/                | <https://www.adobe.com/devnet/xmp.html>                   |
| stEvt          | https://ns.adobe.com/xap/1.0/sType/ResourceEvent\# | <https://www.adobe.com/devnet/xmp.html>                   |
| stRef          | https://ns.adobe.com/xap/1.0/sType/ResourceRef\#   | <https://www.adobe.com/devnet/xmp.html>                   |
| stVer          | https://ns.adobe.com/xap/1.0/sType/Version\#       | <https://www.adobe.com/devnet/xmp.html>                   |
| stJob          | https://ns.adobe.com/xap/1.0/sType/Job\#           | <https://www.adobe.com/devnet/xmp.html>                   |
| indicação            | https://ns.adobe.com/exif/1.0/aux/                 | <https://www.adobe.com/devnet/xmp.html>                   |
| CRS            | https://ns.adobe.com/camera-raw-settings/1.0/      | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpDM          | https://ns.adobe.com/xmp/1.0/DynamicMedia/         | <https://www.adobe.com/devnet/xmp.html>                   |
| Iptc4xmpCore   | https://iptc.org/std/Iptc4xmpCore/1.0/xmlns/       | <https://www.iptc.org/cms/site/index.html?channel=CH0099> |
| MicrosoftPhoto | https://ns.microsoft.com/photo/1.0/                | [Visão geral de marcação de pessoas](-wic-people-tagging.md)       |
| MP             | https://ns.microsoft.com/photo/1.2/                | [Visão geral de marcação de pessoas](-wic-people-tagging.md)       |
| MPRI           | https://ns.microsoft.com/photo/1.2/t/RegionInfo\#  | [Visão geral de marcação de pessoas](-wic-people-tagging.md)       |
| MPReg          | https://ns.microsoft.com/photo/1.2/t/Region\#      | [Visão geral de marcação de pessoas](-wic-people-tagging.md)       |



 

Se não houver nenhum prefixo de esquema amigável para um esquema específico, por exemplo, se uma imagem contiver metadados XMP usando um esquema de terceiros personalizado, a consulta de metadados deverá usar a URL de esquema completa.

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

[Visão geral da extensibilidade de metadados](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Como: codificar novamente uma imagem JPEG com metadados](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 
