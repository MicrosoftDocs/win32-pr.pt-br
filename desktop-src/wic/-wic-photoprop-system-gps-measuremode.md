---
description: A política de metadados de foto para a propriedade System.GPS.MeasureMode.
ms.assetid: 911a0d81-bd12-4155-b45a-ae1a18f2dd07
title: Política de metadados de foto System.GPS.MeasureMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827cd278a71b23934fb0475e78d98b25a9f2b72d413b70f9abc60ba3dbe2c3fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882316"
---
# <a name="systemgpsmeasuremode-photo-metadata-policy"></a>Política de metadados de foto System.GPS.MeasureMode

A política de metadados de foto para a [propriedade System.GPS.MeasureMode.](../properties/props-system-gps-measuremode.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ MeasureMode

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



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=10} | ascii       |
| 2     | /xmp/exif:GPSMeasureMode  | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=10} | ascii       |
| 2     | /xmp/exif:GPSMeasureMode  | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=10} |
| 2     | /xmp/exif:gpsmeasuremode  |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort=10}         | ascii       |
| 2     | /ifd/xmp/exif:GPSMeasureMode | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort=10}         | ascii       |
| 2     | /ifd/xmp/exif:GPSMeasureMode | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                         |
|-------|------------------------------|
| 1     | /ifd/gps/{ushort=10}         |
| 2     | /ifd/xmp/exif:gpsmeasuremode |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.GPS.MeasureMode](../properties/props-system-gps-measuremode.md)
</dt> </dl>

 

 
