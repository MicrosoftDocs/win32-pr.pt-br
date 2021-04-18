---
description: A política de metadados de foto para a propriedade System. GPS. Track.
ms.assetid: ac9e14a0-55f1-437e-9d27-df0fa09671c1
title: Política de metadados de foto System. GPS. Track
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 773c65eec8b165c51456f3871309644638c1e2da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764562"
---
# <a name="systemgpstrack-photo-metadata-policy"></a>Política de metadados de foto System. GPS. Track

A política de metadados de foto para a propriedade [System. GPS. Track](../properties/props-system-gps-track.md) .

### <a name="pkey"></a>PKEY

\_Faixa de GPS PKEY \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Yes

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

R8 de VT \_

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Esse valor é gerado de System. GPS. TrackNumerator e System. GPS. TrackDenominator. Ele não pode ser gravado diretamente. Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 15} |             |
| 2     | /xmp/exif:GPSTrack        |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 15} |             |
| 2     | /xmp/exif:GPSTrack        |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{UShort = 15} |
| 2     | /xmp/exif:gpstrack        |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 15}   |             |
| 2     | /ifd/xmp/exif:GPSTrack |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 15}   |             |
| 2     | /ifd/xmp/exif:GPSTrack |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                   |
|-------|------------------------|
| 1     | /IFD/GPS/{UShort = 15}   |
| 2     | /ifd/xmp/exif:gpstrack |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema. GPS. Track](../properties/props-system-gps-track.md)
</dt> </dl>

 

 
