---
description: A política de metadados de foto para a propriedade System.GPS.ImgDirection.
ms.assetid: c9a0f5de-4010-4251-a5d5-8728b7ae6d33
title: Política de metadados de foto System.GPS.ImgDirection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43544458c4b6a64df1d396426ebbe487d80324d24dd10c2f8f6f0e548d9eca99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710666"
---
# <a name="systemgpsimgdirection-photo-metadata-policy"></a>Política de metadados de foto System.GPS.ImgDirection

A política de metadados de foto para a [propriedade System.GPS.ImgDirection.](../properties/props-system-gps-imgdirection.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ ImgDirection

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Sim

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ R8

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Esse valor pode ser escrito escrevendo em System.GPS.ImgDirectionNumerator e System.GPS.ImgDirectionDenominator. Ele não pode ser gravado diretamente. Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=17} |             |
| 2     | /xmp/exif:GPSImgDirection |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=17} |             |
| 2     | /xmp/exif:GPSImgDirection |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=17} |
| 2     | /xmp/exif:gpsimgdirection |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=17}          |             |
| 2     | /ifd/xmp/exif:GPSImgDirection |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=17}          |             |
| 2     | /ifd/xmp/exif:GPSImgDirection |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /ifd/gps/{ushort=17}          |
| 2     | /ifd/xmp/exif:gpsimgdirection |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.GPS.ImgDirection](../properties/props-system-gps-imgdirection.md)
</dt> </dl>

 

 
