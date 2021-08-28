---
description: A política de metadados de foto para a propriedade System. Photo. DateTaken.
ms.assetid: 800aa01b-6064-45df-a40e-6537819df4d7
title: Política de metadados de foto System. Photo. DateTaken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691476c704d3fdbc4ff5e01467031f2b41884ccb16be537904484a9d01c8fa18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087072"
---
# <a name="systemphotodatetaken-photo-metadata-policy"></a>Política de metadados de foto System. Photo. DateTaken

A política de metadados de foto para a propriedade [System. Photo. DateTaken](../properties/props-system-photo-datetaken.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ DateTaken

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

FILETIME do VT \_

### <a name="input-type"></a>Tipo de entrada

Datetime

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                                  | Formato de disco |
|-------|---------------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 36867}         | ascii       |
| 2     | /app13/IRB/8bimiptc/IPTC/Date criado | Unicode     |
| 3     | /XMP/XMP: CreateDate                   | Unicode     |
| 4     | /App1/IFD/EXIF/{UShort = 36868}         | ascii       |
| 5     | /app13/IRB/8bimiptc/IPTC/Date criado | Unicode     |
| 6     | /xmp/exif:DateTimeOriginal            | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                                  | Formato de disco |
|-------|---------------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 36867}         | ascii       |
| 2     | /app13/IRB/8bimiptc/IPTC/Date criado | Unicode     |
| 3     | /XMP/XMP: CreateDate                   | Unicode     |
| 4     | /App1/IFD/EXIF/{UShort = 36868}         | ascii       |
| 5     | /xmp/exif:DateTimeOriginal            | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                                  |
|-------|---------------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 36867}         |
| 2     | /App1/IFD/EXIF/{UShort = 37521}         |
| 3     | /App1/IFD/EXIF/{UShort = 36868}         |
| 4     | /App1/IFD/EXIF/{UShort = 37522}         |
| 5     | /xmp/exif:DateTimeOriginal            |
| 6     | /XMP/XMP: CreateDate                   |
| 7     | /app13/IRB/8bimiptc/IPTC/Date criado |
| 8     | /app13/IRB/8bimiptc/IPTC/time criado |



 

### <a name="tiff-policy"></a>Política TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                                | Formato de disco |
|-------|-------------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 36867}            | ascii       |
| 2     | /IFD/IPTC/Date criado              | Unicode     |
| 3     | /IFD/XMP/XMP: CreateDate             | Unicode     |
| 4     | /IFD/EXIF/{UShort = 36868}            | ascii       |
| 5     | /IFD/IPTC/Date criado              | Unicode     |
| 6     | /IFD/IRB/8bimiptc/IPTC/Date criado | Unicode     |
| 7     | /ifd/xmp/exif:DateTimeOriginal      | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                                | Formato de disco |
|-------|-------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=36867}            | ascii       |
| 2     | /ifd/iptc/date criado              | Unicode     |
| 3     | /ifd/xmp/xmp:CreateDate             | Unicode     |
| 4     | /ifd/exif/{ushort=36868}            | ascii       |
| 5     | /ifd/irb/8bimiptc/iptc/date criado | Unicode     |
| 6     | /ifd/xmp/exif:DateTimeOriginal      | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                                |
|-------|-------------------------------------|
| 1     | /ifd/exif/{ushort=36867}            |
| 2     | /ifd/exif/{ushort=37521}            |
| 3     | /ifd/exif/{ushort=36868}            |
| 4     | /ifd/exif/{ushort=37522}            |
| 5     | /ifd/xmp/exif:DateTimeOriginal      |
| 6     | /ifd/xmp/xmp:CreateDate             |
| 7     | /ifd/iptc/date criado              |
| 8     | /ifd/iptc/time criado              |
| 9     | /ifd/irb/8bimiptc/iptc/date criado |
| 10    | /ifd/irb/8bimiptc/iptc/time criado |



 

### <a name="png-policy"></a>Política PNG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /\[\*\]tEXt/Hora de criação | ascii       |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 2     | /\[\*\]tEXt/Hora de criação | ascii       |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 3     | /\[\*\]tEXt/Hora de criação |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Photo.DateTaken](../properties/props-system-photo-datetaken.md)
</dt> </dl>

 

 
