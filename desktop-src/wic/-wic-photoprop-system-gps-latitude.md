---
description: A política de metadados de foto para a propriedade System. GPS. latitude.
ms.assetid: 0f8cea07-da96-4d2a-8444-6073b51e1236
title: Política de metadados de foto System. GPS. latitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41dd1eb0ee21ab02eeb8c83d5ea84f28c07c2811929f2b8c973cace4a4a06fd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710620"
---
# <a name="systemgpslatitude-photo-metadata-policy"></a>Política de metadados de foto System. GPS. latitude

A política de metadados de foto para a propriedade [System. GPS. latitude](../properties/props-system-gps-latitude.md) .

### <a name="pkey"></a>PKEY

\_Latitude PKEY GPS \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Sim

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

\_R8 de \| VT de vetor VT \_

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Esse valor pode ser gravado escrevendo em System. GPS. LatitudeNumerator e System. GPS. LatitudeDenominator. Ele não pode ser gravado diretamente. Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 2} |             |
| 2     | /xmp/exif:GPSLatitude    |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 2} |             |
| 2     | /xmp/exif:GPSLatitude    |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{UShort = 2} |
| 2     | /xmp/exif:gpslatitude    |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 2}       |             |
| 2     | /ifd/xmp/exif:GPSLatitude |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 2}       |             |
| 2     | /ifd/xmp/exif:GPSLatitude |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /IFD/GPS/{UShort = 2}       |
| 2     | /ifd/xmp/exif:gpslatitude |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. latitude](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
