---
description: A política de metadados de foto para a propriedade System.GPS.DestLongitude.
ms.assetid: 885a522d-e1bf-43fb-a996-97e725b6cf0c
title: Política de metadados de foto System.GPS.DestLongitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 917c65dbd580b00cf25603e04050386383967e3a70c1896405346652667ef5f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087837"
---
# <a name="systemgpsdestlongitude-photo-metadata-policy"></a>Política de metadados de foto System.GPS.DestLongitude

A política de metadados de foto para a [propriedade System.GPS.DestLongitude.](../properties/props-system-gps-destlongitude.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ DestLongitude

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Sim

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ VECTOR \| VT \_ R8

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

VT \_ VECTOR \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Esse valor é gerado de System.GPS.DestLongitudeNumerator e System.GPS.DestLongitudeDenominator. Ele não pode ser gravado diretamente. Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=22}  |             |
| 2     | /xmp/exif:GPSDestLongitude |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=22}  |             |
| 2     | /xmp/exif:GPSDestLongitude |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                       |
|-------|----------------------------|
| 1     | /app1/ifd/gps/{ushort=22}  |
| 2     | /xmp/exif:gpsdestlongitude |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /ifd/gps/{ushort=22}           |             |
| 2     | /ifd/xmp/exif:GPSDestLongitude |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /ifd/gps/{ushort=22}           |             |
| 2     | /ifd/xmp/exif:GPSDestLongitude |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                           |
|-------|--------------------------------|
| 1     | /ifd/gps/{ushort=22}           |
| 2     | /ifd/xmp/exif:gpsdestlongitude |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.GPS.DestLongitude](../properties/props-system-gps-destlongitude.md)
</dt> </dl>

 

 
