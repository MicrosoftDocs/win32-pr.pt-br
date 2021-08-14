---
description: A política de metadados de foto para a propriedade System.GPS.Latitude.
ms.assetid: 0f8cea07-da96-4d2a-8444-6073b51e1236
title: Política de metadados de foto System.GPS.Latitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41dd1eb0ee21ab02eeb8c83d5ea84f28c07c2811929f2b8c973cace4a4a06fd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710620"
---
# <a name="systemgpslatitude-photo-metadata-policy"></a>Política de metadados de foto System.GPS.Latitude

A política de metadados de foto para a [propriedade System.GPS.Latitude.](../properties/props-system-gps-latitude.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ Latitude

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Sim

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ VECTOR \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Esse valor pode ser escrito escrevendo em System.GPS.LatitudeNumerator e System.GPS.LatitudeDenominator. Ele não pode ser gravado diretamente. Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=2} |             |
| 2     | /xmp/exif:GPSLatitude    |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=2} |             |
| 2     | /xmp/exif:GPSLatitude    |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=2} |
| 2     | /xmp/exif:gpslatitude    |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=2}       |             |
| 2     | /ifd/xmp/exif:GPSLatitude |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=2}       |             |
| 2     | /ifd/xmp/exif:GPSLatitude |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /ifd/gps/{ushort=2}       |
| 2     | /ifd/xmp/exif:gpslatitude |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.GPS.Latitude](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
