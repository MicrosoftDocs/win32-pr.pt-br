---
description: A política de metadados de foto para a propriedade System.GPS.Altitude.
ms.assetid: 63d59aa3-52a6-4b6f-b6ec-a1c4abcee83f
title: Política de metadados de foto System.GPS.Altitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40a9209bfb0bbc1a4c6f95ce4a995d32d3f532c293dd2295c335eea61c22df89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441996"
---
# <a name="systemgpsaltitude-photo-metadata-policy"></a>Política de metadados de foto System.GPS.Altitude

A política de metadados de foto para a [propriedade System.GPS.Altitude.](../properties/props-system-gps-altitude.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ Altitude

### <a name="description"></a>Descrição

A altitude é indicada como um valor absoluto referenciado em metros.

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Sim

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ R8

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

VT \_ R8

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Esse valor pode ser escrito escrevendo em System.GPS.Altitude.Numerator e System.GPS.Altitude.Denominator. Ele não pode ser gravado diretamente. Os caminhos de gravação nas tabelas a seguir indicam onde o valor pode ser salvo quando ele é gerado, não quando ele é gravado diretamente. Quando o valor é lido, os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=6} |             |
| 2     | /xmp/exif:GPSAltitude    |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=6} |             |
| 2     | /xmp/exif:GPSAltitude    |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=6} |
| 2     | /xmp/exif:gpsaltitude    |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=6}       |             |
| 2     | /ifd/xmp/exif:GPSAltitude |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=6}       |             |
| 2     | /ifd/xmp/exif:GPSAltitude |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |     |
|-------|---------------------------|-----|
| 1     | /ifd/gps/{ushort=6}       |     |
| 2     | /ifd/xmp/exif:gpsaltitude |     |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.GPS.Altitude](../properties/props-system-gps-altitude.md)
</dt> </dl>

 

 
