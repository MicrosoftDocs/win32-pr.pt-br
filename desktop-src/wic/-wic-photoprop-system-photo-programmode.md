---
description: A política de metadados de foto para a propriedade System. Photo. programmode.
ms.assetid: f1954dc7-d4df-4675-ab3b-a65f2354e57a
title: Política de metadados de foto System. Photo. programmode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f5dffa822454509134c485e4792f4be4270912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922345"
---
# <a name="systemphotoprogrammode-photo-metadata-policy"></a>Política de metadados de foto System. Photo. programmode

A política de metadados de foto para a propriedade [System. Photo. programmode](../properties/props-system-photo-programmode.md) .

### <a name="pkey"></a>PKEY

\_Programa de foto PKEY \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

\_UI4 VT

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 34850} | ushort      |
| 2     | /xmp/exif:ExposureProgram     | Unicode     |
| 3     | /XMP/EXIF: programmode         | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 34850} | ushort      |
| 2     | /xmp/exif:ExposureProgram     | Unicode     |
| 3     | /XMP/EXIF: programmode         | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 34850} |
| 2     | /xmp/exif:exposureprogram     |
| 3     | /XMP/EXIF: programmode         |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 34850}      | ushort      |
| 2     | /ifd/xmp/exif:ExposureProgram | Unicode     |
| 3     | /IFD/XMP/EXIF: programmode     | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 34850}      | ushort      |
| 2     | /ifd/xmp/exif:ExposureProgram | Unicode     |
| 3     | /IFD/XMP/EXIF: programmode     | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /IFD/EXIF/{UShort = 34850}      |
| 2     | /ifd/xmp/exif:exposureprogram |
| 3     | /IFD/XMP/EXIF: programmode     |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. programmode](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
