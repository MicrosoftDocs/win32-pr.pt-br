---
description: A política de metadados de foto para a propriedade System.GPS.ProcessingMethod.
ms.assetid: 840021a8-ec1d-4916-93b2-7cc1803e2d8c
title: System.GPS.ProcessingMethod Photo Metadata Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800515d3a7870fa2dc9b5a6ec8c19178889482fa820f66d7d98e8e3ff09870f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931736"
---
# <a name="systemgpsprocessingmethod-photo-metadata-policy"></a>System.GPS.ProcessingMethod Photo Metadata Policy

A política de metadados de foto [para a propriedade System.GPS.ProcessingMethod.](../properties/props-system-gps-processingmethod.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ ProcessingMethod

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

O VT \_ LPWSTR é preferencial, mas o VT \_ LPSTR também é aceito.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policies"></a>Políticas JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=27}     |             |
| 2     | /xmp/exif:GPSProcessingMethod | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=27}     |             |
| 2     | /xmp/exif:GPSProcessingMethod | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /app1/ifd/gps/{ushort=27}     |
| 2     | /xmp/exif:gpsprocessingmethod |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                              | Formato de disco |
|-------|-----------------------------------|-------------|
| 1     | /ifd/xmp/exif:GPSProcessingMethod | Unicode     |
| 2     | /ifd/gps/{ushort=27}              |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                              | Formato de disco |
|-------|-----------------------------------|-------------|
| 1     | /ifd/xmp/exif:GPSProcessingMethod | Unicode     |
| 2     | /ifd/gps/{ushort=27}              |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                              |
|-------|-----------------------------------|
| 1     | /ifd/xmp/exif:gpsprocessingmethod |
| 2     | /ifd/gps/{ushort=27}              |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.GPS.ProcessingMethod](../properties/props-system-gps-processingmethod.md)
</dt> </dl>

 

 
