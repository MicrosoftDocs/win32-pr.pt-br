---
description: A lista a seguir fornece descrições dos itens de propriedade com suporte no Windows GDI+.
ms.assetid: fc95aa3f-8381-430d-8cbf-6d23816a738d
title: Descrições de item de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc2a627ec809bb4f7d7299c522fd0e9d3e1cc05
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/27/2021
ms.locfileid: "105636118"
---
# <a name="property-item-descriptions"></a>Descrições de item de propriedade

A lista a seguir fornece descrições dos itens de propriedade com suporte no Windows GDI+. As descrições são breves e gerais para que se apliquem a uma variedade de formatos de arquivo de imagem. Para obter uma descrição detalhada de como um item de propriedade é usado por um determinado formato de arquivo, consulte a especificação para esse formato de arquivo. Para obter links para várias especificações de arquivo e outros documentos que descrevem metadados em detalhes, consulte [especificações de formato de arquivo de imagem](-gdiplus-constant-image-file-format-specifications.md).

O formato EXIF (exchangável Image File) é um padrão JEIDA (Associação de desenvolvimento do setor eletrônico) do Japão, revisado em junho de 1998 como a versão 2,1. Partes da especificação EXIF são usadas com a permissão de JEIDA.

## <a name="propertytaggpsver"></a>PropertyTagGpsVer

Versão da IFD GPS (Global Positioning Systems), fornecida como 2.0.0.0. Essa marca é obrigatória quando a marca PropertyTagGpsIFD está presente. Quando a versão for 2.0.0.0, o valor da marca será 0x02000000.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x0000              |
| Type  | PropertyTagTypeByte |
| Contagem | 4                   |



 

## <a name="propertytaggpslatituderef"></a>PropertyTagGpsLatitudeRef

Cadeia de caracteres terminada em nulo que especifica se a latitude é norte ou Sul. `N` Especifica a latitude do Norte e `S` especifica a latitude do Sul.



| Informações da propriedade | Valor |
|-------|--------------------------------------------|
| Marca   | 0x0001                                     |
| Type  | PropertyTagTypeASCII                       |
| Contagem | 2 (um caractere mais o terminador nulo) |



 

## <a name="propertytaggpslatitude"></a>PropertyTagGpsLatitude

Latitude. A latitude é expressa como três valores racionalizados fornecendo os graus, os minutos e os segundos, respectivamente. Quando graus, minutos e segundos são expressos, o formato é dd/1, mm/1, SS/1. Quando os graus e minutos são usados e, por exemplo, frações de minutos são dadas até duas casas decimais, o formato é dd/1, MMMM/100, 0/1.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x0002                  |
| Type  | PropertyTagTypeRational |
| Contagem | 3                       |



 

## <a name="propertytaggpslongituderef"></a>PropertyTagGpsLongitudeRef

Cadeia de caracteres terminada em nulo que especifica se a longitude é a longitude Oriental ou oeste. `E` Especifica a longitude Oriental e `W` especifica a longitude ocidental.



| Informações da propriedade | Valor |
|-------|--------------------------------------------|
| Marca   | 0x0003                                     |
| Type  | PropertyTagTypeASCII                       |
| Contagem | 2 (um caractere mais o terminador nulo) |



 

## <a name="propertytaggpslongitude"></a>PropertyTagGpsLongitude

Longitude. A longitude é expressa como três valores racionalizados fornecendo os graus, os minutos e os segundos, respectivamente. Quando graus, minutos e segundos são expressos, o formato é DDD/1, mm/1, SS/1. Quando os graus e minutos são usados e, por exemplo, frações de minutos são dadas até duas casas decimais, o formato é DDD/1, MMMM/100, 0/1.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x0004                  |
| Type  | PropertyTagTypeRational |
| Contagem | 3                       |



 

## <a name="propertytaggpsaltituderef"></a>PropertyTagGpsAltitudeRef

Altitude de referência, em metros.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x0005              |
| Type  | PropertyTagTypeByte |
| Contagem | 1                   |



 

## <a name="propertytaggpsaltitude"></a>PropertyTagGpsAltitude

Altitude, em metros, com base na altitude de referência especificada por PropertyTagGpsAltitudeRef.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x0006                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytaggpsgpstime"></a>PropertyTagGpsGpsTime

Tempo como UTC (tempo Universal Coordenado). O valor é expresso como três números racionales que fornecem a hora, minuto e segundo.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x0007                  |
| Type  | PropertyTagTypeRational |
| Contagem | 3                       |



 

## <a name="propertytaggpsgpssatellites"></a>PropertyTagGpsGpsSatellites

Cadeia de caracteres terminada em nulo que especifica os satélites de GPS usados para medições. Essa marca pode ser usada para especificar o número de ID, o ângulo de elevação, Azimuth, SNR e outras informações sobre cada satélite. O formato não foi especificado. Se o receptor GPS for incapaz de fazer medições, o valor da marca deverá ser definido como **NULL**.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x0008                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytaggpsgpsstatus"></a>PropertyTagGpsGpsStatus

Cadeia de caracteres terminada em nulo que especifica o status do receptor GPS quando a imagem é registrada. `A` significa que a medição está em andamento e `V` significa que a medição é interoperabilidade.



| Informações da propriedade | Valor |
|-------|--------------------------------------------|
| Marca   | 0x0009                                     |
| Type  | PropertyTagTypeASCII                       |
| Contagem | 2 (um caractere mais o terminador nulo) |



 

## <a name="propertytaggpsgpsmeasuremode"></a>PropertyTagGpsGpsMeasureMode

Cadeia de caracteres terminada em nulo que especifica o modo de medição GPS. `2` Especifica a medida de 2-D e `3` especifica a medida 3D.



| Informações da propriedade | Valor |
|-------|--------------------------------------------|
| Marca   | 0x000A                                     |
| Type  | PropertyTagTypeASCII                       |
| Contagem | 2 (um caractere mais o terminador nulo) |



 

## <a name="propertytaggpsgpsdop"></a>PropertyTagGpsGpsDop

DOP GPS (grau de precisão de dados). Um valor de HDOP é gravado durante a medição de 2D e um valor de PDOP é gravado durante a medição 3D.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x000B                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytaggpsspeedref"></a>PropertyTagGpsSpeedRef

Cadeia de caracteres terminada em nulo que especifica a unidade usada para expressar a velocidade do movimento do receptor GPS. `K`, `M` e `N` representam quilômetros por hora, milhas por hora e nós respectivamente.



| Informações da propriedade | Valor |
|-------|--------------------------------------------|
| Marca   | 0x000C                                     |
| Type  | PropertyTagTypeASCII                       |
| Contagem | 2 (um caractere mais o terminador nulo) |



 

## <a name="propertytaggpsspeed"></a>PropertyTagGpsSpeed

Velocidade do movimento do receptor GPS.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x000D                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytaggpstrackref"></a>PropertyTagGpsTrackRef

Cadeia de caracteres terminada em nulo que especifica a referência para dar a direção do movimento do receptor de GPS. `T` Especifica a direção true e `M` especifica a direção magnética.



| Informações da propriedade | Valor |
|-------|--------------------------------------------|
| Marca   | 0x000E                                     |
| Type  | PropertyTagTypeASCII                       |
| Contagem | 2 (um caractere mais o terminador nulo) |



 

## <a name="propertytaggpstrack"></a>PropertyTagGpsTrack

Direção da movimentação do receptor de GPS. O intervalo de valores é de 0, 0 a 359,99.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x000F                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytaggpsimgdirref"></a>PropertyTagGpsImgDirRef

Cadeia de caracteres terminada em nulo que especifica a referência para a direção da imagem quando ela é capturada. `T` Especifica a direção true e `M` especifica a direção magnética.



| Informações da propriedade | Valor |
|-------|--------------------------------------------|
| Marca   | 0x0010                                     |
| Type  | PropertyTagTypeASCII                       |
| Contagem | 2 (um caractere mais o terminador nulo) |



 

## <a name="propertytaggpsimgdir"></a>PropertyTagGpsImgDir

Direção da imagem quando ela foi capturada. O intervalo de valores é de 0, 0 a 359,99.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x0011                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytaggpsmapdatum"></a>PropertyTagGpsMapDatum

Cadeia de caracteres terminada em nulo que especifica dados de pesquisa geodésico usados pelo receptor GPS. Se os dados da pesquisa estiverem restritos ao Japão, o valor dessa marca será `TOKYO` ou `WGS-84` .



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x0012                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytaggpsdestlatref"></a>PropertyTagGpsDestLatRef

Cadeia de caracteres terminada em nulo que especifica se a latitude do ponto de destino é norte ou sul da latitude. `N` Especifica a latitude do Norte e `S` especifica a latitude do Sul.



| Informações da propriedade | Valor |
|-------|--------------------------------------------|
| Marca   | 0x0013                                     |
| Type  | PropertyTagTypeASCII                       |
| Contagem | 2 (um caractere mais o terminador nulo) |



 

## <a name="propertytaggpsdestlat"></a>PropertyTagGpsDestLat

Latitude do ponto de destino. A latitude é expressa como três valores racionalizados fornecendo os graus, minutos e segundos, respectivamente. Quando graus, minutos e segundos são expressos, o formato é dd/1, mm/1, SS/1. Quando os graus e minutos são usados e, por exemplo, frações de minutos são dadas até duas casas decimais, o formato é dd/1, MMMM/100, 0/1.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x0014                  |
| Type  | PropertyTagTypeRational |
| Contagem | 3                       |



 

## <a name="propertytaggpsdestlongref"></a>PropertyTagGpsDestLongRef

Cadeia de caracteres terminada em nulo que especifica se a longitude do ponto de destino é a longitude Oriental ou oeste. `E` Especifica a longitude Oriental e `W` especifica a longitude ocidental.



| Informações da propriedade | Valor |
|-------|--------------------------------------------|
| Marca   | 0x0015                                     |
| Type  | PropertyTagTypeASCII                       |
| Contagem | 2 (um caractere mais o terminador nulo) |



 

## <a name="propertytaggpsdestlong"></a>PropertyTagGpsDestLong

Longitude do ponto de destino. A longitude é expressa como três valores racionalizados fornecendo os graus, os minutos e os segundos, respectivamente. Quando graus, minutos e segundos são expressos, o formato é DDD/1, mm/1, SS/1. Quando os graus e minutos são usados e, por exemplo, frações de minutos são dadas até duas casas decimais, o formato é DDD/1, MMMM/100, 0/1.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x0016                  |
| Type  | PropertyTagTypeRational |
| Contagem | 3                       |



 

## <a name="propertytaggpsdestbearref"></a>PropertyTagGpsDestBearRef

Cadeia de caracteres terminada em nulo que especifica a referência usada para dar a passagem ao ponto de destino. `T` Especifica a direção true e `M` especifica a direção magnética.



| Informações da propriedade | Valor |
|-------|--------------------------------------------|
| Marca   | 0x0017                                     |
| Type  | PropertyTagTypeASCII                       |
| Contagem | 2 (um caractere mais o terminador nulo) |



 

## <a name="propertytaggpsdestbear"></a>PropertyTagGpsDestBear

Enrumo ao ponto de destino. O intervalo de valores é de 0, 0 a 359,99.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x0018                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytaggpsdestdistref"></a>PropertyTagGpsDestDistRef

Cadeia de caracteres terminada em nulo que especifica a unidade usada para expressar a distância para o ponto de destino. K, M e N representam quilômetros, milhas e nós, respectivamente.



| Informações da propriedade | Valor |
|-------|--------------------------------------------|
| Marca   | 0x0019                                     |
| Type  | PropertyTagTypeASCII                       |
| Contagem | 2 (um caractere mais o terminador nulo) |



 

## <a name="propertytaggpsdestdist"></a>PropertyTagGpsDestDist

Distância para o ponto de destino.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x001A                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytagnewsubfiletype"></a>PropertyTagNewSubfileType

Tipo de dados em um subarquivo.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x00FE              |
| Type  | PropertyTagTypeLong |
| Contagem | 1                   |



 

## <a name="propertytagsubfiletype"></a>PropertyTagSubfileType

Tipo de dados em um subarquivo.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x00FF               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagimagewidth"></a>PropertyTagImageWidth

Número de pixels por linha.



| Informações da propriedade | Valor |
|-------|---------------------------------------------|
| Marca   | 0x0100                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Contagem | 1                                           |



 

## <a name="propertytagimageheight"></a>PropertyTagImageHeight

Número de linhas de pixel.



| Informações da propriedade | Valor |
|-------|---------------------------------------------|
| Marca   | 0x0101                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Contagem | 1                                           |



 

## <a name="propertytagbitspersample"></a>PropertyTagBitsPerSample

Número de bits por componente de cor. Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informações da propriedade | Valor |
|-------|------------------------------------------|
| Marca   | 0x0102                                   |
| Type  | PropertyTagTypeShort                     |
| Contagem | Número de amostras (componentes) por pixel |



 

## <a name="propertytagcompression"></a>PropertyTagCompression

Esquema de compactação usado para os dados da imagem.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x0103               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagphotometricinterp"></a>PropertyTagPhotometricInterp

Como os dados de pixel serão interpretados.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x0106               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagthreshholding"></a>PropertyTagThreshHolding

Técnica usada para converter pixels de cinza em pixels pretos e brancos.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x0107               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagcellwidth"></a>PropertyTagCellWidth

Largura da matriz de pontilhamento ou de meio-tom.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x0108               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagcellheight"></a>PropertyTagCellHeight

Altura da matriz de pontilhado ou de meio-tom.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x0109               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagfillorder"></a>PropertyTagFillOrder

Ordem lógica de bits em um byte.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x010A               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagdocumentname"></a>PropertyTagDocumentName

Cadeia de caracteres terminada em nulo que especifica o nome do documento do qual a imagem foi verificada.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x010D                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytagimagedescription"></a>PropertyTagImageDescription

Cadeia de caracteres terminada em nulo que especifica o título da imagem.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x010E                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytagequipmake"></a>PropertyTagEquipMake

Cadeia de caracteres terminada em nulo que especifica o fabricante do equipamento usado para gravar a imagem.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x010F                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytagequipmodel"></a>PropertyTagEquipModel

Cadeia de caracteres terminada em nulo que especifica o nome do modelo ou o número do modelo do equipamento usado para gravar a imagem.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x0110                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytagstripoffsets"></a>PropertyTagStripOffsets

Para cada faixa, o deslocamento de byte dessa faixa. Consulte também [PropertyTagRowsPerStrip](#propertytagrowsperstrip) e [PropertyTagStripBytesCount](#propertytagstripbytescount).



| Informações da propriedade | Valor |
|-------|---------------------------------------------|
| Marca   | 0x0111                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Contagem | Número de faixas                            |



 

## <a name="propertytagorientation"></a>PropertyTagOrientation

Orientação da imagem exibida em termos de linhas e colunas.



Marca

0x0112

Type

PropertyTagTypeShort

Contagem

1

1-a linha 0º está na parte superior da imagem visual e a coluna 0º é a do lado esquerdo do Visual. 2-a linha 0º está na parte superior visual da imagem e a coluna 0º é o lado direito Visual. 3-a linha 0º está na parte inferior Visual da imagem e a coluna 0º é o lado direito Visual. 4-a linha 0º está na parte inferior Visual da imagem e a coluna 0º é o lado esquerdo do Visual. 5-a linha 0º é o lado esquerdo do Visual da imagem e a coluna 0º é a parte superior visual. 6-a linha 0º é o lado direito Visual da imagem e a coluna 0º é a parte superior visual. 7-a linha 0º é o lado direito Visual da imagem e a coluna 0º é a parte inferior Visual. 8-a linha 0º é o lado esquerdo do Visual da imagem e a coluna 0º é a parte inferior Visual.



 

## <a name="propertytagsamplesperpixel"></a>PropertyTagSamplesPerPixel

Número de componentes de cores por pixel.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x0115               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagrowsperstrip"></a>PropertyTagRowsPerStrip

Número de linhas por faixa. Consulte também [PropertyTagStripBytesCount](#propertytagstripbytescount) e [PropertyTagStripOffsets](#propertytagstripoffsets).



| Informações da propriedade | Valor |
|-------|---------------------------------------------|
| Marca   | 0x0116                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Contagem | 1                                           |



 

## <a name="propertytagstripbytescount"></a>PropertyTagStripBytesCount

Para cada faixa, o número total de bytes nessa faixa.



| Informações da propriedade | Valor |
|-------|---------------------------------------------|
| Marca   | 0x0117                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Contagem | Número de faixas                            |



 

## <a name="propertytagminsamplevalue"></a>PropertyTagMinSampleValue

Para cada componente de cor, o valor mínimo atribuído a esse componente. Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informações da propriedade | Valor |
|-------|------------------------------------------|
| Marca   | 0x0118                                   |
| Type  | PropertyTagTypeShort                     |
| Contagem | Número de amostras (componentes) por pixel |



 

## <a name="propertytagmaxsamplevalue"></a>PropertyTagMaxSampleValue

Para cada componente de cor, o valor máximo atribuído a esse componente. Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informações da propriedade | Valor |
|-------|------------------------------------------|
| Marca   | 0x0119                                   |
| Type  | PropertyTagTypeShort                     |
| Contagem | Número de amostras (componentes) por pixel |



 

## <a name="propertytagxresolution"></a>PropertyTagXResolution

Número de pixels por unidade na direção da largura da imagem (x). A unidade é especificada por [PropertyTagResolutionUnit](#propertytagresolutionunit).



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x011A                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytagyresolution"></a>PropertyTagYResolution

Número de pixels por unidade na direção da altura da imagem (y). A unidade é especificada por [PropertyTagResolutionUnit](#propertytagresolutionunit).



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x011B                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytagplanarconfig"></a>PropertyTagPlanarConfig

Se os componentes de pixel são gravados em formato de plana ou de planar.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x011C               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagpagename"></a>PropertyTagPageName

Cadeia de caracteres terminada em nulo que especifica o nome da página da qual a imagem foi verificada.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x011D                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytagxposition"></a>PropertyTagXPosition

Deslocamento do lado esquerdo da página para o lado esquerdo da imagem. A unidade de medida é especificada por [PropertyTagResolutionUnit](#propertytagresolutionunit).



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x011E                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytagyposition"></a>PropertyTagYPosition

Deslocamento da parte superior da página até a parte superior da imagem. A unidade de medida é especificada por [PropertyTagResolutionUnit](#propertytagresolutionunit).



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x011F                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytagfreeoffset"></a>PropertyTagFreeOffset

Para cada cadeia de caracteres de bytes não usados contíguos, o deslocamento de byte dessa cadeia de caracteres.



| Informações da propriedade | Valor |
|------|---------------------|
| Marca  | 0x0120              |
| Type | PropertyTagTypeLong |



 

## <a name="propertytagfreebytecounts"></a>PropertyTagFreeByteCounts

Para cada cadeia de caracteres de bytes não usados contíguos, o número de bytes nessa cadeia de caracteres.



| Informações da propriedade | Valor |
|-------|-----------------------------------------------|
| Marca   | 0x0121                                        |
| Type  | PropertyTagTypeLong                           |
| Contagem | Número de cadeias de caracteres de bytes não utilizados contíguos. |



 

## <a name="propertytaggrayresponseunit"></a>PropertyTagGrayResponseUnit

Precisão do número especificado por PropertyTagGrayResponseCurve. 1 especifica décimos, 2 especifica centésimos, 3 especifica milésimos de milhares e assim por diante.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x0122               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytaggrayresponsecurve"></a>PropertyTagGrayResponseCurve

Para cada valor de pixel possível em uma imagem em tons de cinza, a densidade óptica desse valor de pixel.



| Informações da propriedade | Valor |
|-------|---------------------------------|
| Marca   | 0x0123                          |
| Type  | PropertyTagTypeShort            |
| Contagem | Número de valores de pixel possíveis |



 

## <a name="propertytagt4option"></a>PropertyTagT4Option

Conjunto de sinalizadores relacionados à codificação T4.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x0124              |
| Type  | PropertyTagTypeLong |
| Contagem | 1                   |



 

## <a name="propertytagt6option"></a>PropertyTagT6Option

Conjunto de sinalizadores relacionados à codificação T6.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x0125              |
| Type  | PropertyTagTypeLong |
| Contagem | 1                   |



 

## <a name="propertytagresolutionunit"></a>PropertyTagResolutionUnit

Unidade de medida para a resolução horizontal e a resolução vertical.



Marca

0x0128

Type

PropertyTagTypeShort

Contagem

1

2 polegadas e 3 centímetros



 

## <a name="propertytagpagenumber"></a>PropertyTagPageNumber

Número de página da página da qual a imagem foi verificada.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x0129               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagtransferfunction"></a>PropertyTagTransferFunction

Tabelas que especificam funções de transferência para a imagem.



| Informações da propriedade | Valor |
|-------|------------------------------------------------------|
| Marca   | 0x012D                                               |
| Type  | PropertyTagTypeShort                                 |
| Contagem | Número total de palavras de 16 bits necessárias para as tabelas |



 

## <a name="propertytagsoftwareused"></a>PropertyTagSoftwareUsed

Cadeia de caracteres terminada em nulo que especifica o nome e a versão do software ou firmware do dispositivo usado para gerar a imagem.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x0131                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytagdatetime"></a>PropertyTagDateTime

Data e hora em que a imagem foi criada.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x0132               |
| Type  | PropertyTagTypeASCII |
| Contagem | 20                   |



 

## <a name="propertytagartist"></a>PropertyTagArtist

Cadeia de caracteres terminada em nulo que especifica o nome da pessoa que criou a imagem.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x013B                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytaghostcomputer"></a>PropertyTagHostComputer

Cadeia de caracteres terminada em nulo que especifica o computador e/ou sistema operacional usado para criar a imagem.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x013C                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytagpredictor"></a>PropertyTagPredictor

Tipo de esquema de previsão que foi aplicado aos dados da imagem antes da aplicação do esquema de codificação.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x013D               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagwhitepoint"></a>PropertyTagWhitePoint

A desvio do ponto branco da imagem.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x013E                  |
| Type  | PropertyTagTypeRational |
| Contagem | 2                       |



 

## <a name="propertytagprimarychromaticities"></a>PropertyTagPrimaryChromaticities

Para cada uma das três cores primárias na imagem, a desvio dessa cor.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x013F                  |
| Type  | PropertyTagTypeRational |
| Contagem | 6                       |



 

## <a name="propertytagcolormap"></a>PropertyTagColorMap

Paleta de cores (tabela de pesquisa) para uma imagem indexada por paleta.



| Informações da propriedade | Valor |
|-------|-------------------------------------------------|
| Marca   | 0x0140                                          |
| Type  | PropertyTagTypeShort                            |
| Contagem | Número de palavras de 16 bits necessárias para a paleta |



 

## <a name="propertytaghalftonehints"></a>PropertyTagHalftoneHints

Informações usadas pela função de meio-tom



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x0141               |
| Type  | PropertyTagTypeShort |
| Contagem | 2                    |



 

## <a name="propertytagtilewidth"></a>PropertyTagTileWidth

Número de colunas de pixel em cada bloco.



| Informações da propriedade | Valor |
|-------|---------------------------------------------|
| Marca   | 0x0142                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Contagem | 1                                           |



 

## <a name="propertytagtilelength"></a>PropertyTagTileLength

Número de linhas de pixel em cada bloco.



| Informações da propriedade | Valor |
|-------|---------------------------------------------|
| Marca   | 0x0143                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Contagem | 1                                           |



 

## <a name="propertytagtileoffset"></a>PropertyTagTileOffset

Para cada bloco, o deslocamento de byte desse bloco.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x0144              |
| Type  | PropertyTagTypeLong |
| Contagem | Número de blocos     |



 

## <a name="propertytagtilebytecounts"></a>PropertyTagTileByteCounts

Para cada bloco, o número de bytes nesse bloco.



| Informações da propriedade | Valor |
|-------|---------------------------------------------|
| Marca   | 0x0145                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Contagem | Número de blocos                             |



 

## <a name="propertytaginkset"></a>PropertyTagInkSet

Conjunto de tintas usadas em uma imagem separada.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x014C               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytaginknames"></a>PropertyTagInkNames

Sequência de cadeias de caracteres concatenadas, terminadas em nulo, que especificam os nomes das tintas usadas em uma imagem separada.



| Informações da propriedade | Valor |
|-------|------------------------------------------------------------------------|
| Marca   | 0x014D                                                                 |
| Type  | PropertyTagTypeASCII                                                   |
| Contagem | Comprimento total da sequência de cadeias de caracteres, incluindo os terminadores nulos |



 

## <a name="propertytagnumberofinks"></a>PropertyTagNumberOfInks

Número de tintas.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x014E               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagdotrange"></a>PropertyTagDotRange

Valores de componente de cor que correspondem a um ponto de 0% e um ponto de 100 por cento.



| Informações da propriedade | Valor |
|-------|---------------------------------------------|
| Marca   | 0x0150                                      |
| Type  | PropertyTagTypeByte ou PropertyTagTypeShort |
| Contagem | 2 ou 2 × PropertyTagSamplesPerPixel           |



 

## <a name="propertytagtargetprinter"></a>PropertyTagTargetPrinter

Cadeia de caracteres terminada em nulo que descreve o ambiente de impressão pretendido.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x0151                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytagextrasamples"></a>PropertyTagExtraSamples

Número de componentes de cores extras. Por exemplo, um componente extra pode conter um valor alfa.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x0152               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagsampleformat"></a>PropertyTagSampleFormat

Para cada componente de cor, o formato numérico (sem sinal, assinado, ponto flutuante) desse componente. Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informações da propriedade | Valor |
|-------|------------------------------------------|
| Marca   | 0x0153                                   |
| Type  | PropertyTagTypeShort                     |
| Contagem | Número de amostras (componentes) por pixel |



 

## <a name="propertytagsminsamplevalue"></a>PropertyTagSMinSampleValue

Para cada componente de cor, o valor mínimo desse componente. Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informações da propriedade | Valor |
|-------|-----------------------------------------------------|
| Marca   | 0x0154                                              |
| Type  | O tipo que melhor corresponde aos dados do componente de pixel |
| Contagem | Número de amostras (componentes) por pixel            |



 

## <a name="propertytagsmaxsamplevalue"></a>PropertyTagSMaxSampleValue

Para cada componente de cor, o valor máximo desse componente. Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informações da propriedade | Valor |
|-------|-----------------------------------------------------|
| Marca   | 0x0155                                              |
| Type  | O tipo que melhor corresponde aos dados do componente de pixel |
| Contagem | Número de amostras (componentes) por pixel            |



 

## <a name="propertytagtransferrange"></a>PropertyTagTransferRange

Tabela de valores que estende o intervalo da função de transferência.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x0156               |
| Type  | PropertyTagTypeShort |
| Contagem | 6                    |



 

## <a name="propertytagjpegproc"></a>PropertyTagJPEGProc

Processo de compactação JPEG.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x0200               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagjpeginterformat"></a>PropertyTagJPEGInterFormat

Offset para o início de um fragmentado de JPEG.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x0201              |
| Type  | PropertyTagTypeLong |
| Contagem | 1                   |



 

## <a name="propertytagjpeginterlength"></a>PropertyTagJPEGInterLength

Comprimento, em bytes, do JPEG fragmentado.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x0202              |
| Type  | PropertyTagTypeLong |
| Contagem | 1                   |



 

## <a name="propertytagjpegrestartinterval"></a>PropertyTagJPEGRestartInterval

Comprimento do intervalo de reinicialização.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x0203               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagjpeglosslesspredictors"></a>PropertyTagJPEGLosslessPredictors

Para cada componente de cor, um valor de seleção de pregnóstico sem perdas para esse componente. Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informações da propriedade | Valor |
|-------|------------------------------------------|
| Marca   | 0x0205                                   |
| Type  | PropertyTagTypeShort                     |
| Contagem | Número de amostras (componentes) por pixel |



 

## <a name="propertytagjpegpointtransforms"></a>PropertyTagJPEGPointTransforms

Para cada componente de cor, um valor de transformação de ponto para esse componente. Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informações da propriedade | Valor |
|-------|------------------------------------------|
| Marca   | 0x0206                                   |
| Type  | PropertyTagTypeShort                     |
| Contagem | Número de amostras (componentes) por pixel |



 

## <a name="propertytagjpegqtables"></a>PropertyTagJPEGQTables

Para cada componente de cor, o deslocamento para a tabela de quantificação para esse componente. Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informações da propriedade | Valor |
|-------|------------------------------------------|
| Marca   | 0x0207                                   |
| Type  | PropertyTagTypeLong                      |
| Contagem | Número de amostras (componentes) por pixel |



 

## <a name="propertytagjpegdctables"></a>PropertyTagJPEGDCTables

Para cada componente de cor, o deslocamento para a tabela de Huffman de DC (ou tabela de Huffman sem perdas) para esse componente. Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informações da propriedade | Valor |
|-------|------------------------------------------|
| Marca   | 0x0208                                   |
| Type  | PropertyTagTypeLong                      |
| Contagem | Número de amostras (componentes) por pixel |



 

## <a name="propertytagjpegactables"></a>PropertyTagJPEGACTables

Para cada componente de cor, o deslocamento para a tabela de Huffman de AC para esse componente. Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).



| Informações da propriedade | Valor |
|-------|------------------------------------------|
| Marca   | 0x0209                                   |
| Type  | PropertyTagTypeLong                      |
| Contagem | Número de amostras (componentes) por pixel |



 

## <a name="propertytagycbcrcoefficients"></a>PropertyTagYCbCrCoefficients

Coeficientes para transformação de RGB para dados de imagem YCbCr.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x0211                  |
| Type  | PropertyTagTypeRational |
| Contagem | 3                       |



 

## <a name="propertytagycbcrsubsampling"></a>PropertyTagYCbCrSubsampling

Taxa de amostragem de componentes crominância em relação ao componente de luminância.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x0212               |
| Type  | PropertyTagTypeShort |
| Contagem | 2                    |



 

## <a name="propertytagycbcrpositioning"></a>PropertyTagYCbCrPositioning

Posição dos componentes do crominância em relação ao componente de luminância.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x0213               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagrefblackwhite"></a>PropertyTagREFBlackWhite

Valor de ponto preto de referência e valor de ponto branco de referência.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x0214                  |
| Type  | PropertyTagTypeRational |
| Contagem | 6                       |



 

## <a name="propertytaggamma"></a>PropertyTagGamma

Valor de gama anexado à imagem. O valor de gama é armazenado como um número racional (par de **longo**) com um numerador de 100000. Por exemplo, um valor de gama de 2,2 é armazenado como o par (100000, 45455).



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x0301                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytagiccprofiledescriptor"></a>PropertyTagICCProfileDescriptor

Cadeia de caracteres terminada em nulo que identifica um perfil ICC.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x0302                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytagsrgbrenderingintent"></a>PropertyTagSRGBRenderingIntent

Como a imagem deve ser exibida conforme definido pelo consórcio de cor internacional (ICC). Se um objeto de  [**imagem**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) GDI+ for construído com o parâmetro *UseEmbeddedColorManagement* definido como **true**, o GDI+ renderizará a imagem de acordo com a tentativa de renderização especificada. A intenção pode ser definida como perceptiva, colorimétrico relativo, saturação ou colorimétrico absoluto.

-   A intenção perceptiva, que é adequada para fotografias, oferece boa adaptação à gama do dispositivo de vídeo às custas da precisão colorimétrico.
-   A intenção colorimétrico relativa é adequada para imagens (por exemplo, logotipos) que exigem correspondência de aparência de cor em relação ao ponto branco do dispositivo de vídeo.
-   A intenção de saturação, que é adequada para gráficos e grafos, preserva a saturação às custas de matiz e claridade.
-   A intenção colorimétrico absoluta é adequada para provas (visualizações de imagens destinadas a um dispositivo de vídeo diferente) que exigem a preservação do colorimetry absoluto.



Marca

0x0303

Type

BYTE

Contagem

1

0-perceptiva 1-colorimétrico relativo 2-saturação 3-colorimétrico absoluto



 

## <a name="propertytagimagetitle"></a>PropertyTagImageTitle

Cadeia de caracteres terminada em nulo que especifica o título da imagem.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x0320                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytagresolutionxunit"></a>PropertyTagResolutionXUnit

Unidades nas quais exibir a resolução horizontal.



Marca

0x5001

Type

PropertyTagTypeShort

Contagem

1

1-pixels por polegada 2-pixels por centímetro



 

## <a name="propertytagresolutionyunit"></a>PropertyTagResolutionYUnit

Unidades nas quais exibir a resolução vertical.



Marca

0x5002

Type

PropertyTagTypeShort

Contagem

1

1-pixels por polegada 2-pixels por centímetro



 

## <a name="propertytagresolutionxlengthunit"></a>PropertyTagResolutionXLengthUnit

Unidades nas quais exibir a largura da imagem.



Marca

0x5003

Type

PropertyTagTypeShort

Contagem

1

1-polegadas 2-centímetros 3-pontos 4-paicas 5-colunas



 

## <a name="propertytagresolutionylengthunit"></a>PropertyTagResolutionYLengthUnit

Unidades nas quais exibir a altura da imagem.



Marca

0x5004

Type

PropertyTagTypeShort

Contagem

1

1-polegadas 2-centímetros 3-pontos 4-paicas 5-colunas



 

## <a name="propertytagprintflags"></a>PropertyTagPrintFlags

Sequência de valores Boolianos de um byte que especificam opções de impressão.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x5005               |
| Type  | PropertyTagTypeASCII |
| Contagem | Número de sinalizadores      |



 

## <a name="propertytagprintflagsversion"></a>PropertyTagPrintFlagsVersion

Versão de sinalizadores de impressão.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x5006               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagprintflagscrop"></a>PropertyTagPrintFlagsCrop

Imprimir marcas de corte do centro de sinalizadores.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x5007              |
| Type  | PropertyTagTypeByte |
| Contagem | 1                   |



 

## <a name="propertytagprintflagsbleedwidth"></a>PropertyTagPrintFlagsBleedWidth

Largura de sangria de sinalizadores de impressão.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x5008              |
| Type  | PropertyTagTypeLong |
| Contagem | 1                   |



 

## <a name="propertytagprintflagsbleedwidthscale"></a>PropertyTagPrintFlagsBleedWidthScale

Escala da largura de sangria de sinalizadores de impressão.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x5009               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytaghalftonelpi"></a>PropertyTagHalftoneLPI

Frequência de tela da tinta, em linhas por polegada.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x500A                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytaghalftonelpiunit"></a>PropertyTagHalftoneLPIUnit

Unidades para a frequência da tela.



Marca

0x500B

Type

PropertyTagTypeShort

Contagem

1

1-linhas por polegada 2-linhas por centímetro



 

## <a name="propertytaghalftonedegree"></a>PropertyTagHalftoneDegree

Ângulo da tela.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x500C                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytaghalftoneshape"></a>PropertyTagHalftoneShape

Forma dos pontos de retícula.



Marca

0x500D

Type

PropertyTagTypeShort

Contagem

1

0-redondo 1-elipse 2-linha 3-quadrado 4-Cruz 6-losango



 

## <a name="propertytaghalftonemisc"></a>PropertyTagHalftoneMisc

Várias informações de meio-tom.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x500E              |
| Type  | PropertyTagTypeLong |
| Contagem | 1                   |



 

## <a name="propertytaghalftonescreen"></a>PropertyTagHalftoneScreen

Valor booliano que especifica se as telas padrão da impressora devem ser usadas.



Marca

0x500F

Type

PropertyTagTypeByte

Contagem

1

1-usar as telas padrão 2-outras da impressora



 

## <a name="propertytagjpegquality"></a>PropertyTagJPEGQuality

Marca particular usada pelo formato Adobe Photoshop. Não destinado ao uso público.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x5010               |
| Type  | PropertyTagTypeShort |
| Contagem | Qualquer                  |



 

## <a name="propertytaggridsize"></a>PropertyTagGridSize

Bloco de informações sobre grades e guias.



| Informações da propriedade | Valor |
|-------|--------------------------|
| Marca   | 0x5011                   |
| Type  | PropertyTagTypeUndefined |
| Contagem | Qualquer                      |



 

## <a name="propertytagthumbnailformat"></a>PropertyTagThumbnailFormat

Formato da imagem em miniatura.



Marca

0x5012

Type

PropertyTagTypeLong

Contagem

1

0-RGB bruto 1-JPEG



 

## <a name="propertytagthumbnailwidth"></a>PropertyTagThumbnailWidth

Largura, em pixels, da imagem em miniatura.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x5013              |
| Type  | PropertyTagTypeLong |
| Contagem | 1                   |



 

## <a name="propertytagthumbnailheight"></a>PropertyTagThumbnailHeight

Altura, em pixels, da imagem em miniatura.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x5014              |
| Type  | PropertyTagTypeLong |
| Contagem | 1                   |



 

## <a name="propertytagthumbnailcolordepth"></a>PropertyTagThumbnailColorDepth

bits por pixel (BPP) para a imagem em miniatura.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x5015               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagthumbnailplanes"></a>PropertyTagThumbnailPlanes

Número de planos de cores para a imagem em miniatura.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x5016               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagthumbnailrawbytes"></a>PropertyTagThumbnailRawBytes

Deslocamento de bytes entre linhas de dados de pixel.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x5017              |
| Type  | PropertyTagTypeLong |
| Contagem | 1                   |



 

## <a name="propertytagthumbnailsize"></a>PropertyTagThumbnailSize

Tamanho total, em bytes, da imagem em miniatura.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x5018              |
| Type  | PropertyTagTypeLong |
| Contagem | 1                   |



 

## <a name="propertytagthumbnailcompressedsize"></a>PropertyTagThumbnailCompressedSize

Tamanho compactado, em bytes, da imagem em miniatura.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x5019              |
| Type  | PropertyTagTypeLong |
| Contagem | 1                   |



 

## <a name="propertytagcolortransferfunction"></a>PropertyTagColorTransferFunction

Tabela de valores que especificam funções de transferência de cor.



| Informações da propriedade | Valor |
|-------|--------------------------|
| Marca   | 0x501A                   |
| Type  | PropertyTagTypeUndefined |
| Contagem | Qualquer                      |



 

## <a name="propertytagthumbnaildata"></a>PropertyTagThumbnailData

Bits de miniatura bruta no formato JPEG ou RGB. Depende de PropertyTagThumbnailFormat.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x501B              |
| Type  | PropertyTagTypeByte |
| Contagem | Variável            |



 

## <a name="propertytagthumbnailimagewidth"></a>PropertyTagThumbnailImageWidth

Número de pixels por linha na imagem em miniatura.



| Informações da propriedade | Valor |
|-------|---------------------------------------------|
| Marca   | 0x5020                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Contagem | 1                                           |



 

## <a name="propertytagthumbnailimageheight"></a>PropertyTagThumbnailImageHeight

Número de linhas de pixel na imagem em miniatura.



| Informações da propriedade | Valor |
|-------|---------------------------------------------|
| Marca   | 0x5021                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Contagem | 1                                           |



 

## <a name="propertytagthumbnailbitspersample"></a>PropertyTagThumbnailBitsPerSample

Número de bits por componente de cor na imagem em miniatura. Consulte também [PropertyTagThumbnailSamplesPerPixel](#propertytagthumbnailsamplesperpixel).



| Informações da propriedade | Valor |
|-------|-----------------------------------------------------------------|
| Marca   | 0x5022                                                          |
| Type  | PropertyTagTypeShort                                            |
| Contagem | Número de amostras (componentes) por pixel na imagem em miniatura |



 

## <a name="propertytagthumbnailcompression"></a>PropertyTagThumbnailCompression

Esquema de compactação usado para dados de imagem em miniatura.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x5023               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagthumbnailphotometricinterp"></a>PropertyTagThumbnailPhotometricInterp

Como os dados de pixel de miniatura serão interpretados.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x5024               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagthumbnailimagedescription"></a>PropertyTagThumbnailImageDescription

Cadeia de caracteres terminada em nulo que especifica o título da imagem.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x5025                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytagthumbnailequipmake"></a>PropertyTagThumbnailEquipMake

Cadeia de caracteres terminada em nulo que especifica o fabricante do equipamento usado para gravar a imagem em miniatura.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x5026                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytagthumbnailequipmodel"></a>PropertyTagThumbnailEquipModel

Cadeia de caracteres terminada em nulo que especifica o nome do modelo ou o número do modelo do equipamento usado para gravar a imagem em miniatura.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x5027                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytagthumbnailstripoffsets"></a>PropertyTagThumbnailStripOffsets

Para cada faixa na imagem em miniatura, o deslocamento de bytes dessa faixa. Consulte também [PropertyTagThumbnailRowsPerStrip](#propertytagthumbnailrowsperstrip) e [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount).



| Informações da propriedade | Valor |
|-------|---------------------------------------------|
| Marca   | 0x5028                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Contagem | Número de faixas                            |



 

## <a name="propertytagthumbnailorientation"></a>PropertyTagThumbnailOrientation

Orientação da imagem em miniatura em termos de linhas e colunas. Consulte também [PropertyTagOrientation](#propertytagorientation).



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x5029               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagthumbnailsamplesperpixel"></a>PropertyTagThumbnailSamplesPerPixel

Número de componentes de cor por pixel na imagem em miniatura.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x502A               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagthumbnailrowsperstrip"></a>PropertyTagThumbnailRowsPerStrip

Número de linhas por faixa na imagem em miniatura. Consulte também [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount) e [PropertyTagThumbnailStripOffsets](#propertytagthumbnailstripoffsets).



| Informações da propriedade | Valor |
|-------|---------------------------------------------|
| Marca   | 0x502B                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Contagem | 1                                           |



 

## <a name="propertytagthumbnailstripbytescount"></a>PropertyTagThumbnailStripBytesCount

Para cada faixa de imagem em miniatura, o número total de bytes nessa faixa.



| Informações da propriedade | Valor |
|-------|---------------------------------------------|
| Marca   | 0x502C                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Contagem | Número de faixas na imagem em miniatura     |



 

## <a name="propertytagthumbnailresolutionx"></a>PropertyTagThumbnailResolutionX

Resolução de miniaturas na direção da largura. A unidade de resolução é fornecida em [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).



| Informações da propriedade | Valor |
|-----|--------|
| Marca | 0x502D |



 

## <a name="propertytagthumbnailresolutiony"></a>PropertyTagThumbnailResolutionY

Resolução de miniaturas na direção da altura. A unidade de resolução é fornecida em [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).



| Informações da propriedade | Valor |
|-----|--------|
| Marca | 0x502E |



 

## <a name="propertytagthumbnailplanarconfig"></a>PropertyTagThumbnailPlanarConfig

Se os componentes de pixel na imagem em miniatura são registrados no formato de partes ou do planar. Consulte também [PropertyTagPlanarConfig](#propertytagplanarconfig).



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x502F               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagthumbnailresolutionunit"></a>PropertyTagThumbnailResolutionUnit

Unidade de medida para a resolução horizontal e a resolução vertical da imagem em miniatura. Consulte também [PropertyTagResolutionUnit](#propertytagresolutionunit).



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x5030               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagthumbnailtransferfunction"></a>PropertyTagThumbnailTransferFunction

Tabelas que especificam funções de transferência para a imagem em miniatura. Consulte também [PropertyTagTransferFunction](#propertytagtransferfunction).



| Informações da propriedade | Valor |
|-------|------------------------------------------------------|
| Marca   | 0x5031                                               |
| Type  | PropertyTagTypeShort                                 |
| Contagem | Número total de palavras de 16 bits necessárias para as tabelas |



 

## <a name="propertytagthumbnailsoftwareused"></a>PropertyTagThumbnailSoftwareUsed

Cadeia de caracteres terminada em nulo que especifica o nome e a versão do software ou firmware do dispositivo usado para gerar a imagem em miniatura.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x5032                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytagthumbnaildatetime"></a>PropertyTagThumbnailDateTime

Data e hora em que a imagem em miniatura foi criada. Consulte também [PropertyTagDateTime](#propertytagdatetime).



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x5033               |
| Type  | PropertyTagTypeASCII |
| Contagem | 20                   |



 

## <a name="propertytagthumbnailartist"></a>PropertyTagThumbnailArtist

Cadeia de caracteres terminada em nulo que especifica o nome da pessoa que criou a imagem em miniatura.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x5034                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytagthumbnailwhitepoint"></a>PropertyTagThumbnailWhitePoint

A desvio do ponto branco da imagem em miniatura. Consulte também [PropertyTagWhitePoint](#propertytagwhitepoint).



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x5035                  |
| Type  | PropertyTagTypeRational |
| Contagem | 2                       |



 

## <a name="propertytagthumbnailprimarychromaticities"></a>PropertyTagThumbnailPrimaryChromaticities

Para cada uma das três cores primárias na imagem em miniatura, a desvio dessa cor. Consulte também [PropertyTagPrimaryChromaticities](#propertytagprimarychromaticities).



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x5036                  |
| Type  | PropertyTagTypeRational |
| Contagem | 6                       |



 

## <a name="propertytagthumbnailycbcrcoefficients"></a>PropertyTagThumbnailYCbCrCoefficients

Coeficientes para transformação de RGB para dados YCbCr para a imagem em miniatura. Consulte também [PropertyTagYCbCrCoefficients](#propertytagycbcrcoefficients).



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x5037                  |
| Type  | PropertyTagTypeRational |
| Contagem | 3                       |



 

## <a name="propertytagthumbnailycbcrsubsampling"></a>PropertyTagThumbnailYCbCrSubsampling

Taxa de amostragem de componentes crominância em relação ao componente de luminância para a imagem em miniatura. Consulte também [PropertyTagYCbCrSubsampling](#propertytagycbcrsubsampling).



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x5038               |
| Type  | PropertyTagTypeShort |
| Contagem | 2                    |



 

## <a name="propertytagthumbnailycbcrpositioning"></a>PropertyTagThumbnailYCbCrPositioning

Posição dos componentes crominância em relação ao componente de luminância para a imagem em miniatura. Consulte também [PropertyTagYCbCrPositioning](#propertytagycbcrpositioning).



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x5039               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagthumbnailrefblackwhite"></a>PropertyTagThumbnailRefBlackWhite

Valor de ponto preto de referência e valor de ponto branco de referência para a imagem em miniatura. Consulte também [PropertyTagREFBlackWhite](#propertytagrefblackwhite).



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x503A                  |
| Type  | PropertyTagTypeRational |
| Contagem | 6                       |



 

## <a name="propertytagthumbnailcopyright"></a>PropertyTagThumbnailCopyRight

Cadeia de caracteres terminada em nulo que contém informações de direitos autorais da imagem em miniatura.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x503B                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytagluminancetable"></a>PropertyTagLuminanceTable

Tabela de luminância. A tabela de luminescência e a tabela crominância são usadas para controlar a qualidade JPEG. Uma tabela de luminância ou crominância válida tem 64 entradas do tipo PropertyTagTypeShort. Se uma imagem tiver uma tabela de luminância ou uma tabela crominância, ela deverá ter ambas as tabelas.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x5090               |
| Type  | PropertyTagTypeShort |
| Contagem | 64                   |



 

## <a name="propertytagchrominancetable"></a>PropertyTagChrominanceTable

Tabela crominância. A tabela de luminescência e a tabela crominância são usadas para controlar a qualidade JPEG. Uma tabela de luminância ou crominância válida tem 64 entradas do tipo PropertyTagTypeShort. Se uma imagem tiver uma tabela de luminância ou uma tabela crominância, ela deverá ter ambas as tabelas.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x5091               |
| Type  | PropertyTagTypeShort |
| Contagem | 64                   |



 

## <a name="propertytagframedelay"></a>PropertyTagFrameDelay

Tempo de atraso, em centésimos de um segundo, entre dois quadros em uma imagem GIF animada.



| Informações da propriedade | Valor |
|-------|-------------------------------|
| Marca   | 0x5100                        |
| Type  | PropertyTagTypeLong           |
| Contagem | Número de quadros na imagem |



 

## <a name="propertytagloopcount"></a>PropertyTagLoopCount

Para uma imagem GIF animada, o número de vezes para exibir a animação. Um valor de 0 especifica que a animação deve ser exibida infinitamente.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x5101               |
| Type  | PropertyTagTypeShort |
| Contagem | 1                    |



 

## <a name="propertytagglobalpalette"></a>PropertyTagGlobalPalette

Paleta de cores para um bitmap indexado em uma imagem GIF.



| Informações da propriedade | Valor |
|-------|-------------------------------|
| Marca   | 0x5102                        |
| Type  | PropertyTagTypeByte           |
| Contagem | 3 x número de entradas da paleta |



 

## <a name="propertytagindexbackground"></a>PropertyTagIndexBackground

Índice da cor do plano de fundo na paleta de uma imagem GIF.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x5103              |
| Type  | PropertyTagTypeByte |
| Contagem | 1                   |



 

## <a name="propertytagindextransparent"></a>PropertyTagIndexTransparent

Índice da cor transparente na paleta de uma imagem GIF.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x5104              |
| Type  | PropertyTagTypeByte |
| Contagem | 1                   |



 

## <a name="propertytagpixelunit"></a>PropertyTagPixelUnit

Unidade para PropertyTagPixelPerUnitX e PropertyTagPixelPerUnitY.



Marca

0x5110

Type

PropertyTagTypeByte

Contagem

1

0-desconhecido



 

## <a name="propertytagpixelperunitx"></a>PropertyTagPixelPerUnitX

Pixels por unidade na direção x.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x5111              |
| Type  | PropertyTagTypeLong |
| Contagem | 1                   |



 

## <a name="propertytagpixelperunity"></a>PropertyTagPixelPerUnitY

Pixels por unidade na direção y.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x5112              |
| Type  | PropertyTagTypeLong |
| Contagem | 1                   |



 

## <a name="propertytagpalettehistogram"></a>PropertyTagPaletteHistogram

Histograma da paleta.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x5113                  |
| Type  | PropertyTagTypeByte     |
| Contagem | Comprimento do histograma |



 

## <a name="propertytagcopyright"></a>PropertyTagCopyright

Cadeia de caracteres terminada em nulo que contém informações de direitos autorais.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x8298                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytagexifexposuretime"></a>PropertyTagExifExposureTime

Tempo de exposição, medido em segundos.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x829A                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytagexiffnumber"></a>PropertyTagExifFNumber

Número F.



| Informações da propriedade | Valor |
|-------|----------|
| Marca   | 0x829D   |
| Type  | RACIONAL |
| Contagem | 1        |



 

## <a name="propertytagexififd"></a>PropertyTagExifIFD

Marca particular usada pelo GDI+. Não destinado ao uso público. O GDI+ usa essa marca para localizar informações específicas de EXIF.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x8769              |
| Type  | PropertyTagTypeLong |
| Contagem | 1                   |



 

## <a name="propertytagiccprofile"></a>PropertyTagICCProfile

Perfil ICC inserido na imagem.



| Informações da propriedade | Valor |
|-------|-----------------------|
| Marca   | 0x8773                |
| Type  | PropertyTagTypeByte   |
| Contagem | Comprimento do perfil |



 

## <a name="propertytagexifexposureprog"></a>PropertyTagExifExposureProg

Classe do programa usada pela câmera para definir a exposição quando a imagem é executada.



Marca

0x8822

Type

BAIXO

Contagem

1

Padrão

0

0-não definido 1-Manual 2-programa normal 3-prioridade de abertura 4-prioridade 5 do obturador – programa criativo (em relação à profundidade do campo) 6-programa de ação (polarizado em direção à rapidez velocidade do obturador) 7-modo retrato (para fotos de fechamento com o plano de fundo fora do foco) modo 8-paisagem (para fotos em paisagem com o plano de fundo em foco) de 9 a 255-reservado



 

## <a name="propertytagexifspectralsense"></a>PropertyTagExifSpectralSense

Cadeia de caracteres terminada em nulo que especifica a sensibilidade de Spectral de cada canal da câmera usada. A cadeia de caracteres é compatível com o padrão desenvolvido pelo comitê técnico do ASTM.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x8824                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytaggpsifd"></a>PropertyTagGpsIFD

Deslocamento para um bloco de itens de propriedade GPS. Itens de propriedade cujas marcas têm o prefixo PropertyTagGps são armazenadas no bloco GPS. Os itens de propriedade GPS são definidos na especificação EXIF. O GDI+ usa essa marca para localizar informações de GPS, mas GDI+ não expõe essa marca para uso público.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0x8825              |
| Type  | PropertyTagTypeLong |
| Contagem | 1                   |



 

## <a name="propertytagexifisospeed"></a>PropertyTagExifISOSpeed

Velocidade ISO e latitude ISO da câmera ou dispositivo de entrada, conforme especificado no ISO 12232.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x8827               |
| Type  | PropertyTagTypeShort |
| Contagem | Qualquer                  |



 

## <a name="propertytagexifoecf"></a>PropertyTagExifOECF

Função de conversão Optoelectronic (OECF) especificada no ISO 14524. O OECF é a relação entre a entrada óptica da câmera e os valores da imagem.



| Informações da propriedade | Valor |
|-------|--------------------------|
| Marca   | 0x8828                   |
| Type  | PropertyTagTypeUndefined |
| Contagem | Qualquer                      |



 

## <a name="propertytagexifver"></a>PropertyTagExifVer

Versão do padrão de EXIF com suporte. A não existência deste campo é usada para significar não conformidade com o padrão. A conformidade com o padrão é indicada pela gravação de 0210 como uma cadeia de caracteres ASCII de 4 bytes. Como o tipo é PropertyTagTypeUndefined, não há nenhum terminador nulo.



| Informações da propriedade | Valor |
|---------|--------------------------|
| Marca     | 0x9000                   |
| Type    | PropertyTagTypeUndefined |
| Contagem   | 4                        |
| Padrão | 0210                     |



 

## <a name="propertytagexifdtorig"></a>PropertyTagExifDTOrig

Data e hora em que os dados da imagem original foram gerados. Para uma DSC, a data e a hora em que a imagem foi tirada. O formato é aaaa: MM: DD HH: MM: SS com o tempo mostrado no formato de 24 horas e a data e hora separadas por um caractere em branco (0x2000). O comprimento da cadeia de caracteres é de 20 bytes, incluindo o terminador nulo. Quando o campo está vazio, ele é tratado como desconhecido.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x9003               |
| Type  | PropertyTagTypeASCII |
| Contagem | 20                   |



 

## <a name="propertytagexifdtdigitized"></a>PropertyTagExifDTDigitized

Data e hora em que a imagem foi armazenada como dados digitais. Se, por exemplo, uma imagem foi capturada pela DSC e, ao mesmo tempo em que o arquivo foi gravado, DateTimeOriginal e DateTimeDigitized terão o mesmo conteúdo.

O formato é aaaa: MM: DD HH: MM: SS com o tempo mostrado no formato de 24 horas e a data e hora separadas por um caractere em branco (0x2000). O comprimento da cadeia de caracteres é de 20 bytes, incluindo o terminador nulo. Quando o campo está vazio, ele é tratado como desconhecido.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0x9004               |
| Type  | PropertyTagTypeASCII |
| Contagem | 20                   |



 

## <a name="propertytagexifcompconfig"></a>PropertyTagExifCompConfig

Informações específicas para dados compactados. Os canais de cada componente são organizados em ordem do primeiro componente até o quarto. Para dados descompactados, a disposição dos dados é fornecida na marca PropertyTagPhotometricInterp.

No entanto, como PropertyTagPhotometricInterp só pode expressar a ordem de Y, CB e CR, essa marca é fornecida para casos em que os dados compactados usam componentes diferentes de Y, CB e CR e para dar suporte a outras sequências.



Marca

0x9101

Type

PropertyTagTypeUndefined

Contagem

4

Padrão

4 5 6 0 (se RGB descompactado) 1 2 3 0 (outros casos)

0-não existe 1-Y 2-CB 3-CR 4-R 5-G 6-B Other-reserved



 

## <a name="propertytagexifcompbpp"></a>PropertyTagExifCompBPP

Informações específicas para dados compactados. O modo de compactação usado para uma imagem compactada é indicado na unidade BPP.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x9102                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytagexifshutterspeed"></a>PropertyTagExifShutterSpeed

Velocidade do obturador. A unidade é o sistema aditivo de valor de exposição fotográfica (APEX).



| Informações da propriedade | Valor |
|-------|--------------------------|
| Marca   | 0x9201                   |
| Type  | PropertyTagTypeSRational |
| Contagem | 1                        |



 

## <a name="propertytagexifaperture"></a>PropertyTagExifAperture

Abertura de lentes. A unidade é o valor de APEX.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x9202                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytagexifbrightness"></a>PropertyTagExifBrightness

Valor de brilho. A unidade é o valor de APEX. Normalmente, ele é fornecido no intervalo de-99,99 a 99,99.



| Informações da propriedade | Valor |
|-------|--------------------------|
| Marca   | 0x9203                   |
| Type  | PropertyTagTypeSRational |
| Contagem | 1                        |



 

## <a name="propertytagexifexposurebias"></a>PropertyTagExifExposureBias

Tendência de exposição. A unidade é o valor de APEX. Normalmente, ele é fornecido no intervalo de-99,99 a 99,99.



| Informações da propriedade | Valor |
|-------|--------------------------|
| Marca   | 0x9204                   |
| Type  | PropertyTagTypeSRational |
| Contagem | 1                        |



 

## <a name="propertytagexifmaxaperture"></a>PropertyTagExifMaxAperture

Menor número F da lente. A unidade é o valor de APEX. Normalmente, ele é fornecido no intervalo de 0, 0 a 99,99, mas não está limitado a esse intervalo.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x9205                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytagexifsubjectdist"></a>PropertyTagExifSubjectDist

Distância para o assunto, medida em metros.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x9206                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytagexifmeteringmode"></a>PropertyTagExifMeteringMode

Modo de medição.



Marca

0x9207

Type

PropertyTagTypeShort

Contagem

1

Padrão

0

0-desconhecido 1-média 2-CenterWeightedAverage 3-Spot 4-AutoSpot 5-padrão 6-parcial 7 a 254-reservado 255-outro



 

## <a name="propertytagexiflightsource"></a>PropertyTagExifLightSource

Tipo de fonte de luz.



Marca

0x9208

Type

PropertyTagTypeShort

Contagem

1

Padrão

0

0-desconhecido 1-horário de verão 2-flourescent 3-Tungsten 17-luz padrão de 18-padrão Light B 19 – luz padrão C 20-D55 21-D65 22-D75 23 a 254-reservado 255-outro



 

## <a name="propertytagexifflash"></a>PropertyTagExifFlash

Status do flash. Essa marca é registrada quando uma imagem é executada usando uma luz de estroboscópico (flash). O bit 0 indica o status de acionamento do flash, e os bits 1 e 2 indicam o status de retorno do flash.



Marca

0x9209

Type

PropertyTagTypeShort

Contagem

1

Valores para o bit 0 que indicam se o flash foi acionado: 0B-flash não disparou 1B-flash acionado

Valores para bits 1 e 2 que indicam o status da luz retornada: 00B-nenhuma função de detecção de retorno estroboscópico 01B-reservado 10B-sinal de retorno estroboscópico não detectado 11b-luz de retorno estroboscópico detectada

Valores de marca flash resultantes: 0x0000-flash não disparou 0x0001-flash disparado 0x0005-sinal de retorno estroboscópico não detectado



 

## <a name="propertytagexiffocallength"></a>PropertyTagExifFocalLength

O comprimento focal real, em milímetros, da lente. A conversão não é feita no comprimento focal de uma câmera de filme de 35 milímetros.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0x920A                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytagexifmakernote"></a>PropertyTagExifMakerNote

Marca de observação. Uma marca usada pelos fabricantes de gravadores EXIF para registrar informações. O conteúdo é para o fabricante.



| Informações da propriedade | Valor |
|-------|--------------------------|
| Marca   | 0x927C                   |
| Type  | PropertyTagTypeUndefined |
| Contagem | Qualquer                      |



 

## <a name="propertytagexifusercomment"></a>PropertyTagExifUserComment

Marca de comentário. Uma marca usada por usuários do EXIF para escrever palavras-chave ou comentários sobre a imagem além daquelas em PropertyTagImageDescription e sem as limitações de código de caractere da marca PropertyTagImageDescription.



| Informações da propriedade | Valor |
|-------|--------------------------|
| Marca   | 0x9286                   |
| Type  | PropertyTagTypeUndefined |
| Contagem | Qualquer                      |



 

O código de caractere usado na marca PropertyTagExifUserComment é identificado com base em um código de ID em uma área fixa de 8 bytes no início da área de dados da marca. A porção não utilizada da área é preenchida com caracteres nulos (0). Os códigos de ID são atribuídos por meio de registro. Como o tipo não é ASCII, não é necessário usar um terminador nulo.

## <a name="propertytagexifdtsubsec"></a>PropertyTagExifDTSubsec

Cadeia de caracteres terminada em nulo que especifica uma fração de um segundo para a marca PropertyTagDateTime.



| Informações da propriedade | Valor |
|-------|----------------------------------------------------|
| Marca   | 0x9290                                             |
| Type  | PropertyTagTypeASCII                               |
| Contagem | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytagexifdtorigss"></a>PropertyTagExifDTOrigSS

Cadeia de caracteres terminada em nulo que especifica uma fração de um segundo para a marca PropertyTagExifDTOrig.



| Informações da propriedade | Valor |
|------|----------------------------------------------------|
| Marca  | 0x9291                                             |
| Type | PropertyTagTypeASCII                               |
| N    | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytagexifdtdigss"></a>PropertyTagExifDTDigSS

Cadeia de caracteres terminada em nulo que especifica uma fração de um segundo para a marca PropertyTagExifDTDigitized.



| Informações da propriedade | Valor |
|------|----------------------------------------------------|
| Marca  | 0x9292                                             |
| Type | ASCII                                              |
| N    | Comprimento da cadeia de caracteres incluindo o terminador nulo |



 

## <a name="propertytagexiffpxver"></a>PropertyTagExifFPXVer

Versão de formato FlashPix com suporte por um arquivo FPXR. Se a função FPXR der suporte à versão de formato FlashPix 1,0, isso será indicado da mesma forma que o PropertyTagExifVer, gravando 0100 como uma cadeia de caracteres ASCII de 4 bytes. Como o tipo é PropertyTagTypeUndefined, não há nenhum terminador nulo.



Marca

0xA000

Type

PropertyTagTypeUndefined

Contagem

4

Padrão

0100

0100-formato FlashPix versão 1,0 outro – reservado



 

## <a name="propertytagexifcolorspace"></a>PropertyTagExifColorSpace

Especificador de espaço de cor. Normalmente, sRGB (= 1) é usado para definir o espaço de cores com base nas condições e no ambiente do monitor do PC. Se um espaço de cores diferente de sRGB for usado, não calibrado (= 0xFFFF) será definido. Os dados de imagem registrados como não calibrados podem ser tratados como sRGB quando convertidos em FlashPix.



Marca

0xA001

Type

PropertyTagTypeShort

Contagem

1

0x1-sRGB 0xFFFF-não calibrado-reservado



 

## <a name="propertytagexifpixxdim"></a>PropertyTagExifPixXDim

Informações específicas para dados compactados. Quando um arquivo compactado é registrado, a largura válida da imagem significativa deve ser registrada nessa marca, independentemente de haver ou não dados de preenchimento ou um marcador de reinicialização. Essa marca não deve existir em um arquivo descompactado.



| Informações da propriedade | Valor |
|-------|---------------------------------------------|
| Marca   | 0xA002                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Contagem | 1                                           |



 

## <a name="propertytagexifpixydim"></a>PropertyTagExifPixYDim

Informações específicas para dados compactados. Quando um arquivo compactado é registrado, a altura válida da imagem significativa deve ser registrada nessa marca se houver ou não dados de preenchimento ou um marcador de reinicialização. Essa marca não deve existir em um arquivo descompactado. Como o preenchimento de dados é desnecessário na direção vertical, o número de linhas registradas nessa marca de altura de imagem válida será o mesmo que o registrado no vers.



| Informações da propriedade | Valor |
|-------|---------------------------------------------|
| Marca   | 0xA003                                      |
| Type  | PropertyTagTypeShort ou PropertyTagTypeLong |
| Contagem | 1                                           |



 

## <a name="propertytagexifrelatedwav"></a>PropertyTagExifRelatedWav

O nome de um arquivo de áudio relacionado aos dados da imagem. As únicas informações relacionais registradas são o nome e a extensão do arquivo de áudio EXIF (uma cadeia de caracteres ASCII que consiste em 8 caracteres mais um ponto (.), mais 3 caracteres). O caminho não é registrado. Quando você usa essa marca, os arquivos de áudio devem ser registrados em conformidade com o formato de áudio EXIF. Os gravadores também podem armazenar dados de áudio dentro de APP2 como dados de fluxo de extensão FlashPix.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0xA004               |
| Type  | PropertyTagTypeASCII |
| Contagem | 13                   |



 

## <a name="propertytagexifinterop"></a>PropertyTagExifInterop

Deslocamento para um bloco de itens de propriedade que contêm informações de interoperabilidade.



| Informações da propriedade | Valor |
|-------|---------------------|
| Marca   | 0xA005              |
| Type  | PropertyTagTypeLong |
| Contagem | 1                   |



 

## <a name="propertytagexifflashenergy"></a>PropertyTagExifFlashEnergy

Energia de estroboscópico, no feixe de BCPS (alimentação de segundos), no momento em que a imagem foi capturada.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0xA20B                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytagexifspatialfr"></a>PropertyTagExifSpatialFR

Tabela de frequência espacial do dispositivo de entrada e câmera e valores de SFR na largura da imagem, na altura da imagem e na direção diagonal, conforme especificado no ISO 12233.



| Informações da propriedade | Valor |
|-------|--------------------------|
| Marca   | 0xA20C                   |
| Type  | PropertyTagTypeUndefined |
| Contagem | Qualquer                      |



 

## <a name="propertytagexiffocalxres"></a>PropertyTagExifFocalXRes

Número de pixels na direção da largura da imagem (x) por unidade no plano focal da câmera. A unidade é especificada em PropertyTagExifFocalResUnit.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0xA20E                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytagexiffocalyres"></a>PropertyTagExifFocalYRes

Número de pixels na direção da altura da imagem (y) por unidade no plano focal da câmera. A unidade é especificada em PropertyTagExifFocalResUnit.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0xA20F                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytagexiffocalresunit"></a>PropertyTagExifFocalResUnit

Unidade de medida para PropertyTagExifFocalXRes e PropertyTagExifFocalYRes.



Marca

0xA210

Type

PropertyTagTypeShort

Contagem

1

2 polegadas e 3 centímetros



 

## <a name="propertytagexifsubjectloc"></a>PropertyTagExifSubjectLoc

Local do assunto principal na cena. O valor dessa marca representa o pixel no centro do assunto principal relativo à borda esquerda. O primeiro valor indica o número da coluna e o segundo valor indica o número da linha.



| Informações da propriedade | Valor |
|-------|----------------------|
| Marca   | 0xA214               |
| Type  | PropertyTagTypeShort |
| Contagem | 2                    |



 

## <a name="propertytagexifexposureindex"></a>PropertyTagExifExposureIndex

Índice de exposição selecionado na câmera ou no dispositivo de entrada no momento em que a imagem foi capturada.



| Informações da propriedade | Valor |
|-------|-------------------------|
| Marca   | 0xA215                  |
| Type  | PropertyTagTypeRational |
| Contagem | 1                       |



 

## <a name="propertytagexifsensingmethod"></a>PropertyTagExifSensingMethod

Tipo de sensor de imagem na câmera ou no dispositivo de entrada.



Marca

0xA217

Type

PropertyTagTypeShort

Contagem

1

1-não definido 2 – sensor de área de cor de um chip 3-dois-chips sensor de área de cores 4-três chips sensor de área de cores 5-cor sequencial de área do sensor 7-triline sensor linear de cor outro-reservado



 

## <a name="propertytagexiffilesource"></a>PropertyTagExifFileSource

A origem da imagem. Se uma DSC registrou a imagem, o valor dessa marca será 3.



| Informações da propriedade | Valor |
|-------|--------------------------|
| Marca   | 0xA300                   |
| Type  | PropertyTagTypeUndefined |
| Contagem | 1                        |



 

## <a name="propertytagexifscenetype"></a>PropertyTagExifSceneType

O tipo de cena. Se uma DSC registrou a imagem, o valor dessa marca deverá ser definido como 1, indicando que a imagem foi fotografada diretamente.



| Informações da propriedade | Valor |
|-------|--------------------------|
| Marca   | 0xA301                   |
| Type  | PropertyTagTypeUndefined |
| Contagem | 1                        |



 

## <a name="propertytagexifcfapattern"></a>PropertyTagExifCfaPattern

O padrão geométrico da matriz de filtro de cor (CFA) do sensor de imagem quando um sensor de área de cor de um chip é usado. Ele não se aplica a todos os métodos de detecção.



| Informações da propriedade | Valor |
|-------|--------------------------|
| Marca   | 0xA302                   |
| Type  | PropertyTagTypeUndefined |
| Contagem | Qualquer                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificações de formato de arquivo de imagem](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[Constantes de marca de propriedade de imagem](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[**Constantes de tipo de marca de propriedade de imagem**](-gdiplus-constant-image-property-tag-type-constants.md)
</dt> <dt>

[Marcas de propriedade em ordem alfabética](-gdiplus-constant-property-tags-in-alphabetical-order.md)
</dt> <dt>

[Marcas de propriedade em ordem numérica](-gdiplus-constant-property-tags-in-numerical-order.md)
</dt> <dt>

[Lendo e gravando metadados](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 



