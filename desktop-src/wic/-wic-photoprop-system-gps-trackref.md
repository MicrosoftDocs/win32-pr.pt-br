---
description: A política de metadados de foto para a propriedade System.GPS.TrackRef.
ms.assetid: e6912177-8add-4520-b396-c28060b359c7
title: Política de metadados de foto System.GPS.TrackRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a523f801b8e82fc4191b54bf0bb5fee659ab4f5b09c326d5d1adf14c713f13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087174"
---
# <a name="systemgpstrackref-photo-metadata-policy"></a>Política de metadados de foto System.GPS.TrackRef

A política de metadados de foto para a [propriedade System.GPS.TrackRef.](../properties/props-system-gps-trackref.md)

### <a name="pkey"></a>Pkey

TrackRef \_ do GPS \_ PKEY

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

String

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policies"></a>Políticas JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=14} | ascii       |
| 2     | /xmp/exif:GPSTrackRef     | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=14} | ascii       |
| 2     | /xmp/exif:GPSTrackRef     | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=14} |
| 2     | /xmp/exif:gpstrackref     |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=14}      | ascii       |
| 2     | /ifd/xmp/exif:GPSTrackRef | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=14}      | ascii       |
| 2     | /ifd/xmp/exif:GPSTrackRef | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /ifd/gps/{ushort=14}      |
| 2     | /ifd/xmp/exif:gpstrackref |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.GPS.TrackRef](../properties/props-system-gps-trackref.md)
</dt> </dl>

 

 
