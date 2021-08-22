---
description: A política de metadados de foto para a propriedade System. GPS. longitude.
ms.assetid: 36539e20-d00c-4bbb-b9ee-1cf5e4b8df4b
title: Política de metadados de foto System. GPS. longitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff05dd8ada6e10bbd3109187d34b220ff352ae984f92bd68281c56d3c1a29a76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087183"
---
# <a name="systemgpslongitude-photo-metadata-policy"></a>Política de metadados de foto System. GPS. longitude

A política de metadados de foto para a propriedade [System. GPS. longitude](../properties/props-system-gps-longitude.md) .

### <a name="pkey"></a>PKEY

\_Longitude de GPS PKEY \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Sim

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

\_R8 de \| VT de vetor VT \_

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Esse valor pode ser gravado escrevendo em System. GPS. LongitudeNumerator e System. GPS. LongitudeDenominator. Ele não pode ser gravado diretamente. Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 4} |             |
| 2     | /xmp/exif:GPSLongitude   |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 4} |             |
| 2     | /xmp/exif:GPSLongitude   |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{UShort = 4} |
| 2     | /xmp/exif:gpslongitude   |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 4}        |             |
| 2     | /ifd/xmp/exif:GPSLongitude |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 4}        |             |
| 2     | /ifd/xmp/exif:GPSLongitude |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                       |
|-------|----------------------------|
| 1     | /IFD/GPS/{UShort = 4}        |
| 2     | /ifd/xmp/exif:gpslongitude |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. longitude](../properties/props-system-gps-longitude.md)
</dt> </dl>

 

 
