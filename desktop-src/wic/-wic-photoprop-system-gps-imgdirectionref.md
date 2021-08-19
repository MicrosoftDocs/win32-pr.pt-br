---
description: A política de metadados de foto para a propriedade System.GPS.ImgDirectionRef.
ms.assetid: 74ae0989-6d53-4d72-abe9-84f40c0c884a
title: Política de metadados de foto System.GPS.ImgDirectionRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e735f91133d4ec473537f063e30d2d48f801a99f8f6bc80fa228b98a9bd95437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667893"
---
# <a name="systemgpsimgdirectionref-photo-metadata-policy"></a>Política de metadados de foto System.GPS.ImgDirectionRef

A política de metadados de foto para a [propriedade System.GPS.ImgDirectionRef.](../properties/props-system-gps-imgdirectionref.md)

### <a name="pkey"></a>Pkey

\_GPS PKEY. ImgDirectionRef

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

O VT \_ LPWSTR é preferencial, mas o VT \_ LPSTR também é aceito.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policies"></a>Políticas JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=16}    | ascii       |
| 2     | /xmp/exif:GPSImgDirectionRef | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=16}    | ascii       |
| 2     | /xmp/exif:GPSImgDirectionRef | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                         |
|-------|------------------------------|
| 1     | /app1/ifd/gps/{ushort=16}    |
| 2     | /xmp/exif:gpsimgdirectionref |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort=16}             | ascii       |
| 2     | /ifd/xmp/exif:GPSImgDirectionRef | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort=16}             | ascii       |
| 2     | /ifd/xmp/exif:GPSImgDirectionRef | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                             |
|-------|----------------------------------|
| 1     | /ifd/gps/{ushort=16}             |
| 2     | /ifd/xmp/exif:gpsimgdirectionref |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.GPS.ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md)
</dt> </dl>

 

 
