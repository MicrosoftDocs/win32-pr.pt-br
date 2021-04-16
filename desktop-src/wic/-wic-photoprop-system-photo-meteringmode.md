---
description: A política de metadados de foto para a propriedade System. Photo. MeteringMode.
ms.assetid: cb0bf0d5-eccf-4345-a242-76769c34e02d
title: Política de metadados de foto System. Photo. MeteringMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12a4443521c84113e4e2a6f4c2b9b2b3f822ae90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759271"
---
# <a name="systemphotometeringmode-photo-metadata-policy"></a>Política de metadados de foto System. Photo. MeteringMode

A política de metadados de foto para a propriedade [System. Photo. MeteringMode](../properties/props-system-photo-meteringmode.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ MeteringMode

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

\_UI2 VT

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37383} | ushort      |
| 2     | /xmp/exif:MeteringMode        | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37383} | ushort      |
| 2     | /xmp/exif:MeteringMode        | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37383} |
| 2     | /xmp/exif:meteringmode        |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37383}   | ushort      |
| 2     | /ifd/xmp/exif:MeteringMode | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37383}   | ushort      |
| 2     | /ifd/xmp/exif:MeteringMode | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                       |
|-------|----------------------------|
| 1     | /IFD/EXIF/{UShort = 37383}   |
| 2     | /ifd/xmp/exif:meteringmode |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. MeteringMode](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
