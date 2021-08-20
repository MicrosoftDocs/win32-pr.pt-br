---
description: A política de metadados de foto para a propriedade System.GPS.AltitudeRef.
ms.assetid: abbb2441-25ca-484b-a744-620ff2794221
title: Política de metadados de foto System.GPS.AltitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca49213754f605dcf6df40dfa3ff00e2b7aeaf765008037c23da21e35ab9ddee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710693"
---
# <a name="systemgpsaltituderef-photo-metadata-policy"></a>Política de metadados de foto System.GPS.AltitudeRef

A política de metadados de foto para a [propriedade System.GPS.AltitudeRef.](../properties/props-system-gps-altituderef.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ AltitudeRef

### <a name="description"></a>Descrição

Indica a altitude usada como a altitude de referência. Um valor de 0 indica que a altitude está acima do nível do mar. Um valor de 1 indica uma altitude abaixo do nível do mar.

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ UI1

### <a name="input-type"></a>Tipo de entrada

Byte.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policies"></a>Políticas JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=5} | byte        |
| 2     | /xmp/exif:GPSAltitudeRef | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=5} | byte        |
| 2     | /xmp/exif:GPSAltitudeRef | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=5} |
| 2     | /xmp/exif:gpsaltituderef |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort=5}          | byte        |
| 2     | /ifd/xmp/exif:GPSAltitudeRef | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort=5}          | byte        |
| 2     | /ifd/xmp/exif:GPSAltitudeRef | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                         |
|-------|------------------------------|
| 1     | /ifd/gps/{ushort=5}          |
| 2     | /ifd/xmp/exif:gpsaltituderef |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.GPS.AltitudeRef](../properties/props-system-gps-altituderef.md)
</dt> </dl>

 

 
